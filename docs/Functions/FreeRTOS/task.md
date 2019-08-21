# タスク(task)

マルチタスク系の関数群。

## メンバー

### コア指定タスク作成 xTaskCreatePinnedToCore()
xTaskCreate()関数はCPUコアの指定ができませんので、こちらを利用します。ほぼ同じ動きで、指定したCPUコア番号でxTaskCreatePinnedToCore()とxTaskCreate()を呼び分けるxTaskCreateUniversal()も存在しています。

ウォッチドッグが動いているCPUコアで動かすタスクはdelay(1)などを定期的の呼び出してください。

```c
BaseType_t xTaskCreatePinnedToCore(TaskFunction_t pvTaskCode, const char *const pcName, const uint32_t usStackDepth, void *const pvParameters, UBaseType_t uxPriority, TaskHandle_t *const pvCreatedTask, const BaseType_t xCoreID)
```

!!! summary "引数"
	- TaskFunction_t `pvTaskCode` タスク関数へのポインタ。無限ループで終了しないよう関数を指定します
	- const char *const `pcName` タスクの説明用名前。重複しても動きますがデバッグ用途。最大16文字まで
	- const uint32_t `usStackDepth` スタックサイズ(Byte)
	- void *const `pvParameters` 作成タスクのパラメータのポインタ
	- UBaseType_t `uxPriority` 作成タスクの優先順位(0:低 - 25:高)
	- TaskHandle_t * const `pvCreatedTask` 作成タスクのHandleへのポインタ
	- BaseType_tconst `xCoreID` 利用するCPUコア(0-1)

!!! note "戻り値"
	BaseType_t 実行結果

!!! Tip "利用例"
	```c
	TaskHandle_t taskHandle[2];

	void testTask(void *pvParameters) {
	  while (1) {
	    Serial.print( xPortGetCoreID() ); // 動作確認用出力
	    vPortYield();                     // vPortYield()ではウォッチドッグに影響しない
	    yield();                          // yield()ではウォッチドッグに影響しない
	    delay(1);                         // 1以上にするとウォッチドッグのリセットがなくなる
	    delayMicroseconds(1000000);       // delayMicroseconds()はウォッチドッグとは関係ない単なるウエイト
	  }
	}

	void setup() {
	  Serial.begin(115200);

	  // Core0でタスク起動
	  xTaskCreatePinnedToCore(
	    testTask,
	    "testTask1",
	    8192,
	    NULL,
	    1,
	    &taskHandle[0],
	    0
	  );

	  // Core1でタスク起動
	  xTaskCreatePinnedToCore(
	    testTask,
	    "testTask2",
	    8192,
	    NULL,
	    1,
	    &taskHandle[1],
	    1
	  );

	  // ウォッチドッグ停止
	  //disableCore0WDT();
	  //disableCore1WDT();  // 起動直後は有効化されていないのでエラーがでる

	  // ウォッチドッグ起動
	  //enableCore0WDT();
	  //enableCore1WDT();
	}

	void loop() {
	}
	```

### タスク作成 xTaskCreate()
xTaskCreatePinnedToCore()関数のxCoreIDが0に設定されている関数です。過去との互換性のために存在。

```c
static IRAM_ATTR BaseType_t xTaskCreate(TaskFunction_t pvTaskCode, const char *const pcName, const uint32_t usStackDepth, void *const pvParameters, UBaseType_t uxPriority, TaskHandle_t *const pvCreatedTask)
```

!!! summary "引数"
	- TaskFunction_t `pvTaskCode` タスク関数へのポインタ。無限ループで終了しないよう関数を指定します
	- const char *const `pcName` タスクの説明用名前。重複しても動きますがデバッグ用途。最大16文字まで
	- const uint32_t `usStackDepth` スタックサイズ(Byte)
	- void *const `pvParameters` 作成タスクのパラメータのポインタ
	- UBaseType_t `uxPriority` 作成タスクの優先順位(0:低 - 25:高)
	- TaskHandle_t * const `pvCreatedTask` 作成タスクのHandleへのポインタ

!!! note "戻り値"
	BaseType_tIRAM_ATTR

### コア指定タスク作成 xTaskCreateUniversal()
指定したCPUコア番号でxTaskCreatePinnedToCore()とxTaskCreate()を呼び分けます。一般的ではない関数なのでxTaskCreatePinnedToCore()を使った方が無難です。

```c
BaseType_t xTaskCreateUniversal(TaskFunction_t pvTaskCode, const char *const pcName, const uint32_t usStackDepth, void *const pvParameters, UBaseType_t uxPriority, TaskHandle_t *const pvCreatedTask, const BaseType_t xCoreID)
```

!!! summary "引数"
	- TaskFunction_t `pvTaskCode` タスク関数へのポインタ。無限ループで終了しないよう関数を指定します
	- const char *const `pcName` タスクの説明用名前。重複しても動きますがデバッグ用途。最大16文字まで
	- const uint32_t `usStackDepth` スタックサイズ(Byte)
	- void *const `pvParameters` 作成タスクのパラメータのポインタ
	- UBaseType_t `uxPriority` 作成タスクの優先順位(0:低 - 25:高)
	- TaskHandle_t * const `pvCreatedTask` 作成タスクのHandleへのポインタ
	- BaseType_tconst `xCoreID` 利用するCPUコア(0-1)

!!! note "戻り値"
	BaseType_t 実行結果

### タスク削除 vTaskDelete()
タスクを削除します。

```c
void vTaskDelete(TaskHandle_t xTaskToDelete) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TaskHandle_t `xTaskToDelete` タスクハンドル。NULLを指定すると呼び出し元タスクが指定

!!! Tip "利用例"
	```c
	TaskHandle_t taskHandle[2];

	void testTask(void *pvParameters) {
	  while (1) {
	    Serial.print( xPortGetCoreID() ); // 動作確認用出力
	    delay(1000);
	  }
	}

	void testTask2(void *pvParameters) {
	  for( int i = 0 ; i < 5 ; i++ ) {
	    Serial.print( xPortGetCoreID() ); // 動作確認用出力
	    delay(1000);
	  }

	  // 基本的には無限ループにするが、完了するときにはタスクを削除する
	  vTaskDelete(NULL);
	}

	void setup() {
	  Serial.begin(115200);

	  // Core0でタスク起動
	  xTaskCreatePinnedToCore(
	    testTask,
	    "testTask1",
	    8192,
	    NULL,
	    1,
	    &taskHandle[0],
	    0
	  );

	  // Core1でタスク起動
	  xTaskCreatePinnedToCore(
	    testTask2,
	    "testTask2",
	    8192,
	    NULL,
	    1,
	    &taskHandle[1],
	    1
	  );

	  // 10秒後にtestTaskを削除
	  delay(10000);
	  vTaskDelete(taskHandle[0]);
	}

	void loop() {
	}
	```

### タスクディレイ vTaskDelay()
タスクの実行を一時停止して、他のタスクを実行します。
実時間ではなくCPUのTick数で指定するので、通常は内部でvTaskDelay()を呼び出しているdelay()関数を利用しましょう。

```c
void vTaskDelay(const TickType_t xTicksToDelay) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TickType_tconst `xTicksToDelay` ブロックを解除するTick数


### 時間指定タスクディレイ vTaskDelayUntil()
タスクの実行を一時停止して、他のタスクを実行します。
portTICK_PERIOD_MS定数を利用して実時間を指定できますが、通常は内部でvTaskDelay()を呼び出しているdelay()関数を利用しましょう。
```c
void vTaskDelayUntil(TickType_t *const pxPreviousWakeTime, const TickType_t xTimeIncrement) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TickType_t*const `pxPreviousWakeTime` 最後にブロックが解除された時間を保存する変数のポインタ
	- TickType_tconst `xTimeIncrement` サイクル時間

### 優先順位取得 uxTaskPriorityGet()
タスクの優先順位を取得します。
```c
UBaseType_t uxTaskPriorityGet(TaskHandle_t xTask) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TaskHandle_t `xTask` タスクハンドル。NULLを指定すると呼び出し元タスクが指定

!!! note "戻り値"
	UBaseType_t 優先順位

### 割り込み優先順位取得 uxTaskPriorityGetFromISR()
ISR(割り込み)から利用できる優先順位の取得です。

```c
UBaseType_t uxTaskPriorityGetFromISR(TaskHandle_t xTask) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TaskHandle_t `xTask` タスクハンドル。NULLを指定すると呼び出し元タスクが指定

!!! note "戻り値"
	UBaseType_t 優先順位

### タスク状態取得 eTaskGetState()
タスクの状態を取得します。

```c
eTaskState eTaskGetState(TaskHandle_t xTask) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TaskHandle_t `xTask` タスクハンドル。NULLは許容しません

!!! note "戻り値"
	eTaskState 状態(eRunning:0, eReady:1, eBlocked:2, eSuspended:3, eDeleted:4)

### タスク優先順位設定 vTaskPrioritySet()


A context switch will occur before the function returns if the priority being set is higher than the currently executing task.
```c
void vTaskPrioritySet(TaskHandle_t xTask, UBaseType_t uxNewPriority) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TaskHandle_t `xTask` タスクハンドル。NULLを指定すると呼び出し元タスクが指定
	- UBaseType_t `uxNewPriority` 新しい優先順位


### タスクサスペンド vTaskSuspend()
タスクを停止させます。

```c
void vTaskSuspend(TaskHandle_t xTaskToSuspend) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TaskHandle_t `xTaskToSuspend` タスクハンドル。NULLを指定すると呼び出し元タスクが指定

### タスクレジューム vTaskResume()
停止させたタスクを再開させます。

```c
void vTaskResume(TaskHandle_t xTaskToResume) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TaskHandle_t `xTaskToResume` タスクハンドル。NULLは許容しません

### 割り込みタスクレジューム xTaskResumeFromISR()
割り込みで停止させたタスクを再開させます。

```c
BaseType_t xTaskResumeFromISR(TaskHandle_t xTaskToResume) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TaskHandle_t `xTaskToResume` タスクハンドル。NULLは許容しません

!!! note "戻り値"
	BaseType_t 実行結果

### 全タスクサスペンド vTaskSuspendAll()
全タスクをサスペンドします。一時的に他のタスクの実行を停止する場合に利用します。利用した後にxTaskResumeAll()で再開してください。

```c
void vTaskSuspendAll(void) PRIVILEGED_FUNCTION
```

### 全タスクレジューム xTaskResumeAll()
全タスクをレジュームします。

```c
BaseType_t xTaskResumeAll(void) PRIVILEGED_FUNCTION
```

!!! note "戻り値"
	BaseType_t 実行結果

### タスク起動時間 xTaskGetTickCount()
タスクが起動したTick数を取得します。

```c
TickType_t xTaskGetTickCount(void) PRIVILEGED_FUNCTION
```

!!! note "戻り値"
	TickType_t タスクが起動したTick数

### 割り込みタスク起動時間 xTaskGetTickCountFromISR()
割り込みでのタスクが起動したTick数を取得します。

```c
TickType_t xTaskGetTickCountFromISR(void) PRIVILEGED_FUNCTION
```

!!! note "戻り値"
	TickType_t タスクが起動したTick数

### タスク数取得 uxTaskGetNumberOfTasks()
タスクの数を取得します。

```c
UBaseType_t uxTaskGetNumberOfTasks(void) PRIVILEGED_FUNCTION
```

!!! note "戻り値"
	UBaseType_t タスク数

### タスク名取得 pcTaskGetTaskName()
タスクの名前を取得します。

```c
char* pcTaskGetTaskName(TaskHandle_t xTaskToQuery) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TaskHandle_t `xTaskToQuery` タスクハンドル。NULLを指定すると呼び出し元タスクが指定

!!! note "戻り値"
	char * タスク名

### 残りスタック取得 uxTaskGetStackHighWaterMark()
タスクで一番少なくなったスタックバイト数を取得します。0に近づくほどオーバーフローしやすくなります。

```c
UBaseType_t uxTaskGetStackHighWaterMark(TaskHandle_t xTask) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TaskHandle_t `xTask` タスクハンドル。NULLを指定すると呼び出し元タスクが指定

!!! note "戻り値"
	UBaseType_t スタックバイト数

### スタック開始アドレス取得 pxTaskGetStackStart()
スタックの開始アドレス取得します。

```c
uint8_t* pxTaskGetStackStart(TaskHandle_t xTask) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TaskHandle_t `xTask` タスクハンドル。NULLを指定すると呼び出し元タスクが指定

!!! note "戻り値"
	uint8_t * アドレス

### (非公開)フック関数呼び出し xTaskCallApplicationTaskHook()
(非公開)タスクに関連付けられたフック関数を呼び出します。

```c
BaseType_t xTaskCallApplicationTaskHook(TaskHandle_t xTask, void *pvParameter) PRIVILEGED_FUNCTION
```

### アイドルタスク取得 xTaskGetIdleTaskHandle()
現在実行しているCPUコアの、アイドルタスクハンドルを取得します。

```c
TaskHandle_t xTaskGetIdleTaskHandle(void)
```

!!! note "戻り値"
	TaskHandle_t タスクハンドル

### CPUコア指定アイドルタスク取得 xTaskGetIdleTaskHandleForCPU()
CPUコアを指定して、アイドルタスクハンドルを取得します。

 is only available if INCLUDE_xTaskGetIdleTaskHandle is set to 1 in .
```c
TaskHandle_t xTaskGetIdleTaskHandleForCPU(UBaseType_t cpuid)
```

!!! summary "引数"
	- UBaseType_t `cpuid` CPUコア(0, 1)

!!! note "戻り値"
	TaskHandle_t タスクハンドル



### (非公開)システムタスク取得 uxTaskGetSystemState()

```c
UBaseType_t uxTaskGetSystemState(TaskStatus_t *const pxTaskStatusArray, const UBaseType_t uxArraySize, uint32_t *const pulTotalRunTime)
```

### (非公開)タスク一覧取得 vTaskList()
```c
void vTaskList(char *pcWriteBuffer) PRIVILEGED_FUNCTION
```

### (非公開)タスクランタイム状態取得 vTaskGetRunTimeStats()
```c
void vTaskGetRunTimeStats(char *pcWriteBuffer) PRIVILEGED_FUNCTION
```

### タスク通知 xTaskNotify()
タスクへ通知を送信します。

```c
BaseType_t xTaskNotify(TaskHandle_t xTaskToNotify, uint32_t ulValue, eNotifyAction eAction)
```

!!! summary "引数"
	- TaskHandle_t `xTaskToNotify` タスクハンドラ
	- uint32_t `ulValue` 通知するデータ。eActionによって通知方法は異なります
	- eNotifyAction `eAction` Specifies how the notification updates the task's notification value, if at all. Valid values for eAction are as follows:
		- eNoAction = 0	通知の値を更新しません
		- eSetBits = 1	通知の値にビットを設定
		- eIncrement = 2 通知の値をインクリメント
		- eSetValueWithOverwrite = 3	前回の通知を受け取っていない場合でも上書きします
		- eSetValueWithoutOverwrite = 4	前回の通知を受け取っていた場合のみ上書きします

!!! note "戻り値"
	BaseType_t 実行結果

!!! Tip "利用例"
	```c
	TaskHandle_t taskHandle;

	void testTask(void *pvParameters) {
	  uint32_t ulNotifiedValue;
	  while (1) {
	    // 通知が来るまで待機する。値のクリアはしない
	    xTaskNotifyWait( 0,
	                     0,
	                     &ulNotifiedValue,
	                     portMAX_DELAY );
	    Serial.println( pcTaskGetTaskName(NULL) );
	    Serial.println( ulNotifiedValue );
	  }
	}

	void setup() {
	  Serial.begin(115200);

	  // Core0でタスク起動
	  xTaskCreatePinnedToCore(
	    testTask,
	    "loopTask1",
	    8192,
	    NULL,
	    1,
	    &taskHandle,
	    0
	  );
	}

	void loop() {
	  delay(500);

	  // 通知送信(値は0から増えていき、100の値は無視される)
	  xTaskNotify(taskHandle, 100, eIncrement );
	}
	```

### 割り込みタスク通知 xTaskNotifyFromISR()
割り込みでのタスクへ通知を送信します。

```c
BaseType_t xTaskNotifyFromISR(TaskHandle_t xTaskToNotify, uint32_t ulValue, eNotifyAction eAction, BaseType_t *pxHigherPriorityTaskWoken)
```

!!! summary "引数"
	- TaskHandle_t `xTaskToNotify` タスクハンドラ
	- uint32_t `ulValue` 通知するデータ。eActionによって通知方法は異なります
	- eNotifyAction `eAction` Specifies how the notification updates the task's notification value, if at all. Valid values for eAction are as follows:
		- eNoAction = 0	通知の値を更新しません
		- eSetBits = 1	通知の値にビットを設定
		- eIncrement = 2 通知の値をインクリメント
		- eSetValueWithOverwrite = 3	前回の通知を受け取っていない場合でも上書きします
		- eSetValueWithoutOverwrite = 4	前回の通知を受け取っていた場合のみ上書きします
	- BaseType_t* `pxHigherPriorityTaskWoken`  通知送信先のタスクがブロック状態から抜けるときに、現在実行中のタスクより優先順位が高い場合pdTRUEに設定します

!!! note "戻り値"
	BaseType_t 実行結果

### タスク通知取得 xTaskNotifyWait()
タスクの通知がくるまで待機する。

```c
BaseType_t xTaskNotifyWait(uint32_t ulBitsToClearOnEntry, uint32_t ulBitsToClearOnExit, uint32_t *pulNotificationValue, TickType_t xTicksToWait)
```

!!! summary "引数"
	- uint32_t `ulBitsToClearOnEntry` 呼び出し前にクリアされる値のビット。0がリセットしない、ULONG_MAXで0にリセット
	- uint32_t `ulBitsToClearOnExit` 関数が終了する前にクリアされる値のビット。0がリセットしない、ULONG_MAXで0にリセット
	- uint32_t * `pulNotificationValue` 通知で利用される変数のポインタ
	- TickType_t `xTicksToWait` 最大待機時間。pdMS_TO_TICSK( value_in_ms )マクロを利用して指定をするか、portMAX_DELAYで無限に待機します

!!! note "戻り値"
	BaseType_t 実行結果


### 簡易タスク通知 xTaskNotifyGive()
タスクへ通知を送信します。内部でxTaskNotify( ( xTaskToNotify ), 0, eIncrement )を呼び出しているインライン関数です。

```c
BaseType_t xTaskNotifyGive(TaskHandle_t xTaskToNotify)
```

!!! summary "引数"
	- TaskHandle_t `xTaskToNotify` タスクハンドラ

!!! note "戻り値"
	BaseType_t 実行結果

### 割り込み簡易タスク通知 vTaskNotifyGiveFromISR()
割り込みでタスクへ通知を送信します。

```c
void vTaskNotifyGiveFromISR(TaskHandle_t xTaskToNotify, BaseType_t *pxHigherPriorityTaskWoken)
```

!!! summary "引数"
	- TaskHandle_t `xTaskToNotify` タスクハンドラ
	- BaseType_t* `pxHigherPriorityTaskWoken`  通知送信先のタスクがブロック状態から抜けるときに、現在実行中のタスクより優先順位が高い場合pdTRUEに設定します

### 簡易タスク通知取得 ulTaskNotifyTake()


```c
uint32_t ulTaskNotifyTake(BaseType_t xClearCountOnExit, TickType_t xTicksToWait)
```

!!! summary "引数"
	- BaseType_t `xClearCountOnExit` pdFALSEの場合、通知値はデクリメントし、pdTRUEの場合はクリアされます
	- TickType_t `xTicksToWait` 最大待機時間。pdMS_TO_TICSK( value_in_ms )マクロを利用して指定をするか、portMAX_DELAYで無限に待機します

!!! note "戻り値"
	uint32_t 通知値

!!! Tip "利用例"
	```c
	TaskHandle_t taskHandle;

	void testTask(void *pvParameters) {
	  while (1) {
	    // 通知が来るまで待機する。値のクリアはしないので通知が受け取れている限り1のまま
	    int ulNotifiedValue = ulTaskNotifyTake( pdFALSE, portMAX_DELAY );
	    Serial.println( pcTaskGetTaskName(NULL) );
	    Serial.println( ulNotifiedValue );
	  }
	}

	void setup() {
	  Serial.begin(115200);

	  // Core0でタスク起動
	  xTaskCreatePinnedToCore(
	    testTask,
	    "loopTask1",
	    8192,
	    NULL,
	    1,
	    &taskHandle,
	    0
	  );
	}

	void loop() {
	  delay(500);

	  // 通知送信(値は0から増えていき、100の値は無視される)
	  xTaskNotify(taskHandle, 100, eIncrement ); 
	}
	```

# リファレンス
- [ESP-IDF Programming Guide FreeRTOS Task API](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/system/freertos.html#task-api)

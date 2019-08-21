# キュー(queue)

## メンバー

### キュー作成 xQueueCreate()
キューを作成します。内部的にはxQueueGenericCreate( ( uxQueueLength ), ( uxItemSize ), ( queueQUEUE_TYPE_BASE ) )が呼び出されています。

```c
QueueHandle_t xQueueCreate(const UBaseType_t uxQueueLength, const UBaseType_t uxItemSize)
```

!!! summary "引数"
	- UBaseType_tconst `uxQueueLength` キューの数
	- UBaseType_tconst `uxItemSize` アイテムのサイズ

!!! note "戻り値"
	QueueHandle_t キュー

### 拡張キュー作成 xQueueGenericCreate()
ESP32で拡張されたキューを作成します。内部関数のため通常はxQueueCreate()を利用してください。

```c
QueueHandle_t xQueueGenericCreate(const UBaseType_t uxQueueLength, const UBaseType_t uxItemSize, const uint8_t ucQueueType)
```

!!! summary "引数"
	- UBaseType_tconst `uxQueueLength` キューの数
	- UBaseType_tconst `uxItemSize` アイテムのサイズ
	- const uint8_t `ucQueueType` キューの種類
		- queueQUEUE_TYPE_BASE	( ( uint8_t ) 0U )
		- queueQUEUE_TYPE_SET	( ( uint8_t ) 0U )
		- queueQUEUE_TYPE_MUTEX	( ( uint8_t ) 1U )
		- queueQUEUE_TYPE_COUNTING_SEMAPHORE	( ( uint8_t ) 2U )
		- queueQUEUE_TYPE_BINARY_SEMAPHORE	( ( uint8_t ) 3U )
		- queueQUEUE_TYPE_RECURSIVE_MUTEX		( ( uint8_t ) 4U )

!!! note "戻り値"
	QueueHandle_t キュー

### (非公開)静的キュー作成 xQueueCreateStatic()
キューで利用するストレージがコンパイル時に割り当てられます。内部ではxQueueGenericCreateStatic( ( uxQueueLength ), ( uxItemSize ), ( pucQueueStorage ), ( pxQueueBuffer ), ( queueQUEUE_TYPE_BASE ) )が呼び出されます。

```c
QueueHandle_t xQueueCreateStatic( const UBaseType_t uxQueueLength, const UBaseType_t uxItemSize, uint8_t *pucQueueStorage, StaticQueue_t *pxStaticQueue );
```





### キュー送信 xQueueSend()
キューを送信します。内部的にはxQueueGenericSend( ( xQueue ), ( pvItemToQueue ), ( xTicksToWait ), queueSEND_TO_BACK )を呼んでいます。

```c
BaseType_t xQueueSend(QueueHandle_t xQueue, const void *const pvItemToQueue, TickType_t xTicksToWait)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- const void *const `pvItemToQueue` キューに送信するアイテムへのポインタ。データはキューが保持するストレージにコピーされます
	- TickType_t `xTicksToWait` キューが一杯の場合、利用可能になるまで待機する最大時間。0だと即時終了

!!! note "戻り値"
	BaseType_t 実行結果

### 先頭にキュー送信 xQueueSendToBack()
キューを送信します。xQueueSend()と同じく内部的にはxQueueGenericSend( ( xQueue ), ( pvItemToQueue ), ( xTicksToWait ), queueSEND_TO_BACK )を呼んでいます。

```c
BaseType_t xQueueSendToBack(QueueHandle_t xQueue, const void *const pvItemToQueue, TickType_t xTicksToWait)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- const void *const `pvItemToQueue` キューに送信するアイテムへのポインタ。データはキューが保持するストレージにコピーされます
	- TickType_t `xTicksToWait` キューが一杯の場合、利用可能になるまで待機する最大時間。0だと即時終了

!!! note "戻り値"
	BaseType_t 実行結果

### 先頭にキュー送信 xQueueSendToFront()
先頭にキューを送信します。内部的にはxQueueGenericSend( ( xQueue ), ( pvItemToQueue ), ( xTicksToWait ), queueSEND_TO_FRONT )を呼んでいます。

```c
BaseType_t xQueueSendToFront(QueueHandle_t xQueue, const void *const pvItemToQueue, TickType_t xTicksToWait)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- const void *const `pvItemToQueue` キューに送信するアイテムへのポインタ。データはキューが保持するストレージにコピーされます
	- TickType_t `xTicksToWait` キューが一杯の場合、利用可能になるまで待機する最大時間。0だと即時終了

!!! note "戻り値"
	BaseType_t 実行結果

### キュー上書き送信 xQueueOverwrite()
キューを送信します。キューが一杯の場合でもキューに書き込みます。長さが1のキューでのみ利用できます。それ以外のキューに利用するとリセットがかかります。内部的にはxQueueGenericSend( ( xQueue ), ( pvItemToQueue ), 0, queueOVERWRITE )を呼んでいます。

```c
BaseType_t xQueueOverwrite(QueueHandle_t xQueue, const void *const pvItemToQueue)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- const void *const `pvItemToQueue` キューに送信するアイテムへのポインタ。データはキューが保持するストレージにコピーされます

!!! note "戻り値"
	BaseType_t 実行結果

### 拡張キュー送信 xQueueGenericSend()
ESP32で拡張されたキューを作成します。内部関数のため通常はxQueueSend()かxQueueSendToFront()、xQueueOverwrite()を利用してください。

```c
BaseType_t xQueueGenericSend(QueueHandle_t xQueue, const void *const pvItemToQueue, TickType_t xTicksToWait, const BaseType_t xCopyPosition)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- const void *const `pvItemToQueue` キューに送信するアイテムへのポインタ。データはキューが保持するストレージにコピーされます
	- TickType_t `xTicksToWait` キューが一杯の場合、利用可能になるまで待機する最大時間。0だと即時終了
	- BaseType_tconst `xCopyPosition` キュー追加場所
		- queueSEND_TO_BACK : キューの最後に追加する
		- queueSEND_TO_FRONT : キューの先頭に追加する
		- queueOVERWRITE : 上書きする

!!! note "戻り値"
	BaseType_t 実行結果



### キューピーク受信 xQueuePeek()
キューを受信します。受信したアイテムはキューから削除されません。内部ではxQueueGenericReceive( ( xQueue ), ( pvBuffer ), ( xTicksToWait ), pdTRUE )を呼んでいます。

```c
BaseType_t xQueuePeek(QueueHandle_t xQueue, void *const pvBuffer, TickType_t xTicksToWait)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- void *const `pvBuffer` 受信したアイテムのコピー先ポインタ
	- TickType_t `xTicksToWait` キューが空の場合、受信可能になるまで待機する最大時間。0だと即時終了
!!! note "戻り値"
	BaseType_t 実行結果



### 割り込みキューピーク受信 xQueuePeekFromISR()
割り込み対応のキューを受信します。受信したアイテムはキューから削除されません。

```c
BaseType_t xQueuePeekFromISR(QueueHandle_t xQueue, void *const pvBuffer)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- void *const `pvBuffer` 受信したアイテムのコピー先ポインタ

!!! note "戻り値"
	BaseType_t 実行結果


### キュー受信 xQueueReceive()
キューを受信します。受信したアイテムはキューから削除されます。内部でxQueueGenericReceive( ( xQueue ), ( pvBuffer ), ( xTicksToWait ), pdFAIL )を呼んでいます。

```c
BaseType_t xQueueReceive(QueueHandle_t xQueue, void *const pvBuffer, TickType_t xTicksToWait)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- void *const `pvBuffer` 受信したアイテムのコピー先ポインタ
	- TickType_t `xTicksToWait` キューが空の場合、受信可能になるまで待機する最大時間。0だと即時終了

!!! note "戻り値"
	BaseType_t 実行結果



### キュー受信 xQueueGenericReceive()
キューを受信します。内部関数のため通常はxQueueReceive()かxQueuePeek()を利用してください。

```c
BaseType_t xQueueGenericReceive(QueueHandle_t xQueue, void *const pvBuffer, TickType_t xTicksToWait, const BaseType_t xJustPeek)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- void *const `pvBuffer` 受信したアイテムのコピー先ポインタ
	- TickType_t `xTicksToWait` キューが空の場合、受信可能になるまで待機する最大時間。0だと即時終了
	- BaseType_tconst `xJustPeek` 受信アイテム削除設定
		- true : 受信したアイテムをキューから削除しません
		- false : 受信したアイテムをキューから削除します

!!! note "戻り値"
	BaseType_t 実行結果


### キュー数取得 uxQueueMessagesWaiting()
キューの数を取得します。

```c
UBaseType_t uxQueueMessagesWaiting(const QueueHandle_t xQueue)
```

!!! summary "引数"
	- QueueHandle_t const `xQueue` キューハンドル

!!! note "戻り値"
	UBaseType_t キュー数


### キュー追加可能数取得 uxQueueSpacesAvailable()
キューに追加可能な数を取得します。

```c
UBaseType_t uxQueueSpacesAvailable(const QueueHandle_t xQueue)
```

!!! summary "引数"
	- QueueHandle_t const `xQueue` キューハンドル

!!! note "戻り値"
	UBaseType_t キュー可能数


### キュー削除 vQueueDelete()
キューを削除します。

```c
void vQueueDelete(QueueHandle_t xQueue)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル




### 割り込み対応先頭へキュー送信 xQueueSendToFrontFromISR()
割り込み対応の先頭へキューを送信する。内部でxQueueGenericSendFromISR( ( xQueue ), ( pvItemToQueue ), ( pxHigherPriorityTaskWoken ), queueSEND_TO_FRONT )を呼んでいる。

```c
BaseType_t xQueueSendToFrontFromISR(QueueHandle_t xQueue, const void *const pvItemToQueue, BaseType_t *const pxHigherPriorityTaskWoken)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- const void *const `pvItemToQueue` キューに送信するアイテムへのポインタ。データはキューが保持するストレージにコピーされます
	- BaseType_t*const `pxHigherPriorityTaskWoken` pdTRUEかpdFAILが保存される変数へのポインタ。キュー送信によって現在より高い優先順位タスクのブロックが解除されるとpdTRUEがセットされる

!!! note "戻り値"
	BaseType_t 実行結果

### 割り込み対応キュー送信 xQueueSendToBackFromISR()
割り込み対応のキューを送信する。内部でxQueueGenericSendFromISR( ( xQueue ), ( pvItemToQueue ), ( pxHigherPriorityTaskWoken ), queueSEND_TO_BACK )を呼んでいる。

```c
BaseType_t xQueueSendToBackFromISR(QueueHandle_t xQueue, const void *const pvItemToQueue, BaseType_t *const pxHigherPriorityTaskWoken)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- const void *const `pvItemToQueue` キューに送信するアイテムへのポインタ。データはキューが保持するストレージにコピーされます
	- BaseType_t*const `pxHigherPriorityTaskWoken` pdTRUEかpdFAILが保存される変数へのポインタ。キュー送信によって現在より高い優先順位タスクのブロックが解除されるとpdTRUEがセットされる

!!! note "戻り値"
	BaseType_t 実行結果

### 割り込み対応キュー上書き送信 xQueueOverwriteFromISR()
割り込み対応のキューを送信します。キューが一杯の場合でもキューに書き込みます。長さが1のキューでのみ利用できます。それ以外のキューに利用するとリセットがかかります。内部的にはxQueueGenericSendFromISR( ( xQueue ), ( pvItemToQueue ), 0, queueOVERWRITE )を呼んでいます。

```c
BaseType_t xQueueOverwriteFromISR(QueueHandle_t xQueue, const void *const pvItemToQueue, BaseType_t *const pxHigherPriorityTaskWoken)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- const void *const `pvItemToQueue` キューに送信するアイテムへのポインタ。データはキューが保持するストレージにコピーされます
	- BaseType_t*const `pxHigherPriorityTaskWoken` pdTRUEかpdFAILが保存される変数へのポインタ。キュー送信によって現在より高い優先順位タスクのブロックが解除されるとpdTRUEがセットされる

!!! note "戻り値"
	BaseType_t 実行結果

### 割り込み対応キュー送信 xQueueSendFromISR()
割り込み対応のキューを送信する。xQueueSendToBackFromISR()と同じく、内部でxQueueGenericSendFromISR( ( xQueue ), ( pvItemToQueue ), ( pxHigherPriorityTaskWoken ), queueSEND_TO_BACK )を呼んでいる。

```c
BaseType_t xQueueSendFromISR(QueueHandle_t xQueue, const void *const pvItemToQueue, BaseType_t *const pxHigherPriorityTaskWoken)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- const void *const `pvItemToQueue` キューに送信するアイテムへのポインタ。データはキューが保持するストレージにコピーされます
	- BaseType_t*const `pxHigherPriorityTaskWoken` pdTRUEかpdFAILが保存される変数へのポインタ。キュー送信によって現在より高い優先順位タスクのブロックが解除されるとpdTRUEがセットされる

!!! note "戻り値"
	BaseType_t 実行結果


### 割り込み対応拡張キュー送信 xQueueGenericSendFromISR()
割り込み対応の拡張キューを送信する。内部関数のため通常はxQueueSendToFrontFromISR()、xQueueSendToBackFromISR()、xQueueOverwriteFromISR()、xQueueSendFromISR()関数などを利用してください。

```c
BaseType_t xQueueGenericSendFromISR(QueueHandle_t xQueue, const void *const pvItemToQueue, BaseType_t *const pxHigherPriorityTaskWoken, const BaseType_t xCopyPosition)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- const void *const `pvItemToQueue` キューに送信するアイテムへのポインタ。データはキューが保持するストレージにコピーされます
	- BaseType_t*const `pxHigherPriorityTaskWoken` pdTRUEかpdFAILが保存される変数へのポインタ。キュー送信によって現在より高い優先順位タスクのブロックが解除されるとpdTRUEがセットされる
	- BaseType_tconst `xCopyPosition` キュー追加場所
		- queueSEND_TO_BACK : キューの最後に追加する
		- queueSEND_TO_FRONT : キューの先頭に追加する
		- queueOVERWRITE : 上書きする

!!! note "戻り値"
	BaseType_t 実行結果



### 割り込み対応キュー取得 xQueueGiveFromISR()
割り込み対応のキューを受信しますが、データはコピーされません。セフォマ的なキューの利用です。

```c
BaseType_t xQueueGiveFromISR(QueueHandle_t xQueue, BaseType_t *const pxHigherPriorityTaskWoken)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- BaseType_t*const `pxHigherPriorityTaskWoken` pdTRUEかpdFAILが保存される変数へのポインタ。キュー送信によって現在より高い優先順位タスクのブロックが解除されるとpdTRUEがセットされる

!!! note "戻り値"
	BaseType_t


### 割り込み対応キュー受信 xQueueReceiveFromISR()
割り込み対応のキューを受信します。

```c
BaseType_t xQueueReceiveFromISR(QueueHandle_t xQueue, void *const pvBuffer, BaseType_t *const pxHigherPriorityTaskWoken)
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- void *const `pvBuffer` 受信したアイテムのコピー先ポインタ
	- BaseType_t*const `pxHigherPriorityTaskWoken` pdTRUEかpdFAILが保存される変数へのポインタ。キュー送信によって現在より高い優先順位タスクのブロックが解除されるとpdTRUEがセットされる

!!! note "戻り値"
	BaseType_t 実行結果

### 割り込みキュー空確認 xQueueIsQueueEmptyFromISR()
割り込み対応のキューが空か確認します。ISRから安全に利用できます。ISRまたはクリティカルセクション内でのみ利用してください。

```c
BaseType_t xQueueIsQueueEmptyFromISR(const QueueHandle_t xQueue)
```

!!! summary "引数"
	- QueueHandle_t const `xQueue` キューハンドル

!!! note "戻り値"
	BaseType_t 結果

### 割り込み対応キューフル確認 xQueueIsQueueFullFromISR()
割り込み対応のキューに空きがないか確認します。ISRから安全に利用できます。ISRまたはクリティカルセクション内でのみ利用してください。

```c
BaseType_t xQueueIsQueueFullFromISR(const QueueHandle_t xQueue)
```

!!! summary "引数"
	- QueueHandle_t const `xQueue` キューハンドル

!!! note "戻り値"
	BaseType_t 結果

### 割り込み対応キュー数取得 uxQueueMessagesWaitingFromISR()
割り込み対応のキュー数を取得します。ISRから安全に利用できます。ISRまたはクリティカルセクション内でのみ利用してください。

```c
UBaseType_t uxQueueMessagesWaitingFromISR(const QueueHandle_t xQueue)
```

!!! summary "引数"
	- QueueHandle_t const `xQueue` キューハンドル

!!! note "戻り値"
	UBaseType_t キュー数




### キューリセット xQueueReset()
キューをリセットします。内部でxQueueGenericReset( xQueue, pdFALSE )を呼んでいます。

```c
BaseType_t xQueueReset( QueueHandle_t xQueue )
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル

!!! note "戻り値"
	UBaseType_t 実行結果(pdTRUE:成功, pdFAIL:ブロックされて失敗)


### キュー拡張リセット xQueueGenericReset()
キューをリセットします。通常はxQueueGenericReset()関数を利用してください。

```c
BaseType_t xQueueGenericReset( QueueHandle_t xQueue, BaseType_t xNewQueue )
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- BaseType_t `xNewQueue` 不明
		- pdTRUE 
		- pdFAIL 

!!! note "戻り値"
	UBaseType_t 実行結果(pdTRUE:成功, pdFAIL:ブロックされて失敗)






### キューデバッガー登録 vQueueAddToRegistry()
キューをデバッガーで利用できるように登録します。

```c
void vQueueAddToRegistry( QueueHandle_t xQueue, const char *pcName )
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル
	- const char * `pcName` 登録される名前


### キューデバッガー解除 vQueueUnregisterQueue()
キューをデバッガーの利用から解除します。

```c
void vQueueUnregisterQueue( QueueHandle_t xQueue )
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル


### キューデバッガー登録名取得 pcQueueGetName()
キューをデバッガーで利用できるように登録した名前を取得します。

```c
const char *pcQueueGetName( QueueHandle_t xQueue )
```

!!! summary "引数"
	- QueueHandle_t `xQueue` キューハンドル

!!! note "戻り値"
	const char * 登録名












### キューセット作成 xQueueCreateSet()
キューの読み出しをロックするセットを作成する。

```c
QueueSetHandle_t xQueueCreateSet(const UBaseType_t uxEventQueueLength)
```

!!! summary "引数"
	- UBaseType_tconst `uxEventQueueLength` セットに含まれるすべてのキューの長さの合計


!!! note "戻り値"
	QueueSetHandle_t キューセットハンドル


### キューセットメンバー追加 xQueueAddToSet()
キューセットにキューを追加します。

```c
BaseType_t xQueueAddToSet(QueueSetMemberHandle_t xQueueOrSemaphore, QueueSetHandle_t xQueueSet)
```

!!! summary "引数"
	- QueueSetMemberHandle_t `xQueueOrSemaphore` キューハンドル
	- QueueSetHandle_t `xQueueSet` キューセットハンドル

!!! note "戻り値"
	BaseType_t 実行結果

### キューセットメンバー削除 xQueueRemoveFromSet()
キューセットからキューを削除します。

```c
BaseType_t xQueueRemoveFromSet(QueueSetMemberHandle_t xQueueOrSemaphore, QueueSetHandle_t xQueueSet)
```

!!! summary "引数"
	- QueueSetMemberHandle_t `xQueueOrSemaphore` キューハンドル
	- QueueSetHandle_t `xQueueSet` キューセットハンドル

!!! note "戻り値"
	BaseType_t 実行結果

### キューセット受信可能取得 xQueueSelectFromSet()
キューセットの中で受信可能なキューを取得します。一度呼び出すたびに1つのキューアイテムが受信できます。NULLが戻るまで受信をすることができます。

```c
QueueSetMemberHandle_t xQueueSelectFromSet(QueueSetHandle_t xQueueSet, const TickType_t xTicksToWait)
```

!!! summary "引数"
	- QueueSetHandle_t `xQueueSet` キューセットハンドル
	- TickType_tconst `xTicksToWait` 待機する最大時間

!!! note "戻り値"
	QueueSetMemberHandle_t キューハンドル

### 割り込み対応キューセット受信可能取得 xQueueSelectFromSetFromISR()
割り込み対応のキューセットの中で受信可能なキューを取得します。一度呼び出すたびに1つのキューアイテムが受信できます。NULLが戻るまで受信をすることができます。

```c
QueueSetMemberHandle_t xQueueSelectFromSetFromISR(QueueSetHandle_t xQueueSet)
```

!!! summary "引数"
	- QueueSetHandle_t `xQueueSet` キューセットハンドル

!!! note "戻り値"
	QueueSetMemberHandle_t キューハンドル

# サンプル

## サンプルスケッチ
```c
// キューの大きさ
#define QUEUE_LENGTH 4

// 通常のキュー
QueueHandle_t xQueue;

// Mailbox用のキュー
QueueHandle_t xQueueMailbox;

void setup() {
  // キューアイテム
  uint8_t data = 1;

  // デバッグ出力準備
  Serial.begin(115200);
  Serial.println("Queue Test");

  // キュー作成
  xQueue = xQueueGenericCreate( QUEUE_LENGTH, sizeof( uint8_t ), queueQUEUE_TYPE_BASE );

  // メールボックス用途は長さ1のみ
  xQueueMailbox = xQueueGenericCreate( 1, sizeof( uint8_t ), queueQUEUE_TYPE_BASE );

  // 最後に追加(1)
  xQueueSend(xQueue, &data, 0);
  data++;

  // 先頭に追加(2)
  xQueueSendToFront(xQueue, &data, 0);
  data++;

  // 最後に追加(3)
  xQueueSendToBack(xQueue, &data, 0);
  data++;

  // 上書き送信(4)
  xQueueOverwrite(xQueueMailbox, &data);
  data++;

  // 上書き送信(5)
  xQueueOverwrite(xQueueMailbox, &data);
  data++;

  // キューの数確認
  Serial.printf( "uxQueueMessagesWaiting = %d\n", uxQueueMessagesWaiting(xQueue) );

  // キューの追加可能数確認
  Serial.printf( "uxQueueSpacesAvailable = %d\n", uxQueueSpacesAvailable(xQueue) );

  // キューの状態取得
  Serial.printf( "xQueueIsQueueEmptyFromISR = %d\n", xQueueIsQueueEmptyFromISR(xQueue) );
  Serial.printf( "xQueueIsQueueFullFromISR = %d\n", xQueueIsQueueFullFromISR(xQueue) );
  Serial.printf( "uxQueueMessagesWaitingFromISR = %d\n", uxQueueMessagesWaitingFromISR(xQueue) );

  // Peek受信(何度受信しても同じ値)
  Serial.println( "Peek Test" );
  xQueuePeek( xQueue, &data, 0 );
  Serial.println( data );
  xQueuePeek( xQueue, &data, 0 );
  Serial.println( data );

  // 通常受信(213の順で受信し、受信成功した場合のみアイテムが更新される)
  int ret;
  Serial.println( "Receive Test" );
  ret = xQueueReceive( xQueue, &data, 0 );
  Serial.printf( "ret = %d, data = %d\n", ret, data );
  ret = xQueueReceive( xQueue, &data, 0 );
  Serial.printf( "ret = %d, data = %d\n", ret, data );
  ret = xQueueReceive( xQueue, &data, 0 );
  Serial.printf( "ret = %d, data = %d\n", ret, data );
  ret = xQueueReceive( xQueue, &data, 0 );
  Serial.printf( "ret = %d, data = %d\n", ret, data );
  ret = xQueueReceive( xQueue, &data, 0 );
  Serial.printf( "ret = %d, data = %d\n", ret, data );

  // Mailbox受信(最後に送信したデータのみ受信)
  Serial.println( "Mailbox Test" );
  xQueuePeek( xQueueMailbox, &data, 0 );
  Serial.println( data );

  // キュークリア
  Serial.println( "xQueueReset Test" );
  xQueueReset(xQueue);
  xQueueReset(xQueueMailbox);

  // キューセット
  Serial.println( "QueueSet Test" );
  QueueSetHandle_t xQueueSet;
  xQueueSet = xQueueCreateSet( QUEUE_LENGTH + 1 ); // Setするキューの合計
  xQueueAddToSet( xQueue, xQueueSet );
  xQueueAddToSet( xQueueMailbox, xQueueSet );

  // アイテム追加
  data = 100;
  xQueueSend(xQueue, &data, 0);
  data++;
  xQueueSend(xQueue, &data, 0);
  data++;
  xQueueSend(xQueueMailbox, &data, 0);

  // 取得してみる
  while(1){
    // 取得可能なキューを取得する
    QueueHandle_t queue = xQueueSelectFromSet( xQueueSet, 0 );
    if( queue == NULL ){
      // キューがなくなったので終了
      break;
    }

    // キューの種類を調べる
    if( queue == xQueue ){
      Serial.print( "xQueue " );
    } else if( queue == xQueueMailbox ) {
      Serial.print( "xQueueMailbox " );
    } else {
      Serial.print( "? " );
    }
    
    // 受信
    ret = xQueueReceive( queue, &data, 0 );
    Serial.printf( "ret = %d, data = %d\n", ret, data );
  }

  // キュー削除
  vQueueDelete(xQueue);
  vQueueDelete(xQueueMailbox);
}

void loop() {
}
```

## 実行結果
```
Queue Test
uxQueueMessagesWaiting = 3
uxQueueSpacesAvailable = 1
xQueueIsQueueEmptyFromISR = 0
xQueueIsQueueFullFromISR = 0
uxQueueMessagesWaitingFromISR = 3
Peek Test
2
2
Receive Test
ret = 1, data = 2
ret = 1, data = 1
ret = 1, data = 3
ret = 0, data = 3
ret = 0, data = 3
Mailbox Test
5
xQueueReset Test
QueueSet Test
xQueue ret = 1, data = 100
xQueue ret = 1, data = 101
xQueueMailbox ret = 1, data = 102
```

# リファレンス
- [ESP-IDF Programming Guide FreeRTOS Queue API](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/system/freertos.html#queue-api)


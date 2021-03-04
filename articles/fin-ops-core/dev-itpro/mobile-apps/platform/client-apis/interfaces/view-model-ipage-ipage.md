---
title: ページのタイプ
description: ページ オブジェクト タイプ。
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a4dca6f7f13c52b15b0cd203caf5056660031f5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688191"
---
# <a name="page-type"></a>ページのタイプ

[!include [banner](../../../../includes/banner.md)]

ページ オブジェクト タイプ。

### <a name="hierarchy"></a>階層

ページ <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [子](view-model-ipage-ipage.md#children)
* [dataLoadedInitially](view-model-ipage-ipage.md#dataloadedinitially)
* [初期化済み](view-model-ipage-ipage.md#initialized)
* [メタデータ](view-model-ipage-ipage.md#metadata)
* [metadataLoaded](view-model-ipage-ipage.md#metadataloaded)
* [pageContext](view-model-ipage-ipage.md#pagecontext)
* [pageFilter](view-model-ipage-ipage.md#pagefilter)
* [状態](view-model-ipage-ipage.md#state)
* [syncError](view-model-ipage-ipage.md#syncerror)
* [syncPending](view-model-ipage-ipage.md#syncpending)
* [syncProcessing](view-model-ipage-ipage.md#syncprocessing)
* [syncUnitEditable](view-model-ipage-ipage.md#syncuniteditable)
* [タイトル](view-model-ipage-ipage.md#title)

### <a name="methods"></a>メソッド

* [canSubmit](view-model-ipage-ipage.md#cansubmit)
* [閉じる](view-model-ipage-ipage.md#close)
* [getAction](view-model-ipage-ipage.md#getaction)
* [getActions](view-model-ipage-ipage.md#getactions)
* [getControl](view-model-ipage-ipage.md#getcontrol)
* [getDesign](view-model-ipage-ipage.md#getdesign)
* [getEntityContext](view-model-ipage-ipage.md#getentitycontext)
* [isEditable](view-model-ipage-ipage.md#iseditable)
* [refreshData](view-model-ipage-ipage.md#refreshdata)
* [経歴](view-model-ipage-ipage.md#resume)
* [送信](view-model-ipage-ipage.md#submit)
* [中断](view-model-ipage-ipage.md#suspend)

### <a name="events"></a>イベント

* [onClose](view-model-ipage-ipage.md#onclose)
* [onComplete](view-model-ipage-ipage.md#oncomplete)
* [onDataLoaded](view-model-ipage-ipage.md#ondataloaded)
* [onInit](view-model-ipage-ipage.md#oninit)
* [onPreInit](view-model-ipage-ipage.md#onpreinit)
* [onRefresh](view-model-ipage-ipage.md#onrefresh)
* [onStateChange](view-model-ipage-ipage.md#onstatechange)
* [onSubmit](view-model-ipage-ipage.md#onsubmit)
* [onSyncStatusChange](view-model-ipage-ipage.md#onsyncstatuschange)

## <a name="properties"></a>プロパティ

### <a name="children"></a>children

子: [Control](view-model-control-basecontrol-icontrol-icontrol.md)[ ]

(読み取り専用) ページのすべての直接の子コントロールの一覧。


### <a name="dataloadedinitially"></a>dataLoadedInitially

dataLoadedInitially: Promise &lt;void&gt;

(読み取り専用) 初めてデータが読み込まれたときに解決する約束。
納期回答在庫は、ページの残りの部分でも解決された状態で維持されます。


### <a name="initialized"></a>initialized

initialized: boolean

(読み取り専用) ページ インスタンスが初期化されている場合は、True です。


### <a name="metadata"></a>metadata

metadata: [PageMetadata](view-model-ipage-ipagemetadata.md)

(読み取り専用) ページ メタデータ。


### <a name="metadataloaded"></a>metadataLoaded

metadataLoaded: Promise &lt;void&gt;

(読み取り専用) メタデータが読み込みを完了したときに解決する約束。


### <a name="pagecontext"></a>pageContext

pageContext: string

現在のページ コンテキスト。


### <a name="pagefilter"></a>pageFilter

pageFilter: DataFilter

ページに適用されている現在のフィルター。


### <a name="state"></a>状態

state: [PageState](../enums/view-model-ipage-pagestate.md)

(読み取り専用) ページの現在の状態。


### <a name="syncerror"></a>syncError

syncError: boolean

(読み取り専用) ページの送信がエラー状態の場合、True です。
これは通常、検証エラーのためにサーバーが送信を拒否した場合に発生します。
ページ データ同期について詳しくは、[このトピック](../modules/view-model-ipage.md#page-data-synchronization)をご覧ください。


### <a name="syncpending"></a>syncPending

syncPending: boolean

(読み取り専用) ページの送信が同期の待機中の場合、True です。
ページ データ同期について詳しくは、[このトピック](../modules/view-model-ipage.md#page-data-synchronization)をご覧ください。


### <a name="syncprocessing"></a>syncProcessing

syncProcessing: boolean

(読み取り専用) ページ インスタンスが現在送信を同期している場合は True です。
ページ データ同期について詳しくは、[このトピック](../modules/view-model-ipage.md#page-data-synchronization)をご覧ください。


### <a name="syncuniteditable"></a>syncUnitEditable

syncUnitEditable: boolean

(読み取り専用) 同期の待機中に送信が編集可能な場合、True です。
ページ データ同期について詳しくは、[このトピック](../modules/view-model-ipage.md#page-data-synchronization)をご覧ください。


### <a name="title"></a>title

title: string

(読み取り専用) ページのタイトル。


## <a name="methods"></a>メソッド

### <a name="cansubmit"></a>canSubmit


canSubmit(): boolean

アクション ページが送信可能で、検証/エラー メッセージが存在しない場合は、true を返します。

#### <a name="returns-boolean"></a>ブール値を返します



### <a name="close"></a>閉じる


close(): void

ページ インスタンスとすべてのライフ サイクルイベントを破棄します。

#### <a name="returns-void"></a>void を返します

### <a name="getaction"></a>getAction


getAction(actionName: string): [PageLink](view-model-control-pagelink-ipagelink-ipagelink.md)

名前でページ アクションを取得します。
これらには、アクション シート/メニュー内のアクションが含まれます。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| actionName|文字列||

#### <a name="returns-pagelink"></a>[PageLink](view-model-control-pagelink-ipagelink-ipagelink.md) を返します



### <a name="getactions"></a>getActions


getActions(): [PageLink](view-model-control-pagelink-ipagelink-ipagelink.md) [ ]

すべてのページ アクションを取得します。
これらには、アクション シート/メニュー内のアクションが含まれます。

#### <a name="returns-pagelink--"></a>[PageLink](view-model-control-pagelink-ipagelink-ipagelink.md) [ ] を返します



### <a name="getcontrol"></a>getControl


getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)

名前でページ コントロールを取得します。
これは、すべての子ページを通して再帰的に検索します。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| controlName|string||

#### <a name="returns-control"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します



### <a name="getdesign"></a>getDesign


getDesign(): [Design](view-model-ipage-idesign.md)

ページに関連付けられているデザイン オブジェクトを取得します。

#### <a name="returns-design"></a>[Design](view-model-ipage-idesign.md) を返します



### <a name="getentitycontext"></a>getEntityContext


getEntityContext(): EntityRef

現在のエンティティ コンテキストを取得します。

#### <a name="returns-entityref"></a>EntityRef を返します



### <a name="iseditable"></a>isEditable


isEditable(): boolean

ページがアクション ページの場合は true を返します

#### <a name="returns-boolean"></a>ブール値を返します



### <a name="refreshdata"></a>refreshData


refreshData(): Promise &lt;void&gt;

ページ データを強制更新します。

#### <a name="returns-promise-ltvoidgt"></a>Promise &lt;void&gt; を返します



### <a name="resume"></a>経歴


resume(): Promise &lt;void&gt;

一時的停止されたページを再開します。

#### <a name="returns-promise-ltvoidgt"></a>Promise &lt;void&gt; を返します



### <a name="submit"></a>submit


submit(): Promise &lt;[CompleteEventArgs](view-model-ipage-icompleteeventargs.md)&gt;

アクションを送信します。

#### <a name="returns-promise-ltcompleteeventargsgt"></a>Promise &lt;[CompleteEventArgs](view-model-ipage-icompleteeventargs.md)&gt; を返します



### <a name="suspend"></a>suspend


suspend(): void

ページを一時的に中断します。
たとえば、ページがアクティブ ビューでない場合。

#### <a name="returns-void"></a>void を返します

## <a name="events"></a>イベント

### <a name="onclose"></a>onClose

onClose: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;

ページを閉じるときに発生するイベント。


### <a name="oncomplete"></a>onComplete

onComplete: [EventHook](event-ievent-ieventhook.md) &lt;any&gt;

アクションが完了したときに発生するイベント。


### <a name="ondataloaded"></a>onDataLoaded

onDataLoaded: [EventHook](event-ievent-ieventhook.md) &lt;any&gt;

ページ データが読み込まれたときに発生するイベント。
このイベントは、新しいデータがロードされるたびに複数回発生する可能性があります。


### <a name="oninit"></a>onInit

onInit: [EventHook](event-ievent-ieventhook.md) &lt;any&gt;

ページ インスタンスが初期化され、メタデータがロードされたときに発生するイベント。


### <a name="onpreinit"></a>onPreInit

onPreInit: [EventHook](event-ievent-ieventhook.md) &lt;any&gt;

ページ インスタンスが初期化されたときに発生するイベント。
これは、メタデータが読み込まれる前に発生します。


### <a name="onrefresh"></a>onRefresh

onRefresh: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;

新しいデータが読み込まれる前に、強制的なページ更新で発生するイベント。


### <a name="onstatechange"></a>onStateChange

onStateChange: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;

ページ状態が変更するときに発生するイベント。


### <a name="onsubmit"></a>onSubmit

onSubmit: [EventHook](event-ievent-ieventhook.md) &lt;[PageSubmitArgs](view-model-ipage-ipagesubmitargs.md)&gt;

アクションが送信される前に発生するイベント。
アクションの検証/遅延について中断できます。使用可能なオプションの詳細については、IPageSubmitArgs を参照してください。


### <a name="onsyncstatuschange"></a>onSyncStatusChange

onSyncStatusChange: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;

ページの同期状態が変更するときに発生するイベント。




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
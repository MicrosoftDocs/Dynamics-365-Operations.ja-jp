---
title: ページ モジュール
description: IPage インターフェイスは、さまざまなプロパティ、ライフ サイクル、およびワークスペース内のページに関連付けられているイベント フックをカプセル化します。
author: tonyafehr
ms.date: 08/01/2017
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: e6213924b1fc0d081c71a72c3467239fd4d45ad1
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781512"
---
# <a name="page-module"></a>ページ モジュール

[!include [banner](../../../../includes/banner.md)]

IPage インターフェイスは、さまざまなプロパティ、ライフ サイクル、およびワークスペース内のページに関連付けられているイベント フックをカプセル化します。
### <a name="page-data-synchronization"></a>ページ データ同期
変更を送信できるページ (アクションとも呼ばれる) は、サーバーと完全に同期される前にさまざまなステージを通過します。
ページが [送信](../interfaces/view-model-ipage-ipage.md#submit) されるとすぐに、起こり得る結果が 3 つあります。
* クライアント側の検証に失敗する場合: クライアント ロジックによってページを送信できない可能性があります。
* クライアントはオンラインです。アプリケーション全体の同期キューがクリアされるとすぐに、送信が処理されます。
* クライアントはオフラインです。送信はアプリケーション全体の同期キューに追加され、クライアントがオフラインである限り、そこにとどまります。

送信の同期の待機中は、以下のいずれかの状態にあります。
* 保留中: 送信が保留中ですが、編集することはできます。
* 処理: 送信は現在同期中です。 この状態では、ページをこれ以上編集できません。

送信がサーバーに送られた後、次のいずれかの状態になります。
* 同期済み: 送信はサーバーに受け入れられて同期されます。
* エラー: サーバーは、送信を拒否およびページがエラー状態を入力します。

特定のページおよびコンテキストにおいて保留中の送信が複数あり、ページが冪等であるとみなされる場合、集められる (かつ送信される) 場合があります。
これは、サーバーがすべての送信をさまざまな順序で処理する必要はなく、サーバー上のページの設計に依存することを意味します。

## <a name="index"></a>指数

### <a name="enumerations"></a>列挙

* [PageState](../enums/view-model-ipage-pagestate.md)

### <a name="types"></a>種類

* [CompleteEventArgs](../interfaces/view-model-ipage-icompleteeventargs.md)
* [Design](../interfaces/view-model-ipage-idesign.md)
* [NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md)
* [ページ](../interfaces/view-model-ipage-ipage.md)
* [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)
* [PageOptions](../interfaces/view-model-ipage-ipageoptions.md)
* [PageSubmitArgs](../interfaces/view-model-ipage-ipagesubmitargs.md)
* [PageTarget](../interfaces/view-model-ipage-ipagetarget.md)

## <a name="enumerations"></a>列挙


### <a name="pagestate"></a>PageState

#### <a name="enumeration-members"></a>列挙型メンバー

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [エラー](../enums/view-model-ipage-pagestate.md#error) |エラー:  <br>10|ページは現在、エラー状態にありますが、更新することでこの状態から抜け出すことができます。<br>  |
| [読み込み済み](../enums/view-model-ipage-pagestate.md#loaded) |loaded:  <br>3|ページが完全に読み込まれ、更新可能であり、可能ならば送信できます。<br>  |
| [読み込み中](../enums/view-model-ipage-pagestate.md#loading) |loading:  <br>2|ページが現在読み込まれています。<br>  |
| [オフライン](../enums/view-model-ipage-pagestate.md#offline) |offline:  <br>1|ページはオフライン モードで読み込まれたので更新できません。<br>  |
| [更新中](../enums/view-model-ipage-pagestate.md#refreshing) |更新中:  <br>4|ページは現在データを更新中です。<br>  |

## <a name="types"></a>種類


### <a name="completeeventargs"></a>CompleteEventArgs

#### <a name="hierarchy"></a>階層

CompleteEventArgs <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [エラー](../interfaces/view-model-ipage-icompleteeventargs.md#error) |エラー: boolean (省略可)  <br>|  |
| [ナビゲーション](../interfaces/view-model-ipage-icompleteeventargs.md#navigation) |navigation: [NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md) (省略可)  <br>|  |
| [処理済](../interfaces/view-model-ipage-icompleteeventargs.md#processed) |processed: boolean (省略可)  <br>|  |


### <a name="design"></a>デザイン

#### <a name="hierarchy"></a>階層

デザイン <br>&nbsp;&nbsp;&nbsp;└─ [PageLinkDesign](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md) <br>&nbsp;&nbsp;&nbsp;└─ [ContainerControlDesign](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md) <br>&nbsp;&nbsp;&nbsp;└─ [InputControlDesign](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md) <br>&nbsp;&nbsp;&nbsp;└─ [ImageDesign](../interfaces/view-model-control-image-iimage-iimagedesign.md) <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [alignItems](../interfaces/view-model-ipage-idesign.md#alignitems) |alignItems: string (optional)  <br>|このプロパティは、CSS プロパティ「align-items」のエイリアスです。<br>  |
| [alignSelf](../interfaces/view-model-ipage-idesign.md#alignself) |alignSelf: string (optional)  <br>|  |
| [バインディング](../interfaces/view-model-ipage-idesign.md#bindings) |bindings: any (optional)  <br>|  |
| [枠線](../interfaces/view-model-ipage-idesign.md#border) |border: "none" &#124; "solid" &#124; "left" &#124; "right" &#124; "top" &#124; "bottom" (省略可)  <br>|コントロールの境界動作。 このプロパティは、子によって継承されません。<br>  |
| [色](../interfaces/view-model-ipage-idesign.md#color) |color: string (optional)  <br>|コンテナーの前景色。<br>  |
| [flexFlow](../interfaces/view-model-ipage-idesign.md#flexflow) |flexFlow: string (省略可)  <br>|このプロパティを指定すると、コンポーネントがフレックス コンテナー コンポーネントになります。<br>  |
| [flexSize](../interfaces/view-model-ipage-idesign.md#flexsize) |flexSize: string (省略可)  <br>|1 つの番号または 2 つの番号が文字列として書き込まれています。 たとえば、「(サイズを拡大) [(サイズを縮小)]」して、即時フレックス コンテナーの使用可能領域に対応します。<br>  |
| [fontSize](../interfaces/view-model-ipage-idesign.md#fontsize) |fontSize: "medium" &#124; "xx-small" &#124; "x-small" &#124; "small" &#124; "large" &#124; "x-large" &#124; "xx-large" (省略可)  <br>|比例テキスト サイズ<br>  |
| [fontWeight](../interfaces/view-model-ipage-idesign.md#fontweight) |fontWeight: "normal" &#124; "bold" (省略可)  <br>|標準または太字のテキスト。<br>  |
| [justifyItems](../interfaces/view-model-ipage-idesign.md#justifyitems) |justifyItems: "flex-start" &#124; "flex-end" &#124; "center" &#124; "space-between" (省略可)  <br>|このプロパティは CSS プロパティ「justify-content」のエイリアスです。<br>  |
| [ラベル](../interfaces/view-model-ipage-idesign.md#label) |label: string (省略可)  <br>|  |
| [labelPosition](../interfaces/view-model-ipage-idesign.md#labelposition) |labelPosition: "stacked" &#124; "hidden" &#124; "inline" (省略可)  <br>|ラベルの配置方法を決定します (行われる場合)。 既定では、labelPosition が stacked に設定されています。<br>  |
| [名前](../interfaces/view-model-ipage-idesign.md#name) |name: string (省略可)  <br>|  |
| [スペース](../interfaces/view-model-ipage-idesign.md#padding) |padding: "none" &#124; "small" &#124; "std" (省略可)  <br>|コンポーネントのスペース動作を指定できるように許可します。<br>  |
| [タイプ](../interfaces/view-model-ipage-idesign.md#type) |type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|文字列としてのコントロールのタイプ。<br>  |


### <a name="navigationargs"></a>NavigationArgs

#### <a name="hierarchy"></a>階層

[PageTarget](../interfaces/view-model-ipage-ipagetarget.md) <br>&nbsp;&nbsp;&nbsp;└─ NavigationArgs <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [ラベル](../interfaces/view-model-ipage-inavigationargs.md#label) |label: string (省略可)  <br>|  |
| [オプション](../interfaces/view-model-ipage-inavigationargs.md#options) |options: any (省略可)  <br>|  |
| [パラメーター](../interfaces/view-model-ipage-inavigationargs.md#params) |params: [PageOptions](../interfaces/view-model-ipage-ipageoptions.md) (省略可)  <br>|  [PageTarget](../interfaces/view-model-ipage-ipagetarget.md).[params](../interfaces/view-model-ipage-ipagetarget.md#params) から継承 <br> |
| [置換](../interfaces/view-model-ipage-inavigationargs.md#replace) |replace: boolean (省略可)  <br>|true と設定されている場合は、ナビゲーション履歴スタックから現在のビューの起動ナビゲーションを削除します。<br>  |
| [to](../interfaces/view-model-ipage-inavigationargs.md#to) |to: string (省略可)  <br>|  [PageTarget](../interfaces/view-model-ipage-ipagetarget.md).[to](../interfaces/view-model-ipage-ipagetarget.md#to) から継承 <br> |
| [url](../interfaces/view-model-ipage-inavigationargs.md#url) |url: string (省略可)  <br>|指定した場合、このリンクは直接開かれます。<br>  |


### <a name="page"></a>ページ

#### <a name="hierarchy"></a>階層

ページ <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [子](../interfaces/view-model-ipage-ipage.md#children) |children: [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) [ ] <br>|ページのすべての直接の子コントロールの一覧。<br>  |
| [dataLoadedInitially](../interfaces/view-model-ipage-ipage.md#dataloadedinitially) |dataLoadedInitially: Promise &lt;void&gt; <br>|初めてデータが読み込まれたときに解決する約束。<br>  |
| [初期化済み](../interfaces/view-model-ipage-ipage.md#initialized) |initialized: boolean <br>|ページ インスタンスが初期化されている場合は、true です。<br>  |
| [メタデータ](../interfaces/view-model-ipage-ipage.md#metadata) |metadata: [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md) <br>|ページ メタデータ。<br>  |
| [metadataLoaded](../interfaces/view-model-ipage-ipage.md#metadataloaded) |metadataLoaded: Promise &lt;void&gt; <br>|メタデータが読み込みを完了したときに解決する約束。<br>  |
| [pageContext](../interfaces/view-model-ipage-ipage.md#pagecontext) |pageContext: string <br>|現在のページ コンテキスト。<br>  |
| [pageFilter](../interfaces/view-model-ipage-ipage.md#pagefilter) |pageFilter: DataFilter <br>|ページに適用されている現在のフィルター。<br>  |
| [状態](../interfaces/view-model-ipage-ipage.md#state) |state: [PageState](../enums/view-model-ipage-pagestate.md) <br>|ページの現在のステータス。<br>  |
| [syncError](../interfaces/view-model-ipage-ipage.md#syncerror) |syncError: boolean <br>|ページの送信がエラー状態の場合、true です。 これは通常、検証エラーのためにサーバーが送信を拒否した場合に発生します。<br>  |
| [syncPending](../interfaces/view-model-ipage-ipage.md#syncpending) |syncPending: boolean <br>|ページの送信が同期の待機中の場合、true です。<br>  |
| [syncProcessing](../interfaces/view-model-ipage-ipage.md#syncprocessing) |syncProcessing: boolean <br>|ページ インスタンスが現在送信を同期している場合は true です。<br>  |
| [syncUnitEditable](../interfaces/view-model-ipage-ipage.md#syncuniteditable) |syncUnitEditable: boolean <br>|同期の待機中に送信が編集可能な場合、true です。<br>  |
| [タイトル](../interfaces/view-model-ipage-ipage.md#title) |title: string <br>|ページのタイトル。<br>  |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [canSubmit](../interfaces/view-model-ipage-ipage.md#cansubmit) |canSubmit(): boolean|アクション ページが送信可能で、検証エラー メッセージが存在しない場合は、true を返します。<br>  |
| [閉じる](../interfaces/view-model-ipage-ipage.md#close) |close(): void|ページ インスタンスとすべてのライフ サイクルイベントを破棄します。<br>  |
| [getAction](../interfaces/view-model-ipage-ipage.md#getaction) |getAction(actionName: string): [PageLink](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md)|名前でページ アクションを取得します。<br>  |
| [getActions](../interfaces/view-model-ipage-ipage.md#getactions) |getActions(): [PageLink](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md) [ ]|すべてのページ アクションを取得します。<br>  |
| [getControl](../interfaces/view-model-ipage-ipage.md#getcontrol) |getControl(controlName: string): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)|名前でページ コントロールを取得します。<br>  |
| [getDesign](../interfaces/view-model-ipage-ipage.md#getdesign) |getDesign(): [Design](../interfaces/view-model-ipage-idesign.md)|ページに関連付けられているデザイン オブジェクトを取得します。<br>  |
| [getEntityContext](../interfaces/view-model-ipage-ipage.md#getentitycontext) |getEntityContext(): EntityRef|現在のエンティティ コンテキストを取得します。<br>  |
| [isEditable](../interfaces/view-model-ipage-ipage.md#iseditable) |isEditable(): boolean|ページがアクション ページの場合は true を返します<br>  |
| [refreshData](../interfaces/view-model-ipage-ipage.md#refreshdata) |refreshData(): Promise &lt;void&gt;|ページ データを強制更新します。<br>  |
| [経歴](../interfaces/view-model-ipage-ipage.md#resume) |resume(): Promise &lt;void&gt;|一時的停止されたページを再開します。<br>  |
| [送信](../interfaces/view-model-ipage-ipage.md#submit) |submit(): Promise &lt;[CompleteEventArgs](../interfaces/view-model-ipage-icompleteeventargs.md)&gt;|アクションを送信します。<br>  |
| [中断](../interfaces/view-model-ipage-ipage.md#suspend) |suspend(): void|ページを一時的に中断します。<br>  |

#### <a name="events"></a>イベント

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [onClose](../interfaces/view-model-ipage-ipage.md#onclose) |onClose: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;null&gt; <br>|ページを閉じるときに発生するイベント。<br>  |
| [onComplete](../interfaces/view-model-ipage-ipage.md#oncomplete) |onComplete: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;any&gt; <br>|アクションが完了したときに発生するイベント。<br>  |
| [onDataLoaded](../interfaces/view-model-ipage-ipage.md#ondataloaded) |onDataLoaded: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;any&gt; <br>|ページ データが読み込まれたときに発生するイベント。<br>  |
| [onInit](../interfaces/view-model-ipage-ipage.md#oninit) |onInit: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;any&gt; <br>|ページ インスタンスが初期化され、メタデータがロードされたときに発生するイベント。<br>  |
| [onPreInit](../interfaces/view-model-ipage-ipage.md#onpreinit) |onPreInit: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;any&gt; <br>|ページ インスタンスが初期化されたときに発生するイベント。<br>  |
| [onRefresh](../interfaces/view-model-ipage-ipage.md#onrefresh) |onRefresh: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;null&gt; <br>|新しいデータが読み込まれる前に、強制的なページ更新で発生するイベント。<br>  |
| [onStateChange](../interfaces/view-model-ipage-ipage.md#onstatechange) |onStateChange: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;null&gt; <br>|ページ状態が変更するときに発生するイベント。<br>  |
| [onSubmit](../interfaces/view-model-ipage-ipage.md#onsubmit) |onSubmit: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;[PageSubmitArgs](../interfaces/view-model-ipage-ipagesubmitargs.md)&gt; <br>|アクションが送信される前に発生するイベント。 これは、アクションの検証遅延について中断できます。<br>  |
| [onSyncStatusChange](../interfaces/view-model-ipage-ipage.md#onsyncstatuschange) |onSyncStatusChange: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;null&gt; <br>|ページの同期状態が変更するときに発生するイベント。<br>  |


### <a name="pagemetadata"></a>PageMetadata

#### <a name="hierarchy"></a>階層

PageMetadata <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [コントロール](../interfaces/view-model-ipage-ipagemetadata.md#controls) |コントロール: [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md) \[ \] (オプション)  <br>|  |
| [Design](../interfaces/view-model-ipage-ipagemetadata.md#design) |デザイン: [デザイン](../interfaces/view-model-ipage-idesign.md) (オプション)  <br>|  |
| [ID](../interfaces/view-model-ipage-ipagemetadata.md#id) |Id: string (オプション)  <br>|  |
| [QuickSubmit](../interfaces/view-model-ipage-ipagemetadata.md#quicksubmit) |QuickSubmit: ブール値 (省略可)  <br>|  |
| [SourcePageId](../interfaces/view-model-ipage-ipagemetadata.md#sourcepageid) |SourcePageId: 文字列 (省略可)  <br>|  |
| [SubmitButtonDesign](../interfaces/view-model-ipage-ipagemetadata.md#submitbuttondesign) |SubmitButtonDesign: [デザイン](../interfaces/view-model-ipage-idesign.md) (省略可)  <br>|  |
| [仕事](../interfaces/view-model-ipage-ipagemetadata.md#tasks) |タスク: [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)\[\] (省略可)  <br>|  |
| [タイトル](../interfaces/view-model-ipage-ipagemetadata.md#title) |タイトル: 文字列 (省略可)  <br>|  |

#### <a name="events"></a>イベント

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [OnDataLoaded](../interfaces/view-model-ipage-ipagemetadata.md#ondataloaded) |OnDataLoaded: 機能 (送信者: [ページ](../interfaces/view-model-ipage-ipage.md)、dataWrapper: すべて) : 無効 (オプション)  <br>|  |
| [OnInit](../interfaces/view-model-ipage-ipagemetadata.md#oninit) |OnInit: 機能 (送信者: [ページ](../interfaces/view-model-ipage-ipage.md)): 無効 (オプション)  <br>|  |
| [OnPreInit](../interfaces/view-model-ipage-ipagemetadata.md#onpreinit) |OnInit: 機能 (送信者: [ページ](../interfaces/view-model-ipage-ipage.md)): 無効 (オプション)  <br>|  |
| [OnSubmit](../interfaces/view-model-ipage-ipagemetadata.md#onsubmit) |OnSubmit: 機能 (dataValues: すべて、args: すべて): 無効 (オプション)  <br>|  |
| [OnTaskSubmitted](../interfaces/view-model-ipage-ipagemetadata.md#ontasksubmitted) |OnTaskSubmitted: 機能 (taskHandle: すべて、taskOptions: すべて): すべて (オプション)  <br>|  |
| [OnTaskSubmitting](../interfaces/view-model-ipage-ipagemetadata.md#ontasksubmitting) |OnTaskSubmitted: 機能 (taskOptions: すべて): すべて (オプション)  <br>|  |


### <a name="pageoptions"></a>PageOptions

#### <a name="hierarchy"></a>階層

PageOptions <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [appId](../interfaces/view-model-ipage-ipageoptions.md#appid) |appId: string (optional)  <br>|  |
| [デザイン](../interfaces/view-model-ipage-ipageoptions.md#design) |design: [Design](../interfaces/view-model-ipage-idesign.md) (optional)  <br>|  |
| [excludeContext](../interfaces/view-model-ipage-ipageoptions.md#excludecontext) |excludeContext: boolean (省略可)  <br>|  |
| [フィルター](../interfaces/view-model-ipage-ipageoptions.md#filter) |filter: DataFilter (省略可)  <br>|  |
| [filterLocalOnly](../interfaces/view-model-ipage-ipageoptions.md#filterlocalonly) |filterLocalOnly: boolean (省略可)  <br>|  |
| [pageContext](../interfaces/view-model-ipage-ipageoptions.md#pagecontext) |pageContext: string (省略可)  <br>|  |
| [pageId](../interfaces/view-model-ipage-ipageoptions.md#pageid) |pageId: string (省略可)  <br>|  |
| [readOptions](../interfaces/view-model-ipage-ipageoptions.md#readoptions) |readOptions: IReadOptions (省略可)  <br>|  |


### <a name="pagesubmitargs"></a>PageSubmitArgs

#### <a name="hierarchy"></a>階層

PageSubmitArgs <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [dataValues](../interfaces/view-model-ipage-ipagesubmitargs.md#datavalues) |dataValues: any <br>|送信アクションの伝送データを取得します。<br>  |
| [送信者](../interfaces/view-model-ipage-ipagesubmitargs.md#sender) |sender: [Page](../interfaces/view-model-ipage-ipage.md) <br>|送信アクションの送信者ページ インスタンスを取得します。<br>  |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [addMessage](../interfaces/view-model-ipage-ipagesubmitargs.md#addmessage) |addMessage(message: string, type: any): any|表示される検証エラー メッセージを追加します。<br>  |
| [キャンセル](../interfaces/view-model-ipage-ipagesubmitargs.md#cancel) |cancel(): any|アクションの送信を禁止します。<br>  |
| [getMessages](../interfaces/view-model-ipage-ipagesubmitargs.md#getmessages) |getMessages(): string [ ]|以前に追加されたすべてのメッセージを取得します<br>  |
| [isCancelled](../interfaces/view-model-ipage-ipagesubmitargs.md#iscancelled) |isCancelled(): boolean|送信アクションがキャンセルされているかどうかを確認します。<br>  |
| [待機](../interfaces/view-model-ipage-ipagesubmitargs.md#wait) |wait(promise: Promise &lt;any&gt;): any|送信を続行する前に、指定された約束を待ちます。<br>  |


### <a name="pagetarget"></a>PageTarget

#### <a name="hierarchy"></a>階層

PageTarget <br>&nbsp;&nbsp;&nbsp;└─ [NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md) <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [パラメーター](../interfaces/view-model-ipage-ipagetarget.md#params) |params: [PageOptions](../interfaces/view-model-ipage-ipageoptions.md) (省略可)  <br>|  |
| [to](../interfaces/view-model-ipage-ipagetarget.md#to) |to: string (省略可)  <br>|  |



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
---
title: "非推奨 API"
description: "このドキュメントでは、非推奨の API のリストと非推奨の API の移行ガイドを提供しています。"
author: aneesmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 26011
ms.assetid: 15d78841-7ea9-4553-905b-ff850d176d4d
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 0d16243902783722d87ce1a70a287f5acf1db1a4
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="deprecated-apis"></a>非推奨 API

[!include [banner](../includes/banner.md)]

このドキュメントでは、非推奨の API のリストと非推奨の API の移行ガイドを提供しています。

## <a name="overview"></a>概要

Dynamics AX 2012 から API の番号が識別されています。 各 API の非推奨理由はさまざまです。 ほとんどの場合、理由は次のいずれかです。

- 新しいクライアントに適用不可です。
- パフォーマンスを低下させます。
- Chatty (サーバーとクライアントの間で多くの相互トラフィックを引き起こす)。
- 冗長 (フレームワークは自動的にこれらを処理するようになりました)。

次のテーブルを通じて、 <br/>**減価償却の理由** 見出し「クライアント」とは、Microsoft Dynamics 365 for Finance and Operations Web クライアントを指します。

## <a name="list-of-deprecated-apis"></a>非推奨 API のリスト

| オブジェクト | 種類 | 氏名 | 摘要 |
|---|---|---|---|
| ActionPane |方法 |tabChanged | ActionPanes (または ActionPanes の内部コントロール) への更新は、タブが有効になったときではなく、行が有効になったときに実行される必要があります。 |
| ActionPaneTab |方法 | selectionChanged |ActionPaneTabs (または ActionPaneTabs の内部コントロール) への更新は、タブが有効になったときではなく、行が有効になったときに実行される必要があります。 |
| ボックス |方法 |yesNoTextMenu- <br>LinkText | |
| ComboBox |方法 |getEditText |**概要**<br/>該当なし<br/>**減価償却の理由**<br/>冗長。<br/>**移行のメモ**<br/>代わりに getText を使用します。 |
| DataSet DataSetNode DataSetRun |クラス | |**概要**<br/>Dynamics AX 2012 のエンタープライズ ポータルで使用されます。<br/>**減価償却の理由**<br/>クライアントでは適用されません。<h4 ><br/><br/>**移行のメモ**<br/>コードからこれらの API への呼び出しを削除します。 |
| DataSourceMethodInfo <br>DataSourceMethodInfoList |クラス | | |
| DDEClient DDEServer DLL DLLFunction HDC HWnd スレッド WinAPINative WinGDI |クラス | |**概要**<br/>該当なし<br/>**減価償却の理由**<br/>Dynamics AX 2012 Windows クライアントに固有であり、クライアントと互換性がありません。<br/>**移行のメモ**<br/>コードからこれらの API の使用を削除します。 |
| DocumentManagement- <br>ヘルパー |クラス | | |
| フォーム |方法 | addhistory <br>currentHistoryName <br>currentHistoryState <br>updateHistory |**概要**<br/>Dynamics AX 2012 のアドレス バーで使用されます。<br/>**減価償却の理由**<br/>クライアントのナビゲーション モデルが変更されました。<br/><br/>**移行のメモ**<br/>コードからこれらの API への呼び出しを削除します。 |
| フォーム |方法 |arrange | |
| フォーム |方法 |controlCallingMethod | |
| フォーム |方法 |controlMethod- <br>controlMethod- のオーバーロード <br>OverloadObject |**概要**<br/>Dynamics AX 2012 でオーバーライド メソッドを登録するのに使用します。<br/>**減価償却の理由**<br/>これは、オーバーライド メソッドを登録するためのクリーンで推奨された方法ではありません。<br/><br/>**移行のメモ**<br/>代わりに registerOverrideMethod を使用します。 |
| フォーム |方法 |copy cut paste | |
| フォーム |方法 |delAutoCompleteString getAutoCompleteString setAutoCompleteString |**概要**<br/>Dynamics AX 2012 で、自動候補の設定、取得、削除に使用されます。<br/>**減価償却の理由**<br/>Dynamics AX 2012 Windows クライアントに固有です。<br/>**移行のメモ**<br/>コードからこれらの API への呼び出しを削除します。 |
| フォーム |方法 |firstField | |
| フォーム |方法 |formOnTop |**概要**<br/>Dynamics AX 2012 で、ウィンドウとナビゲーションを管理するために使用されます。<br/>**減価償却の理由**<br/>クライアントには新しいナビゲーション モデルがあります。<br/>**移行のメモ**<br/>コードからこれらの API への呼び出しを削除します。 |
| フォーム |方法 |hWnd installMessageProc removeMessageProc |**概要**<br/>該当なし<br/>**減価償却の理由**<br/>Dynamics AX 2012 Windows クライアントに固有であり、クライアントと互換性がありません。<br/>**移行のメモ**<br/>コードからこれらの API の使用を削除します。 |
| フォーム |方法 |isPreloadedInstance |**概要**<br/>Dynamics AX 2012 のプリロードで使用されます。<br/>**減価償却の理由**<br/>プリロードは、クライアントでは適用されません。<br/>**移行のメモ**<br/>コードからこれらの API への呼び出しを削除します。 |
| フォーム |方法 |lastField nextField nextGroup prevField prevGroup | |
| フォーム |方法 |ロック <br>lockWindowUpdate <br>unLock |**概要**<br/>これらのメソッドは、一連の UI 更新を実行する際にウィンドウの再描画を防止するために使用されていました。 これらがない場合、それぞれの変更に応答してウィンドウが再描画され、エンド ユーザー エクスペリエンスが悪化してパフォーマンスが低下します。<br/>**減価償却の理由**<br/>これらのメソッドは Windows クライアントに固有のもので、クライアントにとって必要ではなくなりました。<br/>**移行のメモ**<br/>これらの API の発生を削除するためのコード アップグレード ルールが提供されています。 コードからこれらの API への任意の呼び出しを安全に削除することができます。 |
| フォーム |方法 |print printPreview send |**概要**<br/>Dynamics AX 2012 でフォームの自動レポート生成をオーバーライドするのに使用<br/>**減価償却の理由**<br/>Microsoft Office 365 統合では、クライアントでの強化されたユーザー エクスペリエンスが用意されています。  Dynamics AX クライアント フォームのユーザーは、「エクスポート」機能を使用できます。<br/>**移行のメモ**<br/>コードからこれらの API への呼び出しを削除します。 |
| フォーム |方法 |redraw <br>resetStatusBar- <br>BackgroundColor <br>setStatusBar- <br>BackgroundColor <br>sysColorChanged |**概要**<br/>スタイルや色を制御するのに使用します。<br/>**減価償却の理由**<br/>一貫したビジュアルを実現するために API を通じて色を指定する開発者向けの機能を削除します。<br/>**移行のメモ**<br/>API の再振出の発生を削除するためのコード アップグレード ルールが提供されています。 コードからこれらの API の使用を削除します。 |
| フォーム |方法 |reload | |
| フォーム |方法 |resetSize |**概要**<br/>このメソッドは、コントロールがフォームの追加/削除によってサイズが変更された場合に使用されました。 それがないと、追加/削除コントロールを含めるように、ウィンドウが適切な大きさにならない場合があります。<br/>**減価償却の理由**<br/>これらのメソッドは Windows クライアントに固有のもので、クライアントにとって必要ではなくなりました。<br/>**移行のメモ**<br/>コードからこれらの API への任意の呼び出しを安全に削除することができます。 |
| フォーム |方法 |resize | |
| FormActiveXControl <br>FormAnimateControl <br>FormBuildActiveXControl <br>FormBuildAnimateControl <br>FormBuildManaged- <br>HostControl <br>FormBuildSegmented- <br>EntryControl FormManagedHostControl <br>FormSegmented- <br>EntryControl |クラス | |**概要**<br/>これらは、Dynamics AX 2012 のさまざまなカスタム コントロールをホストまたは作成するために使用されました。<br/>**減価償却の理由**<br/>これらのテクノロジーはクライアントでは機能しません。<br/>**移行のメモ**<br/>アプリケーション開発者はコントロールの拡張機能を使用する必要に応じて、交換コントロールを構築する必要があります。 |
| FormControl |方法 |beginDrag <br>dragDrop <br>dragLeave <br>dragOver <br>dragOverEx <br>dragText <br>drop <br>dropEx <br>dropFile <br>endDrag |**概要**<br/>Dynamics AX 2012 でドラッグ アンド ドロップのシナリオを有効にするために使用します。<br/>**減価償却の理由**<br/>ドラッグ アンド ドロップ のシナリオは、クライアントでサポートされていません。<br/>**移行のメモ**<br/>コードからこれらの API の使用を削除し、ドラッグ アンド ドロップ機能への依存がないシナリオが有効になるようにリファクタリングします。 |
| FormControl |方法 |calcControlSize | |
| FormControl |方法 |command processBase processForm processLink processPicture processTitle |**概要**<br/>Dynamics AX 2012 では廃止としてマークされました。<br/>**減価償却の理由**<br/>該当なし<br/>**移行のメモ**<br/>コードからこれらの API への呼び出しを削除します。 |
| FormControl |方法 |context showContextMenu |**概要**<br/>このメソッドは、コントロールがフォームの追加/削除によってサイズが変更された場合に使用されました。 それがないと、追加/削除コントロールを含めるように、ウィンドウが適切な大きさにならない場合があります。<br/>**減価償却の理由**<br/>これらのメソッドは、Windows クライアントに固有の API に依存していました。<br/>**移行のメモ**<br/>代わりに getContextMenuOptions および selectedMenuOptions を使用します。 |
| FormControl |方法 |copy cut paste | |
| FormControl |方法 |dateTextChange | |
| FormControl |方法 |editControl | |
| FormControl |方法 |hasControl- <br>PositionOverride | |
| FormControl |方法 |helpField | |
| FormControl |方法 |hWnd |**概要**<br/>該当なし<br/>**減価償却の理由**<br/>Dynamics AX 2012 Windows クライアントに固有であり、クライアントと互換性がありません。<br/>**移行のメモ**<br/>コードからこれらの API の使用を削除します。 |
| FormControl |方法 |inputSearch | |
| FormControl |方法 |itemChanging | |
| FormControl |方法 |keyDown | |
| FormControl |方法 |labelMouseDblClick <br>mouseDblClick |**概要**<br/>he FormControl.labelMouseDblClick (int x、int y、int ボタン、Boolean Ctrl, Boolean Shift) メソッドは、コントロールのラベルがダブルクリックされたときに呼び出されます。 マウス ポインターの X、Y 座標、クリックされたマウス ボタンを示すブール値、Ctrl キーと Shift キーが押されたかどうかを示すブール値を提供します。 he FormControl.mouseDblClick (int x、int y、int ボタン、Boolean Ctrl, Boolean Shift) メソッドは、labelMouseDblClick メソッドへの関数と似ています。 違いは、このメソッドはダブル クリック (ラベルだけでなく) があるたびに呼び出されることです。<br/>**減価償却の理由**<br/>ダブルクリック アクションは、Web ベースのアプリケーションとタッチベースのシナリオにはうまく反映されません。 また多くのインスタンスで短くなり終了する可能性があります。<br/>**移行のメモ**<br/>これらのメソッドに推奨される代替は、ボタンと**クリックされた**イベントを使用することです。 |
| FormControl |方法 |labelMousedown labelMouseup mouseDown mouseEnter mouseLeave mouseMove mouseUp |**概要**<br/>マウス イベントを検出したり応答したりするのに使用します。<br/>**減価償却の理由**<br/>これらはタッチ スクリーン フレンドリーではなく、クライアントではサポートされていません。<br/>**移行のメモ**<br/>コードからこれらの API の使用を削除し、マウス イベントへの依存がないシナリオが有効になるようにリファクタリングします。 |
| FormControl | 方法 | onHScroll onVScroll |  |
| FormControl | 方法 | paint |  |
| FormControl | 方法 | prefColumnSize | **概要** <br/>Dynamics AX 2012 で幅と高さを制御するために使用<br/>**減価償却の理由** <br/>クライアントでは適用されません。<br/>**移行のメモ** <br/>代わりに幅と高さを明示的に設定します。 |
| FormControl | 方法 | selectionChanging |  |
| FormControl | 方法 | setScrollInfo |  |
|FormControl | 方法 |  サイズ |  |
| FormControl | 方法 | updateWindow |  |
| FormControl / FormDesign | プロパティ | AcquireFocus |  |
| FormControl / FormDesign | プロパティ | ActiveBackCol ActiveBackColor ActiveBackColorRGB ActiveForeColor ActiveForeColorRGB AlternateRowShading BackgroundColor BackgroundColorRGB BackStyle BackStyleRGB CharacterSet ColorScheme DrawFocusRect ForegroundColor ForegroundColorRGB GridLines GridLinesStyle PromptRect | **概要** <br/>スタイルや色を制御するのに使用します。<br/>**減価償却の理由** <br/>一貫したビジュアルを実現するために API を通じて色を指定する開発者向けの機能を削除します。<br/>**移行のメモ** <br/>コードからこれらの API の使用を削除します。 |
| FormControl / FormDesign | プロパティ | AlignChild AlignChildren AlignControl 境界線 BottomMargin BottomMarginMode ColumnSpace ColumnSpaceMode ColumnSpaceValue 左 LeftMargin LeftMarginMode LeftMode RightMargin RightMarginMode SizeHeight SizeWidth TabAppearance TabAutoChange TabLayout TabMode TabPlacement 上 TopMargin TopMarginMode TopMode VerticalSpacing VerticalSpacingMode VerticalSpacingValue | **概要** <br/>レイアウトを制御するのに使用します。<br/>**減価償却の理由** <br/>このプロパティを使用して一貫性のあるレイアウトを実現するレイアウトを制御するための開発者向けの機能を削除します。<h4 ><br/>**移行のメモ** <br/>コードからこれらの API の使用を削除します。 代わりにスタイルまたは CSS を使用します。 |
| FormControl / FormDesign | プロパティ | AllowDocking AlwaysOnTop ArrangeGuide ArrangeWhen ContainerScroll: <br>HorizontalOffset ContainerScroll- <br>VerticalOffset IMEMode MaximizeBox MinimizeBox Mode NeededAccessLevel ProgressType Securable SecurityKey StatusBarStyle WindowResize |**概要** <br/>該当なし<br/>**減価償却の理由** <br/>Dynamics AX 2012 Windows クライアントに固有であり、必須ではなくなりました。<br/>**移行のメモ** <br/>コードからこれらの API の使用を削除します。 |
| FormControl / FormDesign | プロパティ | 太字 |  |
| FormControl / FormDesign | プロパティ | CanScroll |  |
| FormControl / FormDesign | プロパティ | DisabledImage DisabledImageLocation DisabledResource |  |
| FormControl / FormDesign | プロパティ | DisplayTarget HyperLinkDataSource HyperLinkMenuItem SaveFilter SaveSize | **概要** <br/>Dynamics AX 2012 のエンタープライズ ポータルで使用されます。<br/>**減価償却の理由** <br/>クライアントでは適用されません。<br/>**移行のメモ** <br/>コードからこれらの API への呼び出しを削除します。 |
| FormControl / FormDesign | プロパティ | フォント |  |
| FormControl / FormDesign | プロパティ | フォントサイズ |  |
| FormControl / FormDesign | プロパティ | フレーム FramePosition | **概要** <br/>該当なし<br/>**減価償却の理由** <br/>メタデータを経由してフレームを制御するための開発者向けの機能を削除します。<br/>**移行のメモ** <br/>コードからこれらの API の使用を削除します。 |
| FormControl / FormDesign | プロパティ | HideToolbar HorizontalScrollBarVisible Scrollbars VerticalScrollBarVisible |**概要** <br/>該当なし<br/>**減価償却の理由** <br/>メタデータを経由してスクロールバーを制御するための開発者向けの機能を削除します。<br/>**移行のメモ** <br/>コードからこれらの API の使用を削除します。 |
| FormControl / FormDesign | プロパティ | ImageMode |  |
| FormControl / FormDesign | プロパティ | ImageName |  |
| FormControl / FormDesign | プロパティ | ImageResource |  |
| FormControl / FormDesign | プロパティ | 斜体 |  |
| FormControl / FormDesign | プロパティ | LabelAlignment |  |
| FormControl / FormDesign | プロパティ | LabelBold |  |
| FormControl / FormDesign | プロパティ | LabelCharacterSet |  |
| FormControl / FormDesign | プロパティ | LabelFont |  |
| FormControl / FormDesign | プロパティ | LabelFontSize |  |
| FormControl / FormDesign | プロパティ | LabelForegroundColor LabelForegroundColorRGB |  |
| FormControl / FormDesign | プロパティ | LabelGuide |  |
| FormControl / FormDesign | プロパティ | LabelHeight LabelHeightMode LabelHeightValue |  |
| FormControl / FormDesign | プロパティ | LabelItalic |  |
| FormControl / FormDesign | プロパティ | LabelUnderline |  |
| FormControl / FormDesign | プロパティ | LabelWidth LabelWidthMode LabelWidthValue |  |
| FormControl / FormDesign | プロパティ | 保管場所 |  |
| FormControl / FormDesign | プロパティ | NormalResource |  |
| FormControl / FormDesign | プロパティ | ParentPage |  |
| FormControl / FormDesign | プロパティ | SearchAfterInput SearchMode |  |
| FormControl / FormDesign | プロパティ | SelectControl |  |
| FormControl / FormDesign | プロパティ | SendExternalContext |  |
| FormControl / FormDesign | プロパティ | ShortKey |  |
| FormControl / FormDesign | プロパティ | 下線 |  |
| FormDataRow | クラス |  |  |
| FormDataSource | プロパティ | autoNotify | **概要** <br/>Dynamics AX 2012 では廃止としてマークされました。<br/>**減価償却の理由** <br/>該当なし<br/>**移行のメモ** <br/>コードから使用を削除します。 |
| FormDataSource | 方法 | cacheOnlyMode |  |
| FormDataSource | 方法 | cacheRemoveRecord |  |
| FormDataSource | 方法 | defaultMark |  |
| FormDataSource |方法 |findRecord findValue |**用途** <br/>FormDataSource.findRecord (共通レコード) メソッドは、データ ソース内の特定のレコードを検索し、現在のレコードにします。 FormDataSource.findValue(FieldId field、str 値) メソッドは、データ ソース内の特定のフィールド内の特定の値を検索し、対応するレコードを現在のレコードにします。 これに FormDataSource.findRecord メソッドを使用します。<br/>**減価償却の理由** <br/>これらのメソッドは、線形検索を使用し、メモリ内の多数のレコードをロードし、パフォーマンスに悪影響を与えます。<br/>**移行のメモ** <br/>新しい API で置き換えます。 positionToRecord and findValue を持つ findRecord を positionToRecordByValue に置き換えます。 場合によっては、新しい API は特に一時テーブルおよびビューで機能しません。 そのような場合、フレームワークは例外をスローします。 新しい API との交換が不可能な場合、推奨されている交換は、**element.args(). lookupRecord(recordToFind)**、**FormDataSource.research(false);** を呼び出すことです。これは検索するレコードが含まれているデータ ソースです。 “false” 引数を調査に渡すと、現在の位置を維持しなくなります。args.lookup を使って見つけたレコードに位置が変更されるためです。レコードは、並べ替え順序や範囲などのリセットを回避します。 |
| FormDataSource | 方法 | getDataRow |  |
| FormDataSource | 方法 | markAllLoadedRecords |  |
| FormDataSource | 方法 | maxPagingRowCountValue pagingEnabled startRowIndex setPagingParameters totalNumberOfRows |**概要** <br/>Dynamics AX 2012 のエンタープライズ ポータルで使用されます。<br/>**減価償却の理由** <br/>クライアントでは適用されません。<br/>**移行のメモ** <br/>コードからこれらの API への呼び出しを削除します。 |
| FormDataSource | 方法 | 印刷 |  |
| FormDesign | 方法 | cssClass localWebMenu showWebHelp supportReload |**概要** <br/>Dynamics AX 2012 のエンタープライズ ポータルで使用されます。<br/>**減価償却の理由** <br/>クライアントでは適用されません。<br/>**移行のメモ** <br/>コードからこれらの API への呼び出しを削除します。 |
| FormObjectSetNotify | 方法 | onPaging- <br>ParametersChanged |  |
| FormObjectSetPaging- <br>ParamsChangedEvtArgs | クラス |  |  |
| グローバル xInfo |方法 |endLengthyOperation startLengthyOperation |**概要** <br/>これらのメソッドは、長時間実行されている操作中に進行状況インジケータの表示/停止を示すために使用されました。<br/>**減価償却の理由** <br/>クライアントでは、システムによって自動的に進捗状況インジケータの表示/非表示を調整するため、これらの API への呼び出しは必要ありません。<br/>**移行のメモ** <br/>コードからこれらの API への任意の呼び出しを安全に削除することができます。 |
| 画像 | 方法 |captureScreen captureWindow clipboardCopy clipboardPaste crop displayImage displayOrign exportBitmap flip getImageDimensionUnits getPixel height imageInfo imageSpotlight promoteColor reduceColorOctree resize rotate saveImage saveType transparent width |  |
| ListPage ページ | 方法 |  activeActionPane- <br>TabNames | **概要** <br/>このメソッドを使用して、アクティブなアクション ペイン タブを見つけました。<br/>**減価償却の理由** <br/>クライアントでは、アクション ウィンドウのタブはクライアント側でのみ処理され、サーバーでは状態を把握しません。<h4 ><br/>**移行のメモ** <br/>コードからこの API の使用を削除します。 |
| MessageWin | クラス |  |  |
| オブジェクト | 方法 | notify notifyAll wait | **概要** <br/>対話/操作をブロックして待機し、ブロック解除を通知するのに使用されます。<br/>**減価償却の理由** <br/>これらの呼び出しは、formRun とその派生を除くすべてのオブジェクトで廃止予定です。<br/>**移行のメモ** <br/>formRun からこれらの API への呼び出し、またはその派生が許可されています。  他のオブジェクトからこれらの API への呼び出しを削除する必要があります。 |
| オブジェクト | 方法 | objectOnServer | **概要** <br/>オブジェクトがサーバーにあるかどうかを判断するために使用されます。<br/>**減価償却の理由** <br/>これは冗長であり、すべてのオブジェクトがサーバー上にあるため、もはや必要ありません。<br/>**移行のメモ** <br/>コードからこれらの API への呼び出しを安全に削除することができます。 常に true に評価します。 |
| オブジェクト | 方法 | setTimeOut | **概要** <br/>このメソッドはオブジェクト上に存在しましたが、機能しませんでした。 FormRun の実装は、ロジックの実行を遅らせるタイマーとして使用しました。<br/>**減価償却の理由** <br/>ブラウザー ベースのクライアントは、この実装がサポートしなくなりました。<br/>**移行のメモ** <br/>代わりに FormRun で新しい setTimeOutEx メソッドを使用します。 setTimeOutEx メソッドは、myCallBack(AsyncTaskResult の結果) など、型 AsyncTaskResult のパラメーターを受け入れるためのコールバックを期待していることに注意してください。 |
| PopupMenu | クラス |  | **概要** <br/>Dynamics AX 2012 で、分割された 2 つのパートのサイズをユーザーが変更できるようにするために使用されます。<br/>**減価償却の理由** <br/>Dynamics AX 2012 Windows クライアントに固有であり、クライアントと共に使用できない API に依存します。<br/>**移行のメモ** <br/>代わりに、ContextMenu を使用します。 |
| SysExcel | クラス |  | **概要** <br/>SysExcel クラスは、COM を使用して Excel ブックを作成および編集していました。<br/>**減価償却の理由** <br/>SysExcel は、クライアントからの Excel COM オブジェクトへの呼び出しに依存します。 これらの COM オブジェクトはサーバー上に存在しないため、COM 呼び出しは今後推奨されていません。<br/>**移行のメモ** <br/>代わりに OpenXML .NET framework API を使用します。 X++ から呼び出しやすくするために OpenXML をラップするアセンブリの作成を調査しています。 |
| SysINetMai SysMailer SmmOutlook | クラス |  | **概要** <br/>これらのメール関連のクラスは、利用できなくなりました。または非常に落胆しているクライアント側の技術を主に使用していました。<br/>**減価償却の理由** <br/>SysINetMail クラスは、クライアント側 MAPI を使用していたために非推奨になっています。 SysMailer クラスは、CDO (OLE メッセージングのバリアント) を使用していたために非推奨になります。 SmmOutlook で始まるクラスは、Outlook COM オブジェクトを使用しているため廃止予定です。<br/>**移行のメモ** <br/>SysMailerNet クラスを使用した SMTP 経由の電子メールの送信が今後サポートされます。 また、マイクロソフトは、クライアント側の対話型電子メール機能にも積極的に取り組んでいます。 |
| SysFormSplitter | クラス |  | **概要** <br/>Dynamics AX 2012 で、分割された 2 つのパートのサイズをユーザーが変更できるようにするために使用されます。<br/>**減価償却の理由** <br/>クライアントで不要になりました。<br/>**移行のメモ** <br/>コントロールは自動的に機能を提供します。 コードからこれらの API への任意の呼び出しを安全に削除することができます。 今後コード アップグレード ルールを作成して、使用状況を自動的に削除することができます。 |
| SysListPageHelper | クラス |  |  |
| SysSetupFormRun | クラス |  | **概要** <br/>FormRun を間接的に拡張するためにクラスによって使用されます。<br/>**減価償却の理由** <br/>FormRun クラスと統合されました。<br/>**移行のメモ** <br/>代わりに FormRun クラスを使用します。 |
| TextBuffer | 方法 | fromFile | 代わりに .NET StreamReader クラスを使用します。 |
| TextBuffer | 方法 | toFile | 代わりに .NET StreamWriter クラスを使用します。 |
| スレッド | クラス |  | **概要** <br/>該当なし<br/>**減価償却の理由** <br/>Dynamics AX 2012 Windows クライアントに固有であり、クライアントと互換性がありません。<br/>**移行のメモ** <br/>新しい runAsync メソッドに置き換えるか、コードからこれらの API の使用を削除することを検討してください。 |
| WinAPI | クラス |  | **概要** <br/>該当なし<br/>**減価償却の理由** <br/>Dynamics AX 2012 Windows クライアントに固有であり、クライアントと互換性がありません。<br/>**移行のメモ** <br/>コードからこれらの API の使用を削除します。 WinAPI::getTempPath、WinAPI::fileExists など、ファイル アクセス API を新しいファイル API に置き換えます。 |
| WinAPIServer | 方法 | cryptProtectData cryptUnprotectData | **概要** <br/>WinAPIServer::cryptProtectData (CryptoBlob \_unEncryptedDataBlob) および WinAPIServer::cryptUnProtectData (CryptoBlob \_encryptedDataBlob) メソッドを使用して、機密データの暗号化および復号化が行われました。<br/>**減価償却の理由** <br/>これらのメソッドは、デスクトップの使用に最適で、Web ベースのアプリケーションの使用には推奨されません。 また、パフォーマンスに悪影響を及ぼします。<br/>**移行のメモ** <br/>代わりに .NET フレームワーク API とよく知られたハッシュ/セキュリティ アルゴリズムを使用します。 |
| xApplication | 方法 | runAsync | **概要** <br/>Dynamics AX 2012 では、xApplication::runAsync メソッドがメソッドに対する非同期呼び出しに使用されていました。<br/>**減価償却の理由** <br/>クライアントに適したメソッドに置き換えられます。<br/>**移行のメモ** <br/>代わりに、Global クラスまたは FormRun クラスで runAsyncメ ソッドを使用します。 これらの新しいバージョンの runAsync を使用すると、呼び出し元は静的な X++ クラス メソッドへの非同期呼び出しを行うことができます。 これらは、.NET System.Threading.Tasks ライブラリを利用して、X++ で非同期メソッドを実行します。  System.Threading.Tasks.Task タイプを使用することで、開発者は .NET で利用可能な豊富な機能を利用できます。 |
| xGlobal | 方法 | clientKind | **概要** <br/>通常、インタラクティブ セッションなどのクライアントの存在を検出するために使用します。<br/>**減価償却の理由** <br/>クライアントに適したメソッドに置き換えられます。<br/>**移行のメモ** <br/>代わりに global :: hasGUI メソッドを使用します。 |
| xGlobal | 方法 | computerName |  |
| xGlobal | 方法 | forceFormPreload | **概要** <br/>Dynamics AX 2012 のプリロードで使用されます。<br/>**減価償却の理由** <br/>プリロードは、クライアントでは適用されません。<br/>**移行のメモ** <br/>コードからこれらの API への呼び出しを削除します。 |
| xGlobal | 方法 | terminalServer |  |
| xInfo | 方法 | directory |  |
| xInfo | 方法 | navPane |  |
| XmlDocument | 方法 | LoadSave |  |
| XmlWriter | 方法 | CreateNewFile |  |
| [XppCompiler] | クラス |  |  |



---
title: 移行後のフォームのフォーム パターン
description: このトピックでは、移行するフォームに最適なフォーム パターンを選択するのに役立つ情報を提供します。
author: jasongre
ms.date: 11/09/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 28681
ms.assetid: 09a51876-8c9d-41ed-ab81-b780894a4281
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dabc9db8cac7f73f91da08dcc8a6ba060ee365176cb56755f5227726d2d41ba3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733095"
---
# <a name="form-patterns-for-migrated-forms"></a>移行後のフォームのフォーム パターン

[!include [banner](../includes/banner.md)]

このトピックでは、移行するフォームに最適なフォーム パターンを選択するのに役立つ情報を提供します。 

## <a name="introduction"></a>はじめに

フォームパターンの選択は、フォームを移行するプロセスの重要なステップです。 ターゲット フォームに最適なパターンでは、必要な移行作業の量が減少します。 対照的に、適切ではないパターンは無駄な時間と労力を引き起こす可能性があります。 したがって、移行するフォームに最適なフォーム パターンを選択できるよう、調査を行うことが重要です。 フォームの適切なパターンを決定するためのガイダンスおよびヒントを次に示します。

-   フォーム デザイナーでフォームのメタデータを調べます。 よく注意して次の詳細を閉じてください。
    -   フォーム名
    -   Form.Design.Style
    -   コントロール名
    -   コントロールが整理される方法
    -   番号とデータ ソースの名前
-   フォームを実行して、情報が表示される方法を確認することでフォームのビジュアルを調べます。

## <a name="selecting-a-form-pattern-via-metadata"></a>メタデータを通じてフォーム パターンを選択
### <a name="use-formdesignstyle-for-guidance"></a>ガイダンスに Form.Design.Style を使用

**Form.Design.Style** プロパティには多くの場合、フォームの以前対象となっていたパターンの名前が含まれています。 **スタイル** プロパティはメタデータと正確に一致し、次の表を使用して、フォームに適合する可能性があるパターンを検出することができます。

| Form.Design.Style value                                                                          | 対応するパターン                                                                                           |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| DetailsFormMaster                                                                                | [詳細マスター](details-master-form-pattern.md)                              |
| DetailsFormTransaction                                                                           | [詳細トランザクション](details-transaction-form-pattern.md)                    |
| ダイアログ                                                                                           | [ダイアログ](dialog-form-pattern.md)                                              |
| DropDialog                                                                                       | [ドロップ ダイアログ](drop-dialog-form-pattern.md)                                    |
| 単なるフィールドが存在する FormPart                                                            | [フォーム パート 情報ボックス カード](factbox-form-patterns.md)                            |
| グリッドが存在する FormPart                                                                  | [フォーム パート 情報ボックス グリッド](factbox-form-patterns.md)                            |
| ListPage                                                                                         | [リスト ページ](list-page-form-pattern.md)                                        |
| ルックアップ                                                                                           | [ルックアップ](lookup-form-pattern.md)                                              |
| SimpleList                                                                                       | [簡易リスト](simple-list-form-pattern.md)                                    |
| ナビゲーション リストにフィールドが 2 ～ 3 個の場合は SimpleListDetails (推奨)               | [簡易リストと詳細 – リスト グリッド](simple-list-details-form-pattern.md)    |
| ナビゲーション リストにフィールドが 4 ～ 5 個の場合は SimpleListDetails                         | [簡易リストと詳細 – 表形式のグリッド](simple-list-details-form-pattern.md) |
| ツリーがある場合は SimpleListDetails (まれ)                                                  | [簡易リストと詳細 – ツリー](simple-list-details-form-pattern.md)         |
| TableOfContents                                                                                  | [目次](table-of-contents-form-pattern.md)                        |
| 自動には **概要** タブ、**一般** タブ、および単一のデータ ソースが存在する            | [タスク シングル](task-single-form-pattern.md)                                    |
| 自動には **概要** タブ、**一般** タブ、またはヘッダーを含めたラインの 2 つのセットが存在する | [タスク ダブル](task-double-form-pattern.md)                                    |
| 自動には1 つのレコードにフォーカスが存在する                                                    | [簡易詳細](simple-details-form-pattern.md)                              |
| 自動には「ルックアップ」で終了するフォーム名が存在する                                                       | [ルックアップ](lookup-form-pattern.md)                                              |
| 自動には 1 つのタブ コントロールと **次へ**/**前へ** ボタンがある                      | [ウィザード](wizard-form-pattern.md)                                              |
| 自動には「ウィザード」で終了するフォーム名が存在する                                                       | [ウィザード](wizard-form-pattern.md)                                              |
| 自動にはグリッドとボタンが存在する                                                | [簡易リスト](simple-list-form-pattern.md)                                    |

###  <a name="when-a-form-doesnt-match-the-style-property"></a>フォームが Style プロパティと一致しないとき

場合によっては、フォームに間違った **Form.Design.Style** プロパティ値があります。

| Form.Design.Style value | 可能性のあるフォームの実際の値                                                                                  |
|-------------------------|------------------------------------------------------------------------------------------------------------------|
| DetailsFormMaster       | DetailsFormTransaction、明細行の詳細がある場合、またはコントロールの名前に「明細行」を含む場合                 |
| SimpleList              | グリッドが複数といくつかのカスタム フィルター フィールドがある場合は SimpleListDetails。                               |
| SimpleListDetails       | グリッドが 1 つだけといくつかのカスタム フィルター フィールドがある場合は SimpleList。                                                |
| SimpleList              | ListPage、**パーツ** ノードに数多くの情報ボックスがある場合、または対応する詳細フォームがそのフォームにある場合 |

## <a name="selecting-a-form-pattern-via-visuals"></a>ビジュアルを通じてフォーム パターンを選択
この方法はフォームのメタデータを見るよりもあまり役に立ちませんが、フォームについて実行し調べることによってさまざまな情報を取得することができます。 追加のデータ ポイントとしてフォーム ビジュアルを使用すると、フォーム パターンを選択するのに役立ちます。 ターゲット フォームのようなフォームを見つけるために、移行したフォームのスクリーン ショットを参照します。 また、パターンの記述または目的がフォームの説明/目的と一致していることを確認してください。

## <a name="selecting-a-form-pattern-via-the-designer"></a>デザイナーを通じてフォーム パターンを選択

ターゲット フォームの **デザイン** ノードを右クリックし、**パターンの適用** を選択して適用するパターンをクリックします。

## <a name="form-pattern-reference-guide"></a>フォームのパターンの参照ガイド
### <a name="list-of-classes-of-top-level-form-patterns"></a>最上位レベルのフォーム パターンのクラスのリスト

| フォーム パターン                                                                                                        | これは何に使用されますか ?                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [詳細マスター](details-master-form-pattern.md) (2 つのバリアント)                   | 複雑なエンティティの詳細を表示するフォーム                                                                  |
| [詳細トランザクション](details-transaction-form-pattern.md)                        | このフォームは、複雑なトランザクション エンティティとその行の詳細 (例えば、注文とその行) を表示します。 |
| [ダイアログ](dialog-form-pattern.md) (6 バリアント)                                   | 一連の情報を収集するダイアログとして使用されるフォーム                                                        |
| [ドロップ ダイアログ](drop-dialog-form-pattern.md) (2 つのバリアント)                         | アクションにコンテキストを提供するための小さな情報のセットを収集するためにドロップ ダイアログとして使用されるフォーム            |
| [情報ボックス](factbox-form-patterns.md) (2 つのバリアント)                                | 関連するレコードまたはレコードのセットに関する情報を表示する Microsoft Dynamics AX 2012 FactBox。               |
| [リスト ページ](list-page-form-pattern.md)                                            | Dynamics AX 2012 のリスト ページ                                                                                          |
| [ルックアップ](lookup-form-pattern.md) (3 バリアント)                                 | ルックアップとして使用されるフォーム                                                                                       |
| [簡易詳細](simple-details-form-pattern.md) (4 バリアント)                  | 1 つのレコードに特化したフォーム                                                                             |
| [簡易リスト](simple-list-form-pattern.md)                                        | レコードあたり 10 未満のフィールドが含まれるグリッドとして簡易エンティティの詳細を表示するフォーム                   |
| [簡易リストと詳細](simple-list-details-form-pattern.md) (3 バリアント) | 中規模な複雑さのエンティティに関する情報を表示するフォーム                                                 |
| [目次](table-of-contents-form-pattern.md)                            | セットアップ情報または大まかに関連する情報のセットが表示されるフォーム                                            |
| タスク (2 つのバリアント)                                                                                                 | レガシ フォーム パターンは、マスタ エンティティまたはトランザクション エンティティを表示するために使用します。                                          |
| [ウィザード](wizard-form-pattern.md)                                                  | 一定の順序に従って情報を収集するユーザーに一連のタブ ページを表示するフォーム                    |
| [運用ワークスペース](workspace-form-pattern.md)                                | 活動の概要を表示するために使用され、ナビゲーションの主な手段を意味するフォーム            |
| ワークスペース パノラマ セクション (3 バリアント)                                                                        | 運用ワークスペースに (フォームのパーツ コントロールを通じて) パノラマ セクションに内容を表示するためのフォーム     |

### <a name="finding-forms-that-currently-use-a-particular-form-pattern"></a>特定のフォーム パターンを現在使用しているフォームを検索

特定のフォーム パターンを現在使用しているフォームの一覧全体については、Microsoft Visual Studio 内から **フォーム パターン** レポートを生成します。 レポートを実行する詳細については、[フォーム パターン アドイン](form-pattern-add-ins.md) を参照してください。Excel でレポートをフィルター処理し、特定のパターンを使用するフォームを検索できます。

### <a name="form-pattern-visuals-and-descriptions"></a>フォームのパターンのビジュアルと説明

フォーム パターン クラスごとに、各バリアントに関する情報が提供されます。 この情報には、簡単な説明と例フォームの図が含まれています。

#### <a name="details-master"></a>詳細マスター

[詳細マスター](details-master-form-pattern.md)\[既定\] このフォーム パターンは、クイック タブ上の複雑なエンティティの詳細を表示するために使用します。 グリッド ビューと詳細ビューが含まれています。

フォーム: CustTable 

![詳細マスター フォーム。](./media/image001.jpg)

![詳細マスター フォーム。](./media/image002.jpg)

[詳細マスター / 標準タブ](details-master-form-pattern.md) フォームに多数のクイック タブ (>15) があり、カテゴリにグループ化できる場合は、この詳細マスター バリアントを使用します。

フォーム: HcmWorker 

[![標準タブ フォーム付きの詳細マスター。](./media/image003.jpg)](./media/image003.jpg)

[![標準タブ フォーム付きの詳細マスター。](./media/howtoselectaformpattern-31.jpg)](./media/howtoselectaformpattern-31.jpg)



#### <a name="details-transaction"></a>詳細トランザクション

[詳細トランザクション](details-transaction-form-pattern.md) このフォーム パターンを使用して、複雑なトランザクションエンティティとその行の詳細 (例えば、注文とその行) を表示します。

フォーム: SalesTable 

[![詳細トランザクション フォーム。](./media/howtoselectaformpattern-32.jpg)](./media/howtoselectaformpattern-32.jpg)

[![詳細トランザクション フォーム。](./media/howtoselectaformpattern-33.jpg)](./media/howtoselectaformpattern-33.jpg)



#### <a name="dialog"></a>ダイアログ

[ダイアログ – 基本](dialog-form-pattern.md)\[既定\] このフォームのパターンは一連の情報を収集または表示するために使用します。

フォーム: ProjTableCreate

[![ダイアログ - 基本フォーム。](./media/howtoselectaformpattern-34.jpg)](./media/howtoselectaformpattern-34.jpg)

[ダイアログ – 読み取り専用](dialog-form-pattern.md) ダイアログが編集できない情報だけを表示する場合は、このダイアログバリアントを使用します。 **閉じる** ボタンだけがあります。

フォーム: SalesTablePostings

[![ダイアログ - 読み取り専用フォーム。](./media/howtoselectaformpattern-35.jpg)](./media/howtoselectaformpattern-35.jpg)

[ダイアログ – クイック タブ](dialog-form-pattern.md) ダイアログの内容がクイック タブにグループ化されている場合は、このダイアログ バリアントを使用します。

現在、製品にはありません。

[![ダイアログ - FastTabs フォーム。](./media/howtoselectaformpattern-36.jpg)](./media/howtoselectaformpattern-36.jpg)

[ダイアログ – タブ](dialog-form-pattern.md) ダイアログの内容をタブにグループ化する必要がある場合は、このダイアログ バリアントを使用します。

フォーム: CaseDetailCreate

![ダイアログ - タブ フォーム。](./media/howtoselectaformpattern-37.jpg)

[ダイアログ – 二重タブ](dialog-form-pattern.md) ダイアログコンテンツに2つのタブが重ねて表示されている場合は、このダイアログバリアントを使用します。

フォーム: PurchTableReferences

![ダイアログ - 二重タブ フォーム。](./media/howtoselectaformpattern-38.jpg)



#### <a name="drop-dialog"></a>ドロップ ダイアログ

[ドロップ ダイアログ](drop-dialog-form-pattern.md)\[既定\] このフォーム パターンは、フィールド数が少ない場合 (5 未満) にアクションを開始するために使用します。

フォーム: CustCollectionsNewActivityAction

[![ドロップ ダイアログ フォーム。](./media/howtoselectaformpattern-39.jpg)](./media/howtoselectaformpattern-39.jpg)

[ドロップ ダイアログ – 読み取り専用](drop-dialog-form-pattern.md) ドロップ ダイアログのフィールドが編集できない場合は、このドロップ ダイアログ バリアントを使用します。 **OK**/**閉じる** ボタンはモデル化されません。

現在、例が製品に存在しません。

#### <a name="factbox"></a>情報ボックス

[FactBox グリッド](factbox-form-patterns.md) このFactBox バリアントを使用して、関連情報の子コレクションを表示します。

フォーム: ContactsInfoPart

![FactBox フォーム。](./media/howtoselectaformpattern-40.jpg)

[情報ボックス カード](factbox-form-patterns.md) この情報ボックス バリアントを使用して、一連の関連フィールドを表示します。

フォーム: CustStatisticsStatistics

![FactBox カード。](./media/howtoselectaformpattern-41.jpg)

#### <a name="list-page"></a>リスト ページ

[リスト ページ](list-page-form-pattern.md) Dynamics AX 2012 のリストページは、レコード閲覧とそのレコードの操作に最適化されたグリッドです。

フォーム: SalesTableListPage

![リスト ページ フォーム。](./media/howtoselectaformpattern-42.jpg)

#### <a name="lookup"></a>ルックアップ

[基本のルックアップ](lookup-form-pattern.md)\[既定\] このフォーム パターンは、ルックアップ フォームが下部にオプションのフィルターまたはボタンを持つグリッドまたはツリーである場合に使用されます。

フォーム: SysLanguageLookup

[![ルックアップの基本フォーム。](./media/howtoselectaformpattern-43.jpg)](./media/howtoselectaformpattern-43.jpg)

[プレビュー付きのルックアップ](lookup-form-pattern.md) このルックアップ バリアントを使用して、ときに、基本的なパターンだけでなく、現在のレコードのプレビューが表示されます。

フォーム: HcmWorkerLookup

![プレビュー フォーム付きルックアップ。](./media/howtoselectaformpattern-44.jpg)

[タブ付きのルックアップ](lookup-form-pattern.md) ルックアップの複数のビュー (グリッドビュー / ツリービュー、複数のフィルタリングされたリストなど) がある場合は、このルックアップ バリアントを使用します。

フォーム: CaseCategoryLookup

![タブ フォーム付きルックアップ。](./media/howtoselectaformpattern-45.jpg)



#### <a name="panorama-section"></a>パノラマ セクション

[フォーム パート セクション リスト](section-list-form-pattern.md) このフォーム パターンを使用して、ワークスペース セクションにリストを表示します。 これは別のフォームとしてモデル化し、フォーム パーツ コントロールを介してワークスペースにレンダリングする必要があります。

[フォーム パート セクション リスト - ダブル](section-list-form-pattern.md) セカンダリ リストを表示する必要がある場合は、このバリアントを使用します。 このセカンダリ リストは最初は表示されません。

[ハブ パート グラフ](section-chart-form-pattern.md) このバリアントを使用して、ワークスペース セクション にグラフを表示します。 これは別のフォームとしてモデル化し、フォーム パーツ コントロールを介してワークスペースにレンダリングする必要があります。

フォーム: VendInvoiceJourCountChart

[![例。](./media/howtoselectaformpattern-1.jpg)](./media/howtoselectaformpattern-1.jpg)



#### <a name="simple-details"></a>簡易詳細

[ツールバーおよびフィールド付き簡易詳細](simple-details-form-pattern.md) このフォーム パターンを使用して、単一の基本レコードのフィールドを表示します。

フォーム: AgreementLine

![ツールバーおよびフィールド フォーム付き簡易詳細。](./media/howtoselectaformpattern-2.jpg)

[クイック タブ付き簡易詳細](simple-details-form-pattern.md) レコードの情報がクイック タブにまとめられている場合は、この簡易詳細バリアントを使用します。

フォーム: PlanActivityServiceDetails

![FastTabs フォーム付き簡易詳細。](./media/howtoselectaformpattern-3.jpg)

[標準タブ付き簡易詳細](simple-details-form-pattern.md) レコードの情報が通常のタブにまとめられている場合は、この簡易詳細バリアントを使用します。

フォーム: HcmEmploymentDateManager

![標準タブ フォーム付き簡易詳細。](./media/howtoselectaformpattern-4.jpg)

[パノラマ付き簡易詳細](simple-details-form-pattern.md) この簡易詳細バリアントを使用して、水平方向にスクロールするパノラマにレコードの情報を表示します。

フォーム: PdsMRCEventTracker

![パノラマ フォーム付き簡易詳細。](./media/howtoselectaformpattern-5.jpg)


#### <a name="simple-list"></a>簡易リスト

[簡易リスト](simple-list-form-pattern.md) このフォーム パターンは簡易エンティティのデータを管理するために使用します。

フォーム: CustGroup

![簡易リスト フォーム。](./media/howtoselectaformpattern-6.jpg)



#### <a name="simple-list-and-details"></a>簡易リストと詳細

[簡易リストと詳細 – リスト グリッド](simple-list-details-form-pattern.md)\[既定\] このフォーム パターンは中程度の複雑さのエンティティのデータを管理するために使用します。 ナビゲーション リストの 2 ～ 3 フィールドが含まれるリスト グリッドは、現在のバージョンでは、このフォーム スタイルの優先パターンです。

フォーム: PaymTerm

![HowToSelectAFormPattern (7).](./media/howtoselectaformpattern-7.jpg)

[簡易リストと詳細 – 表形式のグリッド](simple-list-details-form-pattern.md) この簡易リストと詳細のバリアントは、フォームのリスト部分に 3 つ以上のフィールドが必要な場合に使用します。

フォーム: ExchangeRate

![簡易リストと詳細 – 表形式のグリッド フォーム。](./media/howtoselectaformpattern-8.jpg)

[簡易リストと詳細 – ツリー](simple-list-details-form-pattern.md) フォームのリスト部分がツリーの場合は、この簡易リストと詳細のバリアントを使用します。

フォーム: FiscalCalendars

![簡易リストおよび詳細 - ツリー フォーム。](./media/howtoselectaformpattern-9.jpg)



#### <a name="table-of-contents"></a>目次

[目次](table-of-contents-form-pattern.md) このフォーム パターンを使用して、設定情報または大まかに関連する情報のセットを表示します。

フォーム: CustParameters

![目次フォーム。](./media/howtoselectaformpattern-10.jpg)



#### <a name="task"></a>タスク

[タスク シングル](task-single-form-pattern.md) このレガシ フォーム パターンは、エンティティを表示するために使用します。 これは、新しいフォームではなく、移行にのみ使用する必要があります。

フォーム: LedgerJournalTable

![タスク シングル フォーム。](./media/howtoselectaformpattern-11.jpg)

[タスク ダブル](task-double-form-pattern.md) このレガシ フォーム パターンは、トランザクション エンティティを表示するために使用します。 これは、新しいフォームではなく、移行にのみ使用する必要があります。

フォーム: HRMAbsenceTableHistory

![タスク ダブル フォーム。](./media/howtoselectaformpattern-12.jpg)



#### <a name="wizard"></a>ウィザード

[ウィザード](wizard-form-pattern.md) このフォーム パターンはあらじめ設定された順序で情報を収集するために、ユーザーに一連のページ ビューを表示するために使用します。

フォーム: WrkCtrBulkResReqEditWizard

![ウィザード フォーム。](./media/howtoselectaformpattern-13.jpg)



#### <a name="workspace"></a>ワークスペース

[運用ワークスペース](workspace-form-pattern.md)\[既定\] これは、ワークスペース パターンで推奨されているパフォーマンスが向上したバリアントです。

フォーム: FmClerkWorkspace

![運用ワークスペース フォーム。](./media/howtoselectaformpattern-1.png)

ワークスペース: これは古いワークスペース パターンです。 これはまもなく削除されるため、使用しないでください。 ここでは完全を期すためだけに含まれています。

使用しないでください。

## <a name="subpattern-reference-guide"></a>サブパターン参照ガイド
### <a name="list-of-subpattern-classes"></a>サブパターン クラスのリスト

| フォーム パターン                                                                                                     | これは何に使用されますか ?                                                                                  |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [カスタム フィルター](custom-filter-group-subpattern.md) (2 つのバリアント)             | QuickFilters およびその他のモデル化されたカスタム フィルターを表示するコンテナー (複数)                           |
| フィールド (5 つのバリアント)                                                                                           | 主に個々のフィールドを表示するコンテナー (複数)                                                 |
| [分析コード式ビルダー](../financial/dimension-expression-builder-subpattern.md)     | 分析コード式ビルダー コントロールを含むコンテナー (複数)                                      |
| [分析コード エントリ コントロール](../financial/dimension-entry-control-subpattern.md)               | 分析コード エントリ コントロールを含むコンテナー (複数)                                                   |
| [リスト パネル](list-panel-subpattern.md)                                         | ユーザーがアイテムを移動する 2 つのリストを表示するコンテナー (複数)                                     |
| [入れ子になった簡易リストおよび詳細](nested-simple-list-details-subpattern.md) | 簡単な簡易リストと詳細フォームをフォームのセクション内に埋め込むために使用されるコンテナー (複数) |
| [ツールバーおよびフィールド](toolbar-fields-subpattern.md)                         | フィールド セットの上にアクションを表示するコンテナー (複数)                                               |
| [ツールバーおよびリスト](toolbar-list-subpattern.md) (2 バリアント)              | 1 ～ 2 グリッドを超えるアクションを表示するコンテナー (複数)                                                     |
| ワークスペース関連 (8 バリアント)                                                                               | 操作可能なワークスペース内のさまざまなセクションに対応するコンテナー (複数)                      |

### <a name="finding-containers-that-require-that-a-subpattern-be-applied-on-a-form"></a>フォーム上で適用されるサブパターンが必要なコンテナーの検索

フォームが Visual Studio デザイナーで開かれていると、デザイナーの上部にあるコントロール検索ボックスで「指定されていません」を検索することによって、まだサブパターンを適用する必要のあるコンテナーを簡単に検索できます (次のスクリーン ショットに図示)。

[![コンテナーを検索する。](./media/howtoselectaformpattern-15.jpg)](./media/howtoselectaformpattern-15.jpg)

### <a name="subpattern-visuals-and-descriptions"></a>サブパターンのビジュアルと説明

サブパターン クラスごとに、各バリアントに関する情報が提供されます。 この情報には、簡単な説明と例フォームの図が含まれています。

#### <a name="custom-filters"></a>カスタム フィルター

[カスタム フィルター](custom-filter-group-subpattern.md) カスタム フィルターがモデル化されている場合は、このフォーム パターンを使用します。 QuickFilter は必要ありません。

フォーム: LedgerJournalTable (TopFields)

![カスタム フィルター フォーム。](./media/howtoselectaformpattern-16.jpg)

[カスタムと クイック フィルター](../financial/dimension-entry-control-subpattern.md) QuickFilter が必要な場合は、このバリアントを使用します。

フォーム: CustTable (CustomFilterGroup)

![カスタムおよびクイック フィルター フォーム。](./media/howtoselectaformpattern-17.jpg)



#### <a name="fields"></a>フィールド

[フィールドおよびフィールド グループ](fields-field-groups-subpattern.md) このフォーム パターンを使用して、フィールドのみを含むコンテナーの応答レイアウトを取得します。

フォーム: InventLocation (LocationNames)

![フィールドおよびフィールド グループ フォーム。](./media/howtoselectaformpattern-18.jpg)

[表形式フィールド](tabular-fields-subpattern.md) このフォーム パターンを使用して、フィールドの構造化されたレイアウトを取得します。 主に合計のためです。

フォーム: LedgerJournalTransVendPaym (残高)

![表形式フィールド フォーム。](./media/howtoselectaformpattern-19.jpg)

[テキスト入力](fill-text-subpattern.md) このフォーム パターンは、単一入力コントロールで全幅が必要な場合に使用します。

フォーム: FmRental (メモ)

![テキスト フォームの入力。](./media/howtoselectaformpattern-20.jpg)

[水平フィールドおよびボタン グループ](horizontal-fields-buttons-group-subpattern.md) フィールドにインライン アクションがある場合は、このフォーム パターンを使用します。

フォーム: SalesTable (GroupHeaderAddressHeaderOverview)

![水平フィールドおよびボタン グループ フォーム。](./media/howtoselectaformpattern-21.jpg)

[画像のプレビュー](image-preview-subpattern.md) このフォーム パターンは、イメージ コントロール (およびオプションの関連フィールド) を持つコンテナーに使用します。

フォーム: RetailVisualProfile (ログイン)

![画像のプレビュー フォーム。](./media/howtoselectaformpattern-22.jpg)



#### <a name="toolbar-and-list"></a>ツールバーおよびリスト

[ツールバーおよびフィールド](toolbar-list-subpattern.md) アクションとグリッドのみを持つコンテナーでこのフォーム パターンを使用します。

フォーム: VendTable (TabCommunication)

![ツールバーおよびリスト フォーム。](./media/howtoselectaformpattern-23.jpg)

[ツールバーおよびリスト: 二重](toolbar-list-subpattern.md) コンテナーに2 つのグリッドがある場合、このツールバーおよびリスト バリアントを使用します。

フォーム: SalesQuickQuote (TabPageExistingItems)

![ツールバーおよびリスト - ダブル フォーム。](./media/howtoselectaformpattern-24.jpg)



#### <a name="workspace-related"></a>関連するワークスペース

[セクション タイル](section-tiles-subpattern.md) このバリアントを使用して、ワークスペースのセクションに一連のタイル/グラフを表示します。 これは、ワークスペース フォームのタブ ページでモデル化する必要があります。 グラフはフォーム パーツ コントロールを使用して定義されます

フォーム: SalesOrderProcessingWorkspace

![セクション タイル フォーム。](./media/howtoselectaformpattern-25.jpg)

[セクション関連リンク](section-related-links-subpattern.md) このバリアントを使用して、ワークスペースのセクションに一連のハイパーリンクを表示します。 これは、ワークスペース フォームのタブ ページでモデル化する必要があります。

フォーム: SalesOrderProcessingWorkspace

![セクション関連リンク フォーム。](./media/howtoselectaformpattern-26.jpg)

[セクション タブ付きリスト](section-tabbed-list-subpattern.md) 複数のリスト バリアントを含める必要がある場合に、このバリアントを使用します。 一度に 1 つだけ表示されます。

[セクション積み上げグラフ](section-stacked-chart-subpattern.md) 運用ワークスペースに 2 つのグラフを含める必要がある場合に、このバリアントを使用します。

[セクション PowerBI](section-powerbi-subpattern.md) Power BI セクションを含める必要がある場合に、このバリアントを使用します。

[ワークスペース ページ フィルター グループ](workspace-filter-group-subpattern.md) このフォームのパターンを使用して、ワークスペースに 1 つのフィルターを追加します。

[フィルターおよびツールバー – 積み上げ](filters-toolbar-subpattern.md) このサブパターンをフォーム パート セクション リスト パターンで使用すると、フィルターの下にアクションが表示されます。

[フィルターおよびツール バー – インライン](filters-toolbar-subpattern.md) このサブパターンをフォーム パート セクション リスト パターンで使用すると、フィルターとアクションが同じ行に表示されます。



#### <a name="other"></a>外

[入れ子になった簡易リストおよび詳細](nested-simple-list-details-subpattern.md) このフォーム パターンを使用すると、よりシンプルな簡易リストと詳細フォームをタブまたはグループ内に埋め込むことができます。

フォーム: HcmJob (TaskTabPage)

![入れ子になった簡易リストおよび詳細フォーム。](./media/howtoselectaformpattern-27.jpg)

[リスト パネル](list-panel-subpattern.md) このフォーム パターンは、ユーザーが 2 つのリストの間でアイテムを前後に移動する必要がある場合に使用します。

フォーム: CLIControls\_ListPanel (FormTabPageControl1)

![リスト パネル フォーム。](./media/howtoselectaformpattern-28.jpg)

[ツールバーおよびフィールド](toolbar-fields-subpattern.md) アクションとフィールドのみを持つコンテナーでこのフォーム パターンを使用します。

フォーム: HcmPosition (WorkerAssignmentTabPage)

![ツールバーおよびフィールド フォーム。](./media/howtoselectaformpattern-29.jpg)

[分析コード エントリ コントロール](../financial/dimension-entry-control-subpattern.md) 分析コード エントリ コントロールのみを持つタブページにこのフォームパターンを使用します。

フォーム: CustTable (TabFinancialDimensions)

![分析コード エントリ コントロール フォーム。](./media/howtoselectaformpattern-30.jpg)

[分析コード式ビルダー](../financial/dimension-expression-builder-subpattern.md) このフォーム パターンは、分析コード式ビルダー コントロールを含むコンテナーで使用します。





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
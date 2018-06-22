---
title: "簡易リストおよび簡易詳細のフォーム パターン"
description: "この記事では、簡易リストと詳細フォームのパターンについての情報を提供します。 このパターンは、中程度の複雑さのエンティティのデータを維持するために使用されます。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 16242
ms.assetid: 4c5ae424-86fe-43f1-8f94-71dfe2edfaa7
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: c4adabb11d584da4715c88e7821503809af84580
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="simple-list-and-details-form-pattern"></a>簡易リストおよび簡易詳細のフォーム パターン

[!include [banner](../includes/banner.md)]

この記事では、簡易リストと詳細フォームのパターンについての情報を提供します。 このパターンは、中程度の複雑さのエンティティのデータを維持するために使用されます。

<a name="usage"></a>用途
-----

簡易リストと詳細 (SL+D) パターンは、中程度の複雑さのエンティティのデータを管理するために使用します。 中間の複雑度であるエンティティは、6 つ以上のフィールドを持つエンティティです。 簡易リスト パターンは、フィールドが 6 つ未満の単純なエンティティに使用してください。 依然として最大 15 フィールドのエンティティが単純なエンティティと見なされている場合、いくつかの例外があります。 簡易リストと詳細パターンは、これらの条件が満たされたときに規定されます。

-   基礎となるデータには 6 つ以上のフィールドがあります。
-   子データのコレクションは 0 から 5 です。

このドキュメントでは、3 つのパターンについて説明します。

-   **簡易リストと詳細 – リスト グリッド** – これは基本的な SL + D パターンです。 これは既定で使用されるパターンです。
-   **簡易リストと詳細 – 表形式のグリッド** – これはフォームの「簡易リスト」部分の中のフィールド数が予想よりも大きい場合に使用する SL + D パターン です (この記事の後半のセクション「パターンの変更」を参照)。
-   **簡易リストと詳細 – ツリー** – これはフォームの「簡易リスト」部分が実際には、ツリーである場合に使用する SL + D パターンです。

## <a name="wireframe"></a>ワイヤーフレーム

[![ワイヤーフレーム](./media/simplelistanddetails1-1024x575.png)](./media/simplelistanddetails1.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   上部の ActionPane ストリップ コントロールが標準の ActionPane に変換されました。
-   **新規**、**削除**、および**編集**ボタンは、フレームワークによって提供されます。
-   表示モードが既定で使用されます。
-   クイック フィルター コントロールがフォームの「リスト」部分の上に追加されました。
-   可能な限り、フォームの「リスト」部分にリスト形式のグリッドを使用します。 これらの条件が満たされた場合など、表形式のグリッドは、いくつかの状況では許容できる選択肢です。
    -   同じタイプの複数のフィールド (たとえば、3 つの日付フィールド) は、リスト形式のグリッドで区別することはできません。
    -   ユーザーのタスクは、リスト内の行 (日付の有効日またはルート ステップ番号など) の日付/数字の順序を比較することです。
    -   グリッド内のフィールド数は予想よりも大きくなります (各行がリスト スタイルのグリッドで 3 行以上を占める場合)。
-   ヘッダー グループのフィールドは、垂直方向ではなく水平に配置されます。
-   情報ボックスが許可されます。
-   フォーム構造が簡略化されました (BodyGroup コンテナーが削除されました)。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- デザイン

    - ActionPane
    - NavigationList (グループ)

        - クイック フィルター
        - *CustomFilterGroup (グループ) \[オプション\]*
        - ListStyleGrid (グリッド) | ツリー | TabularGrid (グリッド)

    - VerticalSplitter (Group) *\[Tree またはTabularGrid バリアントの場合にのみ使用可能\]*
    - DetailsHeader (グループ)
    - DetailsTab (タブ)

### <a name="core-components"></a>コア コンポーネント

1.  **Form.Design** に SimpleListDetails パターンのいずれかを適用します。
2.  必要な BP チェックを解決します。
    1.  テーブルの **Name** プロパティで使用されているラベルと同じように **Design.Caption** を設定します。
    2.  **Design.Datasource** を **Grid.Datasource** と同じに設定します。
    3.  基本データ ソースを **InsertIfEmpty**=**No** に設定します。
    4.  プライマリ **ActionPane.DataSource** を **Grid.Datasource** と同じに設定します。
    5.  **Grid.Datasource** を基本データ ソースに設定します。

### <a name="commonly-used-subpatterns"></a>一般的に使用されるサブパターン

-   [フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)
-   [ツールバーおよびリスト](toolbar-list-subpattern.md)
-   [ツールバーおよびフィールド](toolbar-fields-subpattern.md)
-   [入れ子になった簡易リストおよび詳細](nested-simple-list-details-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 

**標準フォーム ガイドライン:**

-   標準フォーム ガイドラインは、Microsoft Dynamics AX の[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**簡易リスト & 詳細 ガイドライン:**

-   ページには、エンティティを正確に説明するフォーム キャプションが表示される必要があります。
    -   フォーム キャプションは、複数形にする必要があります。
-   **新規** ボタンまたは **削除** ボタンは重複してはいけません。
-   既定では、クイック フィルターは名前または説明列を使用する必要があります。
-   カスタム フィルタのガイドラインは、カスタム フィルタ グループのサブパターン ドキュメントに統合されました。
    -   SL&D フォームには、カスタム フィルター フィールドを 2 つ以下にしてください。
-   フォームの左端には、テーブル形式のグリッド、リスト スタイルのグリッド、またはツリー コントロールが必要です。
    -   リスト スタイル グリッドには、リスト スタイル グリッドの各レコードに 3 行 (行) 以下で表示する必要があります。 通常は IDと説明だけで十分です。
    -   2 つのフィールドと 5 つのフィールドの間に左側のリストを使用する必要があります。
    -   表形式のグリッドは、いくつかの固有の状況で使用できますが、通常お勧めしません。
        -   表形式のグリッドを使用している場合、編集**不可能**にすることはできません。
    -   データが存在しないとき、グリッドまたはツリー コントロールは新しいレコードを自動的に追加できません。
-   **詳細**セクションがフォームの右側に表示されます :
    -   リスト フィールド (リスト、表形式のグリッド、ツリーのいずれかから) は、ヘッダー グループの最初のフィールドにする必要があります。 グリッドやツリーに表示される順序と同じ順序で表示されるため、ユーザーはフィールドのラベルを編集して表示できます。
-   簡易リストと詳細フォームにこれらの要素を含めることは**できません**:
    -   グループ フィールドへの標準タブ

## <a name="examples"></a>例
### <a name="simple-list-and-details--list-grid"></a>簡易リストと詳細 – リスト グリッド

フォーム: **PaymTerm** 

[![簡易リストおよび簡易詳細 – リスト グリッドの例](./media/simplelistanddetails2-1024x558.png)](./media/simplelistanddetails2.png)

### <a name="simple-list-and-details--tabular-grid"></a>簡易リストと詳細 – 表形式のグリッド

フォーム: **ExchangeRate** 

[![簡易リストおよび簡易詳細 - 表形式のグリッドの例](./media/simplelistanddetails3-1024x557.png)](./media/simplelistanddetails3.png)

### <a name="simple-list-and-details--tree"></a>簡易リストと詳細 – ツリー

フォーム: **FiscalCalendars** 

[![簡易リストおよび簡易詳細 – 表形式のグリッドの例](./media/simplelistanddetails4-1024x507.png)](./media/simplelistanddetails4.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

-   **ツール バーのアクションにあるアイコンはいつ使うのでしょうか?**
    -   [一般的なフォーム ガイドライン](general-form-guidelines.md) ドキュメントでボタン画像ガイドラインを参照してください。

### <a name="open-issues"></a>未処理の問題

-   **開発者は ListStyleGrid と TabularGrid パターン間をどのように移動できますか。**
    -   現在、開発者は手動でパターン間を移動する必要があります。
-   **FastTabs のないモデリングを詳細本文内で許可しますか。**
    -   詳細本文内でクイック タブが必要ですが、クイック タブが 1 つだけ表示される場合は最終的にクイック タブ ヘッダーを非表示にする予定です。
-   **利息フォームなどの従来の状況でクイック タブ ルールの例外を許可する方法。**
    -   可能な限り、SL&Dパターンに合わせてフォームをリファクターします (**利息** フォームが完了したとき)。 それ以外の場合、カスタム コンテナーを使用します。
-   **UI のフィールドのハイパーリンクを防ぐ方法。**
    -   一部のフィールドでは、UI でハイパーリンクを防ぐため **IgnoreEDTRelation 設定**=**はい**にできます。  他のフィールドについては、最終的には、無効なハイパーリンクで使用できる **EnableFormRef** プロパティを持つことを計画しています。

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

[![AX 2012 の例](./media/simplelistanddetails5.png)](./media/simplelistanddetails5.png)


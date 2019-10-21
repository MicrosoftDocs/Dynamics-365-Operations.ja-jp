---
title: フォーム パターン セクション リストのフォーム パターン
description: このトピックでは、フォーム パート セクション リストのフォーム パターンについての情報を提供します。 これらのワークスペース固有のパターンは、ワークスペース内にフィルターされたリストを表示するために開発されました。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 29211
ms.assetid: 05e02e22-6b71-45f2-bacd-5e3f8ea898fb
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29946fd80059d79463b1be25d3d7210f20498557
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191764"
---
# <a name="form-part-section-list-form-patterns"></a>フォーム パターン セクション リストのフォーム パターン

[!include [banner](../includes/banner.md)]

このトピックでは、フォーム パート セクション リストのフォーム パターンについての情報を提供します。 これらのワークスペース固有のパターンは、ワークスペース内にフィルターされたリストを表示するために開発されました。

<a name="usage"></a>用途
-----

フォーム パターン セクション リストのフォーム パターンは、フィルター処理されたリストの表示に使用されるワークスペース固有のパターンです。 ワークスペースのタブ付きセクションには、一連の垂直タブが含まれています。 各タブはフォーム パーツ コントロールを含み、いずれかのフォーム パーツ セクション リスト パターンを含むフォームを指します。 この記事では、2 つのパターンについて説明します。

-   **フォーム パターン セクション リスト** – これは、既定のセクション パターンです。 これは、フィルターやアクションを含む省略可能なヘッダー グループと共に、単一のデータのリストに使用できます。  ワークスペースのタブ付きセクションにある大部分のコンテンツの領域が、このパターンを使用します。
-   **フォーム パターン セクション リスト - ダブル** – このバリアントでは、データの 2 番目のリストをプライマリ リストの右側に表示できます。 既定では、セカンダリ リストは表示されません。 これを表示するには、プライマリ リストの上にあるツールバーのボタンをクリックします。

## <a name="wireframe"></a>ワイヤーフレーム
### <a name="form-part-section-list"></a>フォーム パート セクション リスト

[![formPartSectionListWireframe](./media/formpartsectionlistwireframe.png)](./media/formpartsectionlistwireframe.png)

### <a name="form-part-section-list---double"></a>フォーム パート セクション リスト - ダブル

[![formPartSectionListDoubleWireframe](./media/formpartsectionlistdoublewireframe.png)](./media/formpartsectionlistdoublewireframe.png)

## <a name="pattern-changes-for-finance-and-operations"></a>Finance and Operations のパターンの変更
これらのパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。

## <a name="model"></a>モデル
### <a name="form-part-section-list-high-level-structure"></a>フォーム パート セクション リスト: 高レベルの構造

- デザイン | コンテナー

    - *ヘッダー (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。
    - グリッド
    - *GridDefaultAction (ボタン) \[オプション\]*
    - *SeeMoreButton (ボタン) \[オプション\]*

### <a name="form-part-section-list---double-high-level-structure"></a>フォーム パート セクション リスト - ダブル: 高レベルの構造

- デザイン | コンテナー

    - PrimaryGroup (グループ)

        - *ヘッダー (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。
        - グリッド
        - *GridDefaultAction (ボタン) \[オプション\]*
        - *SeeMoreButton (ボタン) \[オプション\]*

    - SecondaryGroup (グループ)

        - *ヘッダー (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。
        - グリッド
        - *GridDefaultAction (ボタン) \[オプション\]*
        - *SeeMoreButton (ボタン) \[オプション\]*

### <a name="core-components"></a>コア コンポーネント

1.  **Form.Design** に適切なフォーム パターン セクション リストのパターンを適用します。
2.  バッキング運用ワークスペース フォームで、対応する垂直タブのフォーム パーツ コントロールを設定して、このフォームを指定するメニュー項目を指定します。

### <a name="related-container-patterns"></a>関連するコンテナー パターン

-   [セクション タブ付きリスト](section-tabbed-list-subpattern.md)
-   [フィルターおよびツールバー](filters-toolbar-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   **フォームの全般的なガイドライン**
    -   標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
-   **パターン固有のガイドライン**
    -   バックアップ フォームが存在し、特にすべてのレコードが一覧表示されていない場合に、**詳細情報** ボタンは、ユーザーが完全に一覧表示できるように、一覧の下部に表示されます。
    -   リストの上には、最大 2 つの重要なフィルターが存在します。
    -   リストの上には、頻繁に使用される最大で 3 つのアクションがあります。
-   **グリッド**
    -   リストは、興味のある、比較的小規模のデータまでフィルター処理されます。
    -   リストのグリッドには、行ごとに 3 つまでの明細行があります。
    -   カード グリッドには 4 つのフィールドしか表示されません (イメージは含まれません)。
    -   表形式グリッドには、8 つを超えるフィールドが表示されます。
-   **フォーム パターン セクション リスト - ダブルのガイドライン**
    -   両方のリストにアクションやフィルターがある場合は、両方のリストには、同じ [フィルターおよびツールバー](filters-toolbar-subpattern.md) サブパターン (積み上げバリアントまたはインライン バリアント) がある必要があります。

## <a name="examples"></a>例
### <a name="form-part-section-list"></a>フォーム パート セクション リスト

フォーム: **PurchOrderProcessReceiptsWorkspace** &gt; **PurchOrdersWithDelayedReceiptsPart** (**すべてのワークスペース** &gt; **発注書入庫とフォローアップ**) 

[![formPartSectionListExample](./media/formpartsectionlistexample.png)](./media/formpartsectionlistexample.png)

### <a name="form-part-section-list---double"></a>フォーム パート セクション リスト - ダブル

フォーム: **BudgetTrackingWorkspace** &gt; **BudgetTransactionPart** (**すべてのワークスペース** &gt; **元帳予算および予測**) 

[![formPartSectionListDoubleExample](./media/formpartsectionlistdoubleexample.png)](./media/formpartsectionlistdoubleexample.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

None

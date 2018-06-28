---
title: "フィルターおよびツールバーのサブパターン"
description: "この記事では、フィルターおよびツールバーのサブパターンについて説明します。 これらのワークスペース固有のサブパターンは、リストやグラフをホストする、パノラマ セクション内のフィルターやアクションを表示するために開発されました。"
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
ms.custom: 29191
ms.assetid: 8e32ba2f-6cc1-4bfd-9c79-42a8392fa812
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 53014c3e1a81f2facab268288d4ec64c73830ce2
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="filters-and-toolbar-subpatterns"></a>フィルターおよびツールバーのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、フィルターおよびツールバーのサブパターンについて説明します。 これらのワークスペース固有のサブパターンは、リストやグラフをホストする、パノラマ セクション内のフィルターやアクションを表示するために開発されました。

<a name="usage"></a>用途
-----

フィルターおよびツール バー サブパターンは、リストやグラフをホストする、パノラマ セクション内のフィルターやアクションを表示するために開発されたワークスペース固有のサブパターンです。 これらのサブパターンのフィルタ処理の一部のフィールドは、次のフィールド タイプに限定される必要があります。 これらすべてのフィールド タイプは入力の制約を持ちクエリに適用できます。

-   Lookups を使用した StringEdits
-   日付フィールド
-   ReferenceGroup
-   Comboboxes
-   チェック ボックス
-   クイック フィルター

この記事では、2 つのサブパターンについて説明します。

-   **フィルターおよびツールバー - インライン** – このサブパターンでは、フィルタ フィールドと同じ行に定義されたアクションが表示されます。
-   **フィルターおよびツールバー (積み上げ)** – このサブパターンでは、フィルタ フィールドの下の別の行に定義されたアクションが表示されます。

## <a name="wireframe"></a>ワイヤーフレーム
### <a name="filters-and-toolbar---inline"></a>フィルターおよびツールバー - インライン

[![filterToolbarInlineWireframe](./media/filtertoolbarinlinewireframe.png)](./media/filtertoolbarinlinewireframe.png)

### <a name="filters-and-toolbar---stacked"></a>フィルターおよびツールバー - 積み上げ

[![filterToolbarStackedWireframe](./media/filtertoolbarstackedwireframe.png)](./media/filtertoolbarstackedwireframe.png)

## <a name="pattern-changes-for-microsoft-dynamics-365-for-finance-and-operations"></a>Microsoft Dynamics 365 for Finance and Operations のパターン変更
これらのパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。

## <a name="model"></a>モデル
### <a name="filters-and-toolbar---inline-high-level-structure"></a>フィルターおよびツールバー - インライン: 高度なレベル構造

- グループ (ArrangeMethod=HorizontalLeft)

    - *FilterGroup (グループ) \[オプション\]*

        - *QuickFilter (QuickFilter) \[オプション\]*
        - *フィールド ($ フィールド)\[0..N\]*

    - *ツール バー (ActionPane) \[オプション\]*

### <a name="filters-and-toolbar---stacked-high-level-structure"></a>フィルターおよびツールバー - 積み上げ: 高度なレベル構造

- グループ (ArrangeMethod=Vertical)

    - *FilterGroup (グループ) \[オプション\]*

        - *QuickFilter (QuickFilter) \[オプション\]*
        - *FilterField1 ($ フィールド) \[オプション\]*
        - *FilterField2 ($ フィールド) \[オプション\]*

    - *ツール バー (ActionPane) \[オプション\]*

### <a name="core-components"></a>コア コンポーネント

正しいフィルターおよびツール バーのサブパターンをコンテナー コントロールに適用します。

### <a name="related-container-patterns"></a>関連するコンテナー パターン

-   [フォーム パート セクション リスト](section-list-form-pattern.md)
-   [セクション グラフ](section-chart-form-pattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   **フィルターおよびツールバーのガイドライン**
    -   **積み上げ** バリアントは、狭いリストおよびグラフで使用する必要があります。
    -   **インライン** バリアントは、より広いリストおよびグラフで使用する必要があります。
-   **フィルター**
    -   2 つ以下のフィルター フィールドをフィルター グループで使用する必要があります。 2 つ以上のフィルター フィールドが必要な場合、ツールバーのアクションを使用して、より多くのフィルター フィールドがあるドロップ ダイアログを開くことができます。
    -   フィルター フィールドにはラベルを使用しないでください。 コンテキストは、フィールド値から明白でなければなりません。
    -   フィルター フィールドの幅を合わせて、セクションがセクション内のグリッドまたはグラフよりも大きくならないようにする必要があります。また、フィルターに余分なスクロールバーが発生しないようにする必要があります。
-   **操作**
    -   ワークスペースでユーザーのタスク完了を支援する使用頻度の高いコマンドのみを含めます。
    -   3 つ以下のアクションをツール バーに表示する必要があります。 ツールバーの 1 つのアクションは、最大 3 つの追加アクションのドロップダウン リストとして使用できます。

## <a name="examples"></a>例
### <a name="filters-and-toolbar---inline"></a>フィルターおよびツールバー - インライン

フォーム: **HcmWorkforceManagement** &gt; **HcmOpenPositionsPart** (**すべてのワークスペース** &gt; **要員管理**) 

[![filterToolbarInline](./media/filtertoolbarinline.png)](./media/filtertoolbarinline.png)

### <a name="filters-and-toolbar---stacked"></a>フィルターおよびツールバー - 積み上げ

フォーム: **HcmWorkforceManagement** &gt; **HcmWorkerOnLeaveListPart** (**すべてのワークスペース** &gt; **要員管理**) 

[![filterToolbarStacked](./media/filtertoolbarstacked.png)](./media/filtertoolbarstacked.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

**なぜインライン バリアントはフィルター フィールドの任意の数を許可するのに、積み上げバリアントは最大 3 つまで許可するのでしょうか (QuickFilter および 2 つのカスタム フィルター)?**

この不一致には 2 つの要因が関係します。

-   UX のガイドラインは、これらのセクションに最大 2 つのフィルターを指定しています (それらのフィルターの一つは QuickFilter となる場合があります)。 したがって、Stacked バリアントは、ガイドラインにより一層準拠しています。
-   積み上げバリアントのフィールド数は、審美的な理由から制限されています。 このバリアントのフィルター フィールドは、それらの下に表示されるリスト/チャートの全幅を占めることを意図しているため、その幅は **SizeToAvailable** です。 このバリアントを限られたリストを超えて使用すると、その使用の目的にしたがって、2 つを超えるフィルター フィールドが使用された場合には、その設定によって非常に限られたフィルター フィールドが発生する可能性があります。 インライン バリアントは、幅広いグラフ/リストの上で使用するためのものです。 したがって、元のパターン定義では、任意の数のフィールドが許可されていました。 ただし、今後 2 つのバリエーション間で許可されているフィルター フィールドの数におけるこの不一致に対応する予定です。


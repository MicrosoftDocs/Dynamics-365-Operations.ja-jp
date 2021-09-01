---
title: ワークスペースのフォーム パターン
description: このトピックでは、ワークスペース フォーム パターンについて説明します。 ワークスペースはユーザーがタスクと特定のページに移動する主な方法です。
author: jasongre
ms.date: 05/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29151
ms.assetid: 4ca77c08-1c8f-4b0c-af55-ca89a7e8982b
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45a3264a0ab67b723de3c7899cec2e407c7a4eb4a408a42e88e76a67f5bb9f27
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738494"
---
# <a name="workspace-form-pattern"></a>ワークスペースのフォーム パターン

[!include [banner](../includes/banner.md)]

このトピックでは、ワークスペース フォーム パターンについて説明します。 ワークスペースはユーザーがタスクと特定のページに移動する主な方法です。 ワークスペースは、サポートされている重要な事業活動ごとに作成する必要があります。  

## <a name="usage"></a>用途

ワークスペースは新しい概念で、ユーザーがタスクと特定のページに移動する主な方法となることを意図しています。 ワークスペースは、サポートする重要な事業「活動」ごとに作成する必要があります。 「アクティビティ」はタスクよりも細かく従来の「エリア ページ」よりさらに細分化されています。 ワークスペースは、1 ページの活動の概要を提供したり、ユーザーが現在の状態、今後の作業負荷、プロセスまたはユーザーのパフォーマンスを理解するよう助けるためのものです。 ユーザーは、その活動の最も一般的なタスクを、ワークスペースから直接開始できるようにする必要があります。 可能であれば、ユーザーは、受信した概要に基づいて直接ワークスペースで、タスクを完了する必要があります。 現在、2 つのワークスペース パターンがあります。

-   **タブ付きワークスペース**: コンテンツに水平スクロール パノラマを強制せずに、このパターンは標準タブを使用して垂直スクロール ワークスペースの開発を許可します。 これは、特に Power BI レポートをワークスペースに埋め込むために使用されています。 これらのタブ内のコンテンツを定義するのに役立つ追加のサブパターンは、将来提供される可能性が高くなります。
-   **運用ワークスペース**: これは、ワークスペースの開発のために使用されている標準パターンです。 許可されている一連のコンポーネントのため、このパターンは非推奨の「ワークスペース」パターンよりも優れたパフォーマンスがあります。 この理由および、システム内の他のワークスペースで視覚と行動の一貫性を確実にするため、このパターンを使用することをお勧めします。
-   (非推奨) **ワークスペース**: このパターンは、間違いがないように、念のため記載されています。 パターンを **使用しない** でください。 これはまもなく製品から削除されます。

元のワークスペース パターンは推奨されておらず、使用すべきでないため、このトピックの残りの部分では、稼働中ワークスペース パターンとタブ付きワークスペース パターンに焦点を当てます。

## <a name="wireframe"></a>ワイヤーフレーム

### <a name="operational-workspace"></a>運用ワークスペース

[![運用ワークスペースのワイヤーフレーム。](./media/workspace1.png)](./media/workspace1.png)

### <a name="tabbed-workspace"></a>タブ付きワークスペース

[![タブ付きワークスペースのワイヤーフレーム。](./media/tabbedWorkspaceWireframe.png)](./media/tabbedWorkspaceWireframe.png)

## <a name="pattern-changes-for-finance-and-operations"></a>Finance and Operations 用のパターンの変更
Microsoft Dynamics AX 2012 ロール センターは、アクティビティに特化した複数のワークスペースで置き換えられました。

## <a name="model"></a>モデル

### <a name="operational-workspace--high-level-structure"></a>運用ワークスペース – 高度なレベル構造

- デザイン

    - *アクション ウィンドウ (ActionPane) \[オプション\]*
    - *ワークスペース ページ フィルター グループ (グループ) \[オプション\]* – これは、[ワークスペース ページ フィルター グループ](workspace-filter-group-subpattern.md)のサブパターンを使用する必要があります。
    - パノラマ (タブ)

        - セクション概要タイル (TabPage) – これは[セクション タイル](section-tiles-subpattern.md) サブパターンを使用する必要があります。
        - セクション タグ付きリスト (TabPage): これは[セクション タブ付きリスト](section-tabbed-list-subpattern.md) サブパターンを使用する必要があります。
        - *セクション グラフ (TabPage) \[オプション\]* – これは[セクション 積み上げグラフ](section-stacked-chart-subpattern.md)サブパターンを使用する必要があります。
        - *セクション PowerBI (TabPage) \[オプション\]* – これは[セクション PowerBI](section-powerbi-subpattern.md) サブパターンを使用する必要があります。
        - セクション関連リンク (TabPage): これは[セクション関連リンク](section-related-links-subpattern.md) サブパターンを使用する必要があります。

### <a name="tabbed-workspace--high-level-structure"></a>タブ付きワークスペース – 高度なレベル構造

- デザイン

    - *アクション ウィンドウ (ActionPane) \[オプション\]*
    - *ワークスペース ページ フィルター グループ (グループ) \[オプション\]* – これは、[ワークスペース ページ フィルター グループ](workspace-filter-group-subpattern.md)のサブパターンを使用する必要があります。
    - StandardTab (タブ)

        - ContentTabPage (1..N) 

## <a name="core-components"></a>コア コンポーネント

-   **Form.Design** に適切なワークスペース パターンを適用します。
-   BP 警告に対処します。
    -   **フォーム** は少なくとも 1 つのメニュー項目で参照される必要があります。
    -   **TabPage.Caption** は空ではありません (すべてのパノラマ セクションで)。

## <a name="commonly-used-subpatterns"></a>一般的に使用されるサブパターン

- [ワークスペース ページ フィルター グループ ](workspace-filter-group-subpattern.md)
- [セクション タイル](section-tiles-subpattern.md)
- [セクション タブ付きリスト ](section-tabbed-list-subpattern.md)
- [セクション積み上げグラフ](section-stacked-chart-subpattern.md)
- [セクション PowerBI](section-powerbi-subpattern.md)
- [セクション関連リンク](section-related-links-subpattern.md)

## <a name="related-patterns"></a>関連するパターン

- [フォーム パート セクション リスト](section-list-form-pattern.md)
- [セクション グラフ](section-chart-form-pattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   標準フォーム ガイドライン
    -   標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
-   ワークスペース フォームのガイドライン
    -   ページ タイトルには名詞句を使用し、一般的な単語は避けてください。 ページ タイトルは、エリア ページのタイトルと重複することはできません。
    -   ページ タイトルは、ユーザーが考えている名詞で始まる必要があります。
    -   すべてのセクションはタイトルを持つ必要があります。
    -   セクションは、通常 2 から 4 つの標準タイルの幅の範囲です。
    -   FormPartControl を使用してコンテンツを表示するセクションは、FormPartControl で **HeightMode** を **SizeToAvailable** に設定する必要があります。
-   操作
    -   使用頻度の高いコマンドのみを含めます。
    -   アクション ウィンドウのアクションは、ワークスペース全体に関連付ける必要があります (ワークスペースの特定のセクションではありません)。
        -   **例外:** 非常に頻繁に使用されている場合、**概要** セクションには、単一の「新規」アクションをタイルとして配置することができます。
    -   ドロップダウン メニューで、同じコマンドの変動をグループ化します。
        -   **例:** 新しい販売見積、新しい販売注文、新しい返品注文
-   フィルター
    -   ワークスペース上に、0 ~ 5 つのフィルター フィールドが許されます。
        -   単一フィールドのみ、そのページのタイトルの下に追加することができます。
        -   残りのフィルターは、ワークスペースの構成ダイアログにある必要があります。

## <a name="example"></a>例

### <a name="operational-workspace"></a>運用ワークスペース

フォーム: **FMClerkWorkspace** 

[![運用ワークスペースの例。](./media/workspace3.png)](./media/workspace3.png)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

## <a name="open-issues"></a>未処理の問題

-   なし

## <a name="ax-2012-content"></a>AX 2012 コンテンツ

### <a name="ax-2012-links"></a>AX 2012 リンク

-   [MSDN ロール センター ページ参照 \[AX 2012\]](/dynamicsax-2012/developer/role-center-page-reference)
-   [MSDN ロール センター ユーザー エクスペリエンス ガイドライン \[AX 2012\]](/dynamicsax-2012/developer/role-center-user-experience-guidelines)

### <a name="ax-2012-example"></a>AX 2012 の例

[![前のバージョンのワークスペースの例。](./media/workspace5.png)](./media/workspace5.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
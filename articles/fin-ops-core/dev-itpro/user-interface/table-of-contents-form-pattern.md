---
title: 目次のフォーム パターン
description: この記事では、目次フォームのパターンに関する情報を提供します。 このパターンは、セットアップ構成に論理的に関連する 2 つ以上のフォームが必要な場合に使用します。
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
ms.custom: 14621
ms.assetid: 1785880c-d729-43b7-bd78-9ae03bac4043
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd1967add1619e6ad23891f6db69e3234d78abf6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183034"
---
# <a name="table-of-contents-form-pattern"></a>目次のフォーム パターン

[!include [banner](../includes/banner.md)]

この記事では、目次フォームのパターンに関する情報を提供します。 このパターンは、セットアップ構成に論理的に関連する 2 つ以上のフォームが必要な場合に使用します。 

<a name="usage"></a>用途
-----

目次パターンは、セットアップ構成に論理的に関連する 2 つ以上のフォームが必要な場合に使用します。 タブの垂直配置は、完了の順序を意味します。 このフォーム パターンは、タブごとに異なるルート エンティティを持つタブ ページなど、無関係なアイテムのコレクションにも使用されます。 このフォーム パターンには、ツールバーとリスト、ネストされた簡易リストと詳細、またはフィールドとフィールド グループなどのコンテナー サブパターンに続く小さなコンテンツ領域の集合が含まれています。

## <a name="wireframe"></a>ワイヤーフレーム

[![TOC(1)](./media/toc1.png)](./media/toc1.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   Content Body 子コンテナーは、応答レイアウトに動的列を使用します。
-   オプションの二次命令がタイトル グループの下に追加されました。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- デザイン

    - タブ (スタイル = VerticalTabs)

        - TabPage *\[1..N 回繰り返し\]*

            - タイトル (グループ)

                - MainInstruction (StaticText)
                - *SecondaryInstruction (StaticText) \[オプション\]*

            - 本文 (グループ) | FastTabContent (タブ)

### <a name="core-components"></a>コア コンポーネント

-   **Form.Design** に TableOfContents パターンを適用します。
-   BP 警告に対処します。
    -   **Design.Caption** は空ではありません。
    -   このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。
    -   **TabPage.Caption** は空ではありません。
    -   **TabPage.DataSource** は空ではありません。
    -   **StaticText.Text** は空ではありません。

### <a name="commonly-used-subpatterns"></a>一般的に使用されるサブパターン

各 BodyGroup では、コンテンツ セクションのテーブルの内容に対して、次のコンテナー パターンのいずれかを使用します。

-   [フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)
-   [ツールバーおよびリスト](toolbar-list-subpattern.md)
-   [ツールバーおよびフィールド](toolbar-fields-subpattern.md)
-   [入れ子になった簡易リストおよび詳細](nested-simple-list-details-subpattern.md)
-   [表形式フィールド](tabular-fields-subpattern.md)
-   [リスト パネル](list-panel-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 

**標準フォーム ガイドライン:**

-   標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**目次 ガイドライン:**

-   補足命令が表示されている場合は、文例の完全で簡潔な文で構成され、終端の句読点が付きます。
-   TOC タブは、情報の入力に通常使用されるのと同じ順序で表示されます。
-   別のフォームの特定のタスクのコンテキストでフォームが開かれていない限り、フォームを開いたときにリストの最初のタブを強調表示する必要があります。
-   目次コンテンツの**コンテンツ領域**は、主に 3 つのパターンのいずれかです (単純な一覧、単純なリストと詳細、または単純な詳細)。
    -   簡易リスト コンテンツは、サブパターン ガイドラインに従う必要があります。
    -   簡易リストと詳細のコンテンツは、[入れ子になった簡易リストと詳細](nested-simple-list-details-subpattern.md)サブパターン ガイドラインに従う必要があります。
    -   簡易明細コンテンツは、[ツール バーとフィールド](toolbar-fields-subpattern.md) サブパターン ガイドラインに従う必要があります。
    -   FastTabs は Dynamics AX [全般的なフォーム ガイドライン](general-form-guidelines.md) ドキュメントの FastTab ガイドラインに従う必要があります。
    -   タブ ページのツールバーに表示されるアクション。
-   TOC フォームには、次の項目は**ありません**:
    -   標準の ActionPane に対するアプリケーション アクション。 (フレームワーク アクションのみを必要とします。)
    -   情報ボックス。
    -   TOC タブ ページ上の標準タブ。

## <a name="examples"></a>例
フォーム: **CustParameters** 

[![TOC(2)](./media/toc2.png)](./media/toc2.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

-   **グローバルボタンで何をすればいいですか?**
    -   データを初期化したり、サービス間で情報を同期させるためにボタンが必要な場合がいくつかあります。 このパターンでは標準アクション ウィンドウのシステム ボタンのみを許可するので、これらのボタンは次のいずれかの場所に移動することをお勧めします:
        -   アクションが最も密接に関連しているタブ ページです。
        -   場所が存在しない場合は、パターンの最初のタブ ページのツールバーに表示されます。

### <a name="open-issues"></a>未処理の問題

-   なし

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

[![TOC(3)](./media/toc3.png)](./media/toc3.png)

[![TOC(4)](./media/toc4.png)](./media/toc4.png)

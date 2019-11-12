---
title: カスタム フィルター グループのサブパターン
description: このトピックでは、カスタム フィルター グループのサブパターンについて説明します。
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
ms.custom: 28231
ms.assetid: 1838c10d-9172-4853-aa49-17710adf8bc1
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd6d356f879d50407dc31cd2f7060d1c7df39761
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658848"
---
# <a name="custom-filter-group-subpattern"></a>カスタム フィルター グループのサブパターン

[!include [banner](../includes/banner.md)]

<a name="usage"></a>用途
-----

このサブパターンは、グリッド セクションまたはフォーム セクションにカスタム フィルターを適用する小規模 (5 つ未満) の入力コントロールのコレクションを表示するために使用されます。 カスタム フィルター グループのフィールドは次のフィールド タイプに限定される必要があり、それは入力の制約があり、クエリに適用されるというものです。

-   Lookups を使用した StringEdits
-   日付フィールド
-   ReferenceGroup
-   Comboboxes
-   チェック ボックス
-   クイック フィルター

このドキュメントでは、2 つのパターンについて説明します。 これらのパターンの唯一の違いは、クイック フィルター コントロールが必須かオプションかです。

-   **カスタム フィルター**  – このサブパターンでは、QuickFilter コントロールはオプションです。
-   **カスタムおよびクイック フィルター**  – このサブパターンでは、QuickFilter コントロールは必須です。

## <a name="wireframes"></a>ワイヤーフレーム
### <a name="custom-filterscustom-filtersmediacustomfiltergroup1pngmediacustomfiltergroup1png"></a>カスタム フィルター [カスタム フィルター](./media/customfiltergroup1.png)](./media/customfiltergroup1.png)

### <a name="custom-and-quick-filters"></a>カスタムおよびクイック フィルター

![カスタムおよびクイック フィルター](./media/customfiltergroup2.png)

## <a name="model"></a>モデル
### <a name="custom-filters-high-level-structure"></a>カスタム フィルタ – 高レベルの構造

- CustomFilter (グループ)

    - *QuickFilter (QuickFilter) \[オプション\]*
    - *フィールド グループ (グループ)\[0..N\]*

        - フィールド ($Field) \[1..N\]

    - *フィールド ($ フィールド)\[0..N\]*

### <a name="custom-and-quick-filters-high-level-structure"></a>カスタムおよびクイック フィルター – 高レベルの構造

- CustomFilter (グループ)

    - QuickFilter (QuickFilter)
    - *フィールド グループ (グループ)\[0..N\]*

        - フィールド ($Field) \[1..N\]

    - *フィールド ($ フィールド)\[0..N\]*

### <a name="core-components"></a>コア コンポーネント

-   カスタム フィルター コンテナー パターンをグループ コントロールに適用します。
-   BP 警告に対処します。
    -   CustomFilterGroup 内の入力コントロールに DataSource または DataField を割り当てられません。

### <a name="related-container-patterns"></a>関連するコンテナー パターン

None

### <a name="related-modeling"></a>関連するモデリング

すべてのカスタム フィルターに QueryBuildRange ではなく QueryFilter を使用します。 QueryBuildRange は、外側の結合フィールドでは正しく動作しません。

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   **標準フォーム ガイドライン:**
    -   [フォームの全般的なガイドライン](general-form-guidelines.md)
-   **カスタム フィルター グループのガイドライン**
    -   すべてのコントロール (QuickFilter を除く) は制約された入力コントロールです。 文字列、整数、および実数などの、自由回答式のコントロールを使用しないでください。
    -   フィールド ラベルは、容量を節約するようオフになっています。 たとえば、**未処理**、**終了済**、**転記済**、およびすべての値を持つコンボボックスに対して、ラベルは必要ありません。
        -   ユーザーがフィルターの動作を理解するための十分なコンテキストをフィルター値が提供していない場合は、ラベルを表示します。 たとえば、日付フィールドにはコンテキストがなく、ユーザーがどのタイプの日付が指定されているか (たとえば、**作成日**) を理解するためのラベルを必要とします。
        -   すべてのラベルがオフになるか、またはオンになるかです。 ラベルが付いていないフィルターおよびラベルの付いたフィルターを混在させないでください。
        -   **例外:** チェック ボックス スタイルのブール値を使用すると、他のフィールドにラベルが表示されていなくても、ラベルを残すことができます。
    -   カスタム フィルター グループに配置するコントロールは 5 つ以下にしてください。

## <a name="examples"></a>例
### <a name="custom-filters"></a>カスタム フィルター

フォーム: **LedgerJournalTable (TopFields)** 

![カスタム フィルター](./media/customfiltergroup3.png)

### <a name="custom-and-quick-filters"></a>カスタムおよびクイック フィルター

フォーム: **CustTable** **(CustomFilterGroup)** 

[![カスタムおよびクイック フィルター](./media/customfiltergroup4.png)](./media/customfiltergroup4.png)

## <a name="resources"></a>リソース
### <a name="typically-used-by-form-patterns"></a>通常、フォームのパターンによって使用される

-   簡易リスト
-   詳細マスター
-   詳細トランザクション
-   リスト ページ

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

-   **法人には、何をすればいいですか?**
    -   「法人」は、カスタム フィルター グループに属する典型的なカスタム フィルターです。
-   **カスタム フィルターはリストのツールバーの上に置く必要がありますか。**
    -   カスタム フィルターは、ツールバーのコマンドと同様にリストにより直接影響を与えるため、可能な限りグリッドの近くに属するものと考えています。 また、この位置は、異なるページ パターンにわたって要素の一貫した論理的な順序にします。

### <a name="open-issues"></a>未処理の問題

-   **カスタム フィルター グループに詳細表示/簡易表示を許可していますか。例: BudgetAnalysisInquiry\_PSN**
    -   いいえ、現在それはカスタム コンテナーになります。 十分な例を行う場合は、新しいコンテナー サブパターンを追加する可能性があります。
-   **パターンは制約付き入力値を許可する入力可能タイプを制限しますか。**
    -   このパターンは現在のところどの入力も受け入れますが、値に制約のない入力はガイドラインに反します。
-   **グループをカスタム フィルター グループとして使用できるようにしますか。**
    -   移行を容易にするとともに、カスタム フィルター グループの場所を特定できるようにしました。 ただし、これらの状況でフィールドの小さなセットのみを使用することをお勧めします (および最終的にはこれを強制する場合があります)。

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

#### <a name="ax-2012-links"></a>AX 2012 リンク

-   [MSDN AX 2012 フィルター ウィンドウにコントロールを追加する方法](https://msdn.microsoft.com/library/cc577231.aspx)
-   [MSDN AX 2012 リスト ページの概要 – セクション フィルター ウィンドウ](https://msdn.microsoft.com/library/cc616937.aspx)

#### <a name="ax-2012-example"></a>AX 2012 の例

[![例](./media/customfiltergroup5.png)](./media/customfiltergroup5.png)

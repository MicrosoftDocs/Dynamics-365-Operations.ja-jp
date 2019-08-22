---
title: 表形式フィールドのサブパターン
description: この記事では、表形式フィールドのサブパターンに関する情報を提供します。 このサブパターンは、情報を表形式で効率的に表示するために使用されます。
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
ms.custom: 14761
ms.assetid: a2c38c58-b312-44b1-bf48-c40dc8518011
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a15919250f7a492b28ef5db8d1c053b3348444f0
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851087"
---
# <a name="tabular-fields-subpattern"></a>表形式フィールドのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、表形式フィールドのサブパターンに関する情報を提供します。 このサブパターンは、情報を表形式で効率的に表示するために使用されます。 

<a name="usage"></a>用途
-----

このサブパターンは、情報を表形式で効率的に表示するために使用されます。 フィールドは、行と列を含む表に配置され、オプションで列ヘッダー、行ラベル、キャプション、およびフッターが含まれます。 表形式フィールド サブパターンは、次のコントロールに対して適用できます。

-   TabPage コントロール
-   グループ コントロール

## <a name="wireframes"></a>ワイヤーフレーム
### <a name="tabularfields1mediatabularfields1pngmediatabularfields1pngstructural-wireframe"></a>[![TabularFields(1)](./media/tabularfields1.png)](./media/tabularfields1.png)構造ワイヤーフレーム

[![TabularFields(2)](./media/tabularfields2.png)](./media/tabularfields2.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX の以前のリリースでは、このパターンをモデル化するための正式に許容された方法はありませんでした。 したがって、このパターンは、現在のパターンと一致するように変更する必要がある、一貫性のない多くの方法でモデル化されました。 このパターンをモデル化する最も一般的な方法は、列にグループを使用することでした。 ただし、グループが行に使用されるようになりました。 この変更の主な理由は HTML/CSS コンストラクトにより適合することでした。この変更は、テーブルのタブ順とセマンティクスの保持にも役立ちます。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- TabularFields (グループ\*)

    - CaptionGroup (Group)

        - *TableCaption (StaticText) \[オプション\]*

    - TableHeaderRow (グループ)

        - *Column0Label (静的テキスト) \[オプション\]* – **注記:** この静的テキストは、col0、空白の row0 で入力されます。
        - ColumnLabels (StaticText) \[1..N\] – **注記:** これらは通常の列ヘッダーです。

    - TableRows (グループ) \[1..N\]

        - *RowLabel (StaticText) \[オプション\]*
        - RowValues ($Field) \[1..N\] または SecondaryColumnLabel (StaticText) \[1..N\]

    - TableFooterGroup (グループ)

        - *Column0Label (StaticText) \[オプション\]* – **注記:** この静的テキストは、col0、空白のフッターで入力されます。
        - *RowValues ($ フィールド)\[0..N\]* – **注記:** すべてのフッター フィールドは表示モードです。

表の最上位レベルのフィールドにある 4 つのグループは必須となる構造的な要素であることに注意してください。 ただし、それらすべてのグループ例外の行 (グループ) の内容はオプションです。 また、表形式のフィールドは TabPage コントロールで使用することもできることに注意してください。 構造はここに示す構造と同じです。

### <a name="core-components"></a>コア コンポーネント

トップレベルのグループやタブ ページに表形式フィールドのパターンを適用します。 パターン エラーと問題に対処します。

## <a name="ux-guidelines"></a>UX ガイドライン
手動での検証は必要ありません。

## <a name="examples"></a>例
フォーム: **LedgerJournalTransVendPaym** **(残高)** (**買掛金勘定** &gt; **仕訳帳** &gt; **支払仕訳帳** &gt; **明細行**) 

[![TabularFields(3)](./media/tabularfields3.png)](./media/tabularfields3.png)

## <a name="resources"></a>リソース
### <a name="typically-used-by-patterns"></a>通常、パターンによって使用される

-   [簡易リストと詳細](simple-list-details-form-pattern.md)
-   [目次](table-of-contents-form-pattern.md)
-   [詳細マスター](details-master-form-pattern.md)
-   [詳細トランザクション](details-transaction-form-pattern.md)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

-   **表形式のフィールド レイアウトの作成方法を変更する理由は何ですか?**
    -   HTML でレイアウトを実現するには、HTML レイアウトの動作方法に合わせる必要があります。 HTML レイアウトは、列ごとではなく行ごとにグループ化します。

### <a name="open-issues"></a>未処理の問題

-   None

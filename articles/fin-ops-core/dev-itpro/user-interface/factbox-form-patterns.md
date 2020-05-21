---
title: 情報ボックスのフォーム パターン
description: このトピックでは、FactBox フォームのパターンについて説明します。 情報ボックスはレコードに関連情報を指定するために使用されます。
author: jasongre
manager: AnnBe
ms.date: 11/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 14721
ms.assetid: b3d527bf-6b56-42fb-a135-493a62eb1435
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afc78fde26427a30ae0266386306f59476e875b0
ms.sourcegitcommit: 17fe0218e8e3f2f4c57c73c0c438a6ebf1ef32a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/01/2020
ms.locfileid: "3329893"
---
# <a name="factbox-form-patterns"></a>情報ボックスのフォーム パターン

[!include [banner](../includes/banner.md)]

このトピックでは、FactBox フォームのパターンについて説明します。 情報ボックスはレコードに関連情報を指定するために使用されます。

<a name="usage"></a>用途
-----

一般に、情報ボックスはレコードに「関連情報」を指定するために使用されます。 これらは、合計、残高、期限切れの注文、メール アドレスなどの重要な情報を得るために、追加のフォームを開く必要がないことを保証するのに役立ちます。 情報ボックス グリッド パターンは、関連情報の子コレクション (複数行の可能性がある) がある場合に使用する必要があります。 このドキュメントでは、2 つのパターンについて説明します。

-   **フォーム パターン 情報ボックス グリッド** – この情報ボックス パターンは、関連情報の子コレクション (複数行の可能性がある) がある場合に使用されます。

<!-- -->

-   **フォーム パターン 情報ボックス カード** – この情報ボックス パターンは、表示する必要がある一連の関連するフィールドがある場合に使用されます。

## <a name="wireframe"></a>ワイヤーフレーム
### <a name="form-part-factbox-grid"></a>フォーム パート 情報ボックス グリッド

[![フォーム パート情報ボックス グリッドの図](./media/factbox1.png)](./media/factbox1.png)

### <a name="form-part-factbox-card"></a>フォーム パート 情報ボックス カード

[![フォーム パート情報ボックス カードの図](./media/factbox2.png)](./media/factbox2.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   ボタンを配置しやすくするオプション ボタンのグループが追加されました。

## <a name="model"></a>モデル
### <a name="form-part-factbox-grid--high-level-structure"></a>フォーム パート 情報ボックス グリッド – 高レベルの構造

- デザイン

    - グリッド
    - *GridDefaultAction (ボタン) \[オプション\]*
    - *ButtonGroup (ButtonGroup) \[オプション\]*

        - ボタン

###  <a name="form-part-factbox-card--high-level-structure"></a>フォーム パート 情報ボックス カード – 高レベルの構造

- デザイン

    - *フィールド グループ (グループ)\[0..N\]*

        - フィールド ($Fields、1..N)

    - *フィールド ($ フィールド)\[0..N\]*
    - *ButtonGroup (ButtonGroup) \[オプション\]*

        - ボタン

### <a name="core-components"></a>コア コンポーネント

-   **Form.Design** に情報ボックス パターンを適用します。
-   BP 警告に対処します。
    -   **Design.Caption** は空ではありません。
    -   **Grid.DataSource** が空ではありません。

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 **標準フォーム ガイドライン:**

-   標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**情報ボックス** **全般的なガイドライン:**

-   バッキング フォームが存在する場合、情報ボックスには適切なバッキング フォームに進むたまの **(その他...)** リンクが定義されている必要があります。 情報ボックスとバッキングフォームの名前は似ている必要があります。
-   タイトルは動詞または動詞句にはできません。
-   タイトルには、特定のレコードのラベルを含めることはできません。
-   情報ボックスでは、キーボードで入力することでユーザーがデータを入力できるようにするフィールドを表示すべきではありません。
-   タイトルはコンテンツを正確に記述する必要があり、FactBox 領域が規定サイズのときは切り捨てるべきではありません。

**情報ボックス グリッド ガイドライン:**

-   1 列から 4 列が表示されます。

**情報ボックス カード ガイドライン:**

-   各フィールドには、ラベルが必要です。
-   情報ボックスにコンテンツが表示されているヘッダーおよび行の ID と名前は、表示されません。
-   2 ~ 10 フィールドが表示される必要があります。
-   通貨インジケータ フィールドは、情報ボックスの最後のフィールドとして表示されます。

## <a name="examples"></a>例
### <a name="form-part-factbox-grid"></a>フォーム パート 情報ボックス グリッド

フォーム: **CustTable** &gt; **ContactsInfoPart** 

[![フォーム パート情報ボックス グリッドの例](./media/factbox3.png)](./media/factbox3.png)

### <a name="form-part-factbox-card"></a>フォーム パート 情報ボックス カード

フォーム: **CustTable** &gt; **CustStatisticsStatistics** 

[![フォーム パート情報ボックス カードの例](./media/factbox4.png)](./media/factbox4.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

-   **詳細ボタンを動作させる方法。**
    -   情報ボックスの下部にある **詳細** ボタンをクリックすると、関連するレコードの完全な一覧を含むバッキング フォームに移動します。 このボタンは、次の例のように **クリック済み** メソッドをオーバーライドする通常のボタン コントロールを使用して実装する必要があります。 グリッドのデータを提供するテーブルの **TableRef** および **ListPageRef** プロパティに必ず入力してください。

        ```xpp
        [Control("Button")]
        class More
        {
        public void clicked()
            {    
                super();  
                FormPartUtil::openShowMoreForm(element, <TableName>);     
            }
        }
        ```

### <a name="open-issues"></a>未処理の問題

-   **フィールド ラベルはコンパクト ビジュアルをサポートするために情報ボックスの左側に置くべきですか。**
    -   Factbox 内で **LabelPosition**=**左** と設定できるようにする予定です。

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

#### <a name="ax-2012-links"></a>AX 2012 リンク

-   [AX 2012 MSDN リスト ページ ガイドライン (FactBoxes を含む)](https://msdn.microsoft.com/library/gg853328.aspx)

#### <a name="ax-2012-example"></a>AX 2012 の例

**CustTable** &gt; **ContactsInfoPart** 

[![情報ボックスの例](./media/factbox5.png)](./media/factbox5.png)

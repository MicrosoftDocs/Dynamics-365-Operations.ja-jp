---
title: 水平フィールドおよびボタン グループのサブパターン
description: この記事では、個々のフィールドにアクションを定義する必要があるときに使用される、水平フィールドおよびボタン グループのサブパターンに関する情報を提供します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8379cbbf4ddf0e2beaaeae6d647cd2346bd27a70
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267764"
---
# <a name="horizontal-fields-and-buttons-group-subpattern"></a>水平フィールドおよびボタン グループのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、水平フィールドおよびボタン グループ フォームのサブパターンに関する情報を提供します。 このサブパターンは、フォーム上の個々のフィールドのアクションを定義する必要があるときに使用されます。

## <a name="usage"></a>用途

このサブパターンは、フォーム上の個々のフィールドのアクションを定義する必要があるときに使用されます。 これらのボタンはフィールドの右側に配置され、アクションをフィールドと視覚的に関連付けます。 ボタンには、アイコンのみ (テキストなし) が表示されます。 セクションまたはフォーム全体に関連付けられているアクションは、そのセクションまたはフォーム上にあるツールバーまたは ActionPane に配置する必要があります。

### <a name="typical-contents"></a>標準的な内容

-   1-2 フィールド
-   1-3 ボタン

## <a name="wireframe"></a>ワイヤーフレーム
[![水平フィールドとボタン グループ フォーム サブパターンのワイヤーフレーム。](./media/horizontalfieldsbuttons1.png)](./media/horizontalfieldsbuttons1.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   フィールドとボタンのレイアウトには、**ArrangeMethod**=**HorizontalLeft** という単一の列が使用されます。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- グループ (ArrangeMethod=HorizontalLeft)

    - フィールド
    - *フィールド (オプション)*
    - ボタン (1-3 ボタン)

### <a name="core-components"></a>コア コンポーネント

-   HorizontalFieldsButtonsGroup サブパターンをコンテナー コントロールに適用します。
-   BP 警告に対処します。
    -   ボタンは 3 つ以下にしてください。
    -   繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。

### <a name="related-patterns"></a>関連するパターン

-   [ツールバーおよびフィールド](toolbar-fields-subpattern.md)
-   水平フィールド

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   **標準フォーム ガイドライン:**
    -   標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
-   **水平フィールドおよびボタン グループのガイドライン**
    -   フィールド + ボタンの幅は、列の標準サイズを超えてはいけません。
    -   ボタンにはシンボル イメージが割り当てられている必要があります。
    -   ボタンにはツールヒントが必要です。
    -   最大 3 つのボタンが必要です。 最後のボタンはメニュー ボタンです。

## <a name="examples"></a>例
フォーム: **SalesTable (GroupHeaderAddressHeaderOverview)** 

[![SalesTable フォームの例。](./media/horizontalfieldsbuttons2.png)](./media/horizontalfieldsbuttons2.png)

## <a name="resources"></a>リソース
### <a name="typically-used-by-patterns"></a>通常、パターンによって使用される

-   [簡易リストと詳細](simple-list-details-form-pattern.md)
-   [目次](table-of-contents-form-pattern.md)
-   [詳細マスター](details-master-form-pattern.md)
-   [詳細トランザクション](details-transaction-form-pattern.md)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

-   None

### <a name="dynamics-ax-2012-content"></a>Dynamics AX 2012 コンテンツ
**SalesTable** 

[![フォームの例。](./media/horizontalfieldsbuttons3.png)](./media/horizontalfieldsbuttons3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: テキスト入力のサブパターン
description: この記事では、テキスト入力のサブパターンについて説明します。 このサブパターンは、1 つの String コントロールまたは StaticText コントロールをコンテナーの全幅まで広げる必要があるときに使用されます。これにより、ユーザーはより多くの情報を入力する領域を獲得します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 12414
ms.assetid: 60279057-6aea-428f-b75c-313ec041c0c0
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6625e628ac4c0bdd551acb8b6f7e4fd57e0c057
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555521"
---
# <a name="fill-text-subpattern"></a>テキスト入力のサブパターン

[!include [banner](../includes/banner.md)]

この記事では、テキスト入力のサブパターンについて説明します。 このサブパターンは、1 つの String コントロールまたは StaticText コントロールをコンテナーの全幅まで広げる必要があるときに使用されます。これにより、ユーザーはより多くの情報を入力する領域を獲得します。

<a name="usage"></a>用途
-----

テキスト入力は、コンテナーの幅を最大限に拡大する単一の文字列または StaticText コントロールを必要とする場合に使用されます。 このサブパターンは、通常、ユーザーが情報を入力するために更なる領域を必要とする複数行文字列コントロールに使用されます。

## <a name="wireframe"></a>ワイヤーフレーム

[![テキスト入力のサブパターンのワイヤーフレーム](./media/filltext1.png)](./media/filltext1.png)

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

[Container]

文字列 | StaticText

### <a name="core-components"></a>コア コンポーネント

-   テキスト入力のサブパターンをコンテナー コントロールに適用します。

### <a name="related-container-patterns"></a>関連するコンテナー パターン

-   [フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
None

## <a name="examples"></a>例
フォーム: **FmRental (Notes)** 

[![テキスト入力のサブパターンの例](./media/filltext2.png)](./media/filltext2.png)

## <a name="resources"></a>リソース
### <a name="typically-used-by-patterns"></a>通常、パターンによって使用される

-   [詳細マスター](details-master-form-pattern.md)
-   [詳細トランザクション](details-transaction-form-pattern.md)
-   [簡易詳細](simple-details-form-pattern.md)
-   [簡易リストと詳細](simple-list-details-form-pattern.md)
-   [目次](table-of-contents-form-pattern.md)
-   [ウィザード](wizard-form-pattern.md)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

-   パターンは、現在、コントロールの **HeightMode** プロパティを **SizeToAvailable** に設定します。 これは、パターンが **SizeToAvailable** コンテナーで使用されている場合、非常に大きい文字列コントロールを生成します。 このコントロールで **SizeToContent** 高さを使用するか、またはプロパティをまったく設定せずに、代わりに、開発者に適切なコントロールの高さを決定させるかを調査しています。





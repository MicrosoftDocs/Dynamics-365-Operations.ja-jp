---
title: 評価とレビュー モジュール
description: このトピックでは、Microsoft Dynamics 365 Commerce の製品詳細ページで使用される評価とレビューのモジュールについて説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 85fb1272103eed7d6e44635b7c20438471d96b34
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817733"
---
# <a name="ratings-and-reviews-modules"></a>評価とレビュー モジュール

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の製品詳細ページ (PDP) で使用される評価とレビューのモジュールについて説明します。

## <a name="overview"></a>概要

E コマース Web サイトの評価およびレビューは、購入を決定する前に顧客が製品について学習するのに役立ち、製品に関する他の顧客のフィードバックを収集するメカニズムでもあります。 

評価は、製品リスト ページ、カテゴリ リスト ページ、検索結果ページ、およびその他のサイト ページに表示されます。 

ヒストグラムと製品レビューの評価は、製品の詳細ページ (PDP) に表示されます。 **レビューを書く**ボタンで、顧客は製品の評価およびレビューを送信できます。 これらの PDP 機能は、評価とレビュー モジュールによって制御されます。

## <a name="ratings-and-reviews-modules-on-pdps"></a>PDP 上の評価とレビュー モジュール 

3 つのモジュールは、PDP 上の評価とレビューの概要を表示します。
- レビューの書き込みモジュール
- 製品レビュー リスト モジュール
- 評価ヒストグラム モジュール
 
次の図は、PDP の評価とレビュー モジュールがどのようなものかを示しています。

![PDP 上の評価とレビュー モジュール](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> E コマース サイト上の複数の PDP 間で評価とレビュー モジュールのコンフィグレーションを共有できるように、PDP テンプレートとレイアウトを最適化する方法の詳細は、[テンプレートとレイアウトの概要](templates-layouts-overview.md) を参照してください。

次の図は、**モジュールの追加**ダイアログ ボックスがどのように Dynamics 365 Commerce の評価とレビュー モジュールで表示されるかを示しています。
![モジュールの追加ダイアログ ボックス](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>レビューの書き込みモジュール

レビューの書き込みモジュールには、ユーザーがサインインし、評価を割り当て、製品のレビューを書くことのできる**レビューを書く**ボタンが含まれています。 このモジュールで、ユーザーが以前に送信した評価またはレビューを編集することもできます。 このモジュールは通常、PDP 上の評価ヒストグラムおよび製品レビュー リスト モジュールの上に表示されます。
次の図は、顧客が**レビューを書く**を選択したときに表示される**レビューを書く**ダイアログ ボックスを示しています。 顧客は、このダイアログ ボックスを使用して評価およびレビューを送信できます。
![レビューを書くダイアログ ボックス](media/rnr-eCommerce-write-review-module.png) 次の表は、オーサリング ツールでコンフィギュレーションする必要があるレビューの書き込みモジュール プロパティを示します。
| プロパティ名 | 金額        | プロパティの説明                 |
|---------------|--------------|--------------------------------------|
| 氏名          | レビューの書き込み | レビューの書き込みモジュールの名前。 |

### <a name="ratings-histogram-module"></a>評価ヒストグラム モジュール

評価ヒストグラム モジュールは、評価ヒストグラムを表示します。 このモジュールは通常、レビューの書き込みモジュールと PDP の製品レビュー リスト モジュールの間に表示されます。
評価ヒストグラム モジュールには、コンフィギュレーションは必要ありません。 PDP テンプレートにモジュールを追加するだけです。 次の図は、評価とレビュー モジュールが Dynamics 365 Commerce PDP 上で表示されるようコンフィギュレーションされているときに、どのような PDP テンプレートが表示されるかを示しています。
![PDP 上で表示されるよう評価とレビューがコンフィギュレーションされている場合の PDP テンプレート](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>製品レビュー リスト モジュール

製品レビュー リスト モジュールは、製品レビューのリストと共に並べ替え、フィルタ、およびページネーション オプションを表示します。 このモジュールは通常、PDP の評価ヒストグラム モジュールの後に表示されます。
次の表は、オーサリング ツールでコンフィギュレーションする必要がある 製品レビュー リスト モジュール プロパティを示しています。

| プロパティ名              | 金額 | プロパティの説明 |
|----------------------------|-------| ---------------------|
| 各ページに表示されるレビュー | 10    | PDP で一度に表示されるレビューの数 ユーザーがレビュー ページを移動できるように、**次へ**と**前へ**ボタンが含まれています。 |

#### <a name="ratings-histogram--summary-view"></a>評価ヒストグラム - 概要ビュー

製品レビュー リスト モジュールには、評価ヒストグラム モジュールを追加できるスロットが含まれています。 次の図は、Dynamics 365 Commerce の製品 レビュー リスト モジュールに評価ヒストグラム モジュールを追加する方法を示しています。

![製品レビュー リスト モジュールにおける評価ヒストグラム モジュールの追加](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[コンテナー モジュール](add-container-module.md)

[カート モジュール](add-cart-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[注文確認モジュール](order-confirmation-module.md)

[ヘッダー モジュール](author-header-module.md)

[フッター モジュール](author-footer-module.md)

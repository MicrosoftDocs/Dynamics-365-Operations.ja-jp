---
title: オンライン注文用の消費税のコンフィギュレーション
description: このトピックでは、Dynamics 365 Commerce のさまざまなオンライン注文タイプに対する消費税グループの選択の概要を示します。
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 40c20bf13779f73289e43df21b763e1b864686a7
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530200"
---
# <a name="configure-sales-tax-for-online-orders"></a>オンライン注文用の消費税のコンフィギュレーション

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、さまざまなオンライン注文タイプに対する消費税グループの選択の概要を示します。 

電子商取引チャンネルでは、注文の配送や集配などのオプションをサポートする必要があります。 消費税の適用は、オンライン ユーザーによって選択されたオプションに基づいて行われます。 サイト顧客が品目をオンラインで購入して住所に出荷することを選択した場合、その消費税は、顧客の出荷住所税グループ設定に基づいて決定されます。 顧客が購買品目を店舗でピックアップすることを選択した場合、その消費税は、集配店舗の税グループ設定に基づいて決定されます。 

## <a name="orders-shipped-to-a-customer-address"></a>顧客住所への出荷注文 

一般に、顧客の住所に送付されるオンライン注文の税は、宛先によって定義されます。 各消費税グループには、ビジネスが国/地域、都道府県、郡、市区町村などの出荷先の詳細を階層形式で定義できる、小売の宛先に基づく税コンフィギュレーションがあります。 オンライン注文が行われると、Commerce 税エンジンにより、その注文の各明細行品目の配送先住所が使用され、宛先に基づく税基準が一致する消費税グループが検索されます。 たとえば、明細行品目の配送先がカリフォルニア州サンフランシスコになっているオンライン注文では、税エンジンにより、カリフォルニア州の消費税グループと消費税コードが検出され、それに応じて明細行品目ごとに税金が計算されます。  

## <a name="customer-based-tax-groups"></a>顧客ベースの税グループ

Commerce 本社には、顧客税グループがコンフィギュレーションされている場所が 2 つあります。

- **顧客のプロファイル**
- **顧客の出荷先住所**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>顧客のプロファイルに税グループがコンフィギュレーションされている場合

本社の顧客プロファイル レコードに消費税グループがコンフィギュレーションされている場合がありますが、オンライン注文では、顧客のプロファイルでコンフィギュレーションされた消費税グループは、税エンジンによって使用されません。 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>顧客の出荷先住所に税グループがコンフィギュレーションされている場合

顧客の出荷先住所レコードに税グループがコンフィギュレーションされていて、オンライン注文 (または明細行品目) が顧客の出荷先住所に出荷される場合、顧客の住所レコードにコンフィギュレーションされている税グループは、税計算のために税エンジンによって使用されます。

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>顧客の出荷先住所レコードの税グループのコンフィギュレーション

Commerce 本社の顧客の出荷先住所レコードに対する税グループをコンフィギュレーションするには、次の手順に従います。

1. **すべての顧客** に移動し、目的の顧客を選択します。 
1. **住所** クイックタブで、目的の住所を選択し、**その他のオプション \> 詳細** を選択します。 
1. **住所の管理** ページの **全般** タブで、必要に応じ て消費税額を設定します。

> [!NOTE]
> 税グループは、注文明細行の配送先住所を使用して定義され、宛先に基づく税は税グループ自体でコンフィギュレーションされます。 詳細については、[宛先に基づくオンライン ストアのための税の設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)を参照してください。

## <a name="order-pickup-in-store"></a>店舗での注文の受け取り

店舗での受け取りまたはカーブサイド ピックアップが指定されている注文明細行の場合は、選択したピックアップ店舗の税グループが適用されます。 特定の店舗の税グループをコンフィギュレーションする方法の詳細については、[店舗のその他の税オプションの設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores)を参照してください。

> [!NOTE]
> 店舗で注文明細行がピックアップされると、顧客の住所の税設定 (設定されている場合) が税エンジンによって無視され、ピックアップ店舗の税コンフィギュレーションが適用されます。 

## <a name="additional-resources"></a>追加リソース

[消費税の概要](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[[発生元] フィールドでの消費税計算方法](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[消費税の割り当ておよび上書き](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[消費税コードの合計額と間隔計算オプション](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[非課税の計算](tax-exempt-price-inclusive.md) 


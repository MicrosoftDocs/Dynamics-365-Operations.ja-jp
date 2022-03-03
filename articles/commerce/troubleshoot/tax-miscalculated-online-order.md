---
title: オンライン注文の税金が間違って計算される
description: このトピックでは、オンライン注文の税金が間違って計算された場合、または販売明細行の税グループが正しく設定されていない場合に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
ms.date: 02/16/2022
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0e4361b436cc78eccaff29dfa2927d342e26072d
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312034"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>オンライン注文の税金が間違って計算される

[!include [banner](../../includes/banner.md)]

このトピックでは、オンライン注文の税金が間違って計算された場合、または販売明細行の税グループが正しく設定されていない場合に役立つトラブルシューティング ガイドを示します。

## <a name="description"></a>説明

eコマース注文が行われると、税金が正しく計算されていないか、販売明細行の税グループが正しく設定されていません。

## <a name="resolution"></a>解決策

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Commerce 本社の一般的な消費税グループの構成

Commerce 本社で一般的な消費税グループを構成するには、次の手順を実行します。

1. **税 \> 間接税 \> 売上税 \> 消費税グループ** の順に移動します。
1. 左のナビゲーション ウィンドウで、構成する税グループを選択します。
1. **小売の宛先に基づく税** クイックタブで、消費税グループの税金を構成します。

> [!NOTE]
> 顧客の住所により決定される消費税がかからない出荷の場合、税グループに対して構成されている明細行の配送先住所と宛先に基づく税によって、税グループが決まります。 詳細については、[宛先に基づくオンライン ストアのための税の設定](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)を参照してください。

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Commerce 本社で小売店舗の消費税を構成する

Commerce 本社で小売店舗の消費税を構成するには、次の手順を実行します。

1. **Retail と Commerce \> チャネル \> すべての店舗** の順に移動します。
1. 消費税を構成する店舗を選択します。
1. **一般** クイックタブの **消費税** セクションで、店舗の消費税情報を構成します。

> [!NOTE]
> 店舗からの製品集荷の場合、税グループは、集荷用に選択された店舗から取得されます。 詳細については、[店舗のほかの税オプションの設定](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores) を参照してください。

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Commerce 本社で顧客の住所の消費税を構成する

Commerce 本社で顧客の住所の消費税を構成するには、次の手順を実行します。

1. **売掛金勘定 \> 顧客 \> すべての顧客** の順に移動します。
1. 消費税を構成する対象の顧客を選択します。
1. **住所** クイックタブで、消費税を構成する対象の住所を選択し、**詳細オプション** を選択して、**詳細** を選択します。
1. **一般** クイックタブで、**税グループ** を選択します。
1. **消費税** フィールドで、適切な値を選択します。

> [!NOTE]
> 顧客の住所で消費税がかかる出荷の場合、その明細行の配送先住所により、その明細行の税グループが決まります。 顧客が既に構成されている税グループがある既存の住所に出荷する場合は、既存の税グループが使用されます。 既定では、住所には作成時に税グループがありません。

## <a name="additional-resources"></a>追加リソース

[オンライン注文用の消費税のコンフィギュレーション](../sales-tax-config.md)

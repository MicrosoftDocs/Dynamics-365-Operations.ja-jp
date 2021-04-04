---
title: 支払は、注文が請求または出荷される前に自動的に決済されます
description: このトピックでは、販売注文が請求または出荷されていない場合でも、注文の直後に支払が Adyen ポータルで決済される場合に役立つトラブルシューティングガイドを示します。
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585411"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>支払は、注文が請求または出荷される前に自動的に決済されます

[!include [banner](../../includes/banner.md)]

このトピックでは、販売注文が請求または出荷されていない場合でも、注文の直後に支払が Adyen ポータルで決済される場合に役立つトラブルシューティングガイドを示します。

## <a name="description"></a>説明

販売注文が請求または出荷されていない場合でも、注文の直後に支払が Adyen ポータルで決済されます。

## <a name="resolution"></a>解像度

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Adyen ポータルで e コマース支払の手動取得を構成

Adyen ポータルで eコマース支払の手動取得を構成するには、次の手順に従います。

1. Adyen ポータルにサインインします。
1. 右上隅で、e コマース チャンネルのマーチャント口座を選択します。
1. ナビゲーション上部で、**アカウント** を選択し、**設定** を選択します。
1. **キャプチャの遅延** フィールドで、**手動** を選択します。

    ![Adyen ポータルの キャプチャの遅延の設定](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>追加リソース

[Adyen 支払いのキャプチャ](https://docs.adyen.com/point-of-sale/capturing-payments)

[Adyen 向け Dynamics 365 Payment Connector](../dev-itpro/adyen-connector.md)

[Dynamics 365 の Adyen 支払コネクタを設定](https://docs.adyen.com/plugins/microsoft-dynamics)

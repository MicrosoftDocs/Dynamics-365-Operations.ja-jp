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
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="4d789-103">支払は、注文が請求または出荷される前に自動的に決済されます</span><span class="sxs-lookup"><span data-stu-id="4d789-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d789-104">このトピックでは、販売注文が請求または出荷されていない場合でも、注文の直後に支払が Adyen ポータルで決済される場合に役立つトラブルシューティングガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="4d789-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="4d789-105">説明</span><span class="sxs-lookup"><span data-stu-id="4d789-105">Description</span></span>

<span data-ttu-id="4d789-106">販売注文が請求または出荷されていない場合でも、注文の直後に支払が Adyen ポータルで決済されます。</span><span class="sxs-lookup"><span data-stu-id="4d789-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="4d789-107">解像度</span><span class="sxs-lookup"><span data-stu-id="4d789-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="4d789-108">Adyen ポータルで e コマース支払の手動取得を構成</span><span class="sxs-lookup"><span data-stu-id="4d789-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="4d789-109">Adyen ポータルで eコマース支払の手動取得を構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4d789-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="4d789-110">Adyen ポータルにサインインします。</span><span class="sxs-lookup"><span data-stu-id="4d789-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="4d789-111">右上隅で、e コマース チャンネルのマーチャント口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d789-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="4d789-112">ナビゲーション上部で、**アカウント** を選択し、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d789-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="4d789-113">**キャプチャの遅延** フィールドで、**手動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d789-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Adyen ポータルの キャプチャの遅延の設定](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="4d789-115">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4d789-115">Additional resources</span></span>

[<span data-ttu-id="4d789-116">Adyen 支払いのキャプチャ</span><span class="sxs-lookup"><span data-stu-id="4d789-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="4d789-117">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="4d789-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="4d789-118">Dynamics 365 の Adyen 支払コネクタを設定</span><span class="sxs-lookup"><span data-stu-id="4d789-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)

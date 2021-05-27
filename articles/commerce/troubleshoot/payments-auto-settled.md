---
title: 支払は、注文が請求または出荷される前に自動的に決済されます
description: このトピックでは、販売注文が請求または出荷されていない場合でも、注文の直後に支払が Adyen ポータルで決済される場合に役立つトラブルシューティングガイドを示します。
author: Reza-Assadi
ms.date: 03/11/2021
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
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018263"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="0dd86-103">支払は、注文が請求または出荷される前に自動的に決済されます</span><span class="sxs-lookup"><span data-stu-id="0dd86-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0dd86-104">このトピックでは、販売注文が請求または出荷されていない場合でも、注文の直後に支払が Adyen ポータルで決済される場合に役立つトラブルシューティングガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="0dd86-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="0dd86-105">説明</span><span class="sxs-lookup"><span data-stu-id="0dd86-105">Description</span></span>

<span data-ttu-id="0dd86-106">販売注文が請求または出荷されていない場合でも、注文の直後に支払が Adyen ポータルで決済されます。</span><span class="sxs-lookup"><span data-stu-id="0dd86-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="0dd86-107">解像度</span><span class="sxs-lookup"><span data-stu-id="0dd86-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="0dd86-108">Adyen ポータルで e コマース支払の手動取得を構成</span><span class="sxs-lookup"><span data-stu-id="0dd86-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="0dd86-109">Adyen ポータルで eコマース支払の手動取得を構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0dd86-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="0dd86-110">Adyen ポータルにサインインします。</span><span class="sxs-lookup"><span data-stu-id="0dd86-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="0dd86-111">右上隅で、e コマース チャンネルのマーチャント口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="0dd86-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="0dd86-112">ナビゲーション上部で、**アカウント** を選択し、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0dd86-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="0dd86-113">**キャプチャの遅延** フィールドで、**手動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0dd86-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Adyen ポータルの キャプチャの遅延の設定](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="0dd86-115">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0dd86-115">Additional resources</span></span>

[<span data-ttu-id="0dd86-116">Adyen 支払いのキャプチャ</span><span class="sxs-lookup"><span data-stu-id="0dd86-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="0dd86-117">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="0dd86-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="0dd86-118">Dynamics 365 の Adyen 支払コネクタを設定</span><span class="sxs-lookup"><span data-stu-id="0dd86-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)

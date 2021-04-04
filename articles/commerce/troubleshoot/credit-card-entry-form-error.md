---
title: チェックアウト時に、クレジット カード エントリ ページにエラーが表示される
description: このトピックでは、支払方法セクションが読み込まれずエラーが表示される場合に役立つトラブルシューティング ガイドを示します。
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585406"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="9b892-103">チェックアウト時に、クレジット カード エントリ ページにエラーが表示される</span><span class="sxs-lookup"><span data-stu-id="9b892-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b892-104">このトピックでは、**支払方法** セクションが読み込まれずエラーが表示される場合に役立つトラブルシューティング ガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="9b892-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="9b892-105">説明</span><span class="sxs-lookup"><span data-stu-id="9b892-105">Description</span></span>

<span data-ttu-id="9b892-106">オンライン ストアのチェックアウト ページを開く際、**支払方法** セクションが読み込まれず、次のエラー メッセージが表示されます: 「問題が発生しました。</span><span class="sxs-lookup"><span data-stu-id="9b892-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="9b892-107">後でもう一度お試しください。」</span><span class="sxs-lookup"><span data-stu-id="9b892-107">Please try again later."</span></span>

![支払モジュール エラー](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="9b892-109">解像度</span><span class="sxs-lookup"><span data-stu-id="9b892-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="9b892-110">Commerce Scale Unit キャッシュの有効期限が切れるのを待つ</span><span class="sxs-lookup"><span data-stu-id="9b892-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="9b892-111">オンライン ストアのチェックアウト ページの支払サービス設定は、Commerce Scale Unit にキャッシュされ、e コマース サイトに表示されるまでに、最大 15 分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9b892-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="9b892-112">これらの支払サービス設定には、マーチャント口座 ID、クラウド API キー、および支払方法に関連するさまざまなコンフィギュレーション設定の変更が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9b892-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b892-113">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9b892-113">Additional resources</span></span>

[<span data-ttu-id="9b892-114">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="9b892-114">Set up an online channel</span></span>](../channel-setup-online.md)

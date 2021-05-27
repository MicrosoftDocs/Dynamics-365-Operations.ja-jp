---
title: 既定の支払サービスに関連する注文の同期エラー
description: このトピックでは、オンライン注文の同期時に発生する可能性があるエラーの修正に役立つトラブルシューティング ガイドを示します。
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021130"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="11e04-103">既定の支払サービスに関連する注文の同期エラー</span><span class="sxs-lookup"><span data-stu-id="11e04-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11e04-104">このトピックでは、オンライン注文の同期時に発生する可能性があるエラーの修正に役立つトラブルシューティング ガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="11e04-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="11e04-105">説明</span><span class="sxs-lookup"><span data-stu-id="11e04-105">Description</span></span>

<span data-ttu-id="11e04-106">オンライン注文を同期すると、次のエラー メッセージが表示されます。「クレジット カード トランザクションを処理するには既定の支払サービスが必要です。」</span><span class="sxs-lookup"><span data-stu-id="11e04-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![既定の支払サービス エラーの欠落](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="11e04-108">解像度</span><span class="sxs-lookup"><span data-stu-id="11e04-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="11e04-109">Commerce 本社で既定の支払サービスを確認または設定する</span><span class="sxs-lookup"><span data-stu-id="11e04-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="11e04-110">Commerce 本社で既定の支払サービスを確認または設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="11e04-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="11e04-111">**売掛金勘定 \> 支払設定 \> 支払サービス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11e04-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="11e04-112">1 つの支払サービスに対して、**新しいクレジット カードの既定のプロセッサ** オプションが **はい** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="11e04-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11e04-113">追加リソース</span><span class="sxs-lookup"><span data-stu-id="11e04-113">Additional resources</span></span>

[<span data-ttu-id="11e04-114">クレジット カードの設定、認証、および取得</span><span class="sxs-lookup"><span data-stu-id="11e04-114">Credit card setup, authorization, and capture</span></span>](../../finance/accounts-receivable/credit-card-authorizations.md)
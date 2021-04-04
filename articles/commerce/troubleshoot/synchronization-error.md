---
title: 既定の支払サービスに関連する注文の同期エラー
description: このトピックでは、オンライン注文の同期時に発生する可能性があるエラーの修正に役立つトラブルシューティング ガイドを示します。
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585405"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="cc518-103">既定の支払サービスに関連する注文の同期エラー</span><span class="sxs-lookup"><span data-stu-id="cc518-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc518-104">このトピックでは、オンライン注文の同期時に発生する可能性があるエラーの修正に役立つトラブルシューティング ガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="cc518-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="cc518-105">説明</span><span class="sxs-lookup"><span data-stu-id="cc518-105">Description</span></span>

<span data-ttu-id="cc518-106">オンライン注文を同期すると、次のエラー メッセージが表示されます。「クレジット カード トランザクションを処理するには既定の支払サービスが必要です。」</span><span class="sxs-lookup"><span data-stu-id="cc518-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![既定の支払サービス エラーの欠落](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="cc518-108">解像度</span><span class="sxs-lookup"><span data-stu-id="cc518-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="cc518-109">Commerce 本社で既定の支払サービスを確認または設定する</span><span class="sxs-lookup"><span data-stu-id="cc518-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="cc518-110">Commerce 本社で既定の支払サービスを確認または設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cc518-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="cc518-111">**売掛金勘定 \> 支払設定 \> 支払サービス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cc518-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="cc518-112">1 つの支払サービスに対して、**新しいクレジット カードの既定のプロセッサ** オプションが **はい** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="cc518-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc518-113">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cc518-113">Additional resources</span></span>

[<span data-ttu-id="cc518-114">クレジット カードの設定、認証、および取得</span><span class="sxs-lookup"><span data-stu-id="cc518-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)

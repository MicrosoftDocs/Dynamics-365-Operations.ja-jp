---
title: 指数化された販売価格
description: 定期売買手数料を作成する場合は、定期売買の販売価格の指数を設定します。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8eebb6aa044a24efc549f4be0b668e60e78c7954
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841338"
---
# <a name="indexed-sales-prices"></a><span data-ttu-id="ba317-103">指数化された販売価格</span><span class="sxs-lookup"><span data-stu-id="ba317-103">Indexed sales prices</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ba317-104">定期売買手数料を作成する場合は、定期売買の販売価格の指数を設定します。</span><span class="sxs-lookup"><span data-stu-id="ba317-104">You set up the index for a subscription sales price when you create a subscription fee.</span></span>

<span data-ttu-id="ba317-105">**定期売買手数料の作成** フォームで、**価格の取得元** フィールドを **指標化された基準価格** に設定し、基準価格に **価格変更率** フィールドの割合を乗算して、定期売買トランザクションの販売価格を取得します。</span><span class="sxs-lookup"><span data-stu-id="ba317-105">In the **Create subscription fee** form, set the **Get pricing from** field to **Indexed base price**, and then multiply the base price by the percentage in the **Percent price change** field to get the sales price of the subscription transaction.</span></span>

<span data-ttu-id="ba317-106">たとえば、基準価格が 1,000 EUR で、指数が 110 の場合、販売価格は 1,100 EUR になります。</span><span class="sxs-lookup"><span data-stu-id="ba317-106">For example, if the base price is EUR 1,000, and the index is 110, the sales price is EUR 1,100.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba317-107">参照</span><span class="sxs-lookup"><span data-stu-id="ba317-107">See also</span></span>

[<span data-ttu-id="ba317-108">定期売買手数料トランザクションの作成</span><span class="sxs-lookup"><span data-stu-id="ba317-108">Create subscription fee transactions</span></span>](create-subscription-fee-transactions.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 販売見積に関するトラブルシューティング
description: このトピックでは、販売見積と作業する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 98011dbf22ff55b7651ce63557fa4a360130b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974763"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="c0c8c-103">販売見積に関するトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="c0c8c-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="c0c8c-104">このトピックでは、販売見積と作業する際に発生する可能性がある問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c0c8c-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="c0c8c-105">サービス品目の販売見積の販売数量を変更できません。</span><span class="sxs-lookup"><span data-stu-id="c0c8c-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c0c8c-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="c0c8c-106">Issue description</span></span>

<span data-ttu-id="c0c8c-107">販売見積明細行の *サービス* タイプの品目の販売数量 (**SalesQty** フィールド) を設定しようとすると、"フィールドの数量に対する更新は許可されません" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0c8c-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c0c8c-108">問題の解決</span><span class="sxs-lookup"><span data-stu-id="c0c8c-108">Issue resolution</span></span>

<span data-ttu-id="c0c8c-109">サービス品目の製品に対して、販売数量を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="c0c8c-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="c0c8c-110">たとえば、品目をインストールするサービスを提供している場合は、現物品目がないため、数量を記録する意味はありません。</span><span class="sxs-lookup"><span data-stu-id="c0c8c-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="c0c8c-111">サービスは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="c0c8c-111">There is only a service.</span></span>


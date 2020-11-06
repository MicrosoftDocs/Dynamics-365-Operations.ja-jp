---
title: 二重書き込みでの在庫状況
description: このトピックでは、二重書き込みでの在庫状況の確認方法について説明します。
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997895"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="63b70-103">二重書き込みでの在庫状況</span><span class="sxs-lookup"><span data-stu-id="63b70-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63b70-104">在庫状況を使用すると、Microsoft Dynamics 365 Sales の **見積** 、 **注文** 、または **請求書** ページに製品を追加する前に、在庫を確認できます。</span><span class="sxs-lookup"><span data-stu-id="63b70-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations** , **Orders** , or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="63b70-105">たとえば、[見込顧客から現金](dual-write-prospect-to-cash.md) の一つの重要なタスクとして在庫の確認と履行日の決定をおこないます。</span><span class="sxs-lookup"><span data-stu-id="63b70-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="63b70-106">十分な在庫がない場合は、予想在庫の入庫および払出に基づいて出荷日を見積もることができます。</span><span class="sxs-lookup"><span data-stu-id="63b70-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="63b70-107">また、製品の納期回答可能在庫 (ATP) 情報を確認して、事前に定義されたタイム フェンスで ATP 数量を検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="63b70-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="63b70-108">手持在庫</span><span class="sxs-lookup"><span data-stu-id="63b70-108">On-hand inventory</span></span>

<span data-ttu-id="63b70-109">Dynamics 365 Sales で、 **見積** 、 **注文** 、 **請求書** の各ページのヘッダーに、新規の **手持在庫** ボタンが追加されました。</span><span class="sxs-lookup"><span data-stu-id="63b70-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="63b70-110">このボタンをクリックすると、ダイアログ ボックスが表示され、手持在庫を確認する会社と製品を指定できます。</span><span class="sxs-lookup"><span data-stu-id="63b70-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="63b70-111">このダイアログボックスには、[手持在庫](../../../../supply-chain/inventory/tasks/check-availability-stock.md) と同じ情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="63b70-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="63b70-112">このダイアログ ボックスでは、Dynamics 365 Supply Chain Management からの在庫情報が返されます。</span><span class="sxs-lookup"><span data-stu-id="63b70-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="63b70-113">この情報には、次の数量が含まれています。</span><span class="sxs-lookup"><span data-stu-id="63b70-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="63b70-114">手持在庫数量</span><span class="sxs-lookup"><span data-stu-id="63b70-114">On-hand quantity</span></span>
- <span data-ttu-id="63b70-115">予約済み手持数量</span><span class="sxs-lookup"><span data-stu-id="63b70-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="63b70-116">使用可能な手持数量</span><span class="sxs-lookup"><span data-stu-id="63b70-116">Available on-hand quantity</span></span>
- <span data-ttu-id="63b70-117">注文済数量</span><span class="sxs-lookup"><span data-stu-id="63b70-117">Ordered quantity</span></span>
- <span data-ttu-id="63b70-118">注文中数量</span><span class="sxs-lookup"><span data-stu-id="63b70-118">On-order quantity</span></span>
- <span data-ttu-id="63b70-119">引当済の注文済数量</span><span class="sxs-lookup"><span data-stu-id="63b70-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="63b70-120">利用可能な合計数量</span><span class="sxs-lookup"><span data-stu-id="63b70-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="63b70-121">ATP 情報</span><span class="sxs-lookup"><span data-stu-id="63b70-121">ATP information</span></span>

<span data-ttu-id="63b70-122">Sales では、 **ATP情報** ボタンが **見積** 、 **注文** 、 **請求書** の各ページの品目に追加されました。</span><span class="sxs-lookup"><span data-stu-id="63b70-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="63b70-123">このボタンを選択すると、ダイアログ ボックスが表示され、会社、製品、在庫サイト、在庫倉庫、注文数量を指定できます。</span><span class="sxs-lookup"><span data-stu-id="63b70-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="63b70-124">このダイアログボックスの設定は、[注文-受注](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) に記述されている設定と同じです。</span><span class="sxs-lookup"><span data-stu-id="63b70-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="63b70-125">このダイアログ ボックスでは、Supply Chain Management からの ATP 情報が返されます。</span><span class="sxs-lookup"><span data-stu-id="63b70-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="63b70-126">この情報には、次の数量が含まれています。</span><span class="sxs-lookup"><span data-stu-id="63b70-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="63b70-127">ATP 数量</span><span class="sxs-lookup"><span data-stu-id="63b70-127">ATP quantity</span></span>
- <span data-ttu-id="63b70-128">受入数量</span><span class="sxs-lookup"><span data-stu-id="63b70-128">Receipt quantity</span></span>
- <span data-ttu-id="63b70-129">払出数量</span><span class="sxs-lookup"><span data-stu-id="63b70-129">Issue quantity</span></span>
- <span data-ttu-id="63b70-130">手持在庫数量</span><span class="sxs-lookup"><span data-stu-id="63b70-130">On-hand quantity</span></span>

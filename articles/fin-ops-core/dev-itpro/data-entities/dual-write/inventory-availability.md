---
title: 二重書き込みでの在庫状況
description: このトピックでは、二重書き込みでの在庫状況の確認について説明します。
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426985"
---
# <a name="inventory-availability"></a><span data-ttu-id="f19be-103">在庫状況</span><span class="sxs-lookup"><span data-stu-id="f19be-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f19be-104">在庫状況を使用すると、Dynamics 365 のモデル駆動型アプリの **見積**、**注文**、または **請求書** の各フォームに製品を追加する前に、在庫を確認できます。</span><span class="sxs-lookup"><span data-stu-id="f19be-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="f19be-105">たとえば、在庫の確認と履行日の決定は、[見込顧客から現金](dual-write-prospect-to-cash.md) プロセスの重要なタスクです。</span><span class="sxs-lookup"><span data-stu-id="f19be-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="f19be-106">十分な在庫がない場合は、予想在庫の入庫および払出に基づいて出荷日を見積もることができます。</span><span class="sxs-lookup"><span data-stu-id="f19be-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="f19be-107">また、製品の納期回答可能在庫 (ATP) 情報を確認して、事前に定義されたタイム フェンスで ATP 数量を検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="f19be-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="f19be-108">手持在庫</span><span class="sxs-lookup"><span data-stu-id="f19be-108">On-hand Inventory</span></span> 

<span data-ttu-id="f19be-109">Dynamics 365 Sales の **見積**、**注文**、または **請求書** フォームのヘッダーに、新しいボタン **手持在庫** が追加されました。</span><span class="sxs-lookup"><span data-stu-id="f19be-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="f19be-110">このボタンをクリックすると、ダイアログ ボックスが表示され、手持在庫を確認する会社と製品を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f19be-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="f19be-111">Dynamics 365 Supply Chain Management から在庫情報を返し、[手持在庫](../../../../supply-chain/inventory/tasks/check-availability-stock.md) と同じ情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="f19be-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="f19be-112">情報には、次の数量が含まれます:</span><span class="sxs-lookup"><span data-stu-id="f19be-112">The information includes these quantities:</span></span>

- <span data-ttu-id="f19be-113">**手持数量**</span><span class="sxs-lookup"><span data-stu-id="f19be-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="f19be-114">**予約済み手持数量**</span><span class="sxs-lookup"><span data-stu-id="f19be-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="f19be-115">**使用可能な手持数量**</span><span class="sxs-lookup"><span data-stu-id="f19be-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="f19be-116">**注文済数量**</span><span class="sxs-lookup"><span data-stu-id="f19be-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="f19be-117">**注文中数量**</span><span class="sxs-lookup"><span data-stu-id="f19be-117">**On-order Quantity**</span></span>
- <span data-ttu-id="f19be-118">**引当済の注文済数量**</span><span class="sxs-lookup"><span data-stu-id="f19be-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="f19be-119">**利用可能な合計数量**</span><span class="sxs-lookup"><span data-stu-id="f19be-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="f19be-120">ATP 情報</span><span class="sxs-lookup"><span data-stu-id="f19be-120">ATP information</span></span>

<span data-ttu-id="f19be-121">Dynamics 365 Sales の **見積**、**注文**、または **請求書** フォームの明細行品目に、新しいボタン **ATP 情報** が追加されました。</span><span class="sxs-lookup"><span data-stu-id="f19be-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="f19be-122">このボタンをクリックすると、ダイアログ ボックスが表示され、会社、製品、在庫サイト、在庫倉庫、注文数量を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f19be-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="f19be-123">Supply Chain Management から **ATP 情報** を返し、[注文納期日](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) で説明されている設定を表示します。</span><span class="sxs-lookup"><span data-stu-id="f19be-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="f19be-124">この情報には、**ATP 数量**、**入庫数量**、**払出数量**、**手持数量** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f19be-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>

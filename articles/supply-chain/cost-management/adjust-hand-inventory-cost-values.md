---
title: 手持在庫原価価値の調整
description: '[手持在庫の調整] ページを使用して、在庫決算プロセスの実行後に、手持在庫数量の原価価格を調整します。'
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2417a278e58f4309873ab4d33b0d1f1686081951
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "335166"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="bb1bb-103">手持在庫原価価値の調整</span><span class="sxs-lookup"><span data-stu-id="bb1bb-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb1bb-104">[手持在庫の調整] ページを使用して、在庫決算プロセスの実行後に、手持在庫数量の原価価格を調整します。</span><span class="sxs-lookup"><span data-stu-id="bb1bb-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="bb1bb-105">**手持在庫の調整**ページを使用すると、在庫決算プロセスの実行後に、手持在庫数量の原価価格を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="bb1bb-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="bb1bb-106">**注記:** **手持在庫の調整**ページを開くには、**決算と調整**ページで、完了した在庫決算プロセスのレコードを選択し、**調整** &gt; **手持在庫**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb1bb-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="bb1bb-107">**例:** 2 月に次のトランザクションが発生しました。</span><span class="sxs-lookup"><span data-stu-id="bb1bb-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="bb1bb-108">2 月 1 日: コスト USD 10.00、数量 2 の在庫財務入庫</span><span class="sxs-lookup"><span data-stu-id="bb1bb-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="bb1bb-109">2 月 5 日: コスト USD 13.00、数量 1 の在庫財務入庫</span><span class="sxs-lookup"><span data-stu-id="bb1bb-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="bb1bb-110">2 月 19 日: 移動平均コスト USD 11.00、数量 1 の在庫財務出庫</span><span class="sxs-lookup"><span data-stu-id="bb1bb-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="bb1bb-111">この品目には先入れ先出し (FIFO) 在庫モデルが設定され、2 月 28 日に在庫原価計算が実行されました。</span><span class="sxs-lookup"><span data-stu-id="bb1bb-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="bb1bb-112">USD 11.00 の財務出庫トランザクションは 2 月 1 日の財務入庫に対して決済され、USD 1.00 の調整が行われます。</span><span class="sxs-lookup"><span data-stu-id="bb1bb-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="bb1bb-113">この場合、次の在庫入庫に未処理の在庫数量が含まれることになります。</span><span class="sxs-lookup"><span data-stu-id="bb1bb-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="bb1bb-114">2 月 1 日: コスト USD 10.00、数量 1</span><span class="sxs-lookup"><span data-stu-id="bb1bb-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="bb1bb-115">2 月 5 日: コスト USD 13.00、数量 1</span><span class="sxs-lookup"><span data-stu-id="bb1bb-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="bb1bb-116">この 2 つの品目の原価を USD 15.00 に設定するには、手持在庫調整オプションを使用して、未処理の手持在庫数量を最後の在庫原価計算期間の時点で調整します。</span><span class="sxs-lookup"><span data-stu-id="bb1bb-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="bb1bb-117">**注記:** 手持在庫調整トランザクションの転記日は、最後の在庫原価計算の実行日になります。</span><span class="sxs-lookup"><span data-stu-id="bb1bb-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="bb1bb-118">この日付は変更できません。</span><span class="sxs-lookup"><span data-stu-id="bb1bb-118">This date can't be modified.</span></span>

---
title: 一般会計の既定の説明
description: 既定の説明を使用して、一般会計への伝票の転記の説明フィールドを更新できます。
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 25dd72c86b22b50eccef22a5d2cbcfcf04280684
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021615"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="64f50-103">一般会計の既定の説明</span><span class="sxs-lookup"><span data-stu-id="64f50-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64f50-104">既定の説明を使用して、一般会計への伝票の転記の **説明** フィールドを更新できます。</span><span class="sxs-lookup"><span data-stu-id="64f50-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="64f50-105">この機能は、陸揚原価に関して強化されました。</span><span class="sxs-lookup"><span data-stu-id="64f50-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="64f50-106">元帳転記の既定の説明を設定するには、**組織管理 \> 設定 \> 既定の説明** に移動します。</span><span class="sxs-lookup"><span data-stu-id="64f50-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="64f50-107">次の表に、陸揚原価をサポートするために **既定の説明** ページの **説明** フィールドに追加された新しい値を示します。</span><span class="sxs-lookup"><span data-stu-id="64f50-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="64f50-108">説明タイプ</span><span class="sxs-lookup"><span data-stu-id="64f50-108">Description type</span></span> | <span data-ttu-id="64f50-109">摘要</span><span class="sxs-lookup"><span data-stu-id="64f50-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="64f50-110">輸入原価計算 - 原価の見越し計上</span><span class="sxs-lookup"><span data-stu-id="64f50-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="64f50-111">発注請求書を転記すると、原価の見越計上が処理され、航海コストの見積もりを行います。</span><span class="sxs-lookup"><span data-stu-id="64f50-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="64f50-112">既定の説明を指定して、航海番号を説明に追加できます。</span><span class="sxs-lookup"><span data-stu-id="64f50-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="64f50-113">出荷番号に *%4* を使用します。</span><span class="sxs-lookup"><span data-stu-id="64f50-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="64f50-114">輸入原価計算 – 輸送中の商品注文</span><span class="sxs-lookup"><span data-stu-id="64f50-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="64f50-115">輸送中処理を使用している場合は、発注請求書が転記され、商品が輸送中の商品勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="64f50-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="64f50-116">既定の説明を指定して、輸送中の注文番号を説明に追加できます。</span><span class="sxs-lookup"><span data-stu-id="64f50-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="64f50-117">輸送中の注文番号に *%4* を使用します。</span><span class="sxs-lookup"><span data-stu-id="64f50-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="64f50-118">在庫 – 原価計算済 – 調整</span><span class="sxs-lookup"><span data-stu-id="64f50-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="64f50-119">買掛金勘定 (AP) 請求書が航海コストとして処理される場合は、在庫調整を処理してその航海コストを見積もる必要があります。</span><span class="sxs-lookup"><span data-stu-id="64f50-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="64f50-120">既定の説明を指定して、航海番号を説明に追加できます。</span><span class="sxs-lookup"><span data-stu-id="64f50-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="64f50-121">出荷番号に *%4* を使用します。</span><span class="sxs-lookup"><span data-stu-id="64f50-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="64f50-122">**既定の説明** ページの使用方法の詳細については、[自動転記の既定の説明の設定](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64f50-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>

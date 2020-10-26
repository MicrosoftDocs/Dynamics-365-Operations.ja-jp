---
title: 返品による請求書更新の実行
description: この機能は、返品注文と販売注文を同じ担当者が同時に請求する、組織で採用されている業務プロセスをサポートしています。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d60e29aec1ebdec939aaafc978ee4de04b96136
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983846"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="e17a9-103">返品による請求書更新の実行</span><span class="sxs-lookup"><span data-stu-id="e17a9-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e17a9-104">返品注文は、返品された注文としてマークされた販売注文の一タイプです。</span><span class="sxs-lookup"><span data-stu-id="e17a9-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="e17a9-105">したがって 、**返品注文**フォームの代わりに返品注文の請求書を生成するには、**すべての販売注文**リスト ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="e17a9-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="e17a9-106">この機能は、返品注文と販売注文を同じ担当者が同時に請求する、組織で採用されている業務プロセスをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e17a9-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="e17a9-107">返品品目の請求書は負の量であるため、訂正票と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="e17a9-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="e17a9-108">請求書の更新をバッチ処理として設定する場合、タイプが**返品注文**の販売注文の返品明細行ステータスを、注文の梱包明細が更新済であることを示す**受入済**にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e17a9-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="e17a9-109">返品注文の請求書を転記する</span><span class="sxs-lookup"><span data-stu-id="e17a9-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="e17a9-110">**売掛金管理** \> **共通** \> **販売注文** \> **すべての販売注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="e17a9-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="e17a9-111">**返品注文**が**注文タイプ**フィールドに表示される販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="e17a9-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="e17a9-112">アクション ウィンドウの、**請求書**タブで、**生成**グループから**請求書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e17a9-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="e17a9-113">**パラメーター**タブで**転記**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e17a9-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="e17a9-114">フォームの情報を確認し、必要な変更を行います。</span><span class="sxs-lookup"><span data-stu-id="e17a9-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="e17a9-115">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e17a9-115">Click **OK**.</span></span> <span data-ttu-id="e17a9-116">訂正票が転記されます。</span><span class="sxs-lookup"><span data-stu-id="e17a9-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="e17a9-117">参照</span><span class="sxs-lookup"><span data-stu-id="e17a9-117">See also</span></span>

[<span data-ttu-id="e17a9-118">返品による梱包明細票の更新</span><span class="sxs-lookup"><span data-stu-id="e17a9-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  



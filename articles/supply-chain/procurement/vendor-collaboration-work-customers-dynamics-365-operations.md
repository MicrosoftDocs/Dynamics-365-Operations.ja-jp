---
title: "顧客対応における仕入先コラボレーション"
description: "このトピックでは、Finance and Operations で仕入先コラボレーションを使用して発注書を処理し委託販売在庫を監視する方法について説明します。"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ad7c4f14cf60b2f59124ac98d55c4b92edabb47
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-collaboration-with-customers"></a><span data-ttu-id="571da-103">顧客対応における仕入先コラボレーション</span><span class="sxs-lookup"><span data-stu-id="571da-103">Vendor collaboration with customers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="571da-104">このトピックでは、Finance and Operations で仕入先コラボレーションを使用して発注書を処理し委託販売在庫を監視する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="571da-104">This topic describes how you can use vendor collaboration in Finance and Operations to work with POs and to monitor consignment inventory.</span></span>

<span data-ttu-id="571da-105">このトピックでは、Microsoft Finance and Operations で仕入先コラボレーションを使用して顧客に対応する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="571da-105">This topic describes how you can use vendor collaboration to work with customers in Microsoft Finance and Operations.</span></span> <span data-ttu-id="571da-106">これには、発注書を監視して対応する方法、および委託販売在庫を監視する方法に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="571da-106">It includes information about how to monitor and respond to purchase orders, and how to monitor consignment inventory.</span></span> <span data-ttu-id="571da-107">請求書の作業で仕入先コラボレーションを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="571da-107">It's also possible to use vendor collaboration to work with invoices.</span></span> <span data-ttu-id="571da-108">詳細については次を参照してください。[仕入先コラボレーションの請求ワークスペース](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md)</span><span class="sxs-lookup"><span data-stu-id="571da-108">For more information, see [Vendor collaboration invoicing workspace](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).</span></span>

## <a name="working-with-purchase-orders"></a><span data-ttu-id="571da-109">発注書に関連した作業</span><span class="sxs-lookup"><span data-stu-id="571da-109">Working with purchase orders</span></span>
<span data-ttu-id="571da-110">**発注書確認**ワークスペースにより、確認のために送られてきた発注書に対応することができます。</span><span class="sxs-lookup"><span data-stu-id="571da-110">The **Purchase order confirmation** workspace enables you to respond to the PO’s that have been sent to you for review.</span></span> <span data-ttu-id="571da-111">顧客からのアクションを待っている発注書、および、確認済みではあるが未処理の発注書についての情報を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="571da-111">It also enables you to view information about POs that are awaiting action from the customer, and POs that have been confirmed, but are still open.</span></span> <span data-ttu-id="571da-112">**発注書確認**ワークスペースには、3 つのリストがあります。</span><span class="sxs-lookup"><span data-stu-id="571da-112">There are three lists in the **Purchase order confirmation** workspace:</span></span>

-   <span data-ttu-id="571da-113">**確認用の発注書** - このリストには、送られてきた発注書のうち対応待ちの発注書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="571da-113">**Purchase orders for review** -This list shows POs that have been sent to you and are awaiting a response from you.</span></span> <span data-ttu-id="571da-114">対応した後、注文書はリストに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="571da-114">After you respond, the PO disappears from the list.</span></span> <span data-ttu-id="571da-115">以前のバージョンの発注書に対応する前に、顧客から新しいバージョンの発注書が送られてきた場合、最新のバージョンのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="571da-115">If the customer sends you a new version of the PO before you’ve responded to the previous one, only the latest version is shown.</span></span>
-   <span data-ttu-id="571da-116">**顧客のアクション待ち** - このリストには、対応したものの、顧客がまだ確認していない発注書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="571da-116">**Awaiting customer action** - This list allows you to see POs that you’ve responded to, but have not yet been confirmed by the customer.</span></span> <span data-ttu-id="571da-117">発注書を受け取ったら、ステータスが [**確認済**] に変更になるまで、このリストで監視できます。</span><span class="sxs-lookup"><span data-stu-id="571da-117">If you accepted the PO, you can monitor it in this list until the status changes to **Confirmed**.</span></span> <span data-ttu-id="571da-118">発注書を否認するか、または変更した内容で承認したら、顧客が新しいバージョンを送信するまで発注書をここで監視できます。</span><span class="sxs-lookup"><span data-stu-id="571da-118">If you rejected the PO or accepted it with changes, you can monitor the PO here until the customer sends a new version.</span></span>
-   <span data-ttu-id="571da-119">**確認済発注書を開く** - アカウントの発注書のうち、ステータスが**確認済**のものがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="571da-119">**Open confirmed purchase orders** - This list contains all the POs for your account that have a status of **Confirmed**.</span></span> <span data-ttu-id="571da-120">発注書の製品またはサービスがすべて受領されると、発注書はリストに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="571da-120">When products or services are fully received against the PO, the PO disappears from the list.</span></span>

<span data-ttu-id="571da-121">次のリストには、発注書の作業で使用できる 4 つのページが表示されます。そのうち 2 ページはワークスペースのリストと同じ情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="571da-121">The following list shows the four pages that you can use to work with purchase orders, two of which contain the same information as the lists in the workspace:</span></span>

-   <span data-ttu-id="571da-122">**確認用の発注書** (上記を参照)</span><span class="sxs-lookup"><span data-stu-id="571da-122">**Purchase orders for review** (see above)</span></span>
-   <span data-ttu-id="571da-123">**発注書仕入先確認履歴** - このページには、仕入先に送信したすべての発注書とすべてのバージョンの発注書、および仕入先からのすべての応答が含まれています。</span><span class="sxs-lookup"><span data-stu-id="571da-123">**Purchase order vendor confirmation history** -This page contains all POs and all versions of POs that have been sent to the vendor, and all the responses that have been returned from the vendor.</span></span>
-   <span data-ttu-id="571da-124">**確認済発注書を開く** (上記を参照)</span><span class="sxs-lookup"><span data-stu-id="571da-124">**Open confirmed purchase orders** (see above)</span></span>
-   <span data-ttu-id="571da-125">**すべての確認済発注書** - このページには、製品やサービスが受領済みのものも含め、確認済みのすべての発注書が含まれています。</span><span class="sxs-lookup"><span data-stu-id="571da-125">**All confirmed purchase orders** - This page contains all the POs that have been confirmed, including those where products or services have been received.</span></span> <span data-ttu-id="571da-126">どの発注書に対して請求書を送ることができるかを監視するのにこのリストを使用できます。</span><span class="sxs-lookup"><span data-stu-id="571da-126">You can use this list to monitor which POs you can send invoices for.</span></span>

### <a name="responding-to-purchase-orders"></a><span data-ttu-id="571da-127">発注書への対応</span><span class="sxs-lookup"><span data-stu-id="571da-127">Responding to purchase orders</span></span>

<span data-ttu-id="571da-128">顧客が確認のために送信した発注書は **発注書の確認** ワークスペースと **確認用の発注書** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="571da-128">The purchase orders that the customer has sent you to review are visible in the **Purchase order confirmation** workspace and on the **Purchase orders for review** page.</span></span> <span data-ttu-id="571da-129">発注書を開いた後、それを承認、否認、または変更した内容で承認を選択できます。</span><span class="sxs-lookup"><span data-stu-id="571da-129">After you open a PO, you can choose to accept it, reject it, or accept it with changes.</span></span> <span data-ttu-id="571da-130">発注書のヘッダーまたは個々の明細行に添付ファイルがある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="571da-130">There could be attachments on the PO header or on individual lines.</span></span> <span data-ttu-id="571da-131">応答の際、発注書のヘッダーまたは個々の明細行に情報を添付することもできます。</span><span class="sxs-lookup"><span data-stu-id="571da-131">It's also possible for you to attach information to your response on the PO header or individual lines.</span></span> <span data-ttu-id="571da-132">たとえば、明細行の 1 つに代替品目を提案する場合があります。</span><span class="sxs-lookup"><span data-stu-id="571da-132">For example, you might suggest a substitute item for one of the lines.</span></span> <span data-ttu-id="571da-133">**プレビュー/印刷**オプションを使用して、発注書のプレビュー表示、および PDF ファイルとして印刷できます。</span><span class="sxs-lookup"><span data-stu-id="571da-133">You can preview and print the PO as a PDF file by using the **Preview/Print** option.</span></span> <span data-ttu-id="571da-134">**分析コードの表示**アクションを使用して、次の分析コード列の表示または非表示を選択できます: サイト、倉庫、色、サイズ、スタイル、構成。</span><span class="sxs-lookup"><span data-stu-id="571da-134">You can hide or show the following dimension columns using the **Display dimensions** action: Site, Warehouse, Color, Size, Style, Configuration.</span></span> <span data-ttu-id="571da-135">使用する際は **変更した内容で承認** オプションを個々の明細行を承認または否認できます。</span><span class="sxs-lookup"><span data-stu-id="571da-135">If you use the **Accept with changes** option, you can accept or reject individual lines.</span></span> <span data-ttu-id="571da-136">また、以下の変更を明細行に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="571da-136">You can also make the following changes to lines:</span></span>

-   <span data-ttu-id="571da-137">日付や数量を変更する。</span><span class="sxs-lookup"><span data-stu-id="571da-137">Change dates or quantities.</span></span> <span data-ttu-id="571da-138">すべての明細行の確認済の配送日を更新する場合は、発注書のヘッダーの**配送日の更新**オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="571da-138">If you want to update the confirmed delivery date on all lines, use the **Update delivery date** option on the PO header.</span></span>
-   <span data-ttu-id="571da-139">異なる配送日または数量の分割明細行</span><span class="sxs-lookup"><span data-stu-id="571da-139">Split lines for different delivery dates or quantities</span></span>
-   <span data-ttu-id="571da-140">品目を代用する。</span><span class="sxs-lookup"><span data-stu-id="571da-140">Substitute an item.</span></span> <span data-ttu-id="571da-141">これを行うには、**行の詳細**セクションの**外部**フィールドに品目説明と品目番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="571da-141">To do this, enter an item description and your item number in the **External** field in the **Line details** section.</span></span>

<span data-ttu-id="571da-142">価格情報や諸費用を変更することはできませんが、これらのメモを利用して変更の提案をすることができます。</span><span class="sxs-lookup"><span data-stu-id="571da-142">You can't change pricing information or charges, but you can make suggestions for changes to these using notes.</span></span> <span data-ttu-id="571da-143">顧客が新しいバージョンの発注書を送信した場合、以前送られたものに変更が加えられたバージョンの発注書であることを示すため、バージョンに接尾語が付きます。</span><span class="sxs-lookup"><span data-stu-id="571da-143">If your customer sends you a new version of a PO, this will have a version suffix to indicate that it’s a modified version of a PO that was previously communicated.</span></span> <span data-ttu-id="571da-144">**発注書仕入先確認履歴**ページでは、各オーダーの履歴を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="571da-144">The **Purchase order vendor confirmation history** page allows you to track the history of each order.</span></span>

## <a name="monitoring-consignment-inventory"></a><span data-ttu-id="571da-145">委託販売在庫の監視</span><span class="sxs-lookup"><span data-stu-id="571da-145">Monitoring consignment inventory</span></span>
<span data-ttu-id="571da-146">委託販売在庫を使用している場合、仕入先コラボレーション インターフェイスを使用して、以下のページの情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="571da-146">If you’re using consignment inventory, you can use the vendor collaboration interface to view information on the following pages:</span></span>

-   <span data-ttu-id="571da-147">**委託販売在庫を消費する発注書** - 委託販売在庫の発注書は、顧客が在庫品目の所有権を取得したときに作成されます。</span><span class="sxs-lookup"><span data-stu-id="571da-147">**Purchase orders consuming consignment inventory** - Purchase orders for consignment inventory are generated when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="571da-148">これらの委託販売在庫発注書は、[**委託販売在庫を消費する発注書**] ページでのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="571da-148">These consignment purchase orders are only displayed on the **Purchase orders consuming consignment inventory** page.</span></span> <span data-ttu-id="571da-149">**すべての確認済発注書**ページには含まれません。</span><span class="sxs-lookup"><span data-stu-id="571da-149">They are not included on the **All confirmed purchase orders** page.</span></span>
-   <span data-ttu-id="571da-150">**委託販売在庫から受領された製品** - このページには、製品の所有権が在庫を消費する会社に移されたトランザクションすべてをリスト表示します。</span><span class="sxs-lookup"><span data-stu-id="571da-150">**Products received from consignment inventory** - This page lists all the transactions where the ownership of products has been transferred to the company that’s consuming the inventory.</span></span> <span data-ttu-id="571da-151">この情報を使用して顧客に請求できます。</span><span class="sxs-lookup"><span data-stu-id="571da-151">You can use this information to invoice the customer.</span></span>
-   <span data-ttu-id="571da-152">**手持委託販売在庫** - このページには、現在顧客の倉庫にある、自社が所有する手持委託販売在庫を表示します。</span><span class="sxs-lookup"><span data-stu-id="571da-152">**On-hand consignment inventory** - This page shows the on-hand consignment inventory owned by your company that is on-hand at the customers warehouse.</span></span>


<a name="see-also"></a><span data-ttu-id="571da-153">参照</span><span class="sxs-lookup"><span data-stu-id="571da-153">See also</span></span>
--------

[<span data-ttu-id="571da-154">仕入先コラボレーション ユーザーの管理</span><span class="sxs-lookup"><span data-stu-id="571da-154">Manage vendor collaboration users</span></span>](manage-vendor-collaboration-users.md)





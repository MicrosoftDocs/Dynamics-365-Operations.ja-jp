--- 
title: "仕入先月次締め請求書の再オープンと編集 (日本)"
description: "日本では、連結プロセス中に請求書を見逃した場合、月次締め請求書を再オープンしてその請求書を追加する必要があります。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 55a71897792b10be5556b4d5ff74a33c35a6e0c1
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="reopen-and-edit-a-vendor-consolidated-invoice-japan"></a><span data-ttu-id="5f02d-103">仕入先月次締め請求書の再オープンと編集 (日本)</span><span class="sxs-lookup"><span data-stu-id="5f02d-103">Reopen and edit a vendor consolidated invoice (Japan)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5f02d-104">日本では、連結プロセス中に請求書を見逃した場合、月次締め請求書を再オープンしてその請求書を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f02d-104">In Japan, when you miss an invoice during the consolidation process, you will need to reopen the consolidated invoice to add the missed invoice.</span></span> 



<span data-ttu-id="5f02d-105">この手順では、確定済の月次締め請求書の再オープンと変更について説明します。</span><span class="sxs-lookup"><span data-stu-id="5f02d-105">This procedure walks you through reopening a confirmed consolidated invoice and modifying it.</span></span> <span data-ttu-id="5f02d-106">手順を完了するためには、月次締め請求書が確定済である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f02d-106">You must have a confirmed consolidated invoice before you can complete procedure.</span></span>



<span data-ttu-id="5f02d-107">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="5f02d-107">This procedure was created using the demo data company JPMF.</span></span>


## <a name="reopen-a-consolidated-invoice"></a><span data-ttu-id="5f02d-108">月次締め請求書の再オープン</span><span class="sxs-lookup"><span data-stu-id="5f02d-108">Reopen a consolidated invoice</span></span>
1. <span data-ttu-id="5f02d-109">[買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5f02d-109">Go to Accounts payable > Periodic tasks > Consolidated invoice.</span></span>
2. <span data-ttu-id="5f02d-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5f02d-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5f02d-111">[再オープン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f02d-111">Click Reopen.</span></span>

## <a name="remove-a-purchase-order-a-consolidated-invoice"></a><span data-ttu-id="5f02d-112">月締め請求書から発注書を削除</span><span class="sxs-lookup"><span data-stu-id="5f02d-112">Remove a purchase order a consolidated invoice</span></span>
1. <span data-ttu-id="5f02d-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f02d-113">In the list, click the link in the selected row.</span></span>
2. <span data-ttu-id="5f02d-114">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f02d-114">Click Edit.</span></span>
3. <span data-ttu-id="5f02d-115">削除する請求書をマークします。</span><span class="sxs-lookup"><span data-stu-id="5f02d-115">Mark the invoice that you want to remove.</span></span>
4. <span data-ttu-id="5f02d-116">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f02d-116">Click Remove.</span></span>

## <a name="add-purchase-orders-and-confirm-the-consolidated-invoice"></a><span data-ttu-id="5f02d-117">月締め請求書への発注書の追加と確定</span><span class="sxs-lookup"><span data-stu-id="5f02d-117">Add purchase orders and confirm the consolidated invoice</span></span>
1. <span data-ttu-id="5f02d-118">[請求書のクエリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f02d-118">Click Query invoice.</span></span>
2. <span data-ttu-id="5f02d-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f02d-119">Click OK.</span></span>
    * <span data-ttu-id="5f02d-120">[月次締め日] 前に請求されている発注書が追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5f02d-120">Confirm the purchase orders  invoiced before the Consolidation date  added</span></span>  
3. <span data-ttu-id="5f02d-121">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f02d-121">Click Confirm.</span></span>



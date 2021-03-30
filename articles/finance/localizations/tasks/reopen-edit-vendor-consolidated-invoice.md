---
title: 仕入先月次締め請求書の再オープンと編集
description: 日本では、連結プロセス中に請求書を見逃した場合、月次締め請求書を再オープンしてその請求書を追加する必要があります。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendConsInvoice_JP, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af926b8c2be352ec00119f97bb6703a85697d96f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225201"
---
# <a name="reopen-and-edit-a-vendor-consolidated-invoice"></a><span data-ttu-id="2ee58-103">仕入先月次締め請求書の再オープンと編集</span><span class="sxs-lookup"><span data-stu-id="2ee58-103">Reopen and edit a vendor consolidated invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ee58-104">日本では、連結プロセス中に請求書を見逃した場合、月次締め請求書を再オープンしてその請求書を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ee58-104">In Japan, when you miss an invoice during the consolidation process, you will need to reopen the consolidated invoice to add the missed invoice.</span></span> 



<span data-ttu-id="2ee58-105">この手順では、確定済の月次締め請求書の再オープンと変更について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ee58-105">This procedure walks you through reopening a confirmed consolidated invoice and modifying it.</span></span> <span data-ttu-id="2ee58-106">手順を完了するためには、月次締め請求書が確定済である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ee58-106">You must have a confirmed consolidated invoice before you can complete procedure.</span></span>



<span data-ttu-id="2ee58-107">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="2ee58-107">This procedure was created using the demo data company JPMF.</span></span>


## <a name="reopen-a-consolidated-invoice"></a><span data-ttu-id="2ee58-108">月次締め請求書の再オープン</span><span class="sxs-lookup"><span data-stu-id="2ee58-108">Reopen a consolidated invoice</span></span>
1. <span data-ttu-id="2ee58-109">[買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2ee58-109">Go to Accounts payable > Periodic tasks > Consolidated invoice.</span></span>
2. <span data-ttu-id="2ee58-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2ee58-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2ee58-111">[再オープン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ee58-111">Click Reopen.</span></span>

## <a name="remove-a-purchase-order-a-consolidated-invoice"></a><span data-ttu-id="2ee58-112">月締め請求書から発注書を削除</span><span class="sxs-lookup"><span data-stu-id="2ee58-112">Remove a purchase order a consolidated invoice</span></span>
1. <span data-ttu-id="2ee58-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ee58-113">In the list, click the link in the selected row.</span></span>
2. <span data-ttu-id="2ee58-114">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ee58-114">Click Edit.</span></span>
3. <span data-ttu-id="2ee58-115">削除する請求書をマークします。</span><span class="sxs-lookup"><span data-stu-id="2ee58-115">Mark the invoice that you want to remove.</span></span>
4. <span data-ttu-id="2ee58-116">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ee58-116">Click Remove.</span></span>

## <a name="add-purchase-orders-and-confirm-the-consolidated-invoice"></a><span data-ttu-id="2ee58-117">月締め請求書への発注書の追加と確定</span><span class="sxs-lookup"><span data-stu-id="2ee58-117">Add purchase orders and confirm the consolidated invoice</span></span>
1. <span data-ttu-id="2ee58-118">[請求書のクエリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ee58-118">Click Query invoice.</span></span>
2. <span data-ttu-id="2ee58-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ee58-119">Click OK.</span></span>
    * <span data-ttu-id="2ee58-120">[月次締め日] 前に請求されている発注書が追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2ee58-120">Confirm the purchase orders  invoiced before the Consolidation date  added</span></span>  
3. <span data-ttu-id="2ee58-121">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ee58-121">Click Confirm.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
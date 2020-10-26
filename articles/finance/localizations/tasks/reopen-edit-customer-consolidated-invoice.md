---
title: 顧客月次締め請求書の再オープンと編集
description: 日本では、連結プロセス中に請求書を見逃した場合、月次締め請求書を再オープンしてその請求書を追加する必要があります。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustConsInvoice_JP, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53a04af2eb7d248f7d34be76e2e81ad08b6c23f0
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985927"
---
# <a name="reopen-and-edit-a-customer-consolidated-invoice"></a><span data-ttu-id="42d40-103">顧客月次締め請求書の再オープンと編集</span><span class="sxs-lookup"><span data-stu-id="42d40-103">Reopen and edit a customer consolidated invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42d40-104">日本では、連結プロセス中に請求書を見逃した場合、月次締め請求書を再オープンしてその請求書を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d40-104">In Japan, when you miss an invoice during the consolidation process, you will need to reopen the consolidated invoice to add the missed invoice.</span></span> 



<span data-ttu-id="42d40-105">この手順では、確定済の月次締め請求書の再オープンと変更について説明します。</span><span class="sxs-lookup"><span data-stu-id="42d40-105">This procedure walks you through reopening a confirmed consolidated invoice and modifying it.</span></span> <span data-ttu-id="42d40-106">手順を完了するためには、月次締め請求書が確定済である必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d40-106">You must have a confirmed consolidated invoice before you can complete procedure.</span></span>



<span data-ttu-id="42d40-107">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="42d40-107">This procedure was created using the demo data company JPMF.</span></span>


## <a name="reopen-a-consolidated-invoice"></a><span data-ttu-id="42d40-108">月次締め請求書の再オープン</span><span class="sxs-lookup"><span data-stu-id="42d40-108">Reopen a consolidated invoice</span></span>
1. <span data-ttu-id="42d40-109">[売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="42d40-109">Go to Accounts receivable > Periodic tasks > Consolidated invoice.</span></span>
2. <span data-ttu-id="42d40-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="42d40-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="42d40-111">既に確定している請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="42d40-111">Select an invoice that is already confirmed.</span></span>  
3. <span data-ttu-id="42d40-112">[再オープン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d40-112">Click Reopen.</span></span>

## <a name="remove-a-sales-order-from-a-consolidated-invoice"></a><span data-ttu-id="42d40-113">月締め請求書から販売注文を削除</span><span class="sxs-lookup"><span data-stu-id="42d40-113">Remove a sales order from a consolidated invoice</span></span>
1. <span data-ttu-id="42d40-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d40-114">In the list, click the link in the selected row.</span></span>
2. <span data-ttu-id="42d40-115">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d40-115">Click Edit.</span></span>
3. <span data-ttu-id="42d40-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="42d40-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="42d40-117">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d40-117">Click Remove.</span></span>

## <a name="add-sales-orders-and-confirm-the-consolidated-invoice"></a><span data-ttu-id="42d40-118">月締め請求書への販売注文の追加と確定</span><span class="sxs-lookup"><span data-stu-id="42d40-118">Add sales orders and confirm the consolidated invoice</span></span>
1. <span data-ttu-id="42d40-119">[請求書のクエリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d40-119">Click Query invoice.</span></span>
2. <span data-ttu-id="42d40-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d40-120">Click OK.</span></span>
    * <span data-ttu-id="42d40-121">[月次締め日] 前に請求済の販売注文が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="42d40-121">Confirm that the sales orders that were invoiced before the Consolidation date are included.</span></span>  
3. <span data-ttu-id="42d40-122">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d40-122">Click Confirm.</span></span>


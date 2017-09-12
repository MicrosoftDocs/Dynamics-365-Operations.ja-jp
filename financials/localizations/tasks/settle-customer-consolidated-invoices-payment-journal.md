--- 
title: "支払仕訳帳を使用した顧客月次締め請求書の決済 (日本)"
description: "日本では、支払は月次締め請求書に対して行われ決済されます。"
author: ShylaThompson
manager: AnnBe
ms.date: 02/16/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 950c8d0fe5a0b89a85825099ae2c97539d0a2ceb
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="settle-customer-consolidated-invoices-by-using-a-payment-journal-japan"></a><span data-ttu-id="728cb-103">支払仕訳帳を使用した顧客月次締め請求書の決済 (日本)</span><span class="sxs-lookup"><span data-stu-id="728cb-103">Settle customer consolidated invoices by using a payment journal (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="728cb-104">日本では、支払は月次締め請求書に対して行われ決済されます。</span><span class="sxs-lookup"><span data-stu-id="728cb-104">In Japan, payments are made and settled against consolidated invoices.</span></span>



<span data-ttu-id="728cb-105">この手順では、支払仕訳帳と支払提案機能を使用した月次締め請求書の決済について説明します。</span><span class="sxs-lookup"><span data-stu-id="728cb-105">This procedure walks you through settling a consolidated invoice using a payment journal and payment proposal feature.</span></span> 



<span data-ttu-id="728cb-106">この手順を完了する前に、月次締め請求書が作成され確定済であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="728cb-106">Before you complete this procedure, be sure that you have a consolidated invoice created and confirmed.</span></span> 



<span data-ttu-id="728cb-107">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="728cb-107">This procedure was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="728cb-108">[売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="728cb-108">Go to Accounts receivable > Periodic tasks > Consolidated invoice.</span></span>
2. <span data-ttu-id="728cb-109">後で参照するために、[締め ID] フィールドの値をメモします。</span><span class="sxs-lookup"><span data-stu-id="728cb-109">Note the value in the Consolidation ID field to reference later</span></span>
    * <span data-ttu-id="728cb-110">デモ データ会社 JPMF の JPMF-000002 を使用できます。</span><span class="sxs-lookup"><span data-stu-id="728cb-110">You can use JPMF-000002 from the demo data company JPMF.</span></span>  
3. <span data-ttu-id="728cb-111">[売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="728cb-111">Go to Accounts receivable > Payments > Payment journal.</span></span>
4. <span data-ttu-id="728cb-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="728cb-112">Click New.</span></span>
5. <span data-ttu-id="728cb-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="728cb-113">In the Name field, type a value.</span></span>
6. <span data-ttu-id="728cb-114">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="728cb-114">Click Lines.</span></span>
7. <span data-ttu-id="728cb-115">[支払提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="728cb-115">Click Payment proposal.</span></span>
8. <span data-ttu-id="728cb-116">[支払提案の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="728cb-116">Click Create payment proposal.</span></span>
9. <span data-ttu-id="728cb-117">[詳細パラメーター] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="728cb-117">Expand the Advanced parameters section.</span></span>
10. <span data-ttu-id="728cb-118">[締め ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="728cb-118">In the Consolidation ID field, type a value.</span></span>
    * <span data-ttu-id="728cb-119">[月次締め請求書] ページで、事前にメモした値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="728cb-119">You can use the value noted previously on the Consolidated invoice page.</span></span>  
11. <span data-ttu-id="728cb-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="728cb-120">Click OK.</span></span>
12. <span data-ttu-id="728cb-121">[支払の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="728cb-121">Click Create payments.</span></span>
    * <span data-ttu-id="728cb-122">支払明細行が提案に基づいて生成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="728cb-122">Confirm the payment line is generated based on the proposal.</span></span>  <span data-ttu-id="728cb-123">[転記日] を入力します。</span><span class="sxs-lookup"><span data-stu-id="728cb-123">Provide a Date for posting.</span></span>  
    * <span data-ttu-id="728cb-124">1 件の月次締め請求書に関連付けられている請求書が複数ある場合は、支払仕訳帳に複数の明細行を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="728cb-124">When there are multiple invoices tied on one consolidated invoice, there may be multiple lines on the payment journal been generated.</span></span>  
13. <span data-ttu-id="728cb-125">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="728cb-125">Click Post.</span></span>
14. <span data-ttu-id="728cb-126">[売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="728cb-126">Go to Accounts receivable > Periodic tasks > Consolidated invoice.</span></span>
    * <span data-ttu-id="728cb-127">月次締め請求書のステータスが [決済済] に更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="728cb-127">Confirm that the status of the consolidated invoice has been updated to be Settled.</span></span>  



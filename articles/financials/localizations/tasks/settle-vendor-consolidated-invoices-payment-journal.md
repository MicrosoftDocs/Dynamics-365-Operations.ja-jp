--- 
title: "支払仕訳帳を使用した仕入先月次締め請求書の決済 (日本)"
description: "日本では、支払は月次締め請求書に対して行われ決済されます。"
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
ms.openlocfilehash: abbaf20ac247126b72bd4dbdc302c7605ddb680b
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="settle-vendor-consolidated-invoices-by-using-a-payment-journal-japan"></a><span data-ttu-id="285f4-103">支払仕訳帳を使用した仕入先月次締め請求書の決済 (日本)</span><span class="sxs-lookup"><span data-stu-id="285f4-103">Settle vendor consolidated invoices by using a payment journal (Japan)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="285f4-104">日本では、支払は月次締め請求書に対して行われ決済されます。</span><span class="sxs-lookup"><span data-stu-id="285f4-104">In Japan, payments are made and settled against consolidated invoices.</span></span>



<span data-ttu-id="285f4-105">この手順では、支払仕訳帳と支払提案機能を使用した月次締め請求書の決済について説明します。</span><span class="sxs-lookup"><span data-stu-id="285f4-105">This procedure walks you through settling a consolidated invoice using a payment journal and payment proposal feature.</span></span> 



<span data-ttu-id="285f4-106">この手順を完了する前に、月次締め請求書が作成され確定済であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="285f4-106">Before you complete this procedure, be sure that you have a consolidated invoice created and confirmed.</span></span> 



<span data-ttu-id="285f4-107">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="285f4-107">This procedure was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="285f4-108">[買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="285f4-108">Go to Accounts payable > Periodic tasks > Consolidated invoice.</span></span>
2. <span data-ttu-id="285f4-109">後で参照するために、[締め ID] フィールドの値をメモします。</span><span class="sxs-lookup"><span data-stu-id="285f4-109">Note the value in the Consolidation ID field to reference later</span></span>
    * <span data-ttu-id="285f4-110">デモ データ会社 JPMF の JPMF-000002 を使用できます。</span><span class="sxs-lookup"><span data-stu-id="285f4-110">You can use JPMF-000002 from the demo data company JPMF.</span></span>  
3. <span data-ttu-id="285f4-111">[買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="285f4-111">Go to Accounts payable > Payments > Payment journal.</span></span>
4. <span data-ttu-id="285f4-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="285f4-112">Click New.</span></span>
5. <span data-ttu-id="285f4-113">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="285f4-113">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="285f4-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="285f4-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="285f4-115">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="285f4-115">Click Lines.</span></span>
8. <span data-ttu-id="285f4-116">[支払提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="285f4-116">Click Payment proposal.</span></span>
9. <span data-ttu-id="285f4-117">[支払提案の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="285f4-117">Click Create payment proposal.</span></span>
10. <span data-ttu-id="285f4-118">[詳細パラメーター] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="285f4-118">Expand or collapse the Advanced parameters section.</span></span>
11. <span data-ttu-id="285f4-119">[締め ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="285f4-119">In the Consolidation ID field, type a value.</span></span>
    * <span data-ttu-id="285f4-120">[月次締め請求書] ページで、事前にメモした値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="285f4-120">You can use the value noted previously on the Consolidated invoice page.</span></span>  
12. <span data-ttu-id="285f4-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="285f4-121">Click OK.</span></span>
13. <span data-ttu-id="285f4-122">[支払の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="285f4-122">Click Create payments.</span></span>
    * <span data-ttu-id="285f4-123">支払明細行が提案に基づいて生成されていること、および転記日付を提供していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="285f4-123">Confirm that the payment line was generated based on the proposal and then provide a date for posting.</span></span>  
    * <span data-ttu-id="285f4-124">1 件の月次締め請求書に関連付けられている請求書が複数ある場合は、支払仕訳帳に複数の明細行を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="285f4-124">When there are multiple invoices tied on one consolidated invoice, multiple lines might be generated on the payment journal.</span></span>  
14. <span data-ttu-id="285f4-125">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="285f4-125">Click Post.</span></span>
15. <span data-ttu-id="285f4-126">[買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="285f4-126">Go to Accounts payable > Periodic tasks > Consolidated invoice.</span></span>
    * <span data-ttu-id="285f4-127">月次締め請求書のステータスが [決済済] に更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="285f4-127">Confirm that the status of the consolidated invoice has been updated to be Settled.</span></span>  



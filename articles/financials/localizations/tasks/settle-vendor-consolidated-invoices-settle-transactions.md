--- 
title: "決済トランザクションを使用した仕入先月次締め請求書の決済 (日本)"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 05f5c34827bd3e0bea5045297e702b89fca0b9e7
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="settle-vendor-consolidated-invoices-by-using-settle-transactions-japan"></a><span data-ttu-id="c3e9d-103">決済トランザクションを使用した仕入先月次締め請求書の決済 (日本)</span><span class="sxs-lookup"><span data-stu-id="c3e9d-103">Settle vendor consolidated invoices by using settle transactions (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3e9d-104">日本では、支払は月次締め請求書に対して行われ決済されます。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-104">In Japan, payments are made and settled against consolidated invoice.</span></span>



<span data-ttu-id="c3e9d-105">この手順では、決済トランザクションを使用した月次締め請求書の決済について説明します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-105">This procedure walks you through settling a consolidated invoice using settle transactions.</span></span>



<span data-ttu-id="c3e9d-106">この手順を実行する前に、月次締め請求書が作成され確定済であること、および支払いが転記されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-106">You need to make sure that a consolidated invoice is created and confirmed, and a payment is posted before running this procedure.</span></span> 



<span data-ttu-id="c3e9d-107">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-107">This procedure was created using the demo data company JPMF.</span></span>


## <a name="confirm-consolidation-invoice-to-be-settled"></a><span data-ttu-id="c3e9d-108">決済される月次締め請求書の確定</span><span class="sxs-lookup"><span data-stu-id="c3e9d-108">Confirm Consolidation invoice to be settled</span></span>
1. <span data-ttu-id="c3e9d-109">[買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-109">Go to Accounts payable > Periodic tasks > Consolidated invoice.</span></span>
2. <span data-ttu-id="c3e9d-110">後で参照するために、[締め ID] フィールドの値をメモします。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-110">Note the value in the Consolidation ID field to reference later</span></span>
    * <span data-ttu-id="c3e9d-111">決済する月次締め請求書のステータスが「確定済」であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-111">Confirm that the consolidated invoice to settle has a status of Confirmed.</span></span>    <span data-ttu-id="c3e9d-112">この例: 締め ID - JPMF-000004</span><span class="sxs-lookup"><span data-stu-id="c3e9d-112">In this example: Consolidation ID - JPMF-000004</span></span>  

## <a name="settle-consolidation-invoice"></a><span data-ttu-id="c3e9d-113">月次締め請求書の決済</span><span class="sxs-lookup"><span data-stu-id="c3e9d-113">Settle Consolidation invoice</span></span> 
1. <span data-ttu-id="c3e9d-114">[買掛金勘定] > [仕入先] > [すべての仕入先] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-114">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="c3e9d-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c3e9d-116">月次締め請求書を決済する仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-116">Select the vendor that you want to settle the consolidated invoice for.</span></span> <span data-ttu-id="c3e9d-117">この例では、JPMF-000002 を使用します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-117">In this example, we use JPMF-000002.</span></span>  
3. <span data-ttu-id="c3e9d-118">アクション ウィンドウで、[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-118">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="c3e9d-119">[トランザクションの決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-119">Click Settle transactions.</span></span>
5. <span data-ttu-id="c3e9d-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c3e9d-121">[締め ID] が JPMF-000004 のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-121">Select the record with Consolidation ID = JPMF-000004.</span></span>  
6. <span data-ttu-id="c3e9d-122">[マーク] のチェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-122">Select or clear the Mark check box.</span></span>
    * <span data-ttu-id="c3e9d-123">[請求書] をマークします。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-123">Mark the Invoice.</span></span>  
7. <span data-ttu-id="c3e9d-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c3e9d-125">請求金額を超過して評価されている支払トランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-125">Select the payment transaction, valued more than the Invoice amount.</span></span>  
8. <span data-ttu-id="c3e9d-126">[マーク] のチェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-126">Select or clear the Mark check box.</span></span>
    * <span data-ttu-id="c3e9d-127">支払トランザクションをマークします。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-127">Mark the payment transaction.</span></span>  
9. <span data-ttu-id="c3e9d-128">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-128">Click Post.</span></span>

## <a name="validate-consolidation-invoice-status-to-settled"></a><span data-ttu-id="c3e9d-129">月次締め請求書のステータスが [決済済] であることを検証</span><span class="sxs-lookup"><span data-stu-id="c3e9d-129">Validate Consolidation invoice status to Settled</span></span>
1. <span data-ttu-id="c3e9d-130">[買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-130">Go to Accounts payable > Periodic tasks > Consolidated invoice.</span></span>
    * <span data-ttu-id="c3e9d-131">月次締め請求書のステータスが「決済済」になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c3e9d-131">Confirm that the status of the consolidated invoice is now "Settled".</span></span>  



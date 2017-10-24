---
title: "不適合の作成および処理"
description: "この手順を使用して、既存の品質指示に基づき不適合管理を実行します。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5187c44aac881273900b2fc0ca91045a65cd838
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="03845-103">不適合の作成および処理</span><span class="sxs-lookup"><span data-stu-id="03845-103">Create and process a conformance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03845-104">この手順を使用して、既存の品質指示に基づき不適合管理を実行します。</span><span class="sxs-lookup"><span data-stu-id="03845-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="03845-105">USMF のデモの会社でこの記録を実行することができ、提案された値を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="03845-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="03845-106">通常この手順は品質担当者が実施します。</span><span class="sxs-lookup"><span data-stu-id="03845-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="03845-107">前提条件として、「商品の品質の調査」タスクの記録を実行します。</span><span class="sxs-lookup"><span data-stu-id="03845-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="03845-108">不適合の承認を処理する場合、タスクの記録を実行するユーザーには、[ユーザー] ページで「名前」の値が割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="03845-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="03845-109">ドキュメントのメモを使用するには、ユーザー オプションで [ドキュメントの処理] も有効化されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="03845-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="03845-110">品質指示の選択</span><span class="sxs-lookup"><span data-stu-id="03845-110">Select a quality order</span></span>
1. <span data-ttu-id="03845-111">[品質指示] に移動します。</span><span class="sxs-lookup"><span data-stu-id="03845-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="03845-112">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="03845-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="03845-113">「商品の品質の調査」タスク記録から作成された品質指示を選択します。</span><span class="sxs-lookup"><span data-stu-id="03845-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="03845-114">不適合の作成</span><span class="sxs-lookup"><span data-stu-id="03845-114">Create a nonconformance</span></span>
1. <span data-ttu-id="03845-115">[照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-115">Click Inquiries.</span></span>
2. <span data-ttu-id="03845-116">[不適合] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-116">Click Non conformances.</span></span>
3. <span data-ttu-id="03845-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-117">Click New.</span></span>
4. <span data-ttu-id="03845-118">[問題タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="03845-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="03845-119">検査プロセス中に検出された問題を選択します。</span><span class="sxs-lookup"><span data-stu-id="03845-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="03845-120">[問題タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="03845-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="03845-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="03845-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="03845-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="03845-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="03845-124">不適合の承認/否認</span><span class="sxs-lookup"><span data-stu-id="03845-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="03845-125">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-125">Click Functions.</span></span>
2. <span data-ttu-id="03845-126">[不適合の承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="03845-127">この例では、不適合を承認します。</span><span class="sxs-lookup"><span data-stu-id="03845-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="03845-128">承認された不適合は、不適合処理の一部としてまたはこのタスクの記録と同様に修正処理として、処理される作業を記録するために、関連する工程に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="03845-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="03845-129">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="03845-130">訂正アクションの作成</span><span class="sxs-lookup"><span data-stu-id="03845-130">Create a correction action</span></span>
1. <span data-ttu-id="03845-131">[訂正] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-131">Click Corrections.</span></span>
2. <span data-ttu-id="03845-132">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-132">Click New.</span></span>
3. <span data-ttu-id="03845-133">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="03845-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="03845-134">[個人番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="03845-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="03845-135">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="03845-136">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-136">Click Select.</span></span>
7. <span data-ttu-id="03845-137">[添付] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-137">Click Attach.</span></span>
    * <span data-ttu-id="03845-138">修正に関するメモを作成します。</span><span class="sxs-lookup"><span data-stu-id="03845-138">Create a note about the correction.</span></span> <span data-ttu-id="03845-139">この例では、アクションは、不適合のケースについて説明するために仕入先に連絡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03845-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="03845-140">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-140">Click New.</span></span>
9. <span data-ttu-id="03845-141">[メモ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-141">Click Note.</span></span>
    * <span data-ttu-id="03845-142">レポートの設定に応じて、異なるドキュメント タイプが不適合管理に関連付けられているレポートに印刷できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="03845-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="03845-143">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03845-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="03845-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03845-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="03845-145">訂正の管理</span><span class="sxs-lookup"><span data-stu-id="03845-145">Maintain a correction</span></span>
1. <span data-ttu-id="03845-146">[完了としてマーク] クリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-146">Click Mark complete.</span></span>
2. <span data-ttu-id="03845-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-147">Click OK.</span></span>
3. <span data-ttu-id="03845-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03845-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="03845-149">不適合のクローズ</span><span class="sxs-lookup"><span data-stu-id="03845-149">Close a nonconformance</span></span>
1. <span data-ttu-id="03845-150">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-150">Click Functions.</span></span>
2. <span data-ttu-id="03845-151">[不適合のクローズ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="03845-152">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03845-152">Click Yes.</span></span>
4. <span data-ttu-id="03845-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03845-153">Close the page.</span></span>
5. <span data-ttu-id="03845-154">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03845-154">Close the page.</span></span>


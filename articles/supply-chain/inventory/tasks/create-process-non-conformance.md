---
title: 不適合の作成および処理
description: このトピックでは、既存の品質指示に基づき不適合管理を実行する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef9c3a06aed1d26e7f5648427178a5638027ec04
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218684"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="c0644-103">不適合の作成および処理</span><span class="sxs-lookup"><span data-stu-id="c0644-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0644-104">このトピックでは、既存の品質指示に基づき不適合管理を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c0644-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="c0644-105">USMF のデモの会社でこの記録を実行することができ、提案された値を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c0644-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="c0644-106">通常この手順は品質担当者が実施します。</span><span class="sxs-lookup"><span data-stu-id="c0644-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="c0644-107">前提条件として、[商品の品質の調査](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="c0644-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="c0644-108">不適合の承認を処理する場合、タスクの記録を実行するユーザーには、[ユーザー] ページで 「名前」 の値が割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0644-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="c0644-109">ドキュメントのメモを使用するには、ユーザー オプションで [ドキュメントの処理] も有効化されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0644-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="c0644-110">品質指示の選択</span><span class="sxs-lookup"><span data-stu-id="c0644-110">Select a quality order</span></span>
1. <span data-ttu-id="c0644-111">ナビゲーション ウィンドウで **モジュール > 在庫管理 > 定期処理 > 品質管理 > 品質指示** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c0644-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="c0644-112">一覧で、[商品の品質の調査](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) で作成された品質指示を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="c0644-113">不適合の作成</span><span class="sxs-lookup"><span data-stu-id="c0644-113">Create a nonconformance</span></span>
1. <span data-ttu-id="c0644-114">アクション ウィンドウで、**照会** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="c0644-115">**不適合** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="c0644-116">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-116">Select **New**.</span></span>
4. <span data-ttu-id="c0644-117">**問題タイプ** フィールドのドロップダウン メニューで、検査プロセス中に検出された問題を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="c0644-118">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="c0644-119">不適合の承認/否認</span><span class="sxs-lookup"><span data-stu-id="c0644-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="c0644-120">**機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-120">Select **Functions**.</span></span>
2. <span data-ttu-id="c0644-121">**不適合の承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="c0644-122">この例では、不適合を承認します。</span><span class="sxs-lookup"><span data-stu-id="c0644-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="c0644-123">承認された不適合は、不適合処理の一部としてまたはこのトピックと同様に修正処理として、処理される作業を記録するために、関連する工程に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="c0644-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="c0644-124">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="c0644-125">訂正アクションの作成</span><span class="sxs-lookup"><span data-stu-id="c0644-125">Create a correction action</span></span>
1. <span data-ttu-id="c0644-126">**訂正** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="c0644-127">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-127">Select **New**.</span></span>
3. <span data-ttu-id="c0644-128">新しい行の **個人番号** フィールドで、ドロップダウン メニューから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="c0644-129">**選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0644-129">Click **Select**.</span></span>
5. <span data-ttu-id="c0644-130">**添付** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-130">Select **Attach**.</span></span> <span data-ttu-id="c0644-131">修正に関するメモを作成します。</span><span class="sxs-lookup"><span data-stu-id="c0644-131">Create a note about the correction.</span></span> <span data-ttu-id="c0644-132">この例では、アクションは、不適合のケースについて説明するために仕入先に連絡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0644-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="c0644-133">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-133">Select **New**.</span></span>
7. <span data-ttu-id="c0644-134">**注記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-134">Select **Note**.</span></span> <span data-ttu-id="c0644-135">レポートの設定に応じて、異なるドキュメント タイプが不適合管理に関連付けられているレポートに印刷できます。</span><span class="sxs-lookup"><span data-stu-id="c0644-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="c0644-136">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0644-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="c0644-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c0644-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="c0644-138">訂正の管理</span><span class="sxs-lookup"><span data-stu-id="c0644-138">Maintain a correction</span></span>
1. <span data-ttu-id="c0644-139">**完了としてマーク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="c0644-140">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-140">Select **OK**.</span></span>
3. <span data-ttu-id="c0644-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c0644-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="c0644-142">不適合のクローズ</span><span class="sxs-lookup"><span data-stu-id="c0644-142">Close a nonconformance</span></span>
1. <span data-ttu-id="c0644-143">**機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-143">Select **Functions**.</span></span>
2. <span data-ttu-id="c0644-144">**不適合のクローズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="c0644-145">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0644-145">Select **Yes**.</span></span>
4. <span data-ttu-id="c0644-146">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c0644-146">Close the pages.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
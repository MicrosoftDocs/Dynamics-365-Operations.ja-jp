---
title: 固定資産の再分類
description: 固定資産を再分類するには、その固定資産を新しい固定資産グループに移動するか、同じグループ内でその固定資産に新しい固定資産番号を割り当てる必要があります。
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944716"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="4a2f7-103">固定資産の再分類</span><span class="sxs-lookup"><span data-stu-id="4a2f7-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a2f7-104">固定資産を再分類するには、その固定資産を新しい固定資産グループに移動するか、同じグループ内でその固定資産に新しい固定資産番号を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="4a2f7-105">固定資産が再分類されるとき:</span><span class="sxs-lookup"><span data-stu-id="4a2f7-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="4a2f7-106">既存の固定資産のすべての帳簿は新しい固定資産用に作成されます。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="4a2f7-107">元の固定資産に対して設定されていたすべての情報が、新しい固定資産にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="4a2f7-108">元の固定資産の帳簿のステータスは、[クローズ済] になります。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="4a2f7-109">新しい固定資産の新しい帳簿の **取得日付** フィールドに再分類日を含みます。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="4a2f7-110">**減価償却日** フィールドの日付は、元の資産の情報からコピーされます。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="4a2f7-111">減価償却が既に開始されている場合には、**最新減価償却日** フィールドに再分類の日付が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="4a2f7-112">元の固定資産の既存の固定資産トランザクションはキャンセルされ、新しい固定資産に対して再生成されます。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="4a2f7-113">移動トランザクションがある資産が再分類されている場合は、システムは **アクション センター** にメッセージを表示して、再分類プロセス中に移動トランザクションの移動が完了しなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="4a2f7-114">既存の再分類トランザクションを適切な財務分析コードに移動するために、転送トランザクションを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="4a2f7-115">再分類プロセス中に、システムは次のアクションを実行して、元の資産から新しい資産への資産残高を再分類します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="4a2f7-116">再分類プロセスでは、元の固定資産帳簿から新しい固定資産帳簿にデータがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="4a2f7-117">再分類トランザクションでは、取得トランザクションに含まれる財務分析コード情報を含む、元の転記された取得からの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="4a2f7-118">同時に、再分類プロセスは、元の資産取得および資産移動トランザクションを元に戻します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="4a2f7-119">次の図と手順は、再分類プロセスの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="4a2f7-120">[![再分類プロセスを示す図](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="4a2f7-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="4a2f7-121">固定資産を再分類するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="4a2f7-122">**固定資産 > 定期処理のタスク > 再分類** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="4a2f7-123">**固定資産グループ** フィールドで、再分類するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="4a2f7-124">**固定資産番号** フィールドで、再分類する固定資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="4a2f7-125">**新しい固定資産グループ** フィールドで、固定資産の転送先のグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="4a2f7-126">新しい固定資産グループが番号順序に関連付けられた場合、**新しい固定資産番号** フィールドが、新しい固定資産グループの番号順序の番号で更新されます。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="4a2f7-127">そうでない場合は、**新しい固定資産番号** フィールドが **固定資産パラメーター** ページで設定された番号順序の番号で更新されます。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="4a2f7-128">番号順序が **固定資産パラメーター** ページで設定されていない場合は、**新しい固定番号** フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="4a2f7-129">**再分類日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="4a2f7-130">**伝票** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="4a2f7-131">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a2f7-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

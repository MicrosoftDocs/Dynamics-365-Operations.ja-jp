---
title: 固定資産の再分類
description: 固定資産を再分類するには、その固定資産を新しい固定資産グループに移動するか、同じグループ内でその固定資産に新しい固定資産番号を割り当てる必要があります。
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85132ee72a72c712f726bec9e3450dbd4e1d8f0b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224720"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="c9977-103">固定資産の再分類</span><span class="sxs-lookup"><span data-stu-id="c9977-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c9977-104">固定資産を再分類するには、その固定資産を新しい固定資産グループに移動するか、同じグループ内でその固定資産に新しい固定資産番号を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9977-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="c9977-105">固定資産が再分類されるとき:</span><span class="sxs-lookup"><span data-stu-id="c9977-105">When a fixed asset is reclassified:</span></span>

* <span data-ttu-id="c9977-106">既存の固定資産のすべての帳簿は新しい固定資産用に作成されます。</span><span class="sxs-lookup"><span data-stu-id="c9977-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="c9977-107">元の固定資産に対して設定されていたすべての情報が、新しい固定資産にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="c9977-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="c9977-108">元の固定資産の帳簿のステータスは、[クローズ済] になります。</span><span class="sxs-lookup"><span data-stu-id="c9977-108">The status of the books for the original fixed asset is Closed.</span></span> 

* <span data-ttu-id="c9977-109">新しい固定資産の新しい帳簿の **取得日付** フィールドに再分類日を含みます。</span><span class="sxs-lookup"><span data-stu-id="c9977-109">The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="c9977-110">**減価償却日** フィールドの日付は、元の資産の情報からコピーされます。</span><span class="sxs-lookup"><span data-stu-id="c9977-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="c9977-111">減価償却が既に開始されている場合には、**最新減価償却日** フィールドに再分類の日付が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9977-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

* <span data-ttu-id="c9977-112">元の固定資産の既存の固定資産トランザクションはキャンセルされ、新しい固定資産に対して再生成されます。</span><span class="sxs-lookup"><span data-stu-id="c9977-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="c9977-113">固定資産を再分類するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c9977-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="c9977-114">**固定資産 > 定期処理のタスク > 再分類** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9977-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="c9977-115">**固定資産グループ** フィールドで、再分類するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9977-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="c9977-116">**固定資産番号** フィールドで、再分類する固定資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9977-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="c9977-117">**新しい固定資産グループ** フィールドで、固定資産の転送先のグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9977-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="c9977-118">新しい固定資産グループが番号順序に関連付けられた場合、**新しい固定資産番号** フィールドが、新しい固定資産グループの番号順序の番号で更新されます。</span><span class="sxs-lookup"><span data-stu-id="c9977-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="c9977-119">そうでない場合は、**新しい固定資産番号** フィールドが **固定資産パラメーター** ページで設定された番号順序の番号で更新されます。</span><span class="sxs-lookup"><span data-stu-id="c9977-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="c9977-120">番号順序が **固定資産パラメーター** ページで設定されていない場合は、**新しい固定番号** フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9977-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="c9977-121">**再分類日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9977-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="c9977-122">**伝票** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c9977-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="c9977-123">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9977-123">Click **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
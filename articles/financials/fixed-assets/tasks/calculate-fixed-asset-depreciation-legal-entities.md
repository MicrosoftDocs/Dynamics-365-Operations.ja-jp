--- 
title: "法人間での固定資産減価償却の計算"
description: "固定資産が割り当てられている固定資産グループを変更する場合にこの手順を使用します。"
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 91f3f4a625d5d4b47bbe9d4e2d0ca0ed8da9dcd6
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="30705-103">法人間での固定資産減価償却の計算</span><span class="sxs-lookup"><span data-stu-id="30705-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30705-104">固定資産が割り当てられている固定資産グループを変更する場合にこの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="30705-104">Use this procedure to change the fixed asset group that a fixed asset is assigned to.</span></span> <span data-ttu-id="30705-105">固定資産は正しい固定資産グループに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="30705-105">Fixed assets should be assigned to the correct fixed asset group.</span></span> <span data-ttu-id="30705-106">固定資産グループは、照会およびレポートの作成、新しい固定資産の設定、元帳の統合、固定資産トランザクションの適切な勘定科目への転記に使用されます。</span><span class="sxs-lookup"><span data-stu-id="30705-106">The fixed asset group is used when you create inquiries and reports, set up new fixed assets, and integrate ledgers and post fixed asset transactions to the appropriate ledger accounts.</span></span>

<span data-ttu-id="30705-107">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="30705-107">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="30705-108">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="30705-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="30705-109">固定資産グループを変更するために、固定資産グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="30705-109">Select the fixed asset to change the fixed asset group for.</span></span>
3. <span data-ttu-id="30705-110">[固定資産グループの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="30705-110">Click Change fixed asset group.</span></span>
4. <span data-ttu-id="30705-111">[新規グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="30705-111">In the New group field, enter or select a value.</span></span>
5. <span data-ttu-id="30705-112">[新しい固定資産番] オプションを [はい] に設定して、固定資産番号を選択した固定資産に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="30705-112">Set the New fixed asset number option to Yes to assign a fixed asset number to the selected fixed asset.</span></span>
    * <span data-ttu-id="30705-113">新しい固定資産番号オプションが [はい] に設定されている場合、固定資産番号フィールドが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="30705-113">The Fixed asset number field becomes available when the New fixed asset number option is set to Yes.</span></span>   <span data-ttu-id="30705-114">固定資産に自動番号付けが設定されている場合、次に使用可能な固定資産番号がフィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="30705-114">If automatic numbering is set up for fixed assets, this field shows the next available fixed asset number.</span></span> <span data-ttu-id="30705-115">数値は変更できます。</span><span class="sxs-lookup"><span data-stu-id="30705-115">You can change the number.</span></span>   <span data-ttu-id="30705-116">手動での番号付けが固定資産に対して設定されている場合、このフィールドは空白で、新しい固定資産番号を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30705-116">If manual numbering is set up for fixed assets, this field is blank, and you must enter the new fixed asset number.</span></span>  
6. <span data-ttu-id="30705-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="30705-117">Click OK.</span></span>
7. <span data-ttu-id="30705-118">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="30705-118">Click Yes.</span></span>



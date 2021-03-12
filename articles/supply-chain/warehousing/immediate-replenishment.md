---
title: 即時補充
description: このトピックでは、場所のディレクティブが在庫の配賦に失敗したときに、在庫を補充するため、即時補充を使用する方法について説明します。
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 6e2919c003d1dc67b988345260b2747364752222
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004780"
---
# <a name="immediate-replenishment"></a><span data-ttu-id="53389-103">即時補充</span><span class="sxs-lookup"><span data-stu-id="53389-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53389-104">場所ディレクティブの明細行が在庫の配賦に失敗した直後に、在庫を補充するため、即時補充ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="53389-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="53389-105">補充は、場所ディレクティブの設定における単一明細行に基づいています。</span><span class="sxs-lookup"><span data-stu-id="53389-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="53389-106">その明細行で指定されている測定単位の在庫の手持がない場合、その測定単位の補充がすぐに発生します。</span><span class="sxs-lookup"><span data-stu-id="53389-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="53389-107">即時補充は、在庫の配賦が場所ディレクティブの複数の明細行に基づいており、要求が配賦の終わりに合計され、および場所ディレクティブの最後の明細行により指定される測定単位で補充される方法への代替を提供します。</span><span class="sxs-lookup"><span data-stu-id="53389-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="53389-108">即時補充を使用する利点は、特定の場所に送信される特定の単位および数量により補充が制限できることです。</span><span class="sxs-lookup"><span data-stu-id="53389-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="53389-109">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="53389-109">Business scenario</span></span>

<span data-ttu-id="53389-110">たとえば、「ボックス」および「各」測定単位に対して個別のピッキング エリアを持つ倉庫があるとします。</span><span class="sxs-lookup"><span data-stu-id="53389-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="53389-111">できるだけ多くのボックスをピッキングしてから、「各」領域から 1 つのボックスより少ない残りの数量をピッキングすることにより、ピッキング プロセスを最適化するようにします。</span><span class="sxs-lookup"><span data-stu-id="53389-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="53389-112">この場合、即時補充を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="53389-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="53389-113">場所ディレクティブで、要求補充を使用して需要数量のボックスの不足分をすぐにピッキングできるよう、即時補充を設定できます。</span><span class="sxs-lookup"><span data-stu-id="53389-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="53389-114">これにより、できるだけ多くのボックスのピッキングが含まれるように、ピッキング プロセスを最適化します。</span><span class="sxs-lookup"><span data-stu-id="53389-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="53389-115">即時補充はボックスの補充を生成し、「各」測定単位でその数量がピッキングされるよう、要求は渡されません。</span><span class="sxs-lookup"><span data-stu-id="53389-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="53389-116">つまり、「各」測定単位(1 つのボックスより少ない数量) でピッキングするはずの数量のみが、「各」領域からピッキングされます。</span><span class="sxs-lookup"><span data-stu-id="53389-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="53389-117">「ボックス」領域に不足が発生した場合、合計要求からできるだけ多くのボックスをピッキングできます。</span><span class="sxs-lookup"><span data-stu-id="53389-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="53389-118">残りの数量は、その後「各」領域からピッキングされます。</span><span class="sxs-lookup"><span data-stu-id="53389-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="53389-119">該当する場所</span><span class="sxs-lookup"><span data-stu-id="53389-119">Where it applies</span></span>

<span data-ttu-id="53389-120">補充テンプレートが設定されている場所ディレクティブの明細行の配賦に失敗した場合、即時補充がウェーブ実行中に使用されます。</span><span class="sxs-lookup"><span data-stu-id="53389-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="53389-121">即時補充の設定</span><span class="sxs-lookup"><span data-stu-id="53389-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="53389-122">**倉庫管理** \> **設定** \> **場所ディレクティブ** の順に移動し、次に、**即時補充テンプレート** リストの **明細行** タブで、 ウェーブ需要に対する補充テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="53389-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="53389-123">場所ディレクティブの明細行が専用測定単位の配賦に失敗した場合は、補充テンプレートが適用されます。</span><span class="sxs-lookup"><span data-stu-id="53389-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="53389-124">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="53389-124">Troubleshooting</span></span>

<span data-ttu-id="53389-125">即時補充が場所ディレクティブの明細行に対して選択されているが、場所ディレクティブの明細行に対して要求補充テンプレートを使用する際に補充作業が生成されない場合、2 つの主要な原因を調査する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53389-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="53389-126">適用される要求補充テンプレートが、正しい場所テンプレートを使用し、**補充** タイプの作業テンプレートに設定されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="53389-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="53389-127">要求補充テンプレートが補充の手持在庫を検索する場所で、十分な手持在庫があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="53389-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>

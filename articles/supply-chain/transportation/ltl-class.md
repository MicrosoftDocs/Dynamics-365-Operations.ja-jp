---
title: トラック 1 台分未満 (LTL) のクラス
description: このトピックでは、トラック 1 台分未満 (LTL) のクラスについて説明し、Microsoft Dynamics 365 Supply Chain Management での設定方法について説明します。
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941813"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="e1313-103">トラック 1 台分未満 (LTL) のクラス</span><span class="sxs-lookup"><span data-stu-id="e1313-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1313-104">トラック 1 台分未満 (LTL) のクラスは、出荷可能な品目の分類に使用される貨物出荷クラスです。</span><span class="sxs-lookup"><span data-stu-id="e1313-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="e1313-105">一般に、製品または商品のすべてのタイプに、LTL 出荷の特定の貨物クラス番号に対応する貨物輸送分類 (NMFC) コードが設定されています。</span><span class="sxs-lookup"><span data-stu-id="e1313-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="e1313-106">LTL 貨物クラスは品目のカテゴリを表しますが、NMFC コードは 18 の各貨物クラスの特定の商品に関連しています。</span><span class="sxs-lookup"><span data-stu-id="e1313-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="e1313-107">この機能を使用すると、システムで次のタスクを実行できます:</span><span class="sxs-lookup"><span data-stu-id="e1313-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="e1313-108">会社で使用する LTL 貨物クラスを定義します。</span><span class="sxs-lookup"><span data-stu-id="e1313-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="e1313-109">各 LTL クラスを **NMFC コード** ページの NMFC コードに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e1313-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="e1313-110">詳細については、 [貨物輸送分類 (NMFC) コード](nmfc-codes.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1313-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="e1313-111">NMFC コード (および NMFC コードに関連付けられた LTL コード) を **製品** ページの各製品に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e1313-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="e1313-112">NMFC コードが割り当てられている各製品の LTL クラスを正確に評価します。</span><span class="sxs-lookup"><span data-stu-id="e1313-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="e1313-113">国際的な LTL 標準を確認して、各 LTL クラスの梱包要件を決定します。</span><span class="sxs-lookup"><span data-stu-id="e1313-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="e1313-114">この方法により、製品が保護され、安全に出荷されることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="e1313-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="e1313-115">各製品の LTL 貨物クラスに基づいて、正確な出荷見積を取得します。</span><span class="sxs-lookup"><span data-stu-id="e1313-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="e1313-116">このトピックでは、Microsoft Dynamics 365 Supply Chain Management で LTL クラスを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e1313-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="e1313-117">LTL クラスの作成</span><span class="sxs-lookup"><span data-stu-id="e1313-117">Create an LTL class</span></span>

<span data-ttu-id="e1313-118">LTL クラスを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e1313-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="e1313-119">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="e1313-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="e1313-120">**倉庫管理 \> 設定 \> 在庫 \> LTL クラス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e1313-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="e1313-121">**輸送管理 \> 設定 \> 輸送標準 \> LTL クラス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e1313-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="e1313-122">アクション ウィンドウで **新規** を選択し、LTL クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e1313-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="e1313-123">その後、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="e1313-123">Then set the following fields:</span></span>

    - <span data-ttu-id="e1313-124">**LTL クラス** – 商品タイプに対する会社の内部 LTL クラス識別子 (ID) を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1313-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="e1313-125">ほとんどの会社では国際標準を使用しています。</span><span class="sxs-lookup"><span data-stu-id="e1313-125">Most companies use the international standard.</span></span> <span data-ttu-id="e1313-126">その場合、このフィールドの値は **クラス** フィールドの値と一致します。</span><span class="sxs-lookup"><span data-stu-id="e1313-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="e1313-127">ただし、会社が独自の標準を使用している場合は、その標準に準拠するコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="e1313-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="e1313-128">**名前** – 自分やほかのユーザーが各 NMFC コードに対して正しい LTL クラスを選択するのに役立つ内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1313-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="e1313-129">**クラス** – 商品タイプの国際標準 LTL クラス ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1313-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="e1313-130">ここで入力するコードは、公式の標準に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1313-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="e1313-131">例: LTL クラスの設定</span><span class="sxs-lookup"><span data-stu-id="e1313-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="e1313-132">次の例は、異なるタイプの製品で使用できる 2 つの異なる LTL クラスの設定方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e1313-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="e1313-133">**倉庫管理 \> 設定 \> 在庫 \> LTL クラス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e1313-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="e1313-134">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1313-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e1313-135">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="e1313-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e1313-136">**LTL クラス :** *92.5*</span><span class="sxs-lookup"><span data-stu-id="e1313-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="e1313-137">**名前 :** *コンピューター、モニター、冷蔵庫*</span><span class="sxs-lookup"><span data-stu-id="e1313-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="e1313-138">**クラス :** *92.5*</span><span class="sxs-lookup"><span data-stu-id="e1313-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="e1313-139">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1313-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e1313-140">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1313-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e1313-141">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="e1313-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e1313-142">**LTL クラス :** *125*</span><span class="sxs-lookup"><span data-stu-id="e1313-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="e1313-143">**名前 :** *小さな家庭電化製品*</span><span class="sxs-lookup"><span data-stu-id="e1313-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="e1313-144">**クラス :** *125*</span><span class="sxs-lookup"><span data-stu-id="e1313-144">**Class:** *125*</span></span>

1. <span data-ttu-id="e1313-145">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1313-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1313-146">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e1313-146">Additional resources</span></span>

- [<span data-ttu-id="e1313-147">貨物輸送分類 (NMFC) コード</span><span class="sxs-lookup"><span data-stu-id="e1313-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="e1313-148">船荷証券の作成</span><span class="sxs-lookup"><span data-stu-id="e1313-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

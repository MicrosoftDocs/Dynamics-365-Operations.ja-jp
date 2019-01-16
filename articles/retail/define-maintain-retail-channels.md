---
title: "小売チャンネルの定義と管理"
description: "このトピックでは、Microsoft Dynamics 365 for Retail では小売店舗とも呼ばれる、従来型の店舗を設定するプロセスの概要を説明します。 ここでは、小売店舗を設定する前と後の、実施する必要のあるタスクについて説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 53ba6cdb2378ce9011c6e7e3ce4e67c789adb1e6
ms.contentlocale: ja-jp
ms.lasthandoff: 01/04/2019

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="8fa46-104">小売チャンネルの定義と管理</span><span class="sxs-lookup"><span data-stu-id="8fa46-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8fa46-105">このトピックでは、Microsoft Dynamics 365 for Retail では小売店舗とも呼ばれる、従来型の店舗を設定するプロセスの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="8fa46-106">ここでは、小売店舗を設定する前と後の、実施する必要のあるタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="8fa46-107">Dynamics 365 for Retail は、オンライン ストア、コール センター、また実店舗などの、複数の小売チャンネルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="8fa46-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="8fa46-108">従来型の店舗は、小売店舗とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="8fa46-109">各小売店舗は、独自の支払方法、価格グループ、POS レジスタ、収入/経費勘定、およびスタッフを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="8fa46-110">作成する前に、小売店舗のこれらすべての要素を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fa46-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="8fa46-111">小売店舗を作成したら、店舗に配送される製品を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="8fa46-112">また、店舗への従業員、レジスター、および顧客の割り当ても行います。</span><span class="sxs-lookup"><span data-stu-id="8fa46-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="8fa46-113">最後に、組織階層に新しい店舗を追加します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="8fa46-114">小売店舗の設定</span><span class="sxs-lookup"><span data-stu-id="8fa46-114">Setting up retail stores</span></span>

<span data-ttu-id="8fa46-115">Dynamics 365 for Retail で小売店舗を設定する前に、必要なタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fa46-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="8fa46-116">その後、小売店舗を作成し、詳細を追加できます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8fa46-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="8fa46-117">Prerequisites</span></span>

<span data-ttu-id="8fa46-118">小売店舗を設定する前に次の作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fa46-118">You must complete the following tasks before you can set up a retail store:</span></span>

1. <span data-ttu-id="8fa46-119">組織構造を設定し、小売品揃え、補充、およびレポートの組織階層を設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="8fa46-120">小売店舗を表す倉庫を設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-120">Set up a warehouse that represents the retail store.</span></span>
3. <span data-ttu-id="8fa46-121">小売店舗、店舗明細書と明細書の伝票の番号順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="8fa46-122">小売用パラメーターをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="8fa46-122">Configure parameters for Retail.</span></span>
5. <span data-ttu-id="8fa46-123">店舗で受け入れる支払方法を設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="8fa46-124">Retail POS のレジスターでクレジット カード取引を処理する場合、支払サービスも設定できます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="8fa46-125">売上税グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="8fa46-126">小売製品を設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-126">Set up retail products.</span></span> <span data-ttu-id="8fa46-127">このタスクの一部として、小売製品階層、製品バリアントおよび製品の品揃えを設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="8fa46-128">製品価格グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-128">Set up product price groups.</span></span>
10. <span data-ttu-id="8fa46-129">小売製品価格を設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-129">Set up retail product pricing.</span></span> <span data-ttu-id="8fa46-130">このタスクの一部として、価格調整、割引および割引期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="8fa46-131">スタッフ メンバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8fa46-132">Dynamics 365 for Retail for Retail POS システムを使用してサインインし、タスクを実行できるように、作業者に適切なアクセス許可を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fa46-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>

12. <span data-ttu-id="8fa46-133">店舗に割り当てる Retail POS のプロファイルをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="8fa46-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="8fa46-134">タスクには、登録設定、オフライン プロファイルの設定、レシートの形式とプロファイルの設定などの多くのタスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="8fa46-135">これらの前提条件に含まれるタスクすべてを確認し、適用するタスクのみを実行します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="8fa46-136">小売店舗の設定</span><span class="sxs-lookup"><span data-stu-id="8fa46-136">Set up a retail store</span></span>

<span data-ttu-id="8fa46-137">必要な作業を完了した後、小売店舗の詳細を設定する次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1. <span data-ttu-id="8fa46-138">小売店舗を作成します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-138">Create a retail store.</span></span>
2. <span data-ttu-id="8fa46-139">店舗に売上税グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="8fa46-140">店舗に受け入れられている支払方法を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="8fa46-141">小売店舗で提供する製品の説明に詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="8fa46-142">たとえば、リッチ テキストと画像を追加できます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="8fa46-143">これらの製品の詳細は POS レジスターやまたは印刷されたラベルなど、さまざまなコンテキストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="8fa46-144">**小売品揃え**、**小売補充**、または**小売レポート**のために割当てられる既存の組織階層に店舗を追加します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="8fa46-145">小売店舗を設定した後</span><span class="sxs-lookup"><span data-stu-id="8fa46-145">After you set up a retail store</span></span>

<span data-ttu-id="8fa46-146">小売店舗の詳細を入力したら、Retail POS に新しい小売店舗のデータを送信するための次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1. <span data-ttu-id="8fa46-147">店舗の POS レジスターをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="8fa46-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="8fa46-148">店舗に、製品の品揃えを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="8fa46-149">品揃えを処理し、品揃えに含める製品のリストを生成して製品を小売店舗で販売できるようにします。</span><span class="sxs-lookup"><span data-stu-id="8fa46-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4. <span data-ttu-id="8fa46-150">番号順序、ハードウェア プロファイル、POS 画面レイアウトなどのデータを Retail POS レジスターに送信します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5. <span data-ttu-id="8fa46-151">小売店舗を公開して、Retail POS に店舗データを送信します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-151">Publish the retail store to send store data to Retail POS.</span></span>
6. <span data-ttu-id="8fa46-152">Retail POS に店舗のデータを送信するジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="8fa46-153">組織階層</span><span class="sxs-lookup"><span data-stu-id="8fa46-153">Organization hierarchies</span></span>

<span data-ttu-id="8fa46-154">Retail は、組織階層を使用して小売チャンネルを構成します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="8fa46-155">組織階層は、業務を構成する組織の関係を表します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="8fa46-156">店舗を設定すると、組織階層にその店舗を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="8fa46-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="8fa46-157">店舗では、品揃え、補充、およびレポートに使用されるデータを共有します。</span><span class="sxs-lookup"><span data-stu-id="8fa46-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>


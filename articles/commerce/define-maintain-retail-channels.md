---
title: 小売チャンネルの定義と管理
description: このトピックでは、Dynamics 365 Commerce では店舗とも呼ばれる、従来型の店舗を設定するプロセスの概要を提供します。 ここでは、店舗を設定する前と後に実施する必要のあるタスクについて説明します。
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 63639d69af90c6aa37bbf7af7868bca71942063f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023125"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="b9517-104">小売チャネルの定義と管理</span><span class="sxs-lookup"><span data-stu-id="b9517-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b9517-105">このトピックでは、Dynamics 365 Commerce では店舗とも呼ばれる、従来型の店舗を設定するプロセスの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="b9517-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="b9517-106">ここでは、店舗を設定する前と後に実施する必要のあるタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b9517-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="b9517-107">Commerce は、オンライン ストア、コール センターと従来型の店舗などの、複数のチャネルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b9517-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="b9517-108">従来型の店舗は、店舗とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b9517-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="b9517-109">各店舗は、独自の支払方法、価格グループ、POS レジスター、収入/経費勘定、およびスタッフを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="b9517-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="b9517-110">作成する前に、店舗のこれらすべての要素を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9517-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="b9517-111">店舗を作成した後、店舗に配送される製品を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b9517-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="b9517-112">また、店舗への従業員、レジスター、および顧客の割り当ても行います。</span><span class="sxs-lookup"><span data-stu-id="b9517-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="b9517-113">最後に、組織階層に新しい店舗を追加します。</span><span class="sxs-lookup"><span data-stu-id="b9517-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="b9517-114">店舗の設定</span><span class="sxs-lookup"><span data-stu-id="b9517-114">Setting up stores</span></span>

<span data-ttu-id="b9517-115">Commerce で店舗を設定する前に必要な作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9517-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="b9517-116">その後、店舗を作成し、詳細を追加できます。</span><span class="sxs-lookup"><span data-stu-id="b9517-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="b9517-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="b9517-117">Prerequisites</span></span>

<span data-ttu-id="b9517-118">店舗を設定する前に次の作業を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9517-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="b9517-119">組織構造を設定し、小売品揃え、補充、およびレポートの組織階層を設定します。</span><span class="sxs-lookup"><span data-stu-id="b9517-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="b9517-120">店舗を表す倉庫を設定します。</span><span class="sxs-lookup"><span data-stu-id="b9517-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="b9517-121">店舗、店舗明細書、および明細書の伝票の番号順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="b9517-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="b9517-122">Commerce パラメーターをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b9517-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="b9517-123">店舗で受け入れる支払方法を設定します。</span><span class="sxs-lookup"><span data-stu-id="b9517-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="b9517-124">Retail POS のレジスターでクレジット カード取引を処理する場合、支払サービスも設定できます。</span><span class="sxs-lookup"><span data-stu-id="b9517-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="b9517-125">売上税グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="b9517-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="b9517-126">小売製品を設定します。</span><span class="sxs-lookup"><span data-stu-id="b9517-126">Set up retail products.</span></span> <span data-ttu-id="b9517-127">このタスクの一部として、製品階層、製品バリアント、および製品の品揃えを設定します。</span><span class="sxs-lookup"><span data-stu-id="b9517-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="b9517-128">製品価格グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="b9517-128">Set up product price groups.</span></span>
10. <span data-ttu-id="b9517-129">製品価格を設定します。</span><span class="sxs-lookup"><span data-stu-id="b9517-129">Set up product pricing.</span></span> <span data-ttu-id="b9517-130">このタスクの一部として、価格調整、割引および割引期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="b9517-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="b9517-131">スタッフ メンバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="b9517-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b9517-132">POS システムを使用してサインインし、タスクを実行できるように、作業者に適切なアクセス許可を割り当てる必要もあります。</span><span class="sxs-lookup"><span data-stu-id="b9517-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="b9517-133">店舗に割り当てる POS プロファイルをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b9517-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="b9517-134">タスクには、登録設定、オフライン プロファイルの設定、レシートの形式とプロファイルの設定などの多くのタスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9517-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="b9517-135">前提条件に含まれるタスクすべてを確認し、適用するタスクのみを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9517-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="b9517-136">店舗の設定</span><span class="sxs-lookup"><span data-stu-id="b9517-136">Set up a store</span></span>

<span data-ttu-id="b9517-137">前提条件のタスクを完了した後、店舗の詳細を設定する次のタスクを完了します。</span><span class="sxs-lookup"><span data-stu-id="b9517-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="b9517-138">店舗を作成していること。</span><span class="sxs-lookup"><span data-stu-id="b9517-138">Create a store.</span></span>
2. <span data-ttu-id="b9517-139">店舗に売上税グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b9517-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="b9517-140">店舗に受け入れられている支払方法を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b9517-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="b9517-141">店舗で提供する製品の説明に詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="b9517-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="b9517-142">たとえば、リッチ テキストと画像を追加できます。</span><span class="sxs-lookup"><span data-stu-id="b9517-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="b9517-143">これらの製品の詳細は POS レジスターやまたは印刷されたラベルなど、さまざまなコンテキストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9517-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="b9517-144">**小売品揃え**、**小売補充**、または**小売レポート**のために割当てられる既存の組織階層に店舗を追加します。</span><span class="sxs-lookup"><span data-stu-id="b9517-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="b9517-145">店舗を設定した後</span><span class="sxs-lookup"><span data-stu-id="b9517-145">After you set up a store</span></span>

<span data-ttu-id="b9517-146">店舗の詳細を入力した後、次のタスクを実行して、POS に新しい店舗のデータを送信します。</span><span class="sxs-lookup"><span data-stu-id="b9517-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="b9517-147">店舗の POS レジスターをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b9517-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="b9517-148">店舗に、製品の品揃えを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b9517-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="b9517-149">品揃えを処理し、品揃えに含める製品のリストを生成して製品を店舗で販売できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b9517-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="b9517-150">番号順序、ハードウェア プロファイル、POS 画面レイアウトなどのデータを POS レジスターに送信します。</span><span class="sxs-lookup"><span data-stu-id="b9517-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="b9517-151">店舗を公開して、POS に店舗データを送信します。</span><span class="sxs-lookup"><span data-stu-id="b9517-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="b9517-152">POS に店舗のデータを送信するジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9517-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="b9517-153">組織階層</span><span class="sxs-lookup"><span data-stu-id="b9517-153">Organization hierarchies</span></span>

<span data-ttu-id="b9517-154">Commerce は、チャネルを構成する組織階層を使用します。</span><span class="sxs-lookup"><span data-stu-id="b9517-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="b9517-155">組織階層は、業務を構成する組織の関係を表します。</span><span class="sxs-lookup"><span data-stu-id="b9517-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="b9517-156">店舗を設定すると、組織階層にその店舗を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b9517-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="b9517-157">店舗では、品揃え、補充、およびレポートに使用されるデータを共有します。</span><span class="sxs-lookup"><span data-stu-id="b9517-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="b9517-158">小売販売機能を使用するには、**複数の出荷先**のコンフィギュレーション キーが有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9517-158">To use Retail sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="b9517-159">このコンフィギュレーション キーは、**システム管理**\> **設定** \> **ライセンス コンフィギュレーション**の下で、**取引コンフィギュレーション** キーで検索できます。</span><span class="sxs-lookup"><span data-stu-id="b9517-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="b9517-160">これは、販売注文明細行レベルでコンフィギュレーションされた配送先住所に基づいて、さまざまな検証を実行する小売機能のために必要です。</span><span class="sxs-lookup"><span data-stu-id="b9517-160">This is required due to Retail functionality that performs various validations based on the delivery address configured at the sales order line level.</span></span>


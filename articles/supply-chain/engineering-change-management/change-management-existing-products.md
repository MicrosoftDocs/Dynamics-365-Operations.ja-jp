---
title: 既存の製品の変更管理の有効化
description: このトピックでは、既存の製品の変更管理を有効にする方法を説明します。 また、変更管理を有効にできる機能が制限されるケースについて説明します。
author: t-benebo
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 8b9f34f5980937da62610d9668a95816ba6054ef
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500865"
---
# <a name="enable-change-management-on-existing-products"></a><span data-ttu-id="67b7d-104">既存の製品の変更管理の有効化</span><span class="sxs-lookup"><span data-stu-id="67b7d-104">Enable change management on existing products</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="67b7d-105">このトピックでは、既存の製品の変更管理を有効にする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-105">This topic explains how you can enable change management for existing products.</span></span> <span data-ttu-id="67b7d-106">また、変更管理を有効にできる機能が制限されるケースについて説明します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-106">It also describes cases where your ability to enable change management is limited.</span></span>

<span data-ttu-id="67b7d-107">既存の製品の変更管理を有効にすると、その製品のバージョンを作成し、その製品の存続期間を通じて行われた変更を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-107">When you enable change management for an existing product, you can create versions of that product and trace changes that are made to it throughout its life.</span></span> <span data-ttu-id="67b7d-108">したがって、変更オーダーを使用することでそれらの変更を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-108">Therefore, you can track those changes by using change orders.</span></span> <span data-ttu-id="67b7d-109">変更管理を有効にするには、関連する製品を *エンジニアリング品目* (エンジニアリング製品とも呼ばれます) に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-109">To enable change management, you must convert the relevant products to *engineering items* (also referred to as engineering products).</span></span> <span data-ttu-id="67b7d-110">エンジニアリング製品は、変更管理によってバージョン指定され、管理される製品です。</span><span class="sxs-lookup"><span data-stu-id="67b7d-110">Engineering products are products that are versioned and managed through change management.</span></span> <span data-ttu-id="67b7d-111">ウィザードに従って変換プロセスを実行できます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-111">A wizard is provided to guide you through the conversion process.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="67b7d-112">システムで機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="67b7d-112">Turn on the feature in your system</span></span>

<span data-ttu-id="67b7d-113">この機能を使用するには、次の設定手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-113">To use this capability, you must complete the following tasks:</span></span>

1. <span data-ttu-id="67b7d-114">[エンジニアリング変更管理の概要](product-engineering-overview.md) の説明に従って、エンジニアリング変更管理および構成キーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="67b7d-114">Enable the Engineering change management feature and its configuration key as described in [Engineering change management overview](product-engineering-overview.md).</span></span>
1. <span data-ttu-id="67b7d-115">機能管理で *既存の製品の変更管理の有効化* 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="67b7d-115">Turn on the *Enable change management on existing products* feature in feature management.</span></span> <span data-ttu-id="67b7d-116">詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67b7d-116">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="restrictions-and-limitations"></a><span data-ttu-id="67b7d-117">規制と制限</span><span class="sxs-lookup"><span data-stu-id="67b7d-117">Restrictions and limitations</span></span>

<span data-ttu-id="67b7d-118">すべての製品タイプを他のすべてのタイプに変換できるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="67b7d-118">Not all product types can be converted to all other types.</span></span> <span data-ttu-id="67b7d-119">適用される規制と制限は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="67b7d-119">The following restrictions and limitations apply:</span></span>

- <span data-ttu-id="67b7d-120">製品をエンジニアリング製品に変換する場合、この製品は *製品* のままです。</span><span class="sxs-lookup"><span data-stu-id="67b7d-120">When you convert a product to an engineering product, it remains a *product*.</span></span> <span data-ttu-id="67b7d-121">*製品マスター* にはなりません。</span><span class="sxs-lookup"><span data-stu-id="67b7d-121">It doesn't become a *product master*.</span></span>
- <span data-ttu-id="67b7d-122">特定の分析コード セットを持つ製品マスターを変換する場合、それらの分析コードは変更後も維持されます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-122">When you convert a product master that has a specific set of dimensions, those dimensions are maintained after the change.</span></span> <span data-ttu-id="67b7d-123">たとえば、サイズ分析コードを持つ製品マスターを変換した場合、サイズ分析コードは維持されます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-123">For example, if you convert a product master that has the size dimension, it will keep the size dimension.</span></span>

<span data-ttu-id="67b7d-124">したがって、特徴的製品がある場合は、トランザクションの製品分析コードを追跡しない (つまり、バージョン分析コードが使用されていない) エンジニアリング製品にのみ変更できます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-124">Therefore, if you have a distinct product, you can change it only to an engineering product that doesn't track the product dimension in transactions (that is, the version dimension isn't used).</span></span> <span data-ttu-id="67b7d-125">これらの問題に関する詳細については、このトピックの残りのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="67b7d-125">See the remaining sections of this topic for more information about these issues.</span></span>

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a><span data-ttu-id="67b7d-126">必要なすべてのエンジニアリング製品カテゴリを作成して、変換の準備をする</span><span class="sxs-lookup"><span data-stu-id="67b7d-126">Prepare for conversion by creating all required engineering product categories</span></span>

<span data-ttu-id="67b7d-127">*エンジニアリング製品カテゴリ* は、すべてのエンジニアリング製品に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-127">An *engineering product category* must be assigned to every engineering product.</span></span> <span data-ttu-id="67b7d-128">この割り当ては、**エンジニアリング製品に変換** ウィザードを実行するときに行います。</span><span class="sxs-lookup"><span data-stu-id="67b7d-128">You will do this assignment when you run the **Convert to engineering product** wizard.</span></span> <span data-ttu-id="67b7d-129">エンジニアリング製品カテゴリは、関連する標準製品を変換する *前* に、すべての標準製品に対して存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-129">Engineering product categories must exist for all relevant standard products *before* you can convert those products.</span></span>

<span data-ttu-id="67b7d-130">エンジニアリング製品カテゴリは、エンジニアリング製品を作成するための基礎を提供し、一連の既定値とポリシーを設定します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-130">The engineering product category provides a basis for creating an engineering product, and it establishes a set of default values and policies.</span></span> <span data-ttu-id="67b7d-131">エンジニアリング製品カテゴリは、割り当てる製品と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-131">The engineering product category must match the product that you assign it to.</span></span> <span data-ttu-id="67b7d-132">たとえば、製品タイプと分析コード グループは、製品およびエンジニアリング製品カテゴリの両方と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-132">For example, the product type and dimension group must match both the product and its engineering product category.</span></span> <span data-ttu-id="67b7d-133">詳細については、[エンジニアリング バージョンとエンジニアリング製品カテゴリ](engineering-versions-product-category.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67b7d-133">For more information, see [Engineering versions and engineering product categories](engineering-versions-product-category.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67b7d-134">**エンジニアリング製品への変換** ウィザードを使用すると、トランザクションでバージョンが追跡されていないエンジニアリング製品にのみ製品を変換できます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-134">The **Convert to engineering product** wizard can convert product only to engineering products where the version isn't tracked in transactions.</span></span> <span data-ttu-id="67b7d-135">したがって、**トランザクションのバージョンを追跡** オプションは、既存の製品を変換するために作成するエンジニアリング製品カテゴリでは *いいえ* に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-135">Therefore, the **Track version in transactions** option must be set to *No* for engineering product categories that you create to convert existing products.</span></span>

<span data-ttu-id="67b7d-136">エンジニアリング製品カテゴリの作成方法については、[エンジニアリング バージョンとエンジニアリング製品カテゴリ](engineering-versions-product-category.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67b7d-136">For information about how to create engineering product categories, see [Engineering versions and engineering product categories](engineering-versions-product-category.md).</span></span>

## <a name="run-the-convert-to-engineering-product-wizard"></a><span data-ttu-id="67b7d-137">エンジニアリング製品への変換ウィザードの実行</span><span class="sxs-lookup"><span data-stu-id="67b7d-137">Run the Convert to engineering product wizard</span></span>

<span data-ttu-id="67b7d-138">**エンジニアリング製品への変換** ウィザードを使用すると、1 つ以上の既存の製品をエンジニアリング製品に変換できます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-138">The **Convert to engineering product** wizard helps you convert one or more existing products to engineering products.</span></span> <span data-ttu-id="67b7d-139">製品をエンジニアリング製品 (バージョン管理された製品) に変換します。この場合、バージョンはトランザクションで追跡されません (つまり、バージョン分析コードは使用されません)。</span><span class="sxs-lookup"><span data-stu-id="67b7d-139">It converts the products into engineering products (versioned products) where the version isn't tracked in transactions (that is, the version dimension isn't used).</span></span> <span data-ttu-id="67b7d-140">変換が完了した後は、エンジニアリング変更管理を使用して製品を管理できます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-140">After the conversion is completed, you can manage the products by using Engineering change management.</span></span>

<span data-ttu-id="67b7d-141">換算は永続的です。</span><span class="sxs-lookup"><span data-stu-id="67b7d-141">The conversion is permanent.</span></span> <span data-ttu-id="67b7d-142">したがって、後で取り消すことはできません。</span><span class="sxs-lookup"><span data-stu-id="67b7d-142">Therefore, you won't be able to reverse it later.</span></span> 

<span data-ttu-id="67b7d-143">変換された各エンジニアリング製品は、元の製品がリリースされたのと同じ会社でリリースされ続けます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-143">Each converted engineering product will continue to be released in the same companies that the original product was released in.</span></span> <span data-ttu-id="67b7d-144">ただし、エンジニアリング部品表 (BOM) および工順は、これらの会社に自動的にはリリースされません。</span><span class="sxs-lookup"><span data-stu-id="67b7d-144">However, the engineering bill of materials (BOM) and routes won't automatically be released to those companies.</span></span>

<span data-ttu-id="67b7d-145">次の手順に従って、**エンジニアリング製品への変換** ウィザードを実行して、製品をエンジニアリング製品に変換します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-145">Follow these steps to run the **Convert to engineering product** wizard and convert a product to an engineering product.</span></span>

1. <span data-ttu-id="67b7d-146">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-146">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="67b7d-147">グリッドで、変換する各製品のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="67b7d-147">In the grid, select the check box for each product that you want to convert.</span></span>
1. <span data-ttu-id="67b7d-148">アクション ウィンドウの **エンジニア** タブの **エンジニアリング変更管理** グループで、**エンジニアリング製品への変換** を選択して、ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-148">On the Action Pane, on the **Engineer** tab, in the **Engineering change management** group, select **Convert to engineering product** to open the wizard.</span></span>
1. <span data-ttu-id="67b7d-149">ウィザードの最初のページは **ようこそ** ページです。</span><span class="sxs-lookup"><span data-stu-id="67b7d-149">The first page of the wizard is the **Welcome** page.</span></span> <span data-ttu-id="67b7d-150">変換プロセスにまだ慣れていない場合は、このページの情報を注意深く読んでください。</span><span class="sxs-lookup"><span data-stu-id="67b7d-150">If you aren't already familiar with the conversion process, carefully read the information on this page.</span></span> <span data-ttu-id="67b7d-151">続行する準備が整ったら、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-151">When you're ready to continue, select **Next**.</span></span>
1. <span data-ttu-id="67b7d-152">**変換する製品の詳細を選択** ページには、ウィザードを開く前に選択した各製品が表示されます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-152">The **Select details for the products to be converted** page shows each product that you selected before you opened the wizard.</span></span> <span data-ttu-id="67b7d-153">リストを確認します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-153">Inspect the list.</span></span> <span data-ttu-id="67b7d-154">ツールバーの **新規** や **削除** ボタンを使用して、必要に応じて製品を追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-154">Use the **New** and **Delete** buttons on the toolbar to add or remove products as you require.</span></span>
1. <span data-ttu-id="67b7d-155">表示されている各製品に既定値を割り当てるには、グリッドの一番上にあるフィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-155">Use the following fields at the top of the grid to assign default values to every product that is listed.</span></span> <span data-ttu-id="67b7d-156">(変換の完了後に、これらの値を個々の製品に対して変更することができます。) 既定値は、関連する値が既に割り当てられている製品には割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="67b7d-156">(You will be able to change these values for individual products after the conversion is completed.) Default values won't be assigned to products where a relevant value has already been assigned.</span></span>

    - <span data-ttu-id="67b7d-157">**既定のエンジニアリング カテゴリ** – 一覧表示されているすべての製品に割り当てる最初のエンジニアリング製品カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-157">**Default engineering category** – Select an initial engineering product category to assign to every listed product.</span></span> <span data-ttu-id="67b7d-158">選択したカテゴリは、互換性のある製品にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-158">The category that you select will be applied only to products that are compatible with it.</span></span>
    - <span data-ttu-id="67b7d-159">**既定のバージョン** – 一覧表示されているすべての製品に割り当てる最初の製品バージョンを入力します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-159">**Default version** – Enter the initial product version to assign to every listed product.</span></span> <span data-ttu-id="67b7d-160">すべてのエンジニアリング製品には、1 つ以上のエンジニアリング バージョンがあります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-160">Every engineering product has at least one engineering version.</span></span>
    - <span data-ttu-id="67b7d-161">**既定のライフサイクルの状態** – 一覧表示されているすべての製品に割り当てる最初のライフサイクルの状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-161">**Default lifecycle state** – Select the initial product lifecycle state to assign to every listed product.</span></span>
    - <span data-ttu-id="67b7d-162">**現在のBOMがエンジニアリング製品の一部になる場合** – 一覧表示されている各製品の現在の BOM をエンジニアリング製品の BOM として使用する必要がある場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="67b7d-162">**Current BOM will be part of the engineering product** – Select this check box if the current BOM for each listed product should be used as a BOM for the engineering product.</span></span>

    <span data-ttu-id="67b7d-163">製品設定の詳細については、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67b7d-163">For more information about product settings, see the next step.</span></span>

1. <span data-ttu-id="67b7d-164">グリッドに一覧表示されている各製品を確認し、割り当てた既定値がその製品にどの程度適切に適用されているかを評価します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-164">Review each product that is listed in the grid, and evaluate how well the default values that you assigned apply to it.</span></span> <span data-ttu-id="67b7d-165">各行について、次の情報を確認し、関連するフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-165">For each row, review the following information and set any relevant fields:</span></span>

    - <span data-ttu-id="67b7d-166">**製品番号** – 製品の番号。</span><span class="sxs-lookup"><span data-stu-id="67b7d-166">**Product number** – The product number.</span></span>
    - <span data-ttu-id="67b7d-167">**製品名** – 製品の名前。</span><span class="sxs-lookup"><span data-stu-id="67b7d-167">**Product name** – The name of the product.</span></span>
    - <span data-ttu-id="67b7d-168">**エンジニアリング カテゴリ** – 製品が変換された後に属するエンジニアリング 製品カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-168">**Engineering category** – Select the engineering product category that the product should belong to after it's converted.</span></span> <span data-ttu-id="67b7d-169">このトピックの前のセクションで説明したように、各製品には適切なカテゴリが既に存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-169">An appropriate category must already exist for each product, as was explained in the previous section of this topic.</span></span> <span data-ttu-id="67b7d-170">すべての製品にカテゴリを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-170">You must assign a category to every product.</span></span>
    - <span data-ttu-id="67b7d-171">**バージョン** – 変換後にその製品に割り当てる製品バージョンを入力します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-171">**Version** – Enter the product version to assign to the product after it's converted.</span></span> <span data-ttu-id="67b7d-172">たとえば、カテゴリで既に使用している番号順序に合う番号を選択できます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-172">For example, you might select a number that fits in the number sequence that your category already uses.</span></span> <span data-ttu-id="67b7d-173">各エンジニアリング バージョンには、そのバージョンに固有のエンジニアリング関連データが格納されます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-173">Each engineering version stores the engineering-relevant data that is specific to that version.</span></span> <span data-ttu-id="67b7d-174">詳細については、[エンジニアリング バージョンとエンジニアリング製品カテゴリ](engineering-versions-product-category.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67b7d-174">For more information, see [Engineering versions and engineering product categories](engineering-versions-product-category.md).</span></span>
    - <span data-ttu-id="67b7d-175">**製品のライフサイクルの状態** – 製品が変換された後の製品のライフサイクルの状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-175">**Product lifecycle state** – Select the product lifecycle state that the product should be in after it's converted.</span></span> <span data-ttu-id="67b7d-176">製品のライフサイクル状態により、特定のエンジニアリング バージョンで許可されるトランザクションを制御できます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-176">The product lifecycle state lets you to control which transactions are allowed for a given engineering version.</span></span> <span data-ttu-id="67b7d-177">詳細については、[製品ライフサイクルの状態とトランザクション](product-lifecycle-state-transactions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67b7d-177">For more information, see [Product lifecycle states and transactions](product-lifecycle-state-transactions.md).</span></span>
    - <span data-ttu-id="67b7d-178">**BOM あり** – このチェック ボックスがオンの場合、その製品には BOM が使用されています。</span><span class="sxs-lookup"><span data-stu-id="67b7d-178">**Has BOM** – A selected check box indicates that the product has a BOM.</span></span> <span data-ttu-id="67b7d-179">このチェック ボックスの設定は、**現在の BOM をエンジニアリング製品に含める** チェック ボックスをオンにするかどうかを決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-179">The setting of this check box can help you decide how to set the **Current BOM will be part of the engineering product** check box.</span></span>
    - <span data-ttu-id="67b7d-180">**現在のBOMがエンジニアリング製品の一部になる場合** – 製品の現在の BOM をエンジニアリング製品の BOM として使用する必要がある場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="67b7d-180">**Current BOM will be part of the engineering product** – Select this check box if the current BOM of the product should be used as a BOM for the engineering product.</span></span> <span data-ttu-id="67b7d-181">その BOMは 、エンジニアリング変更管理によって管理されます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-181">That BOM will then be managed by Engineering change management.</span></span> <span data-ttu-id="67b7d-182">製品に BOM が存在しない場合、または変換された製品の BOM を後ほど手動で作成する場合は、このチェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="67b7d-182">If the product doesn't have a BOM, or if you prefer to manually create a BOM for the converted product later, clear this check box.</span></span>
    - <span data-ttu-id="67b7d-183">**エラーあり** – このチェック ボックスがオンの場合、製品の設定に 1 つ以上のエラーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="67b7d-183">**Has errors** – A selected check box indicates that the product setup has one or more errors.</span></span> <span data-ttu-id="67b7d-184">たとえば、製品タイプや分析コード グループがカテゴリ内で一致していない場合があります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-184">For example, the product type or the dimension group might not match in the category.</span></span> <span data-ttu-id="67b7d-185">エラーがある製品はスキップされ、変換されません。</span><span class="sxs-lookup"><span data-stu-id="67b7d-185">Products that have errors will be skipped and won't be converted.</span></span>

1. <span data-ttu-id="67b7d-186">終了したら、ツール バーの **検証** を選択して製品の設定を検証します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-186">When you've finished, select **Validate** on the toolbar to validate the product setup.</span></span> <span data-ttu-id="67b7d-187">各行について **エラーあり** チェック ボックスが更新され、製品の状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-187">For each row, the **Has errors** check box will be updated to indicate the product's status.</span></span> <span data-ttu-id="67b7d-188">すべての製品の設定にエラーが発生しなくなるまで値を調整します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-188">Adjust the values until the setup of every product is free of errors.</span></span>
1. <span data-ttu-id="67b7d-189">すべての製品が正しく設定された後、**次へ** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-189">When all the products are set up correctly, select **Next** to continue.</span></span>
1. <span data-ttu-id="67b7d-190">**選択を確認する** ページには、設定でエラーが発生せず、換算可能な状態にある製品の数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="67b7d-190">The **Confirm selection** page shows the number of products that have no errors in their setup and are therefore ready for conversion.</span></span> <span data-ttu-id="67b7d-191">また、エラーが原因で省略される製品の数も示します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-191">It also shows the number of products that will be skipped because of errors.</span></span> <span data-ttu-id="67b7d-192">変換をバッチ ジョブとして実行するには、**バッチで実行** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-192">To run the conversion as a batch job, set the **Run in batch** option to *Yes*.</span></span>
1. <span data-ttu-id="67b7d-193">**完了** を選択して設定を適用し、製品のエンジニアリング製品への変換を開始します。</span><span class="sxs-lookup"><span data-stu-id="67b7d-193">Select **Finish** to apply your settings and start to convert the products to engineering products.</span></span>

> [!NOTE]
> <span data-ttu-id="67b7d-194">製品がリリースされる前にシステムが製品を手動で承認するように設定されている場合は、該当する会社の **製品リリースを開く** ページを使用して、変換された各製品を承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67b7d-194">If your system is set up to manually accept products before they are released, you must accept each converted product by using the **Open product releases** page in the appropriate companies.</span></span> <span data-ttu-id="67b7d-195">詳細については、[ローカル企業でリリースする前に製品を確認して承認する](engineering-scenarios.md#accept) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67b7d-195">For more information, see [Review and accept the product before you release it in the local company](engineering-scenarios.md#accept).</span></span>
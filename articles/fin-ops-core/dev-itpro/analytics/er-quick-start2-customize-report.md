---
title: ER 形式を調整してカスタム電子ドキュメントを生成
description: このトピックでは、Microsoft が提供する電子レポート (ER) 形式を調整して、カスタム電子ドキュメントを生成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20e7a32ac5f6ab21f89ed3c11c64458286864c9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680173"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="65bb7-103">ER 形式を調整してカスタム電子ドキュメントを生成</span><span class="sxs-lookup"><span data-stu-id="65bb7-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="65bb7-104">このトピックの手順では、システム管理者または電子レポート機能コンサルタントのロールのユーザーが次のタスクを実行する方法について説明します:</span><span class="sxs-lookup"><span data-stu-id="65bb7-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="65bb7-105">[電子申告 (ER) フレームワーク](general-electronic-reporting.md) のパラメーターを構成します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="65bb7-106">Microsoft が提供し、[仕入先支払](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) の処理中に、支払いファイルを生成するために使用する ER コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="65bb7-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="65bb7-107">Microsoft が提供する標準 ER 形式コンフィギュレーションのカスタム バージョンを作成します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="65bb7-108">カスタム ER 形式コンフィギュレーションを変更して、特定銀行の要求を満たす支払いファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="65bb7-109">カスタム ER 形式コンフィギュレーションで、標準 ER 形式コンフィギュレーションに対して行われた変更を採用します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="65bb7-110">次の手順はすべて **GBSI** 社で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="65bb7-111">コーディングは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="65bb7-111">No coding is required.</span></span>

- [<span data-ttu-id="65bb7-112">ER フレームワークのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65bb7-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="65bb7-113">ER パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65bb7-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="65bb7-114">ER コンフィギュレーション プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="65bb7-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="65bb7-115">ER 構成 プロバイダーの一覧を確認</span><span class="sxs-lookup"><span data-stu-id="65bb7-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="65bb7-116">新しい ER コンフィギュレーション プロバイダーを追加</span><span class="sxs-lookup"><span data-stu-id="65bb7-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="65bb7-117">ER コンフィギュレーション プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="65bb7-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="65bb7-118">標準 ER 形式 コンフィギュレーションをインポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="65bb7-119">標準 ER コンフィギュレーションをインポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="65bb7-120">インポートされた ER コンフィギュレーションのレビュー</span><span class="sxs-lookup"><span data-stu-id="65bb7-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="65bb7-121">処理用仕入先支払の準備</span><span class="sxs-lookup"><span data-stu-id="65bb7-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="65bb7-122">仕入先アカウントの銀行情報の追加</span><span class="sxs-lookup"><span data-stu-id="65bb7-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="65bb7-123">仕入先支払の入力</span><span class="sxs-lookup"><span data-stu-id="65bb7-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="65bb7-124">標準 ER 形式を使用した仕入先支払の処理</span><span class="sxs-lookup"><span data-stu-id="65bb7-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="65bb7-125">電子支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="65bb7-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="65bb7-126">仕入先支払のプロセス</span><span class="sxs-lookup"><span data-stu-id="65bb7-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="65bb7-127">標準 ER 形式のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="65bb7-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="65bb7-128">カスタム形式の作成</span><span class="sxs-lookup"><span data-stu-id="65bb7-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="65bb7-129">カスタム形式の編集</span><span class="sxs-lookup"><span data-stu-id="65bb7-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="65bb7-130">カスタム形式を実行可能としてマーク</span><span class="sxs-lookup"><span data-stu-id="65bb7-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="65bb7-131">カスタム ER 形式を使用した仕入先支払の処理</span><span class="sxs-lookup"><span data-stu-id="65bb7-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="65bb7-132">電子支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="65bb7-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="65bb7-133">仕入先支払のプロセス</span><span class="sxs-lookup"><span data-stu-id="65bb7-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="65bb7-134">標準 ER 形式コンフィギュレーションの新バージョンをインポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="65bb7-135">標準 ER コンフィギュレーションの新バージョンをインポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="65bb7-136">インポートされた ER 形式コンフィギュレーションのレビュー</span><span class="sxs-lookup"><span data-stu-id="65bb7-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="65bb7-137">インポートされた形式の新バージョンの変更をカスタム形式で採用</span><span class="sxs-lookup"><span data-stu-id="65bb7-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="65bb7-138">カスタム形式の現在のドラフト バージョンを完了</span><span class="sxs-lookup"><span data-stu-id="65bb7-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="65bb7-139">カスタム形式を新しい基準バージョンにリベース</span><span class="sxs-lookup"><span data-stu-id="65bb7-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="65bb7-140">リベースされた ER 形式を使用して仕入先支払の処理</span><span class="sxs-lookup"><span data-stu-id="65bb7-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="65bb7-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="65bb7-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a> <span data-ttu-id="65bb7-142">ER フレームワークをコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65bb7-142">Configure the ER framework</span></span>

<span data-ttu-id="65bb7-143">電子申告の機能コンサルタント ロールのユーザーは、ER フレームワークを使用して標準 ER 形式のカスタム バージョンをデザインする前に、最低限の ER パラメータのセットをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="65bb7-144">ER パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65bb7-144">Configure ER parameters</span></span>

1. <span data-ttu-id="65bb7-145">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65bb7-146">**ローカライズ構成** ページの、**関連リンク** セクションで、**電子申告パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="65bb7-147">**電子申告パラメーター** ページの、**一般** タブで、**デザイン モードの有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="65bb7-148">**添付** タブで、次のパラメーターを設定します:</span><span class="sxs-lookup"><span data-stu-id="65bb7-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="65bb7-149">**コンフィギュレーション** フィールドで、**USMF** 社の **ファイル** タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="65bb7-150">**ジョブ アーカイブ**、**一時的**、**ベースライン**、および **その他** フィールドで、**ファイル** タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="65bb7-151">ER パラメーターについては、[ER フレームワークのコンフィギュレーション](electronic-reporting-er-configure-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65bb7-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a> <span data-ttu-id="65bb7-152">ER コンフィギュレーション プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="65bb7-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="65bb7-153">追加されたすべての ER 構成は、ER 構成プロバイダーによって所有されているものとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="65bb7-154">**電子申告** ワークスペースで有効化された ER 構成プロバイダーは、この目的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="65bb7-155">したがって、ER 構成に追加または編集する前に、**電子申告** ワークスペースの ER 構成プロバイダーを有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="65bb7-156">ER 構成の所有者のみが編集できます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="65bb7-157">したがって、ER 構成を編集する前に、適切な ER 構成 プロバイダーは **電子申告** ワークスペースで有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a> <span data-ttu-id="65bb7-158">ER コンフィギュレーション プロバイダーの一覧をレビュー</span><span class="sxs-lookup"><span data-stu-id="65bb7-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="65bb7-159">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65bb7-160">**ローカライズ構成** ページの、**関連リンク** セクションで、**構成プロバイダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="65bb7-161">**構成プロバイダー テーブル** ページでは、各プロバイダー レコードの名前と URL が一意になります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="65bb7-162">このページの内容をレビューします。</span><span class="sxs-lookup"><span data-stu-id="65bb7-162">Review the contents of this page.</span></span> <span data-ttu-id="65bb7-163">**Litware, Inc.** (`https://www.litware.com`) のレコードが既に存在する場合は、次の手順をスキップし、[新しい ER コンフィギュレーション プロバイダーを追加](#ActivateProvider) します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a> <span data-ttu-id="65bb7-164">新しい ER コンフィギュレーション プロバイダーを追加</span><span class="sxs-lookup"><span data-stu-id="65bb7-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="65bb7-165">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65bb7-166">**ローカライズ構成** ページの、**関連リンク** セクションで、**構成プロバイダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="65bb7-167">**構成プロバイダー** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="65bb7-168">**名前** フィールドに、**Litware, Inc.** と入力</span><span class="sxs-lookup"><span data-stu-id="65bb7-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="65bb7-169">**インターネット アドレス** フィールドで、`https://www.litware.com` を入力します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="65bb7-170">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a> <span data-ttu-id="65bb7-171">ER コンフィギュレーション プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="65bb7-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="65bb7-172">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65bb7-173">**ローカライズ構成** ページの **構成プロバイダー** セクションで、**Litware, Inc.** を選び、**有効に設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="65bb7-174">ER コンフィギュレーション プロバイダーについては、[コンフィギュレーション プロバイダーを作成し有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65bb7-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a> <span data-ttu-id="65bb7-175">標準 ER 形式コンフィギュレーションをインポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a> <span data-ttu-id="65bb7-176">標準 ER コンフィギュレーションをインポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-176">Import the standard ER configurations</span></span>

<span data-ttu-id="65bb7-177">標準 ER コンフィギュレーションを現在の Microsoft Dynamics 365 Finance のインスタンスに追加するには、インスタンスにコンフィギュレーションされた ER [リポジトリ](general-electronic-reporting.md#Repository) からインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="65bb7-178">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65bb7-179">**ローカライズ コンフィグレーション** ページの **コンフィギュレーション プロバイダー** セクションで、**Microsoft** タイルを選択し、**リポジトリ** を選択して Microsoft プロバイダーのリポジトリの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="65bb7-180">**コンフィギュレーション リポジトリ** ページで、**グローバル** タイプのリポジトリを選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="65bb7-181">Regulatory Configuration Service に接続するために承認を求める場合は、その承認の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="65bb7-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="65bb7-182">**コンフィギュレーション リポジトリ** ページにて、ウィンドウの左側のコンフィギュレーション ツリーで、**BACS (英国)** 形式コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="65bb7-183">**バージョン** クイック タブで、選択した ER 形式コンフィギュレーションのバージョン **1.1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="65bb7-184">**インポート** を選択して、グローバル リポジトリから現在の Finance インスタンスに選択したバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="65bb7-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![レポジトリ ページのコンフィギュレーション](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="65bb7-186">[グローバル リポジトリ](er-download-configurations-global-repo.md) へのアクセスに問題がある場合は、Microsoft Dynamics Lifecycle Services (LCS) から[コンフィギュレーションをダウンロード](download-electronic-reporting-configuration-lcs.md) ができます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a> <span data-ttu-id="65bb7-187">インポートされた ER コンフィギュレーションのレビュー</span><span class="sxs-lookup"><span data-stu-id="65bb7-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="65bb7-188">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65bb7-189">**ローカライズ構成** ページの、**構成** セクションで、**レポート構成** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="65bb7-190">**コンフィギュレーション** ページでウィンドウの左側のコンフィギュレーション ツリーで、**支払モデル** を展開します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="65bb7-191">選択した **BACS (英国)** ER 形式に加えて、その他の必要な ER コンフィギュレーションがインポートされたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="65bb7-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="65bb7-192">コンフィギュレーションツリーで、次の ER コンフィギュレーションが使用可能であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="65bb7-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="65bb7-193">**支払モデル** – このコンフィギュレーションには、支払業務ドメインのデータ構造を表す[データ モデル](general-electronic-reporting.md#data-model-and-model-mapping-components) ER コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="65bb7-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="65bb7-194">**支払モデルのマッピング 1611** – このコンフィギュレーションには、実行時にデータ モデルがアプリケーション データが格納される方法を記述する[モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components) ER コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="65bb7-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="65bb7-195">**BACS (英国)** – このコンフィギュレーションには、[形式](general-electronic-reporting.md#FormatComponentOutbound) と形式マッピング ER コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="65bb7-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="65bb7-196">形式コンポーネントは、レポートのレイアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-196">The format component specifies the report layout.</span></span> <span data-ttu-id="65bb7-197">形式マッピング コンポーネントには、モデル データソースが含まれており、実行時にこのデータソースを使用することによってレポートのレイアウトがどのように入力されるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![構成ページ](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a> <span data-ttu-id="65bb7-199">処理用仕入先支払の準備</span><span class="sxs-lookup"><span data-stu-id="65bb7-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a> <span data-ttu-id="65bb7-200">仕入先アカウントの銀行情報の追加</span><span class="sxs-lookup"><span data-stu-id="65bb7-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="65bb7-201">後に参照される仕入先アカウントの銀行情報を、登録済の支払に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="65bb7-202">**買掛金勘定** \> **仕入先** \> **すべての仕入先** に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="65bb7-203">**すべての仕入先** ページで、**GB_SI_000001** 仕入先アカウントを選択し、アクション ウィンドウの **仕入先** タブの **設定** グループで、**銀行アカウント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="65bb7-204">**仕入先の銀行アカウント** ページで、**新規** を選択して、次の情報を入力します:</span><span class="sxs-lookup"><span data-stu-id="65bb7-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="65bb7-205">**銀行アカウント** フィールドで、 **GBP OPER** を入力します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="65bb7-206">**銀行グループ** フィールドで、**BankGBP** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="65bb7-207">**銀行アカウント番号** フィールドで、**202015** を入力します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="65bb7-208">**SWIFT コード** フィールドで、<a id="DefineSWIFTCode"></a>**CHASDEFXXXX** を入力します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="65bb7-209">**IBAN** フィールドで、**GB33BUKB20201555555555** を入力します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="65bb7-210">**支店コード** フィールドで、既定値 <a id="DefineRoutingNumber"></a>**123456** をそのまま使用します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![仕入先の銀行アカウント ページ](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="65bb7-212">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-212">Select **Save**.</span></span>
5. <span data-ttu-id="65bb7-213">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-213">Close the page.</span></span>
6. <span data-ttu-id="65bb7-214">**すべての仕入先** ページで、**GB_SI_000001** 仕入先アカウントを開きます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="65bb7-215">必要に応じて、仕入先の詳細ページで、**編集** を選びページの編集が可能です。</span><span class="sxs-lookup"><span data-stu-id="65bb7-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="65bb7-216">**支払い** クイックタブの **銀行アカウント** フィールドで、**GBP OPER** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![仕入先の詳細ページ](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="65bb7-218">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-218">Select **Save**.</span></span>
10. <span data-ttu-id="65bb7-219">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a> <span data-ttu-id="65bb7-220">仕入先支払の入力</span><span class="sxs-lookup"><span data-stu-id="65bb7-220">Enter a vendor payment</span></span>

<span data-ttu-id="65bb7-221">[支払提案](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal) を使用して、新しい仕入先の支払いを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="65bb7-222">**買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="65bb7-223">**仕入先支払仕訳帳** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="65bb7-224">**名前** フィールドで、**VendPay** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="65bb7-225">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-225">Select **Lines**.</span></span>
5. <span data-ttu-id="65bb7-226">**支払提案** \> **支払提案の作成** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="65bb7-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="65bb7-227">**仕入先支払提案** ダイアログボックスで、**GB_SI_000001** 仕入先アカウントのみのレコードをフィルター処理するための条件をコンフィギュレーションし、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="65bb7-228">**00000007_Inv** 請求書の明細行を選び、**支払作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![仕入先支払提案のダイアログ ボックス](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="65bb7-230">入力された支払いが、**電子** 支払方法を使用するようにコンフィギュレーションされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![仕入先支払のページ](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a> <span data-ttu-id="65bb7-232">標準 ER 形式を使用した仕入先支払の処理</span><span class="sxs-lookup"><span data-stu-id="65bb7-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a> <span data-ttu-id="65bb7-233">電子支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="65bb7-233">Set up the electronic payment method</span></span>

<span data-ttu-id="65bb7-234">インポートされた ER 形式のコンフィギュレーションを使用するには、電子支払方法をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="65bb7-235">**買掛金勘定** \> **支払設定** \> **支払方法** に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="65bb7-236">**支払方法 - 仕入先** ページで、ウィンドウの左側の **電子** 支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="65bb7-237">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-237">Select **Edit**.</span></span>
4. <span data-ttu-id="65bb7-238">**ファイル形式** のクイックタブで、**一般的なエクスポート形式** のオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="65bb7-239">**形式の構成のエクスポート** フィールドで、**BACS (英国)** 形式コンフィグレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![支払方法 - 仕入先ページ](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="65bb7-241">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a> <span data-ttu-id="65bb7-242">仕入先支払のプロセス</span><span class="sxs-lookup"><span data-stu-id="65bb7-242">Process a vendor payment</span></span>

1. <span data-ttu-id="65bb7-243">**買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="65bb7-244">**仕入先支払仕訳帳** ページで、以前作成した支払仕訳帳を選択し、**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="65bb7-245">**仕入先支払** ページで、**支払生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="65bb7-246">**支払生成** ダイアログ ボックスで、次の情報を入力してください:</span><span class="sxs-lookup"><span data-stu-id="65bb7-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="65bb7-247">**支払方法** フィールドで、**電子** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="65bb7-248">**銀行口座** フィールドで、 **GBSI OPER** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="65bb7-249">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-249">Select **OK**.</span></span>
6. <span data-ttu-id="65bb7-250">**電子申告パラメータ** ダイアログ ボックスで、**印刷の管理レポート** オプションを **はい** に選定して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![電子申告パラメーター ダイアログ ボックスのページ](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="65bb7-252">支払ファイルに加えて、管理レポートを生成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="65bb7-253">Zip ファイルをダウンロードしてから、次のファイルをそこから抽出します:</span><span class="sxs-lookup"><span data-stu-id="65bb7-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="65bb7-254">Excel 形式の管理レポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-254">The control report in Excel format</span></span>
    - <span data-ttu-id="65bb7-255">TXT 形式の支払ファイル</span><span class="sxs-lookup"><span data-stu-id="65bb7-255">The payment file in TXT format</span></span>

        <span data-ttu-id="65bb7-256">提供された ER 形式の[構造](#PositionRoutingNumber) に従って、生成されたファイルの支払明細行は、コンフィギュレーションされた銀行アカウントの[定義済み](#DefineRoutingNumber) 支店コードで開始してください。</span><span class="sxs-lookup"><span data-stu-id="65bb7-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![TXT 形式の支払ファイル](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a> <span data-ttu-id="65bb7-258">標準 ER 形式のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="65bb7-258">Customize the standard ER format</span></span>

<span data-ttu-id="65bb7-259">このセクションに表示されている例では、Microsoft が提供する ER コンフィギュレーションを使用して仕入先支払ファイルを BACS 形式で生成しますが、特定の銀行の要求をサポートするには、カスタマイズを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="65bb7-260">また、ER コンフィギュレーションの新しいバージョンが使用可能になったときにカスタム形式をアップグレードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="65bb7-261">ただし、最小限のコストでアップグレードを実行できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="65bb7-262">この場合、Litware, Inc. の担当者として、**BACS (英国)** Microsoft から提供されているコンフィギュレーションを基準として使用して、新しい ER 形式のコンフィギュレーションを作成 (派生) する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a> <span data-ttu-id="65bb7-263">カスタム形式の作成</span><span class="sxs-lookup"><span data-stu-id="65bb7-263">Create a custom format</span></span>

1. <span data-ttu-id="65bb7-264">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="65bb7-265">**コンフィギュレーション** ページでウィンドウの左側のコンフィギュレーション ツリーで、**支払モデル** を展開、**BACS (英国)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="65bb7-266">Litware, Inc. は、この ER 形式コンフィギュレーションのバージョン 1.1 をカスタム バージョンのベースとして使用します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="65bb7-267">**コンフィギュレーションの作成** を選択して、ドロップ ダウンのダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="65bb7-268">このダイアログ ボックスを使用して、カスタムの支払形式の新しいコンフィギュレーションを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="65bb7-269">**新しい** フィールド グループで、**派生元の名前: BACS (英国)、Microsoft** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="65bb7-270">**名前** フィールドに、**BACS (英国カスタム)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![構成の作成ドロップダウン ダイアログボックス](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="65bb7-272">**コンフィギュレーションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-272">Select **Create configuration**.</span></span>

<span data-ttu-id="65bb7-273">**BACS (英国カスタム)** ER 形式コンフィギュレーションのバージョン 1.1.1 が作成されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="65bb7-274">このバージョンは **ドラフト** の[状態](general-electronic-reporting.md#component-versioning) で、編集することができます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="65bb7-275">カスタム ER 形式の現在の内容は、Microsoft が提供する形式の内容と一致しています。</span><span class="sxs-lookup"><span data-stu-id="65bb7-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![構成ページ](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a> <span data-ttu-id="65bb7-277">カスタム形式の編集</span><span class="sxs-lookup"><span data-stu-id="65bb7-277">Edit a custom format</span></span>

<span data-ttu-id="65bb7-278">銀行固有の要件を満たすには、カスタム形式をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="65bb7-279">たとえば、銀行は生成される支払ファイルに、処理済の仕入先支払にてエージェント ロールが割り当てられている銀行のワールドワイド インターバンク ファイナンシャル テレコミュニケーション (SWIFT) コードを含めることを要求する場合があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="65bb7-280">SWIFT コードは、世界中の特定の銀行を識別する国際銀行コードです。</span><span class="sxs-lookup"><span data-stu-id="65bb7-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="65bb7-281">銀行識別子コード (BICs) とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="65bb7-282">SWIFT コードは半角 11 文字で入力する必要があり、生成された支払ファイルの各支払明細行の先頭に入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="65bb7-283">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="65bb7-284">**コンフィギュレーション** ページでウィンドウの左側のコンフィギュレーション ツリーで、**支払モデル** を展開、**BACS (英国カスタム)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="65bb7-285">**バージョン** クイック タブで、選択したコンフィギュレーションのバージョン **1.1.1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="65bb7-286">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65bb7-286">Select **Designer**.</span></span>
5. <span data-ttu-id="65bb7-287">**形式デザイナー** ページで、**詳細表示** を選択して形式要素の詳細情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="65bb7-288">次の要素を展開し、確認します:</span><span class="sxs-lookup"><span data-stu-id="65bb7-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="65bb7-289">**フォルダー** タイプの **BACSReportsFolder** 要素。</span><span class="sxs-lookup"><span data-stu-id="65bb7-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="65bb7-290">この要素は、ZIP 形式で出力を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="65bb7-291">**ファイル** タイプの **ファイル** 要素。</span><span class="sxs-lookup"><span data-stu-id="65bb7-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="65bb7-292">この要素は、TXT 形式で支払ファイルを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="65bb7-293">**シーケンス** タイプの **取引** 要素。</span><span class="sxs-lookup"><span data-stu-id="65bb7-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="65bb7-294">この要素は、支払ファイルで単一の支払明細行を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="65bb7-295">**シーケンス** タイプの **取引** 要素。</span><span class="sxs-lookup"><span data-stu-id="65bb7-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="65bb7-296">この要素は、単一支払明細行の個々のフィールドを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="65bb7-297">**トランザクション** 要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-297">Select the **transaction** element.</span></span>

    ![ER 操作デザイナーのトランザクション要素](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="65bb7-299"><a id="PositionRoutingNumber"></a> すべての支払明細行が銀行支店コードで開始するには、指定されたレポートはコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="65bb7-300">**VendBankRouteNum** 形式の要素は、この目的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="65bb7-301">**追加** をクリックし、追加する形式要素の **テキスト\\文字列** を選択します:</span><span class="sxs-lookup"><span data-stu-id="65bb7-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="65bb7-302">**名前** フィールドに、**vendBankSWIFT** と入力します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="65bb7-303">**最小の長さ** フィールドに **11** を入力します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="65bb7-304">**最大の長さ** フィールドに **11** を入力します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="65bb7-305">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="65bb7-306">**VendBankSWIFT** 要素は、生成されたファイルに仕入先銀行の SWIFT コードを入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="65bb7-307">形式構造ツリーで、**vendBankSWIFT** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="65bb7-308">**上へ移動** を選択して、選択した形式要素がレベル 1 上に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="65bb7-309">**vendBankSWIFT** 要素が、親 **取引** 要素下の <a id="PositionSWIFTCode"></a> 最初の要素になるまで、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![ER 操作デザイナーのトランザクション下の最初の要素なる VendBankSWIFT](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="65bb7-311">**vendBankSWIFT** がまだ形式構造ツリーで選択されている状態で、**マッピング** タブを選択し、**モデル** データ ソースを展開します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="65bb7-312">**model.Payment** \> **model.Payment.CreditorAgent** を展開し、**model.Payment.CreditorAgent.BICFI** データ ソース フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="65bb7-313">このデータ ソースのフィールドでは、処理済の仕入先支払で、エージェント ロールが割り当てられている仕入先銀行の SWIFT コードが公開されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="65bb7-314">**バインド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-314">Select **Bind**.</span></span> <span data-ttu-id="65bb7-315">**vendBankSWIFT** 形式要素は、SWIFT コードが生成された支払いファイルに入力されるように、**model.Payment.CreditorAgent BICFI** データ ソース フィールドにバインドされるようになります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![ER 操作デザイナーで model.Payment.CreditorAgent.BICFI データ ソース フィールドにバインドされた vendBankSWIFT 形式要素](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="65bb7-317">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-317">Select **Save**.</span></span>
15. <span data-ttu-id="65bb7-318">デザイナー ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a> <span data-ttu-id="65bb7-319">カスタム形式を実行可能としてマーク</span><span class="sxs-lookup"><span data-stu-id="65bb7-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="65bb7-320">これで、カスタム書式の最初のバージョンが作成され、ステータスが **ドラフト** になり、テストを目的として実行できます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="65bb7-321">レポートを実行するには、カスタム ER 形式を参照する支払方法を使用して、仕入先支払を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="65bb7-322">既定では、申請から ER 形式を呼び出すとき、**完了済** または **共有** のステータスを持つバージョンのみが[考慮](general-electronic-reporting.md#component-versioning) されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="65bb7-323">この動作により、未完成の設計を持つ ER 形式が使用されるのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="65bb7-324">ただし、テストの実行には、**ドラフト** のステータスを持つ ER 形式のバージョンをアプリケーションに強制的に使用させることができます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="65bb7-325">これにより、変更が必要な場合は、現在の形式バージョンを調整できます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="65bb7-326">詳細については、[適合性](electronic-reporting-destinations.md#applicability) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65bb7-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="65bb7-327">ER 形式のドラフト バージョンを使用するには、ER 形式を明示的にマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="65bb7-328">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="65bb7-329">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="65bb7-330">**ユーザー パラメーター** ダイアログ ボックスで、**実行設定** オプションを **はい** に設定し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="65bb7-331">**編集** を選択し、必要に応じて現在のページを編集可能にします。</span><span class="sxs-lookup"><span data-stu-id="65bb7-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="65bb7-332">ウィンドウの左側にあるコンフィグレーション ツリーで、**BACS (英国カスタム)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="65bb7-333">**ドラフトの実行** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![コンフィギュレーション ページのドラフト実行オプション](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a> <span data-ttu-id="65bb7-335">カスタム ER 形式を使用した仕入先支払の処理</span><span class="sxs-lookup"><span data-stu-id="65bb7-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a> <span data-ttu-id="65bb7-336">電子支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="65bb7-336">Set up the electronic payment method</span></span>

<span data-ttu-id="65bb7-337">カスタム ER 形式を使用して仕入先支払を処理するには、電子支払方法をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="65bb7-338">**買掛金勘定** \> **支払設定** \> **支払方法** に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="65bb7-339">**支払方法 - 仕入先** ページで、ウィンドウの左側の **電子** 支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="65bb7-340">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-340">Select **Edit**.</span></span>
4. <span data-ttu-id="65bb7-341">**ファイル形式** クイック タブで、**一般的な電子エクスポート形式** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="65bb7-342">**形式の構成のエクスポート** フィールドで、**BACS (英国カスタム)** 形式コンフィグレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![支払方法 - 仕入先ページ](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="65bb7-344">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a> <span data-ttu-id="65bb7-345">仕入先支払のプロセス</span><span class="sxs-lookup"><span data-stu-id="65bb7-345">Process a vendor payment</span></span>

1. <span data-ttu-id="65bb7-346">**買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="65bb7-347">**仕入先支払仕訳帳** ページで、以前作成した支払仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="65bb7-348">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-348">Select **Lines**.</span></span>
4. <span data-ttu-id="65bb7-349">**仕入先支払** ページのグリッドの上で、**支払ステータス** \> **なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="65bb7-350">**支払の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="65bb7-351">**支払生成** ダイアログ ボックスで、次の情報を入力してください:</span><span class="sxs-lookup"><span data-stu-id="65bb7-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="65bb7-352">**支払方法** フィールドで、**電子** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="65bb7-353">**銀行口座** フィールドで、 **GBSI OPER** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="65bb7-354">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-354">Select **OK**.</span></span>
8. <span data-ttu-id="65bb7-355">**電子申告パラメータ** ダイアログ ボックスで、**印刷の管理レポート** オプションを **はい** に選定して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="65bb7-356">支払ファイルに加えて、管理レポートのみ生成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="65bb7-357">Zip ファイルをダウンロードしてから、次のファイルをそこから抽出します:</span><span class="sxs-lookup"><span data-stu-id="65bb7-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="65bb7-358">Excel 形式の管理レポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-358">The control report in Excel format</span></span>
    - <span data-ttu-id="65bb7-359">TXT 形式の支払ファイル</span><span class="sxs-lookup"><span data-stu-id="65bb7-359">The payment file in TXT format</span></span>

        <span data-ttu-id="65bb7-360">カスタム ER 形式の構造に従って、生成されたファイルの支払明細行は、支払が処理された仕入先の銀行アカウントに対して[入力](#DefineSWIFTCode) された SWIFT コードで[開始](#PositionSWIFTCode) されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="65bb7-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![TXT 形式の支払ファイル](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a> <span data-ttu-id="65bb7-362">標準 ER 形式コンフィギュレーションの新バージョンをインポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="65bb7-363">このセクションに表示されている例では、サポート技術情報の記事 [KB 3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046) に関する通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="65bb7-364">Microsoft が発行した **BACS (英国)** ER 形式の新バージョンについて通知されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="65bb7-365">この新バージョンでは、管理レポートに加えて、仕入先支払の処理中にユーザーが支払通知レポートと出席メモ レポートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="65bb7-366">この機能の使用を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a> <span data-ttu-id="65bb7-367">標準 ER コンフィギュレーションの新バージョンをインポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="65bb7-368">ER コンフィギュレーションの新バージョンを現在の Finance インスタンスに追加するには、コンフィギュレーションした ER [リポジトリ](general-electronic-reporting.md#Repository) からインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="65bb7-369">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65bb7-370">**ローカライズ コンフィグレーション** ページの **コンフィギュレーション プロバイダー** セクションで、**Microsoft** タイルを選択し、**リポジトリ** を選択して Microsoft プロバイダーのリポジトリの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="65bb7-371">**コンフィギュレーション リポジトリ** ページで、**グローバル** タイプのリポジトリを選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="65bb7-372">Regulatory Configuration Service に接続するために承認を求める場合は、その承認の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="65bb7-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="65bb7-373">**コンフィギュレーション リポジトリ** ページにて、ウィンドウの左側のコンフィギュレーション ツリーで、**BACS (英国)** 形式コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="65bb7-374">**バージョン** クイック タブで、選択した ER 形式コンフィギュレーションのバージョン **3.3** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="65bb7-375">**インポート** を選択して、グローバル リポジトリから現在の Finance インスタンスに選択したバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="65bb7-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![レポジトリ ページのコンフィギュレーション](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="65bb7-377">[グローバル化 リポジトリ](er-download-configurations-global-repo.md) のアクセスに問題がある場合は、代わりに LCS から[コンフィグレーションをダウンロード](download-electronic-reporting-configuration-lcs.md) できます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a> <span data-ttu-id="65bb7-378">インポートされた ER 形式コンフィギュレーションのレビュー</span><span class="sxs-lookup"><span data-stu-id="65bb7-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="65bb7-379">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65bb7-380">**ローカライズ構成** ページの、**構成** セクションで、**レポート構成** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="65bb7-381">**コンフィギュレーション** ページでウィンドウの左側のコンフィギュレーション ツリーで、**支払モデル** を展開、**BACS (英国)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="65bb7-382">**バージョン** FastTab で、バージョン **3.3** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="65bb7-383">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65bb7-383">Select **Designer**.</span></span>
6. <span data-ttu-id="65bb7-384">**形式デザイナー** ページで、**BACSReportsFolder** 形式要素を展開できます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="65bb7-385">バージョン 3.3 には、仕入先支払の処理時に、支払通知レポートを生成するために使用される **PaymentAdviceReport** 形式要素が含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="65bb7-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![ER 操作デザイナーの PaymentAdviceReport 形式要素](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="65bb7-387">デザイナー ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a> <span data-ttu-id="65bb7-388">インポートされた形式の新バージョンの変更をカスタム形式で採用</span><span class="sxs-lookup"><span data-stu-id="65bb7-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a> <span data-ttu-id="65bb7-389">カスタム形式の現在のドラフト バージョンを完了</span><span class="sxs-lookup"><span data-stu-id="65bb7-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="65bb7-390">カスタム形式の現在のステータスを保持する場合は、そのステータスを **ドラフト** から **完了済** に変更して、ドラフト バージョン 1.1.1 を完了します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="65bb7-391">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65bb7-392">**ローカライズ構成** ページの、**構成** セクションで、**レポート構成** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="65bb7-393">**コンフィギュレーション** ページのウィンドウ左側のコンフィギュレーション ツリーで、**支払モデル** から **BACS (英国)** を展開して、**BACS (英国カスタム)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="65bb7-394">**バージョン** クイックタブで、**ステータスの変更** \> **完了済**、そして **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="65bb7-395">バージョン 1.1.1 のステータスは、**ドラフト** から **完了済** に変更され、バージョンは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="65bb7-396">新しい編集可能バージョンの 1.1.2 が追加され、ステータスが **ドラフト** になりました。</span><span class="sxs-lookup"><span data-stu-id="65bb7-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="65bb7-397">このバージョンを使用すると、カスタム ER 形式でさらに変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a> <span data-ttu-id="65bb7-398">カスタム形式を新しい基本バージョンにリベース</span><span class="sxs-lookup"><span data-stu-id="65bb7-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="65bb7-399">カスタマイズの **BACS (英国)** 形式によるバージョン 3.3 の新機能を使用するには、カスタム コンフィギュレーション **BACS (英国カスタム)** の基本コンフィギュレーション バージョンを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="65bb7-400">このプロセスは、[再ベース中](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase)と呼ばれています。</span><span class="sxs-lookup"><span data-stu-id="65bb7-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="65bb7-401">**BACS (英国)** のバージョン 1.1 の代わりに、バージョン 3.3 を使用します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="65bb7-402">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="65bb7-403">**コンフィギュレーション** ページでウィンドウの左側のコンフィギュレーション ツリーで、**支払モデル** を展開、**BACS (英国カスタム)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="65bb7-404">**バージョン** クイックタブで、バージョン **1.1.2** を選び、**リベース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="65bb7-405">**リベース** ダイアログ ボックスの **ターゲット バージョン** フィールドで、基準コンフィグレーションのバージョン **3.3** を選択し、新しい基準として適用およびコンフィグレーションを更新するために使用します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![ダイアログ ボックスのリベース](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="65bb7-407">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-407">Select **OK**.</span></span>
6. <span data-ttu-id="65bb7-408">ドラフト バージョンの番号は **1.1.2** から **3.3.2** に変更され、その変更は基本バージョンに反映されます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="65bb7-409">カスタム バージョンと基本バージョンがマージされると、自動的にマージされない形式変更のため、いくつかの矛盾が発見される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![コンフィグレーション ページで競合のあるリベース コンフィギュレーション](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="65bb7-411">競合が検出された場合は、形式デザイナーで手動で解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="65bb7-412">**バージョン** FastTab で、バージョン **3.3.2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="65bb7-413">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65bb7-413">Select **Designer**.</span></span>
9. <span data-ttu-id="65bb7-414">**形式デザイナー** ページの **詳細** クイックタブで、リベースの競合レコードを選び、**基準値の適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![ER 操作デザイナーのリベース競合レコード](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="65bb7-416">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-416">Select **Save**.</span></span>

    <span data-ttu-id="65bb7-417">リベースの競合レコードは、**詳細** クイックタブに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![ER 操作デザイナーで解決される競合](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="65bb7-419">基準モデルのバージョン 3 を、この ER 形式で使用する必要があることを確認して、競合を解決しました。</span><span class="sxs-lookup"><span data-stu-id="65bb7-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="65bb7-420">**BACSReportsFolder** \> **ファイル** \> **トランザクション** \> **トランザクション** を展開します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="65bb7-421">**マッピング** タブで、カスタム ER 形式のバージョン 3.3.2 は、使用しているカスタマイズ (**vendBankSWIFT** 形式要素とそのバインド) と Microsoft が提供する基準 ER 形式のバージョン 3.3 の新しい機能の両方 (入れ子になった要素とコンフィグレーションされたバインド と共にある **PaymentAdviceReport**) を含みます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="65bb7-422">新しい基準バージョンをカスタマイズして適用した場合は、マウスを数回クリックするだけで変更を適用することができます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![ER 操作デザイナーでの結合形式](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="65bb7-424">デザイナー ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="65bb7-425">リベース アクションを元に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="65bb7-425">The rebase action is reversible.</span></span> <span data-ttu-id="65bb7-426">このリベースをキャンセルするには、**バージョン** クイックタブで **BACS (英国カスタム)** 形式のバージョン **1.1.1** を選び、**このバージョンを取得** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="65bb7-427">バージョン 3.3.2 は、1.1.2 の番号が振り直され、ドラフト バージョン 1.1.2 の内容とバージョン 1.1.1 のコンテンツが一致するようになります。</span><span class="sxs-lookup"><span data-stu-id="65bb7-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a> <span data-ttu-id="65bb7-428">リベース ER 形式を使用した仕入先支払の処理</span><span class="sxs-lookup"><span data-stu-id="65bb7-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="65bb7-429">**買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="65bb7-430">**仕入先支払仕訳帳** ページで、以前作成した支払仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="65bb7-431">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-431">Select **Lines**.</span></span>
4. <span data-ttu-id="65bb7-432">**仕入先支払** ページのグリッドの上で、**支払ステータス** \> **なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="65bb7-433">**支払の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="65bb7-434">**支払生成** ダイアログ ボックスで、次の情報を入力してください:</span><span class="sxs-lookup"><span data-stu-id="65bb7-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="65bb7-435">**支払方法** フィールドで、**電子** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="65bb7-436">**銀行口座** フィールドで、 **GBSI OPER** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="65bb7-437">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-437">Select **OK**.</span></span>
8. <span data-ttu-id="65bb7-438">**電子申告パラメータ** ダイアログ ボックスで、次の情報を入力してください:</span><span class="sxs-lookup"><span data-stu-id="65bb7-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="65bb7-439">**管理レポートの印刷** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="65bb7-440">**支払通知の印刷** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![電子申告パラメーター ダイアログ ボックス](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="65bb7-442">支払ファイルに加えて、制御レポートと支払通知レポートの両方を生成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="65bb7-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="65bb7-443">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65bb7-443">Select **OK**.</span></span>
10. <span data-ttu-id="65bb7-444">Zip ファイルをダウンロードしてから、次のファイルをそこから抽出します:</span><span class="sxs-lookup"><span data-stu-id="65bb7-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="65bb7-445">Excel 形式の管理レポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-445">The control report in Excel format</span></span>
    - <span data-ttu-id="65bb7-446">Excel 形式の支払通知レポート</span><span class="sxs-lookup"><span data-stu-id="65bb7-446">The payment advice report in Excel format</span></span>

        ![Excel 形式の支払通知レポート](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="65bb7-448">TXT 形式の支払ファイル</span><span class="sxs-lookup"><span data-stu-id="65bb7-448">The payment file in TXT format</span></span>

        <span data-ttu-id="65bb7-449">生成されたファイルの支払明細行は、支払が処理された仕入先の銀行アカウントに対して入力 された SWIFT コードで開始 されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="65bb7-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![TXT 形式の支払ファイル](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="65bb7-451">追加リソース</span><span class="sxs-lookup"><span data-stu-id="65bb7-451">Additional resources</span></span>

- [<span data-ttu-id="65bb7-452">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="65bb7-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="65bb7-453">ER コンフィギュレーションを Lifecycle Services からダウンロードする</span><span class="sxs-lookup"><span data-stu-id="65bb7-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="65bb7-454">ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする</span><span class="sxs-lookup"><span data-stu-id="65bb7-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)

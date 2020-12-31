---
title: 電子レポートのカスタマイズを構成して電子ドキュメントを生成する
description: このトピックでは、Microsoft が提供する電子レポート (ER) の構成をカスタマイズして、カスタム電子ドキュメントを生成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: 47bb8a2a9adab4ec963a1d0b95e783299aab3819
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683019"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a><span data-ttu-id="7f062-103">電子レポートのカスタマイズを構成して電子ドキュメントを生成する</span><span class="sxs-lookup"><span data-stu-id="7f062-103">Customize Electronic reporting configurations to generate an electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7f062-104">[電子レポート (ER) フレームワーク](general-electronic-reporting.md)を使用すると 、が Microsoft Dynamics 365 Finance のインスタンスで提供している ER の[構成](general-electronic-reporting.md#Configuration)をアップロードでき ます。</span><span class="sxs-lookup"><span data-stu-id="7f062-104">The [Electronic reporting (ER) framework](general-electronic-reporting.md) lets you upload the ER [configurations](general-electronic-reporting.md#Configuration) that Microsoft provides into your Microsoft Dynamics 365 Finance instance.</span></span> <span data-ttu-id="7f062-105">このように、Microsoft が提供する構成は ER ソリューションとして機能し、電子顧客請求書 (電子インボイス) の生成に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-105">In this way, the Microsoft-provided configurations can serve as the ER solution that is used to generate electronic customer invoices (e-invoices).</span></span> <span data-ttu-id="7f062-106">この ER ソリューションを使用すると、ソースコードを編集することなく、カスタム データベースのフィールドにアクセスし、特定の要件に準拠した電子インボイスを生成するカスタム ER ソリューションを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-106">You can use this ER solution to configure your custom ER solution to access your custom database fields and generate e-invoices that are compliant with your specific requirements, without having to edit the source code.</span></span>

## <a name="overview"></a><span data-ttu-id="7f062-107">概要</span><span class="sxs-lookup"><span data-stu-id="7f062-107">Overview</span></span>

<span data-ttu-id="7f062-108">このトピックの例では、電子請求書を発行するすべての顧客の新しいカスタム属性として連邦税の ID コードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-108">For the example in this topic, you must specify a federal tax identification code as a new custom attribute of every customer that you electronically invoice.</span></span> <span data-ttu-id="7f062-109">そのため、現在使用している請求書の構造をカスタマイズするには、生成される電子請求書のすべてに対して税コードの記入を必須かした項目を新たに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-109">Therefore, you must customize the structure of the invoice that is currently used, by adding a new item that must be filled with the tax code in every e-invoice that is generated.</span></span>

<span data-ttu-id="7f062-110">このトピックの手順では、システム管理者、電子レポート開発者、電子レポート機能コンサルタントのロールを持つユーザーが財務インスタンスで以下のタスクを実行する方法について説明します :</span><span class="sxs-lookup"><span data-stu-id="7f062-110">The procedures in this topic explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can perform the following tasks in your Finance instance:</span></span>

- <span data-ttu-id="7f062-111">[ER フレームワークを使い始めるにあたって必要となる ER パラメーターの最小限のセットを構成する](#ConfigureER)。</span><span class="sxs-lookup"><span data-stu-id="7f062-111">[Configure the minimal set of ER parameters that is required to start to use the ER framework](#ConfigureER).</span></span>
- <span data-ttu-id="7f062-112">[電子インボイスの生成に向けて提供されている標準的な ER 構成の最初のバージョンをインポートする](#ImportERConfigurations1)。</span><span class="sxs-lookup"><span data-stu-id="7f062-112">[Import the initial versions of the standard ER configurations that are provided to generate e-invoices](#ImportERConfigurations1).</span></span>
- <span data-ttu-id="7f062-113">[売掛金勘定パラメーターを構成して、標準的な ER の構成を使用する](#ConfigureAR1)。</span><span class="sxs-lookup"><span data-stu-id="7f062-113">[Configure the Accounts receivable parameters to start to use the standard ER configurations](#ConfigureAR1).</span></span>
- <span data-ttu-id="7f062-114">[法人のパラメーターを構成して、顧客に請求書を発行する](#ConfigureLE)。</span><span class="sxs-lookup"><span data-stu-id="7f062-114">[Configure the legal entity parameters to invoice customers](#ConfigureLE).</span></span>
- <span data-ttu-id="7f062-115">[電子請求書で使用する顧客レコードを準備する](#ConfigureCustomer1)。</span><span class="sxs-lookup"><span data-stu-id="7f062-115">[Prepare a customer record for electronic invoicing](#ConfigureCustomer1).</span></span>
- <span data-ttu-id="7f062-116">[標準的な ER の構成を使用して、顧客請求書を追加、転記、送信する ](#ProcessInvoice1)。</span><span class="sxs-lookup"><span data-stu-id="7f062-116">[Add, post, and send a customer invoice by using the standard ER configurations](#ProcessInvoice1).</span></span>
- <span data-ttu-id="7f062-117">[カスタマイズしたデータベース フィールドを追加して、顧客の連邦税 ID コードを管理する](#AddCustomField)。</span><span class="sxs-lookup"><span data-stu-id="7f062-117">[Add a custom database field to manage a federal tax identification code for customers](#AddCustomField).</span></span>
- <span data-ttu-id="7f062-118">[ER のメタデータを更新して、ER モデル マッピング デザイナのデータベース変更を有効にする](#RefreshERMetadata)。</span><span class="sxs-lookup"><span data-stu-id="7f062-118">[Refresh the ER metadata to enable database changes for the ER model mapping designer](#RefreshERMetadata).</span></span>
- <span data-ttu-id="7f062-119">[カスタマイズした ER 構成を設計して、新しい税コードを含む電子インボイスを生成する](#DesignCustomERConfigurations)。</span><span class="sxs-lookup"><span data-stu-id="7f062-119">[Design the custom ER configurations to generate e-invoices that contain the new tax code](#DesignCustomERConfigurations).</span></span>
- <span data-ttu-id="7f062-120">[売掛金勘定パラメーターを構成して、カスタマイズした ER の構成を使用する](#ConfigureAR2)。</span><span class="sxs-lookup"><span data-stu-id="7f062-120">[Configure the Accounts receivable parameters to start to use the custom ER configurations](#ConfigureAR2).</span></span>
- <span data-ttu-id="7f062-121">[電子請求書で使用する顧客レコードを更新する](#ConfigureCustomer2)。</span><span class="sxs-lookup"><span data-stu-id="7f062-121">[Update a customer record for electronic invoicing](#ConfigureCustomer2).</span></span>
- <span data-ttu-id="7f062-122">[カスタマイズした ER の構成を使用して、顧客請求書を追加、転記、送信する ](#ProcessInvoice2)。</span><span class="sxs-lookup"><span data-stu-id="7f062-122">[Add, post, and send a customer invoice by using the custom ER configurations](#ProcessInvoice2).</span></span>
- <span data-ttu-id="7f062-123">[電子インボイスの生成に向けて提供されている標準的な ER 構成の新しいバージョンをインポートする](#ImportERConfigurations2)。</span><span class="sxs-lookup"><span data-stu-id="7f062-123">[Import the new versions of the standard ER configurations that are provided to generate e-invoices](#ImportERConfigurations2).</span></span>
- <span data-ttu-id="7f062-124">[カスタマイズした ER の構成に新しいバージョンの標準的な ER の構成に変更を適用する](#RebaseCustomERConfigurations)。</span><span class="sxs-lookup"><span data-stu-id="7f062-124">[Adopt the changes to the new versions of the standard ER configurations in your custom ER configurations](#RebaseCustomERConfigurations).</span></span>
- <span data-ttu-id="7f062-125">[新しいバージョンの ER の構成を使用して、顧客請求書を追加、転記、送信する ](#ProcessInvoice3)。</span><span class="sxs-lookup"><span data-stu-id="7f062-125">[Add, post, and send a customer invoice by using the new versions of the custom ER configurations](#ProcessInvoice3).</span></span>

<span data-ttu-id="7f062-126">**DEMF** 社を例に使用して、これらの手順について解説します。</span><span class="sxs-lookup"><span data-stu-id="7f062-126">All these procedures can be completed in the **DEMF** company.</span></span>

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a> <span data-ttu-id="7f062-127">ER フレームワークを構成する</span><span class="sxs-lookup"><span data-stu-id="7f062-127">Configure the ER framework</span></span>

<span data-ttu-id="7f062-128">電子レポート機能コンサルタントや電子レポート開発者ロールを持つユーザーは、ER パラメーターの最小限のセットを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-128">As a user in the Electronic Reporting Functional Consultant or Electronic Reporting Developer role, you must configure the minimal set of ER parameters.</span></span> <span data-ttu-id="7f062-129">この手順を完了した後は、ER フレームワークを使用して、電子インボイスの生成に使用する ER ソリューションの標準的な構成のカスタマイズ版を設計することができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-129">You can then start to use the ER framework to design custom versions of the standard configurations of the ER solution that is used to generate e-invoices.</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="7f062-130">ER パラメーターの構成</span><span class="sxs-lookup"><span data-stu-id="7f062-130">Configure ER parameters</span></span>

1. <span data-ttu-id="7f062-131">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-131">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7f062-132">**ローカライズ構成** ページの、**関連リンク** セクションで、**電子申告パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-132">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="7f062-133">**電子申告パラメーター** ページの、**一般** タブで、**デザイン モードの有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7f062-133">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="7f062-134">**添付** タブの **構成** フィールドで、**ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-134">On the **Attachments** tab, in the **Configurations** field, select **File**.</span></span>
5. <span data-ttu-id="7f062-135">**ジョブ アーカイブ**、**一時的**、**ベースライン**、および **その他** フィールドで、**ファイル** タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-135">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="7f062-136">ER パラメーターについては、[ER フレームワークのコンフィギュレーション](electronic-reporting-er-configure-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-136">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><span data-ttu-id="7f062-137"> ER 構成プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="7f062-137">Activate an ER configuration provider</span></span>

<span data-ttu-id="7f062-138">追加されたすべての ER 構成は、ER 構成プロバイダーによって所有されているものとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="7f062-138">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="7f062-139">**電子申告** ワークスペースで有効化された ER 構成プロバイダーは、この目的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f062-139">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="7f062-140">したがって、ER 構成に追加または編集する前に、**電子申告** ワークスペースの ER 構成プロバイダーを有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-140">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="7f062-141">ER 構成の所有者のみが編集できます。</span><span class="sxs-lookup"><span data-stu-id="7f062-141">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="7f062-142">したがって、ER 構成を編集する前に、適切な ER 構成 プロバイダーは **電子申告** ワークスペースで有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-142">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><span data-ttu-id="7f062-143"> ER 構成 プロバイダーの一覧をレビュー</span><span class="sxs-lookup"><span data-stu-id="7f062-143">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="7f062-144">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-144">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7f062-145">**ローカライズ構成** ページの、**関連リンク** セクションで、**構成プロバイダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-145">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="7f062-146">**構成プロバイダー テーブル** ページでは、各プロバイダー レコードの名前と URL が一意になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-146">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="7f062-147">このページの内容をレビューします。</span><span class="sxs-lookup"><span data-stu-id="7f062-147">Review the contents of this page.</span></span> <span data-ttu-id="7f062-148">**Litware, Inc.** (`https://www.litware.com`) のレコードが既に存在する場合は、次の手順をスキップし、[新しい ER 構成プロバイダーを追加](#AddProvider) します。</span><span class="sxs-lookup"><span data-stu-id="7f062-148">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#AddProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a> <span data-ttu-id="7f062-149">新しい ER 構成プロバイダーを追加</span><span class="sxs-lookup"><span data-stu-id="7f062-149">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="7f062-150">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-150">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7f062-151">**ローカライズ構成** ページの、**関連リンク** セクションで、**構成プロバイダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-151">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="7f062-152">**構成プロバイダー** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-152">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="7f062-153">**名前** フィールドに、**Litware, Inc.** と入力</span><span class="sxs-lookup"><span data-stu-id="7f062-153">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="7f062-154">**インターネット アドレス** フィールドで、`https://www.litware.com` を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-154">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="7f062-155">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-155">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><span data-ttu-id="7f062-156"> ER 構成 プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="7f062-156">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="7f062-157">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-157">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7f062-158">**ローカライズ構成** ページの **構成プロバイダー** セクションで、**Litware, Inc.** を選び、**有効に設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-158">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="7f062-159">ER 構成 プロバイダーについては、[構成 プロバイダーを作成し有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-159">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a><span data-ttu-id="7f062-160">標準的な ER 構成の初期バージョンをインポートする</span><span class="sxs-lookup"><span data-stu-id="7f062-160">Import the initial versions of standard ER configurations</span></span>

<span data-ttu-id="7f062-161">現在の財務インスタンスに標準的な ER の構成を追加するには、そのインスタンスに設定されている ER [リポジトリ](general-electronic-reporting.md#Repository)からインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-161">To add the standard ER configurations to your current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="7f062-162">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7f062-163">**ローカライズ コンフィグレーション** ページの **コンフィギュレーション プロバイダー** セクションで、**Microsoft** タイルを選択し、**リポジトリ** を選択して Microsoft プロバイダーのリポジトリの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="7f062-163">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="7f062-164">**コンフィギュレーション リポジトリ** ページで、**グローバル** タイプのリポジトリを選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-164">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="7f062-165">Regulatory Configuration Service に接続するために承認を求める場合は、その承認の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="7f062-165">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="7f062-166">**構成リポジトリ** ページにて、ウィンドウの左側の構成ツリーで、**Peppol 売上請求書** 形式の構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-166">On the **Configuration repository** page, in the configuration tree in the left pane, select the **Peppol Sales Invoice** format configuration.</span></span>
5. <span data-ttu-id="7f062-167">**バージョン** FastTab で、バージョン **11.2.2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-167">On the **Versions** FastTab, select version **11.2.2**.</span></span>
6. <span data-ttu-id="7f062-168">**インポート** を選択して、グローバル リポジトリから選択したバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7f062-168">Select **Import** to download the selected version from the Global repository.</span></span>

![レポジトリ ページの構成](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> <span data-ttu-id="7f062-170">[グローバル リポジトリ](er-download-configurations-global-repo.md) へのアクセスに問題がある場合は、Microsoft Dynamics Lifecycle Services (LCS) から[構成をダウンロード](download-electronic-reporting-configuration-lcs.md) ができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-170">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><span data-ttu-id="7f062-171"> インポートされた ER 構成のレビュー</span><span class="sxs-lookup"><span data-stu-id="7f062-171">Review the imported ER configurations</span></span>

1. <span data-ttu-id="7f062-172">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7f062-173">**ローカライズ構成** ページの、**構成** セクションで、**レポート構成** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-173">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="7f062-174">**構成** ページで、**構成コンポーネント** クイックタブを展開します。</span><span class="sxs-lookup"><span data-stu-id="7f062-174">On the **Configurations** page, expand the **Configuration components** FastTab.</span></span>
4. <span data-ttu-id="7f062-175">左ウィンドウの構成ツリーで、**請求書モデル** を展開し、 **UBL 売上請求書** を展開します。</span><span class="sxs-lookup"><span data-stu-id="7f062-175">In the configuration tree in the left pane, expand **Invoice model**, and then expand **UBL Sales invoice**.</span></span>

<span data-ttu-id="7f062-176">選択した **Peppol 売上請求書** ER 形式に加えて、その他の必要な ER の構成がインポートされたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-176">Notice that, in addition to the selected **Peppol Sales Invoice** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="7f062-177">新しいバージョンの ER の構成は、新しい要件に準拠するソリューションを維持するためにグローバル リポジトリと LCS に常に公開されているため、必要な [データ モデル](general-electronic-reporting.md#data-model-and-model-mapping-components)構成の最新バージョンとその [モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)の構成がインポートされます。</span><span class="sxs-lookup"><span data-stu-id="7f062-177">Because new versions of ER configurations are constantly published to the Global repository and LCS to keep the corresponding solutions compliant with new requirements, the latest versions of the required [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) configuration and its [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) configurations were imported.</span></span>

![構成ページ](./media/er-quick-start3-imported-solution1a.png)

<span data-ttu-id="7f062-179">過去に **Peppol 売上請求書** の ER 形式のバージョン **11.2.2** をインポートした場合 (例えば 2019 年 8 月 7 日) に、現在の財務インスタンスの ER 構成がどのような状態になるかをシミュレーションするには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7f062-179">To simulate the state that ER configurations in the current Finance instance  would be in if you imported version **11.2.2** of the **Peppol Sales Invoice** ER format in the past (for example, on August 7, 2019), follow these steps.</span></span>

- <span data-ttu-id="7f062-180">アクション ペインで、**削除** を選択して、2019 年 8 月 7 日より後に発行されたすべての ER 構成を削除します。</span><span class="sxs-lookup"><span data-stu-id="7f062-180">On the Action Pane, select **Delete** to delete all ER configurations that were published after August 7, 2019.</span></span> <span data-ttu-id="7f062-181">**請求書モデル**、**請求書モデルのマッピング** (初期状態の名称は **顧客請求書モデル マッピング** です)、**UBL の売上請求書** および **Peppol の売上請求書** の売上請求書の構成のみを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-181">The only **Invoice model**, **Invoice model mapping** (initially named **Customer invoice model mapping**), **UBL Sales invoice** and **Peppol Sales Invoice** configurations must be left.</span></span>
- <span data-ttu-id="7f062-182">変更されていない場合の構成については、**バージョン** クイックタブの **削除** を選択して、2019 年 8 月 7 日より後に発行されたすべてのバージョンの ER 構成を削除します。</span><span class="sxs-lookup"><span data-stu-id="7f062-182">For the remained ER configurations, on the **Versions** FastTab, select **Delete** to delete all versions of ER configurations that were published after August 7, 2019.</span></span>

<span data-ttu-id="7f062-183">構成ツリーで以下の構成が利用可能であることを確認してください :</span><span class="sxs-lookup"><span data-stu-id="7f062-183">Then verify that the following configurations are available in the configuration tree:</span></span>

- <span data-ttu-id="7f062-184">**請求書モデル** ER データモデルの構成 (初期状態の名称は **顧客請求書モデル** です) :</span><span class="sxs-lookup"><span data-stu-id="7f062-184">**Invoice model** ER data model configuration (initially named **Customer invoice model**):</span></span>

    - <span data-ttu-id="7f062-185">バージョン 11 には、請求書発行ビジネス ドメインのデータ構造を表す[データモデル](general-electronic-reporting.md#data-model-and-model-mapping-components) ER コンポーネントのバージョン 10 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f062-185">Version 11 contains version 10 of the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the invoicing business domain.</span></span> <span data-ttu-id="7f062-186">この ER 構成は、インポート対象として選択された **Peppol 売り上げ請求書** の ER 形式の原型としてインポートされました。</span><span class="sxs-lookup"><span data-stu-id="7f062-186">This ER configuration has been imported as an ancestor of the **Peppol Sales Invoice** ER format that was selected for import.</span></span>
    - <span data-ttu-id="7f062-187">バージョン 50 には、データモデル ER コンポーネントのバージョン31 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f062-187">Version 50 contains version 31 of the data model ER component.</span></span> <span data-ttu-id="7f062-188">この ER 構成は、2019 年 8 月 7 日版の **請求書モデル マッピング**  ER モデル マッピング構成の原型としてインポートされています。</span><span class="sxs-lookup"><span data-stu-id="7f062-188">This ER configuration has been imported as an ancestor of the August 7, 2019, version of the **Invoice model mapping** ER model mapping configuration.</span></span>

    ![構成ページの請求書 モデル ER データモデルの設定](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > <span data-ttu-id="7f062-190">このデータ モデルのバージョン 50 が表示されない場合は、グローバル リポジトリを開き、**請求書マッピング** ER 構成のバージョン 50.19 をインポートし ます。</span><span class="sxs-lookup"><span data-stu-id="7f062-190">If you don't see version 50 of this data model, open the Global repository, and import version 50.19 of the **Invoice model mapping** ER configuration.</span></span>

- <span data-ttu-id="7f062-191">**請求書モデル マッピング** ER モデル マッピングの構成 (初期状態の名称は **顧客請求書モデル マッピング** です) :</span><span class="sxs-lookup"><span data-stu-id="7f062-191">**Invoice model mapping** ER model mapping configuration (initially named **Customer invoice model mapping**):</span></span>

    - <span data-ttu-id="7f062-192">バージョン 50.19 は、**請求モデル** ER のデータモデル構成の最新の50バージョンでの実装としてインポートされました。</span><span class="sxs-lookup"><span data-stu-id="7f062-192">Version 50.19 has been imported as the latest implementation of version 50 of the **Invoice model** ER data model configuration.</span></span> <span data-ttu-id="7f062-193">これには、実行時にデータモデルがどのようにアプリケーションデータで格納されるかを記述した、 2 つの[モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)ERコンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f062-193">It contains two [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER components that describe how the data model is filled in with application data at runtime.</span></span>

    ![構成ページにおける請求書モデル マッピング ER モデル マッピングの設定](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > <span data-ttu-id="7f062-195">このモデル マッピングのバージョン 50.19 が表示されない場合は、グローバル リポジトリを開き、**請求書マッピング** ER 構成のバージョン 50.19 をインポートします。</span><span class="sxs-lookup"><span data-stu-id="7f062-195">If you don't see version 50.19 of this model mapping, open the Global repository, and import version 50.19 of the **Invoice model mapping** ER configuration.</span></span>

- <span data-ttu-id="7f062-196">**UBL 売上請求書** ER 形式の構成 :</span><span class="sxs-lookup"><span data-stu-id="7f062-196">**UBL Sales invoice** ER format configuration:</span></span>

    - <span data-ttu-id="7f062-197">バージョン 11.2 には、[形式](general-electronic-reporting.md#FormatComponentOutbound)と形式マッピング ER コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f062-197">Version 11.2 contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="7f062-198">形式コンポーネントは、レポートのレイアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="7f062-198">The format component specifies the report layout.</span></span> <span data-ttu-id="7f062-199">形式マッピング コンポーネントは、モデル データ ソースが含まれており、このデータ ソースが実行時にレポート レイアウトを埋めるためにどのように使用されるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7f062-199">The format mapping component contains the model data source and specifies how this data source is used to fill in the report layout at runtime.</span></span> <span data-ttu-id="7f062-200">この ER 形式は、電子インボイスを汎用ビジネス言語 (UBL) 形式で生成するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="7f062-200">This ER format was configured to generate e-invoices in Universal Business Language (UBL) format.</span></span> <span data-ttu-id="7f062-201">この ER 構成は、インポート対象として選択された **Peppol 売り上げ請求書** の ER 形式の親としてインポートされました。</span><span class="sxs-lookup"><span data-stu-id="7f062-201">It has been imported as a parent of the **Peppol Sales Invoice** ER format that was selected for import.</span></span>

- <span data-ttu-id="7f062-202">**Peppol 売上請求書** ER 形式の構成 :</span><span class="sxs-lookup"><span data-stu-id="7f062-202">**Peppol Sales Invoice** ER format configuration:</span></span>

    - <span data-ttu-id="7f062-203">バージョン 11.2.2 には、汎欧州オンライン公的調達 (PEPPOL)フォーマットで電子インボイスを生成するように構成された形式と形式マッピング ER コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f062-203">Version 11.2.2 contains the format and format mapping ER components that were configured to generate e-invoices in Pan-European Public Procurement OnLine (PEPPOL) format.</span></span>

    ![構成ページの Peppol 売上請求書 ER 形式の設定](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a><span data-ttu-id="7f062-205">売掛金のパラメーターを設定する</span><span class="sxs-lookup"><span data-stu-id="7f062-205">Configure the Accounts receivable parameters</span></span>

1. <span data-ttu-id="7f062-206">**売掛金勘定** \> **設定** \> **売掛金勘定パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-206">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="7f062-207">**電子ドキュメント** タブの **電子報告書** クイックタブで、**売上と自由書式の請求書** フィールドの **Peppol 売上請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-207">On the **Electronic documents** tab, on the **Electronic reporting** FastTab, in the **Sales and Free text invoice** field, select **Peppol Sales Invoice**.</span></span>
3. <span data-ttu-id="7f062-208">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-208">Select **Save**.</span></span>

![売掛金パラメーター ページの電子ドキュメント タブ](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a><span data-ttu-id="7f062-210">法人パラメーターの構成</span><span class="sxs-lookup"><span data-stu-id="7f062-210">Configure the legal entity parameters</span></span>

1. <span data-ttu-id="7f062-211">**組織管理** \> **組織** \> **法人** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-211">Go to **Organization administration** \> **Organizations** \> **Legal entities**.</span></span>
2. <span data-ttu-id="7f062-212">選択した **DEMF** 社の、**銀行口座情報** クイックタブの **ルーティング番号** フィールドに、**1234** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-212">For the selected **DEMF** company, on the **Bank account information** FastTab, in the **Routing number** field, enter **1234**.</span></span>
3. <span data-ttu-id="7f062-213">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-213">Select **Save**.</span></span>
4. <span data-ttu-id="7f062-214">**法人** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-214">Close the **Legal entities** page.</span></span>

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a><span data-ttu-id="7f062-215">顧客レコードを準備する</span><span class="sxs-lookup"><span data-stu-id="7f062-215">Prepare a customer record</span></span>

1. <span data-ttu-id="7f062-216">**売掛金勘定** \> **顧客** \> **すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-216">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="7f062-217">**すべての顧客** ページで、顧客アカウント リンクに **DE-014** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-217">On the **All customers** page, select the **DE-014** customer account link.</span></span>

### <a name="add-a-customer-contact"></a><span data-ttu-id="7f062-218">顧客連絡先の追加</span><span class="sxs-lookup"><span data-stu-id="7f062-218">Add a customer contact</span></span>

1. <span data-ttu-id="7f062-219">**売掛金勘定** \> **顧客** \> **すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-219">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="7f062-220">アクション ペインで、**顧客** タブの **アカウント** グループで、**連絡先** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-220">On the Action Pane, on the **Customer** tab, in the **Accounts** group, select **Contacts**.</span></span>
3. <span data-ttu-id="7f062-221">**連絡先の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-221">Select **Add contacts**.</span></span>
4. <span data-ttu-id="7f062-222">**連絡先** ページの **名前** フィールドで検索を開き、**Adam Carter** を選択して、 **選択** を選択して検索を終了します。</span><span class="sxs-lookup"><span data-stu-id="7f062-222">On the **Contacts** page, in the **First name** field, open the lookup, select **Adam Carter**, and then select **Select** to close the lookup.</span></span>
5. <span data-ttu-id="7f062-223">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-223">Select **Save**.</span></span>
6. <span data-ttu-id="7f062-224">**連絡先** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-224">Close the **Contacts** page.</span></span>

### <a name="define-a-primary-contact"></a><span data-ttu-id="7f062-225">基本連絡先を定義する</span><span class="sxs-lookup"><span data-stu-id="7f062-225">Define a primary contact</span></span>

1. <span data-ttu-id="7f062-226">**売掛金勘定** \> **顧客** \> **すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-226">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="7f062-227">**顧客情報** クイックタブの **基本連絡先** フィールドで、**Adam Carter** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-227">On the **Sales demographics** FastTab, in the **Primary contact** field, select **Adam Carter**.</span></span>

### <a name="set-the-e-invoicing-option"></a><span data-ttu-id="7f062-228">電子請求書のオプションの設定</span><span class="sxs-lookup"><span data-stu-id="7f062-228">Set the e-invoicing option</span></span>

1. <span data-ttu-id="7f062-229">**売掛金勘定** \> **顧客** \> **すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-229">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="7f062-230">**請求と出荷** クイックタブで、**eInvoice** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7f062-230">On the **Invoice and delivery** FastTab, set the **eInvoice** option to **Yes**.</span></span>
3. <span data-ttu-id="7f062-231">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-231">Select **Save**.</span></span>
4. <span data-ttu-id="7f062-232">**すべての顧客** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-232">Close the **All customers** page.</span></span>

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a><span data-ttu-id="7f062-233">標準的な ER の構成を使用して、顧客請求書を処理する</span><span class="sxs-lookup"><span data-stu-id="7f062-233">Process a customer invoice by using the standard ER configurations</span></span>

<span data-ttu-id="7f062-234">以上で、インポートした標準の ER 構成を使用して、自由書式の請求書を顧客に電子的に送信できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="7f062-234">You can now use the standard ER configurations that you imported to electronically send a free text invoice to a customer.</span></span>

### <a name="add-a-new-invoice"></a><span data-ttu-id="7f062-235">新しい請求書の追加</span><span class="sxs-lookup"><span data-stu-id="7f062-235">Add a new invoice</span></span>

1. <span data-ttu-id="7f062-236">**売掛金勘定** \> **請求書** \> **すべての自由書式の請求書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-236">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="7f062-237">**自由書式の請求書** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-237">On the **Free text invoice** page, select **New**.</span></span>
3. <span data-ttu-id="7f062-238">**自由書式の請求書ヘッダー** クイックタブの **顧客アカウント** フィールドで、**DE-014** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-238">On the **Free text invoice header** FastTab, in the **Customer account** field, select **DE-014**.</span></span>
4. <span data-ttu-id="7f062-239">**請求明細行** クイックタブで、請求書の明細行が自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="7f062-239">On the **Invoice lines** FastTab, an invoice line is automatically added.</span></span> <span data-ttu-id="7f062-240">この明細行で、次の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="7f062-240">On this line, set the following fields:</span></span>

    - <span data-ttu-id="7f062-241">**説明** フィールドで **ノートブック** を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-241">In the **Description** field, enter **Notebook**.</span></span>
    - <span data-ttu-id="7f062-242">**主勘定** フィールドで、 **401100** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-242">In the **Main account** field, select **401100**.</span></span>
    - <span data-ttu-id="7f062-243">**単価フィールド** に **1000** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-243">In the **Unit price** field, enter **1000**.</span></span>

5. <span data-ttu-id="7f062-244">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-244">Select **Save**.</span></span>

![自由書式の請求書のページ](./media/er-quick-start3-add-invoice.png)

<span data-ttu-id="7f062-246">詳細については、[自由書式の請求書](../../../finance/accounts-receivable/create-free-text-invoice-new.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-246">For more information, see [Create a free text invoice](../../../finance/accounts-receivable/create-free-text-invoice-new.md).</span></span>

### <a name="post-a-new-invoice"></a><span data-ttu-id="7f062-247">新しい請求書を転記する</span><span class="sxs-lookup"><span data-stu-id="7f062-247">Post a new invoice</span></span>

1. <span data-ttu-id="7f062-248">**売掛金勘定** \> **請求書** \> **すべての自由書式の請求書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-248">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="7f062-249">**自由書式の請求書** ページのアクション ペインで、**転記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-249">On the **Free text invoice** page, on the Action Pane, select **Post**.</span></span>
3. <span data-ttu-id="7f062-250">**自由書式の請求書の転記**  ダイアログ ボックスで、**OK** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="7f062-250">In the **Post free text invoice** dialog box, select **OK**.</span></span>

![自由書式の請求書の詳細ページ](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a><span data-ttu-id="7f062-252">転記された請求書を送信する</span><span class="sxs-lookup"><span data-stu-id="7f062-252">Send a posted invoice</span></span>

1. <span data-ttu-id="7f062-253">**売掛金勘定** \> **請求書** \> **すべての自由書式の請求書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-253">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="7f062-254">**自由書式の請求書** ページのアクション ペイン **ドキュメント** グループで、 **送信** \> **原本** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="7f062-254">On the **Free text invoice** page, on the Action Pane, in the **Document** group, select **Send** \> **Original**.</span></span>

    ![原本の請求書のプレビュー](./media/er-quick-start3-send-invoice.png)

3. <span data-ttu-id="7f062-256">**自由書式の請求書**  ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-256">Close the **Free text invoice** page.</span></span>

### <a name="analyze-a-generated-e-invoice"></a><span data-ttu-id="7f062-257">生成された電子請求書の分析</span><span class="sxs-lookup"><span data-stu-id="7f062-257">Analyze a generated e-invoice</span></span>

1. <span data-ttu-id="7f062-258">**組織管理** \> **電子申告** \> **電子申告ジョブ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-258">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>
2. <span data-ttu-id="7f062-259">**電子申告** ジョブ ページで、タスクの説明に **eInvoice XML を送信する** がある初期レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-259">On the **Electronic reporting jobs** page, select the initial record that has the task description **Send the eInvoice XML**.</span></span>
3. <span data-ttu-id="7f062-260">**ファイルの表示** を選択 すると、生成されたファイルの一覧にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7f062-260">Select **Show files** to access the list of generated files.</span></span>

    ![電子申告ジョブ ページ](./media/er-quick-start3-jobs-list.png)

4. <span data-ttu-id="7f062-262">**開く** を選択して、生成された電子請求書の XML ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7f062-262">Select **Open** to download the e-invoice XML file that is generated.</span></span>
5. <span data-ttu-id="7f062-263">電子請求書の XML ファイルを分析します。</span><span class="sxs-lookup"><span data-stu-id="7f062-263">Analyze the e-invoice XML file.</span></span> <span data-ttu-id="7f062-264">顧客税スキーマは現在、**schemeID** と **schemeAgencyID** の XML 属性で表されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-264">Notice that the customer tax schema is currently represented by the **schemeID** and **schemeAgencyID** XML attributes.</span></span> <span data-ttu-id="7f062-265">また、**cbc: CustomizationID** XML 要素には次のテキストが現在含まれていることに注意してください :  `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` 。</span><span class="sxs-lookup"><span data-stu-id="7f062-265">Also notice that the **cbc:CustomizationID** XML element currently contains the following text: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.</span></span>

    ![生成された電子請求書の XML ファイルのプレビュー](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a><span data-ttu-id="7f062-267">カスタム データベース フィールドの追加</span><span class="sxs-lookup"><span data-stu-id="7f062-267">Add a custom database field</span></span>

<span data-ttu-id="7f062-268">[カスタム フィールド](../../fin-ops/get-started/user-defined-fields.md)機能を使用すると、現在の財務インスタンスで次のようなカスタマイズを実行できます :</span><span class="sxs-lookup"><span data-stu-id="7f062-268">You can use the [Custom field](../../fin-ops/get-started/user-defined-fields.md) feature to do the following customization in the current Finance instance:</span></span>

- <span data-ttu-id="7f062-269">顧客ごとに連邦税の識別コードを格納するカスタム データベース フィールドを新たに追加して、データベースの構造をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="7f062-269">Customize the database structure by adding a new custom database field that stores a federal tax identification code for every customer.</span></span>
- <span data-ttu-id="7f062-270">新しいカスタムデータベースのフィールドに税コードの値を入力するために使用できる新しいデータ入力フィールドを追加して、**顧客ページ** をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="7f062-270">Customize the **Customer** page by adding a new data entry field that can be used to enter a tax code value in the new custom database field.</span></span>

<span data-ttu-id="7f062-271">これらの手順に従ってカスタマイズを行います。</span><span class="sxs-lookup"><span data-stu-id="7f062-271">Follow these steps to do the customization.</span></span>

1. <span data-ttu-id="7f062-272">**売掛金勘定** \> **顧客** \> **すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-272">Go to **Accounts receivables** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="7f062-273">**すべての顧客** ページで、顧客アカウント リンクに **DE-014** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-273">On the **All customers** page, select the **DE-014** customer account link.</span></span>
3. <span data-ttu-id="7f062-274">**全般** クイックタブで、**言語**  フィールドの下の空白領域を右クリックし、**個人設定 : UpperGroup** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f062-274">On the **General** FastTab, right-click in any blank area under the **Language** field, and then select **Personalize: UpperGroup**.</span></span>

    <span data-ttu-id="7f062-275">**一般** クイックタブの内容が強調表示され、**個人用** メニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f062-275">The contents of the **General** FastTab are highlighted, and a **Personalize** menu appears.</span></span>

4. <span data-ttu-id="7f062-276">**個人設定** メニューで、**フィールドの追加** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="7f062-276">On the **Personalize** menu, select **Add a field**.</span></span>
5. <span data-ttu-id="7f062-277">**新しい列の追加** ダイアログ ボックスで、 **新規フィールドの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-277">In the **Add columns** dialog box, select **Create new field**.</span></span>
6. <span data-ttu-id="7f062-278">**新しいフィールドの作成** ダイアログ ボックスの **テーブル名** フィールドで、**顧客** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-278">In the **Create new field** dialog box, in the **Table name** field, select **Customers**.</span></span>
7. <span data-ttu-id="7f062-279">**名前の接頭辞** フィールドに、**FederalTaxID** を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-279">In the **Name prefix** field, enter **FederalTaxID**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f062-280">フィールド名全体が自動的に **FederalTaxID\_Custom** と定義されています。</span><span class="sxs-lookup"><span data-stu-id="7f062-280">The whole field name has been automatically defined as **FederalTaxID\_Custom**.</span></span>

8. <span data-ttu-id="7f062-281">**ラベル** フィールドで、**連邦税 ID** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-281">In the **Label** field, enter **Federal Tax ID**.</span></span>
9. <span data-ttu-id="7f062-282">**タイプ** フィールドで、**テキスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-282">In the **Type** field, select **Text**.</span></span>
10. <span data-ttu-id="7f062-283">**長さ** フィールドに **20** を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-283">In the **Length** field, enter **20**.</span></span>
11. <span data-ttu-id="7f062-284">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-284">Select **Save**.</span></span>
12. <span data-ttu-id="7f062-285">表示されたメッセージボックスで、**はい** を選択し、**顧客** テーブルに対して新しい **FederalTaxID** フィールド エントリを作成することを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f062-285">In the message box that appears, select **Yes** to confirm that you want to create a new **FederalTaxID** field entry for the **Customers** table.</span></span>
13. <span data-ttu-id="7f062-286">**挿入** を選択して <a name="insert_custom_field"></a> **FederalTaxID\_Custom** フィールドを現在のページに追加します。</span><span class="sxs-lookup"><span data-stu-id="7f062-286">Select **Insert** to <a name="insert_custom_field"></a>add the **FederalTaxID\_Custom** field to the current page.</span></span>

    ![すべての顧客のページ](./media/er-quick-start3-create-new-field.gif)

14. <span data-ttu-id="7f062-288">**すべての顧客** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-288">Close the **All customers** page.</span></span>

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a><span data-ttu-id="7f062-289">ER メタデータの更新</span><span class="sxs-lookup"><span data-stu-id="7f062-289">Refresh the ER metadata</span></span>

<span data-ttu-id="7f062-290">追加したカスタム フィールドを ER モデル マッピング デザイナーで[表示する](electronic-reporting-er-configure-parameters.md#frequently-asked-questions)には、ER のメタデータを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-290">You must refresh the ER metadata to make the custom field that you added [visible](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) in the ER model mapping designer.</span></span>

1. <span data-ttu-id="7f062-291">**組織管理** \> **電子申告** \> **テーブル参照のリビルド** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-291">Go to **Organization administration** \> **Electronic reporting** \> **Rebuild table references**.</span></span>
2. <span data-ttu-id="7f062-292">**データ モデルの更新** ダイアログ ボックスで、**OK** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="7f062-292">In the **Update data model** dialog box, select **OK**.</span></span>

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a><span data-ttu-id="7f062-293">カスタム ER 構成の設計</span><span class="sxs-lookup"><span data-stu-id="7f062-293">Design the custom ER configurations</span></span>

<span data-ttu-id="7f062-294">Microsoft が提供する ER 構成を使用して、カスタム ER 構成を設計し、新しい税コードを含む電子インボイスを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-294">You can use the Microsoft-provided ER configurations to design your custom ER configurations so that they generate e-invoices that contain the new tax code.</span></span>

### <a name="customize-the-data-model-configuration"></a><span data-ttu-id="7f062-295">データ モデルの構成をカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="7f062-295">Customize the data model configuration</span></span>

<span data-ttu-id="7f062-296">電子レポート機能コンサルタントのロールを持つユーザーは、カスタム ER データ モデルを設計することができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-296">As a user in the Electronic Reporting Functional Consultant role, you can design your custom ER data model.</span></span>

#### <a name="add-a-custom-data-model-configuration"></a><span data-ttu-id="7f062-297">カスタム ER データ モデルの構成を追加する</span><span class="sxs-lookup"><span data-stu-id="7f062-297">Add a custom data model configuration</span></span>

1. <span data-ttu-id="7f062-298">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-298">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7f062-299">**構成** ページで、ペインの左側の構成ツリーで、**顧客請求書モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-299">On the **Configurations** page, in the configuration tree in the left pane, select **Customer invoice model**.</span></span>
3. <span data-ttu-id="7f062-300">アクション ウィンドウで、**構成の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-300">On the Action Pane, select **Create configuration**.</span></span>
4. <span data-ttu-id="7f062-301">ドロップダウン ダイアログ ボックスの **新規** フィールドで、 **名前から派生 : 顧客請求書モデル、Microsoft** を選択し、新しいカスタム ER データ モデルの構成が ER データ モデルの構成に基づくものであることを明示します。</span><span class="sxs-lookup"><span data-stu-id="7f062-301">In the drop-down dialog box, in the **New** field, select **Derive from Name: Customer invoice model, Microsoft** to indicate that your new custom ER data model configuration should be based on the ER data model configuration.</span></span>
5. <span data-ttu-id="7f062-302">**名前** フィールドに、**請求書モデル (Litware)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-302">In the **Name** field, enter **Invoice model (Litware)**.</span></span>
6. <span data-ttu-id="7f062-303">**構成の作成** を選択して、新しい ER の構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="7f062-303">Select **Create configuration** to add the new ER configuration.</span></span>

<span data-ttu-id="7f062-304">これで、ER データ モデル デザイナーを使用して、**請求モデル (Litware)** の ER 構成のバージョン 50.1 を **ドラフト** の[状態](general-electronic-reporting.md#component-versioning)で編集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="7f062-304">You can now use the ER data model designer to edit version 50.1 of the **Invoice model (Litware)** ER configuration in **Draft** [status](general-electronic-reporting.md#component-versioning).</span></span>

![構成ページの ER の構成 バージョン 50.1](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a><span data-ttu-id="7f062-306">カスタム データ モデルの構成</span><span class="sxs-lookup"><span data-stu-id="7f062-306">Configure a custom data model</span></span>

<span data-ttu-id="7f062-307">連邦税 ID コードの値を提供する新たなフィールドを追加して、カスタム データ モデルを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-307">You must modify your custom data model by adding a new field to provide the value of a federal tax identification code.</span></span> <span data-ttu-id="7f062-308">このコードは、このデータ モデルをデータ ソースとして使用するすべての ER 形式の顧客データの一部となります。</span><span class="sxs-lookup"><span data-stu-id="7f062-308">This code is part of the customer data for every ER format that will use this data model as a data source.</span></span>

1. <span data-ttu-id="7f062-309">**構成** ページの、左側のペインの構成ツリーで、**請求書モデル (Litware)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-309">On the **Configurations** page, in the configuration tree in the left pane, select **Invoice model (Litware)**.</span></span>
2. <span data-ttu-id="7f062-310">**バージョン**  クイック タブで、**ドラフト** の状態となっている、選択した ER データ モデルの構成バージョン **50.1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-310">On the **Versions** FastTab, select version **50.1** of the selected ER data model configuration in **Draft** status.</span></span>
3. <span data-ttu-id="7f062-311">アクション ペインで、選択した構成バージョンの  **デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-311">On the Action Pane, select **Designer** for the selected configuration version.</span></span>
4. <span data-ttu-id="7f062-312">**データ モデル デザイナー** ページのデータ モデル ツリーで、**顧客情報 (顧客)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-312">On the **Data model designer** page, in the data model tree, select **Customer information (Customer)**.</span></span>
5. <span data-ttu-id="7f062-313">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-313">Select **New**.</span></span>
6. <span data-ttu-id="7f062-314">ドロップダウン ダイアログ ボックスの **新しいノード** フィールドで、**アクティブなノードの子** の既定値をそのまま使用します。</span><span class="sxs-lookup"><span data-stu-id="7f062-314">In the drop-down dialog box, in the **New node as a** field, accept the default value, **Child of an active node**.</span></span>
7. <span data-ttu-id="7f062-315">**名前** フィールドに、**FederalTaxID\_Litware** を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-315">In the **Name** field, enter **FederalTaxID\_Litware**.</span></span>
8. <span data-ttu-id="7f062-316">**品目タイプ** フィールドで、既定値の **文字列** をそのまま使用します。</span><span class="sxs-lookup"><span data-stu-id="7f062-316">In the **Item type** field, accept the default value, **String**.</span></span>
9. <span data-ttu-id="7f062-317">**追加** を選択してから、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-317">Select **Add**, and then select **Save**.</span></span>

    ![データ モデル デザイナーのページ](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > <span data-ttu-id="7f062-319">**ラベル** フィールドと **説明** フィールドには、新しいフィールドの目的が示されます。</span><span class="sxs-lookup"><span data-stu-id="7f062-319">The **Label** and **Description** fields describe the purpose of the new field.</span></span> <span data-ttu-id="7f062-320">これらのフィールドは、複数の言語で入力できます。</span><span class="sxs-lookup"><span data-stu-id="7f062-320">You can fill in these fields in multiple languages.</span></span> <span data-ttu-id="7f062-321">詳細については、[電子申告で複数言語のレポートを設計する](er-design-multilingual-reports.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-321">For more information, see [Design multilingual reports in Electronic reporting](er-design-multilingual-reports.md).</span></span>

10. <span data-ttu-id="7f062-322">**データ モデル デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-322">Close the **Data model designer** page.</span></span>

#### <a name="complete-a-custom-data-model-configuration"></a><span data-ttu-id="7f062-323">カスタム データ モデルの構成を完了する</span><span class="sxs-lookup"><span data-stu-id="7f062-323">Complete a custom data model configuration</span></span>

<span data-ttu-id="7f062-324">他のカスタム ER の構成を追加できるように、カスタム ER データ モデル構成のバージョン 50.1 を使用して作業を[完了](general-electronic-reporting.md#component-versioning)する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-324">You must [complete](general-electronic-reporting.md#component-versioning) your work with version 50.1 of your custom ER data model configuration to make it available so that other custom ER configurations can be added.</span></span>

1. <span data-ttu-id="7f062-325">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-325">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7f062-326">**構成** ページの左側ペインの構成ツリーで、**請求書モデル** を展開し、**請求書モデル (Litware)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-326">On the **Configurations** page, in the configuration tree in the left pane, expand **Invoice model**, and select **Invoice model (Litware)**.</span></span>
3. <span data-ttu-id="7f062-327">**バージョン** クイックタブで、**ステータスの変更** \> **完了済**、そして **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-327">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="7f062-328">バージョン 50.1 のステータスは、**ドラフト** から **完了済** に変更され、バージョンは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-328">The status of version 50.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="7f062-329">新しい編集可能なバージョン 50.2 が追加され、状態が **ドラフト** になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-329">A new editable version, 50.2, is added and has a status of **Draft**.</span></span> <span data-ttu-id="7f062-330">このバージョンを使用すると、カスタム ER データ モデルの構成にさらに変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-330">You can use this version to make further changes in your custom ER data model configuration.</span></span>

![構成ページで完了したバージョン 50.1](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a><span data-ttu-id="7f062-332">モデル マッピングの構成をカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="7f062-332">Customize the model mapping configuration</span></span>

<span data-ttu-id="7f062-333">電子レポート機能の開発者のロールを持つユーザーは、カスタム ER モデル マッピングを設計することができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-333">As a user in the Electronic Reporting Developer role, you can design your custom ER model mapping.</span></span>

#### <a name="add-a-custom-model-mapping-configuration"></a><span data-ttu-id="7f062-334">カスタム モデル マッピングの構成を追加する</span><span class="sxs-lookup"><span data-stu-id="7f062-334">Add a custom model mapping configuration</span></span>

1. <span data-ttu-id="7f062-335">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-335">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7f062-336">**構成** ページの左側ペインの構成ツリーで、**顧客請求書モデル** を展開し、**顧客請求書モデル マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-336">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model**, and select **Customer invoice model mapping**.</span></span>
3. <span data-ttu-id="7f062-337">アクション ウィンドウで、**構成の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-337">On the Action Pane, select **Create configuration**.</span></span>
4. <span data-ttu-id="7f062-338">ドロップダウン ダイアログ ボックスの **新規** フィールドで、 **名前から派生 : 顧客請求書モデル マッピング、Microsoft** を選択し、新しいカスタム ER モデル マッピングの構成が ER モデル マッピングの構成に基づくものであることを明示します。</span><span class="sxs-lookup"><span data-stu-id="7f062-338">In the drop-down dialog box, in the **New** field, select **Derive from Name: Customer invoice model mapping, Microsoft** to indicate that your new custom ER model mapping configuration should be based on the ER model mapping configuration.</span></span>
5. <span data-ttu-id="7f062-339">**名前** フィールドに、**請求書モデル マッピング (Litware)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-339">In the **Name** field, enter **Invoice model mapping (Litware)**.</span></span>
6. <span data-ttu-id="7f062-340">**ターゲット モデル** フィールドで、**請求書モデル (Litware)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-340">In the **Target model** field, select **Invoice model (Litware)**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7f062-341">この手順は非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="7f062-341">This step is very important.</span></span> <span data-ttu-id="7f062-342">これを省略すると、構成済のモデル マッピングでカスタム データ モデルを使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="7f062-342">If you omit it, you won't be able to use your custom data model in the configured model mapping.</span></span>

7. <span data-ttu-id="7f062-343">**構成の作成** を選択して、新しい ER の構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="7f062-343">Select **Create configuration** to add the new ER configuration.</span></span>

![構成ページにおけるカスタム モデル マッピング構成の追加](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a><span data-ttu-id="7f062-345">カスタム モデル マッピングの構成</span><span class="sxs-lookup"><span data-stu-id="7f062-345">Configure a custom model mapping</span></span>

<span data-ttu-id="7f062-346">カスタム モデルのマッピングを修正し、カスタム データ モデルのカスタム **FederalTaxID\_Litware** フィールドを実行時にアプリケーション データでどのように入力するかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-346">You must modify your custom model mapping and specify how the custom **FederalTaxID\_Litware** field of the custom data model should be filled in with application data at runtime.</span></span>

1. <span data-ttu-id="7f062-347">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-347">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7f062-348">**構成** ページの左側ペインの構成ツリーで、 **顧客請求書モデル** \> **顧客請求書モデル マッピング** を展開し、**請求書モデル マッピング (Litware)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-348">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model** \> **Customer invoice model mapping**, and select **Invoice model mapping (Litware)**.</span></span>
3. <span data-ttu-id="7f062-349">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-349">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="7f062-350">**モデルからデータ ソースへのマッピング** ページで、**顧客請求書** マッピングを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-350">On the **Model to datasource mapping** page, select the **Customer invoice** mapping.</span></span>

    ![モデルからデータ ソースへのマッピング ページ](./media/er-quick-start3-select-customer-mapping.png)

5. <span data-ttu-id="7f062-352">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f062-352">Select **Designer**.</span></span>
6. <span data-ttu-id="7f062-353">**モデル マッピング デザイナ** ページの **データ ソース** ペインで、**CustInvoiceJour** アプリケーション テーブルを表す **CustInvoiceJour** データソースを展開します。</span><span class="sxs-lookup"><span data-stu-id="7f062-353">On the **Model mapping designer** page, in the **Data sources** pane, expand the **CustInvoiceJour** data source that represents the **CustInvoiceJour** application table.</span></span>
7. <span data-ttu-id="7f062-354">**CustInvoiceJour** 配下の **関係** を展開して、**CustInvoiceJour** テーブルの多対一 (N:1) タイプの関係の一覧を確認します。</span><span class="sxs-lookup"><span data-stu-id="7f062-354">Under **CustInvoiceJour**, expand **Relations** to review the list of relations of the many-to-one (N:1) type for the **CustInvoiceJour** table.</span></span>
8. <span data-ttu-id="7f062-355">**CustInvoiceJour** \> **関係** 配下で、**顧客 (CustTable)** を展開して、**Customers (CustTable)** テーブルのフィールドと関係にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="7f062-355">Under **CustInvoiceJour** \> **Relations**, expand **Customers (CustTable)** to access the fields and relations of the **Customers (CustTable)** table.</span></span>
9. <span data-ttu-id="7f062-356">[前述の手順](#insert_custom_field)で実装した **FederalTaxID\_カスタム** データ ソース フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-356">Select the **FederalTaxID\_Custom** data source field that you implemented [earlier](#insert_custom_field).</span></span>
10. <span data-ttu-id="7f062-357">**データモデル** ペインで、**顧客情報 (顧客)** を展開 し、**FederalTaxID\_Litware** データ モデル フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-357">In the **Data model** pane, expand **Customer information (Customer)**, and select the **FederalTaxID\_Litware** data model field.</span></span>
11. <span data-ttu-id="7f062-358">**バインド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-358">Select **Bind**.</span></span>

    ![モデル マッピング デザイナーのページ](./media/er-quick-start3-customize-model-mapping.gif)

12. <span data-ttu-id="7f062-360">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-360">Select **Save**.</span></span>
13. <span data-ttu-id="7f062-361">**モデル マッピング デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-361">Close the **Model mapping designer** page.</span></span>
14. <span data-ttu-id="7f062-362">**モデルからデータ ソースへのマッピング** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-362">Close the **Model to datasource mapping** page.</span></span>

#### <a name="complete-a-custom-model-mapping-configuration"></a><span data-ttu-id="7f062-363">カスタム モデルの構成を完了する</span><span class="sxs-lookup"><span data-stu-id="7f062-363">Complete a custom model mapping configuration</span></span>

<span data-ttu-id="7f062-364">カスタム ER モデル マッピング構成のバージョン 50.19.1 を使用できるようにするには、作業を[完了](general-electronic-reporting.md#component-versioning)させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-364">You must [complete](general-electronic-reporting.md#component-versioning) your work with version 50.19.1 of your custom ER model mapping configuration to make it available for use.</span></span>

1. <span data-ttu-id="7f062-365">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-365">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7f062-366">**構成** ページの左側ペインの構成ツリーで、 **顧客請求書モデル** \> **顧客請求書モデル マッピング** を展開し、**請求書モデル マッピング (Litware)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-366">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model** \> **Customer invoice model mapping**, and select **Invoice model mapping (Litware)**.</span></span>
3. <span data-ttu-id="7f062-367">**バージョン** クイックタブで、**ステータスの変更** \> **完了済**、そして **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-367">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="7f062-368">バージョン 50.19.1 のステータスは、**ドラフト** から **完了済** に変更され、バージョンは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-368">The status of version 50.19.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="7f062-369">新しい編集可能なバージョン 50.19.2 が追加され、状態が **ドラフト** になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-369">A new editable version, 50.19.2, is added and has a status of **Draft**.</span></span> <span data-ttu-id="7f062-370">このバージョンを使用すると、カスタム ER モデル マッピングの構成にさらに変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-370">You can use this version to make further changes in your custom ER model mapping configuration.</span></span>

![構成ページで完了したバージョン 50.19.1](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> <span data-ttu-id="7f062-372">サポートされている構成[ライフサイクル](general-electronic-reporting-manage-configuration-lifecycle.md) は、データベースの変更のライフサイクルをカバーしていません。</span><span class="sxs-lookup"><span data-stu-id="7f062-372">The supported configuration [lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md) doesn't cover the lifecycle of database changes.</span></span> <span data-ttu-id="7f062-373">現在の財務インスタンスから **請求書モデルマッピング (Litware)** 構成のバージョン 50.19.1 をエクスポートして、**CustTable** テーブルのカスタム **FederalTaxID\_Custom** フィールドを含まない別のインスタンスにインポートしようとすると、例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="7f062-373">If you export version 50.19.1 of the **Invoice model mapping (Litware)** configuration from the current Finance instance and try to import it into another instance that doesn't contain the custom **FederalTaxID\_Custom** field in the **CustTable** table, an exception will occur.</span></span> <span data-ttu-id="7f062-374">この例外は、インポートした ER の構成がターゲットの財務インスタンスのメタデータと互換性がないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="7f062-374">The exception will state that the imported ER configuration isn't compatible with the metadata of the target Finance instance.</span></span>

### <a name="customize-the-format-configuration"></a><span data-ttu-id="7f062-375">形式の構成をカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="7f062-375">Customize the format configuration</span></span>

<span data-ttu-id="7f062-376">電子レポート機能コンサルタントのロールを持つユーザーは、カスタム ER の形式を設計することができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-376">As a user in the Electronic Reporting Functional Consultant role, you can design your custom ER format.</span></span>

#### <a name="add-a-custom-format-configuration"></a><span data-ttu-id="7f062-377">カスタム ER 形式の構成を追加する</span><span class="sxs-lookup"><span data-stu-id="7f062-377">Add a custom format configuration</span></span>

1. <span data-ttu-id="7f062-378">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-378">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7f062-379">**構成**  ページの左側ペインの構成ツリーで、**顧客請求書モデル** \> **UBL 売上請求書** を展開し、**Peppol 売上請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-379">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model** \> **UBL Sales invoice**, and select **Peppol Sales Invoice**.</span></span>
3. <span data-ttu-id="7f062-380">アクション ウィンドウで、**構成の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-380">On the Action Pane, select **Create configuration**.</span></span>
4. <span data-ttu-id="7f062-381">ドロップダウン ダイアログ ボックスの **新規** フィールドで、 **名前から派生 : Peppol 売上請求書、Microsoft** を選択し、カスタム ER 形式の構成が ER 形式の構成に基づくものであることを明示します。</span><span class="sxs-lookup"><span data-stu-id="7f062-381">In the drop-down dialog box, in the **New** field, select **Derive from Name: Peppol Sales Invoice, Microsoft** to indicate that your custom ER format configuration should be based on the ER format configuration.</span></span>
5. <span data-ttu-id="7f062-382">**名前** フィールドに、**Peppol 売上請求書 (Litware)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-382">In the **Name** field, enter **Peppol Sales Invoice (Litware)**.</span></span>
6. <span data-ttu-id="7f062-383">**データ モデル** フィールドで、**請求書モデル (Litware)** を選択してカスタム データ モデルとモデル マッピング コンポーネントを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f062-383">In the **Data model** field, select **Invoice model (Litware)** to use your custom data model and model mapping components.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f062-384">この手順は非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="7f062-384">This step is very important.</span></span> <span data-ttu-id="7f062-385">これを省略すると、構成済の形式でカスタム データ モデルを使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="7f062-385">If you omit it, you won't be able to use your custom data model in the configured format.</span></span>

7. <span data-ttu-id="7f062-386">**データ モデル** フィールドで、**InvoiceCustomer** のルート定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-386">In the **Data model** field, select the **InvoiceCustomer** root definition.</span></span>
8. <span data-ttu-id="7f062-387">**構成の作成** を選択して、新しい ER の構成を追加します。</span><span class="sxs-lookup"><span data-stu-id="7f062-387">Select **Create configuration** to add the new ER configuration.</span></span>

![構成ページにおけるカスタム形式構成の追加](./media/er-quick-start3-adding-custom-format.png)

<span data-ttu-id="7f062-389">これで、ER オペレーション デザイナーを使用して、**Peppol 売上請求書 (Litware)** の ER 構成のバージョン 11.2.2.1 を **ドラフト** の[状態](general-electronic-reporting.md#component-versioning)で編集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="7f062-389">You can now use the ER Operations designer to edit version 11.2.2.1 of the **Peppol Sales Invoice (Litware)** ER configuration in **Draft** [status](general-electronic-reporting.md#component-versioning).</span></span>

![構成ページの ER の構成 バージョン 11.2.2.1](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a><span data-ttu-id="7f062-391">カスタム形式の構成</span><span class="sxs-lookup"><span data-stu-id="7f062-391">Configure a custom format</span></span>

<span data-ttu-id="7f062-392">請求書を発行した顧客の連邦税 ID コードの値を記入する新しい形式要素を追加して、カスタム フォーマットを修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-392">You must modify your custom format by adding a new format element to fill in the value of an invoiced customer's federal tax identification code.</span></span>

1. <span data-ttu-id="7f062-393">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-393">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7f062-394">**構成** ページの左側ペインの構成ツリーで、**顧客請求書モデル** \> **UBL 売上請求書** \> **Peppol 売上請求書** を展開し、**Peppol 売上請求書 (Litware)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-394">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model** \> **UBL Sales invoice** \> **Peppol Sales Invoice**, and select **Peppol Sales Invoice (Litware)**.</span></span>
3. <span data-ttu-id="7f062-395">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-395">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="7f062-396">形式のツリーで、**XMLHeader** \> **請求書** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** を展開し、**cbc:ID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-396">In the format tree, expand **XMLHeader** \> **Invoice** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme**, and select **cbc:ID**.</span></span>
5. <span data-ttu-id="7f062-397">**追加** を選択し、**XML** \> **属性** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-397">Select **Add**, and then select **XML** \> **Attribute**.</span></span>
6. <span data-ttu-id="7f062-398">**コンポーネント プロパティ** ダイアログ ボックスの、**名前** フィールドで、**FederalTaxID** を入力してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-398">In the **Component property** dialog box, in the **Name** field, enter **FederalTaxID**.</span></span>
7. <span data-ttu-id="7f062-399">**OK** を選択して新しい形式要素を追加し、新たな **FederalTaxID** XML 属性を生成した XML ファイルに作成します。</span><span class="sxs-lookup"><span data-stu-id="7f062-399">Select **OK** to add a new format element to create a new **FederalTaxID** XML attribute in a generated XML file.</span></span>
8. <span data-ttu-id="7f062-400">形式のツリーで、 **XMLHeader** \> **請求書** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** 配下で、**FederalTaxID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-400">In the format tree, under **XMLHeader** \> **Invoice** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID**, select **FederalTaxID**.</span></span>
9. <span data-ttu-id="7f062-401">**上へ移動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-401">Select **Move up**.</span></span>

![形式デザイナー ページにおける新しい形式要素](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a><span data-ttu-id="7f062-403">カスタム形式マッピングの構成</span><span class="sxs-lookup"><span data-stu-id="7f062-403">Configure a custom format mapping</span></span>

1. <span data-ttu-id="7f062-404">**形式デザイナー** ページの **マッピング** タブで、**モデル** タイプの **請求書** データ ソースを展開します。</span><span class="sxs-lookup"><span data-stu-id="7f062-404">On the **Format designer** page, on the **Mapping** tab, expand the **Invoice** data source of the **Model** type.</span></span>
2. <span data-ttu-id="7f062-405">**請求書** 配下で  **顧客情報 (顧客)** を展開し、**FederalTaxID\_Litware** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-405">Under **Invoice**, expand **Customer information (Customer)**, and select **FederalTaxID\_Litware**.</span></span>
3. <span data-ttu-id="7f062-406">**バインド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-406">Select **Bind**.</span></span>

    ![形式デザイナーのページ](./media/er-quick-start3-customized-format-mapping.png)

4. <span data-ttu-id="7f062-408">**モデル** タイプの **請求書** データ ソースを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-408">Select the **Invoice** data source of the **Model** type, and then select **Edit**.</span></span>
5. <span data-ttu-id="7f062-409">**バージョン** フィールドで、カスタム データモデルのバージョン **1** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-409">In the **Version** field, select version **1** of your custom data model, and then select **OK**.</span></span>
6. <span data-ttu-id="7f062-410">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-410">Select **Save**.</span></span>
7. <span data-ttu-id="7f062-411">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-411">Close the **Format designer** page.</span></span>

#### <a name="complete-a-custom-format-configuration"></a><span data-ttu-id="7f062-412">カスタム形式の構成を完了する</span><span class="sxs-lookup"><span data-stu-id="7f062-412">Complete a custom format configuration</span></span>

<span data-ttu-id="7f062-413">カスタム ER 形式の構成バージョン 11.2.2.1 を使用できるようにするには、作業を[完了](general-electronic-reporting.md#component-versioning)させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-413">You must [complete](general-electronic-reporting.md#component-versioning) your work with version 11.2.2.1 of your custom ER format configuration to make it available for use.</span></span>

1. <span data-ttu-id="7f062-414">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-414">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7f062-415">**構成** ページの左側ペインの構成ツリーで、**顧客請求書モデル** \> **UBL 売上請求書** \> **Peppol 売上請求書** を展開し、**Peppol 売上請求書 (Litware)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-415">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model** \> **UBL Sales invoice** \> **Peppol Sales Invoice**, and select **Peppol Sales Invoice (Litware)**.</span></span>
3. <span data-ttu-id="7f062-416">**バージョン** クイックタブで、**ステータスの変更** \> **完了済**、そして **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-416">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="7f062-417">バージョン 11.2.2.1 のステータスは、**ドラフト** から **完了済** に変更され、バージョンは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-417">The status of version 11.2.2.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="7f062-418">新しい編集可能なバージョン 11.2.2.2 が追加され、状態が **ドラフト** になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-418">A new editable version, 11.2.2.2, is added and has a status of **Draft**.</span></span> <span data-ttu-id="7f062-419">このバージョンを使用すると、カスタム ER 形式の構成に追加の変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-419">You can use this version to make further changes in your custom ER format configuration.</span></span>

![構成ページで完了したバージョン 11.2.2.1](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a><span data-ttu-id="7f062-421">売掛金勘定パラメーターを構成して、カスタマイズした ER の構成を使用する</span><span class="sxs-lookup"><span data-stu-id="7f062-421">Configure the Accounts receivable parameters to start to use custom ER configurations</span></span>

1. <span data-ttu-id="7f062-422">**売掛金勘定** \> **設定** \> **売掛金勘定パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-422">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="7f062-423">**電子ドキュメント** タブの **電子報告書** クイックタブで、**売上と自由書式の請求書** フィールドの **Peppol 売上請求書 (Litware)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-423">On the **Electronic documents** tab, on the **Electronic reporting** FastTab, in the **Sales and Free text invoice** field, select **Peppol Sales Invoice (Litware)**.</span></span>
3. <span data-ttu-id="7f062-424">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-424">Select **Save**.</span></span>

![売掛金パラメーター ページの、電子ドキュメント タブ、電子報告書 クイックタブ](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a><span data-ttu-id="7f062-426">連邦税 ID コードを追加して顧客記録を更新する</span><span class="sxs-lookup"><span data-stu-id="7f062-426">Update a customer record by adding a federal tax identification code</span></span>

1. <span data-ttu-id="7f062-427">**売掛金勘定** \> **顧客** \> **すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-427">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="7f062-428">**すべての顧客** ページで、顧客アカウント リンクに **DE-014** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-428">On the **All customers** page, select the **DE-014** customer account link.</span></span>
3. <span data-ttu-id="7f062-429">**全般** クイックタブの **連邦税 ID** フィールドに、**LITWARE-6789** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f062-429">On the **General** FastTab, in the **Federal Tax ID** field, enter **LITWARE-6789**.</span></span>
4. <span data-ttu-id="7f062-430">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-430">Select **Save**.</span></span>

    ![DE-014 顧客の詳細 ページ](./media/er-quick-start3-added-tax-id-value.png)

5. <span data-ttu-id="7f062-432">**すべての顧客** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-432">Close the **All customers** page.</span></span>

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a><span data-ttu-id="7f062-433">カスタマイズした ER の構成を使用して、顧客請求書を処理する</span><span class="sxs-lookup"><span data-stu-id="7f062-433">Process a customer invoice by using custom ER configurations</span></span>

### <a name="select-and-send-a-posted-invoice"></a><span data-ttu-id="7f062-434">転記された請求書を選択して送信する</span><span class="sxs-lookup"><span data-stu-id="7f062-434">Select and send a posted invoice</span></span>

1. <span data-ttu-id="7f062-435">**売掛金勘定** \> **請求書** \> **すべての自由書式の請求書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-435">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="7f062-436">**自由書式の請求書** ページで、前述の手順で追加して転記した請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-436">On the **Free text invoice** page, select the invoice that you previously added and posted.</span></span>
3. <span data-ttu-id="7f062-437">アクション ペインの **ドキュメント** グループで、**送信** \> **原本** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-437">On the Action Pane, in the **Document** group, select **Send** \> **Original**.</span></span>
4. <span data-ttu-id="7f062-438">**自由書式の請求書**  ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-438">Close the **Free text invoice** page.</span></span>

### <a name="analyze-a-generated-e-invoice"></a><span data-ttu-id="7f062-439">生成された電子請求書の分析</span><span class="sxs-lookup"><span data-stu-id="7f062-439">Analyze a generated e-invoice</span></span>

1. <span data-ttu-id="7f062-440">**組織管理** \> **電子申告** \> **電子申告ジョブ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-440">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>
2. <span data-ttu-id="7f062-441">**電子申告ジョブ** ページで、タスクの説明に **eInvoice XML を送信する** がある最新のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-441">On the **Electronic reporting jobs** page, select the latest record that has the task description **Send the eInvoice XML**.</span></span>
3. <span data-ttu-id="7f062-442">**ファイルの表示** を選択 すると、生成されたファイルの一覧にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7f062-442">Select **Show files** to access the list of generated files.</span></span>
4. <span data-ttu-id="7f062-443">**開く** を選択して、生成された電子請求書の XML ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7f062-443">Select **Open** to download the e-invoice XML file that is generated.</span></span>
5. <span data-ttu-id="7f062-444">電子請求書の XML ファイルを分析します。</span><span class="sxs-lookup"><span data-stu-id="7f062-444">Analyze the e-invoice XML file.</span></span> <span data-ttu-id="7f062-445">カスタマイズに従って、顧客税スキーマには、**schemeID** と **schemeAgencyID** の XML 属性に加えて、カスタマイズした **FederalTaxID** XML属性が含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-445">Notice that, in accordance with your customization, the customer tax schema includes the custom **FederalTaxID** XML attribute in addition to the **schemeID** and **schemeAgencyID** XML attributes.</span></span> <span data-ttu-id="7f062-446">この新しい XML 属性の値は、請求先に入力された 連邦税ID **LITWARE-6789** によって指定されます。</span><span class="sxs-lookup"><span data-stu-id="7f062-446">The value of this new XML attribute is specified by the **LITWARE-6789** federal tax ID that was entered for an invoiced customer.</span></span>

    ![カスタマイズして生成された e-インボイス XMLファイルのプレビュー](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a><span data-ttu-id="7f062-448">標準的な ER 構成の最新のバージョンをインポートする</span><span class="sxs-lookup"><span data-stu-id="7f062-448">Import the latest versions of standard ER configurations</span></span>

<span data-ttu-id="7f062-449">標準の ER 設定のセットを財務インスタンスを[最新](general-electronic-reporting-manage-configuration-lifecycle.md)に保持するには、そのインスタンスに設定されたER [リポジトリ](general-electronic-reporting.md#Repository)で利用できるようになるたびに、新しいバージョンをインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-449">To keep the set of standard ER configurations in your Finance instance [up to date](general-electronic-reporting-manage-configuration-lifecycle.md), you must import new versions of them whenever they become available in the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="7f062-450">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-450">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7f062-451">**ローカライズ コンフィグレーション** ページの **コンフィギュレーション プロバイダー** セクションで、**Microsoft** タイルを選択し、**リポジトリ** を選択して Microsoft プロバイダーのリポジトリの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="7f062-451">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="7f062-452">**コンフィギュレーション リポジトリ** ページで、**グローバル** タイプのリポジトリを選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-452">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="7f062-453">Regulatory Configuration Service に接続するために承認を求める場合は、その承認の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="7f062-453">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="7f062-454">**構成リポジトリ** ページにて、ウィンドウの左側の構成ツリーで、**Peppol 売上請求書** 形式の構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-454">On the **Configuration repository** page, in the configuration tree in the left pane, select the **Peppol Sales Invoice** format configuration.</span></span>
5. <span data-ttu-id="7f062-455">**バージョン** クイックタブで、PEPPOL BIS 3形式の顧客電子請求書をサポートするためにリリースされた ER 形式構成のバージョン **32.6.7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-455">On the **Versions** FastTab, select version **32.6.7** of the selected ER format configuration that has been released to support customer electronic invoices in PEPPOL BIS 3 format.</span></span> <span data-ttu-id="7f062-456">詳細については、[KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-456">For more information, see [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).</span></span>
6. <span data-ttu-id="7f062-457">**インポート** を選択して、グローバル リポジトリから現在の Finance インスタンスに選択したバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7f062-457">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![構成リポジトリ ページにおける、選択されたバージョン 32.6.7](./media/er-quick-start3-import-solution2.png)

<span data-ttu-id="7f062-459">このプロセスを自動化する方法の詳細については、[ER 構成の更新されたバージョンをインポートする](er-download-updated-versions-global-repo.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-459">For information about how this process can be automated, see [Import updated versions of ER configurations](er-download-updated-versions-global-repo.md).</span></span>

### <a name="review-the-imported-er-configurations"></a><span data-ttu-id="7f062-460"> インポートされた ER コンフィギュレーションのレビュー</span><span class="sxs-lookup"><span data-stu-id="7f062-460">Review the imported ER configurations</span></span>

1. <span data-ttu-id="7f062-461">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-461">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7f062-462">**ローカライズ構成** ページの、**構成** セクションで、**レポート構成** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-462">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="7f062-463">**コンポーネントの構成** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="7f062-463">Expand the **Configuration components** FastTab.</span></span>
4. <span data-ttu-id="7f062-464">ウィンドウの左側にある構成ツリーで、**請求書モデル** を展開します。</span><span class="sxs-lookup"><span data-stu-id="7f062-464">In the configuration tree in the left pane, expand **Invoice model**.</span></span> <span data-ttu-id="7f062-465">インポートされた ER データモデル構成のいずれかが、**顧客請求書モデル** の名前が **請求書モデル** に変更されていることに確認します。</span><span class="sxs-lookup"><span data-stu-id="7f062-465">Notice that the name of **Customer invoice model** has been changed to **Invoice model** in one of the imported ER data model configurations.</span></span>
5. <span data-ttu-id="7f062-466">ウィンドウの左側にある構成ツリーで、**請求書モデル マッピング** を展開します。</span><span class="sxs-lookup"><span data-stu-id="7f062-466">In the configuration tree in the left pane, expand **Invoice model mapping**.</span></span> <span data-ttu-id="7f062-467">インポートされた ER モデル構成のいずれかで、**顧客請求書モデル マッピング** の名前が **請求書モデル マッピング** に変更されていることに確認します。</span><span class="sxs-lookup"><span data-stu-id="7f062-467">Notice that the name of **Customer invoice model mapping** has been changed to **Invoice model mapping** in one of the imported ER model mapping configurations.</span></span>
6. <span data-ttu-id="7f062-468">**UBL 売上請求書** \> **Peppol 売上請求書** を展開します。</span><span class="sxs-lookup"><span data-stu-id="7f062-468">Expand **UBL Sales invoice** \> **Peppol Sales Invoice**.</span></span>

<span data-ttu-id="7f062-469">選択した **Peppol 売上請求書** ER 形式に加えて、その他の必要な ER 構成の最新バージョンがインポートされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-469">Notice that, in addition to the selected **Peppol Sales Invoice** ER format, the latest versions of other required ER configurations were imported.</span></span> <span data-ttu-id="7f062-470">新しいバージョンの ER の構成は、新しい要件に準拠する ER ソリューションを維持するためにグローバル リポジトリと LCS に常に公開されているため、必要な データ モデル構成の最新バージョンとその モデル マッピングの構成がインポートされます。</span><span class="sxs-lookup"><span data-stu-id="7f062-470">Because new versions of ER configurations are constantly published to the Global repository and LCS to keep the corresponding ER solutions compliant with new requirements, the latest versions of the required data model configuration and its model mapping configurations were imported.</span></span>

<span data-ttu-id="7f062-471">構成ツリーで、最終的に以下の ER 構成が利用可能となるように設定をしてください :</span><span class="sxs-lookup"><span data-stu-id="7f062-471">Make sure that the following ER configurations are eventually available in the configuration tree:</span></span>

- <span data-ttu-id="7f062-472">**請求書モデル** ER データ モデルの構成 :</span><span class="sxs-lookup"><span data-stu-id="7f062-472">**Invoice model** ER data model configuration:</span></span>

    - <span data-ttu-id="7f062-473">バージョン 206 (またはそれ以降) には、請求書発行ビジネス ドメインのデータ構造を表すデータモデル ER コンポーネントのバージョン 24 (またはそれ以降) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f062-473">Version 206 (or later) contains version 24 (or later) of the data model ER component that represents the data structure of the invoicing business domain.</span></span> <span data-ttu-id="7f062-474">この ER 構成は、最新版の **請求書モデル マッピング**  ER モデル マッピング構成の原型としてインポートされています。</span><span class="sxs-lookup"><span data-stu-id="7f062-474">This ER configuration has been imported as an ancestor of the latest available **Invoice model mapping** ER model mapping configuration.</span></span>

    ![構成ページにおけるバージョン 206](./media/er-quick-start3-imported-solution2b1.png)

- <span data-ttu-id="7f062-476">**請求書 モデル マッピング** ER モデル マッピングの構成 :</span><span class="sxs-lookup"><span data-stu-id="7f062-476">**Invoice model mapping** ER model mapping configuration:</span></span>

    - <span data-ttu-id="7f062-477">**請求書モデル** ER データ モデルの構成バージョン 206 の最新実装として、バージョン206.132 (またはそれ以降) がインポートされています。</span><span class="sxs-lookup"><span data-stu-id="7f062-477">Version 206.132 (or later) has been imported as the latest implementation of version 206 of the **Invoice model** ER data model configuration.</span></span> <span data-ttu-id="7f062-478">これには、実行時にデータモデルがどのようにアプリケーションデータで格納されるかを記述した、複数のモデル マッピングERコンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f062-478">It contains several model mapping ER components that describe how the data model is filled in with application data at runtime.</span></span>

    ![構成ページにおけるバージョン 206.132](./media/er-quick-start3-imported-solution2b2.png)

- <span data-ttu-id="7f062-480">**UBL 売上請求書** ER 形式の構成 :</span><span class="sxs-lookup"><span data-stu-id="7f062-480">**UBL Sales invoice** ER format configuration:</span></span>

    - <span data-ttu-id="7f062-481">バージョン 32.6 には、形式と形式マッピング ER のコンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f062-481">Version 32.6 contains the format and format mapping ER components.</span></span> <span data-ttu-id="7f062-482">形式コンポーネントは、レポートのレイアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="7f062-482">The format component specifies the report layout.</span></span> <span data-ttu-id="7f062-483">形式マッピング コンポーネントは、モデル データ ソースが含まれており、このデータ ソースが実行時にレポート レイアウトを埋めるためにどのように使用されるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7f062-483">The format mapping component contains the model data source and specifies how this data source is used to fill in the report layout at runtime.</span></span> <span data-ttu-id="7f062-484">この ER 形式は、電子インボイスを UBL 形式で生成するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="7f062-484">This ER format was configured to generate e-invoices in UBL format.</span></span> <span data-ttu-id="7f062-485">この ER 構成は、インポート対象として選択された **Peppol 売り上げ請求書** の ER 形式の親としてインポートされました。</span><span class="sxs-lookup"><span data-stu-id="7f062-485">It has been imported as a parent of the **Peppol Sales Invoice** ER format that was selected for import.</span></span>

- <span data-ttu-id="7f062-486">**Peppol 売上請求書** ER 形式の構成 :</span><span class="sxs-lookup"><span data-stu-id="7f062-486">**Peppol Sales Invoice** ER format configuration:</span></span>

    - <span data-ttu-id="7f062-487">バージョン 32.6.7 には、PEPPOL フォーマットで電子インボイスを生成するように構成された形式と形式マッピング ER コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f062-487">Version 32.6.7 contains the format and format mapping ER components that were configured to generate e-invoices in PEPPOL format.</span></span>

    ![構成ページにおけるバージョン 32.6.7](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a><span data-ttu-id="7f062-489">カスタマイズした ER の構成に新しいバージョンの標準的な ER の構成に変更を適用する</span><span class="sxs-lookup"><span data-stu-id="7f062-489">Adopt the changes to the new standard ER configurations in your custom ER configurations</span></span>

### <a name="adopt-your-custom-er-data-model"></a><span data-ttu-id="7f062-490">カスタム ER データモデルの採用</span><span class="sxs-lookup"><span data-stu-id="7f062-490">Adopt your custom ER data model</span></span>

1. <span data-ttu-id="7f062-491">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-491">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7f062-492">**構成** ページの左側ペインの構成ツリーで、**請求書モデル** を展開し、**請求書モデル (Litware)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-492">On the **Configurations** page, in the configuration tree in the left pane, expand **Invoice model**, and select **Invoice model (Litware)**.</span></span>
3. <span data-ttu-id="7f062-493">**バージョン**  クイック タブで、選択されたデータモデル構成のドラフトバージョン **50.2** に対して **リベース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-493">On the **Versions** FastTab, for draft version **50.2** of the selected data model configuration, select **Rebase**.</span></span>
4. <span data-ttu-id="7f062-494">**ターゲット バージョン** フィールドで、基本 ER デー タモデル構成のバージョン **206** が選択されていることを確認し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-494">In the **Target version** field, confirm the selection of version **206** of the base ER data model configuration, and then select **OK**.</span></span>

    <span data-ttu-id="7f062-495">カスタム ER データ モデル構成のドラフト版の番号が **50.2** から **206.2** に変更され、基本 ER データ モデル構成の最新バージョン (206) の変更とマージされたカスタマイズが含まれていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="7f062-495">The draft version of your custom ER data model configuration is renumbered from **50.2** to **206.2** to indicate that it now contains your customization that was merged with the changes in the latest version (206) of the base ER data model configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f062-496">リベース アクションを元に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-496">The rebase action is reversible.</span></span> <span data-ttu-id="7f062-497">このリベースをキャンセルするには、**バージョン** クイックタブで **請求書モデル (Litware)** のバージョン **50.1** を選び、**このバージョンを取得する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-497">To cancel this rebase, select version **50.1** of the **Invoice model (Litware)** model on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="7f062-498">バージョン 206.2 は **50.2** に番号が振り直され、バージョン 50.2 のドラフトの内容はバージョン 50.1 の内容と一致します。</span><span class="sxs-lookup"><span data-stu-id="7f062-498">Version 206.2 will be renumbered back to **50.2**, and the content of draft version 50.2 will match the content of version 50.1.</span></span>

5. <span data-ttu-id="7f062-499">**バージョン** クイックタブで、**ステータスの変更** \> **完了済**、そして **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-499">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="7f062-500">バージョン 206.2 のステータスは、**ドラフト** から **完了済** に変更され、バージョンは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-500">The status of version 206.2 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="7f062-501">新しい編集可能なバージョン 206.3 が追加され、状態が **ドラフト** になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-501">A new editable version, 206.3, is added and has a status of **Draft**.</span></span> <span data-ttu-id="7f062-502">このバージョンを使用すると、カスタム ER データ モデルの構成にさらに変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-502">You can use this version to make further changes in your custom ER data model configuration.</span></span>

![構成ページで完了したバージョン 206.2](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a><span data-ttu-id="7f062-504">カスタム ER モデル マッピングの採用</span><span class="sxs-lookup"><span data-stu-id="7f062-504">Adopt your custom ER model mapping</span></span>

1. <span data-ttu-id="7f062-505">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-505">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7f062-506">**構成** ページの左側ペインの構成ツリーで、 **請求書モデル** \> **請求書モデル マッピング** を展開し、**請求書モデル マッピング (Litware)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-506">On the **Configurations** page, in the configuration tree in the left pane, expand **Invoice model** \> **Invoice model mapping**, and select **Invoice model mapping (Litware)**.</span></span>
3. <span data-ttu-id="7f062-507">**バージョン**  クイック タブで、選択されたモデル マッピング構成のドラフトバージョン **50.19.2** に対して **リベース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-507">On the **Versions** FastTab, for draft version **50.19.2** of the selected model mapping configuration, select **Rebase**.</span></span>
4. <span data-ttu-id="7f062-508">**ターゲット バージョン** フィールドで、基本 ER モデル マッピング構成のバージョン **206.132** が選択されていることを確認し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-508">In the **Target version** field, confirm the selection of version **206.132** of the base ER model mapping configuration, and then select **OK**.</span></span>

    <span data-ttu-id="7f062-509">カスタム ER データ モデル マッピング構成のドラフト版の番号が **50.19.2** から **206.132.2** に変更され、基本 ER モデル マッピング構成の最新バージョン (206.132) の変更とマージされたカスタマイズが含まれていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="7f062-509">The draft version of your custom ER model mapping configuration is renumbered from **50.19.2** to **206.132.2** to indicate that it now contains your customization that was merged with the changes in the latest version (206.132) of the base ER model mapping configuration.</span></span>

    <span data-ttu-id="7f062-510">一部のリベースの競合が検出されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f062-510">Notice that some rebase conflicts were discovered.</span></span> <span data-ttu-id="7f062-511">このような競合は手動で解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-511">You must now manually resolve those conflicts.</span></span>

    ![構成ページにおける競合メッセージのリベース](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. <span data-ttu-id="7f062-513">アクション ペインで **デザイナ** を選択 し、マッピングの一覧で **顧客請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-513">On the Action Pane, select **Designer**, and then, in the list of mappings, select **Customer Invoice**.</span></span>
6. <span data-ttu-id="7f062-514">それぞれのリベースの競合については、各コンポーネントに対してカスタム データ モデルのバージョン番号を保持する必要があるため、**独自の値を保持する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-514">For each rebase conflict, select **Retain own value**, because you must keep the version number of your custom data model for every component that has been mentioned.</span></span>

    ![モデル マッピング デザイナ ページにおける競合をリベースする](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. <span data-ttu-id="7f062-516">**保存** を選択し、**モデル マッピング デザイナ** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-516">Select **Save**, and then close the **Model mapping designer** page.</span></span>
8. <span data-ttu-id="7f062-517">マッピングの一覧で、 **プロジェクト請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-517">In the list of mappings, select **Project Invoice**.</span></span>
9. <span data-ttu-id="7f062-518">それぞれのリベースの競合については、各コンポーネントに対してカスタム データ モデルのバージョン番号を保持する必要があるため、**独自の値を保持する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-518">For each rebase conflict, select **Retain own value**, because you must keep the version number of your custom data model for every component that has been mentioned.</span></span>
10. <span data-ttu-id="7f062-519">**保存** を選択し、**モデル マッピング** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-519">Select **Save**, and then close the **Model mappings** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f062-520">リベース アクションを元に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-520">The rebase action is reversible.</span></span> <span data-ttu-id="7f062-521">このリベースをキャンセルするには、**バージョン** クイックタブで **請求書モデル マッピング (Litware)** のバージョン **50.19.1** を選び、**このバージョンを取得する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-521">To cancel this rebase, select version **50.19.1** of the **Invoice model mapping (Litware)** model mapping on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="7f062-522">バージョン 206.132.2 は **50.19.2** に番号が振り直され、バージョン 50.19.2 のドラフトの内容はバージョン 50.19.1 の内容と一致します。</span><span class="sxs-lookup"><span data-stu-id="7f062-522">Version 206.132.2 will be renumbered back to **50.19.2**, and the content of draft version 50.19.2 will match the content of version 50.19.1.</span></span>

11. <span data-ttu-id="7f062-523">**バージョン** クイックタブで、**ステータスの変更** \> **完了済**、そして **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-523">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="7f062-524">バージョン 206.132.2 のステータスは、**ドラフト** から **完了済** に変更され、バージョンは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-524">The status of version 206.132.2 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="7f062-525">新しい編集可能なバージョン 206.132.3 が追加され、状態が **ドラフト** になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-525">A new editable version, 206.132.3, is added and has a status of **Draft**.</span></span> <span data-ttu-id="7f062-526">このバージョンを使用すると、カスタム ER モデル マッピングの構成にさらに変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-526">You can use this version to make further changes in your custom ER model mapping configuration.</span></span>

![構成ページで完了したバージョン 206.132.2](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a><span data-ttu-id="7f062-528">カスタム ER フォーマットの採用</span><span class="sxs-lookup"><span data-stu-id="7f062-528">Adopt your custom ER format</span></span>

1. <span data-ttu-id="7f062-529">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-529">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7f062-530">**構成** ページの左側ペインの構成ツリーで、**請求書モデル** \> **UBL 売上請求書** \> **Peppol 売上請求書** を展開し、**Peppol 売上請求書 (Litware)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-530">On the **Configurations** page, in the configuration tree in the left pane, expand **Invoice model** \> **UBL Sales invoice** \> **Peppol Sales Invoice**, and select **Peppol Sales Invoice (Litware)**.</span></span>
3. <span data-ttu-id="7f062-531">**バージョン**  クイック タブで、選択された形式の構成ドラフト バージョン **11.2.2.2** に対して **リベース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-531">On the **Versions** FastTab, for draft version **11.2.2.2** of the selected format configuration, select **Rebase**.</span></span>
4. <span data-ttu-id="7f062-532">**ターゲット** バージョン フィールドで、基本 ER 形式の構成のバージョン **32.6.7** が選択されていることを確認し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-532">In the **Target** version field, confirm the selection of version **32.6.7** of the base ER format configuration, and then select **OK**.</span></span>

    <span data-ttu-id="7f062-533">カスタム ER 形式構成のドラフト バージョンの番号が **11.2.2.2** から **32.6.7.2** に変更され、基本 ER 形式構成の最新バージョン (32.6.7) の変更とマージされたカスタマイズが含まれていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="7f062-533">The draft version of your custom ER format configuration is renumbered from **11.2.2.2** to **32.6.7.2** to indicate that it now contains your customization that was merged with the changes in the latest version (32.6.7) of the base ER format configuration.</span></span>

    <span data-ttu-id="7f062-534">一部のリベースの競合が検出されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f062-534">Notice that some rebase conflicts were discovered.</span></span> <span data-ttu-id="7f062-535">このような競合は手動で解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f062-535">You must now manually resolve those conflicts.</span></span>

5. <span data-ttu-id="7f062-536">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-536">On the Action Pane, select **Designer**.</span></span>
6. <span data-ttu-id="7f062-537">それぞれのリベースの競合については、各コンポーネントに対してカスタム データ モデルのバージョン番号を保持する必要があるため、**独自の値を保持する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-537">For each rebase conflict, select **Retain own value**, because you must keep the version number of your custom data model for every component that has been mentioned.</span></span>
7. <span data-ttu-id="7f062-538">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-538">Select **Save**.</span></span>
8. <span data-ttu-id="7f062-539">**マッピング** タブで、**モデル** タイプの **インボイス** データ ソースを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-539">On the **Mapping** tab, select the **Invoice** data source of the **Model** type, and then select **Edit**.</span></span>
9. <span data-ttu-id="7f062-540">**バージョン** フィールドで、カスタム データモデルのバージョン **2** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-540">In the **Version** field, select version **2** of your custom data model, and then select **OK**.</span></span>
10. <span data-ttu-id="7f062-541">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-541">Select **Save**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f062-542">リベース アクションを元に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-542">The rebase action is reversible.</span></span> <span data-ttu-id="7f062-543">このリベースをキャンセルするには、**バージョン** クイックタブで **Peppol 売上請求書 (Litware)** 形式のバージョン **11.2.2.1** を選び、**このバージョンを取得する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-543">To cancel this rebase, select version **11.2.2.1** of the **Peppol Sales Invoice (Litware)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="7f062-544">バージョン 32.6.7.2 は **11.2.2.2** に番号が振り直され、バージョン 11.2.2.2 のドラフトの内容はバージョン 11.2.2.1 の内容と一致します。</span><span class="sxs-lookup"><span data-stu-id="7f062-544">Version 32.6.7.2 will be renumbered back to **11.2.2.2**, and the content of draft version 11.2.2.2 will match the content of version 11.2.2.1.</span></span>

11. <span data-ttu-id="7f062-545">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-545">Close the **Format designer** page.</span></span>
12. <span data-ttu-id="7f062-546">**バージョン** クイックタブで、**ステータスの変更** \> **完了済**、そして **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-546">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="7f062-547">バージョン 32.6.7.2 のステータスは、**ドラフト** から **完了済** に変更され、バージョンは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-547">The status of version 32.6.7.2 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="7f062-548">新しい編集可能なバージョン 32.6.7.3 が追加され、状態が **ドラフト** になります。</span><span class="sxs-lookup"><span data-stu-id="7f062-548">A new editable version, 32.6.7.3, is added and has a status of **Draft**.</span></span> <span data-ttu-id="7f062-549">このバージョンを使用すると、カスタム ER 形式の構成に追加の変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="7f062-549">You can use this version to make further changes in your custom ER format configuration.</span></span>

![構成ページで完了したバージョン 32.6.7.2](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a><span data-ttu-id="7f062-551">新しいバージョンの カスタマイズした ER の構成を使用して、顧客請求書を処理する</span><span class="sxs-lookup"><span data-stu-id="7f062-551">Process a customer invoice by using new versions of the custom ER configurations</span></span>

### <a name="select-and-send-a-posted-invoice"></a><span data-ttu-id="7f062-552">転記された請求書を選択して送信する</span><span class="sxs-lookup"><span data-stu-id="7f062-552">Select and send a posted invoice</span></span>

1. <span data-ttu-id="7f062-553">**売掛金勘定** \> **請求書** \> **すべての自由書式の請求書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f062-553">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="7f062-554">**自由書式の請求書** ページで、前述の手順で追加して転記した請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-554">On the **Free text invoice** page, select the invoice that you previously added and posted.</span></span>
3. <span data-ttu-id="7f062-555">アクション ペインの **ドキュメント** グループで、**送信** \> **原本** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-555">On the Action Pane, in the **Document** group, select **Send** \> **Original**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="7f062-556">この時点では、**Peppol 売上請求書 (Litware)** ER 形式の設定には 2 つのバージョンがあり、どちらのバージョンにも [有効日](general-electronic-reporting.md#component-date-effectivity) の値がないため、最新のバージョンを使用して電子請求書を作成しています。</span><span class="sxs-lookup"><span data-stu-id="7f062-556">Because you now have two versions of the **Peppol Sales Invoice (Litware)** ER format configuration, and neither version has an [effective date](general-electronic-reporting.md#component-date-effectivity) value, the latest version is used to generate an e-invoice.</span></span>

4. <span data-ttu-id="7f062-557">**自由書式の請求書**  ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7f062-557">Close the **Free text invoice** page.</span></span>

### <a name="analyze-a-generated-e-invoice"></a><span data-ttu-id="7f062-558">生成された電子請求書の分析</span><span class="sxs-lookup"><span data-stu-id="7f062-558">Analyze a generated e-invoice</span></span>

1. <span data-ttu-id="7f062-559">**組織管理** \> **電子申告** \> **電子申告ジョブ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-559">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>
2. <span data-ttu-id="7f062-560">**電子申告ジョブ** ページで、タスクの説明に **eInvoice XML を送信する** がある直近のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f062-560">On the **Electronic reporting jobs** page, select the most recent record that has the task description **Send the eInvoice XML**.</span></span>
3. <span data-ttu-id="7f062-561">**ファイルの表示** を選択 すると、生成されたファイルの一覧にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7f062-561">Select **Show files** to access the list of generated files.</span></span>
4. <span data-ttu-id="7f062-562">**開く** を選択して、生成された電子請求書の XML ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7f062-562">Select **Open** to download the e-invoice XML file that is generated.</span></span>
5. <span data-ttu-id="7f062-563">電子請求書の XML ファイルを分析します。</span><span class="sxs-lookup"><span data-stu-id="7f062-563">Analyze the e-invoice XML file.</span></span> <span data-ttu-id="7f062-564">カスタマイズに従って、顧客税スキーマには、**schemeID** と **schemeAgencyID** の XML 属性に加えて、カスタマイズした **FederalTaxID** XML 属性が含まれていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7f062-564">Notice that, in accordance with your customization, the customer tax schema still contains the custom **FederalTaxID** XML attribute in addition to the **schemeID** and **schemeAgencyID** XML attributes.</span></span> <span data-ttu-id="7f062-565">また、ベースとなる新しいバージョンの **UBL 売上請求書** 形式の変更点が、カスタマイズしたものにマージされたため、 XML要素 **cbc:CustomizationID** のテキストが `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` から `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0` に変更されています。</span><span class="sxs-lookup"><span data-stu-id="7f062-565">Additionally, because the changes in the new version of the base **UBL Sales invoice** format were merged with your customization, the text of the **cbc:CustomizationID** XML element has been changed from `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` to `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`.</span></span>

    ![カスタマイズして生成された e-インボイス XML ファイルのプレビュー](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a><span data-ttu-id="7f062-567">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7f062-567">Additional resources</span></span>

- [<span data-ttu-id="7f062-568">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="7f062-568">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="7f062-569">ER コンフィギュレーションを Lifecycle Services からダウンロードする</span><span class="sxs-lookup"><span data-stu-id="7f062-569">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="7f062-570">ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする</span><span class="sxs-lookup"><span data-stu-id="7f062-570">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
- [<span data-ttu-id="7f062-571">自由書式の請求書の作成</span><span class="sxs-lookup"><span data-stu-id="7f062-571">Create a free text invoice</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/create-free-text-invoice-new)
- [<span data-ttu-id="7f062-572">カスタム フィールドの作成と操作</span><span class="sxs-lookup"><span data-stu-id="7f062-572">Create and work with custom fields</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields)

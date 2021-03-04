---
title: オーストラリアのキャッシュ レジスターの配置ガイドライン
description: このトピックは、オーストリアのローカライズ用配置ガイドです。
author: AlexChern0v
manager: ezubov
ms.date: ''
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Austria
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2022b24a87136f332542cbfd66099ecf75cf20da
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985938"
---
# <a name="deployment-guidelines-for-cash-registers-for-austria"></a><span data-ttu-id="f9b16-103">オーストラリアのキャッシュ レジスターの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="f9b16-103">Deployment guidelines for cash registers for Austria</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f9b16-104">このトピックは、Dynamics 365 Commerce のオーストラリアでのローカライズを有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="f9b16-104">This topic is a deployment guide that shows how to enable the Dynamics 365 Commerce localization for Austria.</span></span> <span data-ttu-id="f9b16-105">ローカライズは、コマース コンポーネントのいくつかの拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-105">The localization consists of several extensions of Commerce components.</span></span> <span data-ttu-id="f9b16-106">たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷し、追加の監査イベントを登録し、EFSTA システムと Electronical 会計登録ソフトウェアとの統合サンプルを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-106">For example, the extensions let you print custom fields on receipts, register additional audit events, includes samples of the integration with the EFSTA System and Electronical Fiscal Register Software.</span></span> <span data-ttu-id="f9b16-107">オーストリアのローカライズの詳細については、[オーストリアの会計登録サービス統合サンプル](./emea-aut-fi-sample.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9b16-107">For more information about the localization for Austria, see [Fiscal registration service integration sample for Austria](./emea-aut-fi-sample.md).</span></span>

<span data-ttu-id="f9b16-108">統合サンプルは、会計統合フレームワークに基づいて作成されました。</span><span class="sxs-lookup"><span data-stu-id="f9b16-108">Integration samples were developed based on the fiscal integration framework.</span></span> <span data-ttu-id="f9b16-109">会計統合機能の詳細については、 [コマース チャネルの財政統合の概要](fiscal-integration-for-retail-channel.md) を参照してください。これらのサンプルは、市販ソフトウェア開発キット (SDK)の一部です。</span><span class="sxs-lookup"><span data-stu-id="f9b16-109">For details about the fiscal integration functionality, see [Overview of fiscal integration for Commerce channels](fiscal-integration-for-retail-channel.md), these samples are part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="f9b16-110">SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9b16-110">For information about how to install and use the SDK, see the [Retail software development kit (SDK) architecture](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="f9b16-111">このローカライズは、Commerce runtime (CRT)、ハードウェア ステーション、および POS の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-111">This localization consists of extensions for the Commerce runtime (CRT), Hardware station, and POS.</span></span> <span data-ttu-id="f9b16-112">このサンプルを実行するには、CRT、ハードウェア ステーション、および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9b16-112">To run this sample, you must modify and build the CRT, Hardware station, and POS projects.</span></span> <span data-ttu-id="f9b16-113">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-113">We recommend that you use an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="f9b16-114">また Azure DevOps のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-114">We also recommend that you use a source control system, such as Azure DevOps, where no files have been changed yet.</span></span>

## <a name="development-environment"></a><span data-ttu-id="f9b16-115">開発環境</span><span class="sxs-lookup"><span data-stu-id="f9b16-115">Development environment</span></span>

<span data-ttu-id="f9b16-116">次の手順に従って開発環境を設定し、ローカライズ機能をテストし、拡張できるようにします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-116">Follow these steps to set up a development environment so that you can test and extend the localization functionality.</span></span>

### <a name="crt-extension-components"></a><span data-ttu-id="f9b16-117">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f9b16-117">CRT extension components</span></span>

<span data-ttu-id="f9b16-118">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-118">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="f9b16-119">次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-119">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

#### <a name="documentproviderefrsample-component"></a><span data-ttu-id="f9b16-120">DocumentProvider.EFRSample コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f9b16-120">DocumentProvider.EFRSample component</span></span>

1. <span data-ttu-id="f9b16-121">**Runtime.Extensions.DocumentProvider.EFRSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-121">Find the **Runtime.Extensions.DocumentProvider.EFRSample** project, and build it.</span></span>
2. <span data-ttu-id="f9b16-122">**Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-122">In the **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** assembly file.</span></span>
3. <span data-ttu-id="f9b16-123">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-123">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="f9b16-124">**Commerce Scale Unit:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Commerce Scale Unit のサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-124">**Commerce Scale Unit:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Commerce Scale Unit site location.</span></span>
    - <span data-ttu-id="f9b16-125">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-125">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="f9b16-126">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-126">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="f9b16-127">**Commerce Scale Unit:** ファイル名は **commerceruntime.ext.config** で、IIS Commerce Scale Unit サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="f9b16-127">**Commerce Scale Unit:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Commerce Scale Unit site location.</span></span>
    - <span data-ttu-id="f9b16-128">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="f9b16-128">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="f9b16-129">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-129">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a><span data-ttu-id="f9b16-130">DocumentProvider.DataModelEFR コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f9b16-130">DocumentProvider.DataModelEFR component</span></span>

1. <span data-ttu-id="f9b16-131">**Runtime.Extensions.DocumentProvider.DataModelEFR** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-131">Find the **Runtime.Extensions.DocumentProvider.DataModelEFR** project, and build it.</span></span>
2. <span data-ttu-id="f9b16-132">**Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-132">In the **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** assembly file.</span></span>
3. <span data-ttu-id="f9b16-133">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-133">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="f9b16-134">**Commerce Scale Unit:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Commerce Scale Unit のサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-134">**Commerce Scale Unit:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Commerce Scale Unit site location.</span></span>
    - <span data-ttu-id="f9b16-135">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-135">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="f9b16-136">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-136">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="f9b16-137">**Retail とコマース:** ファイル名は **commerceruntime.ext.config** で、IIS Retail とコマース サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="f9b16-137">**Retail and Commerce:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail and Commerce site location.</span></span>
    - <span data-ttu-id="f9b16-138">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="f9b16-138">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="f9b16-139">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-139">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="enable-microsoft-components"></a><span data-ttu-id="f9b16-140">Microsoft コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="f9b16-140">Enable Microsoft components</span></span>

1. <span data-ttu-id="f9b16-141">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-141">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="f9b16-142">**Commerce Scale Unit:** ファイル名は **commerceruntime.ext.config** で、IIS Commerce Scale Unit サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="f9b16-142">**Commerce Scale Unit:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Commerce Scale Unit site location.</span></span>
    - <span data-ttu-id="f9b16-143">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="f9b16-143">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="f9b16-144">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-144">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="hardware-station-extension-components"></a><span data-ttu-id="f9b16-145">ハードウェア ステーション拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f9b16-145">Hardware station extension components</span></span>

<span data-ttu-id="f9b16-146">ハードウェア ステーション拡張コンポーネントは、ハードウェア ステーション サンプルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="f9b16-146">The Hardware station extension components are included in the Hardware station samples.</span></span> <span data-ttu-id="f9b16-147">次の手順を完了するには、**RetailSdk\\SampleExtensions\\HardwareStation** にある、ソリューション、**HardwareStationSamples.sln.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-147">To complete the following procedures, open the solution, **HardwareStationSamples.sln.sln**, under **RetailSdk\\SampleExtensions\\HardwareStation**.</span></span>

#### <a name="efrsample-component"></a><span data-ttu-id="f9b16-148">EFRSample コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f9b16-148">EFRSample component</span></span>

1. <span data-ttu-id="f9b16-149">**HardwareStation.Extension.EFRSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-149">Find the **HardwareStation.Extension.EFRSample** project, and build it.</span></span>
2. <span data-ttu-id="f9b16-150">**Extension.EFRSample\\bin\\Debug** フォルダーで、以下のファイルを探します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-150">In the **Extension.EFRSample\\bin\\Debug** folder, find following files:</span></span>

    - <span data-ttu-id="f9b16-151">**Contoso.Commerce.HardwareStation.EFRSample.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="f9b16-151">The **Contoso.Commerce.HardwareStation.EFRSample.dll** assembly</span></span>
    - <span data-ttu-id="f9b16-152">**Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="f9b16-152">The **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** assembly</span></span>

3. <span data-ttu-id="f9b16-153">アセンブリ ファイルをハードウェア ステーション拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-153">Copy the assembly file to the Hardware station extensions folder:</span></span>

    - <span data-ttu-id="f9b16-154">**共有ハードウェア ステーション:** ファイルを、Microsoft インターネット インフォメーション サービス (IIS) ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-154">**Shared hardware station:** Copy the files to the **bin** folder under the Microsoft Internet Information Services (IIS) Hardware station site location.</span></span>
    - <span data-ttu-id="f9b16-155">**Modern POS の専用ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-155">**Dedicated hardware station on Modern POS:** Copy the files to the Modern POS client broker location.</span></span>

4. <span data-ttu-id="f9b16-156">拡張コンフィギュレーション ファイルのハードウェア ステーションの拡張機能の **HardwareStation.Extension.config** が見つかりません。</span><span class="sxs-lookup"><span data-stu-id="f9b16-156">Find the extension configuration file Hardware station's extensions **HardwareStation.Extension.config**:</span></span>

    - <span data-ttu-id="f9b16-157">**共有ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。</span><span class="sxs-lookup"><span data-stu-id="f9b16-157">**Shared hardware station:** The file is located under the IIS Hardware station site location.</span></span>
    - <span data-ttu-id="f9b16-158">**Modern POS の専用ハードウェア ステーション:** ファイルは、Modern POS クライアント ブローカーの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="f9b16-158">**Dedicated hardware station on Modern POS:** The file is located under the Modern POS client broker location.</span></span>

5. <span data-ttu-id="f9b16-159">コンフィギュレーション ファイルの **構成** セクションに、次のセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-159">Add the following section to the **composition** section of the config file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="modern-pos-extension-components"></a><span data-ttu-id="f9b16-160">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f9b16-160">Modern POS extension components</span></span>

1. <span data-ttu-id="f9b16-161">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-161">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="f9b16-162">また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-162">Additionally, make sure that you can run Modern POS from Microsoft Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9b16-163">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="f9b16-163">Modern POS must not be customized.</span></span> <span data-ttu-id="f9b16-164">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9b16-164">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

2. <span data-ttu-id="f9b16-165">**extensions.json** で、次の明細行を追加することによって拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-165">Enable the extensions to be loaded by adding the following lines in **extensions.json**:</span></span>

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > <span data-ttu-id="f9b16-166">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9b16-166">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

3. <span data-ttu-id="f9b16-167">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-167">Rebuild the solution.</span></span>
4. <span data-ttu-id="f9b16-168">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-168">Run Modern POS in the debugger, and test the functionality.</span></span>

### <a name="cloud-pos-extension-components"></a><span data-ttu-id="f9b16-169">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f9b16-169">Cloud POS extension components</span></span>

1. <span data-ttu-id="f9b16-170">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-170">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="f9b16-171">**extensions.json** で、次の明細行を追加することによって拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-171">Enable the extensions to be loaded by adding the following lines in **extensions.json**:</span></span>

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > <span data-ttu-id="f9b16-172">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9b16-172">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

3. <span data-ttu-id="f9b16-173">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-173">Rebuild the solution.</span></span>
4. <span data-ttu-id="f9b16-174">**実行** コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-174">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>

### <a name="set-up-required-parameters-in-headquarters"></a><span data-ttu-id="f9b16-175">バックオフィスで要求されるパラメーターを設定します</span><span class="sxs-lookup"><span data-stu-id="f9b16-175">Set up required parameters in Headquarters</span></span>

#### <a name="set-up-the-registration-process"></a><span data-ttu-id="f9b16-176">登録プロセスの設定</span><span class="sxs-lookup"><span data-stu-id="f9b16-176">Set up the registration process</span></span>

<span data-ttu-id="f9b16-177">登録プロセスを有効にするには、次の手順を使用してバックオフィスを設定します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-177">To enable the registration process, set up Headquarters using the steps below.</span></span> <span data-ttu-id="f9b16-178">詳細については、[コマース チャネルの会計統合の設定](./setting-up-fiscal-integration-for-retail-channel.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9b16-178">For more details, see [Set up the fiscal integration for Commerce channels](./setting-up-fiscal-integration-for-retail-channel.md).</span></span>

1. <span data-ttu-id="f9b16-179">**コマース共有パラメーター** を開き、**全般** タブで **会計統合** を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-179">Open **Commerce shared parameters** and enable **Fiscal integration** on the **General** tab.</span></span>
2. <span data-ttu-id="f9b16-180">**Retail とコマース \> チャネル設定 \> 会計統合 \> 会計コネクタ** メニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-180">Open **Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal connectors** menu.</span></span> <span data-ttu-id="f9b16-181">RetailSdk からコネクタ構成を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-181">Load connector configuration from RetailSdk.</span></span> <span data-ttu-id="f9b16-182">ファイルは、SampleExtensions\HardwareStation\Extension.EFRSample\Configuration\ConnectorEFRSampleAustria.xml の下に保存されています。</span><span class="sxs-lookup"><span data-stu-id="f9b16-182">The file is located under SampleExtensions\HardwareStation\Extension.EFRSample\Configuration\ConnectorEFRSampleAustria.xml.</span></span>
3. <span data-ttu-id="f9b16-183">**Retail とコマース \> チャネル設定 \> 会計統合 \> 会計ドキュメント プロバイダー** メニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-183">Open **Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal document providers** menu.</span></span> <span data-ttu-id="f9b16-184">RetailSdk からドキュメント プロバイダー コンフィギュレーションを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-184">Load documment provider configurations from RetailSdk.</span></span>

    <span data-ttu-id="f9b16-185">コンフィギュレーション ファイルは **SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration** の下にあります:</span><span class="sxs-lookup"><span data-stu-id="f9b16-185">Configuration files are located under **SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration**:</span></span>

    - <span data-ttu-id="f9b16-186">DocumentProviderEFRSampleAustria.xml</span><span class="sxs-lookup"><span data-stu-id="f9b16-186">DocumentProviderEFRSampleAustria.xml</span></span>
    - <span data-ttu-id="f9b16-187">DocumentProviderNonFiscalEFRSampleAustria.xml</span><span class="sxs-lookup"><span data-stu-id="f9b16-187">DocumentProviderNonFiscalEFRSampleAustria.xml</span></span>

4. <span data-ttu-id="f9b16-188">**Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ機能プロファイル** を開きます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-188">Open **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector functional profiles**.</span></span> <span data-ttu-id="f9b16-189">上記の手順からドキュメント プロバイダーごとに 2 つの新しいプロファイルを作成し、読み込まれたコネクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-189">Create two new profiles per document provider from step above and select the loaded connector.</span></span> <span data-ttu-id="f9b16-190">必要な場合は、データ マッピング設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-190">Update data mapping settings if needed.</span></span>
5. <span data-ttu-id="f9b16-191">**Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ技術プロファイル** を開きます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-191">Open **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector technical profiles**.</span></span> <span data-ttu-id="f9b16-192">上記の手順から新しいプロファイルを作成し、読み込まれたコネクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-192">Create a new profile and select the loaded connector from the step above.</span></span> <span data-ttu-id="f9b16-193">必要な場合は、接続設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-193">Update connection settings if needed.</span></span>
6. <span data-ttu-id="f9b16-194">**Retail とコマース \> チャネル設定 \> 会計統合 \> 会計コネクタ グループ** を開きます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-194">Open **Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal connector group**.</span></span> <span data-ttu-id="f9b16-195">上記の手順からコネクタの機能プロファイルごとに 2 つの新しいグループを作成します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-195">Create two new group per connector's functional profile from the step above.</span></span>
7. <span data-ttu-id="f9b16-196">**Retail とコマース \> チャネル設定 \> 会計統合 \> 登録プロセス** を開きます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-196">Open **Retail and Commerce \> Channel setup \> Fiscal integration \> Registration process**.</span></span> <span data-ttu-id="f9b16-197">新しいプロセスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-197">Create a new process.</span></span> <span data-ttu-id="f9b16-198">上記の手順から両方のコネクタの機能グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-198">Select both connector's functional groups from the step above.</span></span>
8. <span data-ttu-id="f9b16-199">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル** を開きます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-199">Open **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**.</span></span> <span data-ttu-id="f9b16-200">登録プロセスを有効化する、店舗にリンクされているプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-200">Select one that is linked to the store where the registration process should be activated.</span></span> <span data-ttu-id="f9b16-201">**会計登録プロセス** タブを展開します。上記の手順から作成された登録プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-201">Expand the **Fiscal registration process** tab. Select the created registration process from the step above.</span></span> <span data-ttu-id="f9b16-202">POS で非会計イベントの登録を有効にするには、**機能** クイック タブで **監査** プロパティを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f9b16-202">For enabling registration of non-fiscal events on POS enable **Audit** property at **Functions** fasttab.</span></span>
9. <span data-ttu-id="f9b16-203">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** を開きます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-203">Open the **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span> <span data-ttu-id="f9b16-204">会計プリンターの接続先のハードウェア ステーションにリンクされているプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-204">Select one that is linked to the hardware station to which the fiscal printer will be connected.</span></span> <span data-ttu-id="f9b16-205">**会計周辺機器** を展開します。コネクタの技術的なプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-205">Expand the **Fiscal peripherals** Tab. Select the connector technical profile.</span></span>

<span data-ttu-id="f9b16-206">詳細については、[オーストリアの会計登録サービス統合サンプル](./emea-aut-fi-sample.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9b16-206">For more information, see [Fiscal registration service integration sample for Austria](./emea-aut-fi-sample.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="f9b16-207">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="f9b16-207">Production environment</span></span>

<span data-ttu-id="f9b16-208">以下の手順に従い、コマース コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-208">Follow these steps to create deployable packages that contain Commerce components, and to apply those packages in a production environment.</span></span>

1. <span data-ttu-id="f9b16-209">[クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-209">Complete the steps in the [Cloud POS extension components](#cloud-pos-extension-components) or [Modern POS extension components](#modern-pos-extension-components) section earlier in this topic.</span></span>
2. <span data-ttu-id="f9b16-210">**RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-210">Make the following changes in the package configuration files under the **RetailSdk\\Assets** folder:</span></span>

    1. <span data-ttu-id="f9b16-211">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの **構成** セクションに、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-211">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files, add the following lines to the **composition** section:</span></span>

        ```xml  
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    2. <span data-ttu-id="f9b16-212">**HardwareStation.Extension.config** 構成ファイルで、**合成** セクションに追加の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-212">In the **HardwareStation.Extension.config** configuration file, add the following lines to the **composition** section.</span></span>

        ```xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. <span data-ttu-id="f9b16-213">**BuildTools\Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="f9b16-213">Make the following changes in the **BuildTools\Customization.settings** package customization configuration file:</span></span>

    ```xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
    <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
    <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
    ```

4. <span data-ttu-id="f9b16-214">Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-214">Start the MSBuild Command Prompt for Visual Studio utility, and run **msbuild** under the Retail SDK folder to create deployable packages.</span></span>
5. <span data-ttu-id="f9b16-215">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="f9b16-215">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="f9b16-216">詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9b16-216">For more information, see [Create deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>
6. <span data-ttu-id="f9b16-217">[バックオフィスで要求されるパラメーターの設定](#set-up-required-parameters-in-headquarters) を完了します</span><span class="sxs-lookup"><span data-stu-id="f9b16-217">Complete the [Set up required parameters in Headquarters](#set-up-required-parameters-in-headquarters)</span></span>

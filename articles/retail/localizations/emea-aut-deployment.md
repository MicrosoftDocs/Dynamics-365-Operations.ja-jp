---
title: オーストラリアのキャッシュ レジスターの配置ガイドライン
description: このトピックは、オーストラリアの小売ローカライズ用配置ガイドです。
author: AlexChern0v
manager: ezubov
ms.date: ''
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.search.region: Austria
ms.search.industry: Retail
ms.author: v-alexec
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 03c551cb06d90be1b9a8f06c42791c28a2d007fe
ms.sourcegitcommit: 25c45428162194c5db8feb3ab53d8df9551b0301
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/05/2019
ms.locfileid: "2559796"
---
# <a name="deployment-guidelines-for-cash-registers-for-austria"></a><span data-ttu-id="d063a-103">オーストラリアのキャッシュ レジスターの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="d063a-103">Deployment guidelines for cash registers for Austria</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d063a-104">このトピックは、Dynamics 365 Retail のオーストラリアでのローカライズを有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="d063a-104">This topic is a deployment guide that shows how to enable the Dynamics 365 Retail localization for Austria.</span></span> <span data-ttu-id="d063a-105">ローカライズは、小売コンポーネントのいくつかの拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d063a-105">The localization consists of several extensions of Retail components.</span></span> <span data-ttu-id="d063a-106">たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷し、追加の監査イベントを登録し、EFSTA システムと Electronical 会計登録ソフトウェアとの統合サンプルを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d063a-106">For example, the extensions let you print custom fields on receipts, register additional audit events, includes samples of the integration with the EFSTA System and Electronical Fiscal Register Software.</span></span> <span data-ttu-id="d063a-107">オーストリアの小売ローカライズの詳細については、[オーストリアの会計登録サービス統合サンプル](./emea-aut-fi-sample.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d063a-107">For more information about the Retail localization for Austria, see [Fiscal registration service integration sample for Austria](./emea-aut-fi-sample.md).</span></span>

<span data-ttu-id="d063a-108">統合サンプルは、会計統合フレームワークに基づいて作成されました。</span><span class="sxs-lookup"><span data-stu-id="d063a-108">Integration samples were developed based on the fiscal integration framework.</span></span> <span data-ttu-id="d063a-109">会計統合機能に関する詳細は、[小売チャンネルの会計統合](fiscal-integration-for-retail-channel.md)を参照してください。これらのサンプルは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="d063a-109">For details about the fiscal integration functionality, see [Fiscal integration for Retail channel](fiscal-integration-for-retail-channel.md), these samples are part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="d063a-110">リテール SDK をダウンロードして使用する方法については、[リテール SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d063a-110">For information about how to install and use the Retail SDK, see the [Retail SDK documentation](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="d063a-111">このローカライズは、Commerce runtime (CRT)、ハードウェア ステーション、および POS の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d063a-111">This localization consists of extensions for the Commerce runtime (CRT), Hardware station, and POS.</span></span> <span data-ttu-id="d063a-112">このサンプルを実行するには、CRT、ハードウェア ステーション、および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d063a-112">To run this sample, you must modify and build the CRT, Hardware station, and POS projects.</span></span> <span data-ttu-id="d063a-113">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d063a-113">We recommend that you use an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="d063a-114">また Azure DevOps のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d063a-114">We also recommend that you use a source control system, such as Azure DevOps, where no files have been changed yet.</span></span>

## <a name="development-environment"></a><span data-ttu-id="d063a-115">開発環境</span><span class="sxs-lookup"><span data-stu-id="d063a-115">Development environment</span></span>

<span data-ttu-id="d063a-116">次の手順に従って開発環境を設定し、ローカライズ機能をテストし、拡張できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d063a-116">Follow these steps to set up a development environment so that you can test and extend the localization functionality.</span></span>

### <a name="crt-extension-components"></a><span data-ttu-id="d063a-117">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d063a-117">CRT extension components</span></span>

<span data-ttu-id="d063a-118">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d063a-118">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="d063a-119">次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d063a-119">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

#### <a name="documentproviderefrsample-component"></a><span data-ttu-id="d063a-120">DocumentProvider.EFRSample コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d063a-120">DocumentProvider.EFRSample component</span></span>

1. <span data-ttu-id="d063a-121">**Runtime.Extensions.DocumentProvider.EFRSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="d063a-121">Find the **Runtime.Extensions.DocumentProvider.EFRSample** project, and build it.</span></span>
2. <span data-ttu-id="d063a-122">**Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="d063a-122">In the **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** assembly file.</span></span>
3. <span data-ttu-id="d063a-123">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d063a-123">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="d063a-124">**Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d063a-124">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail Server site location.</span></span>
    - <span data-ttu-id="d063a-125">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d063a-125">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="d063a-126">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="d063a-126">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="d063a-127">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="d063a-127">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="d063a-128">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="d063a-128">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="d063a-129">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="d063a-129">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a><span data-ttu-id="d063a-130">DocumentProvider.DataModelEFR コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d063a-130">DocumentProvider.DataModelEFR component</span></span>

1. <span data-ttu-id="d063a-131">**Runtime.Extensions.DocumentProvider.DataModelEFR** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="d063a-131">Find the **Runtime.Extensions.DocumentProvider.DataModelEFR** project, and build it.</span></span>
2. <span data-ttu-id="d063a-132">**Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="d063a-132">In the **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** assembly file.</span></span>
3. <span data-ttu-id="d063a-133">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d063a-133">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="d063a-134">**Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d063a-134">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail Server site location.</span></span>
    - <span data-ttu-id="d063a-135">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d063a-135">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="d063a-136">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="d063a-136">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="d063a-137">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="d063a-137">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="d063a-138">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="d063a-138">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="d063a-139">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="d063a-139">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="enable-microsoft-components"></a><span data-ttu-id="d063a-140">Microsoft コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="d063a-140">Enable Microsoft components</span></span>

1. <span data-ttu-id="d063a-141">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="d063a-141">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="d063a-142">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="d063a-142">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="d063a-143">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="d063a-143">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="d063a-144">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="d063a-144">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="hardware-station-extension-components"></a><span data-ttu-id="d063a-145">ハードウェア ステーション拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d063a-145">Hardware station extension components</span></span>

<span data-ttu-id="d063a-146">ハードウェア ステーション拡張コンポーネントは、ハードウェア ステーション サンプルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="d063a-146">The Hardware station extension components are included in the Hardware station samples.</span></span> <span data-ttu-id="d063a-147">次の手順を完了するには、**RetailSdk\\SampleExtensions\\HardwareStation** にある、ソリューション、**HardwareStationSamples.sln.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d063a-147">To complete the following procedures, open the solution, **HardwareStationSamples.sln.sln**, under **RetailSdk\\SampleExtensions\\HardwareStation**.</span></span>

#### <a name="efrsample-component"></a><span data-ttu-id="d063a-148">EFRSample コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d063a-148">EFRSample component</span></span>

1. <span data-ttu-id="d063a-149">**HardwareStation.Extension.EFRSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="d063a-149">Find the **HardwareStation.Extension.EFRSample** project, and build it.</span></span>
2. <span data-ttu-id="d063a-150">**Extension.EFRSample\\bin\\Debug** フォルダーで、以下のファイルを探します。</span><span class="sxs-lookup"><span data-stu-id="d063a-150">In the **Extension.EFRSample\\bin\\Debug** folder, find following files:</span></span>

    - <span data-ttu-id="d063a-151">**Contoso.Commerce.HardwareStation.EFRSample.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="d063a-151">The **Contoso.Commerce.HardwareStation.EFRSample.dll** assembly</span></span>
    - <span data-ttu-id="d063a-152">**Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="d063a-152">The **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** assembly</span></span>

3. <span data-ttu-id="d063a-153">アセンブリ ファイルをハードウェア ステーション拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d063a-153">Copy the assembly file to the Hardware station extensions folder:</span></span>

    - <span data-ttu-id="d063a-154">**共有ハードウェア ステーション:** ファイルを、Microsoft インターネット インフォメーション サービス (IIS) ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d063a-154">**Shared hardware station:** Copy the files to the **bin** folder under the Microsoft Internet Information Services (IIS) Hardware station site location.</span></span>
    - <span data-ttu-id="d063a-155">**Modern POS の専用ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="d063a-155">**Dedicated hardware station on Modern POS:** Copy the files to the Modern POS client broker location.</span></span>

4. <span data-ttu-id="d063a-156">拡張コンフィギュレーション ファイルのハードウェア ステーションの拡張機能の **HardwareStation.Extension.config** が見つかりません。</span><span class="sxs-lookup"><span data-stu-id="d063a-156">Find the extension configuration file Hardware station's extensions **HardwareStation.Extension.config**:</span></span>

    - <span data-ttu-id="d063a-157">**共有ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。</span><span class="sxs-lookup"><span data-stu-id="d063a-157">**Shared hardware station:** The file is located under the IIS Hardware station site location.</span></span>
    - <span data-ttu-id="d063a-158">**Modern POS の専用ハードウェア ステーション:** ファイルは、Modern POS クライアント ブローカーの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="d063a-158">**Dedicated hardware station on Modern POS:** The file is located under the Modern POS client broker location.</span></span>

5. <span data-ttu-id="d063a-159">コンフィギュレーション ファイルの **構成** セクションに、次のセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="d063a-159">Add the following section to the **composition** section of the config file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="modern-pos-extension-components"></a><span data-ttu-id="d063a-160">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d063a-160">Modern POS extension components</span></span>

1. <span data-ttu-id="d063a-161">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d063a-161">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="d063a-162">また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d063a-162">Additionally, make sure that you can run Modern POS from Microsoft Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d063a-163">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="d063a-163">Modern POS must not be customized.</span></span> <span data-ttu-id="d063a-164">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d063a-164">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

2. <span data-ttu-id="d063a-165">**extensions.json**で、次の明細行を追加することによって拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="d063a-165">Enable the extensions to be loaded by adding the following lines in **extensions.json**:</span></span>

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
    > <span data-ttu-id="d063a-166">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d063a-166">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

3. <span data-ttu-id="d063a-167">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="d063a-167">Rebuild the solution.</span></span>
4. <span data-ttu-id="d063a-168">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="d063a-168">Run Modern POS in the debugger, and test the functionality.</span></span>

### <a name="cloud-pos-extension-components"></a><span data-ttu-id="d063a-169">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d063a-169">Cloud POS extension components</span></span>

1. <span data-ttu-id="d063a-170">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d063a-170">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="d063a-171">**extensions.json**で、次の明細行を追加することによって拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="d063a-171">Enable the extensions to be loaded by adding the following lines in **extensions.json**:</span></span>

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
    > <span data-ttu-id="d063a-172">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d063a-172">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

3. <span data-ttu-id="d063a-173">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="d063a-173">Rebuild the solution.</span></span>
4. <span data-ttu-id="d063a-174">**実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d063a-174">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>

### <a name="set-up-required-parameters-in-retail-headquarters"></a><span data-ttu-id="d063a-175">Retail Headquartersにて必要パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="d063a-175">Set up required parameters in Retail Headquarters</span></span>

#### <a name="set-up-the-registration-process"></a><span data-ttu-id="d063a-176">登録プロセスの設定</span><span class="sxs-lookup"><span data-stu-id="d063a-176">Set up the registration process</span></span>

<span data-ttu-id="d063a-177">登録プロセスを有効にするには、次の手順を使用して Retail Headquarters を設定します。</span><span class="sxs-lookup"><span data-stu-id="d063a-177">To enable the registration process, set up Retail Headquarters using the steps below.</span></span> <span data-ttu-id="d063a-178">詳細については、[会計登録プロセスの設定方法](./setting-up-fiscal-integration-for-retail-channel.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d063a-178">For more details, see [How to set up a fiscal registration process](./setting-up-fiscal-integration-for-retail-channel.md).</span></span>

1. <span data-ttu-id="d063a-179">**小売共有パラメーター** を開き、**全般** タブで **会計統合** を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d063a-179">Open **Retail shared parameters** and enable **Fiscal integration** on the **General** tab.</span></span>
2. <span data-ttu-id="d063a-180">**小売 \> チャンネル設定 \> 会計統合 \> 会計コネクタ** メニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="d063a-180">Open **Retail \> Channel setup \> Fiscal integration \> Fiscal connectors** menu.</span></span> <span data-ttu-id="d063a-181">RetailSdk からコネクタ構成を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="d063a-181">Load connector configuration from RetailSdk.</span></span> <span data-ttu-id="d063a-182">ファイルは、SampleExtensions\HardwareStation\Extension.EFRSample\Configuration\ConnectorEFRSampleAustria.xml の下に保存されています。</span><span class="sxs-lookup"><span data-stu-id="d063a-182">The file is located under SampleExtensions\HardwareStation\Extension.EFRSample\Configuration\ConnectorEFRSampleAustria.xml.</span></span>
3. <span data-ttu-id="d063a-183">**小売 \> チャンネル設定 \> 会計統合 \> 会計ドキュメント プロバイダー** メニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="d063a-183">Open **Retail \> Channel setup \> Fiscal integration \> Fiscal document providers** menu.</span></span> <span data-ttu-id="d063a-184">RetailSdk からドキュメント プロバイダー コンフィギュレーションを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="d063a-184">Load documment provider configurations from RetailSdk.</span></span>

    <span data-ttu-id="d063a-185">コンフィギュレーション ファイルは **SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration** の下にあります:</span><span class="sxs-lookup"><span data-stu-id="d063a-185">Configuration files are located under **SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration**:</span></span>

    - <span data-ttu-id="d063a-186">DocumentProviderEFRSampleAustria.xml</span><span class="sxs-lookup"><span data-stu-id="d063a-186">DocumentProviderEFRSampleAustria.xml</span></span>
    - <span data-ttu-id="d063a-187">DocumentProviderNonFiscalEFRSampleAustria.xml</span><span class="sxs-lookup"><span data-stu-id="d063a-187">DocumentProviderNonFiscalEFRSampleAustria.xml</span></span>

4. <span data-ttu-id="d063a-188">**小売 \> チャンネル設定 \> 会計統合 \> コネクタ機能プロファイル** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d063a-188">Open **Retail \> Channel setup \> Fiscal integration \> Connector functional profiles**.</span></span> <span data-ttu-id="d063a-189">上記の手順からドキュメント プロバイダーごとに 2 つの新しいプロファイルを作成し、読み込まれたコネクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="d063a-189">Create two new profiles per document provider from step above and select the loaded connector.</span></span> <span data-ttu-id="d063a-190">必要な場合は、データ マッピング設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="d063a-190">Update data mapping settings if needed.</span></span>
5. <span data-ttu-id="d063a-191">**小売 \> チャンネル設定 \> 会計統合 \> コネクタ技術プロファイル** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d063a-191">Open **Retail \> Channel setup \> Fiscal integration \> Connector technical profiles**.</span></span> <span data-ttu-id="d063a-192">上記の手順から新しいプロファイルを作成し、読み込まれたコネクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="d063a-192">Create a new profile and select the loaded connector from the step above.</span></span> <span data-ttu-id="d063a-193">必要な場合は、接続設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="d063a-193">Update connection settings if needed.</span></span>
6. <span data-ttu-id="d063a-194">**小売 \> チャンネル設定 \> 会計統合 \> 会計コネクタ グループ** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d063a-194">Open **Retail \> Channel setup \> Fiscal integration \> Fiscal connector group**.</span></span> <span data-ttu-id="d063a-195">上記の手順からコネクタの機能プロファイルごとに 2 つの新しいグループを作成します。</span><span class="sxs-lookup"><span data-stu-id="d063a-195">Create two new group per connector's functional profile from the step above.</span></span>
7. <span data-ttu-id="d063a-196">**小売 \> チャンネル設定 \> 会計統合 \> 登録プロセス** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d063a-196">Open **Retail \> Channel setup \> Fiscal integration \> Registration process**.</span></span> <span data-ttu-id="d063a-197">新しいプロセスを作成します。</span><span class="sxs-lookup"><span data-stu-id="d063a-197">Create a new process.</span></span> <span data-ttu-id="d063a-198">上記の手順から両方のコネクタの機能グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="d063a-198">Select both connector's functional groups from the step above.</span></span>
8. <span data-ttu-id="d063a-199">**小売 \> チャンネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d063a-199">Open **Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**.</span></span> <span data-ttu-id="d063a-200">登録プロセスを有効化する、店舗にリンクされているプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d063a-200">Select one that is linked to the store where the registration process should be activated.</span></span> <span data-ttu-id="d063a-201">**会計登録プロセス** タブを展開します。上記の手順から作成された登録プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="d063a-201">Expand the **Fiscal registration process** tab. Select the created registration process from the step above.</span></span> <span data-ttu-id="d063a-202">POS で非会計イベントの登録を有効にするには、**機能** クイック タブで **監査** プロパティを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d063a-202">For enabling registration of non-fiscal events on POS enable **Audit** prorerty at **Functions** fasttab.</span></span>
9. <span data-ttu-id="d063a-203">**小売 \> チャンネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d063a-203">Open the **Retail \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span> <span data-ttu-id="d063a-204">会計プリンターの接続先のハードウェア ステーションにリンクされているプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d063a-204">Select one that is linked to the hardware station to which the fiscal printer will be connected.</span></span> <span data-ttu-id="d063a-205">**会計周辺機器** を展開します。コネクタの技術的なプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d063a-205">Expand the **Fiscal peripherals** Tab. Select the connector technical profile.</span></span>

<span data-ttu-id="d063a-206">詳細については、[オーストリアの会計登録サービス統合サンプル](./emea-aut-fi-sample.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d063a-206">For more information, see [Fiscal registration service integration sample for Austria](./emea-aut-fi-sample.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="d063a-207">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="d063a-207">Production environment</span></span>

<span data-ttu-id="d063a-208">以下の手順に従い、小売コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="d063a-208">Follow these steps to create deployable packages that contain Retail components, and to apply those packages in a production environment.</span></span>

1. <span data-ttu-id="d063a-209">[クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="d063a-209">Complete the steps in the [Cloud POS extension components](#cloud-pos-extension-components) or [Modern POS extension components](#modern-pos-extension-components) section earlier in this topic.</span></span>
2. <span data-ttu-id="d063a-210">**RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="d063a-210">Make the following changes in the package configuration files under the **RetailSdk\\Assets** folder:</span></span>

    1. <span data-ttu-id="d063a-211">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの**構成**セクションに、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d063a-211">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files, add the following lines to the **composition** section:</span></span>

        ``` xml 
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    2. <span data-ttu-id="d063a-212">**HardwareStation.Extension.config** 構成ファイルで、**合成** セクションに追加の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d063a-212">In the **HardwareStation.Extension.config** configuration file, add the following lines to the **composition** section.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. <span data-ttu-id="d063a-213">**BuildTools\Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="d063a-213">Make the following changes in the **BuildTools\Customization.settings** package customization configuration file:</span></span>

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

4. <span data-ttu-id="d063a-214">Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="d063a-214">Start the MSBuild Command Prompt for Visual Studio utility, and run **msbuild** under the Retail SDK folder to create deployable packages.</span></span>
5. <span data-ttu-id="d063a-215">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="d063a-215">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="d063a-216">詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d063a-216">For more information, see [Retail SDK packaging](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>
6. <span data-ttu-id="d063a-217">[Retail Headquartersにおいて設定が必要なパラメーター](#set-up-required-parameters-in-retail-headquarters)の入力を完了します</span><span class="sxs-lookup"><span data-stu-id="d063a-217">Complete the [Set up required parameters in Retail Headquarters](#set-up-required-parameters-in-retail-headquarters)</span></span>

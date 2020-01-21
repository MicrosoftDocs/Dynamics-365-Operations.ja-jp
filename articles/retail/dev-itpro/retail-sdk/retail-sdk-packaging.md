---
title: 配置可能小売パッケージの作成
description: このトピックでは、Microsoft Dynamics 365 Retail の配置可能小売パッケージを作成する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: 0fa3c8e7-49e4-417d-afe9-fa2055f6546f
ms.search.region: Global
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e99d78fe69981d49e97c06432fcd7a98c90e1672
ms.sourcegitcommit: 282552609fdb82ec4463f801023b4bc01bc151d5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935375"
---
# <a name="create-retail-deployable-packages"></a><span data-ttu-id="39337-103">配置可能な小売パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="39337-103">Create retail deployable packages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="39337-104">このトピックでは、次の小売コンポーネントに展開可能な小売パッケージ (すべての拡張機能を含む) の作成し、 Microsoft Dynamics Lifecycle Services (LCS) を使用して、このパッケージをご利用の環境に展開する方法を解説します。</span><span class="sxs-lookup"><span data-stu-id="39337-104">This topic explains how to create a Retail deployable package (which is a package that contain all the extensions) for the following Retail components and deploy the package to your environment by using Microsoft Dynamics Lifecycle Services (LCS):</span></span>

- <span data-ttu-id="39337-105">Commerce Runtime (CRT)</span><span class="sxs-lookup"><span data-stu-id="39337-105">Commerce runtime (CRT)</span></span>
- <span data-ttu-id="39337-106">Retail プロキシ</span><span class="sxs-lookup"><span data-stu-id="39337-106">Retail proxy</span></span>
- <span data-ttu-id="39337-107">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="39337-107">Retail Server</span></span>
- <span data-ttu-id="39337-108">Modern POS</span><span class="sxs-lookup"><span data-stu-id="39337-108">Modern POS</span></span>
- <span data-ttu-id="39337-109">クラウド POS</span><span class="sxs-lookup"><span data-stu-id="39337-109">Cloud POS</span></span>
- <span data-ttu-id="39337-110">Hardware Station</span><span class="sxs-lookup"><span data-stu-id="39337-110">Hardware station</span></span>
- <span data-ttu-id="39337-111">チャネル データベース スクリプト</span><span class="sxs-lookup"><span data-stu-id="39337-111">Channel database scripts</span></span>
- <span data-ttu-id="39337-112">支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="39337-112">Payment connector</span></span>
- <span data-ttu-id="39337-113">Retail Store Scale Unit</span><span class="sxs-lookup"><span data-stu-id="39337-113">Retail Store Scale Unit</span></span>
- <span data-ttu-id="39337-114">ハイブリッド アプリ (IOS および Android POS アプリ)</span><span class="sxs-lookup"><span data-stu-id="39337-114">Hybrid app (IOS and Android POS app)</span></span>

## <a name="retail-deployable-package"></a><span data-ttu-id="39337-115">配置可能 Retail パッケージ</span><span class="sxs-lookup"><span data-stu-id="39337-115">Retail deployable package</span></span>

<span data-ttu-id="39337-116">小売可能なパッケージは、配置に必要なすべてのメタデータと共に、すべてのカスタマイズを含む 1 つの結合されたパッケージです。</span><span class="sxs-lookup"><span data-stu-id="39337-116">A retail deployable package is one combined package that contains all your customizations together with all the metadata that is required for deployment.</span></span> <span data-ttu-id="39337-117">この小売展開可能パッケージを使用して、カスタマイズをさまざまな環境に展開できます。</span><span class="sxs-lookup"><span data-stu-id="39337-117">You can use this retail deployable package to deploy your customizations to various environments.</span></span> <span data-ttu-id="39337-118">LCS で自動フローを使用して、配置を行うことができます。またはパッケージ内に用意されているスクリプトを使用して手動で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="39337-118">You can do the deployment by using the automated flow in LCS, or you can do it manually by using the scripts that are provided inside the package.</span></span> <span data-ttu-id="39337-119">このトピックでは、配置可能小売パッケージを生成するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="39337-119">This topic guides you through the process of generating the retail deployable package.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39337-120">Retail コンポーネントのすべてのカスタマイズは、1 つの配置可能なパッケージとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="39337-120">All customizations for the Retail components are packaged as a single retail deployable package.</span></span> <span data-ttu-id="39337-121">Modern POS、Cloud POS、Retail Store Scale Unit、CRT、および Retail Server といった、個々の Retail コンポーネントの個別パッケージはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="39337-121">Separate packages for individual Retail components, such as Modern POS, Cloud POS, Retail Store Scale Unit, CRT, and Retail Server are not supported.</span></span> <span data-ttu-id="39337-122">独立したソフトウェア ベンダー (ISV) またはさまざまなパートナーの拡張機能をマージまたは結合する必要がある場合でも、すべての拡張機能を単一の小売展開可能パッケージとしてパッケージする必要があります。</span><span class="sxs-lookup"><span data-stu-id="39337-122">You must package all extensions as a single retail deployable package, even if you must merge or combine extensions from independent software vendors (ISVs) or various partners.</span></span>
>
> <span data-ttu-id="39337-123">アプリケーション バージョン 7.1.1541.3036 よりも古い Retail ソフトウェア開発キット (SDK) のバージョンを使用して、カスタマイズが個々の Retail コンポーネント パッケージとして構築されパッケージ化された場合、パッケージは LCS の展開に対してサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="39337-123">If your customizations were built and packaged as individual Retail component packages by using a version of the Retail software development kit (SDK) that is older than application version 7.1.1541.3036, the packages are no longer supported for deployment in LCS.</span></span> <span data-ttu-id="39337-124">[KB 4015062](https://fix.lcs.dynamics.com/Home/Index/0/kb/4015062?permission=Download) で修正プログラムを取得する必要があります。その際、カスタマイズはリビルドおよび再梱包されます。</span><span class="sxs-lookup"><span data-stu-id="39337-124">You must uptake the hotfix in [KB 4015062](https://fix.lcs.dynamics.com/Home/Index/0/kb/4015062?permission=Download), and then rebuild and repackage your customizations.</span></span>

<span data-ttu-id="39337-125">Retail SDK に関する詳細については、[Retail ソフトウエア開発キット (SDK) アーキテクチャ](retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39337-125">For detailed information about the Retail SDK, see [Retail software development kit (SDK) architecture](retail-sdk-overview.md).</span></span>

### <a name="steps-to-create-a-retail-deployable-package"></a><span data-ttu-id="39337-126">小売展開可能パッケージを作成する手順</span><span class="sxs-lookup"><span data-stu-id="39337-126">Steps to create a retail deployable package</span></span>

<span data-ttu-id="39337-127">小売展開可能パッケージを生成するには、2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="39337-127">There are two ways to generate a retail deployable package.</span></span> <span data-ttu-id="39337-128">Retail ビルドの自動化を使用することができます。または Retail SDK のビルド ツールを使用し、手動でパッケージを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="39337-128">You can use the Retail build automation, or you can generate the package manually by using the build tools in the Retail SDK.</span></span> <span data-ttu-id="39337-129">このトピックでは、手動メソッドを対象としています。</span><span class="sxs-lookup"><span data-stu-id="39337-129">This topic focuses on the manual method.</span></span>

1. <span data-ttu-id="39337-130">小売スタックに機能をカスタマイズまたは追加します。</span><span class="sxs-lookup"><span data-stu-id="39337-130">Customize or add functionality to the Retail stack.</span></span>
2. <span data-ttu-id="39337-131">ビルド ツールを使用して、カスタマイズされたインストール パッケージを識別して、コードサインし、カスタマイズされた CRT、Retail サーバー、ハードウェア ステーション アセンブリ、カスタマイズされたデータベース スクリプトを指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-131">Use the build tools to identify the customized installation package, code-sign it, and specify the customized CRT, Retail Server, and Hardware station assemblies, and customized database scripts.</span></span>
3. <span data-ttu-id="39337-132">すべての設定が **...\\Retail SDK\\BuildTools** フォルダーの **Customization.settings** ファイルで指定された後、Retail SDK フォルダーのルートで **msbuild /t:rebuild** を起動します。</span><span class="sxs-lookup"><span data-stu-id="39337-132">After all the settings have been specified in the **Customization.settings** file in the **...\\Retail SDK\\BuildTools** folder, run **msbuild /t:rebuild** on the root of the Retail SDK folder.</span></span> <span data-ttu-id="39337-133">配置可能小売パッケージを生成するために、MSBuild ビルド ツールまたは Microsoft Visual Studio 開発者コマンド ライン ツールのいずれかを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="39337-133">You can use either the MSBuild build tool or the Microsoft Visual Studio developer command-line tool to generate the retail deployable packages.</span></span> <span data-ttu-id="39337-134">パッケージを作成する前に、すべてのカスタマイズされたアセンブリを、**...\\Retail SDK\\References** フォルダに保存します。</span><span class="sxs-lookup"><span data-stu-id="39337-134">Before you build the package, put all the customized assemblies in the **...\\Retail SDK\\References** folder.</span></span> <span data-ttu-id="39337-135">さらに、**...\\Retail SDK\\Assets** フォルダーの **CommerceRuntime.Ext.config**、**CommerceRuntime.MPOSOffline.Ext.config**、 **HardwareStation.Extension.config**、および **RetailProxy.MPOSOffline.ext.config** のような変更済の構成ファイルを入力します。</span><span class="sxs-lookup"><span data-stu-id="39337-135">Additionally, put the modified configuration files, such as **CommerceRuntime.Ext.config**, **CommerceRuntime.MPOSOffline.Ext.config**, **HardwareStation.Extension.config**, and **RetailProxy.MPOSOffline.ext.config**, in the **...\\Retail SDK\\Assets** folder.</span></span>

## <a name="retail-sdk-build-tools--customization-settings"></a><span data-ttu-id="39337-136">Retail SDK ビルド ツール: カスタマイズ設定</span><span class="sxs-lookup"><span data-stu-id="39337-136">Retail SDK build tools – Customization settings</span></span>

<span data-ttu-id="39337-137">カスタマイズを構築しパッケージ化するために Retail SDK が使用するコンフィギュレーション値のほとんどが BuildTools\\Customization.setting files で設定されます。</span><span class="sxs-lookup"><span data-stu-id="39337-137">Most of the configuration values that the Retail SDK uses to build and package customizations are set in the BuildTools\\Customization.setting files.</span></span> <span data-ttu-id="39337-138">これらの値は、バイナリ、コンポーネント、パッケージの名前付け、バージョン管理、コード署名の方法を制御するメタデータを定義します。</span><span class="sxs-lookup"><span data-stu-id="39337-138">These values define metadata that controls how binaries, components, and packages are named, versioned, and code-signed.</span></span> <span data-ttu-id="39337-139">このメタデータを定義した後、Retail SDK ビルド システムはカスタマイズ資産を識別し、すべての Retail コンポーネントのためにカスタマイズ資産をパッケージ化します。</span><span class="sxs-lookup"><span data-stu-id="39337-139">After you define this metadata, the Retail SDK build system uses it to identify the customization assets and package them for all the Retail components.</span></span>

<span data-ttu-id="39337-140">次のコンフィギュレーション設定は、 Customization.settings ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="39337-140">The following configuration settings are available in the Customization.settings file:</span></span>

- <span data-ttu-id="39337-141">**AssemblyNamePrefix** - アセンブリの接頭語名を指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-141">**AssemblyNamePrefix** – Specify the prefix name for the assembly.</span></span> <span data-ttu-id="39337-142">Retail SDK を作成するときは、すべてのアセンブリに接頭辞としてこの名前が付きます。</span><span class="sxs-lookup"><span data-stu-id="39337-142">When you build the Retail SDK, all the assemblies are prefixed with this name.</span></span>
- <span data-ttu-id="39337-143">**CustomAssemblyVersion** - Retail SDK を使用して作成されたすべてのアセンブリのカスタム アセンブリ バージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-143">**CustomAssemblyVersion** – Specify the custom assembly version for all assemblies that are built by using the Retail SDK.</span></span>
- <span data-ttu-id="39337-144">**CustomVersion** - Retail SDK を使用して作成されたすべてのアセンブリのカスタム ファイル バージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-144">**CustomVersion** – Specify the custom file version for all assemblies that are built by using the Retail SDK.</span></span>
- <span data-ttu-id="39337-145">**CustomName** - アセンブリのカスタム名を指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-145">**CustomName** – Specify the custom name for the assembly.</span></span>
- <span data-ttu-id="39337-146">**CustomDescription** - アセンブリの説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-146">**CustomDescription** – Specify the description for the assembly.</span></span>
- <span data-ttu-id="39337-147">**CustomPublisher** – アセンブリの発行元を指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-147">**CustomPublisher** – Specify the publisher for the assembly.</span></span>
- <span data-ttu-id="39337-148">**CustomPublisherDisplayName** - アセンブリの著作権を指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-148">**CustomPublisherDisplayName** – Specify the copyright for the assembly.</span></span>
- <span data-ttu-id="39337-149">**SignAssembly** – ビルド時にアセンブリに署名するには**はい**を指定してください。</span><span class="sxs-lookup"><span data-stu-id="39337-149">**SignAssembly** – Specify **True** to sign the assembly during the build.</span></span>
- <span data-ttu-id="39337-150">**DelaySign** – ビルド中にアセットの署名を延期するには **True** を指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-150">**DelaySign** – Specify **True** to delay signing of the assets during the build.</span></span>
- <span data-ttu-id="39337-151">**AssemblyOriginatorKeyFile** - アセンブリに署名するために使用する厳密な名前キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-151">**AssemblyOriginatorKeyFile** – Specify the strong name key to use to sign the assembly.</span></span>
- <span data-ttu-id="39337-152">**ModernPOSPackageCertificateKeyFile** – Modern POS とハードウェア ステーションの署名に使用する個人情報交換 (PFX) ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-152">**ModernPOSPackageCertificateKeyFile** – Specify the Personal Information Exchange (PFX) file to use to sign Modern POS and Hardware station.</span></span>
- <span data-ttu-id="39337-153">**RetailServerLibraryPathForProxyGeneration** – プロキシの生成に使用するカスタマイズされたRetail サーバー アセンブリを指定します (TypeScript と C\# プロキシの両方)。</span><span class="sxs-lookup"><span data-stu-id="39337-153">**RetailServerLibraryPathForProxyGeneration** – Specify the customized Retail Server assembly to use for proxy generation (both TypeScript and C\# proxies).</span></span>

    <span data-ttu-id="39337-154">7.1 以前のバージョンでは、ここで Retail サーバー アセンブリの名前を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39337-154">For 7.1 and earlier versions, you must specify the name of the Retail Server assembly here.</span></span>

    <span data-ttu-id="39337-155">7.2 以降のバージョンでは、プロキシ生成の commerce ジェネレーター ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="39337-155">For 7.2 and later versions, use the commerce generator tool for proxy generation.</span></span> <span data-ttu-id="39337-156">ただし、E コマース クライアント側でプロキシを使用している場合は、ここでアセンブリ名を指定してください。</span><span class="sxs-lookup"><span data-stu-id="39337-156">However, if you're using the proxy on the e-commerce client side, specify the assembly name here.</span></span>

- <span data-ttu-id="39337-157">**ItemGroup** セクションには、次の設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="39337-157">The **ItemGroup** section includes the following settings:</span></span>

    - <span data-ttu-id="39337-158">**ISV\_CommerceRuntime\_CustomizableFile** – すべてのカスタマイズされた CRT および依存アセンブリの詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-158">**ISV\_CommerceRuntime\_CustomizableFile** – Specify the details of all the customized CRT and dependent assemblies.</span></span> <span data-ttu-id="39337-159">各アセンブリに対して 1 つずつ、複数のエントリを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="39337-159">You can have multiple entries, one for each assembly.</span></span>
    
> [!NOTE]
> <span data-ttu-id="39337-160">拡張機能が Newtonsoft.Json.Portable またはその他のアセンブリに依存している場合は、明示的に追加します。</span><span class="sxs-lookup"><span data-stu-id="39337-160">If the extension depends on Newtonsoft.Json.Portable or some other assemblies, then explicitly include it.</span></span> <span data-ttu-id="39337-161">帯域外 (OOB) Retail サーバーまたは CRT が使用しているため、これらのアセンブリが、既定でパッケージまたは Retail サーバー フォルダーに含まれるとは仮定しないでください。</span><span class="sxs-lookup"><span data-stu-id="39337-161">Don’t assume that these assemblies will be included by default in the packaging or Retail server folder because the out-of-band (OOB) Retail server or CRT is using this.</span></span> <span data-ttu-id="39337-162">今後、OOB 機能でこれらのアセンブリを使用していない場合は、削除することができます。</span><span class="sxs-lookup"><span data-stu-id="39337-162">In the future, if the OOB functionalities don’t use these assemblies, it could be removed.</span></span> <span data-ttu-id="39337-163">その結果、すべての拡張機能に依存するアセンブリを明示的に常に含めることによって、それらを適切なフォルダにパッケージ化して配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39337-163">As a result, you should always explicitly include all of the extension dependent assemblies in order to package and place them in the correct folder.</span></span>

<span data-ttu-id="39337-164">**例**</span><span class="sxs-lookup"><span data-stu-id="39337-164">**Example**</span></span>

```
        ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\MyCrtExtension.dll"
```

- <span data-ttu-id="39337-165">**ISV\_RetailServer\_CustomizableFile** – カスタマイズされたすべての Retail サーバー アセンブリの詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-165">**ISV\_RetailServer\_CustomizableFile** – Specify the details of all the customized Retail Server assemblies.</span></span> <span data-ttu-id="39337-166">各 Retail サーバー アセンブリに対して 1 つの、複数のエントリを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="39337-166">You can have multiple entries, one for each Retail Server assembly.</span></span>

<span data-ttu-id="39337-167">**例**</span><span class="sxs-lookup"><span data-stu-id="39337-167">**Example**</span></span>

```
        ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\MyRetailServerExtension.dll"
        ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\MyRetailServerExtension2.dll"
```

- <span data-ttu-id="39337-168">**ISV\_RetailProxy\_CustomizableFile** – カスタマイズされたすべての Retail プロキシ アセンブリの詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-168">**ISV\_RetailProxy\_CustomizableFile** – Specify the details of all the customized Retail proxy assemblies.</span></span> <span data-ttu-id="39337-169">各 Retail プロキシ アセンブリに対して 1 つの、複数のエントリを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="39337-169">You can have multiple entries, one for each Retail proxy assembly.</span></span> 

<span data-ttu-id="39337-170">**例**</span><span class="sxs-lookup"><span data-stu-id="39337-170">**Example**</span></span>

```
        ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\MyRetailProxyExtension.dll"
```

- <span data-ttu-id="39337-171">**ISV\_HardwareStation\_CustomizableFile** – カスタマイズされたすべてのハードウェア ステーション アセンブリの詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-171">**ISV\_HardwareStation\_CustomizableFile** – Specify the details of all the customized Hardware station assemblies.</span></span> <span data-ttu-id="39337-172">カスタマイズされた各ハードウェア ステーション アセンブリに対して 1 つずつ、複数のエントリを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="39337-172">You can have multiple entries, one for each customized Hardware station assembly.</span></span>

<span data-ttu-id="39337-173">**例**</span><span class="sxs-lookup"><span data-stu-id="39337-173">**Example**</span></span>

```
   ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\MyHardwareStationExtension.dll"
```

- <span data-ttu-id="39337-174">**ISV\_CustomDatabaseFile\_アップグレード\_カスタム** – カスタマイズされたすべてのデータベース スクリプトの詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="39337-174">**ISV\_CustomDatabaseFile\_Upgrade\_Custom** – Specify the details of all the customized database scripts.</span></span>

 <span data-ttu-id="39337-175">**例**</span><span class="sxs-lookup"><span data-stu-id="39337-175">**Example**</span></span>

 ```
     ISV_CustomDatabaseFile_Upgrade_Custom Include="$(SdkRootPath)\Database\Upgrade\Custom\SqlUpdatev1.sql"
```

> [!IMPORTANT]
> <span data-ttu-id="39337-176">ビルド プロセスを開始する前に、拡張アセンブリを \\Retail SDK\\References に、カスタム データベース スクリプトを \\RetailSDK\\Database\Upgrade\\Custom に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39337-176">Before you start the build process, you must put extension assemblies in ...\\Retail SDK\\References and custom database scripts under ...\\RetailSDK\\Database\Upgrade\\Custom.</span></span>

### <a name="database-scripts"></a><span data-ttu-id="39337-177">データベース スクリプト</span><span class="sxs-lookup"><span data-stu-id="39337-177">Database scripts</span></span>

<span data-ttu-id="39337-178">データベース スクリプトは、Retail サーバーおよび Modern POS オフライン パッケージとともにパッケージ化され、Retail Server および Modern POS がインストールされたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="39337-178">Database scripts are packaged together with the Retail Server and Modern POS Offline packages, and are run when Retail Server and Modern POS are installed.</span></span> <span data-ttu-id="39337-179">複数のカスタム データベース スクリプトがある場合は、アルファベット順に実行されます。</span><span class="sxs-lookup"><span data-stu-id="39337-179">If there are multiple custom database scripts, they are run in alphabetical order.</span></span> <span data-ttu-id="39337-180">したがって、スクリプトを特定の順序で実行したい場合は、それに応じて名前を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="39337-180">Therefore, to run the scripts in a specific order, you must name them accordingly.</span></span> <span data-ttu-id="39337-181">CRT.RETAILUPGRADEHISTORY テーブルは、データベースに既に適用されているスクリプトを追跡します。</span><span class="sxs-lookup"><span data-stu-id="39337-181">The CRT.RETAILUPGRADEHISTORY table tracks the scripts that are already applied to the database.</span></span> <span data-ttu-id="39337-182">したがって、次のパッケージ アップグレードは、CRT.RETAILUPGRADEHISTORY テーブルに項目がないアップグレード スクリプトのみを実行します。</span><span class="sxs-lookup"><span data-stu-id="39337-182">Therefore, the next package upgrade runs only the upgrade scripts that don't have an entry in the CRT.RETAILUPGRADEHISTORY table.</span></span>

<span data-ttu-id="39337-183">チャネル データベース拡張機能の詳細については、[チャネル データベース拡張機能](../channel-db-extensions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39337-183">For more details about Channel database extensions, see [Channel database extensions](../channel-db-extensions.md).</span></span>

## <a name="update-the-extension-configuration-files"></a><span data-ttu-id="39337-184">拡張機能の構成ファイルを更新します</span><span class="sxs-lookup"><span data-stu-id="39337-184">Update the extension configuration files</span></span>

<span data-ttu-id="39337-185">CRT、Retail Server、ハードウェア ステーション、またはプロキシに新しい拡張機能がある場合は、関連する拡張構成ファイルの\<構成\>セクションに拡張アセンブリの詳細を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39337-185">If you have any new extensions in CRT, Retail Server, Hardware station, or proxy, you should register the details of the extension assemblies in the \<composition\> section of the relevant extension configuration file.</span></span> <span data-ttu-id="39337-186">すべての拡張設定ファイルは次で見つけることができます。\\RetailSDK\\資産フォルダ。</span><span class="sxs-lookup"><span data-stu-id="39337-186">You can find all the extension configuration files in the ...\\RetailSDK\\Assets folder.</span></span> <span data-ttu-id="39337-187">すべての拡張機能は拡張ファイルの情報に基づいて読み込まれるため、アセンブリを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39337-187">Because all extensions are loaded based on the information in the extension configuration files, you must register your assemblies there.</span></span>

<span data-ttu-id="39337-188">パッケージを使用する前に、次の構成ファイルを更新する必要があります (この領域でカスタマイズがある場合)。</span><span class="sxs-lookup"><span data-stu-id="39337-188">Before you use the package, you must update the following configuration files if you have any customization in that area:</span></span>

- <span data-ttu-id="39337-189">**CommerceRuntime.Ext.config** – すべての CRT 拡張機能、CRT、Retail サーバー依存アセンブリ、そしてカスタム キー値ペア構成を登録します。</span><span class="sxs-lookup"><span data-stu-id="39337-189">**CommerceRuntime.Ext.config** – Register all of your CRT extensions, CRT and Retail server dependent assemblies, and custom Key Value pair configurations.</span></span> <span data-ttu-id="39337-190">拡張機能のコンフィギュレーション値のキー名には、先頭に "ext" を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="39337-190">The key name for the extension configuration values must be prefixed with "ext".</span></span> <span data-ttu-id="39337-191">Commerce Runtime 初期化ではこの規則が適用され、この規則が使用されない場合は読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="39337-191">The Commerce runtime initialization will enforce this convention and will not load if this is not used.</span></span> <span data-ttu-id="39337-192">プレフィックスを追加して、制御されるサブ領域 ("ext.CusomStorageConfig.CustomKeyCart" など) を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="39337-192">Additional prefixes can be added to represent the sub-area that is controlled, such as  "ext.CusomStorageConfig.CustomKeyCart”.</span></span>

> [!NOTE]
> <span data-ttu-id="39337-193">拡張機能が Newtonsoft.Json.Portable またはその他のアセンブリに依存している場合は、明示的に追加します。</span><span class="sxs-lookup"><span data-stu-id="39337-193">If the extension depends on Newtonsoft.Json.Portable or some other assemblies, then explicitly include it.</span></span> <span data-ttu-id="39337-194">既定では、パッケージ内または Retail サーバー フォルダにおいて、これらのアセンブリを OOB 機能で使用していない場合は、これらのアセンブリは含まれない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="39337-194">By default, in the packaging or in the Retail server folder these assemblies may not be include if the OOB functionalities don’t use these assemblies anymore.</span></span> <span data-ttu-id="39337-195">よって、拡張機能にはすべての拡張機能依存アセンブリを明示的に常に含め、それらを適切なフォルダにパッケージ化して配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39337-195">So extensions should always explicitly include all the extension dependent assemblies to package and place them in the correct folder.</span></span>

<span data-ttu-id="39337-196">**例: 拡張機能アセンブリと拡張キー値ペアの構成の登録方法**</span><span class="sxs-lookup"><span data-stu-id="39337-196">**Example - How to register extension assemblies and extension key value pair configurations**</span></span>


 ```C#
    <?xml version="1.0" encoding="utf-8"?>
    <commerceRuntimeExtensions>
        <composition>
            <!-- Register your own assemblies here. -->
            <add source="assembly" value="my custom library" />
        </composition>
        
        <settings>
             <add name="ext.myCustomKey1" value="myCustomValue1" />
             <add name="ext.myCustomarea.myCustomKey2" value="myCustomValue2" />
        </settings>
    </commerceRuntimeExtensions>
```

- <span data-ttu-id="39337-197">**CommerceRuntime.MPOSOffline.Ext.config** – すべての CRT 拡張機能、依存アセンブリ、そして拡張キー値ペア構成を登録します。</span><span class="sxs-lookup"><span data-stu-id="39337-197">**CommerceRuntime.MPOSOffline.Ext.config** – Register all your CRT extensions, dependent assemblies and extension Key Value pair configurations.</span></span> <span data-ttu-id="39337-198">拡張機能のコンフィギュレーション値のキー名には、先頭に "ext" を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="39337-198">The key name for the extension configuration values must be prefixed with "ext."</span></span> <span data-ttu-id="39337-199">Commerce Runtime 初期化ではこの規則が適用され、それ以外の場合は読み込まれないため、プレフィックスを追加して制御するサブ領域を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="39337-199">as the CommerceRuntime initialization will enforce this convention and will not load otherwise, additional prefixes can be added to represent the sub-area they control.</span></span> <span data-ttu-id="39337-200">例: "ext.CusomStorageConfig.CustomKeyCart"</span><span class="sxs-lookup"><span data-stu-id="39337-200">Ex: "ext.CusomStorageConfig.CustomKeyCart"</span></span>

<span data-ttu-id="39337-201">**例: 拡張機能アセンブリと拡張キー値ペアの構成の登録方法**</span><span class="sxs-lookup"><span data-stu-id="39337-201">**Example - How to register extension assemblies and extension key value pair configurations**</span></span>

```C#
    <?xml version="1.0" encoding="utf-8"?>
    <commerceRuntimeExtensions>
        <composition>
            <!-- Register your own assemblies or types here. -->
            <add source="assembly" value=" my custom library" />
        </composition>
        
        <settings>
             <add name="ext.myCustomKey1" value="myCustomValue1" />
             <add name="ext.myCustomarea.myCustomKey2" value="myCustomValue2" />
        </settings>
    </commerceRuntimeExtensions>
```

- <span data-ttu-id="39337-202">**HardwareStation.Extension.config** – すべてのハードウェア ステーション拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="39337-202">**HardwareStation.Extension.config** – Register all your Hardware station extensions.</span></span>

<span data-ttu-id="39337-203">**例**</span><span class="sxs-lookup"><span data-stu-id="39337-203">**Example**</span></span>

```C#
    <?xml version="1.0" encoding="utf-8"?>
    <hardwareStationExtension>
        <composition>
            <! -- Register your own assemblies or types here. -->
            <add source="assembly" value=" my custom library" />
        </composition>
    </hardwareStationExtension>
 ```

- <span data-ttu-id="39337-204">**RetailProxy.MPOSOffline.ext.config** – すべての小売プロキシ拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="39337-204">**RetailProxy.MPOSOffline.ext.config** – Register all your retail proxy extensions.</span></span>

 <span data-ttu-id="39337-205">**例**</span><span class="sxs-lookup"><span data-stu-id="39337-205">**Example**</span></span>

    ```C#
    <?xml version="1.0" encoding="utf-8"?>
    <retailProxyExtensions>
        <composition>
            <!-- Register your own proxy extension assemblies. -->
            <add source="assembly" value=" my custom library" />
        </composition>
    </retailProxyExtensions>
    ```

### <a name="retail-server-extension-assemblies"></a><span data-ttu-id="39337-206">Retail サーバーの拡張機能アセンブリ</span><span class="sxs-lookup"><span data-stu-id="39337-206">Retail Server extension assemblies</span></span>

<span data-ttu-id="39337-207">パッケージを開始する前に、Retail Server web.config file の \<extensionComposition\> に、Retail Server 拡張アセンブリのエントリを追加する必要があります。これにより、アセンブリがロードされ、使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="39337-207">Before you start the package, you must add an entry for the Retail Server extension assemblies in the \<extensionComposition\> of the Retail Server web.config file, so that the assemblies are loaded and used.</span></span> <span data-ttu-id="39337-208">web.config ファイルは、Retail SDK\\パッケージ\\RetailServer\\ コード フォルダーで検索できます。</span><span class="sxs-lookup"><span data-stu-id="39337-208">You can find the web.config file in the Retail SDK\\Packages\\RetailServer\\Code folder.</span></span>

<span data-ttu-id="39337-209">次の図は、Retail サーバーの Web.config ファイルの例を示します。</span><span class="sxs-lookup"><span data-stu-id="39337-209">The following illustration shows an example of a Retail Server web.config file.</span></span>

<span data-ttu-id="39337-210">[![Retail サーバーの Web.config ファイル](./media/retail-server-web-config.png)](./media/retail-server-web-config.png)</span><span class="sxs-lookup"><span data-stu-id="39337-210">[![Retail Server web.config file](./media/retail-server-web-config.png)](./media/retail-server-web-config.png)</span></span>

### <a name="shared-hardware-station-webconfig"></a><span data-ttu-id="39337-211">共有されたハードウェア ステーション Web コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="39337-211">Shared Hardware station web.config</span></span>

<span data-ttu-id="39337-212">従来の支払コネクタを使用していない場合は、従来の支払コネクタをコメントして、web.構成ファイル内の非従来型コネクタを有効にします。</span><span class="sxs-lookup"><span data-stu-id="39337-212">If you are not using the legacy payment connector, then comment the legacy payment connector and enable the non-legacy connector in the web.config file.</span></span> <span data-ttu-id="39337-213">既定では、共有されたハードウェア ステーションの web.config で、従来の支払コネクタが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="39337-213">By default, the legacy payment connector is enabled in the shared hardware station web.config.</span></span>

<span data-ttu-id="39337-214">**例** 従来のコネクタを無効にするには、\RetailSDK\References\Microsoft.Dynamics.Retail.HardwareStation.WebHost.x.x.x.x\Pkg\bin から web.config ファイルを開き、従来のコネクタをコメントします。</span><span class="sxs-lookup"><span data-stu-id="39337-214">**Example** To disable the legacy connector, open the web.config file from \RetailSDK\References\Microsoft.Dynamics.Retail.HardwareStation.WebHost.x.x.x.x\Pkg\bin and comment the legacy connector.</span></span> <span data-ttu-id="39337-215">次のサンプル コードに示すように、合成セクションで非従来型のコネクタを有効にします。</span><span class="sxs-lookup"><span data-stu-id="39337-215">Enable the non-legacy connector under the composition section, as shown in the following sample code.</span></span>

> [!NOTE]
> <span data-ttu-id="39337-216">web.config フォルダー パス (\RetailSDK\References\Microsoft.Dynamics.Retail.HardwareStation.WebHost.x.x.x.x\Pkg\bin) の x.x.x.x はバージョン番号です。</span><span class="sxs-lookup"><span data-stu-id="39337-216">x.x.x.x in the web.config folder path (\RetailSDK\References\Microsoft.Dynamics.Retail.HardwareStation.WebHost.x.x.x.x\Pkg\bin) is the version number.</span></span> <span data-ttu-id="39337-217">これは、Retail SDK のバージョン番号によって異なります。</span><span class="sxs-lookup"><span data-stu-id="39337-217">This will vary based on your Retail SDK version number.</span></span>

```C#
    <composition>
      <!-- Defaulting to legacy payment devices.
 <add source="assembly" value="Microsoft.Dynamics.Commerce.HardwareStation.Peripherals.Legacy.PaymentDeviceAdapter"/>
      -->
      <add source="assembly" value="Microsoft.Dynamics.Commerce.HardwareStation.Peripherals.PaymentDeviceAdapter" />
    </composition>
```

> [!NOTE]
> <span data-ttu-id="39337-218">上記の例、またはチャネル構成ファイルのいずれかで、カスタム設定を追加したり変更したりしないでください。</span><span class="sxs-lookup"><span data-stu-id="39337-218">Do not add or change any custom settings in the above mentioned example or in any of the channel config files.</span></span> <span data-ttu-id="39337-219">サポートされている変更は、合成セクションでのカスタム アセンブリの詳細の追加のみです。</span><span class="sxs-lookup"><span data-stu-id="39337-219">The only supported modification is to add custom assemblies details in the composition section.</span></span>
>
> <span data-ttu-id="39337-220">また、拡張機能またはパッケージの一部として、構成ファイルのいずれも編集しないでください。</span><span class="sxs-lookup"><span data-stu-id="39337-220">As part of your extension or package, do not edit any of the following config files.</span></span> <span data-ttu-id="39337-221">これらの構成ファイルは、配置の際にコア Microsoft パッケージの最新のファイルで更新され、変更内容は失われます。</span><span class="sxs-lookup"><span data-stu-id="39337-221">These config files will be updated with the latest file from core Microsoft package during deployment and your changes will be lost.</span></span>
>
> - <span data-ttu-id="39337-222">CommerceRuntime.config</span><span class="sxs-lookup"><span data-stu-id="39337-222">CommerceRuntime.config</span></span>
> - <span data-ttu-id="39337-223">dllhost.exe.config</span><span class="sxs-lookup"><span data-stu-id="39337-223">dllhost.exe.config</span></span>
> - <span data-ttu-id="39337-224">HardwareStation.Dedicated.config</span><span class="sxs-lookup"><span data-stu-id="39337-224">HardwareStation.Dedicated.config</span></span>
> - <span data-ttu-id="39337-225">HardwareStation.Shared.config</span><span class="sxs-lookup"><span data-stu-id="39337-225">HardwareStation.Shared.config</span></span>
> - <span data-ttu-id="39337-226">workflowFoundation.config</span><span class="sxs-lookup"><span data-stu-id="39337-226">workflowFoundation.config</span></span>
> - <span data-ttu-id="39337-227">ハードウェア ステーション - Web.config</span><span class="sxs-lookup"><span data-stu-id="39337-227">Hardware station - Web.config</span></span>

## <a name="install-nugetexe"></a><span data-ttu-id="39337-228">NuGet.exe のインストール</span><span class="sxs-lookup"><span data-stu-id="39337-228">Install NuGet.exe</span></span> 

<span data-ttu-id="39337-229">ファイルの結合およびSDKのサイズを最小限に抑えるため、いくつかの依存関係パッケージおよび参照を NuGet パッケージに移動します。</span><span class="sxs-lookup"><span data-stu-id="39337-229">Some of the dependency packages and references have moved to NuGet packages to minimize the file merge and the size of the SDK.</span></span> <span data-ttu-id="39337-230">これらは NuGet.org からダウンロードできます。Retail SDK を作成すると、これらの依存関係は自動的に packages.config ファイルに基づいて NuGet.org から収集されます。</span><span class="sxs-lookup"><span data-stu-id="39337-230">These are available for download from the NuGet.org. When you build the Retail SDK these dependencies are automatically pulled from the NuGet.org based on the packages.config file.</span></span> <span data-ttu-id="39337-231">このためには、「[NuGet コマンド ライン インターフェイス](https://docs.microsoft.com/nuget/tools/nuget-exe-cli-reference#installing-nugetexe)」をインストールし、 NuGet.org から nuget.exe をダウンロードした後、nuget を Windows パスに追加する必要があります。次の手順は、Windows パスに nuget を追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="39337-231">For this to work, you need to install the [NuGet command line interface](https://docs.microsoft.com/nuget/tools/nuget-exe-cli-reference#installing-nugetexe) and add the nuget to the Windows path after downloading nuget.exe from NuGet.org. The following steps show how to add the nuget to the Windows path:</span></span>

1. <span data-ttu-id="39337-232">Windows メニューを開き、 **Path**と入力します。</span><span class="sxs-lookup"><span data-stu-id="39337-232">Open the Windows menu and type **Path**.</span></span> <span data-ttu-id="39337-233">**システム環境変数を編集**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="39337-233">The **Edit the system environment variables** will be available.</span></span> 
2. <span data-ttu-id="39337-234">メニューの右下の**環境変数**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="39337-234">In that menu, click **Environment variables** on the lower right.</span></span>
3. <span data-ttu-id="39337-235">次のウィンドウで、**システム変数**の**パス**を選択し、**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="39337-235">In the next window, under **System variables**, select **Path** and click **Edit**.</span></span>
4. <span data-ttu-id="39337-236">nuget.exe ファイルを保存するフォルダーのエントリを追加するか、既に登録されているフォルダーに nuget.exe ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="39337-236">Add an entry for the folder where you would like to store the nuget.exe file or store the nuget.exe file in a folder that is already listed.</span></span>

## <a name="generate-a-retail-deployable-package"></a><span data-ttu-id="39337-237">配置可能小売パッケージを生成</span><span class="sxs-lookup"><span data-stu-id="39337-237">Generate a retail deployable package</span></span>

<span data-ttu-id="39337-238">配置可能小売パッケージを生成するには、MSBuild ビルド コマンド プロンプト ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="39337-238">To generate the retail deployable package, open the MSBuild build Command Prompt window.</span></span> <span data-ttu-id="39337-239">(開発者仮想マシンの、**開始**メニューで **msbuild** を検索します。) そして、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="39337-239">(On the developer virtual machine, search for **msbuild** on the **Start** menu.) Then run the following command.</span></span>

```
msbuild /p:Configuration=Release
```

<span data-ttu-id="39337-240">Microsoft Visual Studio 2015 開発者コマンド ライン ツールで同じコマンドを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="39337-240">You can also run the same command in the Microsoft Visual Studio 2015 developer command-line tool.</span></span>

### <a name="packages"></a><span data-ttu-id="39337-241">梱包</span><span class="sxs-lookup"><span data-stu-id="39337-241">Packages</span></span>

<span data-ttu-id="39337-242">ビルドが完了した後、Retail SDK\\Packages\\RetailDeployablePackage フォルダーに、配置可能小売パッケージ が zip ファイルとして (RetailDeployablePackage.zip) が生成されます。</span><span class="sxs-lookup"><span data-stu-id="39337-242">After the build is completed, retail deployable packages are generated as a zip file (RetailDeployablePackage.zip) in the Retail SDK\\Packages\\RetailDeployablePackage folder.</span></span>

> [!NOTE]
> <span data-ttu-id="39337-243">さまざまな Retail コンポーネントを別々のパッケージにすることはありません。</span><span class="sxs-lookup"><span data-stu-id="39337-243">There won't be separate packages the various Retail components.</span></span> <span data-ttu-id="39337-244">すべてのパッケージは、RetailDeployablePackage という名の 1 つのバンドル パッケージに結合されます。</span><span class="sxs-lookup"><span data-stu-id="39337-244">All the packages will be combined into one bundle package that is named RetailDeployablePackage.</span></span>

## <a name="deploy-the-retail-deployable-packages"></a><span data-ttu-id="39337-245">小売展開可能パッケージを配置する</span><span class="sxs-lookup"><span data-stu-id="39337-245">Deploy the retail deployable packages</span></span>

<span data-ttu-id="39337-246">手動または LCS 自動化フローを使用してパッケージを配置する方法については、[配置可能なパッケージを適用する](../../../dev-itpro/deployment/apply-deployable-package-system.md)および[配置可能なパッケージをインストールする](../../../dev-itpro/deployment/install-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39337-246">For information about how to deploy the packages either manually or by using the automated flow in LCS, see [Apply a deployable package](../../../dev-itpro/deployment/apply-deployable-package-system.md) and [Install a deployable package](../../../dev-itpro/deployment/install-deployable-package.md).</span></span>

---
title: スウェーデン用の管理単位との Retail POS の統合
description: このトピックは、スウェーデンの管理単位統合サンプルのビルドとインストールのガイドです。
author: EvgenyPopovMBS
manager: Annbe
ms.date: 02/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: shylaw
ms.search.scope: Operations, Retail
ms.search.region: Sweden
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-2-28
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: 958285e4dbbee486d92c171d52356199c12cdf4f
ms.sourcegitcommit: 0e01d3907b70261aee2df3e3ce0dde2f1343a43a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/27/2019
ms.locfileid: "770170"
---
# <a name="sample-for-retail-pos-integration-with-control-units-for-sweden"></a><span data-ttu-id="9aaea-103">スウェーデン用の管理単位との Retail POS の統合</span><span class="sxs-lookup"><span data-stu-id="9aaea-103">Sample for Retail POS integration with control units for Sweden</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9aaea-104">**サンプル コードの通知**</span><span class="sxs-lookup"><span data-stu-id="9aaea-104">**SAMPLE CODE NOTICE**</span></span>

<span data-ttu-id="9aaea-105">**このサンプルコードは現状のまま利用可能です。明示的または黙示的を問わず、特定の目的への適合性、正確性、完全性、結果、または商品性の条件に関して、Microsoft は一切保証しません。このサンプル コードの使用またはその結果に対するリスクは、すべてお客様が負うものとします。**</span><span class="sxs-lookup"><span data-stu-id="9aaea-105">**THIS SAMPLE CODE IS MADE AVAILABLE AS IS.  MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED, OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.  THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.**</span></span>

<span data-ttu-id="9aaea-106">**技術サポートは提供されません。コード配布を許可する Microsoft の使用許諾契約がない限り、このコードを配布することはできません。**</span><span class="sxs-lookup"><span data-stu-id="9aaea-106">**NO TECHNICAL SUPPORT IS PROVIDED.  YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.**</span></span>

<span data-ttu-id="9aaea-107">このサンプルでは、Retail Modern POS または クラウド POS を会計登録と統合する Microsoft Dynamics 365 for Retail 拡張機能を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-107">This sample shows how to create Microsoft Dynamics 365 for Retail extensions to integrate Retail Modern POS or Cloud POS with a fiscal register.</span></span> <span data-ttu-id="9aaea-108">特に、このサンプルには Microsoft Dynamics for Retail POS をスウェーデンの管理単位と統合するコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9aaea-108">Specifically, this sample includes the code for integrating Microsoft Dynamics for Retail POS with control units for Sweden.</span></span> <span data-ttu-id="9aaea-109">たとえば、このサンプルでは Retail Innovation HTT AB の CleanCash® Type A 管理単位のアプリケーション プログラミング インターフェイス (API) を使用します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-109">As an example, this sample uses the application programming interface (API) of the CleanCash® Type A control unit by Retail Innovation HTT AB.</span></span> <span data-ttu-id="9aaea-110">CleanCash® API のバージョン1.1.4 が使用されます。</span><span class="sxs-lookup"><span data-stu-id="9aaea-110">Version 1.1.4 of the CleanCash® API is used.</span></span> <span data-ttu-id="9aaea-111">API およびドキュメントを含む統合パッケージについては、デバイスの製造元に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="9aaea-111">For the integration package that includes the API and documentation, contact the manufacturer of the device.</span></span>

<span data-ttu-id="9aaea-112">このサンプルは、Retail ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="9aaea-112">This sample is a part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="9aaea-113">Retail SDK をダウンロードして使用する方法については、[Retail SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9aaea-113">For information about how to install and use the Retail SDK, see the [Retail SDK documentation](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="9aaea-114">このサンプルは、ハードウェア ステーション、Commerce Runtime (CRT)、および 販売時点管理 (POS) で構成されます。</span><span class="sxs-lookup"><span data-stu-id="9aaea-114">This sample consists of extensions for the Hardware station, commerce runtime (CRT), and point of sale (POS).</span></span> <span data-ttu-id="9aaea-115">このサンプルを実行するには、ハードウェア ステーション、CRT、および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9aaea-115">To run this sample, you must modify and build the Hardware station, CRT, and POS projects.</span></span> <span data-ttu-id="9aaea-116">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-116">We recommend that use you an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="9aaea-117">また Microsoft Visual Studio オンライン (VSO) のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-117">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>


> [!NOTE]
> <span data-ttu-id="9aaea-118">使用している Microsoft Dynamics 365 for Retail のバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="9aaea-118">Some steps in the procedures in this topic differ, depending on the version of Microsoft Dynamics 365 for Retail that you're using.</span></span> <span data-ttu-id="9aaea-119">詳細については、 [Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9aaea-119">For more information, see [What's new or changed in Dynamics 365 for Retail](../get-started/whats-new.md).</span></span>

## <a name="development-environment"></a><span data-ttu-id="9aaea-120">開発環境</span><span class="sxs-lookup"><span data-stu-id="9aaea-120">Development environment</span></span>

<span data-ttu-id="9aaea-121">サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9aaea-121">Follow these steps to set up a development environment so that you can test and extend the sample.</span></span>

1. <span data-ttu-id="9aaea-122">ハードウェア ステーション コンポーネントを拡張します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-122">Extend the Hardware station component:</span></span>

   1. <span data-ttu-id="9aaea-123">**RetailSDK\SampleExtensions\HardwareStation** で ハードウェア ステーション ソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="9aaea-123">Open the Hardware station solution under **RetailSDK\SampleExtensions\HardwareStation**.</span></span>
   2. <span data-ttu-id="9aaea-124">**HardwareStation.Extension.FiscalRegisterSample.csproj** 拡張機能プロジェクトを検索し、コンパイルします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-124">Find the **HardwareStation.Extension.FiscalRegisterSample.csproj** extension project, and compile it.</span></span>
   3. <span data-ttu-id="9aaea-125">**Extension.FiscalRegisterSample\bin\Debug** で以下のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-125">Find the following files in **Extension.FiscalRegisterSample\bin\Debug**:</span></span>

       - <span data-ttu-id="9aaea-126">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="9aaea-126">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** assembly</span></span>
       - <span data-ttu-id="9aaea-127">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9aaea-127">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** configuration</span></span>
       - <span data-ttu-id="9aaea-128">**Interop.CleanCash_1_1.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="9aaea-128">The **Interop.CleanCash_1_1.dll** assembly</span></span>

   4. <span data-ttu-id="9aaea-129">ファイルを配置した ハードウェア ステーション マシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-129">Copy the files to a deployed Hardware station machine:</span></span>

       - <span data-ttu-id="9aaea-130">**リモート ハードウェア ステーション:** ファイルを、Microsoft インターネット インフォメーション サービス (IIS) ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-130">**Remote Hardware station:** Copy the files to the **bin** folder under the Microsoft Internet Information Services (IIS) Hardware station site location.</span></span>
       - <span data-ttu-id="9aaea-131">**ローカル ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-131">**Local Hardware station:** Copy the files to the Modern POS client broker location.</span></span>

   5. <span data-ttu-id="9aaea-132">ハードウェア ステーションの拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-132">Find the configuration file for Hardware station's extensions.</span></span>

      # <a name="retail-73-and-earliertabretail-7-3"></a>[<span data-ttu-id="9aaea-133">Retail 7.3 以前</span><span class="sxs-lookup"><span data-stu-id="9aaea-133">Retail 7.3 and earlier</span></span>](#tab/retail-7-3)

      <span data-ttu-id="9aaea-134">**リモート ハードウェア ステーション:** ファイルの名前は **hardwarestation.shared.config**で、IIS ハードウェア ステーション サイトの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="9aaea-134">**Remote Hardware station:** The file is named **hardwarestation.shared.config**, and it's under the IIS Hardware station site location.</span></span>

      <span data-ttu-id="9aaea-135">**ローカル ハードウェア ステーション:** ファイルの名前は **HardwareStation.Dedicated.config**で、Modern POS クライアント ブローカーの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="9aaea-135">**Local Hardware station:** The file is named **HardwareStation.Dedicated.config**, and it's under the Modern POS client broker location.</span></span>

      # <a name="retail-731-and-latertabretail-7-3-1"></a>[<span data-ttu-id="9aaea-136">Retail 7.3.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="9aaea-136">Retail 7.3.1 and later</span></span>](#tab/retail-7-3-1)

      <span data-ttu-id="9aaea-137">ファイルの名前は **HardwareStation.Extension.config** です。</span><span class="sxs-lookup"><span data-stu-id="9aaea-137">The file is named **HardwareStation.Extension.config**:</span></span>

      <span data-ttu-id="9aaea-138">**リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。</span><span class="sxs-lookup"><span data-stu-id="9aaea-138">**Remote Hardware station:** The file is located under the IIS Hardware station site location.</span></span>

      <span data-ttu-id="9aaea-139">**ローカル ハードウェア ステーション:** ファイルは Modern POS クライアント ブローカーの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="9aaea-139">**Local Hardware station:** The file is located under the Modern POS client broker location.</span></span>

    ---

    6. <span data-ttu-id="9aaea-140">コンフィギュレーション ファイルの **構成** セクションに、次のセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-140">Add the following section to the **composition** section of the config file.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

    7. <span data-ttu-id="9aaea-141">ハードウェア ステーション サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-141">Restart the Hardware station service:</span></span>

        - <span data-ttu-id="9aaea-142">**リモート ハードウェア ステーション:** IIS マネージャーからハードウェア ステーション サイトを再起動します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-142">**Remote Hardware station:** Restart the Hardware station site from IIS Manager.</span></span>
        - <span data-ttu-id="9aaea-143">**ローカル ハードウェア ステーション:** タスク マネージャーで **dllhost.exe** プロセスを終了して、Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-143">**Local Hardware station:** End the **dllhost.exe** process in Task Manager, and then restart Modern POS.</span></span>

2. <span data-ttu-id="9aaea-144">CRT コンポーネントの拡張。</span><span class="sxs-lookup"><span data-stu-id="9aaea-144">Extend the CRT component:</span></span>

   1. <span data-ttu-id="9aaea-145">**RetailSdk\SampleExtensions\CommerceRuntime** の下の、CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="9aaea-145">Open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\SampleExtensions\CommerceRuntime**.</span></span>
   2. <span data-ttu-id="9aaea-146">**Runtime.Extensions.FiscalRegisterReceiptSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-146">Find the **Runtime.Extensions.FiscalRegisterReceiptSample** project, and build it.</span></span>
   3. <span data-ttu-id="9aaea-147">CRT の ext.config ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-147">Find the ext.config file for CRT:</span></span>

       - <span data-ttu-id="9aaea-148">**小売サーバー:** ファイルは **commerceRuntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="9aaea-148">**Retail Server:** The file is named **commerceRuntime.ext.config**, and it's under the **bin\ext** folder under the IIS Retail server site location.</span></span>
       - <span data-ttu-id="9aaea-149">**Modern POS のローカル CRT:** ファイルの名前は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーの場所の **bin\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="9aaea-149">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the **bin\ext** folder under the local CRT client broker location.</span></span>

   4. <span data-ttu-id="9aaea-150">コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-150">Register the CRT change in the configuration file.</span></span>

       ``` xml
       <add source="type" value="Contoso.Commerce.Runtime.FiscalRegisterReceipt, Contoso.Commerce.Runtime.FiscalRegisterReceipt" />
       ```

       > [!NOTE]
       > <span data-ttu-id="9aaea-151">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="9aaea-151">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="9aaea-152">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="9aaea-152">These files aren't intended for any customizations.</span></span>

   5. <span data-ttu-id="9aaea-153">**Extensions.FiscalRegisterReceiptSample\bin\Debug** で、**Contoso.Commerce.Runtime.FiscalRegisterReceiptSample.dll** アセンブリを検索します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-153">Find the **Contoso.Commerce.Runtime.FiscalRegisterReceiptSample.dll** assembly file in **Extensions.FiscalRegisterReceiptSample\bin\Debug**.</span></span>
   6. <span data-ttu-id="9aaea-154">アセンブリを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-154">Copy the assembly to the CRT extensions folder:</span></span>

       - <span data-ttu-id="9aaea-155">**Retail サーバー:** IIS 小売サーバー サイトの場所の **\bin\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-155">**Retail Server:** Copy the assembly to the **\bin\ext** folder under the IIS Retail server site location.</span></span>
       - <span data-ttu-id="9aaea-156">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-156">**Local CRT on Modern POS:** Copy the assembly to the **\ext** folder under the local CRT client broker location.</span></span>

      > [!NOTE]
      > <span data-ttu-id="9aaea-157">CRT と Retail サーバーのすべてのコードの変更は、RetailSdk\SampleExtensions の一部です。</span><span class="sxs-lookup"><span data-stu-id="9aaea-157">All the code changes for CRT and Retail Server are all part of RetailSdk\SampleExtensions.</span></span> <span data-ttu-id="9aaea-158">したがって、上記の手順は、これらのコードの変更を構築、配置、およびテストする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="9aaea-158">Therefore, the preceding steps show how to build, deploy, and test these code changes.</span></span>

3. <span data-ttu-id="9aaea-159">Modern POS コンポーネントの拡張。</span><span class="sxs-lookup"><span data-stu-id="9aaea-159">Extend the Modern POS component:</span></span>

    1. <span data-ttu-id="9aaea-160">**RetailSdk\POS\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-160">Open the solution at **RetailSdk\POS\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="9aaea-161">また、Modern POS が **Run** コマンドを使用して、Microsoft Visual Studio から実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-161">Also make sure that Modern POS can be run from Microsoft Visual Studio using the **Run** command.</span></span> <span data-ttu-id="9aaea-162">(Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="9aaea-162">(Modern POS must not be customized.</span></span> <span data-ttu-id="9aaea-163">ユーザー アカウント制御 [UAC] を有効にして、必要に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。)</span><span class="sxs-lookup"><span data-stu-id="9aaea-163">You must enable User Account Control [UAC], and you must uninstall previously installed instances of Modern POS as required.)</span></span>
    2. <span data-ttu-id="9aaea-164">**Pos.Extensions** プロジェクトの **FiscalRegisterSample** を含めます。</span><span class="sxs-lookup"><span data-stu-id="9aaea-164">Include **FiscalRegisterSample** in the **Pos.Extensions** project.</span></span>
    3. <span data-ttu-id="9aaea-165">除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-165">Enable the extension to be compiled in **tsconfig.json** by removing the **FiscalRegisterSample** folder from the exclude list.</span></span>
    3. <span data-ttu-id="9aaea-166">適切な場所に次の行を追加して、**InternalExtensions\extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-166">Enable the extension in **InternalExtensions\extensions.json** by adding the following lines in the appropriate place.</span></span>

        ``` json
        {
            "debugBuildsOnly": false,
            "baseUrl": "FiscalRegisterSample"
        }
        ```

    4. <span data-ttu-id="9aaea-167">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-167">Rebuild the solutions.</span></span>
    5. <span data-ttu-id="9aaea-168">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-168">Run Modern POS in the debugger, and test the functionality.</span></span>

4. <span data-ttu-id="9aaea-169">クラウド POS コンポーネントの拡張。</span><span class="sxs-lookup"><span data-stu-id="9aaea-169">Extend the Cloud POS component:</span></span>

    1. <span data-ttu-id="9aaea-170">**RetailSdk\POS\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-170">Open the solution at **RetailSdk\POS\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
    2. <span data-ttu-id="9aaea-171">**Pos.Extensions** プロジェクトの **FiscalRegisterSample** を含めます。</span><span class="sxs-lookup"><span data-stu-id="9aaea-171">Include **FiscalRegisterSample** in the **Pos.Extensions** project.</span></span>
    3. <span data-ttu-id="9aaea-172">除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-172">Enable the extension to be compiled in **tsconfig.json** by removing the **FiscalRegisterSample** folder from the exclude list.</span></span>
    3. <span data-ttu-id="9aaea-173">適切な場所に次の行を追加して、**InternalExtensions\extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-173">Enable the extension in **InternalExtensions\extensions.json** by adding the following lines in the appropriate place.</span></span>

        ``` json
        {
            "debugBuildsOnly": false,
            "baseUrl": "FiscalRegisterSample"
        }
        ```

    4. <span data-ttu-id="9aaea-174">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-174">Rebuild the solutions.</span></span>
    5. <span data-ttu-id="9aaea-175">**実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-175">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>
    6. <span data-ttu-id="9aaea-176">機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-176">Test the functionality.</span></span>

5. <span data-ttu-id="9aaea-177">小売用バックオフィスで、会計登録構成と、その他の必要なパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-177">Set up the fiscal register configuration and other required parameters in Retail headquarters.</span></span> <span data-ttu-id="9aaea-178">詳細については、「[スウェーデンのキャッシュ レジスター](emea-swe-cash-registers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9aaea-178">For more information, see [Cash registers for Sweden](emea-swe-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="9aaea-179">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="9aaea-179">Production environment</span></span>

<span data-ttu-id="9aaea-180">以下の手順に従い、実稼働環境で小売コンポーネントを含む配置可能パッケージを作成して適用します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-180">Follow these steps to create and apply deployable packages that contain Retail components in a production environment.</span></span>

1. <span data-ttu-id="9aaea-181">POS コンポーネントの拡張</span><span class="sxs-lookup"><span data-stu-id="9aaea-181">Extend the POS component</span></span>

    1. <span data-ttu-id="9aaea-182">除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-182">Enable the extension to be compiled in **tsconfig.json** by removing the **FiscalRegisterSample** folder from the exclude list.</span></span>
    2. <span data-ttu-id="9aaea-183">適切な場所に次の行を追加して、**InternalExtensions\extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9aaea-183">Enable the extension in **InternalExtensions\extensions.json** by adding the following lines in the appropriate place.</span></span>

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

1. <span data-ttu-id="9aaea-184">**RetailSdk\Assets** フォルダーのパッケージ構成ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="9aaea-184">Make the following changes in the package config files under the **RetailSdk\Assets** folder:</span></span>

    1. <span data-ttu-id="9aaea-185">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** 構成ファイルの **構成** セクションに、次のセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-185">Add the following section to the **composition** section of the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** config files.</span></span>

        ``` xml
        <add source="type" value="Contoso.Commerce.Runtime.FiscalRegisterReceipt, Contoso.Commerce.Runtime.FiscalRegisterReceipt" />
        ```

    2. <span data-ttu-id="9aaea-186">ハードウェア ステーション構成ファイルの **構成** セクションに、次のセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-186">Add the following section to the **composition** section of the Hardware station configuration file.</span></span>

        # <a name="retail-73-and-earliertabretail-7-3"></a>[<span data-ttu-id="9aaea-187">Retail 7.3 以前</span><span class="sxs-lookup"><span data-stu-id="9aaea-187">Retail 7.3 and earlier</span></span>](#tab/retail-7-3)

        <span data-ttu-id="9aaea-188">**HardwareStation.Shared.config** および **HardwareStation.Dedicated.config** 構成ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-188">Modify the **HardwareStation.Shared.config** and **HardwareStation.Dedicated.config** configuration files.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

        # <a name="retail-731-and-latertabretail-7-3-1"></a>[<span data-ttu-id="9aaea-189">Retail 7.3.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="9aaea-189">Retail 7.3.1 and later</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="9aaea-190">**HardwareStation.Extension.config** 構成ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-190">Modify the **HardwareStation.Extension.config** configuration file:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

        ---

2. <span data-ttu-id="9aaea-191">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-191">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
3. <span data-ttu-id="9aaea-192">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="9aaea-192">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="9aaea-193">詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9aaea-193">For more information, see [Retail SDK packaging](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>

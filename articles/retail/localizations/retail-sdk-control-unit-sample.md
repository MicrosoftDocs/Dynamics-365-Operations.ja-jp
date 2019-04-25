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
ms.openlocfilehash: b5c33ec0a3b88fca62181da06e03e4a8fa0b3fd9
ms.sourcegitcommit: b5e2835e2245414837b7b37056af228dd000f756
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/20/2019
ms.locfileid: "879866"
---
# <a name="sample-for-retail-pos-integration-with-control-units-for-sweden"></a><span data-ttu-id="72043-103">スウェーデン用の管理単位との Retail POS の統合</span><span class="sxs-lookup"><span data-stu-id="72043-103">Sample for Retail POS integration with control units for Sweden</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72043-104">**サンプル コードの通知**</span><span class="sxs-lookup"><span data-stu-id="72043-104">**SAMPLE CODE NOTICE**</span></span>

<span data-ttu-id="72043-105">**このサンプルコードは現状のまま利用可能です。明示的または黙示的を問わず、特定の目的への適合性、正確性、完全性、結果、または商品性の条件に関して、Microsoft は一切保証しません。このサンプル コードの使用またはその結果に対するリスクは、すべてお客様が負うものとします。**</span><span class="sxs-lookup"><span data-stu-id="72043-105">**THIS SAMPLE CODE IS MADE AVAILABLE AS IS.  MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED, OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.  THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.**</span></span>

<span data-ttu-id="72043-106">**技術サポートは提供されません。コード配布を許可する Microsoft の使用許諾契約がない限り、このコードを配布することはできません。**</span><span class="sxs-lookup"><span data-stu-id="72043-106">**NO TECHNICAL SUPPORT IS PROVIDED.  YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.**</span></span>

<span data-ttu-id="72043-107">このサンプルでは、Retail Modern POS または クラウド POS を会計登録と統合する Microsoft Dynamics 365 for Retail 拡張機能を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="72043-107">This sample shows how to create Microsoft Dynamics 365 for Retail extensions to integrate Retail Modern POS or Cloud POS with a fiscal register.</span></span> <span data-ttu-id="72043-108">特に、このサンプルには Microsoft Dynamics for Retail POS をスウェーデンの管理単位と統合するコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="72043-108">Specifically, this sample includes the code for integrating Microsoft Dynamics for Retail POS with control units for Sweden.</span></span> <span data-ttu-id="72043-109">たとえば、このサンプルでは Retail Innovation HTT AB の CleanCash® Type A 管理単位のアプリケーション プログラミング インターフェイス (API) を使用します。</span><span class="sxs-lookup"><span data-stu-id="72043-109">As an example, this sample uses the application programming interface (API) of the CleanCash® Type A control unit by Retail Innovation HTT AB.</span></span> <span data-ttu-id="72043-110">CleanCash® API のバージョン1.1.4 が使用されます。</span><span class="sxs-lookup"><span data-stu-id="72043-110">Version 1.1.4 of the CleanCash® API is used.</span></span> <span data-ttu-id="72043-111">API およびドキュメントを含む統合パッケージについては、デバイスの製造元に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="72043-111">For the integration package that includes the API and documentation, contact the manufacturer of the device.</span></span>

<span data-ttu-id="72043-112">このサンプルは、Retail ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="72043-112">This sample is a part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="72043-113">Retail SDK をダウンロードして使用する方法については、[Retail SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72043-113">For information about how to install and use the Retail SDK, see the [Retail SDK documentation](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="72043-114">このサンプルは、ハードウェア ステーション、Commerce Runtime (CRT)、および 販売時点管理 (POS) で構成されます。</span><span class="sxs-lookup"><span data-stu-id="72043-114">This sample consists of extensions for the Hardware station, commerce runtime (CRT), and point of sale (POS).</span></span> <span data-ttu-id="72043-115">このサンプルを実行するには、ハードウェア ステーション、CRT、および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72043-115">To run this sample, you must modify and build the Hardware station, CRT, and POS projects.</span></span> <span data-ttu-id="72043-116">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="72043-116">We recommend that use you an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="72043-117">ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="72043-117">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>


> [!NOTE]
> <span data-ttu-id="72043-118">使用している Microsoft Dynamics 365 for Retail のバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="72043-118">Some steps in the procedures in this topic differ, depending on the version of Microsoft Dynamics 365 for Retail that you're using.</span></span> <span data-ttu-id="72043-119">詳細については、 [Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72043-119">For more information, see [What's new or changed in Dynamics 365 for Retail](../get-started/whats-new.md).</span></span>

## <a name="development-environment"></a><span data-ttu-id="72043-120">開発環境</span><span class="sxs-lookup"><span data-stu-id="72043-120">Development environment</span></span>

<span data-ttu-id="72043-121">サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="72043-121">Follow these steps to set up a development environment so that you can test and extend the sample.</span></span>

1. <span data-ttu-id="72043-122">ハードウェア ステーション コンポーネントを拡張します。</span><span class="sxs-lookup"><span data-stu-id="72043-122">Extend the Hardware station component:</span></span>

   1. <span data-ttu-id="72043-123">**RetailSDK\SampleExtensions\HardwareStation** で ハードウェア ステーション ソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="72043-123">Open the Hardware station solution under **RetailSDK\SampleExtensions\HardwareStation**.</span></span>
   2. <span data-ttu-id="72043-124">**HardwareStation.Extension.FiscalRegisterSample.csproj** 拡張機能プロジェクトを検索し、コンパイルします。</span><span class="sxs-lookup"><span data-stu-id="72043-124">Find the **HardwareStation.Extension.FiscalRegisterSample.csproj** extension project, and compile it.</span></span>
   3. <span data-ttu-id="72043-125">拡張機能アセンブリおよび設定を検索します。</span><span class="sxs-lookup"><span data-stu-id="72043-125">Find extension assemblies and configurations.</span></span>
      # <a name="retail-73-and-earliertabretail-7-3"></a>[<span data-ttu-id="72043-126">Retail 7.3 以前</span><span class="sxs-lookup"><span data-stu-id="72043-126">Retail 7.3 and earlier</span></span>](#tab/retail-7-3)

      <span data-ttu-id="72043-127">**Extension.FiscalRegisterSample\bin\Debug** で以下のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="72043-127">Find the following files in **Extension.FiscalRegisterSample\bin\Debug**:</span></span>

       - <span data-ttu-id="72043-128">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="72043-128">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** assembly</span></span>
       - <span data-ttu-id="72043-129">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="72043-129">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** configuration</span></span>
       - <span data-ttu-id="72043-130">**Interop.CleanCash_1_1.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="72043-130">The **Interop.CleanCash_1_1.dll** assembly</span></span>

      # <a name="retail-731-and-latertabretail-7-3-1"></a>[<span data-ttu-id="72043-131">Retail 7.3.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="72043-131">Retail 7.3.1 and later</span></span>](#tab/retail-7-3-1)

      <span data-ttu-id="72043-132">**Extension.FiscalRegisterSample\bin\Debug** で以下のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="72043-132">Find the following files in **Extension.FiscalRegisterSample\bin\Debug**:</span></span>

       - <span data-ttu-id="72043-133">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="72043-133">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** assembly</span></span>
       - <span data-ttu-id="72043-134">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="72043-134">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** configuration</span></span>
       - <span data-ttu-id="72043-135">**Interop.CleanCash_1_1.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="72043-135">The **Interop.CleanCash_1_1.dll** assembly</span></span>

      # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="72043-136">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="72043-136">Retail 10.0 and later</span></span>](#tab/retail-10-0)

      <span data-ttu-id="72043-137">**Extension.FiscalRegisterSample\bin\Debug** で以下のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="72043-137">Find the following files in **Extension.FiscalRegisterSample\bin\Debug**:</span></span>

       - <span data-ttu-id="72043-138">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="72043-138">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** assembly</span></span>
       - <span data-ttu-id="72043-139">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="72043-139">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** configuration</span></span>      
      
      <span data-ttu-id="72043-140">**RetailSDK\References\Microsoft.Dynamics.Commerce.CleanCashInterop.1.0.1\lib\net451** にて次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="72043-140">Find the following file in **RetailSDK\References\Microsoft.Dynamics.Commerce.CleanCashInterop.1.0.1\lib\net451**:</span></span>

       - <span data-ttu-id="72043-141">**Interop.CleanCash_1_1.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="72043-141">The **Interop.CleanCash_1_1.dll** assembly</span></span>
    ---
   4. <span data-ttu-id="72043-142">ファイルを配置した ハードウェア ステーション マシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="72043-142">Copy the files to a deployed Hardware station machine:</span></span>

       - <span data-ttu-id="72043-143">**リモート ハードウェア ステーション:** ファイルを、Microsoft インターネット インフォメーション サービス (IIS) ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="72043-143">**Remote Hardware station:** Copy the files to the **bin** folder under the Microsoft Internet Information Services (IIS) Hardware station site location.</span></span>
       - <span data-ttu-id="72043-144">**ローカル ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="72043-144">**Local Hardware station:** Copy the files to the Modern POS client broker location.</span></span>

   5. <span data-ttu-id="72043-145">ハードウェア ステーションの拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="72043-145">Find the configuration file for Hardware station's extensions.</span></span>

      # <a name="retail-73-and-earliertabretail-7-3"></a>[<span data-ttu-id="72043-146">Retail 7.3 以前</span><span class="sxs-lookup"><span data-stu-id="72043-146">Retail 7.3 and earlier</span></span>](#tab/retail-7-3)

      <span data-ttu-id="72043-147">**リモート ハードウェア ステーション:** ファイルの名前は **hardwarestation.shared.config**で、IIS ハードウェア ステーション サイトの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="72043-147">**Remote Hardware station:** The file is named **hardwarestation.shared.config**, and it's under the IIS Hardware station site location.</span></span>

      <span data-ttu-id="72043-148">**ローカル ハードウェア ステーション:** ファイルの名前は **HardwareStation.Dedicated.config**で、Modern POS クライアント ブローカーの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="72043-148">**Local Hardware station:** The file is named **HardwareStation.Dedicated.config**, and it's under the Modern POS client broker location.</span></span>

      # <a name="retail-731-and-latertabretail-7-3-1"></a>[<span data-ttu-id="72043-149">Retail 7.3.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="72043-149">Retail 7.3.1 and later</span></span>](#tab/retail-7-3-1)

      <span data-ttu-id="72043-150">ファイルの名前は **HardwareStation.Extension.config** です。</span><span class="sxs-lookup"><span data-stu-id="72043-150">The file is named **HardwareStation.Extension.config**:</span></span>

      <span data-ttu-id="72043-151">**リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。</span><span class="sxs-lookup"><span data-stu-id="72043-151">**Remote Hardware station:** The file is located under the IIS Hardware station site location.</span></span>

      <span data-ttu-id="72043-152">**ローカル ハードウェア ステーション:** ファイルは Modern POS クライアント ブローカーの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="72043-152">**Local Hardware station:** The file is located under the Modern POS client broker location.</span></span>
      
      # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="72043-153">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="72043-153">Retail 10.0 and later</span></span>](#tab/retail-10-0)

      <span data-ttu-id="72043-154">ファイルの名前は **HardwareStation.Extension.config** です。</span><span class="sxs-lookup"><span data-stu-id="72043-154">The file is named **HardwareStation.Extension.config**:</span></span>

      <span data-ttu-id="72043-155">**リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。</span><span class="sxs-lookup"><span data-stu-id="72043-155">**Remote Hardware station:** The file is located under the IIS Hardware station site location.</span></span>

      <span data-ttu-id="72043-156">**ローカル ハードウェア ステーション:** ファイルは Modern POS クライアント ブローカーの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="72043-156">**Local Hardware station:** The file is located under the Modern POS client broker location.</span></span>

    ---

    6. <span data-ttu-id="72043-157">コンフィギュレーション ファイルの **構成** セクションに、次のセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="72043-157">Add the following section to the **composition** section of the config file.</span></span>

      # <a name="retail-73-and-earliertabretail-7-3"></a>[<span data-ttu-id="72043-158">Retail 7.3 以前</span><span class="sxs-lookup"><span data-stu-id="72043-158">Retail 7.3 and earlier</span></span>](#tab/retail-7-3)

      ``` xml
      <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
      ```

      # <a name="retail-731-and-latertabretail-7-3-1"></a>[<span data-ttu-id="72043-159">Retail 7.3.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="72043-159">Retail 7.3.1 and later</span></span>](#tab/retail-7-3-1)

      ``` xml
      <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
      ```
        
      # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="72043-160">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="72043-160">Retail 10.0 and later</span></span>](#tab/retail-10-0)

      ``` xml
      <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
      ```
    ---

    7. <span data-ttu-id="72043-161">ハードウェア ステーション サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="72043-161">Restart the Hardware station service:</span></span>

        - <span data-ttu-id="72043-162">**リモート ハードウェア ステーション:** IIS マネージャーからハードウェア ステーション サイトを再起動します。</span><span class="sxs-lookup"><span data-stu-id="72043-162">**Remote Hardware station:** Restart the Hardware station site from IIS Manager.</span></span>
        - <span data-ttu-id="72043-163">**ローカル ハードウェア ステーション:** タスク マネージャーで **dllhost.exe** プロセスを終了して、Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="72043-163">**Local Hardware station:** End the **dllhost.exe** process in Task Manager, and then restart Modern POS.</span></span>

2. <span data-ttu-id="72043-164">CRT コンポーネントの拡張。</span><span class="sxs-lookup"><span data-stu-id="72043-164">Extend the CRT component:</span></span>

   1. <span data-ttu-id="72043-165">**RetailSdk\SampleExtensions\CommerceRuntime** の下の、CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="72043-165">Open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\SampleExtensions\CommerceRuntime**.</span></span>
   2. <span data-ttu-id="72043-166">**Runtime.Extensions.FiscalRegisterReceiptSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="72043-166">Find the **Runtime.Extensions.FiscalRegisterReceiptSample** project, and build it.</span></span>
   3. <span data-ttu-id="72043-167">CRT の ext.config ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="72043-167">Find the ext.config file for CRT:</span></span>

       - <span data-ttu-id="72043-168">**小売サーバー:** ファイルは **commerceRuntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="72043-168">**Retail Server:** The file is named **commerceRuntime.ext.config**, and it's under the **bin\ext** folder under the IIS Retail server site location.</span></span>
       - <span data-ttu-id="72043-169">**Modern POS のローカル CRT:** ファイルの名前は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーの場所の **bin\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="72043-169">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the **bin\ext** folder under the local CRT client broker location.</span></span>

   4. <span data-ttu-id="72043-170">コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="72043-170">Register the CRT change in the configuration file.</span></span>

       ``` xml
       <add source="type" value="Contoso.Commerce.Runtime.FiscalRegisterReceipt, Contoso.Commerce.Runtime.FiscalRegisterReceipt" />
       ```

       > [!NOTE]
       > <span data-ttu-id="72043-171">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="72043-171">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="72043-172">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="72043-172">These files aren't intended for any customizations.</span></span>

   5. <span data-ttu-id="72043-173">**Extensions.FiscalRegisterReceiptSample\bin\Debug** で、**Contoso.Commerce.Runtime.FiscalRegisterReceiptSample.dll** アセンブリを検索します。</span><span class="sxs-lookup"><span data-stu-id="72043-173">Find the **Contoso.Commerce.Runtime.FiscalRegisterReceiptSample.dll** assembly file in **Extensions.FiscalRegisterReceiptSample\bin\Debug**.</span></span>
   6. <span data-ttu-id="72043-174">アセンブリを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="72043-174">Copy the assembly to the CRT extensions folder:</span></span>

       - <span data-ttu-id="72043-175">**Retail サーバー:** IIS 小売サーバー サイトの場所の **\bin\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="72043-175">**Retail Server:** Copy the assembly to the **\bin\ext** folder under the IIS Retail server site location.</span></span>
       - <span data-ttu-id="72043-176">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="72043-176">**Local CRT on Modern POS:** Copy the assembly to the **\ext** folder under the local CRT client broker location.</span></span>

      > [!NOTE]
      > <span data-ttu-id="72043-177">CRT と Retail サーバーのすべてのコードの変更は、RetailSdk\SampleExtensions の一部です。</span><span class="sxs-lookup"><span data-stu-id="72043-177">All the code changes for CRT and Retail Server are all part of RetailSdk\SampleExtensions.</span></span> <span data-ttu-id="72043-178">したがって、上記の手順は、これらのコードの変更を構築、配置、およびテストする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="72043-178">Therefore, the preceding steps show how to build, deploy, and test these code changes.</span></span>

3. <span data-ttu-id="72043-179">Modern POS コンポーネントの拡張。</span><span class="sxs-lookup"><span data-stu-id="72043-179">Extend the Modern POS component:</span></span>

    1. <span data-ttu-id="72043-180">**RetailSdk\POS\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="72043-180">Open the solution at **RetailSdk\POS\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="72043-181">また、Modern POS が **Run** コマンドを使用して、Microsoft Visual Studio から実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="72043-181">Also make sure that Modern POS can be run from Microsoft Visual Studio using the **Run** command.</span></span> <span data-ttu-id="72043-182">(Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="72043-182">(Modern POS must not be customized.</span></span> <span data-ttu-id="72043-183">ユーザー アカウント制御 [UAC] を有効にして、必要に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。)</span><span class="sxs-lookup"><span data-stu-id="72043-183">You must enable User Account Control [UAC], and you must uninstall previously installed instances of Modern POS as required.)</span></span>
    2. <span data-ttu-id="72043-184">**Pos.Extensions** プロジェクトの **FiscalRegisterSample** を含めます。</span><span class="sxs-lookup"><span data-stu-id="72043-184">Include **FiscalRegisterSample** in the **Pos.Extensions** project.</span></span>
    3. <span data-ttu-id="72043-185">除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="72043-185">Enable the extension to be compiled in **tsconfig.json** by removing the **FiscalRegisterSample** folder from the exclude list.</span></span>
    3. <span data-ttu-id="72043-186">**InternalExtensions\extensions.json** にて拡張機能を有効にします。次に示す行を適切な箇所に追加します。</span><span class="sxs-lookup"><span data-stu-id="72043-186">Enable the extension in **Extensions\extensions.json** by adding the following lines in the appropriate place.</span></span>

        ``` json
        {
            "debugBuildsOnly": false,
            "baseUrl": "FiscalRegisterSample"
        }
        ```

    4. <span data-ttu-id="72043-187">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="72043-187">Rebuild the solutions.</span></span>
    5. <span data-ttu-id="72043-188">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="72043-188">Run Modern POS in the debugger, and test the functionality.</span></span>

4. <span data-ttu-id="72043-189">クラウド POS コンポーネントの拡張。</span><span class="sxs-lookup"><span data-stu-id="72043-189">Extend the Cloud POS component:</span></span>

    1. <span data-ttu-id="72043-190">**RetailSdk\POS\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="72043-190">Open the solution at **RetailSdk\POS\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
    2. <span data-ttu-id="72043-191">**Pos.Extensions** プロジェクトの **FiscalRegisterSample** を含めます。</span><span class="sxs-lookup"><span data-stu-id="72043-191">Include **FiscalRegisterSample** in the **Pos.Extensions** project.</span></span>
    3. <span data-ttu-id="72043-192">除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="72043-192">Enable the extension to be compiled in **tsconfig.json** by removing the **FiscalRegisterSample** folder from the exclude list.</span></span>
    3. <span data-ttu-id="72043-193">**InternalExtensions\extensions.json** にて拡張機能を有効にします。次に示す行を適切な箇所に追加します。</span><span class="sxs-lookup"><span data-stu-id="72043-193">Enable the extension in **Extensions\extensions.json** by adding the following lines in the appropriate place.</span></span>

        ``` json
        {
            "debugBuildsOnly": false,
            "baseUrl": "FiscalRegisterSample"
        }
        ```

    4. <span data-ttu-id="72043-194">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="72043-194">Rebuild the solutions.</span></span>
    5. <span data-ttu-id="72043-195">**実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="72043-195">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>
    6. <span data-ttu-id="72043-196">機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="72043-196">Test the functionality.</span></span>

5. <span data-ttu-id="72043-197">小売用バックオフィスで、会計登録構成と、その他の必要なパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="72043-197">Set up the fiscal register configuration and other required parameters in Retail headquarters.</span></span> <span data-ttu-id="72043-198">詳細については、「[スウェーデンのキャッシュ レジスター](emea-swe-cash-registers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72043-198">For more information, see [Cash registers for Sweden](emea-swe-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="72043-199">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="72043-199">Production environment</span></span>

<span data-ttu-id="72043-200">以下の手順に従い、実稼働環境で小売コンポーネントを含む配置可能パッケージを作成して適用します。</span><span class="sxs-lookup"><span data-stu-id="72043-200">Follow these steps to create and apply deployable packages that contain Retail components in a production environment.</span></span>

1. <span data-ttu-id="72043-201">POS コンポーネントの拡張</span><span class="sxs-lookup"><span data-stu-id="72043-201">Extend the POS component</span></span>

    1. <span data-ttu-id="72043-202">除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="72043-202">Enable the extension to be compiled in **tsconfig.json** by removing the **FiscalRegisterSample** folder from the exclude list.</span></span>
    2. <span data-ttu-id="72043-203">**InternalExtensions\extensions.json** にて拡張機能を有効にします。次に示す行を適切な箇所に追加します。</span><span class="sxs-lookup"><span data-stu-id="72043-203">Enable the extension in **Extensions\extensions.json** by adding the following lines in the appropriate place.</span></span>

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

1. <span data-ttu-id="72043-204">**RetailSdk\Assets** フォルダーのパッケージ構成ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="72043-204">Make the following changes in the package config files under the **RetailSdk\Assets** folder:</span></span>

    1. <span data-ttu-id="72043-205">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** 構成ファイルの **構成** セクションに、次のセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="72043-205">Add the following section to the **composition** section of the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** config files.</span></span>

        ``` xml
        <add source="type" value="Contoso.Commerce.Runtime.FiscalRegisterReceipt, Contoso.Commerce.Runtime.FiscalRegisterReceipt" />
        ```

    2. <span data-ttu-id="72043-206">ハードウェア ステーション構成ファイルの **構成** セクションに、次のセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="72043-206">Add the following section to the **composition** section of the Hardware station configuration file.</span></span>

        # <a name="retail-73-and-earliertabretail-7-3"></a>[<span data-ttu-id="72043-207">Retail 7.3 以前</span><span class="sxs-lookup"><span data-stu-id="72043-207">Retail 7.3 and earlier</span></span>](#tab/retail-7-3)

        <span data-ttu-id="72043-208">**HardwareStation.Shared.config** および **HardwareStation.Dedicated.config** 構成ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="72043-208">Modify the **HardwareStation.Shared.config** and **HardwareStation.Dedicated.config** configuration files.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

        # <a name="retail-731-and-latertabretail-7-3-1"></a>[<span data-ttu-id="72043-209">Retail 7.3.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="72043-209">Retail 7.3.1 and later</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="72043-210">**HardwareStation.Extension.config** 構成ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="72043-210">Modify the **HardwareStation.Extension.config** configuration file:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```
        
        # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="72043-211">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="72043-211">Retail 10.0 and later</span></span>](#tab/retail-10-0)

        <span data-ttu-id="72043-212">**HardwareStation.Extension.config** 構成ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="72043-212">Modify the **HardwareStation.Extension.config** configuration file:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
        ```
        ---

2. <span data-ttu-id="72043-213">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="72043-213">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
3. <span data-ttu-id="72043-214">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="72043-214">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="72043-215">詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72043-215">For more information, see [Retail SDK packaging](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>

---
title: ノルウェーのキャッシュ レジスタの配置ガイドライン
description: このトピックは、ノルウェーのローカライズ用配置ガイドです。
author: AlexChern0v
manager: olegkl
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.search.region: Norway
ms.search.industry: Retail
ms.author: v-alexec
ms.search.validFrom: 2018-2-28
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: c96d1f7cd1170c41f16307b704920ffba83e7bc0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004680"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a><span data-ttu-id="8b7c5-103">ノルウェーのキャッシュ レジスタの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="8b7c5-103">Deployment guidelines for cash registers for Norway</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b7c5-104">このトピックは、Dynamics 365 Commerce のノルウェーでのローカライズを有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-104">This topic is a deployment guide that shows how to enable the Dynamics 365 Commerce localization for Norway.</span></span> <span data-ttu-id="8b7c5-105">ローカライズは、コマース コンポーネントのいくつかの拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-105">The localization consists of several extensions of Commerce components.</span></span> <span data-ttu-id="8b7c5-106">たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、および販売時点管理 (POS) での支払取引を登録、デジタル署名販売取引、およびローカルの形式で X および Z レポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-106">For example, the extensions let you print custom fields on receipts, register additional audit events, sales transactions, and payment transactions in Point of Sale (POS), digitally sign sales transactions, and print X and Z reports in local formats.</span></span> <span data-ttu-id="8b7c5-107">ノルウェーのローカライズの詳細については、 [ノルウェーのキャッシュ レジスター機能](./emea-nor-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-107">For more information about the localization for Norway, see [Cash register functionality for Norway](./emea-nor-cash-registers.md).</span></span>

<span data-ttu-id="8b7c5-108">このサンプルは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-108">This sample is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="8b7c5-109">SDK に関する詳細については、[Retail ソフトウエア開発キット (SDK) アーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-109">For information about the SDK, see the [Retail software development kit (SDK) architecture](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="8b7c5-110">このサンプルは Commerce runtime (CRT)、Retail Server、そして POS の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-110">This sample consists of extensions for the Commerce runtime (CRT), Retail Server, and POS.</span></span> <span data-ttu-id="8b7c5-111">このサンプルを実行するには、CRT、Retail Servers および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-111">To run this sample, you must modify and build the CRT, Retail Server, and POS projects.</span></span> <span data-ttu-id="8b7c5-112">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-112">We recommend that you use an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="8b7c5-113">ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-113">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE]
> <span data-ttu-id="8b7c5-114">Commerce 10.0.8 およびそれ以降では、Retail Server は Commerce Scale Unit と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-114">In Commerce 10.0.8 and above, Retail Server is known as Commerce Scale Unit.</span></span> <span data-ttu-id="8b7c5-115">このトピックは、アプリの以前の複数のバージョンに適用されるため、このトピック全体で *Retail サーバー*を使用します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-115">Because this topic applies to multiple previous versions of the app, *Retail Server* is used throughout the topic.</span></span>

> [!NOTE]
> <span data-ttu-id="8b7c5-116">使用しているコマースのバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-116">Some steps in the procedures in this topic differ, depending on the version of Commerce that you're using.</span></span> <span data-ttu-id="8b7c5-117">詳細については、 [Dynamics 365 Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-117">For more information, see [What's new or changed in Dynamics 365 Retail](../get-started/whats-new.md).</span></span>

## <a name="development-environment"></a><span data-ttu-id="8b7c5-118">開発環境</span><span class="sxs-lookup"><span data-stu-id="8b7c5-118">Development environment</span></span>

<span data-ttu-id="8b7c5-119">サンプルをテストして拡張できるように開発環境を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-119">Complete these procedures to set up a development environment so that you can test and extend the sample.</span></span>

### <a name="the-crt-extension-components"></a><span data-ttu-id="8b7c5-120">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-120">The CRT extension components</span></span>

<span data-ttu-id="8b7c5-121">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-121">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="8b7c5-122">次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-122">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

#### <a name="receiptsnorway-component"></a><span data-ttu-id="8b7c5-123">ReceiptsNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-123">ReceiptsNorway component</span></span>

1. <span data-ttu-id="8b7c5-124">**Runtime.Extensions.ReceiptsNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-124">Find the **Runtime.Extensions.ReceiptsNorway** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-125">**Extensions.ReceiptsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.ReceiptsNorway.dll** アセンブリファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-125">In the **Extensions.ReceiptsNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.ReceiptsNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-126">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-126">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-127">**Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-127">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-128">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-128">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-129">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-129">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-130">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-130">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-131">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-131">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-132">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-132">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-133">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-133">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-134">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-134">These files aren't intended for any customizations.</span></span>

#### <a name="salespaymenttransext-component"></a><span data-ttu-id="8b7c5-135">SalesPaymentTransExt コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-135">SalesPaymentTransExt component</span></span>

1. <span data-ttu-id="8b7c5-136">**Runtime.Extensions.SalesPaymentTransExt** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-136">Find the **Runtime.Extensions.SalesPaymentTransExt** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-137">**Extensions.SalesPaymentTransExt\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-137">In the **Extensions.SalesPaymentTransExt\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-138">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-138">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-139">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-139">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-140">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-140">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-141">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-141">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-142">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-142">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-143">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-143">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-144">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-144">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-145">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-145">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-146">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-146">These files aren't intended for any customizations.</span></span>

#### <a name="xzreportsnorway-component"></a><span data-ttu-id="8b7c5-147">XZReportsNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-147">XZReportsNorway component</span></span>

1. <span data-ttu-id="8b7c5-148">**Runtime.Extensions.XZReportsNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-148">Find the **Runtime.Extensions.XZReportsNorway** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-149">**Extensions.XZReportsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.XZReportsNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-149">In the **Extensions.XZReportsNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.XZReportsNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-150">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-150">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-151">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-151">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-152">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-152">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-153">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-153">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-154">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-154">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-155">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-155">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-156">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-156">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-157">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-157">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-158">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-158">These files aren't intended for any customizations.</span></span>

# <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-159">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-159">Application update 4</span></span>](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="8b7c5-160">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-160">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="8b7c5-161">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-161">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-162">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-162">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-163">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-163">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-164">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-164">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-165">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-165">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-166">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-166">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-167">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-167">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-168">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-168">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-169">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-169">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-170">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-170">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-171">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-171">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="8b7c5-172">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-172">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="8b7c5-173">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-173">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="8b7c5-174">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-174">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="8b7c5-175">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-175">Build the project.</span></span>
4. <span data-ttu-id="8b7c5-176">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-176">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="8b7c5-177">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-177">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="8b7c5-178">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-178">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="8b7c5-179">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-179">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-180">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-180">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-181">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-181">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="8b7c5-182">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-182">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-183">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-183">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-184">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-184">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="8b7c5-185">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-185">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-186">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-186">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-187">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-187">These files aren't intended for any customizations.</span></span>

# <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-188">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-188">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="8b7c5-189">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-189">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="8b7c5-190">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-190">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-191">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-191">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-192">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-192">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-193">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-193">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-194">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-194">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-195">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-195">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-196">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-196">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-197">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-197">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-198">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-198">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-199">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-199">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-200">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-200">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="8b7c5-201">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-201">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="8b7c5-202">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-202">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="8b7c5-203">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-203">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="8b7c5-204">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-204">Build the project.</span></span>
4. <span data-ttu-id="8b7c5-205">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-205">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="8b7c5-206">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-206">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="8b7c5-207">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-207">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="8b7c5-208">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-208">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-209">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-209">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-210">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-210">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="8b7c5-211">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-211">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-212">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-212">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-213">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-213">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="8b7c5-214">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-214">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-215">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-215">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-216">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-216">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturesamplemessages-component"></a><span data-ttu-id="8b7c5-217">SalesTransactionSignatureSample.Messages コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-217">SalesTransactionSignatureSample.Messages component</span></span>

1. <span data-ttu-id="8b7c5-218">**Runtime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-218">Find the **Runtime.Extensions.SalesTransactionSignatureSample.Messages** project.</span></span>
2. <span data-ttu-id="8b7c5-219">**Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-219">In the **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-220">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-220">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-221">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-221">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-222">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-222">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-223">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-223">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-224">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-224">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-225">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-225">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-226">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-226">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-227">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-227">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-228">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-228">These files aren't intended for any customizations.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="8b7c5-229">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-229">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="8b7c5-230">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-230">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="8b7c5-231">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-231">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-232">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-232">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-233">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-233">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-234">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-234">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-235">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-235">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-236">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-236">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-237">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-237">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-238">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-238">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-239">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-239">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-240">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-240">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-241">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-241">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="8b7c5-242">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-242">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="8b7c5-243">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-243">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="8b7c5-244">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-244">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="8b7c5-245">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-245">Build the project.</span></span>
4. <span data-ttu-id="8b7c5-246">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-246">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="8b7c5-247">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-247">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="8b7c5-248">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-248">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="8b7c5-249">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-249">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-250">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-250">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-251">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-251">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="8b7c5-252">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-252">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-253">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-253">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-254">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-254">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="8b7c5-255">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-255">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-256">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-256">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-257">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-257">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="8b7c5-258">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-258">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="8b7c5-259">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-259">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="8b7c5-260">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-260">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-261">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-261">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-262">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-262">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-263">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-263">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-264">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-264">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="8b7c5-265">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-265">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="8b7c5-266">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-266">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-267">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-267">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-268">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-268">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-269">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-269">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-270">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-270">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-271">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-271">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-272">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-272">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-273">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-273">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-274">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-274">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-275">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-275">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-276">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-276">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="8b7c5-277">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-277">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="8b7c5-278">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-278">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="8b7c5-279">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-279">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="8b7c5-280">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-280">Build the project.</span></span>
4. <span data-ttu-id="8b7c5-281">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-281">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="8b7c5-282">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-282">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="8b7c5-283">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-283">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="8b7c5-284">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-284">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-285">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-285">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-286">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-286">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="8b7c5-287">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-287">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-288">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-288">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-289">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-289">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="8b7c5-290">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-290">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-291">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-291">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-292">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-292">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="8b7c5-293">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-293">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="8b7c5-294">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-294">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="8b7c5-295">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-295">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-296">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-296">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-297">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-297">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-298">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-298">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-299">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-299">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-300">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-300">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-301">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-301">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-302">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-302">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-303">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-303">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-304">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-304">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="8b7c5-305">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-305">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="8b7c5-306">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-306">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="8b7c5-307">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-307">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-308">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-308">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-309">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-309">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-310">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-310">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="8b7c5-311">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-311">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="8b7c5-312">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-312">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-313">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-313">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-314">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-314">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-315">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-315">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-316">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-316">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-317">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-317">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-318">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-318">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-319">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-319">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-320">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-320">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-321">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-321">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-322">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-322">These files aren't intended for any customizations.</span></span>

# <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-323">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-323">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a><span data-ttu-id="8b7c5-324">RegisterAuditEvent ノルウェイ コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-324">RegisterAuditEventNorway component</span></span>

1. <span data-ttu-id="8b7c5-325">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-325">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-326">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-326">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-327">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-327">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="8b7c5-328">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-328">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-329">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-329">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-330">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-330">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="8b7c5-331">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-331">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="8b7c5-332">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-332">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="8b7c5-333">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-333">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="8b7c5-334">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-334">Build the project.</span></span>
4. <span data-ttu-id="8b7c5-335">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-335">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="8b7c5-336">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-336">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="8b7c5-337">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-337">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="8b7c5-338">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-338">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-339">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-339">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-340">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-340">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="8b7c5-341">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-341">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-342">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-342">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-343">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-343">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="8b7c5-344">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-344">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-345">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-345">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-346">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-346">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="8b7c5-347">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-347">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="8b7c5-348">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-348">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="8b7c5-349">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-349">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-350">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-350">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-351">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-351">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-352">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-352">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-353">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-353">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-354">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-354">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-355">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-355">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-356">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-356">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-357">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-357">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-358">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-358">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="8b7c5-359">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-359">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="8b7c5-360">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-360">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="8b7c5-361">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-361">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-362">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-362">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-363">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-363">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-364">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-364">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="8b7c5-365">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-365">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="8b7c5-366">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-366">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-367">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-367">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-368">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-368">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-369">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-369">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-370">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-370">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-371">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-371">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-372">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-372">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-373">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-373">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-374">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-374">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-375">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-375">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-376">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-376">These files aren't intended for any customizations.</span></span>

# <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-377">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-377">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a><span data-ttu-id="8b7c5-378">RegisterAuditEvent ノルウェイ コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-378">RegisterAuditEventNorway component</span></span>

1. <span data-ttu-id="8b7c5-379">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-379">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-380">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-380">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-381">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-381">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="8b7c5-382">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-382">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-383">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-383">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-384">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-384">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="8b7c5-385">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-385">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="8b7c5-386">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-386">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="8b7c5-387">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-387">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="8b7c5-388">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-388">Build the project.</span></span>
4. <span data-ttu-id="8b7c5-389">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-389">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="8b7c5-390">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-390">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="8b7c5-391">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-391">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="8b7c5-392">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-392">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-393">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-393">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-394">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-394">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="8b7c5-395">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-395">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-396">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-396">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-397">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-397">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="8b7c5-398">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-398">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-399">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-399">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-400">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-400">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="8b7c5-401">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-401">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="8b7c5-402">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-402">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="8b7c5-403">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-403">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-404">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-404">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-405">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-405">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-406">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-406">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-407">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-407">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-408">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-408">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-409">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-409">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-410">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-410">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-411">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-411">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-412">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-412">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="8b7c5-413">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-413">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="8b7c5-414">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-414">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="8b7c5-415">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-415">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-416">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-416">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-417">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-417">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-418">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-418">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="8b7c5-419">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-419">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="8b7c5-420">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-420">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-421">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-421">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-422">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-422">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="8b7c5-423">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-423">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-424">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-424">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="8b7c5-425">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-425">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="8b7c5-426">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-426">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="8b7c5-427">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-427">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="8b7c5-428">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-428">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="8b7c5-429">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-429">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="8b7c5-430">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-430">These files aren't intended for any customizations.</span></span>

---

### <a name="the-retail-server-extension-components"></a><span data-ttu-id="8b7c5-431">Retail Server 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-431">The Retail Server extension components</span></span>

#### <a name="salestransactionsignature-retail-server-sample-component"></a><span data-ttu-id="8b7c5-432">SalesTransactionSignature Retail Server サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-432">SalesTransactionSignature Retail Server sample component</span></span>

1. <span data-ttu-id="8b7c5-433">**RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-433">In the **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-434">**RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.RetailServer.SalesTransactionSignatureSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-434">In the **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.RetailServer.SalesTransactionSignatureSample.dll** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-435">アセンブリ ファイルを Retail Server 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-435">Copy the assembly file to the Retail Server extensions folder.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-436">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-436">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="8b7c5-437">フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-437">The folder is the **\\bin** folder under the IIS Retail Server site location.</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-438">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-438">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="8b7c5-439">フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-439">The folder is the **\\bin** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-440">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-440">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    <span data-ttu-id="8b7c5-441">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-441">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-442">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-442">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    <span data-ttu-id="8b7c5-443">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-443">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-444">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-444">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    <span data-ttu-id="8b7c5-445">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-445">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-446">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-446">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    <span data-ttu-id="8b7c5-447">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-447">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    ---

4. <span data-ttu-id="8b7c5-448">Retail Server のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-448">Find the configuration file for Retail Server.</span></span> <span data-ttu-id="8b7c5-449">ファイル名は **web.config** で、IIS Retail Server サイトがある場所の下のルート フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-449">The file is named **web.config**, and it's in the root folder under the IIS Retail Server site location.</span></span>
5. <span data-ttu-id="8b7c5-450">コンフィギュレーションの **extensionComposition** セクションで Retail Server 拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-450">Register the Retail Server extensions in the **extensionComposition** section of the configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. <span data-ttu-id="8b7c5-451">Retail Server 拡張機能の依存関係を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-451">Register the dependencies of the Retail Server extensions.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-452">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-452">Application update 4</span></span>](#tab/app-update-4/)

    1. <span data-ttu-id="8b7c5-453">**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-453">In the **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

        - <span data-ttu-id="8b7c5-454">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-454">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
        - <span data-ttu-id="8b7c5-455">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="8b7c5-455">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

    2. <span data-ttu-id="8b7c5-456">ファイルを、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-456">Copy the files to the **\\bin** folder under the IIS Retail Server site location.</span></span>
    3. <span data-ttu-id="8b7c5-457">CRT用拡張機能コンフィギュレーションファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-457">Register the CRT change in the extension configuration file for CRT.</span></span> <span data-ttu-id="8b7c5-458">ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-458">This file is named **commerceruntime.ext.config**, and it's in the **bin** folder under the IIS Retail Server site location.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-459">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-459">Application update 5 and later</span></span>](#tab/app-update-5-and-later/)

    1. <span data-ttu-id="8b7c5-460">**CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-460">In the **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** assembly file.</span></span>
    2. <span data-ttu-id="8b7c5-461">ファイルをIIS Retail Server サイトがある場所の **\\bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-461">Copy the file to the **\\bin** folder under the IIS Retail Server site location.</span></span>
    3. <span data-ttu-id="8b7c5-462">CRT用拡張機能コンフィギュレーションファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-462">Register the CRT change in the extension configuration file for CRT.</span></span> <span data-ttu-id="8b7c5-463">ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-463">This file is named **commerceruntime.ext.config**, and it's in the **bin** folder under the IIS Retail Server site location.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-464">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-464">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-465">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-465">No actions are required.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-466">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-466">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-467">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-467">No actions are required.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-468">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-468">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-469">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-469">No actions are required.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-470">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-470">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-471">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-471">No actions are required.</span></span>

    ---

### <a name="the-modern-pos-extension-components"></a><span data-ttu-id="8b7c5-472">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-472">The Modern POS extension components</span></span>

#### <a name="implement-the-proxy-code-for-offline-mode"></a><span data-ttu-id="8b7c5-473">オフライン モード用プロキシ コードを実装します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-473">Implement the proxy code for offline mode</span></span>

<span data-ttu-id="8b7c5-474">この箇所は Retail Server コントローラーと同じですが、クライアントが接続されていない場合に使用されるローカル CRT を拡張します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-474">This part is equivalent to the Retail Server controller, but it extends the local CRT that is used when the client isn't connected.</span></span>

1. <span data-ttu-id="8b7c5-475">**Customization.settings** ファイルで、**@(RetailServerLibraryPathForProxyGeneration)** セクションを変更し、プロキシ生成で新しい Retail Server アセンブリを使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-475">In the **customization.settings** file, change the **@(RetailServerLibraryPathForProxyGeneration)** section so that it uses the new Retail Server assembly for proxy generation.</span></span>
2. <span data-ttu-id="8b7c5-476">**StoreOperationsManager** クラスで次のインターフェイス メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-476">Implement the following interface methods in the **StoreOperationsManager** class.</span></span> <span data-ttu-id="8b7c5-477">最初の繰り返しには、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-477">For the first iteration, add the following code:</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-478">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-478">Application update 4</span></span>](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-479">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-479">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-480">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-480">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-481">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-481">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-482">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-482">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-483">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-483">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-484">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-484">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-485">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-485">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-486">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-486">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-487">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-487">This step doesn't apply to this version.</span></span>

    ---

3. <span data-ttu-id="8b7c5-488">プロキシ コードを再生成するには、コマンドラインから **msbuild/t:Rebuild** コマンドを使用して**プロキシ**フォルダーを構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-488">To regenerate the proxy code, build the **Proxies** folder from the command line by using the **msbuild /t:Rebuild** command.</span></span>
4. <span data-ttu-id="8b7c5-489">**Proxies.RetailProxy** プロジェクトの依存関係を解決します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-489">Resolve the **Proxies.RetailProxy** project dependencies:</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-490">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-490">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="8b7c5-491">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** project to reference **SalesTransactionSignatureSample** に追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-491">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, add the **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** project to the solution, and add a project reference to the **RetailProxy** project to reference **SalesTransactionSignatureSample**.</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-492">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-492">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="8b7c5-493">**RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** プロジェクトと、**SalesTransactionSignatureSample.Messages**参照に追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-493">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, add the **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** project to the solution, and add a project reference to the **RetailProxy** project to reference **SalesTransactionSignatureSample.Messages**.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-494">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-494">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-495">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-495">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-496">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-496">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-497">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-497">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-498">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-498">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-499">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-499">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-500">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-500">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-501">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-501">This step doesn't apply to this version.</span></span>

    ---

5. <span data-ttu-id="8b7c5-502">**StoreOperationsManager** クラスでインターフェイス メソッドを調節します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-502">Adjust the interface methods in the **StoreOperationsManager** class:</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-503">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-503">Application update 4</span></span>](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-504">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-504">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-505">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-505">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-506">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-506">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-507">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-507">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-508">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-508">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-509">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-509">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-510">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-510">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-511">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-511">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="8b7c5-512">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-512">This step doesn't apply to this version.</span></span>

    ---

6. <span data-ttu-id="8b7c5-513">**dllhost.exe.config** ファイルを更新し、クライアント ブローカーが新しい RetailProxy アセンブリを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-513">Update the **dllhost.exe.config** file so that the client broker loads the new RetailProxy assembly.</span></span>

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a><span data-ttu-id="8b7c5-514">小売プロキシ拡張コンポーネント (Retail 7.3.1 およびそれ以降)</span><span class="sxs-lookup"><span data-stu-id="8b7c5-514">Retail proxy extension component (Retail 7.3.1 and later)</span></span>

<span data-ttu-id="8b7c5-515">Retail 7.3.1 もしくはそれ以降を使用しているときに限り、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-515">Complete the following procedure only if you're using Retail 7.3.1 and later.</span></span>

1. <span data-ttu-id="8b7c5-516">**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample**  フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-516">In the **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="8b7c5-517">**RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-517">In the **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** assembly file.</span></span>
3. <span data-ttu-id="8b7c5-518">アセンブリ ファイルをローカル CRT クライアント ブローカーの下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-518">Copy the assembly files to the **\\ext** folder under the local CRT client broker location.</span></span>
4. <span data-ttu-id="8b7c5-519">拡張機能コンフィギュレーション ファイルで Retail プロキシの変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-519">Register the Retail proxy change in the extension configuration file.</span></span> <span data-ttu-id="8b7c5-520">ファイル名は **RetailProxy.MPOSOffline.ext.config** で、ローカル CRT クライアント ブローカーの場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-520">The file is named **RetailProxy.MPOSOffline.ext.config**, and it's under the local CRT client broker location.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a><span data-ttu-id="8b7c5-521">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-521">Modern POS extension components</span></span>

1. <span data-ttu-id="8b7c5-522">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-522">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="8b7c5-523">また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-523">Additionally, make sure that you can run Modern POS from Microsoft Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8b7c5-524">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-524">Modern POS must not be customized.</span></span> <span data-ttu-id="8b7c5-525">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-525">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

2. <span data-ttu-id="8b7c5-526">**Pos.Extensions** プロジェクトが、次の既存のソース コード フォルダーを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-526">Include the following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-527">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-527">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="8b7c5-528">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-528">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-529">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-529">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-530">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-530">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="8b7c5-531">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-531">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-532">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-532">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-533">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-533">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="8b7c5-534">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-534">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-535">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-535">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-536">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-536">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="8b7c5-537">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-537">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-538">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-538">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-539">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-539">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-540">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-540">SequentialSignature</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-541">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-541">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="8b7c5-542">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-542">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-543">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-543">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-544">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-544">SequentialSignature</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-545">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-545">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="8b7c5-546">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-546">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-547">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-547">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-548">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-548">SequentialSignature</span></span>

    ---

3. <span data-ttu-id="8b7c5-549">除外リストから次のフォルダーを削除して、**tsconfig.json** で拡張機能がコンパイルされるようにします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-549">Enable the extensions to be compiled in **tsconfig.json** by removing the following folders from the exclude list.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-550">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-550">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="8b7c5-551">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-551">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-552">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-552">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-553">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-553">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="8b7c5-554">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-554">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-555">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-555">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-556">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-556">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="8b7c5-557">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-557">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-558">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-558">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-559">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-559">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="8b7c5-560">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-560">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-561">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-561">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-562">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-562">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-563">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-563">SequentialSignature</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-564">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-564">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="8b7c5-565">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-565">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-566">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-566">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-567">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-567">SequentialSignature</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-568">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-568">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="8b7c5-569">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-569">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-570">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-570">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-571">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-571">SequentialSignature</span></span>

    ---

4. <span data-ttu-id="8b7c5-572">適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-572">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate place.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-573">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-573">Application update 4</span></span>](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-574">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-574">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-575">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-575">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-576">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-576">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-577">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-577">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-578">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-578">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > <span data-ttu-id="8b7c5-579">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-579">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="8b7c5-580">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-580">Rebuild the solution.</span></span>
6. <span data-ttu-id="8b7c5-581">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-581">Run Modern POS in the debugger, and test the functionality.</span></span>

### <a name="cloud-pos-extension-components"></a><span data-ttu-id="8b7c5-582">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8b7c5-582">Cloud POS extension components</span></span>

1. <span data-ttu-id="8b7c5-583">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-583">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="8b7c5-584">**Pos.Extensions** プロジェクトの、既存ソース コード フォルダーを含めます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-584">Include following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-585">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-585">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="8b7c5-586">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-586">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-587">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-587">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-588">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-588">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="8b7c5-589">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-589">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-590">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-590">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-591">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-591">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="8b7c5-592">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-592">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-593">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-593">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-594">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-594">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="8b7c5-595">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-595">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-596">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-596">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-597">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-597">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-598">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-598">SequentialSignature</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-599">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-599">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="8b7c5-600">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-600">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-601">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-601">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-602">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-602">SequentialSignature</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-603">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-603">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="8b7c5-604">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-604">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-605">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-605">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-606">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-606">SequentialSignature</span></span>

    ---

3. <span data-ttu-id="8b7c5-607">除外リストから次のフォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-607">Enable the extensions to be compiled in **tsconfig.json** by removing following folders from the exclude list.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-608">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-608">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="8b7c5-609">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-609">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-610">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-610">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-611">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-611">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="8b7c5-612">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-612">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-613">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-613">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-614">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-614">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="8b7c5-615">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-615">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-616">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-616">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-617">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-617">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="8b7c5-618">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-618">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="8b7c5-619">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-619">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-620">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-620">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-621">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-621">SequentialSignature</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-622">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-622">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="8b7c5-623">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-623">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-624">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-624">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-625">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-625">SequentialSignature</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-626">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-626">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="8b7c5-627">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="8b7c5-627">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="8b7c5-628">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="8b7c5-628">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="8b7c5-629">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="8b7c5-629">SequentialSignature</span></span>

    ---

4. <span data-ttu-id="8b7c5-630">適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-630">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate place.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-631">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-631">Application update 4</span></span>](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-632">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-632">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-633">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-633">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-634">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-634">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-635">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-635">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-636">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-636">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > <span data-ttu-id="8b7c5-637">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-637">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="8b7c5-638">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-638">Rebuild the solution.</span></span>
6. <span data-ttu-id="8b7c5-639">**実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-639">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>
7. <span data-ttu-id="8b7c5-640">機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-640">Test the functionality.</span></span>

### <a name="set-up-required-parameters-in-headquarters"></a><span data-ttu-id="8b7c5-641">バックオフィスで要求されるパラメーターを設定します</span><span class="sxs-lookup"><span data-stu-id="8b7c5-641">Set up required parameters in Headquarters</span></span>

<span data-ttu-id="8b7c5-642">詳細については、 [ノルウェイのキャッシュ レジスター機能](./emea-nor-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-642">For more information, see [Cash register functionality for Norway](./emea-nor-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="8b7c5-643">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="8b7c5-643">Production environment</span></span>

<span data-ttu-id="8b7c5-644">以下の手順に従い、コマース コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-644">Follow these steps to create deployable packages that contain Commerce components, and to apply those packages in a production environment.</span></span>

1. <span data-ttu-id="8b7c5-645">[クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-645">Complete the steps in the [Cloud POS extension components](#cloud-pos-extension-components) or [Modern POS extension components](#modern-pos-extension-components) section earlier in this topic.</span></span>
2. <span data-ttu-id="8b7c5-646">**RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-646">Make the following changes in the package configuration files under the **RetailSdk\\Assets** folder:</span></span>

    1. <span data-ttu-id="8b7c5-647">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの**構成**セクションに、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-647">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files, add the following lines to the **composition** section:</span></span>

        # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-648">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-648">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-649">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-649">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-650">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-650">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-651">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-651">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-652">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-652">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-653">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-653">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. <span data-ttu-id="8b7c5-654">コマース プロキシ カスタマイズを有効にします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-654">Enable Commerce Proxy customization:</span></span>

        # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-655">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-655">Application update 4</span></span>](#tab/app-update-4)

        <span data-ttu-id="8b7c5-656">**dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-656">In the **dllhost.exe.config** configuration file, add the following lines to the **appSettings** subsection of the **configuration** section.</span></span>

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-657">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-657">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        <span data-ttu-id="8b7c5-658">**dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-658">In the **dllhost.exe.config** configuration file, add the following lines to the **appSettings** subsection of the **configuration** section.</span></span>

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-659">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-659">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="8b7c5-660">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-660">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-661">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-661">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        <span data-ttu-id="8b7c5-662">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-662">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-663">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-663">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        <span data-ttu-id="8b7c5-664">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-664">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-665">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-665">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        <span data-ttu-id="8b7c5-666">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-666">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. <span data-ttu-id="8b7c5-667">**Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-667">Make the following changes in the **Customization.settings** package customization configuration file:</span></span>

    1. <span data-ttu-id="8b7c5-668">小売プロキシ カスタマイズを有効にします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-668">Enable Retail Proxy customization.</span></span>

        # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-669">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-669">Application update 4</span></span>](#tab/app-update-4)

        <span data-ttu-id="8b7c5-670">**&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-670">Add the following lines to the **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** section.</span></span>

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-671">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-671">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        <span data-ttu-id="8b7c5-672">**&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-672">Add the following lines to the **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** section.</span></span>

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-673">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-673">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="8b7c5-674">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-674">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-675">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-675">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        <span data-ttu-id="8b7c5-676">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-676">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-677">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-677">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        <span data-ttu-id="8b7c5-678">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-678">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-679">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-679">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        <span data-ttu-id="8b7c5-680">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-680">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. <span data-ttu-id="8b7c5-681">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-681">Add the following lines to the **ItemGroup** section to include the CRT extensions in the deployable packages:</span></span>

        # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-682">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-682">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-683">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-683">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-684">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-684">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-685">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-685">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-686">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-686">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-687">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-687">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. <span data-ttu-id="8b7c5-688">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに Retail Server 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-688">Add following lines to the **ItemGroup** section to include the Retail Server extension in the deployable packages:</span></span>

        # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-689">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-689">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-690">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-690">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-691">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-691">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-692">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-692">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-693">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-693">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-694">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-694">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. <span data-ttu-id="8b7c5-695">以下のファイルを修正して、配置可能なパッケージ内に ノルウェーのリソース ファイルを含めます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-695">Modify the following files to include the resource files for Norway in deployable packages:</span></span>
    - <span data-ttu-id="8b7c5-696">Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj</span><span class="sxs-lookup"><span data-stu-id="8b7c5-696">Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj</span></span>
    - <span data-ttu-id="8b7c5-697">Packages\RetailServer\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="8b7c5-697">Packages\RetailServer\Sdk.RetailServerSetup.proj</span></span>
  
  - <span data-ttu-id="8b7c5-698">**Sdk.ModernPos.Shared.csproj** ファイルの場合</span><span class="sxs-lookup"><span data-stu-id="8b7c5-698">For the **Sdk.ModernPos.Shared.csproj** file</span></span> 
    - <span data-ttu-id="8b7c5-699">**ItemGroup** セクションに新しい行を追加</span><span class="sxs-lookup"><span data-stu-id="8b7c5-699">Add line to the **ItemGroup** section</span></span>
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > <span data-ttu-id="8b7c5-700"><ファイル名> ではなく、リソース ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-700">Instead of the <File_name> specify a name of the resource file.</span></span> <span data-ttu-id="8b7c5-701">次に示す例にも同じことが当てはまります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-701">The same is relevant for the other examples given below.</span></span>
 
    - <span data-ttu-id="8b7c5-702">**Target Name="CopyPackageFiles"** セクションに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-702">Add line to the **Target Name="CopyPackageFiles"** section</span></span>
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - <span data-ttu-id="8b7c5-703">**Sdk.RetailServerSetup.proj** ファイルの場合</span><span class="sxs-lookup"><span data-stu-id="8b7c5-703">For the **Sdk.RetailServerSetup.proj** file</span></span> 
    - <span data-ttu-id="8b7c5-704">**ItemGroup** セクションに新しい行を追加</span><span class="sxs-lookup"><span data-stu-id="8b7c5-704">Add line to the **ItemGroup** section</span></span>
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - <span data-ttu-id="8b7c5-705">**Target Name="CopyPackageFiles"** セクションに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-705">Add line to the **Target Name="CopyPackageFiles"** section</span></span>
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. <span data-ttu-id="8b7c5-706">拇印、保管場所、署名販売取引に使用されるべき証明書の保存名を指定して、証明書のコンフィギュレーションを変更します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-706">Modify the certificate's configuration file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span> <span data-ttu-id="8b7c5-707">その後 **References** フォルダーにコンフィギュレーション ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-707">Then copy the configuration file to the **References** folder.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="8b7c5-708">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="8b7c5-708">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="8b7c5-709">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-709">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="8b7c5-710">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-710">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="8b7c5-711">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-711">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="8b7c5-712">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="8b7c5-712">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    <span data-ttu-id="8b7c5-713">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-713">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="8b7c5-714">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-714">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    <span data-ttu-id="8b7c5-715">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-715">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="8b7c5-716">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-716">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    <span data-ttu-id="8b7c5-717">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-717">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="8b7c5-718">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="8b7c5-718">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    <span data-ttu-id="8b7c5-719">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-719">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    ---

6. <span data-ttu-id="8b7c5-720">Retail Server コンフィギュレーション ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-720">Update Retail Server configuration file.</span></span> <span data-ttu-id="8b7c5-721">**RetailSDK\\Packages\\RetailServer\\Code\\web.config** ファイルの **extensionComposition** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-721">In the **RetailSDK\\Packages\\RetailServer\\Code\\web.config** file, add the following lines to the **extensionComposition** section.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. <span data-ttu-id="8b7c5-722">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-722">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
8. <span data-ttu-id="8b7c5-723">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-723">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="8b7c5-724">詳細については、 [小売の配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-724">For more information, see [Create retail deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a><span data-ttu-id="8b7c5-725">Modern POS のオフライン モードでのデジタル署名を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-725">Enable the digital signature in offline mode for Modern POS</span></span>

<span data-ttu-id="8b7c5-726">Modern POSでオフライン モードでのデジタル署名を有効にするには、新しい端末で Modern POS を有効化した後、これらの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-726">To enable the digital signature in offline mode for Modern POS, you must follow these steps after you activate Modern POS on a new device.</span></span>

1. <span data-ttu-id="8b7c5-727">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-727">Sign in to POS.</span></span>
2. <span data-ttu-id="8b7c5-728">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-728">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="8b7c5-729">**ダウンロードの保留中**フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-729">When the value of the **Pending downloads** field is **0** (zero), the database is fully synchronized.</span></span>
3. <span data-ttu-id="8b7c5-730">POS からのサインアウト</span><span class="sxs-lookup"><span data-stu-id="8b7c5-730">Sign out of POS.</span></span>
4. <span data-ttu-id="8b7c5-731">オフライン データベースが完全に同期するため少しの間待ちます。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-731">Wait a while for the offline database to be fully synchronized.</span></span>
5. <span data-ttu-id="8b7c5-732">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-732">Sign in to POS.</span></span>
6. <span data-ttu-id="8b7c5-733">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-733">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="8b7c5-734">**オフライン データベースで取引を保留中** フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-734">When the value of the **Pending transactions in offline database** field is **0** (zero), the database is fully synchronized.</span></span>
7. <span data-ttu-id="8b7c5-735">Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="8b7c5-735">Restart Modern POS.</span></span>

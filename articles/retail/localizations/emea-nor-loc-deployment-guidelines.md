---
title: ノルウェーのキャッシュ レジスタの配置ガイドライン
description: このトピックは、ノルウェー向け小売ローカライズ用配置ガイドです。
author: AlexChern0v
manager: olegkl
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Retail
ms.search.region: Norway
ms.search.industry: Retail
ms.author: v-alexec
ms.search.validFrom: 2018-2-28
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: 63d17a215720f8b2d3327c1fbbc0521b2f684031
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834164"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a><span data-ttu-id="91e24-103">ノルウェーのキャッシュ レジスタの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="91e24-103">Deployment guidelines for cash registers for Norway</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91e24-104">このトピックは、Microsoft Dynamics 365 for Retail のノルウェーでのローカライズを有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="91e24-104">This topic is a deployment guide that shows how to enable the Microsoft Dynamics 365 for Retail localization for Norway.</span></span> <span data-ttu-id="91e24-105">ローカライズは、小売コンポーネントのいくつかの拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="91e24-105">The localization consists of several extensions of Retail components.</span></span> <span data-ttu-id="91e24-106">たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、および販売時点管理 (POS) での支払取引を登録、デジタル署名販売取引、およびローカルの形式で X および Z レポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="91e24-106">For example, the extensions let you print custom fields on receipts, register additional audit events, sales transactions, and payment transactions in Point of Sale (POS), digitally sign sales transactions, and print X and Z reports in local formats.</span></span> <span data-ttu-id="91e24-107">ノルウェーの小売ローカライズの詳細については、[ノルウェーのキャッシュ レジスター](./emea-nor-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="91e24-107">For more information about the Retail localization for Norway, see [Cash registers for Norway](./emea-nor-cash-registers.md).</span></span>

<span data-ttu-id="91e24-108">このサンプルは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="91e24-108">This sample is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="91e24-109">リテール SDK をダウンロードして使用する方法については、[リテール SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="91e24-109">For information about how to install and use the Retail SDK, see the [Retail SDK documentation](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="91e24-110">このサンプルは Commerce runtime (CRT)、Retail Server、そして POS の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="91e24-110">This sample consists of extensions for the Commerce runtime (CRT), Retail Server, and POS.</span></span> <span data-ttu-id="91e24-111">このサンプルを実行するには、CRT、Retail Servers および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e24-111">To run this sample, you must modify and build the CRT, Retail Server, and POS projects.</span></span> <span data-ttu-id="91e24-112">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="91e24-112">We recommend that you use an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="91e24-113">ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="91e24-113">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE]
> <span data-ttu-id="91e24-114">使用しているバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="91e24-114">Some steps in the procedures in this topic differ, depending on the version of Retail that you're using.</span></span> <span data-ttu-id="91e24-115">詳細については、[Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="91e24-115">For more information, see [What's new or changed in Dynamics 365 for Retail](../get-started/whats-new.md).</span></span>

## <a name="development-environment"></a><span data-ttu-id="91e24-116">開発環境</span><span class="sxs-lookup"><span data-stu-id="91e24-116">Development environment</span></span>

<span data-ttu-id="91e24-117">サンプルをテストして拡張できるように開発環境を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="91e24-117">Complete these procedures to set up a development environment so that you can test and extend the sample.</span></span>

### <a name="the-crt-extension-components"></a><span data-ttu-id="91e24-118">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-118">The CRT extension components</span></span>

<span data-ttu-id="91e24-119">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="91e24-119">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="91e24-120">次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="91e24-120">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

#### <a name="receiptsnorway-component"></a><span data-ttu-id="91e24-121">ReceiptsNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-121">ReceiptsNorway component</span></span>

1. <span data-ttu-id="91e24-122">**Runtime.Extensions.ReceiptsNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-122">Find the **Runtime.Extensions.ReceiptsNorway** project, and build it.</span></span>
2. <span data-ttu-id="91e24-123">**Extensions.ReceiptsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.ReceiptsNorway.dll** アセンブリファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-123">In the **Extensions.ReceiptsNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.ReceiptsNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-124">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-124">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-125">**Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-125">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-126">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-126">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-127">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-127">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-128">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-128">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-129">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-129">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-130">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-130">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-131">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-131">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-132">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-132">These files aren't intended for any customizations.</span></span>

#### <a name="salespaymenttransext-component"></a><span data-ttu-id="91e24-133">SalesPaymentTransExt コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-133">SalesPaymentTransExt component</span></span>

1. <span data-ttu-id="91e24-134">**Runtime.Extensions.SalesPaymentTransExt** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-134">Find the **Runtime.Extensions.SalesPaymentTransExt** project, and build it.</span></span>
2. <span data-ttu-id="91e24-135">**Extensions.SalesPaymentTransExt\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-135">In the **Extensions.SalesPaymentTransExt\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-136">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-136">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-137">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-137">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-138">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-138">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-139">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-139">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-140">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-140">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-141">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-141">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-142">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-142">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-143">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-143">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-144">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-144">These files aren't intended for any customizations.</span></span>

#### <a name="xzreportsnorway-component"></a><span data-ttu-id="91e24-145">XZReportsNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-145">XZReportsNorway component</span></span>

1. <span data-ttu-id="91e24-146">**Runtime.Extensions.XZReportsNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-146">Find the **Runtime.Extensions.XZReportsNorway** project, and build it.</span></span>
2. <span data-ttu-id="91e24-147">**Extensions.XZReportsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.XZReportsNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-147">In the **Extensions.XZReportsNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.XZReportsNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-148">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-148">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-149">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-149">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-150">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-150">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-151">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-151">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-152">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-152">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-153">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-153">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-154">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-154">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-155">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-155">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-156">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-156">These files aren't intended for any customizations.</span></span>

# <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-157">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-157">Application update 4</span></span>](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="91e24-158">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-158">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="91e24-159">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-159">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="91e24-160">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-160">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-161">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-161">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-162">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-162">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-163">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-163">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-164">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-164">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-165">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-165">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-166">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-166">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-167">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-167">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-168">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-168">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-169">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-169">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="91e24-170">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-170">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="91e24-171">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-171">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="91e24-172">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="91e24-172">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="91e24-173">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-173">Build the project.</span></span>
4. <span data-ttu-id="91e24-174">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-174">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="91e24-175">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-175">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="91e24-176">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-176">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="91e24-177">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-177">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-178">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-178">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-179">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-179">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="91e24-180">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-180">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-181">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-181">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-182">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-182">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="91e24-183">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-183">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-184">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-184">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-185">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-185">These files aren't intended for any customizations.</span></span>

# <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-186">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-186">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="91e24-187">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-187">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="91e24-188">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-188">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="91e24-189">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-189">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-190">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-190">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-191">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-191">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-192">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-192">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-193">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-193">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-194">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-194">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-195">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-195">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-196">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-196">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-197">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-197">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-198">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-198">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="91e24-199">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-199">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="91e24-200">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-200">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="91e24-201">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="91e24-201">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="91e24-202">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-202">Build the project.</span></span>
4. <span data-ttu-id="91e24-203">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-203">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="91e24-204">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-204">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="91e24-205">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-205">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="91e24-206">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-206">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-207">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-207">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-208">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-208">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="91e24-209">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-209">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-210">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-210">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-211">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-211">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="91e24-212">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-212">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-213">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-213">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-214">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-214">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturesamplemessages-component"></a><span data-ttu-id="91e24-215">SalesTransactionSignatureSample.Messages コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-215">SalesTransactionSignatureSample.Messages component</span></span>

1. <span data-ttu-id="91e24-216">**Runtime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-216">Find the **Runtime.Extensions.SalesTransactionSignatureSample.Messages** project.</span></span>
2. <span data-ttu-id="91e24-217">**Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-217">In the **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-218">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-218">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-219">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-219">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-220">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-220">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-221">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-221">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-222">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-222">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-223">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-223">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-224">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-224">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-225">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-225">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-226">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-226">These files aren't intended for any customizations.</span></span>

# <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-227">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-227">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="91e24-228">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-228">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="91e24-229">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-229">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="91e24-230">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-230">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-231">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-231">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-232">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-232">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-233">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-233">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-234">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-234">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-235">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-235">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-236">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-236">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-237">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-237">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-238">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-238">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-239">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-239">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="91e24-240">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-240">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="91e24-241">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-241">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="91e24-242">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="91e24-242">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="91e24-243">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-243">Build the project.</span></span>
4. <span data-ttu-id="91e24-244">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-244">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="91e24-245">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-245">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="91e24-246">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-246">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="91e24-247">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-247">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-248">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-248">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-249">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-249">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="91e24-250">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-250">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-251">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-251">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-252">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-252">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="91e24-253">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-253">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-254">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-254">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-255">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-255">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="91e24-256">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-256">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="91e24-257">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-257">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="91e24-258">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-258">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-259">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-259">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-260">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-260">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-261">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-261">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

# <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-262">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-262">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="91e24-263">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-263">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="91e24-264">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-264">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="91e24-265">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-265">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-266">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-266">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-267">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-267">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-268">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-268">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-269">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-269">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-270">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-270">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-271">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-271">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-272">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-272">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-273">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-273">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-274">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-274">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="91e24-275">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-275">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="91e24-276">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-276">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="91e24-277">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="91e24-277">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="91e24-278">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-278">Build the project.</span></span>
4. <span data-ttu-id="91e24-279">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-279">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="91e24-280">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-280">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="91e24-281">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-281">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="91e24-282">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-282">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-283">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-283">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-284">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-284">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="91e24-285">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-285">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-286">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-286">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-287">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-287">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="91e24-288">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-288">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-289">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-289">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-290">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-290">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="91e24-291">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-291">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="91e24-292">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-292">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="91e24-293">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-293">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-294">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-294">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-295">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-295">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-296">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-296">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-297">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-297">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-298">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-298">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-299">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-299">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-300">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-300">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-301">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-301">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-302">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-302">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="91e24-303">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-303">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="91e24-304">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-304">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="91e24-305">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-305">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-306">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-306">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-307">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-307">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-308">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-308">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="91e24-309">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-309">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="91e24-310">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-310">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="91e24-311">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-311">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-312">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-312">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-313">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-313">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-314">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-314">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-315">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-315">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-316">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-316">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-317">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-317">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-318">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-318">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-319">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-319">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-320">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-320">These files aren't intended for any customizations.</span></span>

# <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-321">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-321">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a><span data-ttu-id="91e24-322">RegisterAuditEvent ノルウェイ コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-322">RegisterAuditEventNorway component</span></span>

1. <span data-ttu-id="91e24-323">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-323">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-324">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-324">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-325">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-325">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="91e24-326">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-326">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-327">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-327">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-328">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-328">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="91e24-329">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-329">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="91e24-330">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-330">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="91e24-331">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="91e24-331">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="91e24-332">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-332">Build the project.</span></span>
4. <span data-ttu-id="91e24-333">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-333">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="91e24-334">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-334">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="91e24-335">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-335">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="91e24-336">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-336">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-337">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-337">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-338">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-338">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="91e24-339">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-339">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-340">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-340">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-341">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-341">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="91e24-342">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-342">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-343">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-343">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-344">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-344">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="91e24-345">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-345">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="91e24-346">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-346">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="91e24-347">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-347">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-348">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-348">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-349">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-349">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-350">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-350">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-351">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-351">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-352">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-352">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-353">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-353">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-354">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-354">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-355">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-355">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-356">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-356">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="91e24-357">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-357">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="91e24-358">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-358">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="91e24-359">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-359">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-360">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-360">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-361">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-361">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-362">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-362">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="91e24-363">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-363">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="91e24-364">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-364">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="91e24-365">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-365">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-366">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-366">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-367">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-367">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-368">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-368">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-369">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-369">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-370">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-370">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-371">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-371">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-372">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-372">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-373">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-373">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-374">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-374">These files aren't intended for any customizations.</span></span>

# <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-375">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-375">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a><span data-ttu-id="91e24-376">RegisterAuditEvent ノルウェイ コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-376">RegisterAuditEventNorway component</span></span>

1. <span data-ttu-id="91e24-377">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-377">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-378">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-378">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-379">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-379">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="91e24-380">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-380">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-381">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-381">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-382">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-382">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="91e24-383">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-383">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="91e24-384">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-384">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="91e24-385">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="91e24-385">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="91e24-386">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-386">Build the project.</span></span>
4. <span data-ttu-id="91e24-387">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-387">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="91e24-388">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-388">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="91e24-389">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-389">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="91e24-390">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-390">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-391">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-391">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-392">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-392">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="91e24-393">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-393">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-394">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-394">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-395">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-395">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="91e24-396">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-396">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-397">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-397">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-398">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-398">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="91e24-399">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-399">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="91e24-400">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-400">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="91e24-401">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-401">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-402">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-402">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-403">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-403">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-404">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-404">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-405">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-405">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-406">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-406">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-407">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-407">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-408">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-408">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-409">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-409">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-410">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-410">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="91e24-411">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-411">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="91e24-412">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-412">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="91e24-413">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-413">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-414">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-414">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-415">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-415">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-416">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-416">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="91e24-417">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-417">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="91e24-418">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-418">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="91e24-419">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-419">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-420">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-420">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="91e24-421">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-421">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-422">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-422">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="91e24-423">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-423">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="91e24-424">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-424">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="91e24-425">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-425">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="91e24-426">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-426">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="91e24-427">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="91e24-427">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="91e24-428">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="91e24-428">These files aren't intended for any customizations.</span></span>

---

### <a name="the-retail-server-extension-components"></a><span data-ttu-id="91e24-429">Retail Server 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-429">The Retail Server extension components</span></span>

#### <a name="salestransactionsignature-retail-server-sample-component"></a><span data-ttu-id="91e24-430">SalesTransactionSignature Retail Server サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-430">SalesTransactionSignature Retail Server sample component</span></span>

1. <span data-ttu-id="91e24-431">**RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-431">In the **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="91e24-432">**RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.RetailServer.SalesTransactionSignatureSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-432">In the **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.RetailServer.SalesTransactionSignatureSample.dll** assembly file.</span></span>
3. <span data-ttu-id="91e24-433">アセンブリ ファイルを Retail Server 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-433">Copy the assembly file to the Retail Server extensions folder.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-434">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-434">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="91e24-435">フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="91e24-435">The folder is the **\\bin** folder under the IIS Retail Server site location.</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-436">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-436">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="91e24-437">フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="91e24-437">The folder is the **\\bin** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-438">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-438">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    <span data-ttu-id="91e24-439">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="91e24-439">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-440">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-440">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    <span data-ttu-id="91e24-441">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="91e24-441">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-442">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-442">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    <span data-ttu-id="91e24-443">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="91e24-443">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-444">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-444">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    <span data-ttu-id="91e24-445">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="91e24-445">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    ---

4. <span data-ttu-id="91e24-446">Retail Server のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-446">Find the configuration file for Retail Server.</span></span> <span data-ttu-id="91e24-447">ファイル名は **web.config** で、IIS Retail Server サイトがある場所の下のルート フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-447">The file is named **web.config**, and it's in the root folder under the IIS Retail Server site location.</span></span>
5. <span data-ttu-id="91e24-448">コンフィギュレーションの **extensionComposition** セクションで Retail Server 拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-448">Register the Retail Server extensions in the **extensionComposition** section of the configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. <span data-ttu-id="91e24-449">Retail Server 拡張機能の依存関係を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-449">Register the dependencies of the Retail Server extensions.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-450">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-450">Application update 4</span></span>](#tab/app-update-4/)

    1. <span data-ttu-id="91e24-451">**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-451">In the **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

        - <span data-ttu-id="91e24-452">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-452">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
        - <span data-ttu-id="91e24-453">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="91e24-453">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

    2. <span data-ttu-id="91e24-454">ファイルを、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-454">Copy the files to the **\\bin** folder under the IIS Retail Server site location.</span></span>
    3. <span data-ttu-id="91e24-455">CRT用拡張機能コンフィギュレーションファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-455">Register the CRT change in the extension configuration file for CRT.</span></span> <span data-ttu-id="91e24-456">ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-456">This file is named **commerceruntime.ext.config**, and it's in the **bin** folder under the IIS Retail Server site location.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-457">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-457">Application update 5 and later</span></span>](#tab/app-update-5-and-later/)

    1. <span data-ttu-id="91e24-458">**CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-458">In the **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** assembly file.</span></span>
    2. <span data-ttu-id="91e24-459">ファイルをIIS Retail Server サイトがある場所の **\\bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-459">Copy the file to the **\\bin** folder under the IIS Retail Server site location.</span></span>
    3. <span data-ttu-id="91e24-460">CRT用拡張機能コンフィギュレーションファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-460">Register the CRT change in the extension configuration file for CRT.</span></span> <span data-ttu-id="91e24-461">ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-461">This file is named **commerceruntime.ext.config**, and it's in the **bin** folder under the IIS Retail Server site location.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-462">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-462">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="91e24-463">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="91e24-463">No actions are required.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-464">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-464">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="91e24-465">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="91e24-465">No actions are required.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-466">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-466">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="91e24-467">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="91e24-467">No actions are required.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-468">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-468">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="91e24-469">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="91e24-469">No actions are required.</span></span>

    ---

### <a name="the-modern-pos-extension-components"></a><span data-ttu-id="91e24-470">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-470">The Modern POS extension components</span></span>

#### <a name="implement-the-proxy-code-for-offline-mode"></a><span data-ttu-id="91e24-471">オフライン モード用プロキシ コードを実装します。</span><span class="sxs-lookup"><span data-stu-id="91e24-471">Implement the proxy code for offline mode</span></span>

<span data-ttu-id="91e24-472">この箇所は Retail Server コントローラーと同じですが、クライアントが接続されていない場合に使用されるローカル CRT を拡張します。</span><span class="sxs-lookup"><span data-stu-id="91e24-472">This part is equivalent to the Retail Server controller, but it extends the local CRT that is used when the client isn't connected.</span></span>

1. <span data-ttu-id="91e24-473">**Customization.settings** ファイルで、**@(RetailServerLibraryPathForProxyGeneration)** セクションを変更し、プロキシ生成で新しい Retail Server アセンブリを使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="91e24-473">In the **customization.settings** file, change the **@(RetailServerLibraryPathForProxyGeneration)** section so that it uses the new Retail Server assembly for proxy generation.</span></span>
2. <span data-ttu-id="91e24-474">**StoreOperationsManager** クラスで次のインターフェイス メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="91e24-474">Implement the following interface methods in the **StoreOperationsManager** class.</span></span> <span data-ttu-id="91e24-475">最初の繰り返しには、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-475">For the first iteration, add the following code:</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-476">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-476">Application update 4</span></span>](#tab/app-update-4)

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

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-477">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-477">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

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

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-478">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-478">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="91e24-479">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-479">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-480">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-480">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="91e24-481">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-481">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-482">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-482">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="91e24-483">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-483">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-484">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-484">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="91e24-485">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-485">This step doesn't apply to this version.</span></span>

    ---

3. <span data-ttu-id="91e24-486">プロキシ コードを再生成するには、コマンドラインから **msbuild/t:Rebuild** コマンドを使用して**プロキシ**フォルダーを構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-486">To regenerate the proxy code, build the **Proxies** folder from the command line by using the **msbuild /t:Rebuild** command.</span></span>
4. <span data-ttu-id="91e24-487">**Proxies.RetailProxy** プロジェクトの依存関係を解決します。</span><span class="sxs-lookup"><span data-stu-id="91e24-487">Resolve the **Proxies.RetailProxy** project dependencies:</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-488">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-488">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="91e24-489">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** project to reference **SalesTransactionSignatureSample** に追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-489">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, add the **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** project to the solution, and add a project reference to the **RetailProxy** project to reference **SalesTransactionSignatureSample**.</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-490">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-490">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="91e24-491">**RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** プロジェクトと、**SalesTransactionSignatureSample.Messages**参照に追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-491">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, add the **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** project to the solution, and add a project reference to the **RetailProxy** project to reference **SalesTransactionSignatureSample.Messages**.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-492">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-492">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="91e24-493">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-493">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-494">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-494">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="91e24-495">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-495">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-496">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-496">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="91e24-497">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-497">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-498">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-498">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="91e24-499">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-499">This step doesn't apply to this version.</span></span>

    ---

5. <span data-ttu-id="91e24-500">**StoreOperationsManager** クラスでインターフェイス メソッドを調節します。</span><span class="sxs-lookup"><span data-stu-id="91e24-500">Adjust the interface methods in the **StoreOperationsManager** class:</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-501">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-501">Application update 4</span></span>](#tab/app-update-4)

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

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-502">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-502">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

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

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-503">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-503">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="91e24-504">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-504">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-505">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-505">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="91e24-506">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-506">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-507">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-507">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="91e24-508">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-508">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-509">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-509">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="91e24-510">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="91e24-510">This step doesn't apply to this version.</span></span>

    ---

6. <span data-ttu-id="91e24-511">**dllhost.exe.config** ファイルを更新し、クライアント ブローカーが新しい RetailProxy アセンブリを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="91e24-511">Update the **dllhost.exe.config** file so that the client broker loads the new RetailProxy assembly.</span></span>

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a><span data-ttu-id="91e24-512">小売プロキシ拡張コンポーネント (Retail 7.3.1 およびそれ以降)</span><span class="sxs-lookup"><span data-stu-id="91e24-512">Retail proxy extension component (Retail 7.3.1 and later)</span></span>

<span data-ttu-id="91e24-513">Retail 7.3.1 もしくはそれ以降を使用しているときに限り、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="91e24-513">Complete the following procedure only if you're using Retail 7.3.1 and later.</span></span>

1. <span data-ttu-id="91e24-514">**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample**  フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="91e24-514">In the **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="91e24-515">**RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="91e24-515">In the **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** assembly file.</span></span>
3. <span data-ttu-id="91e24-516">アセンブリ ファイルをローカル CRT クライアント ブローカーの下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-516">Copy the assembly files to the **\\ext** folder under the local CRT client broker location.</span></span>
4. <span data-ttu-id="91e24-517">拡張機能コンフィギュレーション ファイルで Retail プロキシの変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="91e24-517">Register the Retail proxy change in the extension configuration file.</span></span> <span data-ttu-id="91e24-518">ファイル名は **RetailProxy.MPOSOffline.ext.config** で、ローカル CRT クライアント ブローカーの場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-518">The file is named **RetailProxy.MPOSOffline.ext.config**, and it's under the local CRT client broker location.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a><span data-ttu-id="91e24-519">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-519">Modern POS extension components</span></span>

1. <span data-ttu-id="91e24-520">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="91e24-520">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="91e24-521">また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="91e24-521">Additionally, make sure that you can run Modern POS from Microsoft Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="91e24-522">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="91e24-522">Modern POS must not be customized.</span></span> <span data-ttu-id="91e24-523">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e24-523">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

2. <span data-ttu-id="91e24-524">**Pos.Extensions** プロジェクトが、次の既存のソース コード フォルダーを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="91e24-524">Include the following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-525">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-525">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="91e24-526">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-526">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-527">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-527">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-528">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-528">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="91e24-529">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-529">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-530">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-530">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-531">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-531">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="91e24-532">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-532">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-533">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-533">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-534">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-534">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="91e24-535">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-535">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-536">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-536">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-537">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-537">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-538">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-538">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-539">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-539">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="91e24-540">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-540">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-541">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-541">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-542">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-542">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-543">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-543">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="91e24-544">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-544">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-545">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-545">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-546">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-546">SequentialSignature</span></span>

    ---

3. <span data-ttu-id="91e24-547">除外リストから次のフォルダーを削除して、**tsconfig.json** で拡張機能がコンパイルされるようにします。</span><span class="sxs-lookup"><span data-stu-id="91e24-547">Enable the extensions to be compiled in **tsconfig.json** by removing the following folders from the exclude list.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-548">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-548">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="91e24-549">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-549">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-550">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-550">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-551">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-551">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="91e24-552">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-552">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-553">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-553">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-554">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-554">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="91e24-555">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-555">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-556">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-556">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-557">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-557">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="91e24-558">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-558">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-559">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-559">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-560">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-560">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-561">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-561">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-562">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-562">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="91e24-563">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-563">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-564">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-564">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-565">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-565">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-566">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-566">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="91e24-567">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-567">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-568">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-568">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-569">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-569">SequentialSignature</span></span>

    ---

4. <span data-ttu-id="91e24-570">適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="91e24-570">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate place.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-571">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-571">Application update 4</span></span>](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-572">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-572">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-573">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-573">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-574">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-574">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-575">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-575">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-576">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-576">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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
    > <span data-ttu-id="91e24-577">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="91e24-577">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="91e24-578">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="91e24-578">Rebuild the solution.</span></span>
6. <span data-ttu-id="91e24-579">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="91e24-579">Run Modern POS in the debugger, and test the functionality.</span></span>

### <a name="cloud-pos-extension-components"></a><span data-ttu-id="91e24-580">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91e24-580">Cloud POS extension components</span></span>

1. <span data-ttu-id="91e24-581">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="91e24-581">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="91e24-582">**Pos.Extensions** プロジェクトの、既存ソース コード フォルダーを含めます。</span><span class="sxs-lookup"><span data-stu-id="91e24-582">Include following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-583">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-583">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="91e24-584">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-584">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-585">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-585">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-586">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-586">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="91e24-587">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-587">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-588">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-588">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-589">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-589">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="91e24-590">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-590">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-591">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-591">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-592">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-592">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="91e24-593">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-593">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-594">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-594">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-595">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-595">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-596">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-596">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-597">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-597">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="91e24-598">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-598">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-599">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-599">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-600">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-600">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-601">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-601">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="91e24-602">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-602">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-603">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-603">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-604">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-604">SequentialSignature</span></span>

    ---

3. <span data-ttu-id="91e24-605">除外リストから次のフォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="91e24-605">Enable the extensions to be compiled in **tsconfig.json** by removing following folders from the exclude list.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-606">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-606">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="91e24-607">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-607">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-608">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-608">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-609">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-609">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="91e24-610">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-610">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-611">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-611">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-612">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-612">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="91e24-613">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-613">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-614">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-614">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-615">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-615">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="91e24-616">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="91e24-616">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="91e24-617">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-617">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-618">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-618">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-619">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-619">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-620">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-620">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="91e24-621">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-621">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-622">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-622">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-623">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-623">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-624">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-624">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="91e24-625">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="91e24-625">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="91e24-626">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="91e24-626">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="91e24-627">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="91e24-627">SequentialSignature</span></span>

    ---

4. <span data-ttu-id="91e24-628">適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="91e24-628">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate place.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-629">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-629">Application update 4</span></span>](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-630">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-630">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-631">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-631">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-632">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-632">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-633">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-633">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-634">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-634">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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
    > <span data-ttu-id="91e24-635">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="91e24-635">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="91e24-636">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="91e24-636">Rebuild the solution.</span></span>
6. <span data-ttu-id="91e24-637">**実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="91e24-637">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>
7. <span data-ttu-id="91e24-638">機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="91e24-638">Test the functionality.</span></span>

### <a name="set-up-required-parameters-in-retail-headquarters"></a><span data-ttu-id="91e24-639">小売用バックオフィスで要求されるパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="91e24-639">Set up required parameters in Retail headquarters</span></span>

<span data-ttu-id="91e24-640">詳細については、[ノルウェーのキャッシュ レジスター](./emea-nor-cash-registers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="91e24-640">For more information, see [Cash registers for Norway](./emea-nor-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="91e24-641">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="91e24-641">Production environment</span></span>

<span data-ttu-id="91e24-642">以下の手順に従い、小売コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="91e24-642">Follow these steps to create deployable packages that contain Retail components, and to apply those packages in a production environment.</span></span>

1. <span data-ttu-id="91e24-643">[クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="91e24-643">Complete the steps in the [Cloud POS extension components](#cloud-pos-extension-components) or [Modern POS extension components](#modern-pos-extension-components) section earlier in this topic.</span></span>
2. <span data-ttu-id="91e24-644">**RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="91e24-644">Make the following changes in the package configuration files under the **RetailSdk\\Assets** folder:</span></span>

    1. <span data-ttu-id="91e24-645">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの**構成**セクションに、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-645">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files, add the following lines to the **composition** section:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-646">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-646">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-647">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-647">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-648">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-648">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-649">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-649">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-650">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-650">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-651">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-651">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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

    2. <span data-ttu-id="91e24-652">小売プロキシ カスタマイズを有効にします。</span><span class="sxs-lookup"><span data-stu-id="91e24-652">Enable Retail Proxy customization:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-653">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-653">Application update 4</span></span>](#tab/app-update-4)

        <span data-ttu-id="91e24-654">**dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-654">In the **dllhost.exe.config** configuration file, add the following lines to the **appSettings** subsection of the **configuration** section.</span></span>

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-655">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-655">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        <span data-ttu-id="91e24-656">**dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-656">In the **dllhost.exe.config** configuration file, add the following lines to the **appSettings** subsection of the **configuration** section.</span></span>

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-657">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-657">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="91e24-658">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-658">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-659">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-659">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        <span data-ttu-id="91e24-660">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-660">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-661">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-661">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        <span data-ttu-id="91e24-662">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-662">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-663">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-663">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        <span data-ttu-id="91e24-664">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-664">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. <span data-ttu-id="91e24-665">**Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="91e24-665">Make the following changes in the **Customization.settings** package customization configuration file:</span></span>

    1. <span data-ttu-id="91e24-666">小売プロキシ カスタマイズを有効にします。</span><span class="sxs-lookup"><span data-stu-id="91e24-666">Enable Retail Proxy customization.</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-667">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-667">Application update 4</span></span>](#tab/app-update-4)

        <span data-ttu-id="91e24-668">**&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-668">Add the following lines to the **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** section.</span></span>

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-669">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-669">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        <span data-ttu-id="91e24-670">**&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-670">Add the following lines to the **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** section.</span></span>

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-671">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-671">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="91e24-672">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="91e24-672">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-673">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-673">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        <span data-ttu-id="91e24-674">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="91e24-674">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-675">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-675">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        <span data-ttu-id="91e24-676">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="91e24-676">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-677">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-677">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        <span data-ttu-id="91e24-678">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="91e24-678">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. <span data-ttu-id="91e24-679">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="91e24-679">Add the following lines to the **ItemGroup** section to include the CRT extensions in the deployable packages:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-680">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-680">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-681">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-681">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-682">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-682">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-683">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-683">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-684">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-684">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-685">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-685">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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

    3. <span data-ttu-id="91e24-686">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに Retail Server 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="91e24-686">Add following lines to the **ItemGroup** section to include the Retail Server extension in the deployable packages:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-687">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-687">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-688">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-688">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-689">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-689">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-690">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-690">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-691">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-691">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-692">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-692">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. <span data-ttu-id="91e24-693">以下のファイルを修正して、配置可能なパッケージ内に ノルウェーのリソース ファイルを含めます。</span><span class="sxs-lookup"><span data-stu-id="91e24-693">Modify the following files to include the resource files for Norway in deployable packages:</span></span>
    - <span data-ttu-id="91e24-694">Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj</span><span class="sxs-lookup"><span data-stu-id="91e24-694">Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj</span></span>
    - <span data-ttu-id="91e24-695">Packages\RetailServer\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="91e24-695">Packages\RetailServer\Sdk.RetailServerSetup.proj</span></span>
  
  - <span data-ttu-id="91e24-696">**Sdk.ModernPos.Shared.csproj** ファイルの場合</span><span class="sxs-lookup"><span data-stu-id="91e24-696">For the **Sdk.ModernPos.Shared.csproj** file</span></span> 
    - <span data-ttu-id="91e24-697">**ItemGroup** セクションに新しい行を追加</span><span class="sxs-lookup"><span data-stu-id="91e24-697">Add line to the **ItemGroup** section</span></span>
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > <span data-ttu-id="91e24-698">[注意] < ファイル名> ではなく、リソースファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="91e24-698">[Note] Instead of the <File_name> specify a name of the resource file.</span></span> <span data-ttu-id="91e24-699">次に示す例にも同じことが当てはまります。</span><span class="sxs-lookup"><span data-stu-id="91e24-699">The same is relevant for the other examples given below.</span></span>
 
    - <span data-ttu-id="91e24-700">**Target Name="CopyPackageFiles"** セクションに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-700">Add line to the **Target Name="CopyPackageFiles"** section</span></span>
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - <span data-ttu-id="91e24-701">**Sdk.RetailServerSetup.proj** ファイルの場合</span><span class="sxs-lookup"><span data-stu-id="91e24-701">For the **Sdk.RetailServerSetup.proj** file</span></span> 
    - <span data-ttu-id="91e24-702">**ItemGroup** セクションに新しい行を追加</span><span class="sxs-lookup"><span data-stu-id="91e24-702">Add line to the **ItemGroup** section</span></span>
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - <span data-ttu-id="91e24-703">**Target Name="CopyPackageFiles"** セクションに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-703">Add line to the **Target Name="CopyPackageFiles"** section</span></span>
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. <span data-ttu-id="91e24-704">拇印、保管場所、署名販売取引に使用されるべき証明書の保存名を指定して、証明書のコンフィギュレーションを変更します。</span><span class="sxs-lookup"><span data-stu-id="91e24-704">Modify the certificate's configuration file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span> <span data-ttu-id="91e24-705">その後 **References** フォルダーにコンフィギュレーション ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="91e24-705">Then copy the configuration file to the **References** folder.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="91e24-706">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="91e24-706">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="91e24-707">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-707">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="91e24-708">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="91e24-708">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="91e24-709">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-709">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="91e24-710">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="91e24-710">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    <span data-ttu-id="91e24-711">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-711">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="91e24-712">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-712">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    <span data-ttu-id="91e24-713">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-713">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="91e24-714">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-714">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    <span data-ttu-id="91e24-715">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-715">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="91e24-716">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="91e24-716">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    <span data-ttu-id="91e24-717">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="91e24-717">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    ---

6. <span data-ttu-id="91e24-718">Retail Server コンフィギュレーション ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="91e24-718">Update Retail Server configuration file.</span></span> <span data-ttu-id="91e24-719">**RetailSDK\\Packages\\RetailServer\\Code\\web.config** ファイルの **extensionComposition** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e24-719">In the **RetailSDK\\Packages\\RetailServer\\Code\\web.config** file, add the following lines to the **extensionComposition** section.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. <span data-ttu-id="91e24-720">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="91e24-720">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
8. <span data-ttu-id="91e24-721">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="91e24-721">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="91e24-722">詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="91e24-722">For more information, see [Retail SDK packaging](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a><span data-ttu-id="91e24-723">Modern POS のオフライン モードでのデジタル署名を有効にします。</span><span class="sxs-lookup"><span data-stu-id="91e24-723">Enable the digital signature in offline mode for Modern POS</span></span>

<span data-ttu-id="91e24-724">Modern POSでオフライン モードでのデジタル署名を有効にするには、新しい端末で Modern POS を有効化した後、これらの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e24-724">To enable the digital signature in offline mode for Modern POS, you must follow these steps after you activate Modern POS on a new device.</span></span>

1. <span data-ttu-id="91e24-725">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="91e24-725">Sign in to POS.</span></span>
2. <span data-ttu-id="91e24-726">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="91e24-726">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="91e24-727">**ダウンロードの保留中**フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="91e24-727">When the value of the **Pending downloads** field is **0** (zero), the database is fully synchronized.</span></span>
3. <span data-ttu-id="91e24-728">POS からのサインアウト</span><span class="sxs-lookup"><span data-stu-id="91e24-728">Sign out of POS.</span></span>
4. <span data-ttu-id="91e24-729">オフライン データベースが完全に同期するため少しの間待ちます。</span><span class="sxs-lookup"><span data-stu-id="91e24-729">Wait a while for the offline database to be fully synchronized.</span></span>
5. <span data-ttu-id="91e24-730">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="91e24-730">Sign in to POS.</span></span>
6. <span data-ttu-id="91e24-731">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="91e24-731">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="91e24-732">**オフライン データベースで取引を保留中** フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="91e24-732">When the value of the **Pending transactions in offline database** field is **0** (zero), the database is fully synchronized.</span></span>
7. <span data-ttu-id="91e24-733">Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="91e24-733">Restart Modern POS.</span></span>

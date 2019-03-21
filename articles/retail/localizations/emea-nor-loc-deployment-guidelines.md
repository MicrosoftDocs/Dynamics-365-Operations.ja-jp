---
title: ノルウェーのキャッシュ レジスタの配置ガイドライン
description: このトピックは、ノルウェー向け小売ローカライズ用配置ガイドです。
author: AlexChern0v
manager: olegkl
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: shylaw
ms.search.scope: Retail
ms.search.region: Norway
ms.search.industry: Retail
ms.author: v-alexec
ms.search.validFrom: 2018-2-28
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: 0965df99c4b58bbb5ec8dd0fceb3207e8a3eb644
ms.sourcegitcommit: 2cf5498098e7a5ade1c16eac6df26bc98e4565cd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/26/2019
ms.locfileid: "760769"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a><span data-ttu-id="1cc13-103">ノルウェーのキャッシュ レジスタの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="1cc13-103">Deployment guidelines for cash registers for Norway</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cc13-104">このトピックは、Microsoft Dynamics 365 for Retail のノルウェーでのローカライズを有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="1cc13-104">This topic is a deployment guide that shows how to enable the Microsoft Dynamics 365 for Retail localization for Norway.</span></span> <span data-ttu-id="1cc13-105">ローカライズは、小売コンポーネントのいくつかの拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-105">The localization consists of several extensions of Retail components.</span></span> <span data-ttu-id="1cc13-106">たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、および販売時点管理 (POS) での支払取引を登録、デジタル署名販売取引、およびローカルの形式で X および Z レポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-106">For example, the extensions let you print custom fields on receipts, register additional audit events, sales transactions, and payment transactions in Point of Sale (POS), digitally sign sales transactions, and print X and Z reports in local formats.</span></span> <span data-ttu-id="1cc13-107">ノルウェーの小売ローカライズの詳細については、[ノルウェーのキャッシュ レジスター](./emea-nor-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1cc13-107">For more information about the Retail localization for Norway, see [Cash registers for Norway](./emea-nor-cash-registers.md).</span></span>

<span data-ttu-id="1cc13-108">このサンプルは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="1cc13-108">This sample is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="1cc13-109">リテール SDK をダウンロードして使用する方法については、[リテール SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1cc13-109">For information about how to install and use the Retail SDK, see the [Retail SDK documentation](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="1cc13-110">このサンプルは Commerce runtime (CRT)、Retail Server、そして POS の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-110">This sample consists of extensions for the Commerce runtime (CRT), Retail Server, and POS.</span></span> <span data-ttu-id="1cc13-111">このサンプルを実行するには、CRT、Retail Servers および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-111">To run this sample, you must modify and build the CRT, Retail Server, and POS projects.</span></span> <span data-ttu-id="1cc13-112">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-112">We recommend that you use an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="1cc13-113">また Microsoft Visual Studio オンライン (VSO) のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-113">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE]
> <span data-ttu-id="1cc13-114">使用しているバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-114">Some steps in the procedures in this topic differ, depending on the version of Retail that you're using.</span></span> <span data-ttu-id="1cc13-115">詳細については、[Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1cc13-115">For more information, see [What's new or changed in Dynamics 365 for Retail](../get-started/whats-new.md).</span></span>

## <a name="development-environment"></a><span data-ttu-id="1cc13-116">開発環境</span><span class="sxs-lookup"><span data-stu-id="1cc13-116">Development environment</span></span>

<span data-ttu-id="1cc13-117">サンプルをテストして拡張できるように開発環境を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-117">Complete these procedures to set up a development environment so that you can test and extend the sample.</span></span>

### <a name="the-crt-extension-components"></a><span data-ttu-id="1cc13-118">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-118">The CRT extension components</span></span>

<span data-ttu-id="1cc13-119">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-119">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="1cc13-120">次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-120">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

#### <a name="receiptsnorway-component"></a><span data-ttu-id="1cc13-121">ReceiptsNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-121">ReceiptsNorway component</span></span>

1. <span data-ttu-id="1cc13-122">**Runtime.Extensions.ReceiptsNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-122">Find the **Runtime.Extensions.ReceiptsNorway** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-123">**Extensions.ReceiptsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.ReceiptsNorway.dll** アセンブリファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-123">In the **Extensions.ReceiptsNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.ReceiptsNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-124">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-124">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-125">**Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-125">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-126">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-126">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-127">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-127">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-128">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-128">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-129">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-129">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-130">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-130">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-131">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-131">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-132">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-132">These files aren't intended for any customizations.</span></span>

#### <a name="salespaymenttransext-component"></a><span data-ttu-id="1cc13-133">SalesPaymentTransExt コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-133">SalesPaymentTransExt component</span></span>

1. <span data-ttu-id="1cc13-134">**Runtime.Extensions.SalesPaymentTransExt** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-134">Find the **Runtime.Extensions.SalesPaymentTransExt** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-135">**Extensions.SalesPaymentTransExt\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-135">In the **Extensions.SalesPaymentTransExt\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-136">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-136">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-137">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-137">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-138">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-138">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-139">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-139">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-140">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-140">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-141">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-141">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-142">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-142">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-143">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-143">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-144">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-144">These files aren't intended for any customizations.</span></span>

#### <a name="xzreportsnorway-component"></a><span data-ttu-id="1cc13-145">XZReportsNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-145">XZReportsNorway component</span></span>

1. <span data-ttu-id="1cc13-146">**Runtime.Extensions.XZReportsNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-146">Find the **Runtime.Extensions.XZReportsNorway** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-147">**Extensions.XZReportsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.XZReportsNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-147">In the **Extensions.XZReportsNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.XZReportsNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-148">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-148">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-149">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-149">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-150">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-150">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-151">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-151">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-152">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-152">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-153">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-153">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-154">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-154">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-155">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-155">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-156">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-156">These files aren't intended for any customizations.</span></span>

# <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-157">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-157">Application update 4</span></span>](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="1cc13-158">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-158">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="1cc13-159">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-159">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-160">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-160">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-161">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-161">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-162">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-162">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-163">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-163">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-164">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-164">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-165">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-165">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-166">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-166">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-167">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-167">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-168">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-168">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-169">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-169">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="1cc13-170">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-170">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="1cc13-171">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-171">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="1cc13-172">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-172">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="1cc13-173">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-173">Build the project.</span></span>
4. <span data-ttu-id="1cc13-174">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-174">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="1cc13-175">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-175">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="1cc13-176">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-176">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="1cc13-177">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-177">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-178">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-178">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-179">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-179">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="1cc13-180">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-180">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-181">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-181">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-182">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-182">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="1cc13-183">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-183">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-184">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-184">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-185">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-185">These files aren't intended for any customizations.</span></span>

# <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-186">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-186">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="1cc13-187">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-187">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="1cc13-188">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-188">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-189">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-189">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-190">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-190">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-191">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-191">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-192">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-192">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-193">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-193">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-194">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-194">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-195">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-195">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-196">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-196">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-197">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-197">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-198">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-198">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="1cc13-199">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-199">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="1cc13-200">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-200">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="1cc13-201">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-201">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="1cc13-202">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-202">Build the project.</span></span>
4. <span data-ttu-id="1cc13-203">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-203">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="1cc13-204">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-204">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="1cc13-205">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-205">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="1cc13-206">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-206">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-207">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-207">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-208">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-208">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="1cc13-209">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-209">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-210">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-210">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-211">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-211">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="1cc13-212">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-212">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-213">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-213">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-214">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-214">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturesamplemessages-component"></a><span data-ttu-id="1cc13-215">SalesTransactionSignatureSample.Messages コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-215">SalesTransactionSignatureSample.Messages component</span></span>

1. <span data-ttu-id="1cc13-216">**Runtime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-216">Find the **Runtime.Extensions.SalesTransactionSignatureSample.Messages** project.</span></span>
2. <span data-ttu-id="1cc13-217">**Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-217">In the **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-218">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-218">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-219">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-219">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-220">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-220">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-221">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-221">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-222">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-222">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-223">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-223">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-224">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-224">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-225">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-225">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-226">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-226">These files aren't intended for any customizations.</span></span>

# <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-227">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-227">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="1cc13-228">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-228">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="1cc13-229">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-229">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-230">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-230">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-231">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-231">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-232">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-232">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-233">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-233">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-234">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-234">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-235">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-235">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-236">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-236">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-237">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-237">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-238">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-238">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-239">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-239">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="1cc13-240">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-240">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="1cc13-241">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-241">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="1cc13-242">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-242">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="1cc13-243">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-243">Build the project.</span></span>
4. <span data-ttu-id="1cc13-244">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-244">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="1cc13-245">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-245">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="1cc13-246">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-246">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="1cc13-247">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-247">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-248">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-248">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-249">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-249">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="1cc13-250">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-250">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-251">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-251">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-252">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-252">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="1cc13-253">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-253">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-254">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-254">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-255">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-255">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="1cc13-256">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-256">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="1cc13-257">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-257">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="1cc13-258">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-258">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-259">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-259">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-260">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-260">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-261">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-261">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

# <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-262">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-262">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="1cc13-263">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-263">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="1cc13-264">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-264">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-265">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-265">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-266">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-266">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-267">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-267">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-268">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-268">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-269">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-269">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-270">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-270">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-271">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-271">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-272">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-272">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-273">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-273">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-274">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-274">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="1cc13-275">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-275">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="1cc13-276">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-276">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="1cc13-277">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-277">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="1cc13-278">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-278">Build the project.</span></span>
4. <span data-ttu-id="1cc13-279">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-279">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="1cc13-280">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-280">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="1cc13-281">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-281">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="1cc13-282">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-282">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-283">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-283">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-284">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-284">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="1cc13-285">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-285">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-286">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-286">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-287">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-287">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="1cc13-288">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-288">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="1cc13-289">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-289">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="1cc13-290">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-290">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-291">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-291">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-292">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-292">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-293">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-293">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-294">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-294">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-295">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-295">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-296">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-296">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-297">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-297">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-298">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-298">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-299">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-299">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="1cc13-300">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-300">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="1cc13-301">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-301">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="1cc13-302">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-302">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-303">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-303">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-304">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-304">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-305">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-305">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="1cc13-306">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-306">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="1cc13-307">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-307">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-308">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-308">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-309">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-309">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-310">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-310">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-311">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-311">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-312">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-312">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-313">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-313">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-314">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-314">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-315">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-315">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-316">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-316">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-317">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-317">These files aren't intended for any customizations.</span></span>

# <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-318">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-318">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="1cc13-319">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-319">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="1cc13-320">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-320">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="1cc13-321">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-321">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="1cc13-322">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-322">Build the project.</span></span>
4. <span data-ttu-id="1cc13-323">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-323">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="1cc13-324">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-324">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="1cc13-325">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-325">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="1cc13-326">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-326">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-327">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-327">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-328">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-328">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="1cc13-329">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-329">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-330">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-330">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-331">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-331">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="1cc13-332">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-332">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="1cc13-333">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-333">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="1cc13-334">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-334">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-335">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-335">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-336">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-336">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-337">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-337">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-338">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-338">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-339">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-339">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-340">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-340">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-341">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-341">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-342">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-342">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-343">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-343">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="1cc13-344">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-344">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="1cc13-345">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-345">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="1cc13-346">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-346">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-347">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-347">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-348">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-348">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-349">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-349">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="1cc13-350">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-350">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="1cc13-351">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-351">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-352">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-352">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-353">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-353">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-354">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-354">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-355">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-355">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-356">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-356">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-357">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-357">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-358">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-358">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-359">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-359">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-360">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-360">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-361">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-361">These files aren't intended for any customizations.</span></span>

# <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-362">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-362">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="1cc13-363">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-363">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="1cc13-364">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-364">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="1cc13-365">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-365">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="1cc13-366">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-366">Build the project.</span></span>
4. <span data-ttu-id="1cc13-367">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-367">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="1cc13-368">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-368">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="1cc13-369">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-369">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="1cc13-370">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-370">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-371">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-371">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-372">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-372">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="1cc13-373">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-373">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-374">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-374">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-375">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-375">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="1cc13-376">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-376">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="1cc13-377">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-377">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="1cc13-378">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-378">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-379">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-379">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-380">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-380">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-381">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-381">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-382">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-382">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-383">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-383">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-384">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-384">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-385">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-385">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-386">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-386">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-387">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-387">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="1cc13-388">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-388">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="1cc13-389">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-389">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="1cc13-390">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-390">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-391">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-391">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-392">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-392">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-393">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-393">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="1cc13-394">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-394">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="1cc13-395">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-395">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-396">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-396">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-397">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-397">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="1cc13-398">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-398">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-399">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-399">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="1cc13-400">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-400">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="1cc13-401">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-401">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="1cc13-402">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-402">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="1cc13-403">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-403">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="1cc13-404">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="1cc13-404">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="1cc13-405">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-405">These files aren't intended for any customizations.</span></span>

---

### <a name="the-retail-server-extension-components"></a><span data-ttu-id="1cc13-406">Retail Server 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-406">The Retail Server extension components</span></span>

#### <a name="salestransactionsignature-retail-server-sample-component"></a><span data-ttu-id="1cc13-407">SalesTransactionSignature Retail Server サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-407">SalesTransactionSignature Retail Server sample component</span></span>

1. <span data-ttu-id="1cc13-408">**RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-408">In the **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-409">**RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.RetailServer.SalesTransactionSignatureSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-409">In the **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.RetailServer.SalesTransactionSignatureSample.dll** assembly file.</span></span>
3. <span data-ttu-id="1cc13-410">アセンブリ ファイルを Retail Server 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-410">Copy the assembly file to the Retail Server extensions folder.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-411">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-411">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="1cc13-412">フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="1cc13-412">The folder is the **\\bin** folder under the IIS Retail Server site location.</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-413">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-413">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="1cc13-414">フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="1cc13-414">The folder is the **\\bin** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-415">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-415">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    <span data-ttu-id="1cc13-416">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="1cc13-416">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-417">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-417">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    <span data-ttu-id="1cc13-418">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="1cc13-418">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-419">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-419">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    <span data-ttu-id="1cc13-420">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="1cc13-420">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-421">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-421">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    <span data-ttu-id="1cc13-422">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="1cc13-422">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    ---

4. <span data-ttu-id="1cc13-423">Retail Server のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-423">Find the configuration file for Retail Server.</span></span> <span data-ttu-id="1cc13-424">ファイル名は **web.config** で、IIS Retail Server サイトがある場所の下のルート フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-424">The file is named **web.config**, and it's in the root folder under the IIS Retail Server site location.</span></span>
5. <span data-ttu-id="1cc13-425">コンフィギュレーションの **extensionComposition** セクションで Retail Server 拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-425">Register the Retail Server extensions in the **extensionComposition** section of the configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. <span data-ttu-id="1cc13-426">Retail Server 拡張機能の依存関係を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-426">Register the dependencies of the Retail Server extensions.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-427">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-427">Application update 4</span></span>](#tab/app-update-4/)

    1. <span data-ttu-id="1cc13-428">**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-428">In the **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

        - <span data-ttu-id="1cc13-429">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-429">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
        - <span data-ttu-id="1cc13-430">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc13-430">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

    2. <span data-ttu-id="1cc13-431">ファイルを、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-431">Copy the files to the **\\bin** folder under the IIS Retail Server site location.</span></span>
    3. <span data-ttu-id="1cc13-432">CRT 用コンフィギュレーション ファイルで CTR の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-432">Register the CRT change in the extensions configuration file for CRT.</span></span> <span data-ttu-id="1cc13-433">ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-433">This file is named **commerceruntime.ext.config**, and it's in the **bin** folder under the IIS Retail Server site location.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-434">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-434">Application update 5 and later</span></span>](#tab/app-update-5-and-later/)

    1. <span data-ttu-id="1cc13-435">**CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-435">In the **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** assembly file.</span></span>
    2. <span data-ttu-id="1cc13-436">ファイルをIIS Retail Server サイトがある場所の **\\bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-436">Copy the file to the **\\bin** folder under the IIS Retail Server site location.</span></span>
    3. <span data-ttu-id="1cc13-437">CRT 用コンフィギュレーション ファイルで CTR の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-437">Register the CRT change in the extensions configuration file for CRT.</span></span> <span data-ttu-id="1cc13-438">ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-438">This file is named **commerceruntime.ext.config**, and it's in the **bin** folder under the IIS Retail Server site location.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-439">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-439">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="1cc13-440">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="1cc13-440">No actions are required.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-441">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-441">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="1cc13-442">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="1cc13-442">No actions are required.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-443">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-443">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="1cc13-444">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="1cc13-444">No actions are required.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-445">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-445">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="1cc13-446">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="1cc13-446">No actions are required.</span></span>

    ---

### <a name="the-modern-pos-extension-components"></a><span data-ttu-id="1cc13-447">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-447">The Modern POS extension components</span></span>

#### <a name="implement-the-proxy-code-for-offline-mode"></a><span data-ttu-id="1cc13-448">オフライン モード用プロキシ コードを実装します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-448">Implement the proxy code for offline mode</span></span>

<span data-ttu-id="1cc13-449">この箇所は Retail Server コントローラーと同じですが、クライアントが接続されていない場合に使用されるローカル CRT を拡張します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-449">This part is equivalent to the Retail Server controller, but it extends the local CRT that is used when the client isn't connected.</span></span>

1. <span data-ttu-id="1cc13-450">**Customization.settings** ファイルで、**@(RetailServerLibraryPathForProxyGeneration)** セクションを変更し、プロキシ生成で新しい Retail Server アセンブリを使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-450">In the **customization.settings** file, change the **@(RetailServerLibraryPathForProxyGeneration)** section so that it uses the new Retail Server assembly for proxy generation.</span></span>
2. <span data-ttu-id="1cc13-451">**StoreOperationsManager** クラスで次のインターフェイス メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-451">Implement the following interface methods in the **StoreOperationsManager** class.</span></span> <span data-ttu-id="1cc13-452">最初の繰り返しには、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-452">For the first iteration, add the following code:</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-453">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-453">Application update 4</span></span>](#tab/app-update-4)

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

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-454">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-454">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

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

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-455">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-455">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="1cc13-456">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-456">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-457">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-457">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="1cc13-458">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-458">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-459">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-459">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="1cc13-460">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-460">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-461">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-461">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="1cc13-462">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-462">This step doesn't apply to this version.</span></span>

    ---

3. <span data-ttu-id="1cc13-463">プロキシ コードを再生成するには、コマンドラインから **msbuild/t:Rebuild** コマンドを使用して**プロキシ**フォルダーを構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-463">To regenerate the proxy code, build the **Proxies** folder from the command line by using the **msbuild /t:Rebuild** command.</span></span>
4. <span data-ttu-id="1cc13-464">**Proxies.RetailProxy** プロジェクトの依存関係を解決します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-464">Resolve the **Proxies.RetailProxy** project dependencies:</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-465">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-465">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="1cc13-466">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** project to reference **SalesTransactionSignatureSample** に追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-466">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, add the **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** project to the solution, and add a project reference to the **RetailProxy** project to reference **SalesTransactionSignatureSample**.</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-467">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-467">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="1cc13-468">**RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** プロジェクトと、**SalesTransactionSignatureSample.Messages**参照に追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-468">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, add the **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** project to the solution, and add a project reference to the **RetailProxy** project to reference **SalesTransactionSignatureSample.Messages**.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-469">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-469">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="1cc13-470">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-470">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-471">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-471">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="1cc13-472">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-472">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-473">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-473">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="1cc13-474">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-474">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-475">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-475">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="1cc13-476">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-476">This step doesn't apply to this version.</span></span>

    ---

5. <span data-ttu-id="1cc13-477">**StoreOperationsManager** クラスでインターフェイス メソッドを調節します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-477">Adjust the interface methods in the **StoreOperationsManager** class:</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-478">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-478">Application update 4</span></span>](#tab/app-update-4)

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

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-479">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-479">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

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

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-480">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-480">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="1cc13-481">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-481">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-482">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-482">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="1cc13-483">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-483">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-484">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-484">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="1cc13-485">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-485">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-486">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-486">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="1cc13-487">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1cc13-487">This step doesn't apply to this version.</span></span>

    ---

6. <span data-ttu-id="1cc13-488">**dllhost.exe.config** ファイルを更新し、クライアント ブローカーが新しい RetailProxy アセンブリを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-488">Update the **dllhost.exe.config** file so that the client broker loads the new RetailProxy assembly.</span></span>

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a><span data-ttu-id="1cc13-489">小売プロキシ拡張コンポーネント (Retail 7.3.1 およびそれ以降)</span><span class="sxs-lookup"><span data-stu-id="1cc13-489">Retail proxy extension component (Retail 7.3.1 and later)</span></span>

<span data-ttu-id="1cc13-490">Retail 7.3.1 もしくはそれ以降を使用しているときに限り、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-490">Complete the following procedure only if you're using Retail 7.3.1 and later.</span></span>

1. <span data-ttu-id="1cc13-491">**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample**  フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-491">In the **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="1cc13-492">**RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-492">In the **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** assembly file.</span></span>
3. <span data-ttu-id="1cc13-493">アセンブリ ファイルをローカル CRT クライアント ブローカーの下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-493">Copy the assembly files to the **\\ext** folder under the local CRT client broker location.</span></span>
4. <span data-ttu-id="1cc13-494">拡張機能コンフィギュレーション ファイルで 小売プロキシの変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-494">Register the Retail proxy change in the extensions configuration file.</span></span> <span data-ttu-id="1cc13-495">ファイル名は **RetailProxy.MPOSOffline.ext.config** で、ローカル CRT クライアント ブローカーの場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-495">The file is named **RetailProxy.MPOSOffline.ext.config**, and it's under the local CRT client broker location.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a><span data-ttu-id="1cc13-496">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-496">Modern POS extension components</span></span>

1. <span data-ttu-id="1cc13-497">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-497">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="1cc13-498">また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-498">Additionally, make sure that you can run Modern POS from Microsoft Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1cc13-499">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="1cc13-499">Modern POS must not be customized.</span></span> <span data-ttu-id="1cc13-500">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-500">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

2. <span data-ttu-id="1cc13-501">**Pos.Extensions** プロジェクトが、次の既存のソース コード フォルダーを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-501">Include the following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-502">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-502">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="1cc13-503">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-503">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-504">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-504">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-505">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-505">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="1cc13-506">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-506">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-507">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-507">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-508">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-508">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="1cc13-509">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-509">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-510">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-510">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-511">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-511">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="1cc13-512">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-512">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-513">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-513">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-514">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-514">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-515">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-515">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-516">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-516">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="1cc13-517">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-517">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-518">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-518">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-519">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-519">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-520">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-520">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="1cc13-521">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-521">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-522">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-522">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-523">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-523">SequentialSignature</span></span>

    ---

3. <span data-ttu-id="1cc13-524">除外リストから次のフォルダーを削除して、**tsconfig.json** で拡張機能がコンパイルされるようにします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-524">Enable the extensions to be compiled in **tsconfig.json** by removing the following folders from the exclude list.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-525">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-525">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="1cc13-526">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-526">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-527">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-527">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-528">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-528">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="1cc13-529">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-529">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-530">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-530">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-531">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-531">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="1cc13-532">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-532">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-533">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-533">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-534">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-534">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="1cc13-535">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-535">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-536">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-536">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-537">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-537">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-538">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-538">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-539">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-539">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="1cc13-540">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-540">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-541">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-541">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-542">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-542">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-543">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-543">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="1cc13-544">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-544">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-545">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-545">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-546">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-546">SequentialSignature</span></span>

    ---

4. <span data-ttu-id="1cc13-547">適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-547">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate place.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-548">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-548">Application update 4</span></span>](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-549">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-549">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-550">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-550">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-551">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-551">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-552">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-552">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-553">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-553">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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
    > <span data-ttu-id="1cc13-554">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1cc13-554">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="1cc13-555">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-555">Rebuild the solution.</span></span>
6. <span data-ttu-id="1cc13-556">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-556">Run Modern POS in the debugger, and test the functionality.</span></span>

### <a name="cloud-pos-extension-components"></a><span data-ttu-id="1cc13-557">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="1cc13-557">Cloud POS extension components</span></span>

1. <span data-ttu-id="1cc13-558">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-558">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="1cc13-559">**Pos.Extensions** プロジェクトの、既存ソース コード フォルダーを含めます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-559">Include following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-560">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-560">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="1cc13-561">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-561">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-562">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-562">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-563">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-563">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="1cc13-564">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-564">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-565">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-565">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-566">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-566">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="1cc13-567">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-567">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-568">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-568">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-569">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-569">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="1cc13-570">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-570">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-571">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-571">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-572">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-572">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-573">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-573">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-574">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-574">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="1cc13-575">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-575">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-576">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-576">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-577">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-577">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-578">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-578">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="1cc13-579">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-579">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-580">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-580">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-581">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-581">SequentialSignature</span></span>

    ---

3. <span data-ttu-id="1cc13-582">除外リストから次のフォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-582">Enable the extensions to be compiled in **tsconfig.json** by removing following folders from the exclude list.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-583">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-583">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="1cc13-584">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-584">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-585">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-585">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-586">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-586">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="1cc13-587">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-587">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-588">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-588">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-589">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-589">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="1cc13-590">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-590">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-591">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-591">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-592">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-592">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="1cc13-593">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-593">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="1cc13-594">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-594">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-595">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-595">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-596">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-596">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-597">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-597">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="1cc13-598">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-598">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-599">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-599">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-600">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-600">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-601">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-601">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="1cc13-602">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="1cc13-602">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="1cc13-603">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="1cc13-603">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="1cc13-604">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="1cc13-604">SequentialSignature</span></span>

    ---

4. <span data-ttu-id="1cc13-605">適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-605">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate place.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-606">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-606">Application update 4</span></span>](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-607">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-607">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-608">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-608">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-609">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-609">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-610">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-610">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-611">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-611">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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
    > <span data-ttu-id="1cc13-612">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1cc13-612">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="1cc13-613">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-613">Rebuild the solution.</span></span>
6. <span data-ttu-id="1cc13-614">**実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-614">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>
7. <span data-ttu-id="1cc13-615">機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-615">Test the functionality.</span></span>

### <a name="set-up-required-parameters-in-retail-headquarters"></a><span data-ttu-id="1cc13-616">小売用バックオフィスで要求されるパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-616">Set up required parameters in Retail headquarters</span></span>

<span data-ttu-id="1cc13-617">詳細については、[ノルウェーのキャッシュ レジスター](./emea-nor-cash-registers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1cc13-617">For more information, see [Cash registers for Norway](./emea-nor-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="1cc13-618">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="1cc13-618">Production environment</span></span>

<span data-ttu-id="1cc13-619">以下の手順に従い、小売コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-619">Follow these steps to create deployable packages that contain Retail components, and to apply those packages in a production environment.</span></span>

1. <span data-ttu-id="1cc13-620">[クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-620">Complete the steps in the [Cloud POS extension components](#cloud-pos-extension-components) or [Modern POS extension components](#modern-pos-extension-components) section earlier in this topic.</span></span>
2. <span data-ttu-id="1cc13-621">**RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-621">Make the following changes in the package configuration files under the **RetailSdk\\Assets** folder:</span></span>

    1. <span data-ttu-id="1cc13-622">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの**構成**セクションに、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-622">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files, add the following lines to the **composition** section:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-623">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-623">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-624">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-624">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-625">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-625">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-626">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-626">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-627">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-627">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-628">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-628">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. <span data-ttu-id="1cc13-629">小売プロキシ カスタマイズを有効にします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-629">Enable Retail Proxy customization:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-630">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-630">Application update 4</span></span>](#tab/app-update-4)

        <span data-ttu-id="1cc13-631">**dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-631">In the **dllhost.exe.config** configuration file, add the following lines to the **appSettings** subsection of the **configuration** section.</span></span>

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-632">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-632">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        <span data-ttu-id="1cc13-633">**dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-633">In the **dllhost.exe.config** configuration file, add the following lines to the **appSettings** subsection of the **configuration** section.</span></span>

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-634">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-634">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="1cc13-635">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-635">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-636">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-636">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        <span data-ttu-id="1cc13-637">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-637">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-638">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-638">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        <span data-ttu-id="1cc13-639">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-639">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-640">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-640">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        <span data-ttu-id="1cc13-641">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-641">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. <span data-ttu-id="1cc13-642">**Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-642">Make the following changes in the **Customization.settings** package customization configuration file:</span></span>

    1. <span data-ttu-id="1cc13-643">小売プロキシ カスタマイズを有効にします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-643">Enable Retail Proxy customization.</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-644">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-644">Application update 4</span></span>](#tab/app-update-4)

        <span data-ttu-id="1cc13-645">**&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-645">Add the following lines to the **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** section.</span></span>

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-646">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-646">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        <span data-ttu-id="1cc13-647">**&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-647">Add the following lines to the **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** section.</span></span>

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-648">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-648">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="1cc13-649">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-649">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-650">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-650">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        <span data-ttu-id="1cc13-651">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-651">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-652">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-652">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        <span data-ttu-id="1cc13-653">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-653">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-654">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-654">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        <span data-ttu-id="1cc13-655">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-655">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. <span data-ttu-id="1cc13-656">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-656">Add the following lines to the **ItemGroup** section to include the CRT extensions in the deployable packages:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-657">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-657">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-658">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-658">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-659">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-659">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-660">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-660">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-661">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-661">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-662">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-662">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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

    3. <span data-ttu-id="1cc13-663">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに Retail Server 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-663">Add following lines to the **ItemGroup** section to include the Retail Server extension in the deployable packages:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-664">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-664">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-665">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-665">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-666">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-666">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-667">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-667">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-668">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-668">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-669">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-669">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. <span data-ttu-id="1cc13-670">拇印、保管場所、署名販売取引に使用されるべき証明書の保存名を指定して、証明書のコンフィギュレーションを変更します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-670">Modify the certificate's configuration file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span> <span data-ttu-id="1cc13-671">その後 **References** フォルダーにコンフィギュレーション ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-671">Then copy the configuration file to the **References** folder.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="1cc13-672">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="1cc13-672">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="1cc13-673">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-673">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="1cc13-674">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-674">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="1cc13-675">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-675">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="1cc13-676">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="1cc13-676">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    <span data-ttu-id="1cc13-677">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-677">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="1cc13-678">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-678">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    <span data-ttu-id="1cc13-679">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-679">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="1cc13-680">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-680">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    <span data-ttu-id="1cc13-681">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-681">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="1cc13-682">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="1cc13-682">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    <span data-ttu-id="1cc13-683">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-683">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    ---

5. <span data-ttu-id="1cc13-684">Retail Server コンフィギュレーション ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-684">Update Retail Server configuration file.</span></span> <span data-ttu-id="1cc13-685">**RetailSDK\\Packages\\RetailServer\\Code\\web.config** ファイルの **extensionComposition** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-685">In the **RetailSDK\\Packages\\RetailServer\\Code\\web.config** file, add the following lines to the **extensionComposition** section.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. <span data-ttu-id="1cc13-686">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-686">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
7. <span data-ttu-id="1cc13-687">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-687">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="1cc13-688">詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1cc13-688">For more information, see [Retail SDK packaging](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a><span data-ttu-id="1cc13-689">Modern POS のオフライン モードでのデジタル署名を有効にします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-689">Enable the digital signature in offline mode for Modern POS</span></span>

<span data-ttu-id="1cc13-690">Modern POSでオフライン モードでのデジタル署名を有効にするには、新しい端末で Modern POS を有効化した後、これらの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="1cc13-690">To enable the digital signature in offline mode for Modern POS, you must follow these steps after you activate Modern POS on a new device.</span></span>

1. <span data-ttu-id="1cc13-691">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-691">Sign in to POS.</span></span>
2. <span data-ttu-id="1cc13-692">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-692">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="1cc13-693">**ダウンロードの保留中**フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="1cc13-693">When the value of the **Pending downloads** field is **0** (zero), the database is fully synchronized.</span></span>
3. <span data-ttu-id="1cc13-694">POS からのサインアウト</span><span class="sxs-lookup"><span data-stu-id="1cc13-694">Sign out of POS.</span></span>
4. <span data-ttu-id="1cc13-695">オフライン データベースが完全に同期するため少しの間待ちます。</span><span class="sxs-lookup"><span data-stu-id="1cc13-695">Wait a while for the offline database to be fully synchronized.</span></span>
5. <span data-ttu-id="1cc13-696">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="1cc13-696">Sign in to POS.</span></span>
6. <span data-ttu-id="1cc13-697">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-697">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="1cc13-698">**オフライン データベースで取引を保留中** フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="1cc13-698">When the value of the **Pending transactions in offline database** field is **0** (zero), the database is fully synchronized.</span></span>
7. <span data-ttu-id="1cc13-699">Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="1cc13-699">Restart Modern POS.</span></span>

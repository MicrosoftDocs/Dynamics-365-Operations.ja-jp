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
ms.openlocfilehash: 7600d436e4ec945d70036b749f1fbb100860ef4c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369278"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a><span data-ttu-id="86c8c-103">ノルウェーのキャッシュ レジスタの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="86c8c-103">Deployment guidelines for cash registers for Norway</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86c8c-104">このトピックは、Microsoft Dynamics 365 for Retail のノルウェーでのローカライズを有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="86c8c-104">This topic is a deployment guide that shows how to enable the Microsoft Dynamics 365 for Retail localization for Norway.</span></span> <span data-ttu-id="86c8c-105">ローカライズは、小売コンポーネントのいくつかの拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-105">The localization consists of several extensions of Retail components.</span></span> <span data-ttu-id="86c8c-106">たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、および販売時点管理 (POS) での支払取引を登録、デジタル署名販売取引、およびローカルの形式で X および Z レポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-106">For example, the extensions let you print custom fields on receipts, register additional audit events, sales transactions, and payment transactions in Point of Sale (POS), digitally sign sales transactions, and print X and Z reports in local formats.</span></span> <span data-ttu-id="86c8c-107">ノルウェーの小売ローカライズの詳細については、[ノルウェーのキャッシュ レジスター](./emea-nor-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86c8c-107">For more information about the Retail localization for Norway, see [Cash registers for Norway](./emea-nor-cash-registers.md).</span></span>

<span data-ttu-id="86c8c-108">このサンプルは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="86c8c-108">This sample is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="86c8c-109">リテール SDK をダウンロードして使用する方法については、[リテール SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86c8c-109">For information about how to install and use the Retail SDK, see the [Retail SDK documentation](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="86c8c-110">このサンプルは Commerce runtime (CRT)、Retail Server、そして POS の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-110">This sample consists of extensions for the Commerce runtime (CRT), Retail Server, and POS.</span></span> <span data-ttu-id="86c8c-111">このサンプルを実行するには、CRT、Retail Servers および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-111">To run this sample, you must modify and build the CRT, Retail Server, and POS projects.</span></span> <span data-ttu-id="86c8c-112">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-112">We recommend that you use an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="86c8c-113">また Microsoft Visual Studio オンライン (VSO) のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-113">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE] 
> <span data-ttu-id="86c8c-114">使用しているバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-114">Some steps in the procedures in this topic differ, depending on the version of Retail that you're using.</span></span> <span data-ttu-id="86c8c-115">詳細については、[Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86c8c-115">For more information, see [What's new or changed in Dynamics 365 for Retail](../get-started/whats-new.md).</span></span>

## <a name="development-environment"></a><span data-ttu-id="86c8c-116">開発環境</span><span class="sxs-lookup"><span data-stu-id="86c8c-116">Development environment</span></span>

<span data-ttu-id="86c8c-117">サンプルをテストして拡張できるように開発環境を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-117">Complete these procedures to set up a development environment so that you can test and extend the sample.</span></span>

### <a name="the-crt-extension-components"></a><span data-ttu-id="86c8c-118">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-118">The CRT extension components</span></span>

<span data-ttu-id="86c8c-119">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-119">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="86c8c-120">次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-120">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

#### <a name="receiptsnorway-component"></a><span data-ttu-id="86c8c-121">ReceiptsNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-121">ReceiptsNorway component</span></span>

1. <span data-ttu-id="86c8c-122">**Runtime.Extensions.ReceiptsNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-122">Find the **Runtime.Extensions.ReceiptsNorway** project, and build it.</span></span>
2. <span data-ttu-id="86c8c-123">**Extensions.ReceiptsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.ReceiptsNorway.dll** アセンブリファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-123">In the **Extensions.ReceiptsNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.ReceiptsNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-124">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-124">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-125">**Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-125">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-126">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-126">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-127">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-127">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-128">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-128">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-129">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-129">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-130">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-130">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-131">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-131">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-132">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-132">These files aren't intended for any customizations.</span></span>

#### <a name="salespaymenttransext-component"></a><span data-ttu-id="86c8c-133">SalesPaymentTransExt コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-133">SalesPaymentTransExt component</span></span>

1. <span data-ttu-id="86c8c-134">**Runtime.Extensions.SalesPaymentTransExt** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-134">Find the **Runtime.Extensions.SalesPaymentTransExt** project, and build it.</span></span>
2. <span data-ttu-id="86c8c-135">**Extensions.SalesPaymentTransExt\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-135">In the **Extensions.SalesPaymentTransExt\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-136">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-136">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-137">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-137">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-138">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-138">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-139">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-139">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-140">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-140">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-141">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-141">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-142">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-142">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-143">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-143">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-144">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-144">These files aren't intended for any customizations.</span></span>

#### <a name="xzreportsnorway-component"></a><span data-ttu-id="86c8c-145">XZReportsNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-145">XZReportsNorway component</span></span>

1. <span data-ttu-id="86c8c-146">**Runtime.Extensions.XZReportsNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-146">Find the **Runtime.Extensions.XZReportsNorway** project, and build it.</span></span>
2. <span data-ttu-id="86c8c-147">**Extensions.XZReportsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.XZReportsNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-147">In the **Extensions.XZReportsNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.XZReportsNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-148">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-148">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-149">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-149">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-150">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-150">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-151">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-151">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-152">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-152">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-153">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-153">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-154">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-154">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-155">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-155">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-156">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-156">These files aren't intended for any customizations.</span></span>

# <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-157">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-157">Application update 4</span></span>](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="86c8c-158">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-158">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="86c8c-159">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-159">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="86c8c-160">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-160">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-161">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-161">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-162">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-162">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-163">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-163">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-164">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-164">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-165">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-165">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-166">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-166">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-167">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-167">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-168">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-168">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-169">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-169">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="86c8c-170">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-170">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="86c8c-171">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-171">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="86c8c-172">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-172">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="86c8c-173">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-173">Build the project.</span></span>
4. <span data-ttu-id="86c8c-174">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-174">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="86c8c-175">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-175">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="86c8c-176">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-176">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="86c8c-177">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-177">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-178">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-178">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-179">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-179">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="86c8c-180">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-180">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-181">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-181">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-182">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-182">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="86c8c-183">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-183">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-184">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-184">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-185">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-185">These files aren't intended for any customizations.</span></span>

# <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-186">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-186">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="86c8c-187">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-187">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="86c8c-188">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-188">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="86c8c-189">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-189">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-190">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-190">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-191">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-191">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-192">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-192">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-193">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-193">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-194">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-194">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-195">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-195">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-196">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-196">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-197">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-197">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-198">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-198">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="86c8c-199">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-199">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="86c8c-200">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-200">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="86c8c-201">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-201">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="86c8c-202">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-202">Build the project.</span></span>
4. <span data-ttu-id="86c8c-203">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-203">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="86c8c-204">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-204">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="86c8c-205">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-205">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="86c8c-206">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-206">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-207">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-207">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-208">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-208">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="86c8c-209">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-209">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-210">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-210">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-211">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-211">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="86c8c-212">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-212">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-213">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-213">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-214">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-214">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturesamplemessages-component"></a><span data-ttu-id="86c8c-215">SalesTransactionSignatureSample.Messages コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-215">SalesTransactionSignatureSample.Messages component</span></span>

1. <span data-ttu-id="86c8c-216">**Runtime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-216">Find the **Runtime.Extensions.SalesTransactionSignatureSample.Messages** project.</span></span>
2. <span data-ttu-id="86c8c-217">**Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-217">In the **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-218">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-218">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-219">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-219">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-220">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-220">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-221">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-221">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-222">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-222">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-223">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-223">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-224">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-224">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-225">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-225">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-226">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-226">These files aren't intended for any customizations.</span></span>

# <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-227">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-227">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="86c8c-228">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-228">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="86c8c-229">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-229">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="86c8c-230">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-230">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-231">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-231">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-232">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-232">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-233">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-233">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-234">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-234">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-235">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-235">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-236">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-236">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-237">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-237">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-238">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-238">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-239">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-239">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="86c8c-240">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-240">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="86c8c-241">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-241">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="86c8c-242">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-242">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="86c8c-243">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-243">Build the project.</span></span>
4. <span data-ttu-id="86c8c-244">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-244">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="86c8c-245">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-245">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="86c8c-246">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-246">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="86c8c-247">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-247">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-248">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-248">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-249">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-249">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="86c8c-250">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-250">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-251">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-251">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-252">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-252">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="86c8c-253">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-253">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-254">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-254">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-255">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-255">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="86c8c-256">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-256">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="86c8c-257">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-257">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="86c8c-258">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-258">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-259">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-259">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-260">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-260">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-261">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-261">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

# <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-262">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-262">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="86c8c-263">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-263">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="86c8c-264">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-264">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="86c8c-265">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-265">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-266">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-266">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-267">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-267">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-268">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-268">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-269">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-269">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-270">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-270">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-271">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-271">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-272">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-272">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-273">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-273">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-274">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-274">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="86c8c-275">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-275">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="86c8c-276">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-276">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="86c8c-277">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-277">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="86c8c-278">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-278">Build the project.</span></span>
4. <span data-ttu-id="86c8c-279">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-279">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="86c8c-280">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-280">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="86c8c-281">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-281">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="86c8c-282">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-282">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-283">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-283">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-284">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-284">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="86c8c-285">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-285">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-286">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-286">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-287">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-287">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="86c8c-288">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-288">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="86c8c-289">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-289">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="86c8c-290">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-290">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-291">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-291">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-292">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-292">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-293">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-293">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-294">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-294">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-295">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-295">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-296">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-296">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-297">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-297">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-298">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-298">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-299">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-299">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="86c8c-300">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-300">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="86c8c-301">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-301">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="86c8c-302">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-302">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-303">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-303">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-304">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-304">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-305">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-305">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="86c8c-306">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-306">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="86c8c-307">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-307">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="86c8c-308">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-308">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-309">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-309">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-310">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-310">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-311">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-311">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-312">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-312">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-313">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-313">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-314">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-314">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-315">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-315">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-316">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-316">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-317">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-317">These files aren't intended for any customizations.</span></span>

# <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-318">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-318">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="86c8c-319">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-319">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="86c8c-320">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-320">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="86c8c-321">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-321">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="86c8c-322">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-322">Build the project.</span></span>
4. <span data-ttu-id="86c8c-323">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-323">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="86c8c-324">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-324">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="86c8c-325">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-325">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="86c8c-326">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-326">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-327">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-327">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-328">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-328">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="86c8c-329">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-329">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-330">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-330">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-331">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-331">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="86c8c-332">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-332">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="86c8c-333">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-333">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="86c8c-334">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-334">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-335">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-335">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-336">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-336">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-337">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-337">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-338">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-338">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-339">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-339">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-340">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-340">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-341">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-341">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-342">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-342">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-343">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-343">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="86c8c-344">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-344">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="86c8c-345">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-345">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="86c8c-346">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-346">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-347">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-347">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-348">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-348">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-349">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-349">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="86c8c-350">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-350">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="86c8c-351">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-351">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="86c8c-352">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-352">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-353">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-353">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-354">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-354">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-355">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-355">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-356">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-356">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-357">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-357">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-358">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-358">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-359">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-359">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-360">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-360">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-361">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-361">These files aren't intended for any customizations.</span></span>

# <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-362">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-362">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="86c8c-363">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-363">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="86c8c-364">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-364">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="86c8c-365">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-365">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="86c8c-366">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-366">Build the project.</span></span>
4. <span data-ttu-id="86c8c-367">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-367">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="86c8c-368">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-368">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="86c8c-369">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-369">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="86c8c-370">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-370">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-371">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-371">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-372">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-372">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="86c8c-373">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-373">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-374">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-374">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-375">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-375">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="86c8c-376">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-376">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="86c8c-377">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-377">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="86c8c-378">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-378">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-379">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-379">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-380">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-380">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-381">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-381">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-382">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-382">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-383">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-383">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-384">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-384">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-385">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-385">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-386">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-386">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-387">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-387">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="86c8c-388">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-388">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="86c8c-389">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-389">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="86c8c-390">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-390">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-391">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-391">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-392">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-392">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-393">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-393">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="86c8c-394">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-394">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="86c8c-395">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-395">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="86c8c-396">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-396">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-397">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-397">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="86c8c-398">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-398">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-399">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-399">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="86c8c-400">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-400">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="86c8c-401">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-401">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="86c8c-402">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-402">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="86c8c-403">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-403">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="86c8c-404">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="86c8c-404">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="86c8c-405">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-405">These files aren't intended for any customizations.</span></span>

---

### <a name="the-retail-server-extension-components"></a><span data-ttu-id="86c8c-406">Retail Server 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-406">The Retail Server extension components</span></span>

#### <a name="salestransactionsignature-retail-server-sample-component"></a><span data-ttu-id="86c8c-407">SalesTransactionSignature Retail Server サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-407">SalesTransactionSignature Retail Server sample component</span></span>

1. <span data-ttu-id="86c8c-408">**RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-408">In the **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="86c8c-409">**RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.RetailServer.SalesTransactionSignatureSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-409">In the **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.RetailServer.SalesTransactionSignatureSample.dll** assembly file.</span></span>
3. <span data-ttu-id="86c8c-410">アセンブリ ファイルを Retail Server 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-410">Copy the assembly file to the Retail Server extensions folder.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-411">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-411">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="86c8c-412">フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="86c8c-412">The folder is the **\\bin** folder under the IIS Retail Server site location.</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-413">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-413">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="86c8c-414">フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="86c8c-414">The folder is the **\\bin** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-415">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-415">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    <span data-ttu-id="86c8c-416">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="86c8c-416">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-417">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-417">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    <span data-ttu-id="86c8c-418">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="86c8c-418">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-419">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-419">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    <span data-ttu-id="86c8c-420">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="86c8c-420">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-421">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-421">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    <span data-ttu-id="86c8c-422">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="86c8c-422">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    ---

4. <span data-ttu-id="86c8c-423">Retail Server のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-423">Find the configuration file for Retail Server.</span></span> <span data-ttu-id="86c8c-424">ファイル名は **web.config** で、IIS Retail Server サイトがある場所の下のルート フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-424">The file is named **web.config**, and it's in the root folder under the IIS Retail Server site location.</span></span>

5. <span data-ttu-id="86c8c-425">コンフィギュレーションの **extensionComposition** セクションで Retail Server 拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-425">Register the Retail Server extensions in the **extensionComposition** section of the configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. <span data-ttu-id="86c8c-426">Retail Server 拡張機能の依存関係を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-426">Register the dependencies of the Retail Server extensions.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-427">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-427">Application update 4</span></span>](#tab/app-update-4/)

    1. <span data-ttu-id="86c8c-428">**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-428">In the **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

        - <span data-ttu-id="86c8c-429">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-429">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
        - <span data-ttu-id="86c8c-430">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="86c8c-430">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

    2. <span data-ttu-id="86c8c-431">ファイルを、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-431">Copy the files to the **\\bin** folder under the IIS Retail Server site location.</span></span>

    3. <span data-ttu-id="86c8c-432">CRT 用コンフィギュレーション ファイルで CTR の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-432">Register the CRT change in the extensions configuration file for CRT.</span></span> <span data-ttu-id="86c8c-433">ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-433">This file is named **commerceruntime.ext.config**, and it's in the **bin** folder under the IIS Retail Server site location.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-434">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-434">Application update 5 and later</span></span>](#tab/app-update-5-and-later/)

    1. <span data-ttu-id="86c8c-435">**CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-435">In the **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** assembly file.</span></span>

    2. <span data-ttu-id="86c8c-436">ファイルをIIS Retail Server サイトがある場所の **\\bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-436">Copy the file to the **\\bin** folder under the IIS Retail Server site location.</span></span>

    3. <span data-ttu-id="86c8c-437">CRT 用コンフィギュレーション ファイルで CTR の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-437">Register the CRT change in the extensions configuration file for CRT.</span></span> <span data-ttu-id="86c8c-438">ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-438">This file is named **commerceruntime.ext.config**, and it's in the **bin** folder under the IIS Retail Server site location.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-439">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-439">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="86c8c-440">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="86c8c-440">No actions are required.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-441">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-441">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="86c8c-442">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="86c8c-442">No actions are required.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-443">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-443">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)
    > [!NOTE]
    > <span data-ttu-id="86c8c-444">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="86c8c-444">No actions are required.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-445">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-445">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)
    > [!NOTE]
    > <span data-ttu-id="86c8c-446">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="86c8c-446">No actions are required.</span></span>

    ---

### <a name="the-modern-pos-extension-components"></a><span data-ttu-id="86c8c-447">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-447">The Modern POS extension components</span></span>

#### <a name="implement-the-proxy-code-for-offline-mode"></a><span data-ttu-id="86c8c-448">オフライン モード用プロキシ コードを実装します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-448">Implement the proxy code for offline mode</span></span>

<span data-ttu-id="86c8c-449">この箇所は Retail Server コントローラーと同じですが、クライアントが接続されていない場合に使用されるローカル CRT を拡張します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-449">This part is equivalent to the Retail Server controller, but it extends the local CRT that is used when the client isn't connected.</span></span>

1. <span data-ttu-id="86c8c-450">**Customization.settings** ファイルで、**@(RetailServerLibraryPathForProxyGeneration)** セクションを変更し、プロキシ生成で新しい Retail Server アセンブリを使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-450">In the **customization.settings** file, change the **@(RetailServerLibraryPathForProxyGeneration)** section so that it uses the new Retail Server assembly for proxy generation.</span></span>
2. <span data-ttu-id="86c8c-451">**StoreOperationsManager** クラスで次のインターフェイス メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-451">Implement the following interface methods in the **StoreOperationsManager** class.</span></span> <span data-ttu-id="86c8c-452">最初の繰り返しには、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-452">For the first iteration, add the following code:</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-453">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-453">Application update 4</span></span>](#tab/app-update-4)

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

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-454">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-454">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

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

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-455">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-455">Retail 7.3.1</span></span>](#tab/retail-7-3-1)
    > [!NOTE]
    > <span data-ttu-id="86c8c-456">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-456">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-457">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-457">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="86c8c-458">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-458">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-459">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-459">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="86c8c-460">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-460">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-461">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-461">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="86c8c-462">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-462">This step doesn't apply to this version.</span></span>

    ---

3. <span data-ttu-id="86c8c-463">プロキシ コードを再生成するには、コマンドラインから **msbuild/t:Rebuild** コマンドを使用して**プロキシ**フォルダーを構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-463">To regenerate the proxy code, build the **Proxies** folder from the command line by using the **msbuild /t:Rebuild** command.</span></span>
4. <span data-ttu-id="86c8c-464">**Proxies.RetailProxy** プロジェクトの依存関係を解決します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-464">Resolve the **Proxies.RetailProxy** project dependencies:</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-465">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-465">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="86c8c-466">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** project to reference **SalesTransactionSignatureSample** に追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-466">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, add the **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** project to the solution, and add a project reference to the **RetailProxy** project to reference **SalesTransactionSignatureSample**.</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-467">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-467">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="86c8c-468">**RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** プロジェクトと、**SalesTransactionSignatureSample.Messages**参照に追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-468">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, add the **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** project to the solution, and add a project reference to the **RetailProxy** project to reference **SalesTransactionSignatureSample.Messages**.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-469">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-469">Retail 7.3.1</span></span>](#tab/retail-7-3-1)
    > [!NOTE]
    > <span data-ttu-id="86c8c-470">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-470">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-471">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-471">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="86c8c-472">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-472">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-473">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-473">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="86c8c-474">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-474">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-475">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-475">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="86c8c-476">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-476">This step doesn't apply to this version.</span></span>

    ---

5. <span data-ttu-id="86c8c-477">**StoreOperationsManager** クラスでインターフェイス メソッドを調節します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-477">Adjust the interface methods in the **StoreOperationsManager** class:</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-478">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-478">Application update 4</span></span>](#tab/app-update-4)

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

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-479">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-479">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

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

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-480">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-480">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="86c8c-481">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-481">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-482">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-482">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="86c8c-483">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-483">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-484">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-484">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="86c8c-485">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-485">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-486">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-486">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="86c8c-487">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="86c8c-487">This step doesn't apply to this version.</span></span>

    ---

6. <span data-ttu-id="86c8c-488">**dllhost.exe.config** ファイルを更新し、クライアント ブローカーが新しい RetailProxy アセンブリを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-488">Update the **dllhost.exe.config** file so that the client broker loads the new RetailProxy assembly.</span></span>

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a><span data-ttu-id="86c8c-489">小売プロキシ拡張コンポーネント (Retail 7.3.1 およびそれ以降)</span><span class="sxs-lookup"><span data-stu-id="86c8c-489">Retail proxy extension component (Retail 7.3.1 and later)</span></span>
<span data-ttu-id="86c8c-490">Retail 7.3.1 もしくはそれ以降を使用しているときに限り、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-490">Complete the following procedure only if you're using Retail 7.3.1 and later.</span></span> 

1. <span data-ttu-id="86c8c-491">**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample**  フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-491">In the **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>

2. <span data-ttu-id="86c8c-492">**RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-492">In the **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** assembly file.</span></span>

3. <span data-ttu-id="86c8c-493">アセンブリ ファイルをローカル CRT クライアント ブローカーの下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-493">Copy the assembly files to the **\\ext** folder under the local CRT client broker location.</span></span>
4. <span data-ttu-id="86c8c-494">拡張機能コンフィギュレーション ファイルで 小売プロキシの変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-494">Register the Retail proxy change in the extensions configuration file.</span></span> <span data-ttu-id="86c8c-495">ファイル名は **RetailProxy.MPOSOffline.ext.config** で、ローカル CRT クライアント ブローカーの場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-495">The file is named **RetailProxy.MPOSOffline.ext.config**, and it's under the local CRT client broker location.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a><span data-ttu-id="86c8c-496">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-496">Modern POS extension components</span></span>

1. <span data-ttu-id="86c8c-497">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-497">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="86c8c-498">また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-498">Additionally, make sure that you can run Modern POS from Microsoft Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86c8c-499">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="86c8c-499">Modern POS must not be customized.</span></span> <span data-ttu-id="86c8c-500">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-500">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

2. <span data-ttu-id="86c8c-501">**Pos.Extensions** プロジェクトが、次の既存のソース コード フォルダーを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-501">Include the following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-502">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-502">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="86c8c-503">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-503">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-504">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-504">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-505">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-505">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="86c8c-506">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-506">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-507">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-507">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-508">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-508">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="86c8c-509">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-509">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-510">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-510">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-511">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-511">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="86c8c-512">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-512">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-513">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-513">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-514">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-514">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-515">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-515">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-516">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-516">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="86c8c-517">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-517">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-518">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-518">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-519">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-519">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-520">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-520">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="86c8c-521">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-521">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-522">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-522">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-523">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-523">SequentialSignature</span></span>

    ---

3. <span data-ttu-id="86c8c-524">除外リストから次のフォルダーを削除して、**tsconfig.json** で拡張機能がコンパイルされるようにします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-524">Enable the extensions to be compiled in **tsconfig.json** by removing the following folders from the exclude list.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-525">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-525">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="86c8c-526">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-526">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-527">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-527">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-528">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-528">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="86c8c-529">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-529">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-530">SalesTransactionSignatureSample\*\*</span><span class="sxs-lookup"><span data-stu-id="86c8c-530">SalesTransactionSignatureSample\*\*</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-531">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-531">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="86c8c-532">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-532">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-533">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-533">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-534">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-534">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="86c8c-535">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-535">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-536">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-536">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-537">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-537">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-538">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-538">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-539">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-539">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="86c8c-540">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-540">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-541">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-541">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-542">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-542">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-543">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-543">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="86c8c-544">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-544">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-545">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-545">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-546">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-546">SequentialSignature</span></span>

    ---

4. <span data-ttu-id="86c8c-547">適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-547">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate place.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-548">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-548">Application update 4</span></span>](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-549">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-549">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-550">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-550">Retail 7.3.1</span></span>](#tab/retail-7-3-1)
    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-551">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-551">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-552">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-552">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-553">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-553">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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
    > <span data-ttu-id="86c8c-554">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86c8c-554">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="86c8c-555">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-555">Rebuild the solution.</span></span>
6. <span data-ttu-id="86c8c-556">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-556">Run Modern POS in the debugger, and test the functionality.</span></span>

### <a name="cloud-pos-extension-components"></a><span data-ttu-id="86c8c-557">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="86c8c-557">Cloud POS extension components</span></span>

1. <span data-ttu-id="86c8c-558">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-558">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="86c8c-559">**Pos.Extensions** プロジェクトの、既存ソース コード フォルダーを含めます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-559">Include following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-560">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-560">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="86c8c-561">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-561">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-562">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-562">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-563">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-563">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="86c8c-564">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-564">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-565">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-565">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-566">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-566">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="86c8c-567">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-567">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-568">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-568">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-569">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-569">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="86c8c-570">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-570">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-571">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-571">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-572">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-572">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-573">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-573">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-574">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-574">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="86c8c-575">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-575">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-576">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-576">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-577">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-577">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-578">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-578">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="86c8c-579">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-579">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-580">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-580">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-581">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-581">SequentialSignature</span></span>

    ---

3. <span data-ttu-id="86c8c-582">除外リストから次のフォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-582">Enable the extensions to be compiled in **tsconfig.json** by removing following folders from the exclude list.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-583">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-583">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="86c8c-584">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-584">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-585">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-585">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-586">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-586">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="86c8c-587">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-587">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-588">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-588">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-589">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-589">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="86c8c-590">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-590">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-591">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-591">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-592">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-592">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="86c8c-593">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-593">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="86c8c-594">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-594">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-595">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-595">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-596">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-596">SequentialSignature</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-597">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-597">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="86c8c-598">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-598">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-599">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-599">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-600">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-600">SequentialSignature</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-601">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-601">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="86c8c-602">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="86c8c-602">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="86c8c-603">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="86c8c-603">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="86c8c-604">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="86c8c-604">SequentialSignature</span></span>

    ---

4. <span data-ttu-id="86c8c-605">適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-605">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate place.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-606">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-606">Application update 4</span></span>](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-607">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-607">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-608">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-608">Retail 7.3.1</span></span>](#tab/retail-7-3-1)
    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-609">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-609">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-610">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-610">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO.Extension"
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

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-611">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-611">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO.Extension"
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
    > <span data-ttu-id="86c8c-612">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86c8c-612">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="86c8c-613">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-613">Rebuild the solution.</span></span>
6. <span data-ttu-id="86c8c-614">**実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-614">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>
7. <span data-ttu-id="86c8c-615">機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-615">Test the functionality.</span></span>

### <a name="set-up-required-parameters-in-retail-headquarters"></a><span data-ttu-id="86c8c-616">小売用バックオフィスで要求されるパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-616">Set up required parameters in Retail headquarters</span></span>

<span data-ttu-id="86c8c-617">詳細については、[ノルウェーのキャッシュ レジスター](./emea-nor-cash-registers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86c8c-617">For more information, see [Cash registers for Norway](./emea-nor-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="86c8c-618">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="86c8c-618">Production environment</span></span>

<span data-ttu-id="86c8c-619">以下の手順に従い、小売コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-619">Follow these steps to create deployable packages that contain Retail components, and to apply those packages in a production environment.</span></span>

1. <span data-ttu-id="86c8c-620">[クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-620">Complete the steps in the [Cloud POS extension components](#cloud-pos-extension-components) or [Modern POS extension components](#modern-pos-extension-components) section earlier in this topic.</span></span>
2. <span data-ttu-id="86c8c-621">**RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-621">Make the following changes in the package configuration files under the **RetailSdk\\Assets** folder:</span></span>

    1. <span data-ttu-id="86c8c-622">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの**構成**セクションに、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-622">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files, add the following lines to the **composition** section:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-623">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-623">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
            <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
            <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-624">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-624">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
            <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
            <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-625">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-625">Retail 7.3.1</span></span>](#tab/retail-7-3-1)
        ``` xml
            <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
            <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-626">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-626">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
            <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-627">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-627">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
            <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-628">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-628">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
            <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
            <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
            <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. <span data-ttu-id="86c8c-629">小売プロキシ カスタマイズを有効にします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-629">Enable Retail Proxy customization:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-630">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-630">Application update 4</span></span>](#tab/app-update-4)

        <span data-ttu-id="86c8c-631">**dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-631">In the **dllhost.exe.config** configuration file, add the following lines to the **appSettings** subsection of the **configuration** section.</span></span>

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-632">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-632">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        <span data-ttu-id="86c8c-633">**dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-633">In the **dllhost.exe.config** configuration file, add the following lines to the **appSettings** subsection of the **configuration** section.</span></span>

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-634">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-634">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="86c8c-635">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-635">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-636">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-636">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        <span data-ttu-id="86c8c-637">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-637">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-638">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-638">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        <span data-ttu-id="86c8c-639">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-639">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-640">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-640">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        <span data-ttu-id="86c8c-641">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-641">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. <span data-ttu-id="86c8c-642">**Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-642">Make the following changes in the **Customization.settings** package customization configuration file:</span></span>

    1. <span data-ttu-id="86c8c-643">小売プロキシ カスタマイズを有効にします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-643">Enable Retail Proxy customization</span></span>
        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-644">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-644">Application update 4</span></span>](#tab/app-update-4)

        <span data-ttu-id="86c8c-645">**&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-645">Add the following lines to the **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** section.</span></span>

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-646">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-646">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        <span data-ttu-id="86c8c-647">**&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-647">Add the following lines to the **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** section.</span></span>

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-648">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-648">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="86c8c-649">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-649">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
           <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-650">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-650">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        <span data-ttu-id="86c8c-651">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-651">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
            <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-652">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-652">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        <span data-ttu-id="86c8c-653">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-653">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
            <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-654">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-654">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        <span data-ttu-id="86c8c-655">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-655">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
            <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. <span data-ttu-id="86c8c-656">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-656">Add the following lines to the **ItemGroup** section to include the CRT extensions in the deployable packages:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-657">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-657">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-658">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-658">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-659">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-659">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
           <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-660">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-660">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-661">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-661">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-662">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-662">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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

    3. <span data-ttu-id="86c8c-663">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに Retail Server 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-663">Add following lines to the **ItemGroup** section to include the Retail Server extension in the deployable packages:</span></span>

        # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-664">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-664">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
           <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
           <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
           <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-665">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-665">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
           <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
           <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-666">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-666">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
           <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-667">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-667">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
           <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-668">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-668">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
           <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-669">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-669">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
           <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. <span data-ttu-id="86c8c-670">拇印、保管場所、署名販売取引に使用されるべき証明書の保存名を指定して、証明書のコンフィギュレーションを変更します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-670">Modify the certificate's configuration file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span> <span data-ttu-id="86c8c-671">その後 **References** フォルダーにコンフィギュレーション ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-671">Then copy the configuration file to the **References** folder.</span></span>

    # <a name="application-update-4tabapp-update-4"></a>[<span data-ttu-id="86c8c-672">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="86c8c-672">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="86c8c-673">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-673">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="application-update-5-and-latertabapp-update-5-and-later"></a>[<span data-ttu-id="86c8c-674">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-674">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="86c8c-675">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-675">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="86c8c-676">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="86c8c-676">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    <span data-ttu-id="86c8c-677">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-677">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="86c8c-678">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-678">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    <span data-ttu-id="86c8c-679">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-679">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="86c8c-680">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-680">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    <span data-ttu-id="86c8c-681">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-681">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="86c8c-682">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="86c8c-682">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    <span data-ttu-id="86c8c-683">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-683">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    ---

5. <span data-ttu-id="86c8c-684">Retail Server コンフィギュレーション ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-684">Update Retail Server configuration file.</span></span> <span data-ttu-id="86c8c-685">**RetailSDK\\Packages\\RetailServer\\Code\\web.config** ファイルの **extensionComposition** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-685">In the **RetailSDK\\Packages\\RetailServer\\Code\\web.config** file, add the following lines to the **extensionComposition** section.</span></span>

    ``` xml
        <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. <span data-ttu-id="86c8c-686">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-686">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
7. <span data-ttu-id="86c8c-687">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-687">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="86c8c-688">詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86c8c-688">For more information, see [Retail SDK packaging](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a><span data-ttu-id="86c8c-689">Modern POS のオフライン モードでのデジタル署名を有効にします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-689">Enable the digital signature in offline mode for Modern POS</span></span>

<span data-ttu-id="86c8c-690">Modern POSでオフライン モードでのデジタル署名を有効にするには、新しい端末で Modern POS を有効化した後、これらの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="86c8c-690">To enable the digital signature in offline mode for Modern POS, you must follow these steps after you activate Modern POS on a new device.</span></span>

1. <span data-ttu-id="86c8c-691">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-691">Sign in to POS.</span></span>
2. <span data-ttu-id="86c8c-692">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-692">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="86c8c-693">**ダウンロードの保留中**フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="86c8c-693">When the value of the **Pending downloads** field is **0** (zero), the database is fully synchronized.</span></span>
3. <span data-ttu-id="86c8c-694">POS からのサインアウト</span><span class="sxs-lookup"><span data-stu-id="86c8c-694">Sign out of POS.</span></span>
4. <span data-ttu-id="86c8c-695">オフライン データベースが完全に同期するため少しの間待ちます。</span><span class="sxs-lookup"><span data-stu-id="86c8c-695">Wait a while for the offline database to be fully synchronized.</span></span>
5. <span data-ttu-id="86c8c-696">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="86c8c-696">Sign in to POS.</span></span>
6. <span data-ttu-id="86c8c-697">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-697">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="86c8c-698">**オフライン データベースで取引を保留中** フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="86c8c-698">When the value of the **Pending transactions in offline database** field is **0** (zero), the database is fully synchronized.</span></span>
7. <span data-ttu-id="86c8c-699">Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="86c8c-699">Restart Modern POS.</span></span>

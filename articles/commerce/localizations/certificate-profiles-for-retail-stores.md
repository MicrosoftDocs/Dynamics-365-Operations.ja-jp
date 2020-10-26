---
title: 小売店舗のユーザー定義の証明書プロファイル
description: このトピックでは、小売店舗で証明書を使用する方法についての概要を説明します。
author: josaw
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0b8bf49a8eb78d0557ef105b40dd4cb5f0d24ce4
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973936"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a><span data-ttu-id="13053-103">小売店舗のユーザー定義の証明書プロファイル</span><span class="sxs-lookup"><span data-stu-id="13053-103">User-defined certificate profiles for retail stores</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="13053-104">概要</span><span class="sxs-lookup"><span data-stu-id="13053-104">Overview</span></span>

<span data-ttu-id="13053-105">このトピックでは、Microsoft Dynamics 365 Commerce で利用できる証明書プロファイルの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="13053-105">This topic provides an overview of the certificate profiles that are available in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="13053-106">この機能は、ローカル証明書のサポートを追加することによって[小売チャネルのシークレットを管理](../dev-itpro/manage-secrets.md) の機能を拡張します。</span><span class="sxs-lookup"><span data-stu-id="13053-106">This functionality extends the [Manage secrets for retail channels](../dev-itpro/manage-secrets.md) feature by adding support for local certificates.</span></span>

<span data-ttu-id="13053-107">販売時点管理 (POS) がオフライン モードで実行されている間、キー コンテナーに保存されている証明書にはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="13053-107">While the point of sale (POS) is running in offline mode, it can't access the certificates that are stored in the key vault.</span></span> <span data-ttu-id="13053-108">代わりにローカル証明書を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13053-108">The local certificate should be used instead.</span></span> <span data-ttu-id="13053-109">次の機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="13053-109">The following capabilities are supported:</span></span>

- <span data-ttu-id="13053-110">キー コンテナー予備シナリオでのローカル証明書の使用</span><span class="sxs-lookup"><span data-stu-id="13053-110">Using local certificates in key vault fallback scenarios</span></span>
- <span data-ttu-id="13053-111">キー コンテナーを使用しないローカル証明書の使用 (たとえばオンプレミスのインストールで)</span><span class="sxs-lookup"><span data-stu-id="13053-111">Using local certificates without a key vault (for example in an on-premises installation)</span></span>
- <span data-ttu-id="13053-112">一部の店舗およびターミナルは証明書の新しいバージョンを使用しますが、他の店舗またはターミナルは以前のバージョンを引き続き使用する証明書の段階的な更新</span><span class="sxs-lookup"><span data-stu-id="13053-112">Gradual update of certificates, where some stores and terminals use a new version of the certificate, but other stores and terminals continue to use the previous version</span></span>

<span data-ttu-id="13053-113">証明書プロファイル機能を使用すると、既定の証明書を指定して、同じ証明書プロファイル内の証明書を検索する順序を設定できます。</span><span class="sxs-lookup"><span data-stu-id="13053-113">The certificate profiles functionality lets you specify a default certificate and set the order that certificates in the same certificate profile are searched in.</span></span> <span data-ttu-id="13053-114">この機能は、ローカル証明書および Key Vault 証明書についても同じような設定方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="13053-114">This functionality also provides a similar setup approach for local certificates and Key Vault certificates.</span></span> <span data-ttu-id="13053-115">証明書に対して会社固有の設定を追加できますが、各証明書の会社間の一意の識別子を Commerce チャネルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="13053-115">You can add company-specific settings for certificates, but the unique cross-company identifier for each certificate can be used in the Commerce channels.</span></span>

### <a name="scenarios"></a><span data-ttu-id="13053-116">シナリオ</span><span class="sxs-lookup"><span data-stu-id="13053-116">Scenarios</span></span>

<span data-ttu-id="13053-117">証明書プロファイル機能では、Commerce チャネルで次のシナリオをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="13053-117">The certificate profiles functionality supports the following scenarios in the Commerce channels:</span></span>

- <span data-ttu-id="13053-118">キー コンテナー予備シナリオでのローカル証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="13053-118">Use a local certificate in key vault fallback scenarios.</span></span> <span data-ttu-id="13053-119">予備シナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="13053-119">Here are some examples of these fallback scenarios:</span></span>

    - <span data-ttu-id="13053-120">キー コンテナー ストレージにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="13053-120">The key vault storage isn't accessible.</span></span>
    - <span data-ttu-id="13053-121">キー コンテナー ストレージに証明書が見つかりません。</span><span class="sxs-lookup"><span data-stu-id="13053-121">A certificate isn't found in the key vault storage.</span></span>
    - <span data-ttu-id="13053-122">POS はオフライン モードで実行されています。</span><span class="sxs-lookup"><span data-stu-id="13053-122">The POS is running in offline mode.</span></span>

- <span data-ttu-id="13053-123">ローカル証明書を使用しますが、キー コンテナーには保存しません (たとえば、オンプレミスのインストールで)。</span><span class="sxs-lookup"><span data-stu-id="13053-123">Use local certificates, but without storing them in the key vault (for example, in an on-premises installation).</span></span>
- <span data-ttu-id="13053-124">証明書の段階的な更新を実行すると、証明書の新しいバージョンは、新しいバージョンが既に利用可能な店舗またはターミナルでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="13053-124">Do a gradual update of certificates, where a new version of the certificate is used only in stores or on terminals where the new version is already available.</span></span>
- <span data-ttu-id="13053-125">複数の会社で同じ証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="13053-125">Use the same certificate in several companies.</span></span>

## <a name="set-up-certificate-profiles"></a><span data-ttu-id="13053-126">証明書プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="13053-126">Set up certificate profiles</span></span>

<span data-ttu-id="13053-127">次の手順では、証明書プロファイルの設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13053-127">The following procedure explains how to set up certificate profiles.</span></span> <span data-ttu-id="13053-128">Commerce チャネルで証明書プロファイルを使用する前に、次の手順に従って設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="13053-128">Before you use certificate profiles in the Commerce channels, follow these steps to configure the settings.</span></span>

1. <span data-ttu-id="13053-129">**機能管理**ワークスペースで、**小売店舗のユーザー定義の証明書プロファイル**機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="13053-129">In the **Feature management** workspace, turn on the **User-defined certificate profiles for retail stores** feature.</span></span>
2. <span data-ttu-id="13053-130">**システム管理 \> 設定 \> 証明書プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="13053-130">Go to **System administration \> Setup \> Certificate profiles**.</span></span>
3. <span data-ttu-id="13053-131">レコードを作成し、その**証明書プロファイル**、**名前**、および**説明**のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="13053-131">Create a record, and set the **Certificate profile**, **Name**, and **Description** fields for it.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13053-132">証明書プロファイルは、すべての会社および Commerce コンポーネント間の証明書の一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="13053-132">The certificate profile is a unique identifier of a certificate across all companies and Commerce components.</span></span>

3. <span data-ttu-id="13053-133">**法人**タブで、明細行を追加し、現在の証明書プロファイルを使用する必要がある法人 (会社) を選択します。</span><span class="sxs-lookup"><span data-stu-id="13053-133">On the **Legal entities** tab, add a line, and select the legal entity (company) that the current certificate profile should be used for.</span></span> <span data-ttu-id="13053-134">証明書プロファイルを複数の法人に対して使用する必要がある場合は、この手順を繰り返して、追加の法人ごとに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="13053-134">If the certificate profile should be used for multiple legal entities, repeat this step to add a line for each additional legal entity.</span></span>
4. <span data-ttu-id="13053-135">**設定**を選択して、**証明書プロファイル設定**のページを開くと、証明書プロファイルの会社固有の設定を入力できます。</span><span class="sxs-lookup"><span data-stu-id="13053-135">Select **Settings** to open the **Certificate profile settings** page, where you can enter company-specific settings for the certificate profile.</span></span>

### <a name="certificate-profile-settings"></a><span data-ttu-id="13053-136">証明書プロファイル設定</span><span class="sxs-lookup"><span data-stu-id="13053-136">Certificate profile settings</span></span>

<span data-ttu-id="13053-137">証明書プロファイル明細行の**設定**を選択すると、**証明書プロファイル設定**のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="13053-137">When you select **Settings** for certificate profile lines, the **Certificate profile settings** page appears.</span></span> <span data-ttu-id="13053-138">このページでは、現在の証明書プロファイルが Commerce チャネルで呼び出されたときに使用できる証明書を指定できます。</span><span class="sxs-lookup"><span data-stu-id="13053-138">This page lets you specify which certificates can be used when the current certificate profile is called in the Commerce channels.</span></span> <span data-ttu-id="13053-139">証明書を検索する順序を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="13053-139">You can also specify the order that certificates should be searched in.</span></span>

> [!NOTE]
> <span data-ttu-id="13053-140">**優先順位**フィールドは自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="13053-140">The **Priority** field is automatically set.</span></span> <span data-ttu-id="13053-141">値 **1** は、最も高い優先順位を表します。</span><span class="sxs-lookup"><span data-stu-id="13053-141">A value of **1** represents the highest priority.</span></span> <span data-ttu-id="13053-142">新しい明細行が、**証明書プロファイル設定**のページに追加されると、その優先順位は前の明細行の優先順位より 1 大きい番号に設定されます。</span><span class="sxs-lookup"><span data-stu-id="13053-142">When a new line is added on the **Certificate profile settings** page, its priority is set to a number that is one more than the priority of the previous line.</span></span> <span data-ttu-id="13053-143">特定の明細行の優先順位を変更するには、明細行を選択し、**上へ移動**を選択して優先順位を上げるか、**下に移動**を選択して優先順位を下げます。</span><span class="sxs-lookup"><span data-stu-id="13053-143">To change the priority of a specific line, select the line, and then select either **Move up** to increase the priority or **Move down** to decrease the priority.</span></span>

<span data-ttu-id="13053-144">**証明書プロファイル設定**のページに新しい明細行を追加するときは、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="13053-144">When you add a new line to the **Certificate profile settings** page, set the following fields:</span></span>

- <span data-ttu-id="13053-145">**場所タイプ** – 証明書を保存されている場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="13053-145">**Location type** – Select the location where the certificate is stored.</span></span> <span data-ttu-id="13053-146">このフィールドには次の 2 つの値があります: **ローカル証明書**と **Key Vault** です。</span><span class="sxs-lookup"><span data-stu-id="13053-146">This field has two possible values: **Local certificate** and **Key Vault**.</span></span>
- <span data-ttu-id="13053-147">**Key Vault 証明書** – **場所のタイプ** フィールドを **Key Vault** に設定する場合、このフィールドは必須です。</span><span class="sxs-lookup"><span data-stu-id="13053-147">**Key Vault certificate** – This field is required if you set the **Location type** field to **Key Vault**.</span></span> <span data-ttu-id="13053-148">これを使用して、Key Vault 証明書のシークレットを指定します。</span><span class="sxs-lookup"><span data-stu-id="13053-148">Use it to specify a Key Vault certificate secret.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13053-149">証明書プロファイルで Key Vault 証明書を使用する前に、必ずキー コンテナー ストレージに証明書をアップロードし、[Azure Key Vault クライアントの設定](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client) の指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="13053-149">Before you use a Key Vault certificate in certificate profiles, be sure to upload a certificate to the key vault storage, and follow the instructions in [Set up the Azure Key Vault client](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).</span></span>

- <span data-ttu-id="13053-150">**店舗名** – このフィールドはオプションであり、**場所タイプ** フィールドを**ローカル証明書**に設定した場合にのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="13053-150">**Store name** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="13053-151">これを使用して、ローカル証明書の検索に使用する既定の店舗名を指定します。</span><span class="sxs-lookup"><span data-stu-id="13053-151">Use it to specify a default store name that should be used to search local certificates.</span></span>
- <span data-ttu-id="13053-152">**店舗の場所** – このフィールドはオプションであり、**場所タイプ** フィールドを**ローカル証明書**に設定した場合にのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="13053-152">**Store location** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="13053-153">これを使用して、ローカル証明書の検索に使用する既定の店舗の場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="13053-153">Use it to specify a default store location that should be used to search local certificates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13053-154">Commerce Runtime でローカル証明書を検索するプロセスを簡略化するために、既定の店舗名および店舗の場所が追加されます。</span><span class="sxs-lookup"><span data-stu-id="13053-154">The default store name and store location are added to simplify the process of searching local certificates in the Commerce runtime.</span></span> <span data-ttu-id="13053-155">X509StoreProvider には、証明書が保存されるフォルダーの一覧があります。</span><span class="sxs-lookup"><span data-stu-id="13053-155">X509StoreProvider has a list of folders where certificates are stored.</span></span> <span data-ttu-id="13053-156">既定の店舗名および既定の店舗場所が指定されていない場合、X509StoreProvider はその一覧の他のフォルダーにある証明書を検索しようとします。</span><span class="sxs-lookup"><span data-stu-id="13053-156">If the default store name and the default store location aren't specified, X509StoreProvider tries to find a certificate in the other folders on its list.</span></span>

- <span data-ttu-id="13053-157">**サムプリント** – このフィールドは必須であり、**場所タイプ** フィールドを**ローカル証明書**に設定した場合にのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="13053-157">**Thumbprint** – This field is required and available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="13053-158">これを使用して、証明書のサムプリントを指定します。</span><span class="sxs-lookup"><span data-stu-id="13053-158">Use it to specify the certificate thumbprint.</span></span>
- <span data-ttu-id="13053-159">**コメント** – このフィールドはオプションであり、ユーザーはメモを入力できます。</span><span class="sxs-lookup"><span data-stu-id="13053-159">**Comments** – This field is optional and lets users enter notes.</span></span>

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a><span data-ttu-id="13053-160">ワークフロー: Commerce Runtime での証明書の検索</span><span class="sxs-lookup"><span data-stu-id="13053-160">Workflow: Searching certificates in the Commerce runtime</span></span>

<span data-ttu-id="13053-161">Commerce Runtime で、証明書プロファイルが呼び出されたときに証明書を検索するために使用される、基本的なワークフローを次に示します。</span><span class="sxs-lookup"><span data-stu-id="13053-161">Here is the basic workflow that is used to search for a certificate when a certificate profile is called in the Commerce runtime.</span></span>

1. <span data-ttu-id="13053-162">システムでは、証明書プロファイルに現在の法人に対する会社固有の設定があるかどうかが識別されます。</span><span class="sxs-lookup"><span data-stu-id="13053-162">The system identifies whether the certificate profile has company-specific settings for the current legal entity.</span></span>
1. <span data-ttu-id="13053-163">システムでは、**優先順位**フィールドが **1** に設定された明細行に対する**証明書プロファイル設定**のページの値を使用して証明書を検索しようとします。</span><span class="sxs-lookup"><span data-stu-id="13053-163">The system tries to find the certificate by using the values on the **Certificate profile settings** page for the line where the **Priority** field is set to **1**.</span></span>

    - <span data-ttu-id="13053-164">**場所のタイプ** フィールドが **Key Vault** に設定されている場合、**Key Vault 証明書のシークレット** フィールドの値は**キー コンテナー パラメーター**のページの証明書を検索するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="13053-164">If the **Location type** field is set to **Key Vault**, the value of the **Key Vault certificate secret** field is used to search for the certificate on the **Key vault parameters** page.</span></span> <span data-ttu-id="13053-165">次に、証明書がキー コンテナー ストレージで検索されます。</span><span class="sxs-lookup"><span data-stu-id="13053-165">The certificate is then searched for in the key vault storage.</span></span>
    - <span data-ttu-id="13053-166">**場所タイプ** フィールドが**ローカル証明書**に設定される場合、既定の店舗名および店舗の場所を使用して、これらのパラメータが指定されている場合、X509StoreProvider は最初に証明書を検索します。</span><span class="sxs-lookup"><span data-stu-id="13053-166">If the **Location type** field is set to **Local certificate**, X509StoreProvider first searches for the certificate by using the default store name and store location, if these parameters are specified.</span></span> <span data-ttu-id="13053-167">次に、そのフォルダーの一覧にある他のすべてのフォルダーを検索します。</span><span class="sxs-lookup"><span data-stu-id="13053-167">It then searches in all other folders on its list of folders.</span></span>

1. <span data-ttu-id="13053-168">証明書が見つからない場合は、**優先順位**フィールドが **2** などに設定されている明細行に対してプロセスが繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="13053-168">If the certificate isn't found, the process is repeated for the line where the **Priority** field is set to **2**, and so on.</span></span>

> [!NOTE]
> <span data-ttu-id="13053-169">証明書プロファイルに現在の法人の設定がない場合、または証明書検索が**証明書プロファイル設定**のページのすべての明細行で失敗した場合、証明書は見つかりません。</span><span class="sxs-lookup"><span data-stu-id="13053-169">If the certificate profile has no settings for the current legal entity, or if the certificate search is unsuccessful for all lines on the **Certificate profile settings** page, the certificate isn't found.</span></span>

#### <a name="caching-the-results-of-certificate-searches"></a><span data-ttu-id="13053-170">証明書検索の結果のキャッシュ</span><span class="sxs-lookup"><span data-stu-id="13053-170">Caching the results of certificate searches</span></span>

<span data-ttu-id="13053-171">証明書検索の結果がキャッシュされます。</span><span class="sxs-lookup"><span data-stu-id="13053-171">The results of certificate searches are cached.</span></span> <span data-ttu-id="13053-172">キャッシュの既定の有効期限は 1 時間です。</span><span class="sxs-lookup"><span data-stu-id="13053-172">The default expiration time for a cache is one hour.</span></span> <span data-ttu-id="13053-173">ただし、この時間はカスタマイズ可能で、最大 24 時間に設定できます。</span><span class="sxs-lookup"><span data-stu-id="13053-173">However, this time can be customized and can be set to a maximum value of 24 hours.</span></span>

### <a name="gradual-update"></a><span data-ttu-id="13053-174">段階的更新</span><span class="sxs-lookup"><span data-stu-id="13053-174">Gradual update</span></span>

<span data-ttu-id="13053-175">証明書の新しいバージョンが導入されても、すべての店舗で同時に更新できない場合は、証明書プロファイル機能により証明書を段階的に更新できます。</span><span class="sxs-lookup"><span data-stu-id="13053-175">If a new version of the certificate is introduced, but it can't be updated in all stores at the same time, the certificate profiles functionality enables the certificate to be updated gradually.</span></span>

1. <span data-ttu-id="13053-176">証明書プロファイルおよび更新する明細行を検索し、**設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="13053-176">Find a certificate profile and the line that should be updated, and then select **Settings**.</span></span>
1. <span data-ttu-id="13053-177">明細行を追加し、証明書の最新バージョンに関連する設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="13053-177">Add a line, and specify settings that are related to the latest version of the certificate.</span></span>
1. <span data-ttu-id="13053-178">新しい明細行の**優先順位**の値を増やします。</span><span class="sxs-lookup"><span data-stu-id="13053-178">Increase the **Priority** value of the new line.</span></span> <span data-ttu-id="13053-179">**上へ移動**ボタンを使用し、同じ証明書の以前のバージョンの明細行の上になるように明細行を移動します。</span><span class="sxs-lookup"><span data-stu-id="13053-179">Use the **Move up** button to move the line so that it's above the line for the previous version of the same certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="13053-180">Commerce Runtime では、証明書の新しいバージョンが最初に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="13053-180">In the Commerce runtime, the new version of the certificate will be called first.</span></span> <span data-ttu-id="13053-181">証明書がまだ特定の店舗または特定のターミナルで更新されていない場合は、以前のバージョンが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="13053-181">If the certificate hasn't yet been updated in a specific store or on a specific terminal, the previous version will be called.</span></span>

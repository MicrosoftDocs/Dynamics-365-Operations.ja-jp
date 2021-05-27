---
title: 電子請求サービスの管理を開始する
description: このトピックでは、電子請求を開始する方法について説明します。
author: gionoder
ms.date: 05/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f389e111006327fe8d82581d01140b4cff2e200d
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980978"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="798fd-103">電子請求サービスの管理を開始する</span><span class="sxs-lookup"><span data-stu-id="798fd-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="798fd-104">必要条件</span><span class="sxs-lookup"><span data-stu-id="798fd-104">Prerequisites</span></span>

<span data-ttu-id="798fd-105">このトピックの手順を完了する前に、以下の前提条件を満たす必要があります :</span><span class="sxs-lookup"><span data-stu-id="798fd-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="798fd-106">Microsoft Dynamics Lifecycle Services (LCS) アカウントにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="798fd-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="798fd-107">バージョン 10.0.17 以降の Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="798fd-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="798fd-108">さらに、これらのアプリケーションは、次のいずれかの Azure 地域にデプロイされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="798fd-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="798fd-109">米国</span><span class="sxs-lookup"><span data-stu-id="798fd-109">United States</span></span>
    - <span data-ttu-id="798fd-110">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="798fd-110">Europe</span></span>
    - <span data-ttu-id="798fd-111">英国</span><span class="sxs-lookup"><span data-stu-id="798fd-111">United Kingdom</span></span>
    - <span data-ttu-id="798fd-112">アジア</span><span class="sxs-lookup"><span data-stu-id="798fd-112">Asia</span></span>

- <span data-ttu-id="798fd-113">Dynamics 365 Regulatory Configuration Services (RCS) アカウントにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="798fd-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="798fd-114">機能管理で RCS アカウントのグローバル化機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="798fd-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="798fd-115">詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="798fd-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="798fd-116">Azure のストレージ アカウントと Key Vault リソースを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="798fd-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="798fd-117">詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="798fd-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="798fd-118">Lifecycle Services にマイクロサービス向けのアドインをインストールします</span><span class="sxs-lookup"><span data-stu-id="798fd-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="798fd-119">LCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="798fd-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="798fd-120">**プレビュー機能管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="798fd-121">**パブリック プレビュー機能** セクションで、**電子請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-121">In the **Public Preview Features** section, select **Electronic Invoicing**.</span></span>
4. <span data-ttu-id="798fd-122">**プレビュー機能の有効化** オプションが **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="798fd-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="798fd-123">LCS プロジェクト ダッシュボードで、LCS プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-123">On your LCS project dashboard, select a LCS project.</span></span>
6. <span data-ttu-id="798fd-124">LCS プロジェクトの LCS 環境ダッシュボードで、LCS 配置プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-124">In the LCS project, on the LCS environment dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="798fd-125">LCS 展開プロジェクトが実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="798fd-125">The LCS deployment project must be running.</span></span>
7. <span data-ttu-id="798fd-126">**Power Platform 統合** タブの **環境アドイン** フィールド グループで、**新しいアドインをインストールする** を選択します 。</span><span class="sxs-lookup"><span data-stu-id="798fd-126">On the **Power Platform Integration** tab, in the **Environment add-ins** field group, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="798fd-127">**電子請求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-127">Select **Electronic Invoicing**.</span></span>
9. <span data-ttu-id="798fd-128">**AAD アプリケーション ID** フィールドに、**091c98b0-a1c9-4b02-b62c-7753395ccabe** を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-128">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="798fd-129">この値は固定値です。</span><span class="sxs-lookup"><span data-stu-id="798fd-129">This is a fixed value.</span></span>
10. <span data-ttu-id="798fd-130">**AAD のテナント ID** フィールドに、Azure のサブスクリプション アカウントのテナント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-130">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="798fd-131">条件を確認して、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="798fd-131">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="798fd-132">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-132">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="798fd-133">電子請求と RCS 統合のパラメーターを設定する</span><span class="sxs-lookup"><span data-stu-id="798fd-133">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="798fd-134">RCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="798fd-134">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="798fd-135">**関連リンク** セクションの **電子申告** ワークスペースで、**電子申告パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-135">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="798fd-136">**電子請求書作成サービス** タブの **サービス エンドポイントURI** フィールドに、次の表に示すように、Azure の地域に対応するサービス エンドポイントを入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-136">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="798fd-137">Azure geography データ センター</span><span class="sxs-lookup"><span data-stu-id="798fd-137">Datacenter Azure geography</span></span> | <span data-ttu-id="798fd-138">サービス エンドポイント URI</span><span class="sxs-lookup"><span data-stu-id="798fd-138">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="798fd-139">米国</span><span class="sxs-lookup"><span data-stu-id="798fd-139">United States</span></span>              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="798fd-140">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="798fd-140">Europe</span></span>                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="798fd-141">英国</span><span class="sxs-lookup"><span data-stu-id="798fd-141">United Kingdom</span></span>             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="798fd-142">アジア</span><span class="sxs-lookup"><span data-stu-id="798fd-142">Asia</span></span>                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. <span data-ttu-id="798fd-143">**アプリケーション ID** フィールドが、**0cdb527f-a8d1-4bf8-9436-b352c68682b2** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="798fd-143">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="798fd-144">この値は固定値です。</span><span class="sxs-lookup"><span data-stu-id="798fd-144">This value is a fixed value.</span></span>
5. <span data-ttu-id="798fd-145">**LCS 環境** フィールドに、LCS 環境の ID を入力してください。</span><span class="sxs-lookup"><span data-stu-id="798fd-145">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="798fd-146">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="798fd-146">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="798fd-147">Key Vault 参照を作成する</span><span class="sxs-lookup"><span data-stu-id="798fd-147">Create Key Vault references</span></span>

1. <span data-ttu-id="798fd-148">RCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="798fd-148">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="798fd-149">**グローバリゼーション機能** ワークスペースの **環境t** セクションで、**電子請求** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-149">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="798fd-150">**環境の設定**  ページのアクション ウィンドウで、**サービス環境** を選択し、**Key Vault パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-150">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="798fd-151">**新規** を選択して、新しい Key Vault 参照を作成します。</span><span class="sxs-lookup"><span data-stu-id="798fd-151">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="798fd-152">**名前** フィールドに、key vault 参照の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-152">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="798fd-153">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-153">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="798fd-154">**Key Vault URI** フィールドで、Azure Key Vault からの Key Vault シークレットをペーストします。</span><span class="sxs-lookup"><span data-stu-id="798fd-154">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="798fd-155">詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="798fd-155">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="798fd-156">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-156">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="798fd-157">ストレージ アカウントのシークレットを作成する</span><span class="sxs-lookup"><span data-stu-id="798fd-157">Create Storage account secret</span></span>

1. <span data-ttu-id="798fd-158">**環境設定** ページの [アクション] ペインで、**サービス環境** > **Key Vault パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-158">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="798fd-159">**Key Vault 参照** を選択し、**証明書** セクションで **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-159">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="798fd-160">**名前** フィールドに、ストレージ アカウント シークレットの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-160">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="798fd-161">詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="798fd-161">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="798fd-162">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-162">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="798fd-163">**タイプ** フィールドで、**シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-163">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="798fd-164">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="798fd-164">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="798fd-165">デジタル証明書シークレットを作成する</span><span class="sxs-lookup"><span data-stu-id="798fd-165">Create a digital certificate secret</span></span>

1. <span data-ttu-id="798fd-166">**環境設定** ページの [アクション] ペインで、**サービス環境** を選択してから **Key Vault パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-166">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="798fd-167">**Key Vault 参照** を選択してから、**証明書** セクションで **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-167">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="798fd-168">**名前** フィールドに、デジタル証明書シークレットの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-168">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="798fd-169">詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="798fd-169">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="798fd-170">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-170">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="798fd-171">**タイプ** フィールドで、**証明書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-171">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="798fd-172">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="798fd-172">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="798fd-173">サービス環境の作成</span><span class="sxs-lookup"><span data-stu-id="798fd-173">Create a service environment</span></span>

1. <span data-ttu-id="798fd-174">RCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="798fd-174">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="798fd-175">**グローバリゼーション機能** ワークスペースの **環境t** セクションで、**電子請求** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-175">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="798fd-176">**環境の設定** ページのアクション ウィンドウで、**サービス環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-176">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="798fd-177">**新規** を選択して、新しいサービス環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="798fd-177">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="798fd-178">**名前** フィールドに、電子請求書環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-178">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="798fd-179">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-179">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="798fd-180">**ストレージ SAS トークンのシークレット** フィールドで、ストレージ アカウントへのアクセス認証に使用する必要のあるストレージ アカウント シークレットの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-180">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="798fd-181">**ユーザー** セクションで、**追加** を選択し、環境を通じて電子請求書を送信し、記憶域アカウントに接続できるユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="798fd-181">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="798fd-182">**ユーザーID** フィールドに、ユーザーのエイリアスを入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-182">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="798fd-183">**メール** フィールドに、ユーザーのメール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-183">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="798fd-184">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-184">Select **Save**.</span></span>
10. <span data-ttu-id="798fd-185">国や地域固有の請求書でデジタル署名を適用するにあたって一連の証明書が必要な場合は、アクション ウィンドウで **Key Vault パラメーター** を選択し、**証明書チェーン** を選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="798fd-185">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="798fd-186">**新規** を選択して、一連の証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="798fd-186">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="798fd-187">**名称** フィールドに、一連の証明書の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-187">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="798fd-188">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-188">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="798fd-189">**証明書** セクションで、**追加** を択してチェーンに証明書を追加します。</span><span class="sxs-lookup"><span data-stu-id="798fd-189">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="798fd-190">**上** ボタン、または **下** ボタンを使用して、証明書チェーンの位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="798fd-190">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="798fd-191">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="798fd-191">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="798fd-192">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="798fd-192">Close the page.</span></span>
11. <span data-ttu-id="798fd-193">**サービス環境** ページの、アクション ペインで、 **公開** を選択してクラウドに環境を公開します。</span><span class="sxs-lookup"><span data-stu-id="798fd-193">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="798fd-194">**状態** フィールドの値が **公開済** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="798fd-194">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="798fd-195">接続されたアプリケーションを作成する</span><span class="sxs-lookup"><span data-stu-id="798fd-195">Create a connected application</span></span>

1. <span data-ttu-id="798fd-196">**環境の設定** ページ のアクション ウィンドウで、**接続されたアプリケーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-196">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="798fd-197">**新規** を選択して、接続されたアプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="798fd-197">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="798fd-198">**名前** フィールドに、接続するアプリケーションの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-198">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="798fd-199">**アプリケーション** フィールドに、接続する Finance と Supply Chain Management 環境の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-199">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="798fd-200">**テナント** フィールドに、接続する Finance と Supply Chain Management 環境のテナントを入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-200">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="798fd-201">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-201">Select **Save**.</span></span>
6. <span data-ttu-id="798fd-202">アクション ウィンドウで、**接続の確認** を 選択して環境との接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="798fd-202">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="798fd-203">テスト後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="798fd-203">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="798fd-204">接続されたアプリケーションと環境の関連付け</span><span class="sxs-lookup"><span data-stu-id="798fd-204">Link connected applications to environments</span></span>

1. <span data-ttu-id="798fd-205">**環境の設定** ページで **新規** を選択し、接続されたアプリケーションを環境に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="798fd-205">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="798fd-206">**接続されたアプリケーション**  フィールドで、接続されたアプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-206">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="798fd-207">**サービス環境** フィールドで、サービスの環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-207">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="798fd-208">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="798fd-208">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="798fd-209">Finance または Supply Chain Management に電子請求統合を設定する</span><span class="sxs-lookup"><span data-stu-id="798fd-209">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="798fd-210">電子請求統合機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="798fd-210">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="798fd-211">Finance または Supply Chain Management インスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="798fd-211">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="798fd-212">**機能管理** ワークスペースで、**電子請求統合** 機能を検索します。</span><span class="sxs-lookup"><span data-stu-id="798fd-212">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="798fd-213">この機能がページに表示されない場合は、**更新を確認する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-213">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="798fd-214">機能を選択し、**直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="798fd-214">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="798fd-215">サービス エンドポイント URL を設定する</span><span class="sxs-lookup"><span data-stu-id="798fd-215">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="798fd-216">**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="798fd-216">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="798fd-217">**送信サービス** タブの **サービス エンドポイント URI** フィールドに、次の表に示すように、Azure の地域に対応するサービス エンドポイントを入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-217">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="798fd-218">Azure geography データ センター</span><span class="sxs-lookup"><span data-stu-id="798fd-218">Datacenter Azure geography</span></span> | <span data-ttu-id="798fd-219">サービス エンドポイント URI</span><span class="sxs-lookup"><span data-stu-id="798fd-219">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="798fd-220">米国</span><span class="sxs-lookup"><span data-stu-id="798fd-220">United States</span></span>              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="798fd-221">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="798fd-221">Europe</span></span>                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="798fd-222">英国</span><span class="sxs-lookup"><span data-stu-id="798fd-222">United Kingdom</span></span>             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="798fd-223">アジア</span><span class="sxs-lookup"><span data-stu-id="798fd-223">Asia</span></span>                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. <span data-ttu-id="798fd-224">**環境** フィールドで、 電子請求に公開されたサービス環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="798fd-224">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="798fd-225">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="798fd-225">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="798fd-226">フライト キーを有効にする</span><span class="sxs-lookup"><span data-stu-id="798fd-226">Enable Flighting keys</span></span>

<span data-ttu-id="798fd-227">Microsoft Dynamics 365 Finance または  Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.17 以前に対してフライト キーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="798fd-227">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="798fd-228">次の SQL コマンドを実行してください :</span><span class="sxs-lookup"><span data-stu-id="798fd-228">Execute the following SQL command:</span></span>

    <span data-ttu-id="798fd-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="798fd-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="798fd-230">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="798fd-230">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="798fd-231">すべての AOS に IISreset コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="798fd-231">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: 電子請求サービスの管理を開始する
description: このトピックでは、電子請求を開始する方法について説明します。
author: gionoder
ms.date: 05/24/2021
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
ms.openlocfilehash: 7c4d69edd4a8f7c7acc2ac1bc22c1ba6eaba25ae
ms.sourcegitcommit: 90a289962598394ad98209026013689322854b7b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/24/2021
ms.locfileid: "6092409"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="09623-103">電子請求サービスの管理を開始する</span><span class="sxs-lookup"><span data-stu-id="09623-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="09623-104">必要条件</span><span class="sxs-lookup"><span data-stu-id="09623-104">Prerequisites</span></span>

<span data-ttu-id="09623-105">このトピックの手順を完了する前に、以下の前提条件を満たす必要があります :</span><span class="sxs-lookup"><span data-stu-id="09623-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="09623-106">Microsoft Dynamics Lifecycle Services (LCS) アカウントにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="09623-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="09623-107">バージョン 10.0.17 以降の Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="09623-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="09623-108">さらに、これらのアプリケーションは、次のいずれかの Azure 地域にデプロイされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="09623-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="09623-109">米国</span><span class="sxs-lookup"><span data-stu-id="09623-109">United States</span></span>
    - <span data-ttu-id="09623-110">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="09623-110">Europe</span></span>
    - <span data-ttu-id="09623-111">英国</span><span class="sxs-lookup"><span data-stu-id="09623-111">United Kingdom</span></span>
    - <span data-ttu-id="09623-112">アジア</span><span class="sxs-lookup"><span data-stu-id="09623-112">Asia</span></span>

- <span data-ttu-id="09623-113">Dynamics 365 Regulatory Configuration Services (RCS) アカウントにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="09623-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="09623-114">機能管理で RCS アカウントのグローバル化機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="09623-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="09623-115">詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09623-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="09623-116">Azure のストレージ アカウントと Key Vault リソースを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09623-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="09623-117">詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09623-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="09623-118">Lifecycle Services にマイクロサービス向けのアドインをインストールします</span><span class="sxs-lookup"><span data-stu-id="09623-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="09623-119">LCS アカウントにサインインし、LCS プロジェクトのダッシュボードで、LCS プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-119">Sign in to your LCS account, and on the LCS project dashboard, select an LCS project.</span></span>
2. <span data-ttu-id="09623-120">LCS プロジェクトの LCS 環境ダッシュボードで、LCS のデプロイプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-120">In the project, on the environment dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="09623-121">選択するプロジェクトが実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="09623-121">The project you select must must be running.</span></span>
3. <span data-ttu-id="09623-122">**Power Platform 統合** タブの **環境アドイン** フィールド グループで、**新しいアドインをインストールする** を選択します 。</span><span class="sxs-lookup"><span data-stu-id="09623-122">On the **Power Platform Integration** tab, in the **Environment add-ins** field group, select **Install a new add-in**.</span></span>
4. <span data-ttu-id="09623-123">**電子請求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-123">Select **Electronic Invoicing**.</span></span>
5. <span data-ttu-id="09623-124">**AAD アプリケーション ID** フィールドに、**091c98b0-a1c9-4b02-b62c-7753395ccabe** を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-124">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="09623-125">この値は固定値です。</span><span class="sxs-lookup"><span data-stu-id="09623-125">This is a fixed value.</span></span>
6. <span data-ttu-id="09623-126">**AAD のテナント ID** フィールドに、Azure のサブスクリプション アカウントのテナント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-126">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
7. <span data-ttu-id="09623-127">条件を確認して、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="09623-127">Review the terms and conditions, and then select the check box.</span></span>
8. <span data-ttu-id="09623-128">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-128">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="09623-129">電子請求と RCS 統合のパラメーターを設定する</span><span class="sxs-lookup"><span data-stu-id="09623-129">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="09623-130">RCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="09623-130">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="09623-131">**関連リンク** セクションの **電子申告** ワークスペースで、**電子申告パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-131">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="09623-132">**電子請求書作成サービス** タブの **サービス エンドポイントURI** フィールドに、次の表に示すように、Azure の地域に対応するサービス エンドポイントを入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-132">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="09623-133">Azure geography データ センター</span><span class="sxs-lookup"><span data-stu-id="09623-133">Datacenter Azure geography</span></span> | <span data-ttu-id="09623-134">サービス エンドポイント URI</span><span class="sxs-lookup"><span data-stu-id="09623-134">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="09623-135">米国</span><span class="sxs-lookup"><span data-stu-id="09623-135">United States</span></span>              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="09623-136">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="09623-136">Europe</span></span>                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="09623-137">英国</span><span class="sxs-lookup"><span data-stu-id="09623-137">United Kingdom</span></span>             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="09623-138">アジア</span><span class="sxs-lookup"><span data-stu-id="09623-138">Asia</span></span>                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. <span data-ttu-id="09623-139">**アプリケーション ID** フィールドが、**0cdb527f-a8d1-4bf8-9436-b352c68682b2** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="09623-139">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="09623-140">この値は固定値です。</span><span class="sxs-lookup"><span data-stu-id="09623-140">This value is a fixed value.</span></span>
5. <span data-ttu-id="09623-141">**LCS 環境** フィールドに、LCS 環境の ID を入力してください。</span><span class="sxs-lookup"><span data-stu-id="09623-141">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="09623-142">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="09623-142">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="09623-143">Key Vault 参照を作成する</span><span class="sxs-lookup"><span data-stu-id="09623-143">Create Key Vault references</span></span>

1. <span data-ttu-id="09623-144">RCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="09623-144">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="09623-145">**グローバリゼーション機能** ワークスペースの **環境t** セクションで、**電子請求** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-145">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="09623-146">**環境の設定**  ページのアクション ウィンドウで、**サービス環境** を選択し、**Key Vault パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-146">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="09623-147">**新規** を選択して、新しい Key Vault 参照を作成します。</span><span class="sxs-lookup"><span data-stu-id="09623-147">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="09623-148">**名前** フィールドに、key vault 参照の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-148">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="09623-149">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-149">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="09623-150">**Key Vault URI** フィールドで、Azure Key Vault からの Key Vault シークレットをペーストします。</span><span class="sxs-lookup"><span data-stu-id="09623-150">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="09623-151">詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09623-151">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="09623-152">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-152">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="09623-153">ストレージ アカウントのシークレットを作成する</span><span class="sxs-lookup"><span data-stu-id="09623-153">Create Storage account secret</span></span>

1. <span data-ttu-id="09623-154">**環境設定** ページの [アクション] ペインで、**サービス環境** > **Key Vault パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-154">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="09623-155">**Key Vault 参照** を選択し、**証明書** セクションで **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-155">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="09623-156">**名前** フィールドに、ストレージ アカウント シークレットの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-156">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="09623-157">詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09623-157">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="09623-158">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-158">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="09623-159">**タイプ** フィールドで、**シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-159">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="09623-160">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="09623-160">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="09623-161">デジタル証明書シークレットを作成する</span><span class="sxs-lookup"><span data-stu-id="09623-161">Create a digital certificate secret</span></span>

1. <span data-ttu-id="09623-162">**環境設定** ページの [アクション] ペインで、**サービス環境** を選択してから **Key Vault パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-162">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="09623-163">**Key Vault 参照** を選択してから、**証明書** セクションで **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-163">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="09623-164">**名前** フィールドに、デジタル証明書シークレットの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-164">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="09623-165">詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09623-165">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="09623-166">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-166">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="09623-167">**タイプ** フィールドで、**証明書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-167">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="09623-168">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="09623-168">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="09623-169">サービス環境の作成</span><span class="sxs-lookup"><span data-stu-id="09623-169">Create a service environment</span></span>

1. <span data-ttu-id="09623-170">RCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="09623-170">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="09623-171">**グローバリゼーション機能** ワークスペースの **環境t** セクションで、**電子請求** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-171">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="09623-172">**環境の設定** ページのアクション ウィンドウで、**サービス環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-172">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="09623-173">**新規** を選択して、新しいサービス環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="09623-173">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="09623-174">**名前** フィールドに、電子請求書環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-174">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="09623-175">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-175">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="09623-176">**ストレージ SAS トークンのシークレット** フィールドで、ストレージ アカウントへのアクセス認証に使用する必要のあるストレージ アカウント シークレットの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-176">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="09623-177">**ユーザー** セクションで、**追加** を選択し、環境を通じて電子請求書を送信し、記憶域アカウントに接続できるユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="09623-177">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="09623-178">**ユーザーID** フィールドに、ユーザーのエイリアスを入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-178">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="09623-179">**メール** フィールドに、ユーザーのメール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-179">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="09623-180">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-180">Select **Save**.</span></span>
10. <span data-ttu-id="09623-181">国や地域固有の請求書でデジタル署名を適用するにあたって一連の証明書が必要な場合は、アクション ウィンドウで **Key Vault パラメーター** を選択し、**証明書チェーン** を選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="09623-181">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="09623-182">**新規** を選択して、一連の証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="09623-182">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="09623-183">**名称** フィールドに、一連の証明書の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-183">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="09623-184">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-184">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="09623-185">**証明書** セクションで、**追加** を択してチェーンに証明書を追加します。</span><span class="sxs-lookup"><span data-stu-id="09623-185">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="09623-186">**上** ボタン、または **下** ボタンを使用して、証明書チェーンの位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="09623-186">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="09623-187">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="09623-187">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="09623-188">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="09623-188">Close the page.</span></span>
11. <span data-ttu-id="09623-189">**サービス環境** ページの、アクション ペインで、 **公開** を選択してクラウドに環境を公開します。</span><span class="sxs-lookup"><span data-stu-id="09623-189">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="09623-190">**状態** フィールドの値が **公開済** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="09623-190">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="09623-191">接続されたアプリケーションを作成する</span><span class="sxs-lookup"><span data-stu-id="09623-191">Create a connected application</span></span>

1. <span data-ttu-id="09623-192">**環境の設定** ページ のアクション ウィンドウで、**接続されたアプリケーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-192">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="09623-193">**新規** を選択して、接続されたアプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="09623-193">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="09623-194">**名前** フィールドに、接続するアプリケーションの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-194">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="09623-195">**アプリケーション** フィールドに、接続する Finance と Supply Chain Management 環境の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-195">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="09623-196">**テナント** フィールドに、接続する Finance と Supply Chain Management 環境のテナントを入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-196">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="09623-197">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-197">Select **Save**.</span></span>
6. <span data-ttu-id="09623-198">アクション ウィンドウで、**接続の確認** を 選択して環境との接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="09623-198">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="09623-199">テスト後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="09623-199">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="09623-200">接続されたアプリケーションと環境の関連付け</span><span class="sxs-lookup"><span data-stu-id="09623-200">Link connected applications to environments</span></span>

1. <span data-ttu-id="09623-201">**環境の設定** ページで **新規** を選択し、接続されたアプリケーションを環境に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="09623-201">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="09623-202">**接続されたアプリケーション**  フィールドで、接続されたアプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-202">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="09623-203">**サービス環境** フィールドで、サービスの環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-203">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="09623-204">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="09623-204">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="09623-205">Finance または Supply Chain Management に電子請求統合を設定する</span><span class="sxs-lookup"><span data-stu-id="09623-205">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="09623-206">電子請求統合機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="09623-206">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="09623-207">Finance または Supply Chain Management インスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="09623-207">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="09623-208">**機能管理** ワークスペースで、**電子請求統合** 機能を検索します。</span><span class="sxs-lookup"><span data-stu-id="09623-208">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="09623-209">この機能がページに表示されない場合は、**更新を確認する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-209">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="09623-210">機能を選択し、**直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09623-210">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="09623-211">サービス エンドポイント URL を設定する</span><span class="sxs-lookup"><span data-stu-id="09623-211">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="09623-212">**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="09623-212">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="09623-213">**送信サービス** タブの **サービス エンドポイント URI** フィールドに、次の表に示すように、Azure の地域に対応するサービス エンドポイントを入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-213">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="09623-214">Azure geography データ センター</span><span class="sxs-lookup"><span data-stu-id="09623-214">Datacenter Azure geography</span></span> | <span data-ttu-id="09623-215">サービス エンドポイント URI</span><span class="sxs-lookup"><span data-stu-id="09623-215">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="09623-216">米国</span><span class="sxs-lookup"><span data-stu-id="09623-216">United States</span></span>              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="09623-217">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="09623-217">Europe</span></span>                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="09623-218">英国</span><span class="sxs-lookup"><span data-stu-id="09623-218">United Kingdom</span></span>             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="09623-219">アジア</span><span class="sxs-lookup"><span data-stu-id="09623-219">Asia</span></span>                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. <span data-ttu-id="09623-220">**環境** フィールドで、 電子請求に公開されたサービス環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="09623-220">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="09623-221">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="09623-221">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="09623-222">フライト キーを有効にする</span><span class="sxs-lookup"><span data-stu-id="09623-222">Enable Flighting keys</span></span>

<span data-ttu-id="09623-223">Microsoft Dynamics 365 Finance または  Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.17 以前に対してフライト キーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="09623-223">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="09623-224">次の SQL コマンドを実行してください :</span><span class="sxs-lookup"><span data-stu-id="09623-224">Execute the following SQL command:</span></span>

    <span data-ttu-id="09623-225">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="09623-225">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="09623-226">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="09623-226">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="09623-227">すべての AOS に IISreset コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="09623-227">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

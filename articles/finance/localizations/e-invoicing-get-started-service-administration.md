---
title: 電子請求書アドオンのサービス管理を使用する
description: このトピックでは、電子請求書アドオンの使用を開始する方法について解説します。
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592529"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="1deb2-103">電子請求書アドオンのサービス管理を使用する</span><span class="sxs-lookup"><span data-stu-id="1deb2-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="1deb2-104">必要条件</span><span class="sxs-lookup"><span data-stu-id="1deb2-104">Prerequisites</span></span>

<span data-ttu-id="1deb2-105">このトピックの手順を完了する前に、以下の前提条件を満たす必要があります :</span><span class="sxs-lookup"><span data-stu-id="1deb2-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="1deb2-106">Microsoft Dynamics Lifecycle Services (LCS) アカウントにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1deb2-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="1deb2-107">バージョン 10.0.17 以降の Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="1deb2-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1deb2-108">さらに、これらのアプリケーションは、次のいずれかの Azure 地域にデプロイされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1deb2-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="1deb2-109">米国東部</span><span class="sxs-lookup"><span data-stu-id="1deb2-109">East US</span></span>
    - <span data-ttu-id="1deb2-110">米国西部</span><span class="sxs-lookup"><span data-stu-id="1deb2-110">West US</span></span>
    - <span data-ttu-id="1deb2-111">北ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="1deb2-111">North EU</span></span>
    - <span data-ttu-id="1deb2-112">西ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="1deb2-112">West EU</span></span>

- <span data-ttu-id="1deb2-113">Dynamics 365 Regulatory Configuration Services (RCS) アカウントにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1deb2-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="1deb2-114">機能管理で RCS アカウントのグローバル化機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1deb2-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="1deb2-115">詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1deb2-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="1deb2-116">Azure のストレージ アカウントと Key Vault リソースを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1deb2-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="1deb2-117">詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1deb2-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="1deb2-118">Lifecycle Services のマイクロサービス用アドオンをインストールする</span><span class="sxs-lookup"><span data-stu-id="1deb2-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="1deb2-119">LCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="1deb2-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="1deb2-120">**プレビュー機能管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="1deb2-121">**パブリックプレビュー機能** セクションで、**電子請求書サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="1deb2-122">**プレビュー機能の有効化** オプションが **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="1deb2-123">LCS ダッシュボードで、LCS 配置プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="1deb2-124">LCS プロジェクトが実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1deb2-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="1deb2-125">**環境アドイン** タブで、**新しいアドインのインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="1deb2-126">**電子請求サービス** を選択し、**AAD アプリケーション ID** フィールドで、**091c98b0-a1c9-4b02-b62c-7753395ccabe** と入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="1deb2-127">この値は固定値です。</span><span class="sxs-lookup"><span data-stu-id="1deb2-127">This is a fixed value.</span></span>
10. <span data-ttu-id="1deb2-128">**AAD のテナント ID** フィールドに、Azure のサブスクリプション アカウントのテナント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="1deb2-129">条件を確認して、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="1deb2-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="1deb2-130">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="1deb2-131">電子請求書アドオンを使用した RCS 統合に使用するパラメーターを設定する</span><span class="sxs-lookup"><span data-stu-id="1deb2-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="1deb2-132">RCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="1deb2-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1deb2-133">**関連リンク** セクションの **電子申告** ワークスペースで、**電子申告パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="1deb2-134">**電子請求書作成サービス** タブの **サービス エンドポイントURI** フィールドに、次の表に示すように、Azure の地域に対応するサービス エンドポイントを入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="1deb2-135">Azure geography データ センター</span><span class="sxs-lookup"><span data-stu-id="1deb2-135">Datacenter Azure geography</span></span> | <span data-ttu-id="1deb2-136">サービス エンドポイント URI</span><span class="sxs-lookup"><span data-stu-id="1deb2-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1deb2-137">米国東部</span><span class="sxs-lookup"><span data-stu-id="1deb2-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1deb2-138">米国西部</span><span class="sxs-lookup"><span data-stu-id="1deb2-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1deb2-139">北ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="1deb2-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1deb2-140">西ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="1deb2-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="1deb2-141">**アプリケーション ID** フィールドが、**0cdb527f-a8d1-4bf8-9436-b352c68682b2** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="1deb2-142">この値は固定値です。</span><span class="sxs-lookup"><span data-stu-id="1deb2-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="1deb2-143">**LCS 環境 ID** フィールドに、LCS のサブスクリプション アカウントの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="1deb2-144">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="1deb2-145">Key Vault シークレットの作成</span><span class="sxs-lookup"><span data-stu-id="1deb2-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="1deb2-146">RCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="1deb2-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1deb2-147">**グローバリゼーション機能** ワークスペースの **環境** セクションで、**電子請求のアドオン** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="1deb2-148">**環境の設定**  ページのアクション ウィンドウで、**サービス環境** を選択し、**Key Vault パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="1deb2-149">**新規** を 選択すると、主要な key vault のシークレットを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="1deb2-150">**名前** フィールドに、Key Vault のシークレットを入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="1deb2-151">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="1deb2-152">**Key Vault URI** フィールドに、Azure Key Vault のからコピーしたシークレットを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="1deb2-153">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="1deb2-154">ストレージ アカウントのシークレットを作成する</span><span class="sxs-lookup"><span data-stu-id="1deb2-154">Create Storage account secret</span></span>

1. <span data-ttu-id="1deb2-155">**システム管理** > **設定** > **Key Vault パラメーター** に移動し、Key Vault シークレットを選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="1deb2-156">**証明書** セクションで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="1deb2-157">**名前** フィールドに、ストレージ アカウントのシークレットの名前を入力し、**説明** フィールドに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1deb2-158">**タイプ** フィールドで、**証明書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="1deb2-159">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="1deb2-160">デジタル証明書シークレットを作成する</span><span class="sxs-lookup"><span data-stu-id="1deb2-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="1deb2-161">**システム管理** > **設定** > **Key Vault パラメーター** に移動し、Key Vault シークレットを選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="1deb2-162">**証明書** セクションで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="1deb2-163">**名前** フィールドに、デジタル証明書シークレットの名前を入力し、**説明** フィールドに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1deb2-164">**タイプ** フィールドで、**証明書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="1deb2-165">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="1deb2-166">電子請求書アドオン環境を作成する</span><span class="sxs-lookup"><span data-stu-id="1deb2-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="1deb2-167">RCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="1deb2-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1deb2-168">**グローバリゼーション機能** ワークスペースの **環境** セクションで、**電子請求のアドオン** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="1deb2-169">サービス環境の作成</span><span class="sxs-lookup"><span data-stu-id="1deb2-169">Create a service environment</span></span>

1. <span data-ttu-id="1deb2-170">**環境の設定** ページのアクション ウィンドウで、**サービス環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="1deb2-171">**新規** を選択して、新しいサービス環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="1deb2-172">**名前** フィールドに、電子請求書環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="1deb2-173">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1deb2-174">**ストレージ SAS トークンのシークレット** フィールドで、ストレージ アカウントへのアクセス認証に使用する必要のあるストレージ アカウント シークレットの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="1deb2-175">**ユーザー** セクションで、**追加** を選択し、環境を通じて電子請求書を送信し、記憶域アカウントに接続できるユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="1deb2-176">**ユーザーID** フィールドに、ユーザーのエイリアスを入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="1deb2-177">**メール** フィールドに、ユーザーのメール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="1deb2-178">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-178">Select **Save**.</span></span>
8. <span data-ttu-id="1deb2-179">国や地域固有の請求書でデジタル署名を適用するにあたって一連の証明書が必要な場合は、アクション ウィンドウで **Key Vault パラメーター** を選択し、**証明書チェーン** を選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1deb2-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="1deb2-180">**新規** を選択して、一連の証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="1deb2-181">**名称** フィールドに、一連の証明書の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="1deb2-182">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="1deb2-183">**証明書** セクションで、**追加** を択してチェーンに証明書を追加します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="1deb2-184">**上** ボタン、または **下** ボタンを使用して、証明書チェーンの位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="1deb2-185">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="1deb2-186">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-186">Close the page.</span></span>
9. <span data-ttu-id="1deb2-187">**サービス環境** ページの、アクション ペインで、 **公開** を選択してクラウドに環境を公開します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="1deb2-188">**状態** フィールドの値が **公開済** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="1deb2-189">接続されたアプリケーションを作成する</span><span class="sxs-lookup"><span data-stu-id="1deb2-189">Create a connected application</span></span>

1. <span data-ttu-id="1deb2-190">**環境の設定** ページ のアクション ウィンドウで、**接続されたアプリケーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="1deb2-191">**新規** を選択して、接続されたアプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="1deb2-192">**名前** フィールドに、接続するアプリケーションの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="1deb2-193">**アプリケーション** フィールドに、接続する Finance と Supply Chain Management 環境の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="1deb2-194">**テナント** フィールドに、接続する Finance と Supply Chain Management 環境のテナントを入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="1deb2-195">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-195">Select **Save**.</span></span>
6. <span data-ttu-id="1deb2-196">アクション ウィンドウで、**接続の確認** を 選択して環境との接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="1deb2-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="1deb2-197">テスト後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="1deb2-198">接続されたアプリケーションと環境の関連付け</span><span class="sxs-lookup"><span data-stu-id="1deb2-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="1deb2-199">**環境の設定** ページで **新規** を選択し、接続されたアプリケーションを環境に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="1deb2-200">**接続されたアプリケーション**  フィールドで、接続されたアプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="1deb2-201">**サービス環境** フィールドで、サービスの環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="1deb2-202">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="1deb2-203">Finance および Supply Chain Management で電子請求書のアドオン統合を設定する</span><span class="sxs-lookup"><span data-stu-id="1deb2-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="1deb2-204">電子請求書アドオンの統合を有効化する</span><span class="sxs-lookup"><span data-stu-id="1deb2-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="1deb2-205">Finance または Supply Chain Management インスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="1deb2-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="1deb2-206">**機能の管理** ワークスペースで、 **電子請求書アドオンの統合** 機能を検索します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="1deb2-207">この機能がページに表示されない場合は、**更新を確認する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="1deb2-208">機能を選択し、**直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="1deb2-209">サービス エンドポイント URL を設定する</span><span class="sxs-lookup"><span data-stu-id="1deb2-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="1deb2-210">**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="1deb2-211">**送信サービス** タブの **サービス エンドポイント URI** フィールドに、次の表に示すように、Azure の地域に対応するサービス エンドポイントを入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="1deb2-212">Azure geography データ センター</span><span class="sxs-lookup"><span data-stu-id="1deb2-212">Datacenter Azure geography</span></span> | <span data-ttu-id="1deb2-213">サービス エンドポイント URL</span><span class="sxs-lookup"><span data-stu-id="1deb2-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1deb2-214">米国東部</span><span class="sxs-lookup"><span data-stu-id="1deb2-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1deb2-215">米国西部</span><span class="sxs-lookup"><span data-stu-id="1deb2-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1deb2-216">北ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="1deb2-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1deb2-217">西ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="1deb2-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="1deb2-218">**環境** フィールドに、電子請求書のアドオン環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="1deb2-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="1deb2-219">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1deb2-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

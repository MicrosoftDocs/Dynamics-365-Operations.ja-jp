---
title: IoT インテリジェンスの Azure resources を設定する
description: このトピックでは、IoT インテリジェンスに必要となる Microsoft Azure リソースの作成と構成方法について説明します。
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 722904aa75a9d95b99c83f39a1d79b9c796714b3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821108"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="f24db-103">IoT インテリジェンスの Azure resources を設定する</span><span class="sxs-lookup"><span data-stu-id="f24db-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f24db-104">このトピックでは、IoT インテリジェンスに必要となる Microsoft Azure リソースの作成と構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f24db-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="f24db-105">Azure リソースの作成</span><span class="sxs-lookup"><span data-stu-id="f24db-105">Create Azure resources</span></span>

<span data-ttu-id="f24db-106">次の手順に従って、Microsoft  Dynamics 365 Supply Chain Management からアクセスできる IoT hub、Redis キャッシュ、キーボルトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f24db-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="f24db-107">Microsoft Dynamics ERP Microservices ファースト パーティ アプリの ID がテナントに含まれていることを確認する</span><span class="sxs-lookup"><span data-stu-id="f24db-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="f24db-108">Microsoft Dynamics ERP Microservices のファースト パーティ アプリのアプリ ID がテナントに含まれていることを確認するには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="f24db-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="f24db-109"><https://portal.azure.com>で Azure ポータルにログインします。</span><span class="sxs-lookup"><span data-stu-id="f24db-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="f24db-110">**Azure Active Directory** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f24db-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="f24db-111">**エンタープライズ アプリケーション** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f24db-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="f24db-112">**アプリケーション タイプ** フィールドで、**Microsoft アプリケーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="f24db-113">検索フィールドで、**Microsoft Dynamics ERP Microservices** と入力します。</span><span class="sxs-lookup"><span data-stu-id="f24db-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="f24db-114">**Microsoft Dynamics ERP Microservices** が一覧に表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f24db-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="f24db-115">その他のアプリケーションにも同様の名前があります。</span><span class="sxs-lookup"><span data-stu-id="f24db-115">Other applications have similar names.</span></span> <span data-ttu-id="f24db-116">そのため、適切なアプリを見つけるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="f24db-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="f24db-117">アプリの ID は **0cdb527f-a8d1-4bf8-9436-b352c68682b2** です。</span><span class="sxs-lookup"><span data-stu-id="f24db-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="f24db-118">アプリケーションが一覧に含まれていない場合は、テナントに追加する必要があります:</span><span class="sxs-lookup"><span data-stu-id="f24db-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="f24db-119">Azure portal のツールバーで、ボタンを選択して Azure Cloud Shell を開きます。</span><span class="sxs-lookup"><span data-stu-id="f24db-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="f24db-120">コマンド **Install-Module AzureAD** を実行します。</span><span class="sxs-lookup"><span data-stu-id="f24db-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="f24db-121">モジュールをインストールするには、**Y** と入力します。</span><span class="sxs-lookup"><span data-stu-id="f24db-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="f24db-122">コマンド **Get-InstalledModule -Name "AzureAD"** を実行して、モジュールがインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f24db-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="f24db-123">コマンド **Connect-AzureAD -Confirm** を実行し、認証を行います。</span><span class="sxs-lookup"><span data-stu-id="f24db-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="f24db-124">**New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2** を実行します。</span><span class="sxs-lookup"><span data-stu-id="f24db-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="f24db-125">手順 1 ～ 6 を繰り返して、アプリの ID がご利用のテナントに含まれていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="f24db-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="f24db-126">Key Vault のリソースを作成する</span><span class="sxs-lookup"><span data-stu-id="f24db-126">Create a key vault resource</span></span>

<span data-ttu-id="f24db-127">Key Vault のリソースを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f24db-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="f24db-128">Azure ポータルで、リソース グループに移動する、またはリソース グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="f24db-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="f24db-129">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-129">Select **Add**.</span></span>
3. <span data-ttu-id="f24db-130">**新しい** ページの [検索] フィールドに、**キーボルト** を入力します。</span><span class="sxs-lookup"><span data-stu-id="f24db-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="f24db-131">次に **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-131">Then select **Create**.</span></span>
4. <span data-ttu-id="f24db-132">**Key Vault の作成** ページで、**Key Vault の名称** フィールドに名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f24db-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="f24db-133">既定の値を確認し、**確認 + 作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="f24db-134">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-134">Select **Create**.</span></span>

<span data-ttu-id="f24db-135">Key Vault がバックグラウンドで作成されます。</span><span class="sxs-lookup"><span data-stu-id="f24db-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="f24db-136">IoT ハブ リソースの作成</span><span class="sxs-lookup"><span data-stu-id="f24db-136">Create an IoT hub resource</span></span>

<span data-ttu-id="f24db-137">IoT ハブのリソース ファイルを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f24db-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="f24db-138">リソース グループに移動、またはリソース グループを作成する。</span><span class="sxs-lookup"><span data-stu-id="f24db-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="f24db-139">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-139">Select **Add**.</span></span>
3. <span data-ttu-id="f24db-140">**新規** ページの [検索] フィールドに、**Iot ハブ** を入力します。</span><span class="sxs-lookup"><span data-stu-id="f24db-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="f24db-141">次に **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-141">Then select **Create**.</span></span>
4. <span data-ttu-id="f24db-142">**IoT ハブの名称** フィールドに名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f24db-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="f24db-143">既定の値を確認し、**確認 + 作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="f24db-144">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-144">Select **Create**.</span></span>

<span data-ttu-id="f24db-145">IoT ハブ がバックグラウンドで作成されます。</span><span class="sxs-lookup"><span data-stu-id="f24db-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="f24db-146">環境ごとに 1 つの IoT ハブ リソースを作成することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="f24db-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="f24db-147">Redis キャッシュ リソースの作成</span><span class="sxs-lookup"><span data-stu-id="f24db-147">Create a Redis cache resource</span></span>

<span data-ttu-id="f24db-148">Redis キャッシュ のリソースを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f24db-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="f24db-149">リソース グループに移動、またはリソース グループを作成する。</span><span class="sxs-lookup"><span data-stu-id="f24db-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="f24db-150">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-150">Select **Add**.</span></span>
3. <span data-ttu-id="f24db-151">**新規** ページの [検索] フィールドに、**Azure Cache for Redis** を入力します。</span><span class="sxs-lookup"><span data-stu-id="f24db-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="f24db-152">次に **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-152">Then select **Create**.</span></span>
4. <span data-ttu-id="f24db-153">**DNS 名称** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f24db-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="f24db-154">既定の値を確認し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="f24db-155">Redis キャッシュがバックグラウンドで作成されます。</span><span class="sxs-lookup"><span data-stu-id="f24db-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="f24db-156">環境ごとに 1 つの Redis キャッシュを作成することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="f24db-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="f24db-157">以上で、すべてのリソースが作成されました。</span><span class="sxs-lookup"><span data-stu-id="f24db-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="f24db-158">Azure リソースの構成</span><span class="sxs-lookup"><span data-stu-id="f24db-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="f24db-159">IoT ハブの構成</span><span class="sxs-lookup"><span data-stu-id="f24db-159">Configure the IoT hub</span></span>

<span data-ttu-id="f24db-160">IoT ハブを構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f24db-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="f24db-161">ご利用のリソースで、IoT ハブのリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="f24db-162">左側のナビゲーション ウィンドウで、**組み込み型エンドポイント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="f24db-163">**コンシューマー グループ** で、次のコンシューマー グループを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f24db-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="f24db-164">これらのコンシューマー グループは、既成のシナリオに対応しています。</span><span class="sxs-lookup"><span data-stu-id="f24db-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="f24db-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="f24db-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="f24db-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="f24db-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="f24db-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="f24db-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="f24db-168">Key Vault の構成</span><span class="sxs-lookup"><span data-stu-id="f24db-168">Configure the key vault</span></span>

<span data-ttu-id="f24db-169">Key Vault を構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f24db-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="f24db-170">ご利用のリソースで、Key Vault のリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="f24db-171">左側のナビゲーション ウィンドウで、**アクセス ポリシー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="f24db-172">**アクセス ポリシーの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="f24db-173">**アクセス ポリシーの追加** ページの **シークレットの アクセス許可** フィールドで、**取得** と **一覧** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="f24db-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="f24db-174">**プリンシパルの選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f24db-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="f24db-175">**プリンシパル** ダイアログ ボックスで、**Microsoft Dynamics ERP Microservices** を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="f24db-176">**選択する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-176">Then select **Select**.</span></span>
7. <span data-ttu-id="f24db-177">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-177">Select **Add**.</span></span>
8. <span data-ttu-id="f24db-178">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-178">Select **Save**.</span></span>

<span data-ttu-id="f24db-179">以上で、アプリが Key Vault のシークレットにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="f24db-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="f24db-180">IoT ハブの接続文字列シークレットを保存します</span><span class="sxs-lookup"><span data-stu-id="f24db-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="f24db-181">IoT ハブの接続文字列のシークレットを保存するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f24db-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="f24db-182">ご利用のリソースで、IoT ハブのリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="f24db-183">左側のナビゲーション ウィンドウで、**組み込み型エンドポイント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="f24db-184">**イベントハブ互換エンドポイント** フィールドの値をコピー します。</span><span class="sxs-lookup"><span data-stu-id="f24db-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="f24db-185">Key Vault のリソースに移動します。</span><span class="sxs-lookup"><span data-stu-id="f24db-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="f24db-186">左側のナビゲーション ウィンドウで、**シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="f24db-187">**生成/インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="f24db-188">**名前** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f24db-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="f24db-189">**値** フィールドに、前述の手順でコピーした エンドポイントの値を貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f24db-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="f24db-190">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="f24db-191">Redis キャッシュの接続文字列のシークレットを保存する</span><span class="sxs-lookup"><span data-stu-id="f24db-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="f24db-192">Redis キャッシュの接続文字列のシークレットを保存するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f24db-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="f24db-193">ご利用のリソースで、Redis キャッシュのリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="f24db-194">**アクセス キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="f24db-195">**ライマリ接続文字列** フィールドの値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="f24db-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="f24db-196">Key Vault のリソースに移動します。</span><span class="sxs-lookup"><span data-stu-id="f24db-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="f24db-197">左側のナビゲーション ウィンドウで、**シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="f24db-198">**生成/インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="f24db-199">**名前** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f24db-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="f24db-200">**値** フィールドに、前述の手順でコピーした接続文字列を貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f24db-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="f24db-201">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f24db-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="f24db-202">いずれかの接続文字列を更新する場合は、常にこのシークレットの値も更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f24db-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="f24db-203">以上で、必要な Azure リソースのプロビジョニングが完了しました。</span><span class="sxs-lookup"><span data-stu-id="f24db-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="f24db-204">次の手順では、[Microsoft Dynamics Lifecycle Services (LCS) に、IoT インテリジェンスをインストール](iot-lcs-setup.md) します。</span><span class="sxs-lookup"><span data-stu-id="f24db-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
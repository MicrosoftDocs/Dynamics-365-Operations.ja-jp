---
title: 当事者およびグローバル アドレス帳モデルへのアップグレード
description: このトピックでは、二重書き込みデータを当事者およびグローバル アドレス帳モデルにアップグレードする方法について説明します。
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857373"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="71920-103">当事者およびグローバル アドレス帳モデルへのアップグレード</span><span class="sxs-lookup"><span data-stu-id="71920-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="71920-104">[Azure Data Factory テンプレート](https://aka.ms/dual-write-gab-adf)を使用すると、既存の **取引先企業**、**連絡先**、および **仕入先** テーブル データを当事者およびグローバル アドレス帳モデルに二重書き込みでアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="71920-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="71920-105">テンプレートでは、 Finance and Operations アプリおよび Customer Engagement アプリケーションの両方からのデータを調整します。</span><span class="sxs-lookup"><span data-stu-id="71920-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="71920-106">このプロセスの終了時に、**当事者** レコードの **当事者** および **連絡先** が作成され、Customer Engagement アプリケーションの **取引先企業**、**連絡先**、および **仕入先** レコードに関連付けされます。</span><span class="sxs-lookup"><span data-stu-id="71920-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="71920-107">.csv ファイル (`FONewParty.csv`) が生成され、Finance and Operations アプリ内に新しい **当事者** レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="71920-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="71920-108">このトピックでは、Data Factory テンプレートを使用し、データをアップグレードする手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="71920-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="71920-109">カスタマイズを実行しない場合は、テンプレートを現状のままで使用できます。</span><span class="sxs-lookup"><span data-stu-id="71920-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="71920-110">**取引先企業**、**連絡先**、および **仕入先** をカスタマイズする場合は、次の手順に従ってテンプレートを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71920-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="71920-111">テンプレートは、**当事者** データのみをアップグレードするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="71920-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="71920-112">将来のリリースでは、郵便番号および電子住所が含まれる予定です。</span><span class="sxs-lookup"><span data-stu-id="71920-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="71920-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="71920-113">Prerequisites</span></span>

<span data-ttu-id="71920-114">これらの必要条件は必須です:</span><span class="sxs-lookup"><span data-stu-id="71920-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="71920-115">Azure サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="71920-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="71920-116">テンプレートへのアクセス</span><span class="sxs-lookup"><span data-stu-id="71920-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="71920-117">ユーザーは既存の二重書き込み顧客です。</span><span class="sxs-lookup"><span data-stu-id="71920-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="71920-118">アップグレードの準備</span><span class="sxs-lookup"><span data-stu-id="71920-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="71920-119">**完全同期**: 両方の環境は、**取引先企業 (顧客)**、**連絡先**、および **仕入先** に対して完全に同期された状態です。</span><span class="sxs-lookup"><span data-stu-id="71920-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="71920-120">**統合キー**: Customer Engagement アプリの **取引先企業 (顧客)**、**連絡先**、および **仕入先** テーブルは、すぐに出荷される統合キーを使用しています。</span><span class="sxs-lookup"><span data-stu-id="71920-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="71920-121">統合キーをカスタマイズした場合は、テンプレートをカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="71920-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="71920-122">**当事者番号**: すべてのアップグレードされる **取引先企業 (顧客)**、**連絡先**、および **仕入先** レコードには **当事者** 番号があります。</span><span class="sxs-lookup"><span data-stu-id="71920-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="71920-123">**当事者** 番号のないレコードは無視されます。</span><span class="sxs-lookup"><span data-stu-id="71920-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="71920-124">これらのレコードをアップグレードする場合は、アップグレード プロセスを開始する前にレコードに **当事者** 番号を追加します。</span><span class="sxs-lookup"><span data-stu-id="71920-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="71920-125">**システム停止**: アップグレード プロセス中は、Finance and Operations および Customer Engagement 環境の両方をオフラインにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="71920-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="71920-126">**スナップショット**: Finance and Operations および Customer Engagement アプリ両方のスナップショットを作成します。</span><span class="sxs-lookup"><span data-stu-id="71920-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="71920-127">必要に応じて、スナップショットを使用して以前の状態を復元します。</span><span class="sxs-lookup"><span data-stu-id="71920-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="71920-128">配置</span><span class="sxs-lookup"><span data-stu-id="71920-128">Deployment</span></span>

1. <span data-ttu-id="71920-129">テンプレートを [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="71920-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="71920-130">[Microsoft Azure](https://portal.azure.com/) にログインします。</span><span class="sxs-lookup"><span data-stu-id="71920-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="71920-131">[リソース グループ](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal)を作成します。</span><span class="sxs-lookup"><span data-stu-id="71920-131">Create a [resource group](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="71920-132">作成したリソース グループに[ストレージ アカウント](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal)を作成します。</span><span class="sxs-lookup"><span data-stu-id="71920-132">Create a [storage account](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="71920-133">作成した上記のリソース グループに[データ ファクトリー](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal)を作成します。</span><span class="sxs-lookup"><span data-stu-id="71920-133">Create a [data factory](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="71920-134">データ ファクトリーを開き、**作成者 & モニター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="71920-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="71920-135">**管理** タブで、**ARM テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71920-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="71920-136">**ARM テンプレートをインポートする** を選択して、**当事者** テンプレートをインポートします。</span><span class="sxs-lookup"><span data-stu-id="71920-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="71920-137">テンプレートをデータ ファクトリーにインポートします。</span><span class="sxs-lookup"><span data-stu-id="71920-137">Import the template into the data factory.</span></span> <span data-ttu-id="71920-138">**プロジェクトの詳細** および **インスタンスの詳細** に対して次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="71920-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="71920-139">フィールド</span><span class="sxs-lookup"><span data-stu-id="71920-139">Field</span></span> | <span data-ttu-id="71920-140">先頭値</span><span class="sxs-lookup"><span data-stu-id="71920-140">Value</span></span>
    ---|---
    <span data-ttu-id="71920-141">サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="71920-141">Subscription</span></span> | <span data-ttu-id="71920-142">Azure サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="71920-142">Azure subscription</span></span>
    <span data-ttu-id="71920-143">リソース グループ</span><span class="sxs-lookup"><span data-stu-id="71920-143">Resource group</span></span> | <span data-ttu-id="71920-144">ストレージ アカウントを作成されるのと同じリソースを提供します。</span><span class="sxs-lookup"><span data-stu-id="71920-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="71920-145">リージョン</span><span class="sxs-lookup"><span data-stu-id="71920-145">Region</span></span> | <span data-ttu-id="71920-146">リージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="71920-146">Specify region.</span></span>
    <span data-ttu-id="71920-147">ファクトリー名</span><span class="sxs-lookup"><span data-stu-id="71920-147">Factory Name</span></span> | <span data-ttu-id="71920-148">ファクトリー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="71920-148">Specify factory name.</span></span>
    <span data-ttu-id="71920-149">FO リンクされた Service_service プリンシパル キー</span><span class="sxs-lookup"><span data-stu-id="71920-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="71920-150">アプリケーション キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="71920-150">Specify the application's key.</span></span>
    <span data-ttu-id="71920-151">Azure Blob Storage_connection 文字列</span><span class="sxs-lookup"><span data-stu-id="71920-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="71920-152">Azure Blob Storage の接続文字列。</span><span class="sxs-lookup"><span data-stu-id="71920-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="71920-153">Dynamics CRM リンクされた Service_password</span><span class="sxs-lookup"><span data-stu-id="71920-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="71920-154">ユーザー名として指定したユーザー アカウントのパスワード。</span><span class="sxs-lookup"><span data-stu-id="71920-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="71920-155">FO リンクされた Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="71920-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="71920-156">FO リンクされた Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="71920-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="71920-157">アプリケーションが存在するテナント情報 (ドメイン名またはテナント ID) を指定します。</span><span class="sxs-lookup"><span data-stu-id="71920-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="71920-158">FO リンクされた Service_properties_type Properties_aad リソース ID</span><span class="sxs-lookup"><span data-stu-id="71920-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="71920-159">FO リンクされた Service_properties_type Properties_service プリンシパル ID</span><span class="sxs-lookup"><span data-stu-id="71920-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="71920-160">アプリケーションのクライアント ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="71920-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="71920-161">Dynamics CRM リンクされた Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="71920-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="71920-162">Dynamics に接続するユーザー名。</span><span class="sxs-lookup"><span data-stu-id="71920-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="71920-163">詳細については、[各環境の Resource Manager テンプレートの手動促進](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)、[リンクされたサービス プロパティ](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties)、および [Azure Data Factory を使用するデータ ファクトリ](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)参照してください</span><span class="sxs-lookup"><span data-stu-id="71920-163">For more information, see [Manually promote a Resource Manager template for each environment](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="71920-164">配置後に、データ ファクトリのデータセット、データ フロー、およびリンクされたサービスを検証します。</span><span class="sxs-lookup"><span data-stu-id="71920-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![データセット、データ フロー、およびリンクされたサービス](media/data-factory-validate.png)

11. <span data-ttu-id="71920-166">**管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="71920-166">Navigate to **Manage**.</span></span> <span data-ttu-id="71920-167">**接続** で、**リンクされたサービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71920-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="71920-168">**DynamicsCrmLinkedService** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71920-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="71920-169">**リンクされたサービスの編集 (Dynamics CRM)** フォームに、次の値を入力します:</span><span class="sxs-lookup"><span data-stu-id="71920-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="71920-170">フィールド</span><span class="sxs-lookup"><span data-stu-id="71920-170">Field</span></span> | <span data-ttu-id="71920-171">先頭値</span><span class="sxs-lookup"><span data-stu-id="71920-171">Value</span></span>
    ---|---
    <span data-ttu-id="71920-172">氏名</span><span class="sxs-lookup"><span data-stu-id="71920-172">Name</span></span> | <span data-ttu-id="71920-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="71920-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="71920-174">説明</span><span class="sxs-lookup"><span data-stu-id="71920-174">Description</span></span> | <span data-ttu-id="71920-175">エンティティ データをフェッチする CRM インスタンスに接続するリンクされたサービス</span><span class="sxs-lookup"><span data-stu-id="71920-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="71920-176">統合ランタイム経由の接続</span><span class="sxs-lookup"><span data-stu-id="71920-176">Connect via integration runtime</span></span> | <span data-ttu-id="71920-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="71920-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="71920-178">配置のタイプ</span><span class="sxs-lookup"><span data-stu-id="71920-178">Deployment type</span></span> | <span data-ttu-id="71920-179">オンライン</span><span class="sxs-lookup"><span data-stu-id="71920-179">Online</span></span>
    <span data-ttu-id="71920-180">サービス URI</span><span class="sxs-lookup"><span data-stu-id="71920-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="71920-181">認証タイプ</span><span class="sxs-lookup"><span data-stu-id="71920-181">Authentication type</span></span> | <span data-ttu-id="71920-182">Office365</span><span class="sxs-lookup"><span data-stu-id="71920-182">Office365</span></span>
    <span data-ttu-id="71920-183">ユーザー名</span><span class="sxs-lookup"><span data-stu-id="71920-183">User name</span></span> |
    <span data-ttu-id="71920-184">パスワードまたは Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="71920-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="71920-185">パスワード</span><span class="sxs-lookup"><span data-stu-id="71920-185">Password</span></span>
    <span data-ttu-id="71920-186">パスワード</span><span class="sxs-lookup"><span data-stu-id="71920-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="71920-187">テンプレートの実行</span><span class="sxs-lookup"><span data-stu-id="71920-187">Run the template</span></span>

1. <span data-ttu-id="71920-188">Finance and Operations アプリを使用して、次の **取引先企業**、**連絡先**、および **仕入先** の二重書き込みを停止します。</span><span class="sxs-lookup"><span data-stu-id="71920-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="71920-189">顧客 V3 (アカウント)</span><span class="sxs-lookup"><span data-stu-id="71920-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="71920-190">顧客 V3 (連絡先)</span><span class="sxs-lookup"><span data-stu-id="71920-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="71920-191">CDS 連絡先 V2 (連絡先)</span><span class="sxs-lookup"><span data-stu-id="71920-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="71920-192">CDS 連絡先 V2 (連絡先)</span><span class="sxs-lookup"><span data-stu-id="71920-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="71920-193">仕入先 V2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="71920-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="71920-194">Dataverse で `msdy_dualwriteruntimeconfig` テーブルからマップが削除されたのを確認します。</span><span class="sxs-lookup"><span data-stu-id="71920-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="71920-195">AppSource から [二重書き込み当事者およびグローバル アドレス帳ソリューション](https://aka.ms/dual-write-gab)をインストールします 。</span><span class="sxs-lookup"><span data-stu-id="71920-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="71920-196">Finance and Operations アプリで、次の表にデータが含まれている場合は、そのテーブルの **初期同期** を実行します。</span><span class="sxs-lookup"><span data-stu-id="71920-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="71920-197">あいさつ文</span><span class="sxs-lookup"><span data-stu-id="71920-197">Salutations</span></span>
    + <span data-ttu-id="71920-198">個人の特徴タイプ</span><span class="sxs-lookup"><span data-stu-id="71920-198">Personal character types</span></span>
    + <span data-ttu-id="71920-199">結句</span><span class="sxs-lookup"><span data-stu-id="71920-199">Complimentary closing</span></span>
    + <span data-ttu-id="71920-200">連絡担当者の肩書き</span><span class="sxs-lookup"><span data-stu-id="71920-200">Contact person titles</span></span>
    + <span data-ttu-id="71920-201">意思決定ロール</span><span class="sxs-lookup"><span data-stu-id="71920-201">Decision making roles</span></span>
    + <span data-ttu-id="71920-202">ロイヤルティ レベル</span><span class="sxs-lookup"><span data-stu-id="71920-202">Loyalty levels</span></span>

5. <span data-ttu-id="71920-203">Customer Engagement アプリで、次のプラグイン ステップを無効にします。</span><span class="sxs-lookup"><span data-stu-id="71920-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="71920-204">取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="71920-204">Account Update</span></span>
         + <span data-ttu-id="71920-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: 取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="71920-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="71920-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: 取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="71920-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="71920-207">連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-207">Contact Update</span></span>
         + <span data-ttu-id="71920-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: 連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="71920-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: 連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="71920-210">msdyn_party の更新</span><span class="sxs-lookup"><span data-stu-id="71920-210">msdyn_party Update</span></span>
         + <span data-ttu-id="71920-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party の更新</span><span class="sxs-lookup"><span data-stu-id="71920-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="71920-212">msdyn_vendor の更新</span><span class="sxs-lookup"><span data-stu-id="71920-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="71920-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor の更新</span><span class="sxs-lookup"><span data-stu-id="71920-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="71920-214">Customer Engagement アプリで、次のワークフローを無効にします:</span><span class="sxs-lookup"><span data-stu-id="71920-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="71920-215">取引先企業テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="71920-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="71920-216">取引先企業テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="71920-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="71920-217">連絡先テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="71920-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="71920-218">仕入先テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="71920-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="71920-219">取引先企業テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="71920-220">仕入先テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="71920-221">取引先担当者テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="71920-222">仕入先テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="71920-223">データ ファクトリーで、次の図に示すように **今すぐトリガーする** を選択してテンプレートを実行します。</span><span class="sxs-lookup"><span data-stu-id="71920-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="71920-224">このプロセスは、データ量に基づいて完了に数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="71920-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![トリガーの実行](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="71920-226">**取引先企業**、**連絡先**、および **仕入先** をカスタマイズする場合は、テンプレートを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71920-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="71920-227">Finance and Operations アプリで新しい **当事者** レコードをインポートします。</span><span class="sxs-lookup"><span data-stu-id="71920-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="71920-228">Azure Blob Storage から `FONewParty.csv` ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="71920-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="71920-229">パスは `partybootstrapping/output/FONewParty.csv` です。</span><span class="sxs-lookup"><span data-stu-id="71920-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="71920-230">`FONewParty.csv` ファイルを Excel ファイルに変換し、Excel ファイルを Finance and Operations アプリにインポートします。</span><span class="sxs-lookup"><span data-stu-id="71920-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="71920-231">csv インポートがふさわしい場合は、csv ファイルを直接インポートできます。</span><span class="sxs-lookup"><span data-stu-id="71920-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="71920-232">データ量によっては、インポートの実行に数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="71920-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="71920-233">詳細については、[データのインポート ジョブとエクスポート ジョブの概要](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71920-233">For more information, see [Data import and export jobs overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span></span>

    ![Datavers 当事者レコードのインポート](media/data-factory-import-party.png)

9. <span data-ttu-id="71920-235">Customer Engagement アプリで、次のプラグイン ステップを有効にします:</span><span class="sxs-lookup"><span data-stu-id="71920-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="71920-236">取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="71920-236">Account Update</span></span>
         + <span data-ttu-id="71920-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: 取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="71920-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="71920-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: 取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="71920-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="71920-239">連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-239">Contact Update</span></span>
         + <span data-ttu-id="71920-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: 連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="71920-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: 連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="71920-242">msdyn_party の更新</span><span class="sxs-lookup"><span data-stu-id="71920-242">msdyn_party Update</span></span>
         + <span data-ttu-id="71920-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party の更新</span><span class="sxs-lookup"><span data-stu-id="71920-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="71920-244">msdyn_vendor の更新</span><span class="sxs-lookup"><span data-stu-id="71920-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="71920-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor の更新</span><span class="sxs-lookup"><span data-stu-id="71920-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="71920-246">Customer Engagement アプリで、前の手順で次のワークフローを無効化した場合は、有効にします:</span><span class="sxs-lookup"><span data-stu-id="71920-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="71920-247">取引先企業テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="71920-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="71920-248">取引先企業テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="71920-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="71920-249">連絡先テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="71920-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="71920-250">仕入先テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="71920-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="71920-251">取引先企業テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="71920-252">仕入先テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="71920-253">取引先担当者テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="71920-254">仕入先テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="71920-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="71920-255">[当事者およびグローバル アドレス帳](party-gab.md)の指示に従って **当事者** 関連のマップを実行します。</span><span class="sxs-lookup"><span data-stu-id="71920-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="71920-256">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="71920-256">Troubleshooting</span></span>

1. <span data-ttu-id="71920-257">プロセスが失敗すると、失敗した活動からデータ ファクトリを再実行します。</span><span class="sxs-lookup"><span data-stu-id="71920-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="71920-258">一部のファイルは、データ検証の目的で使用できるデータ ファクトリによって生成されます。</span><span class="sxs-lookup"><span data-stu-id="71920-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="71920-259">データ ファクトリは、コンマ区切りされた csv ファイルに基づいて実行されます。</span><span class="sxs-lookup"><span data-stu-id="71920-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="71920-260">コンマを含むフィールド値がある場合は、結果に影響が出る場合があります。</span><span class="sxs-lookup"><span data-stu-id="71920-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="71920-261">コンマを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71920-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="71920-262">**監視** タブでは、すべてのステップおよび処理済みデータに関する情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="71920-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="71920-263">特定の手順を選択してデバッグします。</span><span class="sxs-lookup"><span data-stu-id="71920-263">Select a specific step to debug it.</span></span>

    ![監視タブ](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="71920-265">テンプレートの詳細を確認する</span><span class="sxs-lookup"><span data-stu-id="71920-265">Learn more about the template</span></span>

<span data-ttu-id="71920-266">テンプレート [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) ファイルに対するコメントを検索できます。</span><span class="sxs-lookup"><span data-stu-id="71920-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>

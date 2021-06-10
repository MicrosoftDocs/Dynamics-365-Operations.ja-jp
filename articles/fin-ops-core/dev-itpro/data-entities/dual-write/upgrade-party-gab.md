---
title: 当事者およびグローバル アドレス帳モデルへのアップグレード
description: このトピックでは、二重書き込みデータを当事者およびグローバル アドレス帳モデルにアップグレードする方法について説明します。
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112676"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="a77ef-103">当事者およびグローバル アドレス帳モデルへのアップグレード</span><span class="sxs-lookup"><span data-stu-id="a77ef-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a77ef-104">[Microsoft Azure Data Factory テンプレート](https://aka.ms/dual-write-gab-adf) を使用すると、既存の **取引先企業**、**連絡先**、および **仕入先** テーブル データを当事者およびグローバル アドレス帳モデルに二重書き込みでアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="a77ef-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="a77ef-105">テンプレートでは、Finance and Operations アプリおよび Customer Engagement アプリケーションの両方からのデータを調整します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="a77ef-106">このプロセスの終了時に、**当事者** レコードの **当事者** および **連絡先** が作成され、Customer Engagement アプリケーションの **取引先企業**、**連絡先**、および **仕入先** レコードに関連付けされます。</span><span class="sxs-lookup"><span data-stu-id="a77ef-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="a77ef-107">.csv ファイル (`FONewParty.csv`) が生成され、Finance and Operations アプリ内に新しい **当事者** レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a77ef-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="a77ef-108">このトピックでは、Data Factory テンプレートを使用し、データをアップグレードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="a77ef-109">カスタマイズを実行しない場合は、テンプレートを現状のままで使用できます。</span><span class="sxs-lookup"><span data-stu-id="a77ef-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="a77ef-110">**取引先企業**、**連絡先**、および **仕入先** をカスタマイズする場合は、次の手順に従ってテンプレートを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a77ef-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="a77ef-111">テンプレートは、**当事者** データのみをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="a77ef-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="a77ef-112">将来のリリースでは、郵便番号および電子住所が含まれる予定です。</span><span class="sxs-lookup"><span data-stu-id="a77ef-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a77ef-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="a77ef-113">Prerequisites</span></span>

<span data-ttu-id="a77ef-114">当事者およびグローバル アドレス帳モデルにアップグレードするには、次の前提条件を満たしている必要があります:</span><span class="sxs-lookup"><span data-stu-id="a77ef-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="a77ef-115">Azure サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="a77ef-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="a77ef-116">テンプレートへのアクセス</span><span class="sxs-lookup"><span data-stu-id="a77ef-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="a77ef-117">既存の二重書き込み顧客である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a77ef-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="a77ef-118">アップグレードの準備</span><span class="sxs-lookup"><span data-stu-id="a77ef-118">Prepare for the upgrade</span></span>
<span data-ttu-id="a77ef-119">アップグレードの準備には、次の活動が必要です:</span><span class="sxs-lookup"><span data-stu-id="a77ef-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="a77ef-120">**完全同期**: 両方の環境は、**取引先企業 (顧客)**、**連絡先**、および **仕入先** に対して完全に同期された状態です。</span><span class="sxs-lookup"><span data-stu-id="a77ef-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="a77ef-121">**統合キー**: Customer Engagement アプリの **取引先企業 (顧客)**、**連絡先**、および **仕入先** テーブルは、すぐに出荷される統合キーを使用しています。</span><span class="sxs-lookup"><span data-stu-id="a77ef-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="a77ef-122">統合キーをカスタマイズした場合は、テンプレートをカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a77ef-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="a77ef-123">**当事者番号**: すべてのアップグレードされる **取引先企業 (顧客)**、**連絡先**、および **仕入先** レコードには **当事者** 番号があります。</span><span class="sxs-lookup"><span data-stu-id="a77ef-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="a77ef-124">**当事者** 番号のないレコードは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a77ef-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="a77ef-125">これらのレコードをアップグレードする場合は、アップグレード プロセスを開始する前にレコードに **当事者** 番号を追加します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="a77ef-126">**システム停止**: アップグレード プロセス中は、Finance and Operations および Customer Engagement 環境の両方をオフラインにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a77ef-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="a77ef-127">**スナップショット**: Finance and Operations および Customer Engagement アプリ両方のスナップショットを作成します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="a77ef-128">必要に応じて、スナップショットを使用して以前の状態を復元します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="a77ef-129">配置</span><span class="sxs-lookup"><span data-stu-id="a77ef-129">Deployment</span></span>

1. <span data-ttu-id="a77ef-130">テンプレートを [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a77ef-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="a77ef-131">[Microsoft Azure](https://portal.azure.com/) にログインします。</span><span class="sxs-lookup"><span data-stu-id="a77ef-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="a77ef-132">[リソース グループ](/azure/azure-resource-manager/management/manage-resource-groups-portal)を作成します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="a77ef-133">作成したリソース グループに[ストレージ アカウント](/azure/storage/common/storage-account-create?tabs=azure-portal)を作成します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="a77ef-134">作成した上記のリソース グループに[データ ファクトリー](/azure/data-factory/quickstart-create-data-factory-portal)を作成します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="a77ef-135">データ ファクトリーを開き、**作成者 & モニター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="a77ef-136">**管理** タブで、**ARM テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="a77ef-137">**ARM テンプレートをインポートする** を選択して、**当事者** テンプレートをインポートします。</span><span class="sxs-lookup"><span data-stu-id="a77ef-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="a77ef-138">テンプレートをデータ ファクトリーにインポートします。</span><span class="sxs-lookup"><span data-stu-id="a77ef-138">Import the template into the data factory.</span></span> <span data-ttu-id="a77ef-139">**プロジェクトの詳細** および **インスタンスの詳細** に対して次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="a77ef-140">フィールド</span><span class="sxs-lookup"><span data-stu-id="a77ef-140">Field</span></span> | <span data-ttu-id="a77ef-141">先頭値</span><span class="sxs-lookup"><span data-stu-id="a77ef-141">Value</span></span>
    ---|---
    <span data-ttu-id="a77ef-142">サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="a77ef-142">Subscription</span></span> | <span data-ttu-id="a77ef-143">Azure サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="a77ef-143">Azure subscription</span></span>
    <span data-ttu-id="a77ef-144">リソース グループ</span><span class="sxs-lookup"><span data-stu-id="a77ef-144">Resource group</span></span> | <span data-ttu-id="a77ef-145">ストレージ アカウントを作成されるのと同じリソースを提供します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="a77ef-146">リージョン</span><span class="sxs-lookup"><span data-stu-id="a77ef-146">Region</span></span> | <span data-ttu-id="a77ef-147">リージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-147">Specify region.</span></span>
    <span data-ttu-id="a77ef-148">ファクトリー名</span><span class="sxs-lookup"><span data-stu-id="a77ef-148">Factory Name</span></span> | <span data-ttu-id="a77ef-149">ファクトリー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-149">Specify factory name.</span></span>
    <span data-ttu-id="a77ef-150">FO リンクされた Service_service プリンシパル キー</span><span class="sxs-lookup"><span data-stu-id="a77ef-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="a77ef-151">アプリケーション キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-151">Specify the application's key.</span></span>
    <span data-ttu-id="a77ef-152">Azure Blob Storage_connection 文字列</span><span class="sxs-lookup"><span data-stu-id="a77ef-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="a77ef-153">Azure Blob Storage の接続文字列。</span><span class="sxs-lookup"><span data-stu-id="a77ef-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="a77ef-154">Dynamics CRM リンクされた Service_password</span><span class="sxs-lookup"><span data-stu-id="a77ef-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="a77ef-155">ユーザー名として指定したユーザー アカウントのパスワード。</span><span class="sxs-lookup"><span data-stu-id="a77ef-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="a77ef-156">FO リンクされた Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="a77ef-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="a77ef-157">FO リンクされた Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="a77ef-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="a77ef-158">アプリケーションが存在するテナント情報 (ドメイン名またはテナント ID) を指定します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="a77ef-159">FO リンクされた Service_properties_type Properties_aad リソース ID</span><span class="sxs-lookup"><span data-stu-id="a77ef-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="a77ef-160">FO リンクされた Service_properties_type Properties_service プリンシパル ID</span><span class="sxs-lookup"><span data-stu-id="a77ef-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="a77ef-161">アプリケーションのクライアント ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="a77ef-162">Dynamics CRM リンクされた Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="a77ef-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="a77ef-163">Dynamics 365 に接続する username。</span><span class="sxs-lookup"><span data-stu-id="a77ef-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="a77ef-164">詳細については、次のトピックを参照してください:</span><span class="sxs-lookup"><span data-stu-id="a77ef-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="a77ef-165">各環境の Resource Manager テンプレートの手動促進</span><span class="sxs-lookup"><span data-stu-id="a77ef-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="a77ef-166">リンクされたサービス プロパティ</span><span class="sxs-lookup"><span data-stu-id="a77ef-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="a77ef-167">Azure Data Factory を使用したデータのコピー</span><span class="sxs-lookup"><span data-stu-id="a77ef-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="a77ef-168">配置後に、データ ファクトリのデータセット、データ フロー、およびリンクされたサービスを検証します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![データセット、データ フロー、およびリンクされたサービス](media/data-factory-validate.png)

11. <span data-ttu-id="a77ef-170">**管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-170">Navigate to **Manage**.</span></span> <span data-ttu-id="a77ef-171">**接続** で、**リンクされたサービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="a77ef-172">**DynamicsCrmLinkedService** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="a77ef-173">**リンクされたサービスの編集 (Dynamics CRM)** フォームに、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="a77ef-174">フィールド</span><span class="sxs-lookup"><span data-stu-id="a77ef-174">Field</span></span> | <span data-ttu-id="a77ef-175">先頭値</span><span class="sxs-lookup"><span data-stu-id="a77ef-175">Value</span></span>
    ---|---
    <span data-ttu-id="a77ef-176">氏名</span><span class="sxs-lookup"><span data-stu-id="a77ef-176">Name</span></span> | <span data-ttu-id="a77ef-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="a77ef-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="a77ef-178">説明</span><span class="sxs-lookup"><span data-stu-id="a77ef-178">Description</span></span> | <span data-ttu-id="a77ef-179">エンティティ データをフェッチする CRM インスタンスに接続するリンクされたサービス</span><span class="sxs-lookup"><span data-stu-id="a77ef-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="a77ef-180">統合ランタイム経由の接続</span><span class="sxs-lookup"><span data-stu-id="a77ef-180">Connect via integration runtime</span></span> | <span data-ttu-id="a77ef-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a77ef-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="a77ef-182">配置のタイプ</span><span class="sxs-lookup"><span data-stu-id="a77ef-182">Deployment type</span></span> | <span data-ttu-id="a77ef-183">オンライン</span><span class="sxs-lookup"><span data-stu-id="a77ef-183">Online</span></span>
    <span data-ttu-id="a77ef-184">サービス URI</span><span class="sxs-lookup"><span data-stu-id="a77ef-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="a77ef-185">認証タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ef-185">Authentication type</span></span> | <span data-ttu-id="a77ef-186">Office365</span><span class="sxs-lookup"><span data-stu-id="a77ef-186">Office365</span></span>
    <span data-ttu-id="a77ef-187">ユーザー名</span><span class="sxs-lookup"><span data-stu-id="a77ef-187">User name</span></span> |
    <span data-ttu-id="a77ef-188">パスワードまたは Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a77ef-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="a77ef-189">パスワード</span><span class="sxs-lookup"><span data-stu-id="a77ef-189">Password</span></span>
    <span data-ttu-id="a77ef-190">パスワード</span><span class="sxs-lookup"><span data-stu-id="a77ef-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="a77ef-191">テンプレートの実行</span><span class="sxs-lookup"><span data-stu-id="a77ef-191">Run the template</span></span>

1. <span data-ttu-id="a77ef-192">Finance and Operations アプリを使用して、次の **取引先企業**、**連絡先**、および **仕入先** の二重書き込みマップを停止します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="a77ef-193">顧客 V3 (アカウント)</span><span class="sxs-lookup"><span data-stu-id="a77ef-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="a77ef-194">顧客 V3 (連絡先)</span><span class="sxs-lookup"><span data-stu-id="a77ef-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="a77ef-195">CDS 連絡先 V2 (連絡先)</span><span class="sxs-lookup"><span data-stu-id="a77ef-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="a77ef-196">CDS 連絡先 V2 (連絡先)</span><span class="sxs-lookup"><span data-stu-id="a77ef-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="a77ef-197">仕入先 V2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="a77ef-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="a77ef-198">Dataverse で `msdy_dualwriteruntimeconfig` テーブルからマップが削除されたのを確認します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="a77ef-199">AppSource から [二重書き込み当事者およびグローバル アドレス帳ソリューション](https://aka.ms/dual-write-gab)をインストールします 。</span><span class="sxs-lookup"><span data-stu-id="a77ef-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="a77ef-200">Finance and Operations アプリで、次のテーブルにデータが含まれている場合は、そのテーブルの **初期同期** を実行します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="a77ef-201">あいさつ文</span><span class="sxs-lookup"><span data-stu-id="a77ef-201">Salutations</span></span>
    + <span data-ttu-id="a77ef-202">個人の特徴タイプ</span><span class="sxs-lookup"><span data-stu-id="a77ef-202">Personal character types</span></span>
    + <span data-ttu-id="a77ef-203">結句</span><span class="sxs-lookup"><span data-stu-id="a77ef-203">Complimentary closing</span></span>
    + <span data-ttu-id="a77ef-204">連絡担当者の肩書き</span><span class="sxs-lookup"><span data-stu-id="a77ef-204">Contact person titles</span></span>
    + <span data-ttu-id="a77ef-205">意思決定ロール</span><span class="sxs-lookup"><span data-stu-id="a77ef-205">Decision making roles</span></span>
    + <span data-ttu-id="a77ef-206">ロイヤルティ レベル</span><span class="sxs-lookup"><span data-stu-id="a77ef-206">Loyalty levels</span></span>

5. <span data-ttu-id="a77ef-207">Customer Engagement アプリで、次のプラグイン ステップを無効にします。</span><span class="sxs-lookup"><span data-stu-id="a77ef-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="a77ef-208">取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-208">Account Update</span></span>
         + <span data-ttu-id="a77ef-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: 取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="a77ef-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: 取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="a77ef-211">連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-211">Contact Update</span></span>
         + <span data-ttu-id="a77ef-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: 連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="a77ef-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: 連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="a77ef-214">msdyn_party の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-214">msdyn_party Update</span></span>
         + <span data-ttu-id="a77ef-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="a77ef-216">msdyn_vendor の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="a77ef-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="a77ef-218">Customer Engagement アプリで、次のワークフローを無効にします:</span><span class="sxs-lookup"><span data-stu-id="a77ef-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="a77ef-219">取引先企業テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="a77ef-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="a77ef-220">取引先企業テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="a77ef-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="a77ef-221">連絡先テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="a77ef-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="a77ef-222">仕入先テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="a77ef-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="a77ef-223">取引先企業テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="a77ef-224">仕入先テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="a77ef-225">取引先担当者テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="a77ef-226">仕入先テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="a77ef-227">データ ファクトリーで、次の図に示すように **今すぐトリガーする** を選択してテンプレートを実行します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="a77ef-228">このプロセスは、データ量に基づいて完了に数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a77ef-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![トリガーの実行](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="a77ef-230">**取引先企業**、**連絡先**、および **仕入先** をカスタマイズする場合は、テンプレートを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a77ef-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="a77ef-231">Finance and Operations アプリで新しい **当事者** レコードをインポートします。</span><span class="sxs-lookup"><span data-stu-id="a77ef-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="a77ef-232">Azure Blob Storage から `FONewParty.csv` ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a77ef-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="a77ef-233">パスは `partybootstrapping/output/FONewParty.csv` です。</span><span class="sxs-lookup"><span data-stu-id="a77ef-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="a77ef-234">`FONewParty.csv` ファイルを Excel ファイルに変換し、Excel ファイルを Finance and Operations アプリにインポートします。</span><span class="sxs-lookup"><span data-stu-id="a77ef-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="a77ef-235">csv インポートが機能する場合は、csv ファイルを直接インポートできます。</span><span class="sxs-lookup"><span data-stu-id="a77ef-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="a77ef-236">データ量によっては、インポートの実行に数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a77ef-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="a77ef-237">詳細については、[データのインポート ジョブとエクスポート ジョブの概要](../data-import-export-job.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a77ef-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Datavers 当事者レコードのインポート](media/data-factory-import-party.png)

9. <span data-ttu-id="a77ef-239">Customer Engagement アプリで、次のプラグイン ステップを有効にします:</span><span class="sxs-lookup"><span data-stu-id="a77ef-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="a77ef-240">取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-240">Account Update</span></span>
         + <span data-ttu-id="a77ef-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: 取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="a77ef-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: 取引先企業の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="a77ef-243">連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-243">Contact Update</span></span>
         + <span data-ttu-id="a77ef-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: 連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="a77ef-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: 連絡先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="a77ef-246">msdyn_party の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-246">msdyn_party Update</span></span>
         + <span data-ttu-id="a77ef-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="a77ef-248">msdyn_vendor の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="a77ef-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="a77ef-250">Customer Engagement アプリで、前の手順で次のワークフローを無効化した場合は、有効にします:</span><span class="sxs-lookup"><span data-stu-id="a77ef-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="a77ef-251">取引先企業テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="a77ef-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="a77ef-252">取引先企業テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="a77ef-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="a77ef-253">連絡先テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="a77ef-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="a77ef-254">仕入先テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="a77ef-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="a77ef-255">取引先企業テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="a77ef-256">仕入先テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="a77ef-257">取引先担当者テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="a77ef-258">仕入先テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="a77ef-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="a77ef-259">[当事者およびグローバル アドレス帳](party-gab.md)の指示に従って **当事者** 関連のマップを実行します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="a77ef-260">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a77ef-260">Troubleshooting</span></span>

1. <span data-ttu-id="a77ef-261">プロセスが失敗した場合は、失敗した活動から始めてデータ ファクトリを再実行します。</span><span class="sxs-lookup"><span data-stu-id="a77ef-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="a77ef-262">一部のファイルは、データ検証の目的で使用できるデータ ファクトリによって生成されます。</span><span class="sxs-lookup"><span data-stu-id="a77ef-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="a77ef-263">データ ファクトリは、コンマ区切りされた csv ファイルに基づいて実行されます。</span><span class="sxs-lookup"><span data-stu-id="a77ef-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="a77ef-264">コンマを含むフィールド値がある場合は、結果に影響が出る場合があります。</span><span class="sxs-lookup"><span data-stu-id="a77ef-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="a77ef-265">コンマを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a77ef-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="a77ef-266">**監視** タブでは、すべてのステップおよび処理済みデータに関する情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="a77ef-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="a77ef-267">特定の手順を選択してデバッグします。</span><span class="sxs-lookup"><span data-stu-id="a77ef-267">Select a specific step to debug it.</span></span>

    ![監視タブ](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="a77ef-269">テンプレートの詳細を確認する</span><span class="sxs-lookup"><span data-stu-id="a77ef-269">Learn more about the template</span></span>

<span data-ttu-id="a77ef-270">テンプレートに関する追加情報は、[Azure Data Factory テンプレートの readme のコメント](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) で確認できます。</span><span class="sxs-lookup"><span data-stu-id="a77ef-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>

---
title: 初めて同期をする際に発生する問題のトラブルシューティング
description: このトピックでは、 初めて同期をする際に発生する可能性のある問題の修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410084"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="13768-103">初めて同期をする際に発生する問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="13768-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13768-104">このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="13768-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="13768-105">このトピックでは、 初めて同期をする際に発生する可能性のある問題の修正に役立つトラブルシューティングに特化した情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="13768-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13768-106">このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="13768-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="13768-107">各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。</span><span class="sxs-lookup"><span data-stu-id="13768-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="13768-108">Finance and Operations アプリの初回の同期エラーを確認します</span><span class="sxs-lookup"><span data-stu-id="13768-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="13768-109">マッピングのテンプレートを有効にすると、マッピングの状態が **実行中** になります。</span><span class="sxs-lookup"><span data-stu-id="13768-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="13768-110">状態が **非実行中** のとなっている場合、初回の同期中にエラーが発生しています。</span><span class="sxs-lookup"><span data-stu-id="13768-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="13768-111">エラーを表示するには、**デュアル書き込み** ページの **初回同期の詳細** タブを選択し ます。</span><span class="sxs-lookup"><span data-stu-id="13768-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![初回同期の詳細タブ](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="13768-113">初回同期を完了できません：400 要求が不正です</span><span class="sxs-lookup"><span data-stu-id="13768-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="13768-114">**問題の修正に必要な役割：** システム管理者</span><span class="sxs-lookup"><span data-stu-id="13768-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="13768-115">マッピングと初回の同期実行時に、次のメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="13768-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="13768-116">*リモート サーバーからエラーが返されました：（400）要求が不正です。 AX のエクスポート中にエラーが発生しました*</span><span class="sxs-lookup"><span data-stu-id="13768-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="13768-117">次に、完全なエラー メッセージの例を示します。</span><span class="sxs-lookup"><span data-stu-id="13768-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="13768-118">このエラーが継続して発生し、初回同期を完了できない場合は、次の手順に従って問題を修正してください。</span><span class="sxs-lookup"><span data-stu-id="13768-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="13768-119">Finance and Operations アプリの仮想マシン（VM）にサイン インします。</span><span class="sxs-lookup"><span data-stu-id="13768-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="13768-120">Microsoft 管理コンソールを起動します。</span><span class="sxs-lookup"><span data-stu-id="13768-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="13768-121">**サービス** ウィンドウで、Microsoft Dynamics 365 データインポート エクスポート フレームワーク サービスが実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="13768-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="13768-122">初回同期が必要となるため、停止している場合は再起動してください。</span><span class="sxs-lookup"><span data-stu-id="13768-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="13768-123">初回同期エラー： 403 権限がありません</span><span class="sxs-lookup"><span data-stu-id="13768-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="13768-124">初回の同期を実行した際に、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="13768-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="13768-125">*（\[権限がありません\]、リモート サーバーからエラーが返されました：（403）権限がありません）AX のエクスポート中にエラーが発生しました*</span><span class="sxs-lookup"><span data-stu-id="13768-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="13768-126">問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="13768-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="13768-127">Finance and Operations アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="13768-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="13768-128">**Azure Active Directory アプリケーション** のページで、**DtAppID** クライアントを削除し、再度追加します。</span><span class="sxs-lookup"><span data-stu-id="13768-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD アプリケーションのリスト](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="13768-130">初回の同期中の自己参照または循環参照エラー</span><span class="sxs-lookup"><span data-stu-id="13768-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="13768-131">いずれかのマッピングに自己参照または循環参照がある場合、次のようなエラーメッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="13768-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="13768-132">エラーは次のカテゴリに分類されます:</span><span class="sxs-lookup"><span data-stu-id="13768-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="13768-133">仕入先 V2 から msdyn_vendors エンティティ マッピングへ</span><span class="sxs-lookup"><span data-stu-id="13768-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="13768-134">顧客 V3 から アカウント エンティティー マッピングへ</span><span class="sxs-lookup"><span data-stu-id="13768-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="13768-135">仕入先 V2 のエラーを msdyn_vendors エンティティ マッピングに対して解決する</span><span class="sxs-lookup"><span data-stu-id="13768-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="13768-136">エンティティに **PrimaryContactPersonId** フィールドと **InvoiceVendorAccountNumber** フィールドの値を持つ既存レコードがある場合、**msdyn_vendors** マッピングに対して **仕入先 V2** で次のような初期同期エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="13768-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="13768-137">これは、**InvoiceVendorAccountNumber** が自己参照フィールドであり、**PrimaryContactPersonId** が仕入先マッピングで循環参照であるためです。</span><span class="sxs-lookup"><span data-stu-id="13768-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="13768-138">*フィールドの guid を解決できませんでした: <field>。検索が見つかりませんでした: <value>。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="13768-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="13768-139">次にいくつか例を挙げます:</span><span class="sxs-lookup"><span data-stu-id="13768-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="13768-140">*フィールドの guid を解決できませんでした: msdyn_vendorprimarycontactperson.msdyn_contactpersonid。検索が見つかりませんでした: 000056。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="13768-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="13768-141">*フィールドの guid を解決できませんでした: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber。検索が見つかりませんでした: V24-1。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="13768-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="13768-142">仕入先エンティティのこれらのフィールドに値を持つレコードがある場合は、以下のセクションの手順に従って、初期同期を正常に完了してください。</span><span class="sxs-lookup"><span data-stu-id="13768-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="13768-143">Finance and Operations アプリで、マッピングから **PrimaryContactPersonId** フィールドと **InvoiceVendorAccountNumber** フィールドを削除し、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="13768-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="13768-144">**仕入先 V2 (msdyn_vendors)** の二重書き込みマッピング ページに移動し、**エンティティ マッピング** タブを選択します。左のフィルタで、**Finance and Operations apps.Vendors V2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13768-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="13768-145">右側のフィルターで、**Sales.Vendor** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13768-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="13768-146">**primarycontactperson** を検索して、ソース フィールド **PrimaryContactPersonId** を見つけます。</span><span class="sxs-lookup"><span data-stu-id="13768-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="13768-147">**アクション** ボタンをクリックし、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13768-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![自己参照または循環参照 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="13768-149">繰り返して、**InvoiceVendorAccountNumber** フィールドを削除します。</span><span class="sxs-lookup"><span data-stu-id="13768-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![自己参照または循環参照 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="13768-151">マッピングの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="13768-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="13768-152">**仕入先 V2** エンティティの変更追跡を無効にします。</span><span class="sxs-lookup"><span data-stu-id="13768-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="13768-153">**データ管理 \> データ エンティティ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="13768-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="13768-154">**仕入先 V2** エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="13768-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="13768-155">メニュー バーの **オプション** をクリックし、**変更の追跡** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13768-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![自己参照または循環参照 5](media/selfref_options.png)
    
    4. <span data-ttu-id="13768-157">**変更の追跡を無効にする** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13768-157">Click **Disable Change Tracking**.</span></span>
    
        ![自己参照または循環参照 6](media/selfref_tracking.png)

3. <span data-ttu-id="13768-159">**仕入先 V2 (msdyn_vendors)** マッピングの初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="13768-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="13768-160">初期同期はエラーなしで正常に実行されます。</span><span class="sxs-lookup"><span data-stu-id="13768-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="13768-161">**CDS 連絡先 V2 (contacts)** マッピングの初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="13768-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="13768-162">連絡先レコードも初期同期する必要があるため、仕入先エンティティの "基本連絡先" フィールドを同期する場合は、このマッピングを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13768-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="13768-163">フィールド **PrimaryContactPersonId** と **InvoiceVendorAccountNumber** を **仕入先 V2 (msdyn_vendors)** マッピングに追加し直し、マッピングを保存します。</span><span class="sxs-lookup"><span data-stu-id="13768-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="13768-164">**仕入先 V2 (msdyn_vendors)** マッピングの初期同期を再度実行します。</span><span class="sxs-lookup"><span data-stu-id="13768-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="13768-165">変更の追跡が無効になっているため、すべてのレコードが同期されます。</span><span class="sxs-lookup"><span data-stu-id="13768-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="13768-166">**仕入先 V2** エンティティの変更追跡を有効にします。</span><span class="sxs-lookup"><span data-stu-id="13768-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="13768-167">顧客 V3 のエラーをアカウント エンティティー マッピングに対して解決する</span><span class="sxs-lookup"><span data-stu-id="13768-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="13768-168">エンティティに **ContactPersonID** フィールドと **InvoiceAccount** フィールドの値を持つ既存レコードがある場合、**アカウント** マッピングに対して **顧客 V3** で次のような初期同期エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="13768-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="13768-169">これは、**InvoiceAccount** が自己参照フィールドであり、**ContactPersonID** が仕入先マッピングで循環参照であるためです。</span><span class="sxs-lookup"><span data-stu-id="13768-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="13768-170">*フィールドの guid を解決できませんでした: <field>。検索が見つかりませんでした: <value>。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="13768-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="13768-171">*フィールドの guid を解決できませんでした: primarycontactid.msdyn_contactpersonid。検索が見つかりませんでした: 000056。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="13768-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="13768-172">*フィールドの guid を解決できませんでした: msdyn_billingaccount.accountnumber。検索が見つかりませんでした: 1206-1。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="13768-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="13768-173">顧客エンティティのこれらのフィールドに値を持つレコードがある場合は、以下のセクションの手順に従って、初期同期を正常に完了してください。</span><span class="sxs-lookup"><span data-stu-id="13768-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="13768-174">この方法は、アカウントや連絡先などのすぐに利用できるエンティティに使用できます。</span><span class="sxs-lookup"><span data-stu-id="13768-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="13768-175">Finance and Operations アプリで、**顧客 V3 (accounts)** マッピングからフィールド **ContactPersonID** と **InvoiceAccount** を削除し、マッピングを保存します。</span><span class="sxs-lookup"><span data-stu-id="13768-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="13768-176">**顧客 V3 (accounts)** の二重書き込みマッピング ページに移動し、**エンティティ マッピング** タブを選択します。左のフィルタで、**Finance and Operations apps.Customers V3** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13768-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="13768-177">右側のフィルターで、**Common Data Service.Account** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13768-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="13768-178">**contactperson** を検索して、ソース フィールド **ContactPersonID** を見つけます。</span><span class="sxs-lookup"><span data-stu-id="13768-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="13768-179">**アクション** ボタンをクリックし、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13768-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![自己参照または循環参照 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="13768-181">繰り返して、**InvoiceAccount** フィールドを削除します。</span><span class="sxs-lookup"><span data-stu-id="13768-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![自己参照または循環参照](media/cust_selfref4.png)
    
    5. <span data-ttu-id="13768-183">マッピングの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="13768-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="13768-184">**顧客 V3** エンティティの変更追跡を無効にします。</span><span class="sxs-lookup"><span data-stu-id="13768-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="13768-185">**データ管理 \> データ エンティティ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="13768-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="13768-186">**顧客 V3** エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="13768-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="13768-187">メニュー バーの **オプション** をクリックし、**変更の追跡** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13768-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![自己参照または循環参照 5](media/selfref_options.png)
    
    4. <span data-ttu-id="13768-189">**変更の追跡を無効にする** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13768-189">Click **Disable Change Tracking**.</span></span>
    
        ![自己参照または循環参照 6](media/selfref_tracking.png)

3. <span data-ttu-id="13768-191">**顧客 V3 (Accounts)** マッピングの初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="13768-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="13768-192">初期同期はエラーなしで正常に実行されます。</span><span class="sxs-lookup"><span data-stu-id="13768-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="13768-193">**CDS 連絡先 V2 (contacts)** マッピングの初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="13768-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="13768-194">同じ名前のマップが 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="13768-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="13768-195">**FO.CDS Vendor Contacts V2 から CDS.Contacts への同期のための二重書き込みテンプレート。新しいパッケージ \[Dynamics365SupplyChainExtended\] が必要です。** という説明のあるものを選択します</span><span class="sxs-lookup"><span data-stu-id="13768-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="13768-196">マップの **詳細** タブで。</span><span class="sxs-lookup"><span data-stu-id="13768-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="13768-197">**顧客 V3 (accounts)** マッピングからフィールド **InvoiceAccount** と **ContactPersonId** を追加し、マッピングを保存します。</span><span class="sxs-lookup"><span data-stu-id="13768-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="13768-198">これで、**InvoiceAccount** フィールドと **ContactPersonId** フィールドの両方がライブ同期モードの一部になりました。</span><span class="sxs-lookup"><span data-stu-id="13768-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="13768-199">次の手順では、これらのフィールドの初期同期を完了します。</span><span class="sxs-lookup"><span data-stu-id="13768-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="13768-200">**顧客 V3 (Accounts)** マッピングの初期同期を再度実行します。</span><span class="sxs-lookup"><span data-stu-id="13768-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="13768-201">変更の追跡が無効になっているため、同期を実行すると、**InvoiceAccount** と **ContactPersonId** のデータが Finance and Operations アプリから Common Data Service に同期されます。</span><span class="sxs-lookup"><span data-stu-id="13768-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="13768-202">**InvoiceAccount** と **ContactPersonId** のデータをに Common Data Service から Finance and Operations に同期するには 、データ統合プロジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="13768-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="13768-203">Power Apps で、**Sales.Account** と **Finance and Operations apps.Customers V3** エンティティの間にデータ統合プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="13768-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="13768-204">データの方向は、Common Data Service から Finance and Operations アプリである必要があります。</span><span class="sxs-lookup"><span data-stu-id="13768-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="13768-205">**InvoiceAccount** は二重書き込みの新しい属性なので、この属性の初期同期をスキップすることができます。</span><span class="sxs-lookup"><span data-stu-id="13768-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="13768-206">詳細については、[Common Data Service へデータを統合](https://docs.microsoft.com/power-platform/admin/data-integrator) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13768-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="13768-207">次の図は、**CustomerAccount** と **ContactPersonId** を更新するプロジェクトを示しています。</span><span class="sxs-lookup"><span data-stu-id="13768-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![自己参照または循環参照](media/cust_selfref6.png)

    2. <span data-ttu-id="13768-209">Finance and Operations アプリではフィルター基準と一致するレコードのみが更新されるため、Common Data Service 側のフィルターに会社の基準を追加します。</span><span class="sxs-lookup"><span data-stu-id="13768-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="13768-210">フィルタを追加するには、[フィルタ] アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="13768-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="13768-211">**クエリの編集** ダイアログで、**_msdyn_company_value eq '\<guid\>'** のようなフィルター クエリを追加できます。</span><span class="sxs-lookup"><span data-stu-id="13768-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="13768-212">[フィルタ] アイコンが表示されない場合は、サポート チケットを作成して、データ統合チームにテナントのフィルター機能を有効にするよう依頼します。</span><span class="sxs-lookup"><span data-stu-id="13768-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="13768-213">**_Msdyn_company_value** のフィルター クエリを入力しない場合、すべてのレコードが同期されます。</span><span class="sxs-lookup"><span data-stu-id="13768-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![自己参照または循環参照](media/cust_selfref7.png)

        <span data-ttu-id="13768-215">これで、レコードの初期同期が完了します。</span><span class="sxs-lookup"><span data-stu-id="13768-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="13768-216">Finance and Operations アプリで **顧客 V3** エンティティの変更追跡を有効にします。</span><span class="sxs-lookup"><span data-stu-id="13768-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>


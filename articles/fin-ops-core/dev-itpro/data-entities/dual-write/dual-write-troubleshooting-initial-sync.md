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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 4d0ca1fb4b7a4964194516544686b6bb7d26e76c
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997329"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="69c3a-103">初めて同期をする際に発生する問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="69c3a-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69c3a-104">このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="69c3a-105">このトピックでは、 初めて同期をする際に発生する可能性のある問題の修正に役立つトラブルシューティングに特化した情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69c3a-106">このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="69c3a-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="69c3a-107">各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。</span><span class="sxs-lookup"><span data-stu-id="69c3a-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="69c3a-108">Finance and Operations アプリの初回の同期エラーを確認します</span><span class="sxs-lookup"><span data-stu-id="69c3a-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="69c3a-109">マッピングのテンプレートを有効にすると、マッピングの状態が **実行中** になります。</span><span class="sxs-lookup"><span data-stu-id="69c3a-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="69c3a-110">状態が **非実行中** のとなっている場合、初回の同期中にエラーが発生しています。</span><span class="sxs-lookup"><span data-stu-id="69c3a-110">If the status is **Not running** , errors occurred during initial synchronization.</span></span> <span data-ttu-id="69c3a-111">エラーを表示するには、 **デュアル書き込み** ページの **初回同期の詳細** タブを選択し ます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![[初期同期の詳細] タブでのエラー](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="69c3a-113">初回同期を完了できません：400 要求が不正です</span><span class="sxs-lookup"><span data-stu-id="69c3a-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="69c3a-114">**問題の修正に必要な役割：** システム管理者</span><span class="sxs-lookup"><span data-stu-id="69c3a-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="69c3a-115">マッピングと初回の同期実行時に、次のメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="69c3a-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="69c3a-116">*(\[要求が不正です\]、リモート サーバーからエラーが返されました: (400) 要求が不正です)、AX のエクスポート中にエラーが発生しました*</span><span class="sxs-lookup"><span data-stu-id="69c3a-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="69c3a-117">次に、完全なエラー メッセージの例を示します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="69c3a-118">このエラーが継続して発生し、初回同期を完了できない場合は、次の手順に従って問題を修正してください。</span><span class="sxs-lookup"><span data-stu-id="69c3a-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="69c3a-119">Finance and Operations アプリの仮想マシン（VM）にサイン インします。</span><span class="sxs-lookup"><span data-stu-id="69c3a-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="69c3a-120">Microsoft 管理コンソールを起動します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="69c3a-121">**サービス** ウィンドウで、Microsoft Dynamics 365 データインポート エクスポート フレームワーク サービスが実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="69c3a-122">初回同期が必要となるため、停止している場合は再起動してください。</span><span class="sxs-lookup"><span data-stu-id="69c3a-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="69c3a-123">初回同期エラー： 403 権限がありません</span><span class="sxs-lookup"><span data-stu-id="69c3a-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="69c3a-124">初回の同期を実行した際に、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="69c3a-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="69c3a-125">*（\[権限がありません\]、リモート サーバーからエラーが返されました：（403）権限がありません）AX のエクスポート中にエラーが発生しました*</span><span class="sxs-lookup"><span data-stu-id="69c3a-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="69c3a-126">問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="69c3a-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="69c3a-127">Finance and Operations アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="69c3a-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="69c3a-128">**Azure Active Directory アプリケーション** のページで、 **DtAppID** クライアントを削除し、再度追加します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD アプリケーションの一覧の DtAppID クライアント](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="69c3a-130">初回の同期中の自己参照または循環参照エラー</span><span class="sxs-lookup"><span data-stu-id="69c3a-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="69c3a-131">いずれかのマッピングに自己参照または循環参照がある場合、次のようなエラーメッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="69c3a-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="69c3a-132">エラーは次のカテゴリに分類されます:</span><span class="sxs-lookup"><span data-stu-id="69c3a-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="69c3a-133">仕入先 V2–to–msdyn_vendors  エンティティ マッピングでのエラー</span><span class="sxs-lookup"><span data-stu-id="69c3a-133">Errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="69c3a-134">顧客 V3–to–Accounts エンティティ マッピングでのエラー</span><span class="sxs-lookup"><span data-stu-id="69c3a-134">Errors in the Customers V3–to–Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="69c3a-135">仕入先 V2–to–msdyn_vendors エンティティ マッピングでのエラーを解決する</span><span class="sxs-lookup"><span data-stu-id="69c3a-135">Resolve errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>

<span data-ttu-id="69c3a-136">エンティティに **PrimaryContactPersonId** フィールドと **InvoiceVendorAccountNumber** フィールドの値を持つ既存レコードがある場合、 **msdyn\_vendors** に対して **仕入先 V2** のマッピングで次のような初期同期エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="69c3a-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the entities have existing records where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="69c3a-137">これらのエラーの発生は、 **InvoiceVendorAccountNumber** が自己参照フィールドであり、 **PrimaryContactPersonId** が仕入先マッピングで循環参照であるためです。</span><span class="sxs-lookup"><span data-stu-id="69c3a-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="69c3a-138">表示されるエラーメッセージの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="69c3a-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="69c3a-139">*フィールド \<field\> のガイドを解決できませんでした。検索で \<value\> は見つかりませんでした。次の URL で、参照データが存在するかどうかを確認してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="69c3a-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="69c3a-140">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-140">Here are some examples:</span></span>

- <span data-ttu-id="69c3a-141">*フィールド msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid のガイドを解決できませんでした。検索で 000056 は見つかりませんでした。次の URL で、参照データが存在するかどうかを確認してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="69c3a-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="69c3a-142">*フィールド msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber のガイドを解決できませんでした。検索で V24-1 は見つかりませんでした。参照データが存在するかどうかは次の URL を試してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="69c3a-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="69c3a-143">仕入先エンティティの任意のレコードに **PrimaryContactPersonId** フィールドと **InvoiceVendorAccountNumber** フィールドがある場合、以下のステップの手順に従って、初期同期を正常に完了してください。</span><span class="sxs-lookup"><span data-stu-id="69c3a-143">If any records in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="69c3a-144">Finance and Operations アプリで、マッピングから **PrimaryContactPersonId** フィールドと **InvoiceVendorAccountNumber** フィールドを削除し、マッピングを保存します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="69c3a-145">**仕入先 V2 (msdyn\_vendors)** の二重書き込みマッピング ページで、左のフィールドで **エンティティ マッピング** タブで、 **Finance and Operations アプリ 仕入先 V2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)** , on the **Entity mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="69c3a-146">右側のフィルターで、 **Sales.Vendor** を選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="69c3a-147">**primarycontactperson** を検索して、 **PrimaryContactPersonId** ソース フィールドを見つけます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="69c3a-148">**アクション** を選択し、 **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-148">Select **Actions** , and then select **Delete**.</span></span>

        ![PrimaryContactPersonId フィールドの削除](media/vend_selfref3.png)

    4. <span data-ttu-id="69c3a-150">これらの手順を繰り返して、 **InvoiceVendorAccountNumber** フィールドを削除します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![InvoiceVendorAccountNumber フィールドの削除](media/vend-selfref4.png)

    5. <span data-ttu-id="69c3a-152">マッピングへの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="69c3a-153">**仕入先 V2** エンティティの Change Tracking をオフにします。</span><span class="sxs-lookup"><span data-stu-id="69c3a-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="69c3a-154">**データ管理** ワークスペースで、 **フレームワーク パラメーター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-154">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="69c3a-155">**仕入先 V2** エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="69c3a-156">操作ウィンドウで、 **オプション** を選択し、 **Change Tracking** を選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-156">On the Action Pane, select **Options** , and then select **Change tracking**.</span></span>

        ![Change Tracking オプションの選択](media/selfref_options.png)

    4. <span data-ttu-id="69c3a-158">**Change Tracking を無効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-158">Select **Disable Change Tracking**.</span></span>

        ![Change Tracking を無効にする選択](media/selfref_tracking.png)

3. <span data-ttu-id="69c3a-160">**仕入先 V2 (msdyn\_vendors)** マッピングの初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="69c3a-161">初期同期はエラーなしで正常に実行されます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="69c3a-162">**CDS 連絡先 V2 (連絡先)** マッピングの初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="69c3a-163">連絡先レコードに対しても初期同期する必要があるため、仕入先エンティティの [基本連絡先] フィールドを同期する場合は、このマッピングを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="69c3a-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact records.</span></span>
5. <span data-ttu-id="69c3a-164">**PrimaryContactPersonId** フィールドと **InvoiceVendorAccountNumber** フィールドを **仕入先 V2 (msdyn\_vendors)** マッピングに追加し直し、マッピングを保存します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="69c3a-165">**仕入先 V2 (msdyn\_vendors)** マッピングの初期同期を再度実行します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="69c3a-166">Change Tracking がオフになっているため、すべてのレコードが同期されます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-166">Because change tracking is turned off, all the records will be synced.</span></span>
7. <span data-ttu-id="69c3a-167">**仕入先 V2** エンティティの Change Tracking をオフにし直します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="69c3a-168">Customers V3–to–Accounts エンティティー マッピングでエラーを解決する</span><span class="sxs-lookup"><span data-stu-id="69c3a-168">Resolve errors in the Customers V3–to–Accounts entity mapping</span></span>

<span data-ttu-id="69c3a-169">エンティティに **ContactPersonID** フィールドと **InvoiceAccount** フィールドの値を持つ既存レコードがある場合、 **アカウント** に対して **顧客 V3** のマッピングで次のような初期同期エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="69c3a-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the entities have existing records where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="69c3a-170">これらのエラーは、 **InvoiceAccount** が自己参照フィールドであり、 **ContactPersonID** が仕入先マッピングで循環参照であるためです。</span><span class="sxs-lookup"><span data-stu-id="69c3a-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="69c3a-171">表示されるエラーメッセージの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="69c3a-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="69c3a-172">*フィールド \<field\> のガイドを解決できませんでした。検索で \<value\> は見つかりませんでした。次の URL で、参照データが存在するかどうかを確認してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="69c3a-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="69c3a-173">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-173">Here are some examples:</span></span>

- <span data-ttu-id="69c3a-174">*フィールド primarycontactid.msdyn\_contactpersonid のガイドを解決できませんでした。検索で 000056 は見つかりませんでした。次の URL で、参照データが存在するかどうかを確認してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="69c3a-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="69c3a-175">*フィールド msdyn\_billingaccount.accountnumber のガイドを解決できませんでした。検索で 1206-1 は見つかりませんでした。次の URL で、参照データが存在するかどうかを確認してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="69c3a-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="69c3a-176">仕入先エンティティの任意のレコードに **ContactPersonID** フィールドと **InvoiceAccount** フィールドがある場合、以下のステップの手順に従って、初期同期を正常に完了してください。</span><span class="sxs-lookup"><span data-stu-id="69c3a-176">If any records in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="69c3a-177">この方法は、 **アカウント** と **連絡先** などのすぐに利用できるエンティティに使用できます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-177">You can use this approach for any out-of-box entities, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="69c3a-178">Finance and Operations アプリで、 **顧客 V3 (アカウント)** マッピングからフィールド **ContactPersonID** フィールドと **InvoiceAccount** フィールドを削除し、マッピングを保存します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="69c3a-179">**顧客 V3 (アカウント)** の二重書き込みマッピング ページの、 **エンティティ マッピング** タブ、左のフィルタで、 **Finance and Operations アプリ 顧客 V3** を選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-179">On the dual-write mapping page for **Customers V3 (accounts)** , on the **Entity mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="69c3a-180">右側のフィルターで、 **Common Data Service.Account** を選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-180">In the right filter, select **Common Data Service.Account**.</span></span>
    2. <span data-ttu-id="69c3a-181">**contactperson** を検索して、 **ContactPersonID** ソース フィールドを見つけます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="69c3a-182">**アクション** を選択し、 **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-182">Select **Actions** , and then select **Delete**.</span></span>

        ![ContactPersonID フィールドの削除](media/cust_selfref3.png)

    4. <span data-ttu-id="69c3a-184">これらの手順を繰り返して、 **InvoiceAccount** フィールドを削除します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![InvoiceAccount フィールドの削除](media/cust_selfref4.png)

    5. <span data-ttu-id="69c3a-186">マッピングへの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="69c3a-187">**仕入先 V3** エンティティの Change Tracking をオフにします。</span><span class="sxs-lookup"><span data-stu-id="69c3a-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="69c3a-188">**データ管理** ワークスペースで、 **フレームワーク パラメーター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-188">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="69c3a-189">**顧客 V3** エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="69c3a-190">操作ウィンドウで、 **オプション** を選択し、 **Change Tracking** を選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-190">On the Action Pane, select **Options** , and then select **Change tracking**.</span></span>

        ![Change Tracking オプションの選択](media/selfref_options.png)

    4. <span data-ttu-id="69c3a-192">**Change Tracking を無効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-192">Select **Disable Change Tracking**.</span></span>

        ![Change Tracking を無効にする選択](media/selfref_tracking.png)

3. <span data-ttu-id="69c3a-194">**顧客 V3 (アカウント)** マッピングの初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="69c3a-195">初期同期はエラーなしで正常に実行されます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="69c3a-196">**CDS 連絡先 V2 (連絡先)** マッピングの初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="69c3a-197">同じ名前のマップが 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="69c3a-197">There are two maps that have the same name.</span></span> <span data-ttu-id="69c3a-198">**詳細** タブで次の説明を持つマップを必ず選択してください: **FO.CDS 仕入先の連絡先 V2 から CDS.Contacts との間の同期のための二重書き込みテンプレート。新しいパッケージ \[Dynamics365SupplyChainExtended\] が必要です。**</span><span class="sxs-lookup"><span data-stu-id="69c3a-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="69c3a-199">**顧客 V3 (アカウント)** マッピングから **InvoiceAccount** フィールドと **ContactPersonId** フィールドを追加し、マッピングを保存します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="69c3a-200">**InvoiceAccount** フィールドと **ContactPersonId** フィールドの両方が再度ライブ同期モードの一部になりました。</span><span class="sxs-lookup"><span data-stu-id="69c3a-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="69c3a-201">次の手順では、これらのフィールドの初期同期をおこないます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="69c3a-202">**顧客 V3 (アカウント)** マッピングの初期同期を再度実行します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="69c3a-203">Change Tracking が無効になっているため、 **InvoiceAccount** と **ContactPersonId** のデータが Finance and Operations アプリから Common Data Service に同期されます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Common Data Service.</span></span>
7. <span data-ttu-id="69c3a-204">**InvoiceAccount** と **ContactPersonId** のデータを Common Data Service から Finance and Operations アプリに同期するには 、データ統合プロジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="69c3a-205">Power Apps で、 **Sales.Account** と **Finance and Operations apps.Customers V3** エンティティの間にデータ統合プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="69c3a-206">データの方向は、Common Data Service から Finance and Operations アプリである必要があります。</span><span class="sxs-lookup"><span data-stu-id="69c3a-206">The data direction must be from Common Data Service to the Finance and Operations app.</span></span> <span data-ttu-id="69c3a-207">**InvoiceAccount** は二重書き込みの新しい属性なので、この属性の初期同期をスキップすることができます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="69c3a-208">詳細については、[Common Data Service へデータを統合](https://docs.microsoft.com/power-platform/admin/data-integrator) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69c3a-208">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="69c3a-209">次の図は、 **CustomerAccount** と **ContactPersonId** を更新するプロジェクトを示しています。</span><span class="sxs-lookup"><span data-stu-id="69c3a-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![CustomerAccount と ContactPersonId を更新するためのデータ統合プロジェクト](media/cust_selfref6.png)

    2. <span data-ttu-id="69c3a-211">Finance and Operations アプリではフィルター基準と一致するレコードのみが更新されるため、Common Data Service 側のフィルターに会社の基準を追加します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-211">Add the company criteria in the filter on the Common Data Service side, so that only records that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="69c3a-212">フィルタを追加するには、[フィルタ] ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="69c3a-213">その後、 **クエリの編集** ダイアログ ボックスで、 **\_msdyn\_company\_value eq '\<guid\>'** のようなフィルター クエリを追加できます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="69c3a-214">[注記] フィルタ― ボタンが表示されない場合は、サポート チケットを作成して、データ統合チームにテナントのフィルター機能を有効にするよう依頼します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="69c3a-215">**\_msdyn\_company\_value** のフィルター クエリを入力しない場合、すべてのレコードが同期されます。</span><span class="sxs-lookup"><span data-stu-id="69c3a-215">If you don't enter a filter query for **\_msdyn\_company\_value** , all the records will be synced.</span></span>

        ![フィルタ クエリの追加](media/cust_selfref7.png)

    <span data-ttu-id="69c3a-217">レコードの初期同期が完了しました。</span><span class="sxs-lookup"><span data-stu-id="69c3a-217">The initial synchronization of the records is now completed.</span></span>

8. <span data-ttu-id="69c3a-218">Finance and Operations アプリで、 **顧客 V3** エンティティの Change Tracking をオンにし直します。</span><span class="sxs-lookup"><span data-stu-id="69c3a-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>

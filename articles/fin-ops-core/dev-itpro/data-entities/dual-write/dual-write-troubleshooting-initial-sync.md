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
# <a name="troubleshoot-issues-during-initial-synchronization"></a>初めて同期をする際に発生する問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]

このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、 初めて同期をする際に発生する可能性のある問題の修正に役立つトラブルシューティングに特化した情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Finance and Operations アプリの初回の同期エラーを確認します

マッピングのテンプレートを有効にすると、マッピングの状態が **実行中** になります。 状態が **非実行中** のとなっている場合、初回の同期中にエラーが発生しています。 エラーを表示するには、**デュアル書き込み** ページの **初回同期の詳細** タブを選択し ます。

![初回同期の詳細タブ](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>初回同期を完了できません：400 要求が不正です

**問題の修正に必要な役割：** システム管理者

マッピングと初回の同期実行時に、次のメッセージが表示される場合があります。

*リモート サーバーからエラーが返されました：（400）要求が不正です。 AX のエクスポート中にエラーが発生しました*

次に、完全なエラー メッセージの例を示します。

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

このエラーが継続して発生し、初回同期を完了できない場合は、次の手順に従って問題を修正してください。

1. Finance and Operations アプリの仮想マシン（VM）にサイン インします。
2. Microsoft 管理コンソールを起動します。
3. **サービス** ウィンドウで、Microsoft Dynamics 365 データインポート エクスポート フレームワーク サービスが実行されていることを確認します。 初回同期が必要となるため、停止している場合は再起動してください。

## <a name="initial-synchronization-error-403-forbidden"></a>初回同期エラー： 403 権限がありません

初回の同期を実行した際に、次のエラー メッセージが表示される場合があります。

*（\[権限がありません\]、リモート サーバーからエラーが返されました：（403）権限がありません）AX のエクスポート中にエラーが発生しました*

問題を解決するには、次の手順に従います。

1. Finance and Operations アプリにサインインします。
2. **Azure Active Directory アプリケーション** のページで、**DtAppID** クライアントを削除し、再度追加します。

![Azure AD アプリケーションのリスト](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>初回の同期中の自己参照または循環参照エラー

いずれかのマッピングに自己参照または循環参照がある場合、次のようなエラーメッセージが表示されることがあります。 エラーは次のカテゴリに分類されます:

- [仕入先 V2 から msdyn_vendors エンティティ マッピングへ](#error-vendor-map)
- [顧客 V3 から アカウント エンティティー マッピングへ](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>仕入先 V2 のエラーを msdyn_vendors エンティティ マッピングに対して解決する

エンティティに **PrimaryContactPersonId** フィールドと **InvoiceVendorAccountNumber** フィールドの値を持つ既存レコードがある場合、**msdyn_vendors** マッピングに対して **仕入先 V2** で次のような初期同期エラーが発生する場合があります。 これは、**InvoiceVendorAccountNumber** が自己参照フィールドであり、**PrimaryContactPersonId** が仕入先マッピングで循環参照であるためです。

*フィールドの guid を解決できませんでした: <field>。検索が見つかりませんでした: <value>。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

次にいくつか例を挙げます:

- *フィールドの guid を解決できませんでした: msdyn_vendorprimarycontactperson.msdyn_contactpersonid。検索が見つかりませんでした: 000056。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *フィールドの guid を解決できませんでした: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber。検索が見つかりませんでした: V24-1。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

仕入先エンティティのこれらのフィールドに値を持つレコードがある場合は、以下のセクションの手順に従って、初期同期を正常に完了してください。

1. Finance and Operations アプリで、マッピングから **PrimaryContactPersonId** フィールドと **InvoiceVendorAccountNumber** フィールドを削除し、変更を保存します。

    1. **仕入先 V2 (msdyn_vendors)** の二重書き込みマッピング ページに移動し、**エンティティ マッピング** タブを選択します。左のフィルタで、**Finance and Operations apps.Vendors V2** を選択します。 右側のフィルターで、**Sales.Vendor** を選択します。

    2. **primarycontactperson** を検索して、ソース フィールド **PrimaryContactPersonId** を見つけます。
    
    3. **アクション** ボタンをクリックし、**削除** を選択します。
    
        ![自己参照または循環参照 3](media/vend_selfref3.png)
    
    4. 繰り返して、**InvoiceVendorAccountNumber** フィールドを削除します。
    
        ![自己参照または循環参照 4](media/vend-selfref4.png)
    
    5. マッピングの変更を保存します。

2. **仕入先 V2** エンティティの変更追跡を無効にします。

    1. **データ管理 \> データ エンティティ** に移動します。
    
    2. **仕入先 V2** エンティティを選択します。
    
    3. メニュー バーの **オプション** をクリックし、**変更の追跡** をクリックします。
    
        ![自己参照または循環参照 5](media/selfref_options.png)
    
    4. **変更の追跡を無効にする** をクリックします。
    
        ![自己参照または循環参照 6](media/selfref_tracking.png)

3. **仕入先 V2 (msdyn_vendors)** マッピングの初期同期を実行します。 初期同期はエラーなしで正常に実行されます。

4. **CDS 連絡先 V2 (contacts)** マッピングの初期同期を実行します。 連絡先レコードも初期同期する必要があるため、仕入先エンティティの "基本連絡先" フィールドを同期する場合は、このマッピングを同期する必要があります。

5. フィールド **PrimaryContactPersonId** と **InvoiceVendorAccountNumber** を **仕入先 V2 (msdyn_vendors)** マッピングに追加し直し、マッピングを保存します。

6. **仕入先 V2 (msdyn_vendors)** マッピングの初期同期を再度実行します。 変更の追跡が無効になっているため、すべてのレコードが同期されます。

7. **仕入先 V2** エンティティの変更追跡を有効にします。

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>顧客 V3 のエラーをアカウント エンティティー マッピングに対して解決する

エンティティに **ContactPersonID** フィールドと **InvoiceAccount** フィールドの値を持つ既存レコードがある場合、**アカウント** マッピングに対して **顧客 V3** で次のような初期同期エラーが発生する場合があります。 これは、**InvoiceAccount** が自己参照フィールドであり、**ContactPersonID** が仕入先マッピングで循環参照であるためです。

*フィールドの guid を解決できませんでした: <field>。検索が見つかりませんでした: <value>。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *フィールドの guid を解決できませんでした: primarycontactid.msdyn_contactpersonid。検索が見つかりませんでした: 000056。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *フィールドの guid を解決できませんでした: msdyn_billingaccount.accountnumber。検索が見つかりませんでした: 1206-1。次の URL で、参照データが存在するかどうかを確認してください: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

顧客エンティティのこれらのフィールドに値を持つレコードがある場合は、以下のセクションの手順に従って、初期同期を正常に完了してください。 この方法は、アカウントや連絡先などのすぐに利用できるエンティティに使用できます。

1. Finance and Operations アプリで、**顧客 V3 (accounts)** マッピングからフィールド **ContactPersonID** と **InvoiceAccount** を削除し、マッピングを保存します。

    1. **顧客 V3 (accounts)** の二重書き込みマッピング ページに移動し、**エンティティ マッピング** タブを選択します。左のフィルタで、**Finance and Operations apps.Customers V3** を選択します。 右側のフィルターで、**Common Data Service.Account** を選択します。

    2. **contactperson** を検索して、ソース フィールド **ContactPersonID** を見つけます。
    
    3. **アクション** ボタンをクリックし、**削除** を選択します。
    
        ![自己参照または循環参照 3](media/cust_selfref3.png)
    
    4. 繰り返して、**InvoiceAccount** フィールドを削除します。
    
        ![自己参照または循環参照](media/cust_selfref4.png)
    
    5. マッピングの変更を保存します。

2. **顧客 V3** エンティティの変更追跡を無効にします。

    1. **データ管理 \> データ エンティティ** に移動します。
    
    2. **顧客 V3** エンティティを選択します。
    
    3. メニュー バーの **オプション** をクリックし、**変更の追跡** をクリックします。
    
        ![自己参照または循環参照 5](media/selfref_options.png)
    
    4. **変更の追跡を無効にする** をクリックします。
    
        ![自己参照または循環参照 6](media/selfref_tracking.png)

3. **顧客 V3 (Accounts)** マッピングの初期同期を実行します。 初期同期はエラーなしで正常に実行されます。

4. **CDS 連絡先 V2 (contacts)** マッピングの初期同期を実行します。 同じ名前のマップが 2 つあります。 **FO.CDS Vendor Contacts V2 から CDS.Contacts への同期のための二重書き込みテンプレート。新しいパッケージ \[Dynamics365SupplyChainExtended\] が必要です。** という説明のあるものを選択します マップの **詳細** タブで。

5. **顧客 V3 (accounts)** マッピングからフィールド **InvoiceAccount** と **ContactPersonId** を追加し、マッピングを保存します。 これで、**InvoiceAccount** フィールドと **ContactPersonId** フィールドの両方がライブ同期モードの一部になりました。 次の手順では、これらのフィールドの初期同期を完了します。

6. **顧客 V3 (Accounts)** マッピングの初期同期を再度実行します。 変更の追跡が無効になっているため、同期を実行すると、**InvoiceAccount** と **ContactPersonId** のデータが Finance and Operations アプリから Common Data Service に同期されます。

7. **InvoiceAccount** と **ContactPersonId** のデータをに Common Data Service から Finance and Operations に同期するには 、データ統合プロジェクトを使用します。

    1. Power Apps で、**Sales.Account** と **Finance and Operations apps.Customers V3** エンティティの間にデータ統合プロジェクトを作成します。 データの方向は、Common Data Service から Finance and Operations アプリである必要があります。  **InvoiceAccount** は二重書き込みの新しい属性なので、この属性の初期同期をスキップすることができます。 詳細については、[Common Data Service へデータを統合](https://docs.microsoft.com/power-platform/admin/data-integrator) を参照してください。

        次の図は、**CustomerAccount** と **ContactPersonId** を更新するプロジェクトを示しています。

        ![自己参照または循環参照](media/cust_selfref6.png)

    2. Finance and Operations アプリではフィルター基準と一致するレコードのみが更新されるため、Common Data Service 側のフィルターに会社の基準を追加します。 フィルタを追加するには、[フィルタ] アイコンをクリックします。 **クエリの編集** ダイアログで、**_msdyn_company_value eq '\<guid\>'** のようなフィルター クエリを追加できます。 [フィルタ] アイコンが表示されない場合は、サポート チケットを作成して、データ統合チームにテナントのフィルター機能を有効にするよう依頼します。 **_Msdyn_company_value** のフィルター クエリを入力しない場合、すべてのレコードが同期されます。

        ![自己参照または循環参照](media/cust_selfref7.png)

        これで、レコードの初期同期が完了します。

8. Finance and Operations アプリで **顧客 V3** エンティティの変更追跡を有効にします。


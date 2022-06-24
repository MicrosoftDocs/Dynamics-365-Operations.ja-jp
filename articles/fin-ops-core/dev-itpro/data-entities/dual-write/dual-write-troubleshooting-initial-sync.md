---
title: 初めて同期をする際に発生する問題のトラブルシューティング
description: この記事では、 初めて同期をする際に発生する可能性のある問題の修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: bb3db4c651aaac521974d92753be5a8219bfe1ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892360"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>初めて同期をする際に発生する問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]



この記事では、財務と運用アプリと Dataverse 間のデュアル書き込み統合に関するトラブル シューティングの情報を提供します。 このトピックでは、 初めて同期をする際に発生する可能性のある問題の修正に役立つトラブルシューティングに特化した情報を提供します。

> [!IMPORTANT]
> この記事で説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>財務と運用アプリでの初期同期エラーの確認

マッピングのテンプレートを有効にすると、マッピングの状態が **実行中** になります。 状態が **非実行中** のとなっている場合、初回の同期中にエラーが発生しています。 エラーを表示するには、**デュアル書き込み** ページの **初回同期の詳細** タブを選択し ます。

![[初期同期の詳細] タブでのエラー。](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>初回同期を完了できません：400 要求が不正です

**問題の修正に必要な役割：** システム管理者

マッピングと初回の同期実行時に、次のメッセージが表示される場合があります。

*(\[要求が不正です\]、リモート サーバーからエラーが返されました: (400) 要求が不正です。)、AX のエクスポート中にエラーが発生しました。*

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

1. 仮想マシン (VM) にサインインし、財務と運用アプリにアクセスします。
2. Microsoft 管理コンソールを起動します。
3. **サービス** ウィンドウで、Microsoft Dynamics 365 データインポート エクスポート フレームワーク サービスが実行されていることを確認します。 初回同期が必要となるため、停止している場合は再起動してください。

## <a name="initial-synchronization-error-403-forbidden"></a>初回同期エラー： 403 権限がありません

初回の同期を実行した際に、次のエラー メッセージが表示される場合があります。

*（\[権限がありません\]、リモート サーバーからエラーが返されました：（403）権限がありません）AX のエクスポート中にエラーが発生しました*

問題を解決するには、次の手順に従います。

1. 財務と運用アプリにログインします。
2. **Azure Active Directory アプリケーション** のページで、**DtAppID** クライアントを削除し、再度追加します。

![Azure AD アプリケーションの一覧の DtAppID クライアント。](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>初回の同期中の自己参照または循環参照エラー

いずれかのマッピングに自己参照または循環参照がある場合、次のようなエラーメッセージが表示されることがあります。 エラーは次のカテゴリに分類されます:

- [仕入先 V2–to–msdyn_vendors テーブル マッピングでのエラー](#error-vendor-map)
- [顧客 V3–to–Accounts テーブル マッピングでのエラー](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>仕入先 V2–to–msdyn_vendors テーブル マッピングでのエラーを解決する

テーブルに **PrimaryContactPersonId** 列と **InvoiceVendorAccountNumber** 列の値を持つ既存の行がある場合、**msdyn\_vendors** に対して **仕入先 V2** のマッピングで初期同期エラーが発生する場合があります。 これらのエラーの発生は、**InvoiceVendorAccountNumber** が自己参照列であり、**PrimaryContactPersonId** が仕入先マッピングで循環参照であるためです。

表示されるエラーメッセージの形式は次のとおりです。

*フィールド \<field\> のガイドを解決できませんでした。検索で \<value\> は見つかりませんでした。次の URL で、参照データが存在するかどうかを確認してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

次にいくつか例を挙げます。

- *フィールド msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid のガイドを解決できませんでした。検索で 000056 は見つかりませんでした。次の URL で、参照データが存在するかどうかを確認してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *フィールド msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber のガイドを解決できませんでした。検索で V24-1 は見つかりませんでした。参照データが存在するかどうかは次の URL を試してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

仕入先テーブルの任意の行に **PrimaryContactPersonId** 列と **InvoiceVendorAccountNumber** 列がある場合、以下のステップの手順に従って、初期同期を正常に完了してください。

1. 財務と運用アプリで、マッピングから **PrimaryContactPersonId** 列と **InvoiceVendorAccountNumber** 列を削除し、マッピングを保存します。

    1. **仕入先 V2 (msdyn\_vendors)** のデュアル書き込みマッピング ページで、左のフィールドにある **テーブル マッピング** タブで、**Finance and Operations apps.Vendors V2** を選択します。 右側のフィルターで、**Sales.Vendor** を選択します。
    2. **primarycontactperson** を検索して、**PrimaryContactPersonId** ソース列を見つけます。
    3. **アクション** を選択し、**削除** を選択します。

        ![PrimaryContactPersonId 列を削除します。](media/vend_selfref3.png)

    4. これらの手順を繰り返して、**InvoiceVendorAccountNumber** 列を削除します。

        ![InvoiceVendorAccountNumber 列を削除します。](media/vend-selfref4.png)

    5. マッピングへの変更を保存します。

2. **仕入先 V2** テーブルの Change Tracking をオフにします。

    1. **データ管理** ワークスペースで、**データ テーブル** タイルを選択します。
    2. **仕入先 V2** テーブルを選択します。
    3. 操作ウィンドウで、**オプション** を選択し、**Change Tracking** を選択します。

        ![Change Tracking オプションを選択します。](media/selfref_options.png)

    4. **Change Tracking を無効にする** を選択します。

        ![Change Tracking を無効にするを選択します。](media/selfref_tracking.png)

3. **仕入先 V2 (msdyn\_vendors)** マッピングの初期同期を実行します。 初期同期はエラーなしで正常に実行されます。
4. **CDS 連絡先 V2 (連絡先)** マッピングの初期同期を実行します。 連絡先行に対しても初期同期する必要があるため、仕入先テーブルの基本連絡先列を同期する場合は、このマッピングを同期する必要があります。
5. **PrimaryContactPersonId** 列と **InvoiceVendorAccountNumber** 列を **仕入先 V2 (msdyn\_vendors)** マッピングに追加し直し、マッピングを保存します。
6. **仕入先 V2 (msdyn\_vendors)** マッピングの初期同期を再度実行します。 Change Tracking がオフになっているため、すべての行が同期されます。
7. **仕入先 V2** テーブルの Change Tracking をオフにし直します。

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>顧客 V3–to–Accounts テーブル マッピングでエラーを解決する

テーブルに **ContactPersonID** 列と **InvoiceAccount** 列の値を持つ既存の行がある場合、**アカウント** に対して **顧客 V3** のマッピングで初期同期エラーが発生する場合があります。 これらのエラーは、**InvoiceAccount** が自己参照列であり、**ContactPersonID** が仕入先マッピングで循環参照であるためです。

表示されるエラーメッセージの形式は次のとおりです。

*フィールド \<field\> のガイドを解決できませんでした。検索で \<value\> は見つかりませんでした。次の URL で、参照データが存在するかどうかを確認してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

次にいくつか例を挙げます。

- *フィールド primarycontactid.msdyn\_contactpersonid のガイドを解決できませんでした。検索で 000056 は見つかりませんでした。次の URL で、参照データが存在するかどうかを確認してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *フィールド msdyn\_billingaccount.accountnumber のガイドを解決できませんでした。検索で 1206-1 は見つかりませんでした。次の URL で、参照データが存在するかどうかを確認してください: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

顧客テーブルの任意の行に **ContactPersonID** 列と **InvoiceAccount** 列がある場合、以下のステップの手順に従って、初期同期を正常に完了してください。 この方法は、**アカウント** と **連絡先** などの既成のテーブルに使用できます。

1. 財務と運用アプリで、**顧客 V3 (アカウント)** マッピングから **ContactPersonID** 列と **InvoiceAccount** 列を削除し、マッピングを保存します。

    1. **顧客 V3 (アカウント)** のデュアル書き込みマッピング ページにある **テーブル マッピング** タブの左のフィルタで、**Finance and Operations app.Customers V3** を選択します。 右側のフィルターで、**Dataverse.Account** を選択します。
    2. **contactperson** を検索して、**ContactPersonID** ソース列を見つけます。
    3. **アクション** を選択し、**削除** を選択します。

        ![ContactPersonID 列を削除します。](media/cust_selfref3.png)

    4. これらの手順を繰り返して、**InvoiceAccount** 列を削除します。

        ![InvoiceAccount 列を削除します。](media/cust_selfref4.png)

    5. マッピングへの変更を保存します。

2. **仕入先 V3** テーブルの Change Tracking をオフにします。

    1. **データ管理** ワークスペースで、**データ テーブル** タイルを選択します。
    2. **顧客 V3** テーブルを選択します。
    3. 操作ウィンドウで、**オプション** を選択し、**Change Tracking** を選択します。

        ![Change Tracking オプションを選択します。](media/selfref_options.png)

    4. **Change Tracking を無効にする** を選択します。

        ![Change Tracking を無効にするを選択します。](media/selfref_tracking.png)

3. **顧客 V3 (アカウント)** マッピングの初期同期を実行します。 初期同期はエラーなしで正常に実行されます。
4. **CDS 連絡先 V2 (連絡先)** マッピングの初期同期を実行します。

    > [!NOTE]
    > 同じ名前のマップが 2 つあります。 **詳細** タブで次の説明を持つマップを必ず選択してください: **FO.CDS 仕入先の連絡先 V2 から CDS.Contacts との間の同期のための二重書き込みテンプレート。新しいパッケージ \[Dynamics365SupplyChainExtended\] が必要です。**

5. **顧客 V3 (アカウント)** マッピングに **InvoiceAccount** 列と **ContactPersonId** 列を追加し直し、マッピングを保存します。 **InvoiceAccount** 列と **ContactPersonId** 列の両方が再度ライブ同期モードの一部になりました。 次の手順では、これらの列の初期同期をおこないます。
6. **顧客 V3 (アカウント)** マッピングの初期同期を再度実行します。 Change Tracking が無効になっているため、**InvoiceAccount** と **ContactPersonId** のデータが財務と運用アプリから Dataverse に同期されます。
7. **InvoiceAccount** と **ContactPersonId** のデータを Dataverse から財務と運用アプリに同期するには 、データ統合プロジェクトを使用します。

    1. Power Apps で、 **Sales.Account** と **Finance and Operations apps.Customers V3** テーブルの間にデータ統合プロジェクトを作成します。 データの方向は、Dataverse から財務と運用アプリである必要があります。 **InvoiceAccount** は二重書き込みの新しい属性なので、この属性の初期同期をスキップすることができます。 詳細については、[Dataverse へデータを統合](/power-platform/admin/data-integrator) を参照してください。

        次の図は、**CustomerAccount** と **ContactPersonId** を更新するプロジェクトを示しています。

        ![CustomerAccount と ContactPersonId を更新するためのデータ統合プロジェクト。](media/cust_selfref6.png)

    2. 財務と運用アプリではフィルター基準と一致する行のみが更新されるため、Dataverse 側のフィルターに会社の基準を追加します。 フィルタを追加するには、[フィルタ] ボタンを選択します。 その後、**クエリの編集** ダイアログ ボックスで、**\_msdyn\_company\_value eq '\<guid\>'** のようなフィルター クエリを追加できます。

        > [注記] フィルタ― ボタンが表示されない場合は、サポート チケットを作成して、データ統合チームにテナントのフィルター機能を有効にするよう依頼します。

        **\_msdyn\_company\_value** のフィルター クエリを入力しない場合、すべての行が同期されます。

        ![フィルタ クエリを追加します。](media/cust_selfref7.png)

    行の初期同期が完了しました。

8. 財務と運用アプリで、**顧客 V3** テーブルの Change Tracking をオンにし直します。

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>10 以上のルックアップ フィールドを持つマップでの初期同期に失敗した場合

**顧客 V3 - アカウント**、**販売注文**、または 10 以上のルックアップ フィールドを持つマップで初期同期を実行しようとする場合、失敗して次のエラー メッセージが表示される場合があります:

*CRMExport: パッケージの実行が完了しました。エラーの説明5 https://xxxxx//datasets/yyyyy/tables/accounts/items?$select=accountnumber, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq 'id')&$orderby=accountnumber asc からデータを取得しようとしましたが失敗しました。*

クエリのルックアップの制限により、エンティティ マッピングに 10 件以上のルックアップが含まれている場合、初期同期が失敗します。 詳細については、[クエリで関連エンティティ レコードを取得する](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query)を参照してください。

この問題を解決するには、次の手順に従います:

1. ルックアップの数が 10 以下になるように、オプションのルックアップ フィールドを二重書き込みエンティティ マップから削除します。
2. マップを保存し、初期同期を実行します。
3. 最初の手順の初期同期が正常に完了したら、残りのルックアップ フィールドを追加し、最初の手順で同期したルックアップ フィールドを削除します。 ルックアップ フィールドの数が 10 以下であることを確認します。 マップを保存し、初期同期を実行します。
4. すべてのルックアップ フィールドが同期されるまで、これらの手順を繰り返します。
5. すべてのルックアップ フィールドをマップに戻し、マップを保存し、**初期同期をスキップ** してマップを実行します。

このプロセスにより、マップでライブ同期モードが有効になります。

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>当事者郵便番号と当事者電子住所の初期同期中の既知の問題

当事者の郵便番号と当事者の電子住所の初期同期を実行しようとする場合に、以下のエラー メッセージが表示される場合があります:

*当事者番号が Dataverse で見つかりませんでした。*

**個人** と **組織** タイプの当事者をフィルタ処理するため、財務と運用アプリで **DirPartyCDSEntity** に範囲が指定されています。 その結果、**CDS 当事者 - msdyn_parties** マッピングの初期同期は、**法人** や **作業単位** など、他のタイプの当事者とは同期しません。 **CDS 関係者の郵便番号 (msdyn_partypostaladdresses)** または **関係者の連絡先V3 (msdyn_partyelectronicaddresses)** で初期同期を実行するとき、エラーを受け取る可能性があります。

すべてのタイプの関係者が Dataverse に正常に同期するために、Finance and Operations エンティティで当事者タイプの範囲を削除するよう修正中です。

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>顧客または連絡先データの初期同期を実行する際のパフォーマンスに問題がありますか?

**顧客** データの初期同期を実行し、**顧客** マップを実行中で、**連絡先** データの初期同期を実行しているなら、**顧客** 住所の **LogisticsPostalAddress** や **LogisticsElectronicAddress** テーブルへの挿入および更新時にパフォーマンスに問題が発生する可能性があります。 **CustCustomerV3Entity** と **VendVendorV2Entity** では同じグローバル郵便住所と電子アドレス テーブルが追跡されており、二重書き込みによって、データを他方の側に書き込むクエリをさらに作成しようとします。 **顧客** の初期同期を既に実行している場合は、**連絡先** データの初期同期を実行している間は対応するマップを停止してください。 同じ作業を **仕入先** データに行います。 初期同期が完了したら、すべてのマップを初期同期をスキップして実行できます。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

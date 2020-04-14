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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172717"
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

## <a name="self-reference-failures-during-initial-synchronization"></a>初回の同期中の自己参照エラー

いずれかのマッピングに自己参照が含まれている場合は、次のようなエラーメッセージが表示されることがあります。

*ベンダー V2 で、次のエラーが発生しました： レコード ID： 新しいレコード、ErrorMessage： フィールドの guid を解決できませんでした： msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber。ルックアップ値が見つかりませんでした： CN-001。次の URL で、参照データが存在するかどうかを確認してください：`https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

このタイプのエラーは、自己参照を持つマッピングの初回同期中に発生します。 上記の例では、請求元仕入先フィールドは、仕入先エンティティを参照します。

この問題を解決するには、場合によっては初回の同期が成功する前にマッピングを 2 回実行する必要があります。


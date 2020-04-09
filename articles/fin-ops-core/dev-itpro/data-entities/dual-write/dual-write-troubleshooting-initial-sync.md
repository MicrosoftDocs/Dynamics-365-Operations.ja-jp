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
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="755b8-103">初めて同期をする際に発生する問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="755b8-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="755b8-104">このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="755b8-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="755b8-105">このトピックでは、 初めて同期をする際に発生する可能性のある問題の修正に役立つトラブルシューティングに特化した情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="755b8-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="755b8-106">このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="755b8-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="755b8-107">各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。</span><span class="sxs-lookup"><span data-stu-id="755b8-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="755b8-108">Finance and Operations アプリの初回の同期エラーを確認します</span><span class="sxs-lookup"><span data-stu-id="755b8-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="755b8-109">マッピングのテンプレートを有効にすると、マッピングの状態が **実行中** になります。</span><span class="sxs-lookup"><span data-stu-id="755b8-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="755b8-110">状態が **非実行中** のとなっている場合、初回の同期中にエラーが発生しています。</span><span class="sxs-lookup"><span data-stu-id="755b8-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="755b8-111">エラーを表示するには、**デュアル書き込み** ページの **初回同期の詳細** タブを選択し ます。</span><span class="sxs-lookup"><span data-stu-id="755b8-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![初回同期の詳細タブ](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="755b8-113">初回同期を完了できません：400 要求が不正です</span><span class="sxs-lookup"><span data-stu-id="755b8-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="755b8-114">**問題の修正に必要な役割：** システム管理者</span><span class="sxs-lookup"><span data-stu-id="755b8-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="755b8-115">マッピングと初回の同期実行時に、次のメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="755b8-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="755b8-116">*リモート サーバーからエラーが返されました：（400）要求が不正です。 AX のエクスポート中にエラーが発生しました*</span><span class="sxs-lookup"><span data-stu-id="755b8-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="755b8-117">次に、完全なエラー メッセージの例を示します。</span><span class="sxs-lookup"><span data-stu-id="755b8-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="755b8-118">このエラーが継続して発生し、初回同期を完了できない場合は、次の手順に従って問題を修正してください。</span><span class="sxs-lookup"><span data-stu-id="755b8-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="755b8-119">Finance and Operations アプリの仮想マシン（VM）にサイン インします。</span><span class="sxs-lookup"><span data-stu-id="755b8-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="755b8-120">Microsoft 管理コンソールを起動します。</span><span class="sxs-lookup"><span data-stu-id="755b8-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="755b8-121">**サービス** ウィンドウで、Microsoft Dynamics 365 データインポート エクスポート フレームワーク サービスが実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="755b8-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="755b8-122">初回同期が必要となるため、停止している場合は再起動してください。</span><span class="sxs-lookup"><span data-stu-id="755b8-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="755b8-123">初回同期エラー： 403 権限がありません</span><span class="sxs-lookup"><span data-stu-id="755b8-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="755b8-124">初回の同期を実行した際に、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="755b8-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="755b8-125">*（\[権限がありません\]、リモート サーバーからエラーが返されました：（403）権限がありません）AX のエクスポート中にエラーが発生しました*</span><span class="sxs-lookup"><span data-stu-id="755b8-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="755b8-126">問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="755b8-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="755b8-127">Finance and Operations アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="755b8-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="755b8-128">**Azure Active Directory アプリケーション** のページで、**DtAppID** クライアントを削除し、再度追加します。</span><span class="sxs-lookup"><span data-stu-id="755b8-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD アプリケーションのリスト](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="755b8-130">初回の同期中の自己参照エラー</span><span class="sxs-lookup"><span data-stu-id="755b8-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="755b8-131">いずれかのマッピングに自己参照が含まれている場合は、次のようなエラーメッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="755b8-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="755b8-132">*ベンダー V2 で、次のエラーが発生しました： レコード ID： 新しいレコード、ErrorMessage： フィールドの guid を解決できませんでした： msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber。ルックアップ値が見つかりませんでした： CN-001。次の URL で、参照データが存在するかどうかを確認してください：`https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="755b8-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="755b8-133">このタイプのエラーは、自己参照を持つマッピングの初回同期中に発生します。</span><span class="sxs-lookup"><span data-stu-id="755b8-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="755b8-134">上記の例では、請求元仕入先フィールドは、仕入先エンティティを参照します。</span><span class="sxs-lookup"><span data-stu-id="755b8-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="755b8-135">この問題を解決するには、場合によっては初回の同期が成功する前にマッピングを 2 回実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="755b8-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>


---
title: Finance and Operations アプリのアップグレードで生じる問題のトラブルシューティング
description: このトピックでは、Finance and Operations アプリの更新に関する問題の修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 97509ac662fad6181cbd60e5e0a44f674410acb9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754041"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="9059d-103">Finance and Operations アプリのアップグレードで生じる問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="9059d-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="9059d-104">このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="9059d-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="9059d-105">このトピックでは、Finance and Operations アプリの更新に関する問題の修正に役立つトラブルシューティングに特化した情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="9059d-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9059d-106">このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="9059d-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="9059d-107">各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。</span><span class="sxs-lookup"><span data-stu-id="9059d-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="9059d-108">データベース同期のエラー</span><span class="sxs-lookup"><span data-stu-id="9059d-108">Database synchronization errors</span></span>

<span data-ttu-id="9059d-109">**問題の修正に必要な役割：** システム管理者</span><span class="sxs-lookup"><span data-stu-id="9059d-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="9059d-110">**DualWriteProjectConfiguration** テーブルを使用して、Platform update 30 に Finance and Operations アプリを更新すると、次の例のようなエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="9059d-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="9059d-111">問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9059d-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="9059d-112">Finance and Operations アプリの仮想マシン（VM）にサイン インします。</span><span class="sxs-lookup"><span data-stu-id="9059d-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="9059d-113">Visual Studio を管理者で起動し、アプリケーション オブジェクト ツリー（AOT）を開きます。</span><span class="sxs-lookup"><span data-stu-id="9059d-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="9059d-114">**DualWriteProjectConfiguration** を検索します。</span><span class="sxs-lookup"><span data-stu-id="9059d-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="9059d-115">AOT で、**DualWriteProjectConfiguration** を右クリックし、**新しいプロジェクトに追加する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9059d-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="9059d-116">**OK** を選択すると、既定のオプションを使用した新たなプロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="9059d-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="9059d-117">ソリューション エクスプローラーで、 **プロジェクトのプロパティ** を右クリックし、 **ビルド時にデータベースを同期する** を **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9059d-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="9059d-118">プロジェクトをビルドし、ビルドが成功したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="9059d-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="9059d-119">**Dynamics 365** メニューで、**データベースの同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9059d-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="9059d-120">データベース全体の同期を実行するには、**同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9059d-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="9059d-121">データベース全体の同期処理が正常に完了した後で、Microsoft Dynamics Lifecycle Services（LCS）でデータベースの同期を再実行し、必要に応じて手動アップグレードスクリプトを使用して、更新を進めることができます。</span><span class="sxs-lookup"><span data-stu-id="9059d-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="9059d-122">マップに存在しないテーブル列の問題</span><span class="sxs-lookup"><span data-stu-id="9059d-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="9059d-123">**問題の修正に必要な役割：** システム管理者</span><span class="sxs-lookup"><span data-stu-id="9059d-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="9059d-124">**デュアル書き込み** ページでは、次のようなエラーメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="9059d-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="9059d-125">*スキーマ内の存在しないソース フィールド \<field name\>。*</span><span class="sxs-lookup"><span data-stu-id="9059d-125">*Missing source field \<field name\> in the schema.*</span></span>

![存在しないソース列のエラー メッセージの例](media/error_missing_field.png)

<span data-ttu-id="9059d-127">この問題を解決するには、まず次の手順に従って、列がテーブルに含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9059d-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="9059d-128">Finance and Operations アプリの VM にログインします。</span><span class="sxs-lookup"><span data-stu-id="9059d-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="9059d-129">**ワークスペース \> データ管理** に移動して、**フレームワーク パラメーター** タイルを選択し、**テーブルの設定** タブにて、**テーブル リストの更新** を選択してテーブルを更新します。</span><span class="sxs-lookup"><span data-stu-id="9059d-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="9059d-130">**ワークスペース \> データ管理** に移動し、**データ テーブル** タブを選択して、テーブルが一覧表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9059d-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="9059d-131">テーブルが一覧に表示されない場合は、Finance and Operations アプリの VM にサインインして、テーブルが使用可能となっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9059d-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="9059d-132">Finance and Operations アプリにて **デュアル書き込み** ページの **テーブル マッピング** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="9059d-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="9059d-133">**テーブル リストの更新** を選択すると、テーブル マッピングの列が自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="9059d-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="9059d-134">問題が解決しない場合は、次の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="9059d-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9059d-135">これらの手順では、テーブルを削除してから再度追加するプロセスを示します。</span><span class="sxs-lookup"><span data-stu-id="9059d-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="9059d-136">問題を回避するには、手順を正確に守ってください。</span><span class="sxs-lookup"><span data-stu-id="9059d-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="9059d-137">Finance and Operations アプリで、**ワークスペース \> データ管理** に移動し、**データ テーブル** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9059d-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="9059d-138">属性が欠落しているテーブルを検索します。</span><span class="sxs-lookup"><span data-stu-id="9059d-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="9059d-139">ツールバーの **ターゲット マッピングの変更** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9059d-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="9059d-140">**ステージングをターゲットにマッピング** ウィンドウで、**マッピングの生成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9059d-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="9059d-141">Finance and Operations アプリにて **デュアル書き込み** ページの **テーブル マッピング** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="9059d-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="9059d-142">マッピング上で属性が自動設定されていない場合は、**属性の追加** ボタンをクリックして手動で追加し、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9059d-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="9059d-143">マッピングを選択し、**実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9059d-143">Select the map and click **Run**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
---
title: ライブ同期に関する問題のトラブルシューティング
description: このトピックでは、ライブ同期の問題修正に役立つトラブルシューティング情報を提供します。
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
ms.openlocfilehash: 1c0dfebb3ef442f67d8489d7aed00305c02cf410
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748900"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="27fb2-103">ライブ同期に関する問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="27fb2-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="27fb2-104">このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="27fb2-105">このトピックでは、ライブ同期の問題修正に役立つトラブルシューティングに特化した情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27fb2-106">このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="27fb2-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="27fb2-107">各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。</span><span class="sxs-lookup"><span data-stu-id="27fb2-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="27fb2-108">Finance and Operations アプリで行を作成すると、ライブ同期で 403 Forbidden エラーが発生する</span><span class="sxs-lookup"><span data-stu-id="27fb2-108">Live synchronization throws a 403 Forbidden error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="27fb2-109">Finance and Operations アプリで行を作成した際に、次のエラー メッセージが表示される場合があります:</span><span class="sxs-lookup"><span data-stu-id="27fb2-109">You might receive the following error message when you create a row in a Finance and Operations app:</span></span>

<span data-ttu-id="27fb2-110">*\[{\\"エラー\\"：{\\"コード\\"：\\"0x 80072560\\"、\\"メッセージ\\"：\\"ユーザーは組織のメンバではありません。\\}}\]、リモートサーバーからエラーが返されました：（403）権限がありません。"}}"*</span><span class="sxs-lookup"><span data-stu-id="27fb2-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="27fb2-111">この問題を修正するには、[システム要件と前提条件](requirements-and-prerequisites.md) に記載されている手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="27fb2-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="27fb2-112">これらの手順を完了するには、Dataverse で作成したデュアル書き込みアプリケーションのユーザーにシステム管理者ロールが割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="27fb2-112">To complete those steps, the dual-write application users who are created in Dataverse must have the system admin role.</span></span> <span data-ttu-id="27fb2-113">また、既定の所有チームにシステム管理者ロールが割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="27fb2-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="27fb2-114">Finance and Operations アプリで行を作成時に、テーブルのライブ同期では、常に同様のエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="27fb2-114">Live synchronization for any table consistently throws a similar error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="27fb2-115">**問題の修正に必要な役割：** システム管理者</span><span class="sxs-lookup"><span data-stu-id="27fb2-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="27fb2-116">テーブル データを Finance and Operations アプリに保存するたびに、次のようなエラー メッセージが表示される場合があります:</span><span class="sxs-lookup"><span data-stu-id="27fb2-116">You might receive an error message like the following every time that you try to save table data in a Finance and Operations app:</span></span>

<span data-ttu-id="27fb2-117">*データベースへの変更を保存できません。作業単位で取引をコミットすることはできません。エンティティ uoms にデータを書き込むことができません。UnitOfMeasureEntity への書き込みが失敗し、次のエラーメッセージが表示されました。エンティティ uoms と同期することはできません。*</span><span class="sxs-lookup"><span data-stu-id="27fb2-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="27fb2-118">問題を修正するには、前提条件となる参照データが Finance and Operations アプリと Dataverse の両方に存在していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27fb2-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Dataverse.</span></span> <span data-ttu-id="27fb2-119">たとえば、Finance and Operations アプリで作業している顧客が特定の顧客グループに属している場合は、その顧客グループが Dataverse に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Dataverse.</span></span>

<span data-ttu-id="27fb2-120">データが両面に存在し、問題がデータに起因するものではないことが分かった場合は、次の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="27fb2-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="27fb2-121">関連するテーブルを停止します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-121">Stop the related table.</span></span>
2. <span data-ttu-id="27fb2-122">Finance and Operations アプリにサインインし、失敗したテーブルの行が DualWriteProjectConfiguration テーブルと DualWriteProjectFieldConfiguration テーブルに存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-122">Sign in to the Finance and Operations app, and make sure that rows for the failing table exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="27fb2-123">たとえば、**顧客** テーブルに障害が発生した場合、クエリは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="27fb2-123">For example, here is what the query looks like if the **Customers** table is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="27fb2-124">テーブルのマッピングを停止しても、失敗したテーブルの行が存在する場合は、失敗したテーブルに関連する行を削除してください。</span><span class="sxs-lookup"><span data-stu-id="27fb2-124">If there are rows for the failing table even after you stop the table mapping, delete the rows that are related to the failing table.</span></span> <span data-ttu-id="27fb2-125">DualWriteProjectConfiguration テーブルの **projectname** 列をメモし、プロジェクト名を使用して行を削除することで、DualWriteProjectFieldConfiguration テーブル内の行をフェッチします。</span><span class="sxs-lookup"><span data-stu-id="27fb2-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the row in the DualWriteProjectFieldConfiguration table by using the project name to delete the row.</span></span>
4. <span data-ttu-id="27fb2-126">テーブルのマッピングを開始します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-126">Start the table mapping.</span></span> <span data-ttu-id="27fb2-127">データが問題なく同期されていることを検証してください。</span><span class="sxs-lookup"><span data-stu-id="27fb2-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="27fb2-128">Finance and Operations アプリにデータを作成する際の、読み取り、書き込み権限に関するエラーを処理する</span><span class="sxs-lookup"><span data-stu-id="27fb2-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="27fb2-129">Finance and Operationsアプリでデータを作成する際に、次のような "要求が不正です" というエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="27fb2-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![不正な要求のエラー メッセージの例](media/error_record_id_source.png)

<span data-ttu-id="27fb2-131">この問題を修正するには、マッピングされた Dynamics 365 Sales または Dynamics 365 Customer Service の部署のチームに適切なセキュリティロールを割り当てて、不足している権限を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27fb2-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="27fb2-132">Finance and Operations アプリで、データ統合の接続セットにマッピングされている事業単位を検索します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![組織のマッピング](media/mapped_business_unit.png)

2. <span data-ttu-id="27fb2-134">Dynamics 365 のモデル駆動型アプリケーションの環境にログインし、**設定 \> セキュリティ** に移動し、マッピングされた事業単位のチームを検索します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![マッピングされた事業単位のチーム](media/setting_security_page.png)

3. <span data-ttu-id="27fb2-136">編集をするチームのページを開き、 **ロールの管理** を選択して、**チームロールの管理** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="27fb2-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![ロールの管理ボタン](media/manage_team_roles.png)

4. <span data-ttu-id="27fb2-138">関連するテーブルに対する読み取り/書き込み権限を持つロールの割り当てを行い、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-138">Assign the role that has the read/write privilege for the relevant tables, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a><span data-ttu-id="27fb2-139">最近変更された Dataverse 環境の存在する環境にて、同期の問題を修正する</span><span class="sxs-lookup"><span data-stu-id="27fb2-139">Fix synchronization issues in an environment that has a recently changed Dataverse environment</span></span>

<span data-ttu-id="27fb2-140">**問題の修正に必要な役割：** システム管理者</span><span class="sxs-lookup"><span data-stu-id="27fb2-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="27fb2-141">Finance and Operations アプリでデータを作成した際に、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="27fb2-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="27fb2-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**エンティティ CustCustomerV3Entity のペイロードを生成できません。**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":" ペイロードの作成に失敗しました。エラー 無効な URI です：URI が入力されていません。}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="27fb2-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="27fb2-143">Dynamics 365 のモデル駆動アプリでは、次のようにエラーが表示されます：</span><span class="sxs-lookup"><span data-stu-id="27fb2-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="27fb2-144">*ISV コードに起因する予期しないエラーが発生しました。（ErrorType = ClientError）プラグイン（実行）に起因する予期しない例外が発生しました。Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: エンティティ アカウントの処理に失敗しました ―（接続先が一定期間応答しなかったために接続に失敗したか、接続ホストが応答しなかったために確立された接続が失敗しました*</span><span class="sxs-lookup"><span data-stu-id="27fb2-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="27fb2-145">このエラーは、Finance and Operations アプリでのデータ作成時に、Dataverse 環境が正しくリセットされていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-145">This error occurs when the Dataverse environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="27fb2-146">問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="27fb2-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="27fb2-147">Finance and Operations 仮想マシン (VM) にサインインし、SQL Server Management Studio (SSMS) を起動し、DUALWRITEPROJECTCONFIGURATIONENTITY テーブルにて、**internalentityname** が **顧客 V3**、かつ **externalentityname** が **アカウント** となっている行を探してください。</span><span class="sxs-lookup"><span data-stu-id="27fb2-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for rows in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="27fb2-148">以下にクエリの例を示します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="27fb2-149">前のクエリの結果からプロジェクト名を使用して、次のクエリを実行してください。</span><span class="sxs-lookup"><span data-stu-id="27fb2-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="27fb2-150">**externalenvironmentURL** の列に、正しい Dataverse またはアプリの URL が設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="27fb2-150">Make sure that the **externalenvironmentURL** column has the correct Dataverse or app URL.</span></span> <span data-ttu-id="27fb2-151">誤った Dataverse の URL を指している重複行を削除します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-151">Delete any duplicate rows that point to the wrong Dataverse URL.</span></span> <span data-ttu-id="27fb2-152">DUALWRITEPROJECTFIELDCONFIGURATION テーブルと DUALWRITEPROJECTCONFIGURATION テーブルにて該当する行を削除します。</span><span class="sxs-lookup"><span data-stu-id="27fb2-152">Delete the corresponding rows in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="27fb2-153">テーブルのマッピングを停止して、再起動してください</span><span class="sxs-lookup"><span data-stu-id="27fb2-153">Stop the table mapping, and then restart it</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
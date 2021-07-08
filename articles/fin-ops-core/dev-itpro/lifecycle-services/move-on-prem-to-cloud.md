---
title: LCS 実装プロジェクトをオンプレミスからクラウドに移動する
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) 環境をクラウドに移行する方法について説明します。
author: MartinWalkerDynSA
ms.date: 02/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: marwalke
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4c4f731b987c1d9e0e62f435e8e7a5bb651026b7
ms.sourcegitcommit: c9f55e64416d0bbedfdadafb00e4181921ad0f37
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261926"
---
# <a name="move-lcs-implementation-projects-from-on-premises-to-the-cloud"></a><span data-ttu-id="43846-103">LCS 実装プロジェクトをオンプレミスからクラウドに移動する</span><span class="sxs-lookup"><span data-stu-id="43846-103">Move LCS implementation projects from on-premises to the cloud</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43846-104">このトピックでは、独自のインフラストラクチャでホストされている Microsoft Dynamics 365 Finance + Operations (オンプレミス) 環境を Azure クラウドに移動する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="43846-104">This topic explains how to move your Microsoft Dynamics 365 Finance + Operations (on-premises) environments that are hosted on your own infrastructure to the Azure cloud.</span></span>

## <a name="cloud-subscription-licenses"></a><span data-ttu-id="43846-105">クラウド サブスクリプション ライセンス</span><span class="sxs-lookup"><span data-stu-id="43846-105">Cloud subscription licenses</span></span>

<span data-ttu-id="43846-106">クラウド サブスクリプション ライセンスをまだお持ちでない場合は、クラウド サービス プロバイダーまたはボリューム ライセン スリセラーと協力して、 Azure Active Directory (Azure AD) テナントで必要なサブスクリプションを取得してアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="43846-106">If you don't already have cloud subscription licenses, work with your cloud service provider or volume license reseller to get and activate the required subscriptions on your Azure Active Directory (Azure AD) tenant.</span></span> <span data-ttu-id="43846-107">ユーザーおよびアドオン環境のすべてのサブスクリプションを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-107">All subscriptions for users and add-on environments must be activated.</span></span>

## <a name="configure-lcs-cloud-implementation-project"></a><span data-ttu-id="43846-108">LCS クラウドの実装プロジェクトを構成する</span><span class="sxs-lookup"><span data-stu-id="43846-108">Configure LCS cloud implementation project</span></span>

<span data-ttu-id="43846-109">以前に Azure AD テナントで Finance and Operations クラウド名のユーザー サブスクリプション ライセンスがアクティブ化されていない場合、新しい Microsoft Dynamics Lifecycle Services (LCS) クラウド実装プロジェクトが自動的にプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="43846-109">If no Finance and Operations cloud-named user subscription licenses have previously been activated on the Azure AD tenant, a new Microsoft Dynamics Lifecycle Services (LCS) cloud implementation project is automatically provisioned.</span></span> <span data-ttu-id="43846-110">それ以外の場合は、サポート要求を開いて LCS クラウドの実装プロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-110">Otherwise, you must open a support request to have an LCS cloud implementation project created.</span></span> <span data-ttu-id="43846-111">詳細については、[1 つの Azure AD テナントでの複数の LCS プロジェクトと運用環境](../../fin-ops/get-started/implement-multiple-projects-aad-tenant.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43846-111">For more information, see [Multiple LCS projects and production environments on one Azure AD tenant](../../fin-ops/get-started/implement-multiple-projects-aad-tenant.md).</span></span>

<span data-ttu-id="43846-112">LCS クラウドの実装プロジェクトが作成されたら、完全に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-112">After your LCS cloud implementation project has been created, you must fully configure it.</span></span> <span data-ttu-id="43846-113">この構成の一部として、ユーザー、Azure DevOps DevOps アソシエーション、サブスクリプションの見積りを追加し、アセット ライブラリおよびビジネス プロセス モデラー (BPM) などに入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-113">As part of this configuration, you must add users, an Azure DevOps association, and subscription estimates, fill in the Asset library and Business process modeler (BPM), and more.</span></span>

> [!NOTE]
> <span data-ttu-id="43846-114">プロジェクトのオンボードしている間、ソースシステムとして **AX 2012 アップグレード** を選択する必要があります。これにより、エラスティック プールの代わりにシングルトンの Azure SQL データベースがサンドボックスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="43846-114">While you're onboarding your project, you must select **AX 2012 Upgrade** as the source system, so that a singleton Azure SQL database will be used for your sandbox instead of an elastic pool.</span></span> <span data-ttu-id="43846-115">最終的には、オンプレミスの **Finance and Operations** など、より適切なオプションが利用可能となります。</span><span class="sxs-lookup"><span data-stu-id="43846-115">Eventually, a more appropriate option will be available, such as **On-premises Finance and Operations**.</span></span>

## <a name="complete-development-and-testing-of-updated-integrations"></a><span data-ttu-id="43846-116">更新された統合の開発とテストの完了</span><span class="sxs-lookup"><span data-stu-id="43846-116">Complete development and testing of updated integrations</span></span>

<span data-ttu-id="43846-117">おそらく、Finance + Operations (オンプレミス) 環境とのインターフェイスに使用した統合デザイン パターンにいくつかの変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-117">You will probably have to make some changes to the integration design patterns that you used for interfaces with your Finance + Operations (on-premises) environment.</span></span> <span data-ttu-id="43846-118">これらの変更はかなりのものになる可能性があり、それらの詳細な説明はこのトピックの範囲を超えています。</span><span class="sxs-lookup"><span data-stu-id="43846-118">These changes can be substantial, and a detailed discussion of them is beyond the scope of this topic.</span></span> <span data-ttu-id="43846-119">ただし、すべてのインターフェイスを評価して、それらに適切な変更を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-119">Nevertheless, you must evaluate all your interfaces and make the appropriate changes to them.</span></span>

<span data-ttu-id="43846-120">元のインターフェースと同じコードベースで共存できるように、更新されたインターフェースを開発することを検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-120">You should consider developing your updated interfaces in such a way that they can coexist in the same code base as the original interfaces.</span></span> <span data-ttu-id="43846-121">このアプローチにより、オンプレミスからクラウドへの移行期間中のコード ライフサイクル管理が簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="43846-121">This approach will simplify code lifecycle management during the period of your transition from on-premises to cloud.</span></span> <span data-ttu-id="43846-122">このアプローチが不可能な場合は、クラウドの運用開始を通じて新しい開発ブランチを管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-122">If this approach isn't possible, you must manage a new development branch through your cloud go-live.</span></span> <span data-ttu-id="43846-123">移行期間中のこの新しいブランチの管理を簡素化するために、他のコード変更を可能な限り凍結することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="43846-123">To simplify management of this new branch during the transition period, we recommend that you freeze other code changes as much as you can.</span></span> <span data-ttu-id="43846-124">さらに、詳細なカットオーバー計画では、古いインターフェイスを無効にし、新しいインターフェイスを有効化する手順を慎重に文書化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-124">Additionally, in your detailed cut-over plan, you should carefully document the steps for inactivating your old interfaces and activating the new interfaces.</span></span>

## <a name="do-a-trial-migration-and-resolve-issues"></a><span data-ttu-id="43846-125">試用版の移行を実行し、問題を解決する</span><span class="sxs-lookup"><span data-stu-id="43846-125">Do a trial migration and resolve issues</span></span>

1. <span data-ttu-id="43846-126">階層 2 環境を展開します。</span><span class="sxs-lookup"><span data-stu-id="43846-126">Deploy a tier-2 environment.</span></span>
2. <span data-ttu-id="43846-127">オンプレミスの運用環境 (または、必要に応じて、前のセクションで説明したクラウド統合開発ブランチからの現在のビルド) に適用されるのと同じコード パッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="43846-127">Apply the same code package that is applied in your on-premises production environment (or, as appropriate, in the current build from the cloud integration development branch that was discussed in the previous section).</span></span> <span data-ttu-id="43846-128">このコード パッケージは、独立系ソフトウェア ベンダー (ISV) のソリューションとライセンスを含む単一の完全な展開可能なパッケージである必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-128">This code package should be a single, complete deployable package that includes any independent software vendor (ISV) solutions and licenses.</span></span>
3. <span data-ttu-id="43846-129">SQL Server Management Studio (SSMS) では、サンドボックス データベースに対して次の Transact-SQL (T-SQL) コマンドを実行し、現在の管理者アカウントと Azure AD テナント ID 情報、およびデータ管理フレームワーク (DMF) 共有作業ディレクトリをそのデータベースに保持します。</span><span class="sxs-lookup"><span data-stu-id="43846-129">In SQL Server Management Studio (SSMS), run the following Transact-SQL (T-SQL) commands against the sandbox database to preserve the current Admin account, Azure AD tenant ID information, and Data management framework (DMF) shared working directory in that database.</span></span> <span data-ttu-id="43846-130">結果を保存します。</span><span class="sxs-lookup"><span data-stu-id="43846-130">Save the results.</span></span>

    ```sql
    SELECT SID,NETWORKALIAS,NETWORKDOMAIN,IDENTITYPROVIDER from USERINFO WHERE ID = 'Admin'
    SELECT VALUE from SYSSERVICECONFIGURATIONSETTING where name = 'TENANTID'
    SELECT TENANTID from POWERBICONFIG
    SELECT TENANTID from PROVISIONINGMESSAGETABLE
    SELECT TENANTID from B2BINVITATIONCONFIG
    SELECT TENANTID from RETAILSHAREDPARAMETER
    SELECT SHAREDFOLDERPATH from DMFPARAMETERS
    ```

4. <span data-ttu-id="43846-131">データベースをオンプレミスからオンラインにコピーします。</span><span class="sxs-lookup"><span data-stu-id="43846-131">Copy the database from on-premises to online.</span></span> <span data-ttu-id="43846-132">使用するエクスポートとインポートのプロセスは、[ゴールデン構成プロモーション](../database/dbmovement-scenario-goldenconfig.md) データベースの移動チュートリアルで説明されているプロセスと同じです。</span><span class="sxs-lookup"><span data-stu-id="43846-132">The export and import process that you use is the same process that is described in the [Golden configuration promotion](../database/dbmovement-scenario-goldenconfig.md) database movement tutorial.</span></span> <span data-ttu-id="43846-133">ただし、この場合、ソース データベースは既存のオンプレミスの実稼動 SQL データベースであり、開発環境にインポートするために説明されている sqlpackage.exe アプローチを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-133">However, in this case, the source database is the existing on-premises production SQL database, and you must use the sqlpackage.exe approach that is described for importing into a developer environment.</span></span> <span data-ttu-id="43846-134">代わりに、LCS セルフ サービス データベース インポート オプションを使用する場合は、クリーンアップされるデータ要素に関する警告に記載されているように、一部のデータがインポートされません。</span><span class="sxs-lookup"><span data-stu-id="43846-134">If you use the LCS self-service database import option instead, some data won't be imported, as noted in the warnings about data elements that are cleaned up.</span></span> <span data-ttu-id="43846-135">次のコードに示されているプレースホルダーの代わりに、LCS 環境の詳細で使用可能なターゲット データベース情報を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-135">The target database information that is available in the LCS environment details must be used instead of the placeholders that are shown in the following code.</span></span>

    ```powershell
    SqlPackage.exe /a:import /sf:D:\BacpacToImport\my.bacpac /tsn:<Azure SQL database server> /tdn:<target database name> /tu:<axdbadmin user from LCS> /tp:<axdbadmin password from LCS> /p:CommandTimeout=1200
    ```

5. <span data-ttu-id="43846-136">管理者アカウント、Azure AD テナント ID、および、DMF 共有ディレクトリの値を復元します。</span><span class="sxs-lookup"><span data-stu-id="43846-136">Restore the Admin account, Azure AD tenant ID, and DMF shared directory values.</span></span> <span data-ttu-id="43846-137">また、**SF** スキーマとそのテーブルが存在する場合は削除します。</span><span class="sxs-lookup"><span data-stu-id="43846-137">Also remove the **SF** schema and its tables, if they are present.</span></span>

    ```sql
    UPDATE USERINFO SET SID='<preserved SID>', NETWORKALIAS='<preserved NETWORKALIAS>', NETWORKDOMAIN='<preserved NETWORKDOMAIN>', IDENTITYPROVIDER='<preserved IDENTITYPROVIDER>' WHERE ID = 'Admin'
    UPDATE SYSSERVICECONFIGURATIONSETTING set VALUE='<preserved VALUE>' where name = 'TENANTID'
    UPDATE POWERBICONFIG SET TENANTID='<preserved TENANTID>'
    UPDATE PROVISIONINGMESSAGETABLE SET TENANTID='<preserved TENANTID>'
    UPDATE B2BINVITATIONCONFIG SET TENANTID='<preserved TENANTID>'
    UPDATE RETAILSHAREDPARAMETER SET TENANTID='<preserved TENANTID>'
    UPDATE DMFPARAMETERS SET SHAREDFOLDERPATH='<preserved SHAREDFOLDERPATH>'
    DROP TABLE IF EXISTS SYNCLOG
    DROP TABLE IF EXISTS SYNCLOCK
    DROP SCHEMA IF EXISTS SF
    ```

6. <span data-ttu-id="43846-138">他のすべてのユーザーを再インポートし、適切なセキュリティ ロールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="43846-138">Reimport all other users, and assign the appropriate security roles.</span></span>
7. <span data-ttu-id="43846-139">クラウド環境での直接印刷は、ドキュメント回覧エージェント (DRA) を介して行われます。</span><span class="sxs-lookup"><span data-stu-id="43846-139">Direct printing in a cloud environment is done via the Document Routing Agent (DRA).</span></span> <span data-ttu-id="43846-140">[ネットワーク印刷を有効にしてドキュメント回覧エージェントをインストール](../analytics/install-document-routing-agent.md) の説明に従ってサンドボックス DRA を設定し、回帰テストに印刷シナリオを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="43846-140">Set up sandbox DRAs as described in [Install the Document Routing Agent to enable network printing](../analytics/install-document-routing-agent.md), so that regression testing can include your printing scenarios.</span></span>
8. <span data-ttu-id="43846-141">ドキュメント処理の添付ファイルをクラウドにコピーします。</span><span class="sxs-lookup"><span data-stu-id="43846-141">Copy document handling attachments to the cloud.</span></span> <span data-ttu-id="43846-142">ドキュメント処理の添付ファイルはデータベースに保存されません。</span><span class="sxs-lookup"><span data-stu-id="43846-142">Document handling attachments aren't stored in the database.</span></span> <span data-ttu-id="43846-143">保存する必要がある場合は、個別に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-143">If they must be preserved, you must move them separately.</span></span> <span data-ttu-id="43846-144">手順については、このトピックで後述する[サンドボックスへの添付ファイルを処理するドキュメントの移行](#migrate-document-handling-attachments-to-your-sandbox) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="43846-144">For instructions, see the [Migrate document handling attachments to your sandbox](#migrate-document-handling-attachments-to-your-sandbox) section later in this topic.</span></span>
9. <span data-ttu-id="43846-145">完全な回帰テスト サイクルを実行します。</span><span class="sxs-lookup"><span data-stu-id="43846-145">Run a complete regression test cycle.</span></span> <span data-ttu-id="43846-146">このサイクルには、統合のテストを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-146">This cycle should include testing of integrations.</span></span>
10. <span data-ttu-id="43846-147">テスト中に検出された問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="43846-147">Resolve any issues that are discovered during testing.</span></span> <span data-ttu-id="43846-148">各問題ごとに、サンドボックスで行った修正調整を文書化して追跡し、オンプレミスソースで繰り返します。</span><span class="sxs-lookup"><span data-stu-id="43846-148">For each issue, document and keep track of the correcting adjustments that you make in the sandbox, and repeat them in the on-premises source.</span></span> <span data-ttu-id="43846-149">オンプレミス環境で変更を加えてはならない場合は、その環境の正しい機能と互換性がないため、移行プロセスの繰り返しごとに手動で適用するのではなく、DMF データパッケージを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="43846-149">If any change must not be made in the on-premises environment, because it's incompatible with the correct functioning of that environment, we recommend that you create a DMF data package for it instead of manually applying it for each iteration of the migration process.</span></span>
11. <span data-ttu-id="43846-150">すべてのテストが成功し、コードまたは構成に変更が加えられなくなるまで、手順 2 ～ 10 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="43846-150">Repeat steps 2 through 10 until all tests have been passed, and no further changes are being made to code or the configuration.</span></span>

## <a name="repeat-the-migration-to-production"></a><span data-ttu-id="43846-151">実稼働への移行の繰り返し</span><span class="sxs-lookup"><span data-stu-id="43846-151">Repeat the migration to production</span></span>

1. <span data-ttu-id="43846-152">新しい運用環境を展開します。</span><span class="sxs-lookup"><span data-stu-id="43846-152">Deploy the new production environment.</span></span> <span data-ttu-id="43846-153">通常の前提条件が適用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="43846-153">Note that the regular prerequisites apply.</span></span> <span data-ttu-id="43846-154">たとえば、有効なサブスクリプションの見積もりツールが必要であり、運用フェーズの前に LCS の方法のフェーズを完了し、FastTrack 準備レビューを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-154">For example, you must have an active subscription estimator, complete the LCS methodology phases before the operate phase, and complete the FastTrack readiness review.</span></span> <span data-ttu-id="43846-155">詳細については、「[Go-Live の準備](../../fin-ops/imp-lifecycle/prepare-go-live.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43846-155">For more information, see [Prepare for go-live](../../fin-ops/imp-lifecycle/prepare-go-live.md).</span></span>
2. <span data-ttu-id="43846-156">ソフトウェア展開可能パッケージの最終バージョンを実稼働に適用します。</span><span class="sxs-lookup"><span data-stu-id="43846-156">Apply the final version of the software deployable package to production.</span></span>
3. <span data-ttu-id="43846-157">オンプレミスの運用環境に対するデータの変更を中止します。</span><span class="sxs-lookup"><span data-stu-id="43846-157">Stop making data changes to the on-premises production environment.</span></span>
4. <span data-ttu-id="43846-158">[試用版の移行と問題の解決](#do-a-trial-migration-and-resolve-issues) セクションで手順 3 ～ 6 を繰り返して、最終的な/最新のオンプレミス本番データベースをクラウド サンドボックスにコピーします。</span><span class="sxs-lookup"><span data-stu-id="43846-158">Repeat steps 3 through 6 in the [Do a trial migration and resolve issues](#do-a-trial-migration-and-resolve-issues) section to copy the final/up-to-date on-premises production database to the cloud sandbox.</span></span>
5. <span data-ttu-id="43846-159">[試用版の移行と問題の解決](#do-a-trial-migration-and-resolve-issues) セクションで手順 8 を繰り返して、添付ファイルを処理する最終/最新のドキュメントをクラウドサンドボックスにコピーします。</span><span class="sxs-lookup"><span data-stu-id="43846-159">Repeat step 8 in the [Do a trial migration and resolve issues](#do-a-trial-migration-and-resolve-issues) section to copy the final/up-to-date document handling attachments to the cloud sandbox.</span></span>
6. <span data-ttu-id="43846-160">サンドボックスから実稼働へのデータベースの更新を要求します。</span><span class="sxs-lookup"><span data-stu-id="43846-160">Request a database refresh from sandbox to production.</span></span> <span data-ttu-id="43846-161">(このプロセスは、ゴールデン構成データベースを実稼働にプロモートするために使用されるプロセスと同じです。)</span><span class="sxs-lookup"><span data-stu-id="43846-161">(The process is the same as the process that is used to promote a golden configuration database to production.)</span></span>
7. <span data-ttu-id="43846-162">サポートリクエストを開いて、Dynamics サービス エンジニアリング にドキュメント処理の添付ファイルをサンド ボックス ストレージ アカウントから実稼働ストレージ アカウントにコピーさせ、本番データベースの DocuValue テーブルと DocuDeletedValue テーブルの参照を更新します。</span><span class="sxs-lookup"><span data-stu-id="43846-162">Open a support request to have Dynamics Support Engineering copy the document handling attachments from the sandbox storage account to the production storage account and update the references in the production database's DocuValue and DocuDeletedValue tables.</span></span> <span data-ttu-id="43846-163">要求が完了したら、添付ファイルがドキュメント処理レコードのサンプルに使用できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="43846-163">After the request has been completed, validate that the attachments are available for a sample of document handling records.</span></span>
8. <span data-ttu-id="43846-164">実稼働用の DRA を設定します。</span><span class="sxs-lookup"><span data-stu-id="43846-164">Set up DRAs for production.</span></span> <span data-ttu-id="43846-165">試用版の移行の一部として以前にインストールされた DRA のいずれかを再利用する場合は、サンドボックス URL ではなく、実稼働 URL に接続するように構成を更新するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="43846-165">If you're reusing any of the DRAs that were previously installed as part of your trial migration, remember to update their configuration so that they connect to the production URL instead of the sandbox URL.</span></span>
9. <span data-ttu-id="43846-166">カットオーバー計画で詳しく説明されているように、クラウドとオンプレミスの運用環境を調整します。</span><span class="sxs-lookup"><span data-stu-id="43846-166">Reconcile your cloud and on-premises production environments, as detailed in your cut-over plan.</span></span>
10. <span data-ttu-id="43846-167">運用開始のサインオフを取得します。</span><span class="sxs-lookup"><span data-stu-id="43846-167">Obtain sign-off for the go-live.</span></span>
11. <span data-ttu-id="43846-168">クラウド プロダクション インターフェイス、バッチジョブなどをアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="43846-168">Activate cloud production interfaces, batch jobs, and so on.</span></span>
12. <span data-ttu-id="43846-169">クラウド運用環境での取引を開始します。</span><span class="sxs-lookup"><span data-stu-id="43846-169">Start to transact in your cloud production environment.</span></span>

## <a name="migrate-document-handling-attachments-to-your-sandbox"></a><span data-ttu-id="43846-170">ドキュメント処理の添付ファイルをサンドボックスに移行</span><span class="sxs-lookup"><span data-stu-id="43846-170">Migrate document handling attachments to your sandbox</span></span>

<span data-ttu-id="43846-171">Finance + Operations (オンプレミス) 環境のドキュメント処理添付ファイルは、ファイル共有に格納されます。</span><span class="sxs-lookup"><span data-stu-id="43846-171">Document handling attachments for Finance + Operations (on-premises) environments are stored in a file share.</span></span> <span data-ttu-id="43846-172">ただし、クラウド バージョンはこのファイル共有をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="43846-172">However, the cloud version doesn't support this file share.</span></span> <span data-ttu-id="43846-173">次の手順を使用して、添付ファイルをサンドボックス環境の Azure ストレージ アカウントにコピーし、データベース内の対応するメタデータを更新できます。</span><span class="sxs-lookup"><span data-stu-id="43846-173">You can use the following procedure to copy the attachments to the Azure storage account for your sandbox environment and update the corresponding metadata in the database.</span></span> <span data-ttu-id="43846-174">その後の実稼働への昇格のために、Dynamics サービス エンジニアリングは添付ファイルをサンドボックスから実稼働にコピーするように要求できます。</span><span class="sxs-lookup"><span data-stu-id="43846-174">For subsequent promotion to production, you can request that Dynamics Support Engineering copy the attachments from your sandbox to production.</span></span>

1. <!--HERE--><span data-ttu-id="43846-175">添付ファイルを処理するドキュメントのコピーを、オンプレミスの実稼働ファイル共有から、Application Object Server (AOS) のサンドボックス インスタンスの 1 つにある一時フォルダーにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="43846-175">Upload a copy of the document handling attachment files from the on-premises production file share to a temporary folder on one of the sandbox instances of Application Object Server (AOS).</span></span> <span data-ttu-id="43846-176">たとえば、添付ファイルの ZIP ファイルをアップロードし、ターゲットで展開することができます。</span><span class="sxs-lookup"><span data-stu-id="43846-176">For example, you can upload a zip file of the attachments and unpack it on the target.</span></span> <span data-ttu-id="43846-177">リモート デスクトップ アクセスがない場合 (たとえば、セルフ サービス環境など) は、代わりに別の仮想マシン (VM) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="43846-177">If you don't have remote desktop access (for example, for a self-service environment), you can use a different virtual machine (VM) instead.</span></span> <span data-ttu-id="43846-178">妥当な変換パフォーマンスを得るには、この VM をターゲット サンドボックスと同じ Azure データセンターに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-178">For reasonable conversion performance, this VM should be in the same Azure datacenter as the target sandbox.</span></span> <span data-ttu-id="43846-179">AOS インスタンスを使用していない場合は、サンドボックスの SQL データベース インスタンスへのアクセスの許可リストに VM を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43846-179">If you aren't using the AOS instance, you must add the VM to an allow list for access to the sandbox's SQL database instance.</span></span>
2. <span data-ttu-id="43846-180">サポート リクエストを開いて、サンドボックス Azure ストレージ アカウントの名前と、ドキュメント コンテナの時間制限のある共有アクセス署名トークンを取得します。</span><span class="sxs-lookup"><span data-stu-id="43846-180">Open a support request to get the name of the sandbox Azure storage account and a time-limited shared access signature token for the documents container.</span></span> <span data-ttu-id="43846-181">次の手順で実行する Windows PowerShell スクリプトの対応するプレースホルダーを更新します。</span><span class="sxs-lookup"><span data-stu-id="43846-181">Update the corresponding placeholders in the Windows PowerShell script that is run in the next step.</span></span> <span data-ttu-id="43846-182">また、LCS の環境の詳細を使用して、一時フォルダーと Finance and Operations トランザクション データベースのプレースホルダーを更新し ます。</span><span class="sxs-lookup"><span data-stu-id="43846-182">Also update the placeholders for your temporary folder, and for your Finance and Operations transactional database, by using the environment details in LCS.</span></span>
3. <span data-ttu-id="43846-183">サンドボックス AOS インスタンスまたはその他の VM で次の Windows PowerShell スクリプトを実行して、ドキュメント処理ファイルをストレージアカウントにアップロードし、各ファイルに必要なメタデータを作成します。</span><span class="sxs-lookup"><span data-stu-id="43846-183">Run the following Windows PowerShell script on the sandbox AOS instance or other VM to upload the document handling files to the storage account and create the required metadata for each file.</span></span>

    ```powershell
    #Upload F&O on-prem document handling attachments to Azure storage account
    #
    $filesPath = "<TEMP_ATTACHMENTS_FOLDER_PATH>"
    $dBHostName = "<DATABASE_SERVER>.database.windows.net"
    $dBName = "<DATABASE_NAME>"
    $dBUsername = "<DATABASE_USER>"
    $dBPassword  = "<DATABASE_PASSWORD>"
    $storageAccountName = "<STORAGE_ACCOUNT_NAME>"
    $sasToken = "<SAS_TOKEN>"

    [Reflection.Assembly]::LoadWithPartialName("System.Security.Cryptography") #Load crypto
    $cryptoObj = [System.Security.Cryptography.SHA256]::Create()
    $StorageContext = New-AzStorageContext -StorageAccountName $storageAccountName -SasToken $sasToken
    foreach ($file in Get-ChildItem $filesPath) 
    {
        try
        {
            $blob = (Set-AzStorageBlobContent -Context $StorageContext -Container documents -File $file.FullName -Blob "$($file.Name)" -Force).ICloudBlob
        }
        catch
        {
            Write-Host "Could not upload $($file.Fullname) to blob"
            Write-Host $_
        }
        if($blob)
        {
            #Write-Host "Processing $($file.Fullname)..."
            #FileHash:
            $fileBytes = [System.IO.File]::ReadAllBytes($file.FullName)
            $hashBytes = $cryptoObj.ComputeHash($fileBytes)
            $encodedHash = [System.Convert]::ToBase64String($hashBytes)
            #FullFileName:
            $origFileName = (Invoke-Sqlcmd -Query "SELECT ORIGINALFILENAME FROM DOCUVALUE WHERE FILEID = '$($file.Name)'" -ServerInstance $dBHostName -Database $dBName -Username $dBUsername -Password $dBPassword).ORIGINALFILENAME
            if ($origFileName.Length -eq 0)
            {
                $origFileName = (Invoke-Sqlcmd -Query "SELECT ORIGINALFILENAME FROM DOCUDELETEDVALUE WHERE FILEID = '$($file.Name)'" -ServerInstance $dBHostName -Database $dBName -Username $dBUsername -Password $dBPassword).ORIGINALFILENAME
            }
            if ($origFileName.Length -eq 0)
            {
                Write-Host "Missing DOCUVALUE $($file.Name)"
            }
            else
            {
                $nameBytes  = [System.Text.Encoding]::UTF8.GetBytes($origFileName)
                $encodedName =  [System.Convert]::ToBase64String($nameBytes)
                #Write-Host "Base64 encoded original filename $encodedName."
                $blob.Metadata["FileHash"] = $encodedHash
                $blob.Metadata["FileSize"] = $file.Length
                $blob.Metadata["FullFileName"] = $encodedName
                $blob.SetMetadata()
                Write-Host "Uploaded $($file.Fullname)"
            }
        }
    }
    ```

4. <span data-ttu-id="43846-184">SSMS で、次の T-SQL コマンドを実行して、DocuValue レコードと DocuDeletedValue レコードを更新し、ターゲットの保存場所を参照するようにします。</span><span class="sxs-lookup"><span data-stu-id="43846-184">In SSMS, run the following T-SQL commands to update the DocuValue and DocuDeletedValue records so that they reference the target storage location.</span></span>

    ```sql
    update DOCUVALUE
    set ACCESSINFORMATION = replace(ACCESSINFORMATION, 'file://<SOURCE_PREFIX>/documents/', 'https://<STORAGE_ACCOUNT>.blob.core.windows.net/documents/'), STORAGEPROVIDERID = 1
    where STORAGEPROVIDERID = 4 --4 for LBD filesystem, 1 for Azure blob
    and ACCESSINFORMATION like 'file://<SOURCE_PREFIX>/documents/%'

    update DOCUDELETEDVALUE
    set ACCESSINFORMATION = replace(ACCESSINFORMATION, 'file://<SOURCE_PREFIX>/documents/', 'https://<STORAGE_ACCOUNT>.blob.core.windows.net/documents/'), STORAGEPROVIDERID = 1
    where STORAGEPROVIDERID = 4 --4 for LBD filesystem, 1 for Azure blob
    and ACCESSINFORMATION like 'file://<SOURCE_PREFIX>/documents/%'
    ```

5. <span data-ttu-id="43846-185">ドキュメント処理の添付ファイルのサンプルをテストして、サンドボックス環境でアクセスできるようになったことを確認します。</span><span class="sxs-lookup"><span data-stu-id="43846-185">Test a sample of the document handling attachments to make sure that they can now be accessed in the sandbox environment.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

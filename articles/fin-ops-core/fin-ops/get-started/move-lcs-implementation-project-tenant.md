---
title: LCS 実装プロジェクトを別の Azure AD テナントに移動する
description: このトピックでは、サブスクリプションと LCS 実装プロジェクトを異なる Azure AD テナントに移動する方法について説明します。
author: ClaudiaBetz-Haubold
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0
ms.openlocfilehash: 938617e67b8bcb954f2d5c8662ec00e323dcc07b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744503"
---
# <a name="move-lcs-implementation-projects-to-different-azure-ad-tenants"></a><span data-ttu-id="00be2-103">LCS 実装プロジェクトを別の Azure AD テナントに移動する</span><span class="sxs-lookup"><span data-stu-id="00be2-103">Move LCS implementation projects to different Azure AD tenants</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00be2-104">サブスクリプションと Microsoft Dynamics Lifecycle Services (LCS) 導入プロジェクトを別の Microsoft Azure Active Directory (Azure AD) テナントに移すことができます。</span><span class="sxs-lookup"><span data-stu-id="00be2-104">You can move your subscriptions and your Microsoft Dynamics Lifecycle Services (LCS) Implementation project to a different Microsoft Azure Active Directory (Azure AD) tenant.</span></span> <span data-ttu-id="00be2-105">この移動が必要になる場合のいくつかのシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="00be2-105">Here are some scenarios where this move might be required:</span></span>

- <span data-ttu-id="00be2-106">誤ってサブスクリプションが正しくない Azure AD テナントに対して購入されました。</span><span class="sxs-lookup"><span data-stu-id="00be2-106">Subscriptions were accidentally purchased against the incorrect Azure AD tenant.</span></span>

    > [!NOTE]
    > <span data-ttu-id="00be2-107">ユーザーがクラウド サービス プロバイダーであり、既存の顧客に Finance and Operations アプリのサブスクリプションを販売する場合は、その顧客との再販業者関係を要求して、顧客の既存の Azure AD テナントにサブスクリプションを配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-107">If you're a cloud service provider, and you sell subscriptions for Finance and Operations apps to an existing customer, you must request a reseller relationship with that customer to put the subscriptions on the customer's existing Azure AD tenant.</span></span> <span data-ttu-id="00be2-108">Microsoft パートナー センターで新しい顧客レコードを作成する場合、顧客の新しい Azure AD テナントを作成します。</span><span class="sxs-lookup"><span data-stu-id="00be2-108">If you create a new customer record for the customer in Microsoft Partner Center, you create a new Azure AD tenant for the customer.</span></span>

- <span data-ttu-id="00be2-109">サブスクリプションが購入された後、顧客は Azure AD テナントの構造を変更します。</span><span class="sxs-lookup"><span data-stu-id="00be2-109">The customer changes the structure of the Azure AD tenant after the subscription is purchased.</span></span>

<span data-ttu-id="00be2-110">定期購読および関連するすべてのコンポーネントの移動のプロセスには、次の図に示すように、次の 4 つの主要なステップがあります。</span><span class="sxs-lookup"><span data-stu-id="00be2-110">The process for moving your subscriptions and all related artifacts has four main steps, as shown in the following illustration.</span></span>

![定期売買を移動するためのプロセス](./media/move-subscription-process.png)

## <a name="activate-subscriptions-on-the-new-tenant"></a><span data-ttu-id="00be2-112">新しいテナントのサブスクリプションを有効化</span><span class="sxs-lookup"><span data-stu-id="00be2-112">Activate subscriptions on the new tenant</span></span>

<span data-ttu-id="00be2-113">クラウド サービス プロバイダまたはボリューム ライセンスの再販業者と協力して、新しい Azure AD テナントに対するサブスクリプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="00be2-113">Work with your cloud service provider or volume license reseller to activate the subscriptions against the new Azure AD tenant.</span></span> <span data-ttu-id="00be2-114">ユーザーおよびアドオン環境のすべてのサブスクリプションを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-114">All subscriptions for users, and for add-on environments, must be activated.</span></span>

### <a name="cloud-service-provider"></a><span data-ttu-id="00be2-115">クラウド サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="00be2-115">Cloud service provider</span></span>

<span data-ttu-id="00be2-116">Microsoft クラウド ソリューション プロバイダー (CSP) 契約を通じてライセンスを取得している場合は、クラウド サービス プロバイダーから新しいテナントに対して必要なサブスクリプションを購入してください。</span><span class="sxs-lookup"><span data-stu-id="00be2-116">If you're licensed through a Microsoft Cloud Solution Provider (CSP) agreement, purchase the required subscriptions against the new tenant from your cloud service provider.</span></span> <span data-ttu-id="00be2-117">新しいテナントが既に存在する場合、クラウド サービス プロバイダは、再販業者関係を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-117">If the new tenant already exists, the cloud service provider must request a reseller relationship.</span></span> <span data-ttu-id="00be2-118">または、パートナー センターのクラウド サービス プロバイダで必要な既定ドメイン名の新しい顧客を作成する必要があります **\*.onmicrosoft.com** (たとえば、**contoso.onmicrosoft.com**)。</span><span class="sxs-lookup"><span data-stu-id="00be2-118">Alternatively, in Partner Center, the cloud service provider must create a new customer that has the desired default domain name, **\*.onmicrosoft.com** (for example, **contoso.onmicrosoft.com**).</span></span>

<span data-ttu-id="00be2-119">クラウド サービス プロバイダーに、今回は既存のサブスクリプションを中断しないよう依頼します。</span><span class="sxs-lookup"><span data-stu-id="00be2-119">Ask the cloud service provider not to suspend the existing subscriptions at this time.</span></span>

### <a name="volume-licensing"></a><span data-ttu-id="00be2-120">ボリューム ライセンス</span><span class="sxs-lookup"><span data-stu-id="00be2-120">Volume Licensing</span></span>

<span data-ttu-id="00be2-121">Microsoft ボリューム ライセンス契約を通じてライセンスを取得している場合は、[ボリューム ライセンス サポート センター](https://www.microsoft.com/Licensing/servicecenter/Help/Contact.aspx)に連絡し、サブスクリプションを古いテナントから新しいテナントに再マップするように依頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-121">If you're licensed through a Microsoft Volume Licensing agreement, you must call the [Volume Licensing support center](https://www.microsoft.com/Licensing/servicecenter/Help/Contact.aspx) and ask that the subscriptions be remapped from the old tenant to the new tenant.</span></span> <span data-ttu-id="00be2-122">Microsoft 365 管理センターからボリューム ライセンスのサポートに連絡することができます。</span><span class="sxs-lookup"><span data-stu-id="00be2-122">You can contact Volume Licensing Support through Microsoft 365 Admin center.</span></span> <span data-ttu-id="00be2-123">定期売買が両方のテナントで有効になると、支払猶予期間を要求します。</span><span class="sxs-lookup"><span data-stu-id="00be2-123">Request a grace period, when the subscriptions will be active on both tenants.</span></span> <span data-ttu-id="00be2-124">顧客プライバシーの問題が原因で、顧客がこの要求を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-124">Because of customer privacy concerns, this request must be made by the customer.</span></span> <span data-ttu-id="00be2-125">次の情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="00be2-125">You should have the following information available:</span></span>

- <span data-ttu-id="00be2-126">公的顧客番号。</span><span class="sxs-lookup"><span data-stu-id="00be2-126">Public customer number.</span></span>
- <span data-ttu-id="00be2-127">登録番号。</span><span class="sxs-lookup"><span data-stu-id="00be2-127">Enrollment number.</span></span>
- <span data-ttu-id="00be2-128">現在プロビジョニングされている定期売買の現在のテナント ドメイン。</span><span class="sxs-lookup"><span data-stu-id="00be2-128">The current tenant domain that the subscriptions are currently provisioned on.</span></span>
- <span data-ttu-id="00be2-129">顧客がサブスクリプションのプロビジョニングを希望する宛先テナント ドメイン。</span><span class="sxs-lookup"><span data-stu-id="00be2-129">The destination tenant domain that the customer wants the subscriptions provisioned under.</span></span>
- <span data-ttu-id="00be2-130">顧客が違うテナントに移行したボリューム ライセンス サブスクリプションを必要とする理由の詳細説明。</span><span class="sxs-lookup"><span data-stu-id="00be2-130">A detailed explanation of why the customer must have its Volume Licensing subscriptions migrated to a different tenant.</span></span>
- <span data-ttu-id="00be2-131">新しいテナントに移動しなければならない有料サブスクリプションの総数、サブスクリプション タイプおよび定員数。</span><span class="sxs-lookup"><span data-stu-id="00be2-131">The total number of paid subscriptions that must be moved to the new tenant, together with the subscription type and seat count.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00be2-132">古いテナントで LCS の廃棄が完了するまでの数週間、定期売買が両方のテナントで並行して有効であることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="00be2-132">It's crucial that the subscriptions be active on both tenants in parallel for a few weeks, until you've finished decommissioning LCS on the old tenant.</span></span>

## <a name="configure-lcs-on-the-new-tenant"></a><span data-ttu-id="00be2-133">新しいテナントに LCS をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="00be2-133">Configure LCS on the new tenant</span></span>

<span data-ttu-id="00be2-134">新しいテナントで、開始し設定する必要がある新しい LCS プロジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="00be2-134">On the new tenant, you will get a new LCS project that you must initiate and set up.</span></span>

1. <span data-ttu-id="00be2-135">新しいプロジェクト オンボード ウィザードの操作を完了します。</span><span class="sxs-lookup"><span data-stu-id="00be2-135">Complete the Project Onboarding wizard.</span></span> <span data-ttu-id="00be2-136">詳細については、[LCS プロジェクトのオンボード](../../dev-itpro/lifecycle-services/project-onboarding.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00be2-136">For more information, see [LCS project onboarding](../../dev-itpro/lifecycle-services/project-onboarding.md).</span></span> <span data-ttu-id="00be2-137">ウィザードの完了時に、既存の **LCS プロジェクトを別のテナントから移動** し、ソース LCS プロジェクト ID を提供する **プロジェクトの概要** ページで、このウィザードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-137">When completing the wizard, you must indicate on the **Project Overview** page that you are **Moving existing LCS project from another tenant** and provide the source LCS project ID.</span></span>
2. <span data-ttu-id="00be2-138">LCS を完全に構成します。</span><span class="sxs-lookup"><span data-stu-id="00be2-138">Fully configure LCS.</span></span> <span data-ttu-id="00be2-139">この構成の一部として、次の作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-139">As part of this configuration, you must:</span></span>
    1. <span data-ttu-id="00be2-140">サブスクリプション見積もりをアップロードして有効にします。</span><span class="sxs-lookup"><span data-stu-id="00be2-140">Upload and activate a subscription estimator.</span></span> <span data-ttu-id="00be2-141">ソース LCS プロジェクトで既に住んでいる場合は、見積が一致することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-141">If you are already live in the source LCS project, you need to ensure that the estimates match.</span></span>
    2. <span data-ttu-id="00be2-142">配置可能パッケージをアセット ライブラリに追加します。</span><span class="sxs-lookup"><span data-stu-id="00be2-142">Add your deployable package to the asset library.</span></span>
    3. <span data-ttu-id="00be2-143">ビジネス プロセス モデラー (BPM) ライブラリの更新。</span><span class="sxs-lookup"><span data-stu-id="00be2-143">Update your Business process modeler (BPM) library.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00be2-144">この期間中、2 つの並列 LCS プロジェクトがあります。</span><span class="sxs-lookup"><span data-stu-id="00be2-144">During this period, you will have two parallel LCS projects.</span></span> <span data-ttu-id="00be2-145">LCS 内の **利用可能なサブスクリプション** ページの LCS プロジェクトに関連付けられている Azure AD テナントの名前と ID を確認できます。</span><span class="sxs-lookup"><span data-stu-id="00be2-145">You can verify the name and ID of the Azure AD tenant that is associated with an LCS project on the **Subscriptions available** page in LCS.</span></span>

## <a name="move-your-sandbox-environments-to-the-new-tenant"></a><span data-ttu-id="00be2-146">サンドボックス環境を新しいテナントに移動する</span><span class="sxs-lookup"><span data-stu-id="00be2-146">Move your sandbox environments to the new tenant</span></span>
1. <span data-ttu-id="00be2-147">新しい LCS プロジェクトの非運用環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="00be2-147">Deploy the non-production environments in the new LCS project.</span></span>
2. <span data-ttu-id="00be2-148">必要なコード パッケージを環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="00be2-148">Apply the required code packages to the environments.</span></span> <span data-ttu-id="00be2-149">そのターゲットで、ソースと同じバージョンのアプリケーションが実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-149">Make sure that the target is running the same application version as the source.</span></span> <span data-ttu-id="00be2-150">該当する場合は、[オールインワン配置可能パッケージ](../../dev-itpro/dev-tools/aio-deployable-packages.md) を使用し、ISV ライセンスを含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="00be2-150">We recommend using [All-in-one deployable packages](../../dev-itpro/dev-tools/aio-deployable-packages.md) and include any ISV licenses, if applicable.</span></span>
3. <span data-ttu-id="00be2-151">環境にデータをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="00be2-151">Upload data to the environments.</span></span> <span data-ttu-id="00be2-152">データ パッケージを使用してデータを移動することも、データベースを復元することもできます。</span><span class="sxs-lookup"><span data-stu-id="00be2-152">You can move the data through data packages or by restoring the database.</span></span> <span data-ttu-id="00be2-153">データベースを復元する場合は、いくつかのプロパティを新しいテナントに再マップするために追加の手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="00be2-153">If you restore the database, additional steps are required in order to remap some properties to the new tenant.</span></span>
4. <span data-ttu-id="00be2-154">ユーザー情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="00be2-154">Update your user information.</span></span>
    1. <span data-ttu-id="00be2-155">管理者ユーザーを除くすべてのユーザー アカウントを削除します。</span><span class="sxs-lookup"><span data-stu-id="00be2-155">Remove all user accounts except the admin user.</span></span>
    2. <span data-ttu-id="00be2-156">USERINFO の管理者ユーザー レコードを修正します。</span><span class="sxs-lookup"><span data-stu-id="00be2-156">Fix the admin user record in USERINFO.</span></span>
    
    ```sql
        UPDATE USERINFO
        SET SID='mysid', NETWORKALIAS='myalias/email', NETWORKDOMAIN='https://sts.windows.net'
        WHERE ID = 'Admin'
        ```
5. Re-import all other users that have the correct security identifier (SID) and identity provider.
6. Run the following commands to update the tenant ID in the appropriate tables. You can verify the Azure AD tenant ID that is associated with an LCS project on the **Subscriptions available** page in LCS.
    
    ```sql
    Update POWERBICONFIG set TENANTID = 'newtenantid' where TENANTID = 'oldtenantid'
    Update PROVISIONINGMESSAGETABLE set TENANTID = 'newtenantid' where TENANTID = 'oldtenantid'
    Update B2BINVITATIONCONFIG set TENANTID = 'newtenantid' where TENANTID = 'oldtenantid'
    Update RETAILSHAREDPARAMETERS set TENANTID = 'newtenantid' where TENANTID = 'oldtenantid'
    ```

7. <span data-ttu-id="00be2-157">環境を完全に構成します。</span><span class="sxs-lookup"><span data-stu-id="00be2-157">Fully configure the environments.</span></span> <span data-ttu-id="00be2-158">この手順の一部として、統合のエンドポイントをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="00be2-158">As part of this step, configure the integration endpoints.</span></span>
8. <span data-ttu-id="00be2-159">新しい LCS プロジェクトのユーザー受け入れテスト (UAT) 環境でスモーク テストを実行します。</span><span class="sxs-lookup"><span data-stu-id="00be2-159">Perform smoke tests on the user acceptance testing (UAT) environment in the new LCS project.</span></span> <span data-ttu-id="00be2-160">これらのテストでは、ユーザーのサインイン、統合、ワークフロー、印刷、レポート、および構成やユーザー情報に依存する同様のプロセスに焦点を当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-160">These tests should focus on user sign-in, integrations, workflows, printing, reporting, and similar processes that depend on configuration and user information.</span></span>

<span data-ttu-id="00be2-161">ソリューションとスコープに応じて、新しい Azure AD テナントで追加の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-161">Depending on your solution and scope, you might have to perform additional steps on the new Azure AD tenant.</span></span> <span data-ttu-id="00be2-162">これらの手順には、アプリケーションの登録 (定期的な統合と倉庫管理のため)、ドメインの追加、およびシングル サインオン (SSO) を有効にするディレクトリ同期の設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="00be2-162">These steps might include registering applications (for recurring integrations and warehouse management), adding domains, and setting up directory synchronization to enable single sign-on (SSO).</span></span>

<span data-ttu-id="00be2-163">Web サービスへの呼び出しが、環境の **ホーム** テナントからのみ許可されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="00be2-163">Note that calls to web services are allowed only from the **home** tenant for the environment.</span></span> <span data-ttu-id="00be2-164">たとえば、元のテナントは companya.com であり、統合は `services\@companya.com` として実行されました。</span><span class="sxs-lookup"><span data-stu-id="00be2-164">For example, the original tenant was companya.com, and integration ran as `services\@companya.com`.</span></span> <span data-ttu-id="00be2-165">この場合、テナントを companyb.com に切り替えると、**userInfo.networkdomain** を `https://sts.windows.net/companyb.com` に更新してもWeb サービスの呼び出しに対して `services\@companya.com` を使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="00be2-165">In this case, when you switch tenants to companyb.com, you can no longer use `services\@companya.com` for web service calls, even if you update **userInfo.networkdomain** to `https://sts.windows.net/companyb.com`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00be2-166">サンドボックス環境で、Azure Blob Storage に保存されている添付ファイルを処理するドキュメントは失われます。</span><span class="sxs-lookup"><span data-stu-id="00be2-166">On your sandbox environments, you will lose any document handling attachments that are stored in Azure Blob storage.</span></span> <span data-ttu-id="00be2-167">Blob ストレージは、Microsoft によって運用環境に対してのみ移動されます。</span><span class="sxs-lookup"><span data-stu-id="00be2-167">Blob storage will be moved by Microsoft only for production environments.</span></span>

## <a name="move-your-production-environment-to-the-new-tenant"></a><span data-ttu-id="00be2-168">運用環境を新しいテナントに移動する</span><span class="sxs-lookup"><span data-stu-id="00be2-168">Move your production environment to the new tenant</span></span>

<span data-ttu-id="00be2-169">古いテナントに既に運用環境が配置されていない場合は、このセクションを省略できます。</span><span class="sxs-lookup"><span data-stu-id="00be2-169">If you do not have a production environment deployed already on the old tenant, you can skip this section.</span></span>

<span data-ttu-id="00be2-170">古いテナントに運用環境が既に配置されていた場合、Microsoft は、データベースと Azure Blob のストレージを、古い運用環境から新しい運用環境に移動します。</span><span class="sxs-lookup"><span data-stu-id="00be2-170">If you already had a production environment deployed on the old tenant, Microsoft will move your database and Azure Blob storage from your old production environment to the new one.</span></span> <span data-ttu-id="00be2-171">前提条件として、すべてのサンドボックス環境と完了した UAT の移動が終了した後で、追加の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-171">As a pre-requisite, you must complete the additional steps below after you've finished moving all the sandbox environments and completed UAT.</span></span> <span data-ttu-id="00be2-172">運用環境を新しいテナントに移動するプロセスには、ダウンタイムが必要です。</span><span class="sxs-lookup"><span data-stu-id="00be2-172">The process of moving a production environment to a new tenant requires a downtime.</span></span>

<span data-ttu-id="00be2-173">運用環境を要求する前に、すべての前提条件が完了していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-173">Before requesting the production environment, ensure that all pre-requisites are completed:</span></span>

1. <span data-ttu-id="00be2-174">運用環境ですべてのユーザーを正しくライセンスするために必要なライセンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="00be2-174">Get all required licenses that are needed to correctly license all users on the  production environment.</span></span>
2. <span data-ttu-id="00be2-175">ライセンスが準備できたら、新しい LCS プロジェクトにサブスクリプション見積もりをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="00be2-175">When the licenses are in place, upload a subscription estimator to the new LCS project.</span></span> <span data-ttu-id="00be2-176">これは、ソース LCS プロジェクトで有効なサブスクリプション見積もりに一致する必要があります。また、ピーク トランザクション ボリュームを正確に反映する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-176">It should match the subscription estimator that is active in the source LCS project, and it must correctly reflect peak transaction volumes.</span></span>
3. <span data-ttu-id="00be2-177">Dynamics 365 FO Go Live (d365fogl\@microsoft.com) に、新しい LCS プロジェクトで Microsoft が運用データベースと Azure Blob ストレージを移動する準備ができていることを示す電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="00be2-177">Send an email to Dynamics 365 FO Go-Live (d365fogl\@microsoft.com) stating that your new LCS project is ready for Microsoft to move your production database and Azure Blob Storage.</span></span> <span data-ttu-id="00be2-178">プロセスがスムーズに実行されるようにするには、電子メールに次の詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="00be2-178">To ensure that the process will run smoothly, provide the following details in the email.</span></span> <span data-ttu-id="00be2-179">次のリストを電子メールにコピーしてから、すべての情報に 1 行ずつ答えることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="00be2-179">We suggest that copy the following list to your email, and then answer all of the information line by line.</span></span>

    <span data-ttu-id="00be2-180">**Lifecycle Services**</span><span class="sxs-lookup"><span data-stu-id="00be2-180">**Lifecycle Services**</span></span>
    - <span data-ttu-id="00be2-181">ソースおよびターゲット LCS プロジェクトの LCS ID (LCS プロジェクト URL 番号) を提供します。</span><span class="sxs-lookup"><span data-stu-id="00be2-181">Provide the LCS IDs (number in the LCS project URL) for source and target LCS project.</span></span>
    - <span data-ttu-id="00be2-182">運用日付をターゲット LCS プロジェクトで正しく設定していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-182">Confirm that the go-live date is set correctly in the target LCS project.</span></span>
    - <span data-ttu-id="00be2-183">更新スケジュールが、ターゲット LCS プロジェクト (**LCS > メニュー > プロジェクト設定 > 更新設定**) で設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-183">Confirm that the update schedules are set in the target LCS project (**LCS > Menu > Project settings > Update settings**).</span></span>
    - <span data-ttu-id="00be2-184">ドキュメントの添付ファイルに対して Azure Blob ストレージを使用しているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-184">Confirm if you are using Azure Blob Storage for document attachments.</span></span>
    - <span data-ttu-id="00be2-185">プロジェクト オンボード ウィザードで、プロジェクトがテナント移動として識別されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-185">Confirm that your project is identified as a tenant move in the Project Onboarding wizard.</span></span>
    
    <span data-ttu-id="00be2-186">**テスト**</span><span class="sxs-lookup"><span data-stu-id="00be2-186">**Testing**</span></span>
    - <span data-ttu-id="00be2-187">ターゲット LCS プロジェクトのサンドボックス環境 (Tier-2 またはそれ以降) でスモーク テストが完了していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-187">Confirm that the smoke testing is completed on the sandbox environment (Tier-2 or higher) in the target LCS project.</span></span>
    
    <span data-ttu-id="00be2-188">**コード管理**</span><span class="sxs-lookup"><span data-stu-id="00be2-188">**Code Management**</span></span>
    - <span data-ttu-id="00be2-189">配置可能なパッケージが、ターゲット LCS プロジェクトでリリース候補としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-189">Confirm that your deployable package is marked as a release candidate in the target LCS project.</span></span>
    - <span data-ttu-id="00be2-190">使用している ISV ソリューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="00be2-190">List the ISV solutions you are using.</span></span>
    - <span data-ttu-id="00be2-191">古い運用環境を実行しているバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-191">Confirm which version your old production environment is running on.</span></span>
    - <span data-ttu-id="00be2-192">データベースのコピーの問題を防ぐために、新しい運用環境に適用される非標準コードが、古い運用環境に存在する非標準コードとまったく同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-192">Confirm that non-standard code to be applied in the new production environment will be exactly the same as the non-standard code present in the old production environment in order to prevent database copy issues.</span></span>
    - <span data-ttu-id="00be2-193">カスタム フォントや高度な環境のインストールなど、新しい運用環境で考慮する必要がある、古い運用環境で実行された非典型的なアクションがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-193">Confirm if there were any non-typical actions taken on your old production environment which need to be considered on the new production environment, like installation of a custom font or environment upscale.</span></span>
    
    <span data-ttu-id="00be2-194">**環境**</span><span class="sxs-lookup"><span data-stu-id="00be2-194">**Environment**</span></span>
    - <span data-ttu-id="00be2-195">新しい運用環境を配置するために計画している環境のバージョンを共有します。</span><span class="sxs-lookup"><span data-stu-id="00be2-195">Share which environment version you plan to deploy your new production environment.</span></span>
    - <span data-ttu-id="00be2-196">業務をどのようにして行うかを説明します。</span><span class="sxs-lookup"><span data-stu-id="00be2-196">Describe how you will conduct your cut over.</span></span>
    - <span data-ttu-id="00be2-197">ソース LCS 環境およびプロジェクトの割り当てを解除して削除する日付を確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-197">Confirm the dates when the source LCS environments and project will be deallocated and deleted.</span></span>
    
4. <span data-ttu-id="00be2-198">Dynamics 365 FO Go-Live チームは 2 営業日以内にご回答します。さらに、FastTrack ソリューション アーキテクトは、運用配置に対するプロジェクトの準備の評価において、協力して作業します。</span><span class="sxs-lookup"><span data-stu-id="00be2-198">The Dynamics 365 FO Go-Live team will reply to you within 2 business days and a FastTrack Solution Architect will work with you on the assessment of the project readiness for production deployment.</span></span>
5. <span data-ttu-id="00be2-199">テナント移動評価が正常に完了すると、FastTrack ソリューション アーキテクトが配置用に生産要求を承認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-199">When the tenant move assessment is successfully completed, the FastTrack Solution Architect will approve your production request for deployment.</span></span>
6. <span data-ttu-id="00be2-200">新しい LCS プロジェクトに対して運用配置要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="00be2-200">Create the production deployment request on the new LCS project.</span></span>

    - <span data-ttu-id="00be2-201">古い運用環境で使用されているので、新しい運用環境に対して同じ名前を選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="00be2-201">It is not possible to select the same name for the new production environment, as it is in use for your old production environment.</span></span> <span data-ttu-id="00be2-202">新しい URL が生成されるように、新しい環境名を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-202">You will need to choose a new environment name so that a new URL will be generated.</span></span>
    - <span data-ttu-id="00be2-203">現在の運用環境で使用されているのと同じアプリケーション バージョンを選択していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="00be2-203">Make sure you select the same application version that is used by your current production environment.</span></span>
    - <span data-ttu-id="00be2-204">運用構成ウィザードで、環境管理者として、名前付きユーザーではなく汎用ユーザー アカウントを選択します。</span><span class="sxs-lookup"><span data-stu-id="00be2-204">In the Production configuration wizard, select a generic user account, not a named user, as Environment Administrator.</span></span>

7. <span data-ttu-id="00be2-205">運用環境を配置した後、ソース環境とターゲット環境のコードがまったく同じであることを確認します。それ以外の場合は、移行は失敗します。</span><span class="sxs-lookup"><span data-stu-id="00be2-205">After the production environment has been deployed, verify that source and target environments have exactly the same code, otherwise migration will fail.</span></span> <span data-ttu-id="00be2-206">必要に応じて、配置可能なパッケージをターゲットの運用環境にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-206">If necessary, deployable packages must be installed on the target production environment.</span></span>
8. <span data-ttu-id="00be2-207">古い運用環境から新しい運用環境にデータベースと BLOB ストレージをコピーすることを要求します。</span><span class="sxs-lookup"><span data-stu-id="00be2-207">Request to copy database and blob storage from the old production environment to the new production environment.</span></span>

     - <span data-ttu-id="00be2-208">**セルフ サービス環境へのクラウド配置**: タイプ **その他** の[サービス要求を送信](../../dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md)して、Microsoft サービス エンジニアリング チームがデータベースと Blob ストレージを (該当する場合)、古い運用環境から新しい運用環境にコピーするよう要求します。</span><span class="sxs-lookup"><span data-stu-id="00be2-208">**Cloud deployment to self-service deployment**: [Submit a service request](../../dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md) of type **Other** to request that the Microsoft Service Engineering team copy the database and blob storage, if applicable, from the old production environment to the new production environment.</span></span> <span data-ttu-id="00be2-209">サービス要求には、ソースとターゲット プロジェクトの LCS ID および環境 ID が含まれていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="00be2-209">Be sure to include LCS IDs and environment IDs from source and target projects in the service request.</span></span>
     
     - <span data-ttu-id="00be2-210">**両方のプロジェクト (新旧) はセルフ サービス配置です**: **サポート チケット** を送信して、データベースと Blob ストレージのコピーを (該当する場合)、古い運用環境から新しい運用環境に要求します。</span><span class="sxs-lookup"><span data-stu-id="00be2-210">**Both projects (old and new) are self-service deployments**: Submit a **support ticket** requesting a copy of the database and blob storage, if applicable, from the old production environment to the new production environment.</span></span> <span data-ttu-id="00be2-211">サポート チケットには、ソースとターゲット プロジェクトの LCS ID および環境 ID が含まれていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="00be2-211">Be sure to include LCS IDs and environment IDs from source and target projects in the support ticket.</span></span>
     
     
    1. <span data-ttu-id="00be2-212">このプロセスには、Microsoft と実装するプロジェクト チームとの間の対話が必要です。</span><span class="sxs-lookup"><span data-stu-id="00be2-212">This process will require interaction between Microsoft and the implementing project team.</span></span> <span data-ttu-id="00be2-213">電子メール通知または通知をサービス要求で直接フォローしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00be2-213">Ensure that you follow the email notifications or notifications directly in the service request.</span></span> 
    2. <span data-ttu-id="00be2-214">Microsoft が活動を完了し、更新された情報が提供された後、新しい運用環境を検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-214">After Microsoft has completed the activity and provided you with updated information, you will need to validate the new production environment.</span></span> 
    3. <span data-ttu-id="00be2-215">移行後に問題が発生した場合は、サポート チケットをファイルします。</span><span class="sxs-lookup"><span data-stu-id="00be2-215">If you encounter an issue after the migration, file a support ticket.</span></span>

## <a name="tear-down-the-lcs-project-on-the-old-tenant"></a><span data-ttu-id="00be2-216">古いテナントの LCS プロジェクトの破棄</span><span class="sxs-lookup"><span data-stu-id="00be2-216">Tear down the LCS project on the old tenant</span></span>

<span data-ttu-id="00be2-217">新しい Azure AD テナントの新しい LCS プロジェクトが完全に機能した後、古い LCS プロジェクトで環境を停止、解除および削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-217">After the new LCS project on the new Azure AD tenant is fully functional, you must stop, deallocate, and delete the environments on the old LCS project.</span></span> <span data-ttu-id="00be2-218">完了したとき、**コンフィグレーション** ボタンは環境ごとに使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="00be2-218">When you've finished, the **Configure** button becomes available for each environment.</span></span> <span data-ttu-id="00be2-219">古いテナントに既に運用環境がある場合は、削除するサポート チケットをファイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-219">If you already had a production environment on the old tenant, you must file a support ticket to have it deleted.</span></span>

<span data-ttu-id="00be2-220">後で必要になる可能性のある残りのコンポーネントは、アセット ライブラリから保管する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-220">You should save any remaining artifacts from the Asset library that you might require later.</span></span>

<span data-ttu-id="00be2-221">すべての環境を削除してすべてのアーティファクトを保存した後は、古いテナントの組織の管理者が LCS プロジェクトを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00be2-221">After all environments have been deleted and all artifacts saved, an Organization Administrator on the old tenant must delete the LCS project.</span></span>
<span data-ttu-id="00be2-222">Microsoft は、顧客のアカウントを無効にし、サービスが長期間にわたって中断された後に顧客データを削除する権限を保有します。</span><span class="sxs-lookup"><span data-stu-id="00be2-222">Microsoft reserves the right to disable the customer's account and delete the customer data after the service has been suspended for an extended period.</span></span>

## <a name="suspend-subscriptions-on-the-old-tenant"></a><span data-ttu-id="00be2-223">古いテナントで定期売買を中断します。</span><span class="sxs-lookup"><span data-stu-id="00be2-223">Suspend subscriptions on the old tenant</span></span>

<span data-ttu-id="00be2-224">すべての環境が削除されると、必要な LCS コンポーネントを保存し、クラウド サービス プロバイダまたは Volume Licensing Support と協力して、以前の Azure AD テナントのすべてのライセンスを中断します。</span><span class="sxs-lookup"><span data-stu-id="00be2-224">After all the environments have been deleted, and you've saved the LCS artifacts that you require, work with your cloud service provider or Volume Licensing Support to suspend all the licenses on the old Azure AD tenant.</span></span>

- <span data-ttu-id="00be2-225">**クラウド サービス プロバイダー** - 古いテナントに対して既存のサブスクリプションを中断します。</span><span class="sxs-lookup"><span data-stu-id="00be2-225">**Cloud service provider** - Suspend the existing subscriptions against the old tenant.</span></span>
- <span data-ttu-id="00be2-226">**ボリューム ライセンス サポート** - 作業が完了したこと、およびサブスクリプションが古いテナントに対してすぐ中断することを確認するボリューム ライセンス サポートを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="00be2-226">**Volume Licensing Support** - Call Volume Licensing Support to confirm that you've completed the work and that the subscriptions can now be suspended against the old tenant.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
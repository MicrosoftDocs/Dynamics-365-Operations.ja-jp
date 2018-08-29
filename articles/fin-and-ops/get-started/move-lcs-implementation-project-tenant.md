---
title: "LCS 実装プロジェクトを異なる Azure AD テナントに移動する"
description: "このトピックでは、定期売買と LCS 実装プロジェクトを異なる Azure AD テナントに移動する方法について説明します。"
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: c3d46eab0b0a774930dd999f75c21ede266d23cb
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="move-lcs-implementation-projects-to-different-azure-ad-tenants"></a><span data-ttu-id="151f1-103">LCS 実装プロジェクトを異なる Azure AD テナントに移動する</span><span class="sxs-lookup"><span data-stu-id="151f1-103">Move LCS implementation projects to different Azure AD tenants</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="151f1-104">サブスクリプションと Microsoft Dynamics Lifecyle Services (LCS) 導入プロジェクトを別の Microsoft Azure Active Directory (Azure AD) テナントに移すことができます。</span><span class="sxs-lookup"><span data-stu-id="151f1-104">You can move your subscriptions and your Microsoft Dynamics Lifecyle Services (LCS) Implementation project to a different Microsoft Azure Active Directory (Azure AD) tenant.</span></span> <span data-ttu-id="151f1-105">この移動が必要になる場合のいくつかのシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="151f1-105">Here are some scenarios where this move might be required:</span></span>

- <span data-ttu-id="151f1-106">誤って定期売買が正しくない Azure AD テナントに対して購入されました。</span><span class="sxs-lookup"><span data-stu-id="151f1-106">Subscriptions were accidentally purchased against the incorrect Azure AD tenant.</span></span>

    > [!NOTE]
    > <span data-ttu-id="151f1-107">クラウド サービス プロバイダーであり、既存の顧客に Microsoft Dynamics 365 for Finance and Operations のサブスクリプションを販売する場合は、その顧客との再販業者関係を要求して、顧客の既存の Azure AD テナントにサブスクリプションを配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="151f1-107">If you're a cloud service provider, and you sell subscriptions for Microsoft Dynamics 365 for Finance and Operations to an existing customer, you must request a reseller relationship with that customer to put the subscriptions on the customer's existing Azure AD tenant.</span></span> <span data-ttu-id="151f1-108">Microsoft パートナー センターで新しい顧客レコードを作成する場合、顧客の新しい Azure AD テナントを作成します。</span><span class="sxs-lookup"><span data-stu-id="151f1-108">If you create a new customer record for the customer in Microsoft Partner Center, you create a new Azure AD tenant for the customer.</span></span>

- <span data-ttu-id="151f1-109">定期売買が購入された後、顧客は Azure AD テナントの構造を変更します。</span><span class="sxs-lookup"><span data-stu-id="151f1-109">The customer changes the structure of the Azure AD tenant after the subscription is purchased.</span></span>

<span data-ttu-id="151f1-110">定期購読および関連するすべてのコンポーネントの移動のプロセスには、次の図に示すように、次の 4 つの主要なステップがあります。</span><span class="sxs-lookup"><span data-stu-id="151f1-110">The process for moving your subscriptions and all related artifacts has four main steps, as shown in the following illustration.</span></span>

![定期売買を移動するためのプロセス](./media/move-subscription-process.png)

## <a name="activate-subscriptions-on-the-new-tenant"></a><span data-ttu-id="151f1-112">新しいテナントのサブスクリプションを有効化</span><span class="sxs-lookup"><span data-stu-id="151f1-112">Activate subscriptions on the new tenant</span></span>
<span data-ttu-id="151f1-113">クラウド サービス プロバイダまたはボリューム ライセンスの再販業者と協力して、新しい Azure AD テナントに対するサブスクリプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="151f1-113">Work with your cloud service provider or volume license reseller to activate the subscriptions against the new Azure AD tenant.</span></span> <span data-ttu-id="151f1-114">ユーザーおよびアドオン環境のすべてのサブスクリプションを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="151f1-114">All subscriptions for users, and for add-on environments, must be activated.</span></span>

### <a name="cloud-service-provider"></a><span data-ttu-id="151f1-115">クラウド サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="151f1-115">Cloud service provider</span></span>
<span data-ttu-id="151f1-116">Microsoft クラウド ソリューション プロバイダー (CSP) 契約を通じてライセンスを取得している場合は、クラウド サービス プロバイダーから新しいテナントに対して必要なサブスクリプションを購入してください。</span><span class="sxs-lookup"><span data-stu-id="151f1-116">If you're licensed through a Microsoft Cloud Solution Provider (CSP) agreement, purchase the required subscriptions against the new tenant from your cloud service provider.</span></span> <span data-ttu-id="151f1-117">新しいテナントが既に存在する場合、クラウド サービス プロバイダは、再販業者関係を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="151f1-117">If the new tenant already exists, the cloud service provider must request a reseller relationship.</span></span> <span data-ttu-id="151f1-118">または、パートナー センターのクラウド サービス プロバイダで必要な既定ドメイン名の新しい顧客を作成する必要があります**\*.onmicrosoft.com** (たとえば、**contoso.onmicrosoft.com**)。</span><span class="sxs-lookup"><span data-stu-id="151f1-118">Alternatively, in Partner Center, the cloud service provider must create a new customer that has the desired default domain name, **\*.onmicrosoft.com** (for example, **contoso.onmicrosoft.com**).</span></span>

<span data-ttu-id="151f1-119">クラウド サービス プロバイダーに、今回は既存のサブスクリプションを中断しないよう依頼します。</span><span class="sxs-lookup"><span data-stu-id="151f1-119">Ask the cloud service provider not to suspend the existing subscriptions at this time.</span></span>

### <a name="volume-licensing"></a><span data-ttu-id="151f1-120">ボリューム ライセンス</span><span class="sxs-lookup"><span data-stu-id="151f1-120">Volume Licensing</span></span>
<span data-ttu-id="151f1-121">Microsoft ボリューム ライセンス契約を通じてライセンスを取得している場合は、[ボリューム ライセンス サポート センター](https://www.microsoft.com/Licensing/servicecenter/Help/Contact.aspx)に連絡し、サブスクリプションを古いテナントから新しいテナントに再マップするように依頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="151f1-121">If you're licensed through a Microsoft Volume Licensing agreement, you must call the [Volume Licensing support center](https://www.microsoft.com/Licensing/servicecenter/Help/Contact.aspx) and ask that the subscriptions be remapped from the old tenant to the new tenant.</span></span> <span data-ttu-id="151f1-122">Microsoft Office 365 管理センターからボリューム ライセンスのサポートに連絡することができます。</span><span class="sxs-lookup"><span data-stu-id="151f1-122">You can contact Volume Licensing Support through Microsoft Office 365 Admin center.</span></span> <span data-ttu-id="151f1-123">定期売買が両方のテナントで有効になると、支払猶予期間を要求します。</span><span class="sxs-lookup"><span data-stu-id="151f1-123">Request a grace period, when the subscriptions will be active on both tenants.</span></span> <span data-ttu-id="151f1-124">顧客プライバシーの問題が原因で、顧客がこの要求を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="151f1-124">Because of customer privacy concerns, this request must be made by the customer.</span></span> <span data-ttu-id="151f1-125">次の情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="151f1-125">You should have the following information available:</span></span>

- <span data-ttu-id="151f1-126">公的顧客番号</span><span class="sxs-lookup"><span data-stu-id="151f1-126">Public customer number</span></span>
- <span data-ttu-id="151f1-127">登録番号</span><span class="sxs-lookup"><span data-stu-id="151f1-127">Enrollment number</span></span>
- <span data-ttu-id="151f1-128">現在プロビジョニングされている定期売買の現在のテナント ドメイン</span><span class="sxs-lookup"><span data-stu-id="151f1-128">The current tenant domain that the subscriptions are currently provisioned on</span></span>
- <span data-ttu-id="151f1-129">顧客が定期売買のプロビジョニングを希望する宛先テナント ドメイン</span><span class="sxs-lookup"><span data-stu-id="151f1-129">The destination tenant domain that the customer wants the subscriptions provisioned under</span></span>
- <span data-ttu-id="151f1-130">顧客が違うテナントに移行したボリューム ライセンス サブスクリプションを必要とする理由の詳細説明</span><span class="sxs-lookup"><span data-stu-id="151f1-130">A detailed explanation of why the customer must have its Volume Licensing subscriptions migrated to a different tenant</span></span>
- <span data-ttu-id="151f1-131">新しいテナントに移動しなければならない有料サブスクリプションの総数、サブスクリプション タイプおよび定員数</span><span class="sxs-lookup"><span data-stu-id="151f1-131">The total number of paid subscriptions that must be moved to the new tenant, together with the subscription type and seat count</span></span>

> [!IMPORTANT]
> <span data-ttu-id="151f1-132">古いテナントで LCS の廃棄が完了するまでの数週間、定期売買が両方のテナントで並行して有効であることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="151f1-132">It's crucial that the subscriptions be active on both tenants in parallel for a few weeks, until you've finished decommissioning LCS on the old tenant.</span></span>

## <a name="configure-lcs-on-the-new-tenant"></a><span data-ttu-id="151f1-133">新しいテナントに LCS をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="151f1-133">Configure LCS on the new tenant</span></span>
<span data-ttu-id="151f1-134">新しいテナントで、開始し設定する必要がある新しい LCS プロジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="151f1-134">On the new tenant, you will get a new LCS project that you must initiate and set up.</span></span>

1. <span data-ttu-id="151f1-135">LCS を完全に構成します。</span><span class="sxs-lookup"><span data-stu-id="151f1-135">Fully configure LCS.</span></span> <span data-ttu-id="151f1-136">コンフィギュレーションの一部として、ユーザー、Microsoft Visual Studio Team Services (VSTS) アソシエーション、サブスクリプション見積り、アセット ライブラリおよびビジネス プロセス モデラー (BPM) などを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="151f1-136">As part of this configuration, you must add users, a Microsoft Visual Studio Team Services (VSTS) association, subscription estimates, the Asset library, Business process modeler (BPM), and so on.</span></span>
2. <span data-ttu-id="151f1-137">新しい LCS プロジェクトのすべての非運用環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="151f1-137">Deploy all non-production environments in the new LCS project.</span></span>
3. <span data-ttu-id="151f1-138">必要なコード パッケージを環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="151f1-138">Apply the required code packages to the environments.</span></span>
4. <span data-ttu-id="151f1-139">環境にデータをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="151f1-139">Upload data to the environments.</span></span> <span data-ttu-id="151f1-140">データ パッケージを使用してデータを移動することも、データベースを復元することもできます。</span><span class="sxs-lookup"><span data-stu-id="151f1-140">You can move the data through data packages or by restoring the database.</span></span> <span data-ttu-id="151f1-141">データベースを復元する場合は、いくつかのプロパティを新しいテナントに再マップするために追加の手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="151f1-141">If you restore the database, additional steps are required in order to remap some properties to the new tenant.</span></span>
5. <span data-ttu-id="151f1-142">ユーザー情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="151f1-142">Update your user information.</span></span>

    1. <span data-ttu-id="151f1-143">管理者ユーザーを除くすべてのユーザー アカウントを削除します。</span><span class="sxs-lookup"><span data-stu-id="151f1-143">Remove all user accounts except the admin user.</span></span>
    2. <span data-ttu-id="151f1-144">USERINFO の管理者ユーザー レコードを修正します。</span><span class="sxs-lookup"><span data-stu-id="151f1-144">Fix the admin user record in USERINFO.</span></span>

        ```
        UPDATE USERINFO
        SET SID='mysid', NETWORKALIAS='myalias/email', NETWORKDOMAIN='https://sts.windows.net'
        WHERE ID = 'Admin'
        ```

6. <span data-ttu-id="151f1-145">正しいセキュリティ識別子 (SID) および ID プロバイダーを持つ他のすべてのユーザーを再インポートします。</span><span class="sxs-lookup"><span data-stu-id="151f1-145">Re-import all other users that have the correct security identifier (SID) and identity provider.</span></span>
7. <span data-ttu-id="151f1-146">適切なテーブルでテナント ID を更新するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="151f1-146">Run the following commands to update the tenant ID in the appropriate tables:</span></span>

    - <span data-ttu-id="151f1-147">名前 = 'TENANTID' の際は SYSSERVICECONFIGURATIONSETTING から VALUE を選択します</span><span class="sxs-lookup"><span data-stu-id="151f1-147">select VALUE from SYSSERVICECONFIGURATIONSETTING where name = 'TENANTID'</span></span>
    - <span data-ttu-id="151f1-148">POWERBICONFIG から TENANTID を選択します</span><span class="sxs-lookup"><span data-stu-id="151f1-148">select TENANTID from POWERBICONFIG</span></span>
    - <span data-ttu-id="151f1-149">PROVISIONINGMESSAGETABLE から TENANTID を選択します</span><span class="sxs-lookup"><span data-stu-id="151f1-149">select TENANTID from PROVISIONINGMESSAGETABLE</span></span>
    - <span data-ttu-id="151f1-150">B2BINVITATIONCONFIG から TENANTID を選択します</span><span class="sxs-lookup"><span data-stu-id="151f1-150">select TENANTID from B2BINVITATIONCONFIG</span></span>
    - <span data-ttu-id="151f1-151">RETAILSHAREDPARAMETERS から TENANTID を選択します</span><span class="sxs-lookup"><span data-stu-id="151f1-151">select TENANTID from RETAILSHAREDPARAMETERS</span></span>

8. <span data-ttu-id="151f1-152">環境を完全に構成します。</span><span class="sxs-lookup"><span data-stu-id="151f1-152">Fully configure the environments.</span></span> <span data-ttu-id="151f1-153">この手順の一部として、統合のエンドポイントをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="151f1-153">As part of this step, configure the integration endpoints.</span></span>
9. <span data-ttu-id="151f1-154">新しい LCS プロジェクトのユーザー受け入れテスト (UAT) 環境でスモーク テストを実行します。</span><span class="sxs-lookup"><span data-stu-id="151f1-154">Perform smoke tests on the user acceptance testing (UAT) environment in the new LCS project.</span></span> <span data-ttu-id="151f1-155">これらのテストでは、ユーザーのサインイン、統合、ワークフロー、印刷、レポート、および構成やユーザー情報に依存する同様のプロセスに焦点を当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="151f1-155">These tests should focus on user sign-in, integrations, workflows, printing, reporting, and similar processes that depend on configuration and user information.</span></span>
10. <span data-ttu-id="151f1-156">実稼働環境を既に配置している場合は、すべてのサンドボックス環境の移動が終了し、UAT を完了した後に、新しいテナントに移動するためのサポート要求を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="151f1-156">If you already had a production environment deployed, you must open a support request to move it to the new tenant after you've finished moving all the sandbox environments and completed UAT.</span></span> <span data-ttu-id="151f1-157">実稼働環境を新しいテナントに移動するプロセスには、48 ～ 72 時間のダウンタイムの延長が必要です。</span><span class="sxs-lookup"><span data-stu-id="151f1-157">The process of moving a production environment to a new tenant requires an extended downtime of 48 to 72 hours.</span></span>

<span data-ttu-id="151f1-158">ソリューションとスコープに応じて、新しい Azure AD テナントで追加の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="151f1-158">Depending on your solution and scope, you might have to perform additional steps on the new Azure AD tenant.</span></span> <span data-ttu-id="151f1-159">これらの手順には、アプリケーションの登録 (定期的な統合と倉庫管理のため)、ドメインの追加、およびシングル サインオン (SSO) を有効にするディレクトリ同期の設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="151f1-159">These steps might include registering applications (for recurring integrations and warehouse management), adding domains, and setting up directory synchronization to enable single sign-on (SSO).</span></span>

<span data-ttu-id="151f1-160">Web サービスへの呼び出しが、環境の**ホーム**テナントからのみ許可されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="151f1-160">Note that calls to web services are allowed only from the **home** tenant for the environment.</span></span> <span data-ttu-id="151f1-161">たとえば、元のテナントは companya.com であり、統合は `services@companya.com` として実行されました。</span><span class="sxs-lookup"><span data-stu-id="151f1-161">For example, the original tenant was companya.com, and integration ran as `services@companya.com`.</span></span> <span data-ttu-id="151f1-162">この場合、テナントを companyb.com に切り替えると、**userInfo.networkdomain** を `https://sts.windows.net/companyb.com` に更新してもWeb サービスの呼び出しに対して `services@companya.com` を使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="151f1-162">In this case, when you switch tenants to companyb.com, you can no longer use `services@companya.com` for web service calls, even if you update **userInfo.networkdomain** to `https://sts.windows.net/companyb.com`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="151f1-163">この期間中、2 つの並列 LCS プロジェクトがあります。</span><span class="sxs-lookup"><span data-stu-id="151f1-163">During this period, you will have two parallel LCS projects.</span></span> <span data-ttu-id="151f1-164">LCS 内の**定期売買を使用可能**ページの LCS プロジェクトに関連付けられている Azure AD テナントの名前と ID を確認できます。</span><span class="sxs-lookup"><span data-stu-id="151f1-164">You can verify the name and ID of the Azure AD tenant that is associated with an LCS project on the **Subscriptions available** page in LCS.</span></span> <span data-ttu-id="151f1-165">Azure Blob Storage に保存されている添付ファイルを処理するドキュメントは失われます。</span><span class="sxs-lookup"><span data-stu-id="151f1-165">You will lose any document handling attachments that are stored in Azure Blob storage.</span></span>

## <a name="delete-environments-on-the-old-tenant"></a><span data-ttu-id="151f1-166">古いテナントの環境の削除</span><span class="sxs-lookup"><span data-stu-id="151f1-166">Delete environments on the old tenant</span></span>
<span data-ttu-id="151f1-167">新しい Azure AD テナントに対する新しい LCS プロジェクトが完全に機能した後、古い LCS プロジェクトで環境を停止、開放および削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="151f1-167">After the new LCS project against the new Azure AD tenant is fully functional, you must stop, deallocate, and delete the environments on the old LCS project.</span></span> <span data-ttu-id="151f1-168">完了したとき、**コンフィグレーション** ボタンは環境ごとに使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="151f1-168">When you've finished, the **Configure** button becomes available for each environment.</span></span> <span data-ttu-id="151f1-169">後で必要になる可能性のある残りのコンポーネントは、アセット ライブラリから保管する必要があります。</span><span class="sxs-lookup"><span data-stu-id="151f1-169">You should save any remaining artifacts from the Asset library that you might require later.</span></span> <span data-ttu-id="151f1-170">Microsoft は、顧客のアカウントを無効にし、サービスが長期間にわたって中断された後に顧客データを削除する権限を保有します。</span><span class="sxs-lookup"><span data-stu-id="151f1-170">Microsoft reserves the right to disable the customer's account and delete the customer data after the service has been suspended for an extended period.</span></span>

## <a name="suspend-subscriptions-on-the-old-tenant"></a><span data-ttu-id="151f1-171">古いテナントで定期売買を中断します。</span><span class="sxs-lookup"><span data-stu-id="151f1-171">Suspend subscriptions on the old tenant</span></span>
1. <span data-ttu-id="151f1-172">すべての環境が削除されると、必要な LCS コンポーネントを保存し、クラウド サービス プロバイダまたは Volume Licensing Support と協力して、以前の Azure AD テナントのすべてのライセンスを中断します。</span><span class="sxs-lookup"><span data-stu-id="151f1-172">After all the environments have been deleted, and you've saved the LCS artifacts that you require, work with your cloud service provider or Volume Licensing Support to suspend all the licenses on the old Azure AD tenant.</span></span>

    - <span data-ttu-id="151f1-173">**クラウド サービス プロバイダー:** 古いテナントに対して既存の定期売買を中断します。</span><span class="sxs-lookup"><span data-stu-id="151f1-173">**Cloud service provider:** Suspend the existing subscriptions against the old tenant.</span></span>
    - <span data-ttu-id="151f1-174">**ボリューム ライセンス サポート:** 作業が完了したこと、およびサブスクリプションが古いテナントに対してすぐ中断することを確認するボリューム ライセンス サポート センター。</span><span class="sxs-lookup"><span data-stu-id="151f1-174">**Volume Licensing Support:** Call the Volume Licensing support center to confirm that you've completed the work and that the subscriptions can now be suspended against the old tenant.</span></span>

2. <span data-ttu-id="151f1-175">古い LCS プロジェクトを削除するサポート チケットをファイルします。</span><span class="sxs-lookup"><span data-stu-id="151f1-175">File a support ticket to delete the old LCS project.</span></span>


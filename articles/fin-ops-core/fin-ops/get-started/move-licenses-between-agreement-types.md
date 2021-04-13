---
title: 契約タイプ間でライセンスを移動する
description: このトピックでは、契約タイプの間のライセンスを移動する方法について説明します。
author: ClaudiaBetz-Haubold
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0
ms.openlocfilehash: d76e4c16e551830698f2775554d7c4e18524bec8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750242"
---
# <a name="move-licenses-between-agreement-types"></a><span data-ttu-id="09548-103">契約タイプ間でライセンスを移動する</span><span class="sxs-lookup"><span data-stu-id="09548-103">Move licenses between agreement types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09548-104">場合によっては、もともと Microsoft クラウド サービス プロバイダー (CSP) 契約を通じてサブスクリプションを購入した顧客は、Microsoft Dynamics Lifecycle Services (LCS) 実装プロジェクトが作成された後に、Microsoft との Microsoft ボリューム ライセンス契約に変更することを決定します。</span><span class="sxs-lookup"><span data-stu-id="09548-104">Sometimes, a customer who originally purchased subscriptions through a Microsoft Cloud Service Provider (CSP) agreement decides to change to a Microsoft Volume Licensing agreement with Microsoft after the Microsoft Dynamics Lifecycle Services (LCS) Implementation project has been created.</span></span> <span data-ttu-id="09548-105">顧客は、本番稼働でプロジェクトが稼動した後でもこの変更を実行できます。</span><span class="sxs-lookup"><span data-stu-id="09548-105">The customer can make this change even after the project has gone live in production.</span></span>

<span data-ttu-id="09548-106">ごくまれに、もともと Microsoft とのボリューム ライセンス契約を通して定期売買を購入した顧客は CSP 契約への変更することを決めます。</span><span class="sxs-lookup"><span data-stu-id="09548-106">Less often, a customer who originally purchased the subscriptions through a Volume Licensing agreement with Microsoft decides to change to a CSP agreement.</span></span> <span data-ttu-id="09548-107">この場合、ボリューム ライセンス契約の更新日に合わせて変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09548-107">In this case, the change must align with the renewal date of the Volume Licensing agreement.</span></span>

<span data-ttu-id="09548-108">契約の 1 つのタイプから別のタイプへの定期売買契約の移動のプロセスは、主に商業プロセスです。</span><span class="sxs-lookup"><span data-stu-id="09548-108">The process of moving subscriptions from one type of agreement to another is primarily a commercial process.</span></span> <span data-ttu-id="09548-109">LCS 実装プロジェクトの技術的影響は最小限に抑えられています。</span><span class="sxs-lookup"><span data-stu-id="09548-109">The technical implications for the LCS Implementation project are minimal.</span></span>

> [!NOTE]
> <span data-ttu-id="09548-110">契約タイプ間のサブスクリプションの移動は、Azure Active Directory (Azure AD) テナントの移動と同じではありません。</span><span class="sxs-lookup"><span data-stu-id="09548-110">The movement of subscriptions between agreement types isn't the same as the movement of an Azure Active Directory (Azure AD) tenant.</span></span> <span data-ttu-id="09548-111">契約の契約上の変更により、 Azure AD テナントを移動する必要がある場合は、 [LCS 実装プロジェクトを別の Azure AD テナントに移動する](move-lcs-implementation-project-tenant.md) に記載されているプロセスにも従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="09548-111">If the contractual changes in the agreements require that an Azure AD tenant be moved, you must also follow the process that is described in [Move LCS implementation projects to different Azure AD tenants](move-lcs-implementation-project-tenant.md).</span></span>

<span data-ttu-id="09548-112">サブスクリプションには、運用環境とレベル 2 スタンダード承認テスト環境の 2 つの標準環境が付属しています。</span><span class="sxs-lookup"><span data-stu-id="09548-112">Subscriptions come with two standard environments: a production environment and a Tier-2 Standard Acceptance Test environment.</span></span> <span data-ttu-id="09548-113">これらの環境は、契約タイプ間のサブスクリプションの移動の影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="09548-113">These environments aren't affected by the movement of subscriptions between agreement types.</span></span> <span data-ttu-id="09548-114">アクションは、顧客が追加アドオン環境を持っている場合にのみ、LCS で必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="09548-114">Action might be required in LCS only if the customer has additional add-on environments.</span></span> <span data-ttu-id="09548-115">この場合、アドオン環境に関連付けられているアクションには、パートナーまたは顧客リソースの側で最小限の作業量が必要になります。</span><span class="sxs-lookup"><span data-stu-id="09548-115">In this case, action that is related to the add-on environments requires minimal effort on the part of partner or customer resources.</span></span> <span data-ttu-id="09548-116">環境間でデータの移動を効率化するには、最適な順序を決定するために前もって計画を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09548-116">To streamline the movement of data between environments, you should plan in advance to determine the best sequence.</span></span>

## <a name="the-customer-has-only-default-environments"></a><span data-ttu-id="09548-117">顧客には既定の環境のみがあります</span><span class="sxs-lookup"><span data-stu-id="09548-117">The customer has only default environments</span></span>

<span data-ttu-id="09548-118">顧客が Microsoft が管理するサブスクリプションに付属している 2 つの標準環境のみを持ち、元の CPS 契約またはボリューム ライセンス契約でアドオン環境を購入していない場合、必要な活動は純粋に商業的なものです。</span><span class="sxs-lookup"><span data-stu-id="09548-118">If the customer has only the two standard environments that come with the Microsoft-managed subscription, and didn't purchase any add-on environments through the original CSP agreement or Volume Licensing agreement, the activities that are required are purely commercial.</span></span>

1. <span data-ttu-id="09548-119">顧客は、ボリューム ライセンスの再販業者または CSP との新しい契約の下で定期売買を注文します。</span><span class="sxs-lookup"><span data-stu-id="09548-119">The customer places the order for subscriptions under the new agreement with the Volume Licensing reseller or the CSP.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="09548-120">元の契約で使用される同じ Azure AD テナントに対してサブスクリプションが購入されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="09548-120">Make sure that the subscriptions are purchased against the same Azure AD tenant that is used on the original agreement.</span></span>

2. <span data-ttu-id="09548-121">顧客によって定期売買が有効化されます。</span><span class="sxs-lookup"><span data-stu-id="09548-121">The customer activates the subscriptions.</span></span>
3. <span data-ttu-id="09548-122">Microsoft 365 管理センターで、顧客は新規のサブスクリプションおよび既存のサブスクリプションの両方が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="09548-122">In Microsoft 365 Admin center, the customer verifies that both the new and subscriptions and the existing subscriptions are active.</span></span>
4. <span data-ttu-id="09548-123">新しいサブスクリプションが有効になると、顧客は、ボリューム ライセンスの再販業者または CSP が既存のサブスクリプションを中断することを要求します。</span><span class="sxs-lookup"><span data-stu-id="09548-123">When the new subscriptions are active, the customer requests that the Volume Licensing reseller or the CSP suspend the existing subscriptions.</span></span> <span data-ttu-id="09548-124">通常、継続性を保証し、サービスの中断を回避するために重複があります。</span><span class="sxs-lookup"><span data-stu-id="09548-124">Typically, there is an overlap to help guarantee continuity and avoid disruption of service.</span></span>

## <a name="the-customer-has-add-on-environments"></a><span data-ttu-id="09548-125">顧客にはアドオン環境があります</span><span class="sxs-lookup"><span data-stu-id="09548-125">The customer has add-on environments</span></span>

<span data-ttu-id="09548-126">顧客が、元の CSP 契約またはボリューム ライセンス契約を通じてアドオン環境を購入した場合、それらの環境を再配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09548-126">If the customer purchased add-on environments through the original CSP agreement or Volume Licensing agreement, those environments should be redeployed.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="09548-127">必要条件</span><span class="sxs-lookup"><span data-stu-id="09548-127">Prerequisites</span></span>

<span data-ttu-id="09548-128">移動を開始する前に、次のタスクを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="09548-128">Before you begin the move, you must complete the following tasks:</span></span>

- <span data-ttu-id="09548-129">既存の環境からデータを保存します。</span><span class="sxs-lookup"><span data-stu-id="09548-129">Save the data from your existing environments.</span></span> <span data-ttu-id="09548-130">[データベース移動操作ホーム ページ](../../dev-itpro/database/dbmovement-operations.md) に記載されているオプションのいずれかに従います。</span><span class="sxs-lookup"><span data-stu-id="09548-130">Follow one of the options described in [Database movement operations home page](../../dev-itpro/database/dbmovement-operations.md).</span></span>

- <span data-ttu-id="09548-131">コードのすべてのパッケージが LCS で共有アセット ライブラリにアップロードされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="09548-131">Verify that all code packages have been uploaded to the Shared asset library in LCS.</span></span>

### <a name="commercial-activities"></a><span data-ttu-id="09548-132">商業活動</span><span class="sxs-lookup"><span data-stu-id="09548-132">Commercial activities</span></span>

1. <span data-ttu-id="09548-133">顧客は、ボリューム ライセンスの再販業者または CSP との新しい契約の下で定期売買を注文します。</span><span class="sxs-lookup"><span data-stu-id="09548-133">The customer places the order for the subscriptions under the new agreement with the Volume Licensing reseller or the CSP.</span></span> <span data-ttu-id="09548-134">これらのサブスクリプションには、アドオン環境のサブスクリプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="09548-134">These subscriptions include the subscriptions for the add-on environments.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="09548-135">既存の Azure AD テナントに対してサブスクリプションが購入されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="09548-135">Make sure that the subscriptions are purchased against the existing Azure AD tenant.</span></span>

2. <span data-ttu-id="09548-136">顧客によって定期売買が有効化されます。</span><span class="sxs-lookup"><span data-stu-id="09548-136">The customer activates the subscriptions.</span></span>
3. <span data-ttu-id="09548-137">Microsoft 365 管理センターで、顧客は新規のサブスクリプションおよび既存のサブスクリプションの両方が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="09548-137">In Microsoft 365 Admin center, the customer verifies that both the new subscriptions and the existing subscriptions are active.</span></span>

### <a name="deploy-new-environments"></a><span data-ttu-id="09548-138">新しい環境の配置</span><span class="sxs-lookup"><span data-stu-id="09548-138">Deploy new environments</span></span>

1. <span data-ttu-id="09548-139">新しいサブスクリプションが有効になると、コンフィグレーション可能な追加のアドオン環境が LCS に表示されます。</span><span class="sxs-lookup"><span data-stu-id="09548-139">When the new subscriptions are active, additional add-on environments that you can configure appear in LCS.</span></span> <span data-ttu-id="09548-140">アドオン環境を配置し、適切に構成します。</span><span class="sxs-lookup"><span data-stu-id="09548-140">Deploy the add-on environments, and configure them as appropriate.</span></span>
2. <span data-ttu-id="09548-141">配置可能なパッケージを適用して、データを復元します。</span><span class="sxs-lookup"><span data-stu-id="09548-141">Apply the deployable packages, and restore the data.</span></span>

### <a name="delete-environments-under-the-obsolete-agreement"></a><span data-ttu-id="09548-142">廃止された契約下の環境の削除</span><span class="sxs-lookup"><span data-stu-id="09548-142">Delete environments under the obsolete agreement</span></span>

<span data-ttu-id="09548-143">古い契約下で配置されたすべての環境で、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="09548-143">Follow these steps for every environment that was deployed under the old agreement.</span></span> <span data-ttu-id="09548-144">環境を削除した後、再び使用したり再配置したりしないでください。</span><span class="sxs-lookup"><span data-stu-id="09548-144">After you've deleted the environments, don't use or redeploy them again.</span></span>

1. <span data-ttu-id="09548-145">LCS の、**環境の詳細** ページで、**完全な詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09548-145">In LCS, on the **Environment details** page, select **Full details**.</span></span>
2. <span data-ttu-id="09548-146">環境を停止してから、環境が停止した時に、**割り当て解除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09548-146">Stop the environment, and when the environment has stopped, select **Deallocate**.</span></span>
3. <span data-ttu-id="09548-147">割り当て解除が完了したとき、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09548-147">When the deallocation is completed, select **Delete**.</span></span>
4. <span data-ttu-id="09548-148">環境が削除されたら、**コンフィグレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="09548-148">When the environment has been deleted, select **Configure**.</span></span>

### <a name="update-environments"></a><span data-ttu-id="09548-149">環境の更新</span><span class="sxs-lookup"><span data-stu-id="09548-149">Update environments</span></span>

1. <span data-ttu-id="09548-150">ボリューム ライセンスの再販業者または CSP は、既存の定期売買を中断します。</span><span class="sxs-lookup"><span data-stu-id="09548-150">The Volume Licensing reseller or the CSP suspends the existing subscriptions.</span></span>
2. <span data-ttu-id="09548-151">元のアドオン環境は、LCS に表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="09548-151">Any original add-on environments no longer appear in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="09548-152">アドオン環境の物理的な再配置が完了するまでは、有効な状態にで既存の定期売買と新しい定期売買の両方をアクティブな状態に保つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="09548-152">Until physical redeployment of the add-on environments is completed, both existing subscriptions and new subscriptions must be kept in an active state.</span></span>

> - <span data-ttu-id="09548-153">サンド ボックス環境では、Azure BLOB ストレージに格納されているファイルの移動はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="09548-153">The movement of files that are stored in Azure Blob storage isn't supported in sandbox environments.</span></span>
> - <span data-ttu-id="09548-154">コマース顧客は、移動後にコンポーネントが正常に機能するため追加の手順が必要であることに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09548-154">Commerce customers should be aware that extra steps are required in order for components to work correctly after the move.</span></span> <span data-ttu-id="09548-155">詳細については、 [データ管理の概要](../../dev-itpro/data-entities/data-entities-data-packages.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09548-155">For more information, see [Data management overview](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
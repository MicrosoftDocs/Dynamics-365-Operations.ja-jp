---
title: Go-Live に関するよく寄せられる質問
description: このトピックでは、Dynamics 365 Human Resources 実装プロジェクトの Go-Live についてよく寄せられる質問を一覧表示します。
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64a85840be328702a06779390fe383fd1896fd04
ms.sourcegitcommit: d66fd72342931fad25a696b251c05781280d36c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2020
ms.locfileid: "4011426"
---
# <a name="go-live-faq"></a><span data-ttu-id="c4843-103">Go-Live に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="c4843-103">Go-live FAQ</span></span> 

<span data-ttu-id="c4843-104">このトピックでは、Dynamics 365 Human Resources 実装プロジェクトの Go-Live についてよく寄せられる質問を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="c4843-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="c4843-105">実稼働環境をいつ構成および要求できますか ?</span><span class="sxs-lookup"><span data-stu-id="c4843-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="c4843-106">一般に、次の基準を満たすことによって、運用環境が展開されます :</span><span class="sxs-lookup"><span data-stu-id="c4843-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="c4843-107">すべてのカスタマイズのコードが完了していること。</span><span class="sxs-lookup"><span data-stu-id="c4843-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="c4843-108">ユーザー受け入れテスト (UAT) が完了していること。</span><span class="sxs-lookup"><span data-stu-id="c4843-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="c4843-109">顧客がソリューションと UAT にサインオフしている。</span><span class="sxs-lookup"><span data-stu-id="c4843-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="c4843-110">Go-live にあたってブロッキングの問題がないこと。</span><span class="sxs-lookup"><span data-stu-id="c4843-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="c4843-111">対象の顧客がこの段階にある場合、Microsoft FastTrack チームはプロジェクトチームと協力して Go-live の評価を行います。</span><span class="sxs-lookup"><span data-stu-id="c4843-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="c4843-112">運用環境を展開するための前提条件</span><span class="sxs-lookup"><span data-stu-id="c4843-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="c4843-113">前提条件の一覧については、  [Go-Live の準備](hr-admin-go-live-prepare.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4843-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="c4843-114">運用運用に関する評価について</span><span class="sxs-lookup"><span data-stu-id="c4843-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="c4843-115">Go-live 評価/レビューは、 [Microsoft FastTrack プログラム](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview)の一部です。</span><span class="sxs-lookup"><span data-stu-id="c4843-115">The go-live assessment is part of the [Microsoft FastTrack program](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> <span data-ttu-id="c4843-116">レビュー中に、ソリューション アーキテクトは、実装プロジェクトが成功した切替および Go-live の準備が整っているかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="c4843-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="c4843-117">このレビューは、実稼働環境で準備を開始する前に、すべての実装プロジェクトで必須です。</span><span class="sxs-lookup"><span data-stu-id="c4843-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="c4843-118">当社のサンドボックス環境は、米国中部のデータセンターに配置されています。</span><span class="sxs-lookup"><span data-stu-id="c4843-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="c4843-119">運用環境を米国西部のデータセンターに展開したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="c4843-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="c4843-120">運用環境の構成で、データ センターに米国西部を選択できますか？</span><span class="sxs-lookup"><span data-stu-id="c4843-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="c4843-121">LCS は、人事環境を導入する際に異なるデータセンターを選択することを制限しませんが、異なるデータセンターを選択しないことを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c4843-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="c4843-122">運用環境を米国西部のデータセンターに配置するには、まずサンドボックス環境を米国西部のデータセンターに再展開してテストし、サインオフする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4843-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="c4843-123">適切なデータセンターを選択する方法については、[ネットワーク要件](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4843-123">For information about selecting the correct datacenter, see [Network requirements](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="c4843-124">人事環境では、Azureリソースに対してどのレベルのアクセス許可が必要ですか？</span><span class="sxs-lookup"><span data-stu-id="c4843-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="c4843-125">人事環境へのアクセスは制限されています。</span><span class="sxs-lookup"><span data-stu-id="c4843-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="c4843-126">仮想マシン (VM) または Microsoft インターネット インフォメーション サービス (IIS) にアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c4843-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="c4843-127">また、Microsoft SQL Server Management Studio 経由でデータベースにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c4843-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="c4843-128">Azureリソースや Dynamics 365 Human Resources 環境に直接アクセスすることはできませんが 、データへのアクセスに使用できる追加機能があります。</span><span class="sxs-lookup"><span data-stu-id="c4843-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="c4843-129">Azure SQL データベースを独自の Azure テナントに展開し、BYOD (Bring Your Own Device) 機能を使用してデータを同期させることができます。</span><span class="sxs-lookup"><span data-stu-id="c4843-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="c4843-130">詳細については、[独自のデータベースを導入する (byod)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4843-130">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span>

- <span data-ttu-id="c4843-131">Common Data Service の統合を使用して、選択したエンティティを Common Data Service データベースに同期することができます。</span><span class="sxs-lookup"><span data-stu-id="c4843-131">You can use Common Data Service integration to synchronize select entities into the Common Data Service database.</span></span> <span data-ttu-id="c4843-132">詳細については、[Common Data Service エンティティ](hr-developer-entities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4843-132">For more information, see [Common Data Service entities](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="c4843-133">どのくらいの頻度で生産データベースがバックアップされますか。</span><span class="sxs-lookup"><span data-stu-id="c4843-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="c4843-134">データベースは、以下の頻度で自動バックアップで保護されます :</span><span class="sxs-lookup"><span data-stu-id="c4843-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="c4843-135">バックアップのタイプ</span><span class="sxs-lookup"><span data-stu-id="c4843-135">Type of backup</span></span> | <span data-ttu-id="c4843-136">頻度</span><span class="sxs-lookup"><span data-stu-id="c4843-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="c4843-137">データベースのフル バックアップ</span><span class="sxs-lookup"><span data-stu-id="c4843-137">Full database backup</span></span> | <span data-ttu-id="c4843-138">毎週</span><span class="sxs-lookup"><span data-stu-id="c4843-138">Weekly</span></span> |
| <span data-ttu-id="c4843-139">データベースの差分バックアップ</span><span class="sxs-lookup"><span data-stu-id="c4843-139">Differential database backup</span></span> | <span data-ttu-id="c4843-140">12 - 24 時間ごと</span><span class="sxs-lookup"><span data-stu-id="c4843-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="c4843-141">トランザクション ログのバックアップ</span><span class="sxs-lookup"><span data-stu-id="c4843-141">Transaction log backup</span></span> | <span data-ttu-id="c4843-142">5 - 10 分ごと</span><span class="sxs-lookup"><span data-stu-id="c4843-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="c4843-143">Microsoftでは、過去 7 日間において、ポイントインタイム リストア (PITR) を可能にする十分なバックアップが保持されています。</span><span class="sxs-lookup"><span data-stu-id="c4843-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last seven days.</span></span> 

<span data-ttu-id="c4843-144">詳細については、 [SQL Database の自動バックアップについて](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4843-144">For more information, see [Learn about automatic SQL Database backups](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="c4843-145">生産データベースのバックアップのコピーを要求できますか。</span><span class="sxs-lookup"><span data-stu-id="c4843-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="c4843-146">No.</span><span class="sxs-lookup"><span data-stu-id="c4843-146">No.</span></span> <span data-ttu-id="c4843-147">ただし、運用環境をサンドボックス環境にコピーするデータベースの更新サービス リクエストを送信することはできます。</span><span class="sxs-lookup"><span data-stu-id="c4843-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="c4843-148">Azure SQL データベースを独自の Azure テナントに展開し、BYOD 機能を使用して運用環境からデータを同期させることができます。</span><span class="sxs-lookup"><span data-stu-id="c4843-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="c4843-149">詳細については、[独自のデータベースを導入する (byod)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4843-149">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="c4843-150">サンドボックス環境を運用稼働環境に移行する方法について</span><span class="sxs-lookup"><span data-stu-id="c4843-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="c4843-151">環境をサンドボックスから運用環境に移動するコピー機能は使用できないため、データパッケージを使用してデータを運用環境に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4843-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="c4843-152">プロジェクト全体にわたってサンドボックスで構成されているエンティティの一覧を明確にしておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c4843-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="c4843-153">次に、go-live に必要なデータパッケージのカットオーバーと移行のプロセスをテストします。</span><span class="sxs-lookup"><span data-stu-id="c4843-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="c4843-154">運用環境の準備ができたら、データパッケージを手動で運用環境に移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4843-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="c4843-155">運用環境がダウンした場合の対応について</span><span class="sxs-lookup"><span data-stu-id="c4843-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="c4843-156">運用環境の稼働不能状態を報告するには、  [稼働停止のレポート](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage) で説明されているプロセスに従います。</span><span class="sxs-lookup"><span data-stu-id="c4843-156">To report a Production outage, follow the process described in [Report a production outage](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="c4843-157">参照</span><span class="sxs-lookup"><span data-stu-id="c4843-157">See also</span></span>

 [<span data-ttu-id="c4843-158">Go-Live の準備</span><span class="sxs-lookup"><span data-stu-id="c4843-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)
---
title: Go-Live に関するよく寄せられる質問
description: このトピックでは、Dynamics 365 Human Resources 実装プロジェクトの Go-Live についてよく寄せられる質問を一覧表示します。
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e1b4b336953ef6bd74da009b3bb44fbcf2eab5a8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892326"
---
# <a name="go-live-faq"></a><span data-ttu-id="ab7c8-103">Go-Live に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ab7c8-103">Go-live FAQ</span></span> 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ab7c8-104">このトピックでは、Dynamics 365 Human Resources 実装プロジェクトの Go-Live についてよく寄せられる質問を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="ab7c8-105">実稼働環境をいつ構成および要求できますか ?</span><span class="sxs-lookup"><span data-stu-id="ab7c8-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="ab7c8-106">一般に、次の基準を満たすことによって、運用環境が展開されます :</span><span class="sxs-lookup"><span data-stu-id="ab7c8-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="ab7c8-107">すべてのカスタマイズのコードが完了していること。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="ab7c8-108">ユーザー受け入れテスト (UAT) が完了していること。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="ab7c8-109">顧客がソリューションと UAT にサインオフしている。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="ab7c8-110">Go-live にあたってブロッキングの問題がないこと。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="ab7c8-111">対象の顧客がこの段階にある場合、Microsoft FastTrack チームはプロジェクトチームと協力して Go-live の評価を行います。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="ab7c8-112">運用環境を展開するための前提条件</span><span class="sxs-lookup"><span data-stu-id="ab7c8-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="ab7c8-113">前提条件の一覧については、  [Go-Live の準備](hr-admin-go-live-prepare.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="ab7c8-114">運用運用に関する評価について</span><span class="sxs-lookup"><span data-stu-id="ab7c8-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="ab7c8-115">Go-live 評価/レビューは、 [Microsoft FastTrack プログラム](/dynamics365/fasttrack/)の一部です。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-115">The go-live assessment is part of the [Microsoft FastTrack program](/dynamics365/fasttrack/).</span></span> <span data-ttu-id="ab7c8-116">レビュー中に、ソリューション アーキテクトは、実装プロジェクトが成功した切替および Go-live の準備が整っているかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="ab7c8-117">このレビューは、実稼働環境で準備を開始する前に、すべての実装プロジェクトで必須です。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="ab7c8-118">当社のサンドボックス環境は、米国中部のデータセンターに配置されています。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="ab7c8-119">運用環境を米国西部のデータセンターに展開したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="ab7c8-120">運用環境の構成で、データ センターに米国西部を選択できますか？</span><span class="sxs-lookup"><span data-stu-id="ab7c8-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="ab7c8-121">LCS は、人事環境を導入する際に異なるデータセンターを選択することを制限しませんが、異なるデータセンターを選択しないことを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="ab7c8-122">運用環境を米国西部のデータセンターに配置するには、まずサンドボックス環境を米国西部のデータセンターに再展開してテストし、サインオフする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="ab7c8-123">適切なデータセンターを選択する方法については、[ネットワーク要件](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-123">For information about selecting the correct datacenter, see [Network requirements](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="ab7c8-124">人事環境では、Azureリソースに対してどのレベルのアクセス許可が必要ですか？</span><span class="sxs-lookup"><span data-stu-id="ab7c8-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="ab7c8-125">人事環境へのアクセスは制限されています。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="ab7c8-126">仮想マシン (VM) または Microsoft インターネット インフォメーション サービス (IIS) にアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="ab7c8-127">また、Microsoft SQL Server Management Studio 経由でデータベースにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="ab7c8-128">Azureリソースや Dynamics 365 Human Resources 環境に直接アクセスすることはできませんが 、データへのアクセスに使用できる追加機能があります。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="ab7c8-129">Azure SQL データベースを独自の Azure テナントに展開し、BYOD (Bring Your Own Device) 機能を使用してデータを同期させることができます。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="ab7c8-130">詳細については、[独自のデータベースを導入する (byod)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-130">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span>

- <span data-ttu-id="ab7c8-131">Dataverse の統合を使用して、選択したエンティティを Dataverse データベースに同期することができます。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="ab7c8-132">詳細については、[Dataverse の表](hr-developer-entities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="ab7c8-133">どのくらいの頻度で生産データベースがバックアップされますか。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="ab7c8-134">データベースは、以下の頻度で自動バックアップで保護されます :</span><span class="sxs-lookup"><span data-stu-id="ab7c8-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="ab7c8-135">バックアップのタイプ</span><span class="sxs-lookup"><span data-stu-id="ab7c8-135">Type of backup</span></span> | <span data-ttu-id="ab7c8-136">頻度</span><span class="sxs-lookup"><span data-stu-id="ab7c8-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="ab7c8-137">データベースのフル バックアップ</span><span class="sxs-lookup"><span data-stu-id="ab7c8-137">Full database backup</span></span> | <span data-ttu-id="ab7c8-138">毎週</span><span class="sxs-lookup"><span data-stu-id="ab7c8-138">Weekly</span></span> |
| <span data-ttu-id="ab7c8-139">データベースの差分バックアップ</span><span class="sxs-lookup"><span data-stu-id="ab7c8-139">Differential database backup</span></span> | <span data-ttu-id="ab7c8-140">12 - 24 時間ごと</span><span class="sxs-lookup"><span data-stu-id="ab7c8-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="ab7c8-141">トランザクション ログのバックアップ</span><span class="sxs-lookup"><span data-stu-id="ab7c8-141">Transaction log backup</span></span> | <span data-ttu-id="ab7c8-142">5 - 10 分ごと</span><span class="sxs-lookup"><span data-stu-id="ab7c8-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="ab7c8-143">マイクロソフトでは、過去 14 日間において、ポイントインタイム リストア (PITR) を可能にする十分なバックアップが保持されています。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="ab7c8-144">詳細については、 [SQL Database の自動バックアップについて](/azure/azure-sql/database/automated-backups-overview?tabs=single-database) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-144">For more information, see [Learn about automatic SQL Database backups](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="ab7c8-145">生産データベースのバックアップのコピーを要求できますか。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="ab7c8-146">No.</span><span class="sxs-lookup"><span data-stu-id="ab7c8-146">No.</span></span> <span data-ttu-id="ab7c8-147">ただし、運用環境をサンドボックス環境にコピーするデータベースの更新サービス リクエストを送信することはできます。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="ab7c8-148">Azure SQL データベースを独自の Azure テナントに展開し、BYOD 機能を使用して運用環境からデータを同期させることができます。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="ab7c8-149">詳細については、[独自のデータベースを導入する (byod)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-149">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="ab7c8-150">サンドボックス環境を運用稼働環境に移行する方法について</span><span class="sxs-lookup"><span data-stu-id="ab7c8-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="ab7c8-151">環境をサンドボックスから運用環境に移動するコピー機能は使用できないため、データパッケージを使用してデータを運用環境に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="ab7c8-152">プロジェクト全体にわたってサンドボックスで構成されているエンティティの一覧を明確にしておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="ab7c8-153">次に、go-live に必要なデータパッケージのカットオーバーと移行のプロセスをテストします。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="ab7c8-154">運用環境の準備ができたら、データパッケージを手動で運用環境に移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="ab7c8-155">運用環境がダウンした場合の対応について</span><span class="sxs-lookup"><span data-stu-id="ab7c8-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="ab7c8-156">運用環境の稼働不能状態を報告するには、  [稼働停止のレポート](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md) で説明されているプロセスに従います。</span><span class="sxs-lookup"><span data-stu-id="ab7c8-156">To report a Production outage, follow the process described in [Report a production outage](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="ab7c8-157">参照</span><span class="sxs-lookup"><span data-stu-id="ab7c8-157">See also</span></span>

 [<span data-ttu-id="ab7c8-158">Go-Live の準備</span><span class="sxs-lookup"><span data-stu-id="ab7c8-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
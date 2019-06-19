---
title: Finance and Operations の実装プロジェクトの Go-Live に関するよく寄せられる質問
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations プロジェクトの運用についてよく寄せられる質問を一覧表示します。
author: sshashi7
manager: AnnBe
ms.date: 02/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sshashi
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0072548f50afbd6f11257c1ff3906ce20e636fd1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546583"
---
# <a name="go-live-for-finance-and-operations-implementation-projects-faq"></a><span data-ttu-id="fab3a-103">Finance and Operations の実装プロジェクトの Go-Live に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="fab3a-103">Go-live for Finance and Operations implementation projects FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fab3a-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations プロジェクトの運用についてよく寄せられる質問を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="fab3a-104">This topic lists frequently asked questions about how to go live with a Microsoft Dynamics 365 for Finance and Operations project.</span></span>

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="fab3a-105">実稼働環境をいつ構成および要求できますか ?</span><span class="sxs-lookup"><span data-stu-id="fab3a-105">When can I configure and request my production environment?</span></span>

<span data-ttu-id="fab3a-106">通常、すべてのカスタマイズのコードが完了し、ユーザー受け入れテスト (UAT) が完了し、顧客がソリューションからサインオフし、稼働中にブロッキングの問題がない場合、実稼働環境が展開されます。</span><span class="sxs-lookup"><span data-stu-id="fab3a-106">Typically, a production environment is deployed after all customizations are code-complete, user acceptance testing (UAT) is completed, the customer has signed off on the solution, and there are no blocking issues for go-live.</span></span>

<span data-ttu-id="fab3a-107">お客様がこの段階にいるとき、Microsoft FastTrack チームはプロジェクトチームと連携して、Go-live 評価/レビューを行ういます。</span><span class="sxs-lookup"><span data-stu-id="fab3a-107">When you're at this stage, the Microsoft FastTrack team will work with the project team to do a Go-live assessment/review.</span></span>

## <a name="what-are-the-prerequisites-to-deploy-a-production-environment"></a><span data-ttu-id="fab3a-108">実稼働環境を配置するための前提条件</span><span class="sxs-lookup"><span data-stu-id="fab3a-108">What are the prerequisites to deploy a production environment?</span></span>

<span data-ttu-id="fab3a-109">前提条件の一覧については、[Go-Live の準備](prepare-go-live.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fab3a-109">For a list of the prerequisites, see [Preparing for Go-live](prepare-go-live.md).</span></span>

## <a name="what-is-a-go-live-assessmentreview-and-why-is-it-required"></a><span data-ttu-id="fab3a-110">起動の評価/レビューとは何ですか、またそれがなぜ必要ですか ?</span><span class="sxs-lookup"><span data-stu-id="fab3a-110">What is a Go-live assessment/review, and why is it required?</span></span>

<span data-ttu-id="fab3a-111">Go-live 評価/レビューは、[Microsoft FastTrack プログラム](../get-started/fasttrack-dynamics-365-overview.md)の一部です。</span><span class="sxs-lookup"><span data-stu-id="fab3a-111">The Go-live assessment/review is part of the [Microsoft FastTrack program](../get-started/fasttrack-dynamics-365-overview.md).</span></span> <span data-ttu-id="fab3a-112">レビュー中に、ソリューション アーキテクトは、実装プロジェクトが成功した切替および Go-live の準備が整っているかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="fab3a-112">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="fab3a-113">このレビューは、実稼働環境で準備を開始する前に、すべての Finance and Operations プロジェクトで必須です。</span><span class="sxs-lookup"><span data-stu-id="fab3a-113">This review is mandatory for every Finance and Operations project before you can request to go live in a production environment.</span></span>

## <a name="i-want-to-request-my-production-environment-who-do-i-contact-for-a-go-live-assessmentreview"></a><span data-ttu-id="fab3a-114">実稼働環境を要求します。</span><span class="sxs-lookup"><span data-stu-id="fab3a-114">I want to request my production environment.</span></span> <span data-ttu-id="fab3a-115">Go-live アセスメント/レビューのために誰に連絡しますか。</span><span class="sxs-lookup"><span data-stu-id="fab3a-115">Who do I contact for a Go-live assessment/review?</span></span>

<span data-ttu-id="fab3a-116">FastTrack ソリューション アーキテクトがプロジェクトに割り当てられている場合は、担当者に直接問い合わせます。</span><span class="sxs-lookup"><span data-stu-id="fab3a-116">If a FastTrack solution architect is assigned to your project, contact him or her directly.</span></span> <span data-ttu-id="fab3a-117">それ以外の場合、Microsoft Dynamics Lifecycle Services (LCS) に指定されている運用日付に基づいて、運用前チェックリストに記入し、運用日の数週間前に <go-live@microsoft.com> に送信するように指示する電子メールを受信します。</span><span class="sxs-lookup"><span data-stu-id="fab3a-117">Otherwise, based on the go-live date that is specified in Microsoft Dynamics Lifecycle Services (LCS), you will receive an email that instructs you to fill out the Pre-go-live checklist and send it to <go-live@microsoft.com> a few weeks before the go-live date.</span></span> <span data-ttu-id="fab3a-118">電子メールを受け取っておらず、稼働の準備ができている場合は、、[CustomerSource から稼働前のチェックリストをダウンロード](https://mbs.microsoft.com/customersource/Global/365Enterprise/learning/documentation/installation-setup-guides/fasttrack-checklist-fin-and-ops) して、それを完成させ、<go-live@microsoft.com> に送信します。</span><span class="sxs-lookup"><span data-stu-id="fab3a-118">If you haven't received an email, and you're ready for go-live, you can [download the Pre go-live checklist from CustomerSource](https://mbs.microsoft.com/customersource/Global/365Enterprise/learning/documentation/installation-setup-guides/fasttrack-checklist-fin-and-ops), complete it, and send it to <go-live@microsoft.com>.</span></span>

## <a name="the-production-button-isnt-available-in-lcs-how-do-i-request-my-production-environment"></a><span data-ttu-id="fab3a-119">生産ボタンは、LCS では使用できません。</span><span class="sxs-lookup"><span data-stu-id="fab3a-119">The Production button isn't available in LCS.</span></span> <span data-ttu-id="fab3a-120">実稼働環境を要求するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="fab3a-120">How do I request my production environment?</span></span>

<span data-ttu-id="fab3a-121">LCS の **生産** ボタンは、LCS 実装方法の **分析**、**デザイン & 開発**、および**テスト** フェースを完了した後にのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="fab3a-121">The **Production** button in LCS is available only after you've completed the **Analysis**, **Design & develop**, and **Test** phases of the LCS implementation methodology.</span></span> <span data-ttu-id="fab3a-122">これらのフェーズを完了する方法の詳細については、「[メソドロジ タスクおよびフェーズ](../../dev-itpro/lifecycle-services/lcs-works-lcs.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fab3a-122">For more information about how to complete these phases, see [Methodology tasks and phases](../../dev-itpro/lifecycle-services/lcs-works-lcs.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fab3a-123">実稼働環境は、運用の評価/レビューが完了するまで配置されません。</span><span class="sxs-lookup"><span data-stu-id="fab3a-123">Your production environment won't be deployed until the Go-live assessment/review has been completed.</span></span>

## <a name="my-sandbox-environment-is-currently-on-a-platform-update-that-is-set-to-expire-in-two-months-can-i-request-a-production-environment-that-has-the-latest-platform-update"></a><span data-ttu-id="fab3a-124">自分のサンドボックス環境は、現在有効期限が 2 か月に設定されているプラットフォーム更新プログラムにあります。</span><span class="sxs-lookup"><span data-stu-id="fab3a-124">My sandbox environment is currently on a platform update that is set to expire in two months.</span></span> <span data-ttu-id="fab3a-125">最新のプラットフォーム更新プログラムを含む実稼動環境を要求できますか。</span><span class="sxs-lookup"><span data-stu-id="fab3a-125">Can I request a production environment that has the latest platform update?</span></span>

<span data-ttu-id="fab3a-126">一連番号</span><span class="sxs-lookup"><span data-stu-id="fab3a-126">No.</span></span> <span data-ttu-id="fab3a-127">サンド ボックス環境と異なるバージョンにある実稼働環境に対する要求をすべて拒否します。</span><span class="sxs-lookup"><span data-stu-id="fab3a-127">We will deny any request for a production environment that is on a different version than your sandbox environment.</span></span> <span data-ttu-id="fab3a-128">実稼働環境をコンフィギュレーションするときは、選択したアプリケーションとプラットフォームのバージョンが、ソリューションを承認したサンド ボックス環境のアプリケーションとプラットフォームのバージョンと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fab3a-128">When you configure a production environment, the application and platform versions that you select must match the application and platform versions of the sandbox environment where you signed off on your solution.</span></span> <span data-ttu-id="fab3a-129">したがって、まず最新のプラットフォーム アップデートをサンドボックス環境に適用してテストし、サインオフする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fab3a-129">Therefore, you must first apply the latest platform update to your sandbox environment, test it, and sign off.</span></span>

<span data-ttu-id="fab3a-130">詳細については、「[バージョンと更新ポリシー](../../dev-itpro/migration-upgrade/versions-update-policy.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fab3a-130">For more information, see [Versions Update Policy](../../dev-itpro/migration-upgrade/versions-update-policy.md).</span></span>

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-but-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="fab3a-131">サンドボックス環境は、米国中部データセンターに配置されますが、生産環境は米国西部データセンターに配置する予定です。</span><span class="sxs-lookup"><span data-stu-id="fab3a-131">Our sandbox environments are deployed in the Central US datacenter, but we want our production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="fab3a-132">本番構成で、データ センターとして米国西部を選択できますか？</span><span class="sxs-lookup"><span data-stu-id="fab3a-132">Can I select West US as the datacenter in my production configuration?</span></span>

<span data-ttu-id="fab3a-133">一連番号</span><span class="sxs-lookup"><span data-stu-id="fab3a-133">No.</span></span> <span data-ttu-id="fab3a-134">サンド ボックス環境と異なるデータ センター内にある実稼働環境に対する要求をすべて拒否します。</span><span class="sxs-lookup"><span data-stu-id="fab3a-134">We will deny any request for a production environment that is in a different datacenter than your sandbox environment.</span></span> <span data-ttu-id="fab3a-135">すべての環境が同じデータ センターに配置されていることが必要です。</span><span class="sxs-lookup"><span data-stu-id="fab3a-135">We require that all your environments reside in the same datacenter.</span></span> <span data-ttu-id="fab3a-136">実稼働環境を米国西部データセンターに配置するには、まずサンドボックス環境を米国西部のデータセンターに再展開してテストし、サインオフする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fab3a-136">If you want your production environment to reside in the West US datacenter, you must first redeploy your sandbox environments to the West US datacenter, test them, and sign off.</span></span>

<span data-ttu-id="fab3a-137">正しいデータ センターを選択するのに役立つ情報の詳細については、「システム要件」トピックの [ネットワーク要件](../get-started/system-requirements.md#network-requirements) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fab3a-137">For information that can help you select the correct datacenter, see the [Network requirements](../get-started/system-requirements.md#network-requirements) section of the "System requirements" topic.</span></span>

## <a name="how-will-my-production-environment-be-sized"></a><span data-ttu-id="fab3a-138">実稼働環境はどのくらいの規模になりますか。</span><span class="sxs-lookup"><span data-stu-id="fab3a-138">How will my production environment be sized?</span></span>

<span data-ttu-id="fab3a-139">実稼働環境のサイズは、現在のユーザー ライセンス数と、実稼働環境を要求するときに有効なサブスクリプションの推定の情報に基づいて決まります。</span><span class="sxs-lookup"><span data-stu-id="fab3a-139">Your production environment will be sized based on the current user license count and the information in the subscription estimate that is active when you request the production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="fab3a-140">追加のユーザーを後で追加する場合は、新しいサブスクリプション推定をアクティブ化するためのサポート チケットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fab3a-140">If you add additional users later, you must create a support ticket to activate a new subscription estimate.</span></span> <span data-ttu-id="fab3a-141">実稼働環境のサイズは、ユーザー数、ユーザーのライセンスの種類、および予想されるピーク時のトランザクション量に応じて変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fab3a-141">Your production environment might have to be resized, depending on the number of users, the type of user licenses, and the expected peak transaction volume.</span></span> <span data-ttu-id="fab3a-142">ダウンタイムは、実稼働環境のサイズを変更するために必要です。</span><span class="sxs-lookup"><span data-stu-id="fab3a-142">Downtime is required in order to resize a production environment.</span></span>

## <a name="i-submitted-the-request-for-a-production-environment-but-i-made-a-mistake-can-i-still-change-it"></a><span data-ttu-id="fab3a-143">実稼働環境の要求を送信しましたが、間違いが発生しました。</span><span class="sxs-lookup"><span data-stu-id="fab3a-143">I submitted the request for a production environment, but I made a mistake.</span></span> <span data-ttu-id="fab3a-144">いまでも変更できますか。</span><span class="sxs-lookup"><span data-stu-id="fab3a-144">Can I still change it?</span></span>

<span data-ttu-id="fab3a-145">はい。</span><span class="sxs-lookup"><span data-stu-id="fab3a-145">Yes.</span></span> <span data-ttu-id="fab3a-146">実稼働環境のステータスが**キュー**に設定されている限り、サインオフ フラグをクリアし、変更、および再度サイン オフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="fab3a-146">As long as the status of the production environment is **Queued**, you can clear the sign-off flag, make changes, and then sign off again.</span></span>

## <a name="how-long-does-it-take-to-deploy-my-production-environment"></a><span data-ttu-id="fab3a-147">実稼働環境を配置するにはどのくらい時間がかかりますか。</span><span class="sxs-lookup"><span data-stu-id="fab3a-147">How long does it take to deploy my production environment?</span></span>

<span data-ttu-id="fab3a-148">Microsoft FastTrack チームによる Go-live アセスメントが完了し、生産要求が送信された後、48 時間内で実稼働環境の配置を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fab3a-148">After the Go-live assessment with the Microsoft FastTrack team is completed and the production request is submitted, deployment of the production environment should be completed within 48 hours.</span></span>

## <a name="what-level-of-access-do-i-have-in-my-finance-and-operations-production-environment-can-i-sign-in-to-the-vm"></a><span data-ttu-id="fab3a-149">自分の Finance and Operations 実稼動環境でどのレベルのアクセスが可能ですか ?</span><span class="sxs-lookup"><span data-stu-id="fab3a-149">What level of access do I have in my Finance and Operations production environment?</span></span> <span data-ttu-id="fab3a-150">VM にログインできますか。</span><span class="sxs-lookup"><span data-stu-id="fab3a-150">Can I sign in to the VM?</span></span>

<span data-ttu-id="fab3a-151">一連番号</span><span class="sxs-lookup"><span data-stu-id="fab3a-151">No.</span></span> <span data-ttu-id="fab3a-152">実稼働環境へのアクセスは制限されます。</span><span class="sxs-lookup"><span data-stu-id="fab3a-152">Access to the production environment is limited.</span></span> <span data-ttu-id="fab3a-153">仮想マシン (VM) または Microsoft インターネット インフォメーション サービス (IIS) にアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="fab3a-153">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="fab3a-154">また、Microsoft SQL Server Management Studio 経由でデータベースにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="fab3a-154">You also can't access the database through Microsoft SQL Server Management Studio.</span></span>

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="fab3a-155">どのくらいの頻度で生産データベースがバックアップされますか。</span><span class="sxs-lookup"><span data-stu-id="fab3a-155">How often is my production database backed up?</span></span>

<span data-ttu-id="fab3a-156">データベースは自動バックアップによって保護されています。</span><span class="sxs-lookup"><span data-stu-id="fab3a-156">Databases are protected by automatic backups.</span></span> <span data-ttu-id="fab3a-157">完全なデータベース バックアップは毎週行われ、差異のデータベース バックアップは毎時間行われ、およびトランザクション ログのバックアップは 5 分ごとに行われます。</span><span class="sxs-lookup"><span data-stu-id="fab3a-157">Full database backups are done weekly, differential database backups are done hourly, and transaction log backups are done every five minutes.</span></span> <span data-ttu-id="fab3a-158">自動バックアップは 35 日間保持されます。</span><span class="sxs-lookup"><span data-stu-id="fab3a-158">Automatic backups are retained for 35 days.</span></span>

<span data-ttu-id="fab3a-159">詳細については、[自動 SQL データベースのバックアップについて](/azure/sql-database/sql-database-automated-backups) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fab3a-159">For more information, see [Learn about automatic SQL Database backups](/azure/sql-database/sql-database-automated-backups).</span></span>

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="fab3a-160">生産データベースのバックアップのコピーを要求できますか。</span><span class="sxs-lookup"><span data-stu-id="fab3a-160">Can I request a copy of the backup of my production database?</span></span>

<span data-ttu-id="fab3a-161">一連番号</span><span class="sxs-lookup"><span data-stu-id="fab3a-161">No.</span></span> <span data-ttu-id="fab3a-162">ただし、データベースの更新サービス要求を送信し、レベル 2 およびそれ以上の大きいサンドボックス環境に運用データベースをコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="fab3a-162">However, you can submit a database refresh service request to copy your production database to your Tier 2 and higher sandbox environment.</span></span> <span data-ttu-id="fab3a-163">コピー要求が完了した後、サンドボックス環境をバックアップすることができます。</span><span class="sxs-lookup"><span data-stu-id="fab3a-163">After the copy request is completed, you can back up your sandbox environment.</span></span>

## <a name="my-golden-configuration-database-is-in-a-tier-1-sandbox-environment-how-can-i-copy-and-restore-it-to-my-production-environment"></a><span data-ttu-id="fab3a-164">高品質の構成データベースは、第 1 層サンドボックス環境にあります。</span><span class="sxs-lookup"><span data-stu-id="fab3a-164">My golden configuration database is in a Tier 1 sandbox environment.</span></span> <span data-ttu-id="fab3a-165">実稼働環境にどのようにコピーおよび復元しますか。</span><span class="sxs-lookup"><span data-stu-id="fab3a-165">How can I copy and restore it to my production environment?</span></span>

<span data-ttu-id="fab3a-166">第 1 層サンド ボックス環境からコピーして復元するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fab3a-166">To copy and restore from a Tier 1 sandbox environment, follow these steps.</span></span>

1. <span data-ttu-id="fab3a-167">第 1 層サンドボックス環境から第 2 層サンドボックス環境に高品質の構成データベースを移動します。</span><span class="sxs-lookup"><span data-stu-id="fab3a-167">Move your golden configuration database from a Tier 1 sandbox environment to a Tier 2 sandbox environment.</span></span>
2. <span data-ttu-id="fab3a-168">レベル 2 サンドボックス環境から実稼働環境に、高品質の構成をコピーするサービス要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="fab3a-168">Submit a service request to copy your golden configuration from the Tier 2 sandbox environment to the production environment.</span></span>

<span data-ttu-id="fab3a-169">詳細については、[Finance and Operations データベースを SQL Server から Azure SQL データベース運用環境にコピーする](../../dev-itpro/database/copy-database-from-sql-server-to-azure-sql.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fab3a-169">For more information, see [Copy a Finance and Operations database from SQL Server to a production Azure SQL Database environment](../../dev-itpro/database/copy-database-from-sql-server-to-azure-sql.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fab3a-170">高品質の構成がデータ パッケージにある場合、実稼働環境に手動でデータ パッケージをインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fab3a-170">If your golden configuration is in data packages, you must manually import the data packages to the production environment.</span></span>

## <a name="after-go-live-can-i-apply-new-code-changes-to-the-production-environment"></a><span data-ttu-id="fab3a-171">Go-Live の後、実稼働環境に新しいコード変更を適用することはできますか?</span><span class="sxs-lookup"><span data-stu-id="fab3a-171">After go-live, can I apply new code changes to the production environment?</span></span>

<span data-ttu-id="fab3a-172">はい。</span><span class="sxs-lookup"><span data-stu-id="fab3a-172">Yes.</span></span> <span data-ttu-id="fab3a-173">LCS で、配置可能パッケージを実稼働環境に適用するサービス要求を送信することができます。</span><span class="sxs-lookup"><span data-stu-id="fab3a-173">In LCS, you can submit a service request to apply a deployable package to your production environment.</span></span> <span data-ttu-id="fab3a-174">1 つの配置可能パッケージのアプリケーションを実稼動環境に関与させると、5 時間のリード タイムと約 5 時間のダウンタイムになります。</span><span class="sxs-lookup"><span data-stu-id="fab3a-174">Application of one deployable package to a production environment involves a lead time of five hours and downtime of approximately five hours.</span></span>

<span data-ttu-id="fab3a-175">詳細については、[配置可能パッケージの適用](../../dev-itpro/deployment/apply-deployable-package-system.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fab3a-175">For more information, see [Apply deployable package](../../dev-itpro/deployment/apply-deployable-package-system.md).</span></span>

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="fab3a-176">実稼働環境がダウンした場合はどうすればよいでしょうか ?</span><span class="sxs-lookup"><span data-stu-id="fab3a-176">What should I do if my production environment is down?</span></span>

<span data-ttu-id="fab3a-177">稼働停止を報告するには、[[Lifecycle Services によって稼働停止を報告する新しいプロセス](https://blogs.msdn.microsoft.com/lcs/2017/12/18/report-production-outage-through-lcs/)] のブログ記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fab3a-177">To report a production outage, follow the process that is described in the [New process to report a production outage through Lifecycle Services](https://blogs.msdn.microsoft.com/lcs/2017/12/18/report-production-outage-through-lcs/) blog post.</span></span>

---
title: 実装プロジェクト FAQ の Go-live
description: このトピックでは、実装プロジェクトの運用についてよく寄せられる質問を一覧表示します。
author: sshashi7
manager: AnnBe
ms.date: 07/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: sshashi
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 73fa4623eb0b3e31e8cf57518dd38c6faee56c53
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4799046"
---
# <a name="go-live-for-implementation-projects-faq"></a><span data-ttu-id="b7235-103">実装プロジェクト FAQ の Go-live</span><span class="sxs-lookup"><span data-stu-id="b7235-103">Go-live for implementation projects FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7235-104">このトピックでは、実装プロジェクトの運用についてよく寄せられる質問を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b7235-104">This topic lists frequently asked questions about how to go live with an implementation project.</span></span>

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="b7235-105">実稼働環境をいつ構成および要求できますか ?</span><span class="sxs-lookup"><span data-stu-id="b7235-105">When can I configure and request my production environment?</span></span>

<span data-ttu-id="b7235-106">通常、すべてのカスタマイズのコードが完了し、ユーザー受け入れテスト (UAT) が完了し、顧客がソリューションからサインオフし、稼働中にブロッキングの問題がない場合、実稼働環境が展開されます。</span><span class="sxs-lookup"><span data-stu-id="b7235-106">Typically, a production environment is deployed after all customizations are code-complete, user acceptance testing (UAT) is completed, the customer has signed off on the solution, and there are no blocking issues for go-live.</span></span>

<span data-ttu-id="b7235-107">お客様がこの段階にいるとき、Microsoft FastTrack チームはプロジェクトチームと連携して、Go-live 評価/レビューを行ういます。</span><span class="sxs-lookup"><span data-stu-id="b7235-107">When you're at this stage, the Microsoft FastTrack team will work with the project team to do a Go-live assessment/review.</span></span>

## <a name="what-are-the-prerequisites-to-deploy-a-production-environment"></a><span data-ttu-id="b7235-108">実稼働環境を配置するための前提条件</span><span class="sxs-lookup"><span data-stu-id="b7235-108">What are the prerequisites to deploy a production environment?</span></span>

<span data-ttu-id="b7235-109">前提条件の一覧については、 [Go-Live の準備](prepare-go-live.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7235-109">For a list of the prerequisites, see [Prepare for go-live](prepare-go-live.md).</span></span>

## <a name="what-is-a-go-live-assessmentreview-and-why-is-it-required"></a><span data-ttu-id="b7235-110">起動の評価/レビューとは何ですか、またそれがなぜ必要ですか ?</span><span class="sxs-lookup"><span data-stu-id="b7235-110">What is a Go-live assessment/review, and why is it required?</span></span>

<span data-ttu-id="b7235-111">Go-live 評価/レビューは、[Microsoft FastTrack プログラム](../get-started/fasttrack-dynamics-365-overview.md)の一部です。</span><span class="sxs-lookup"><span data-stu-id="b7235-111">The Go-live assessment/review is part of the [Microsoft FastTrack program](../get-started/fasttrack-dynamics-365-overview.md).</span></span> <span data-ttu-id="b7235-112">レビュー中に、ソリューション アーキテクトは、実装プロジェクトが成功した切替および Go-live の準備が整っているかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="b7235-112">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="b7235-113">このレビューは、実稼働環境で準備を開始する前に、すべての実装プロジェクトで必須です。</span><span class="sxs-lookup"><span data-stu-id="b7235-113">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span>

## <a name="i-want-to-request-my-production-environment-who-do-i-contact-for-a-go-live-assessmentreview"></a><span data-ttu-id="b7235-114">実稼働環境を要求します。</span><span class="sxs-lookup"><span data-stu-id="b7235-114">I want to request my production environment.</span></span> <span data-ttu-id="b7235-115">Go-live アセスメント/レビューのために誰に連絡しますか。</span><span class="sxs-lookup"><span data-stu-id="b7235-115">Who do I contact for a Go-live assessment/review?</span></span>
<span data-ttu-id="b7235-116">FastTrack ソリューション アーキテクトがプロジェクトに割り当てられている場合は、担当者に直接問い合わせます。</span><span class="sxs-lookup"><span data-stu-id="b7235-116">If a FastTrack solution architect is assigned to your project, contact him or her directly.</span></span> <span data-ttu-id="b7235-117">それ以外の場合、Microsoft Dynamics Lifecycle Services (LCS) に指定されている運用日付に基づいて、運用前チェックリストに記入し、運用日の数週間前に <d365fogl@microsoft.com> に送信するように指示する電子メールを受信します。</span><span class="sxs-lookup"><span data-stu-id="b7235-117">Otherwise, based on the go-live date that is specified in Microsoft Dynamics Lifecycle Services (LCS), you will receive an email that instructs you to fill out the Pre-go-live checklist and send it to <d365fogl@microsoft.com> a few weeks before the go-live date.</span></span> <span data-ttu-id="b7235-118">電子メールを受信しておらず Go-Live の準備ができている場合は、[Go-live 計画 TechTalk](https://aka.ms/FastTrackPreGoLiveChecklist) ページの **Dynamics 365 コミュニティ** からチェックリストをダウンロードし、記入して d365fogl@microsoft.com に送信できます。</span><span class="sxs-lookup"><span data-stu-id="b7235-118">If you haven't received an email, and you're ready for go-live, you can download the checklist from **Dynamics 365 Community** on the [Go-live Planning TechTalk](https://aka.ms/FastTrackPreGoLiveChecklist) page, complete it, and send it to d365fogl@microsoft.com.</span></span>

## <a name="the-production-button-isnt-available-in-lcs-how-do-i-request-my-production-environment"></a><span data-ttu-id="b7235-119">生産ボタンは、LCS では使用できません。</span><span class="sxs-lookup"><span data-stu-id="b7235-119">The Production button isn't available in LCS.</span></span> <span data-ttu-id="b7235-120">実稼働環境を要求するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="b7235-120">How do I request my production environment?</span></span>

<span data-ttu-id="b7235-121">LCS の **生産** ボタンは、LCS 実装方法の **分析**、**デザイン & 開発**、および **テスト** フェースを完了した後にのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="b7235-121">The **Production** button in LCS is available only after you've completed the **Analysis**, **Design & develop**, and **Test** phases of the LCS implementation methodology.</span></span> <span data-ttu-id="b7235-122">これらのフェーズを完了する方法の詳細については、[Finance and Operations アプリ顧客用の Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs-works-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7235-122">For more information about how to complete these phases, see [Lifecycle Services (LCS) for Finance and Operations apps customers](../../dev-itpro/lifecycle-services/lcs-works-lcs.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b7235-123">実稼働環境は、運用の評価/レビューが完了するまで配置されません。</span><span class="sxs-lookup"><span data-stu-id="b7235-123">Your production environment won't be deployed until the Go-live assessment/review has been completed.</span></span>

## <a name="my-sandbox-environment-is-currently-on-an-update-that-is-set-to-expire-in-two-months-can-i-request-a-production-environment-that-has-the-latest-update"></a><span data-ttu-id="b7235-124">自分のサンドボックス環境は、現在有効期限が 2 か月に設定されている更新プログラムにあります。</span><span class="sxs-lookup"><span data-stu-id="b7235-124">My sandbox environment is currently on an update that is set to expire in two months.</span></span> <span data-ttu-id="b7235-125">最新の更新プログラムを含む実稼動環境を要求できますか。</span><span class="sxs-lookup"><span data-stu-id="b7235-125">Can I request a production environment that has the latest update?</span></span>

<span data-ttu-id="b7235-126">一連番号</span><span class="sxs-lookup"><span data-stu-id="b7235-126">No.</span></span> <span data-ttu-id="b7235-127">サンド ボックス環境と異なるバージョンにある実稼働環境に対する要求をすべて拒否します。</span><span class="sxs-lookup"><span data-stu-id="b7235-127">We will deny any request for a production environment that is on a different version than your sandbox environment.</span></span> <span data-ttu-id="b7235-128">実稼働環境をコンフィギュレーションするときは、選択したバージョンが、ソリューションを承認したサンド ボックス環境のバージョンと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7235-128">When you configure a production environment, the versions that you select must match the versions of the sandbox environment where you signed off on your solution.</span></span> <span data-ttu-id="b7235-129">したがって、まず最新の更新プログラムをサンドボックス環境に適用してテストし、サインオフする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7235-129">Therefore, you must first apply the latest update to your sandbox environment, test it, and sign off.</span></span>

<span data-ttu-id="b7235-130">詳細については、 [ソフトウェアのライフサイクル ポリシーおよびクラウド リリース](../../dev-itpro/migration-upgrade/versions-update-policy.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7235-130">For more information, see [Software lifecycle policy and cloud releases](../../dev-itpro/migration-upgrade/versions-update-policy.md).</span></span>

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-but-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="b7235-131">サンドボックス環境は、米国中部データセンターに配置されますが、生産環境は米国西部データセンターに配置する予定です。</span><span class="sxs-lookup"><span data-stu-id="b7235-131">Our sandbox environments are deployed in the Central US datacenter, but we want our production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="b7235-132">本番構成で、データ センターとして米国西部を選択できますか？</span><span class="sxs-lookup"><span data-stu-id="b7235-132">Can I select West US as the datacenter in my production configuration?</span></span>

<span data-ttu-id="b7235-133">一連番号</span><span class="sxs-lookup"><span data-stu-id="b7235-133">No.</span></span> <span data-ttu-id="b7235-134">サンド ボックス環境と異なるデータ センター内にある実稼働環境に対する要求をすべて拒否します。</span><span class="sxs-lookup"><span data-stu-id="b7235-134">We will deny any request for a production environment that is in a different datacenter than your sandbox environment.</span></span> <span data-ttu-id="b7235-135">すべての環境が同じデータ センターに配置されていることが必要です。</span><span class="sxs-lookup"><span data-stu-id="b7235-135">We require that all your environments reside in the same datacenter.</span></span> <span data-ttu-id="b7235-136">実稼働環境を米国西部データセンターに配置するには、まずサンドボックス環境を米国西部のデータセンターに再展開してテストし、サインオフする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7235-136">If you want your production environment to reside in the West US datacenter, you must first redeploy your sandbox environments to the West US datacenter, test them, and sign off.</span></span>

<span data-ttu-id="b7235-137">正しいデータ センターを選択するのに役立つ情報の詳細については、「システム要件」トピックの [ネットワーク要件](../get-started/system-requirements.md#network-requirements) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7235-137">For information that can help you select the correct datacenter, see the [Network requirements](../get-started/system-requirements.md#network-requirements) section of the "System requirements" topic.</span></span>

## <a name="how-will-my-production-environment-be-sized"></a><span data-ttu-id="b7235-138">実稼働環境はどのくらいの規模になりますか。</span><span class="sxs-lookup"><span data-stu-id="b7235-138">How will my production environment be sized?</span></span>

<span data-ttu-id="b7235-139">実稼働環境のサイズは、現在のユーザー ライセンス数と、実稼働環境を要求するときに有効なサブスクリプションの推定の情報に基づいて決まります。</span><span class="sxs-lookup"><span data-stu-id="b7235-139">Your production environment will be sized based on the current user license count and the information in the subscription estimate that is active when you request the production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="b7235-140">追加のユーザーを後で追加する場合は、新しいサブスクリプション推定をアクティブ化するためのサポート チケットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7235-140">If you add additional users later, you must create a support ticket to activate a new subscription estimate.</span></span> <span data-ttu-id="b7235-141">実稼働環境のサイズは、ユーザー数、ユーザーのライセンスの種類、および予想されるピーク時のトランザクション量に応じて変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7235-141">Your production environment might have to be resized, depending on the number of users, the type of user licenses, and the expected peak transaction volume.</span></span> <span data-ttu-id="b7235-142">ダウンタイムは、実稼働環境のサイズを変更するために必要です。</span><span class="sxs-lookup"><span data-stu-id="b7235-142">Downtime is required in order to resize a production environment.</span></span>

## <a name="i-submitted-the-request-for-a-production-environment-but-i-made-a-mistake-can-i-still-change-it"></a><span data-ttu-id="b7235-143">実稼働環境の要求を送信しましたが、間違いが発生しました。</span><span class="sxs-lookup"><span data-stu-id="b7235-143">I submitted the request for a production environment, but I made a mistake.</span></span> <span data-ttu-id="b7235-144">いまでも変更できますか。</span><span class="sxs-lookup"><span data-stu-id="b7235-144">Can I still change it?</span></span>

<span data-ttu-id="b7235-145">はい。</span><span class="sxs-lookup"><span data-stu-id="b7235-145">Yes.</span></span> <span data-ttu-id="b7235-146">実稼働環境のステータスが **キュー** に設定されている限り、サインオフ フラグをクリアし、変更、および再度サイン オフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b7235-146">As long as the status of the production environment is **Queued**, you can clear the sign-off flag, make changes, and then sign off again.</span></span>

## <a name="how-long-does-it-take-to-deploy-my-production-environment"></a><span data-ttu-id="b7235-147">実稼働環境を配置するにはどのくらい時間がかかりますか。</span><span class="sxs-lookup"><span data-stu-id="b7235-147">How long does it take to deploy my production environment?</span></span>

<span data-ttu-id="b7235-148">Microsoft FastTrack チームによる Go-live アセスメントが完了し、生産要求が送信された後、48 時間内で実稼働環境の配置を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7235-148">After the Go-live assessment with the Microsoft FastTrack team is completed and the production request is submitted, deployment of the production environment should be completed within 48 hours.</span></span>

## <a name="what-level-of-access-do-i-have-in-my-production-environment-can-i-sign-in-to-the-vm"></a><span data-ttu-id="b7235-149">自分の実稼動環境にて、どのレベルのアクセスが可能ですか。</span><span class="sxs-lookup"><span data-stu-id="b7235-149">What level of access do I have in my production environment?</span></span> <span data-ttu-id="b7235-150">VM にログインできますか。</span><span class="sxs-lookup"><span data-stu-id="b7235-150">Can I sign in to the VM?</span></span>

<span data-ttu-id="b7235-151">一連番号</span><span class="sxs-lookup"><span data-stu-id="b7235-151">No.</span></span> <span data-ttu-id="b7235-152">実稼働環境へのアクセスは制限されます。</span><span class="sxs-lookup"><span data-stu-id="b7235-152">Access to the production environment is limited.</span></span> <span data-ttu-id="b7235-153">仮想マシン (VM) または Microsoft インターネット インフォメーション サービス (IIS) にアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b7235-153">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="b7235-154">また、Microsoft SQL Server Management Studio 経由でデータベースにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b7235-154">You also can't access the database through Microsoft SQL Server Management Studio.</span></span>

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="b7235-155">どのくらいの頻度で生産データベースがバックアップされますか。</span><span class="sxs-lookup"><span data-stu-id="b7235-155">How often is my production database backed up?</span></span>

<span data-ttu-id="b7235-156">データベースは自動バックアップによって保護されています。</span><span class="sxs-lookup"><span data-stu-id="b7235-156">Databases are protected by automatic backups.</span></span> <span data-ttu-id="b7235-157">完全なデータベース バックアップは毎週行われ、差異のデータベース バックアップは毎時間行われ、およびトランザクション ログのバックアップは 5 分ごとに行われます。</span><span class="sxs-lookup"><span data-stu-id="b7235-157">Full database backups are done weekly, differential database backups are done hourly, and transaction log backups are done every five minutes.</span></span> <span data-ttu-id="b7235-158">自動バックアップは 35 日間保持されます。</span><span class="sxs-lookup"><span data-stu-id="b7235-158">Automatic backups are retained for 35 days.</span></span>

<span data-ttu-id="b7235-159">詳細については、[自動 SQL データベースのバックアップについて](/azure/sql-database/sql-database-automated-backups) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7235-159">For more information, see [Learn about automatic SQL Database backups](/azure/sql-database/sql-database-automated-backups).</span></span>

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="b7235-160">生産データベースのバックアップのコピーを要求できますか。</span><span class="sxs-lookup"><span data-stu-id="b7235-160">Can I request a copy of the backup of my production database?</span></span>

<span data-ttu-id="b7235-161">一連番号</span><span class="sxs-lookup"><span data-stu-id="b7235-161">No.</span></span> <span data-ttu-id="b7235-162">ただし、データベースの更新サービス要求を送信し、レベル 2 およびそれ以上の大きいサンドボックス環境に運用データベースをコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="b7235-162">However, you can submit a database refresh service request to copy your production database to your Tier 2 and higher sandbox environment.</span></span> <span data-ttu-id="b7235-163">コピー要求が完了した後、サンドボックス環境をバックアップすることができます。</span><span class="sxs-lookup"><span data-stu-id="b7235-163">After the copy request is completed, you can back up your sandbox environment.</span></span>

## <a name="my-golden-configuration-database-is-in-a-tier-1-sandbox-environment-how-can-i-copy-and-restore-it-to-my-production-environment"></a><span data-ttu-id="b7235-164">高品質の構成データベースは、第 1 層サンドボックス環境にあります。</span><span class="sxs-lookup"><span data-stu-id="b7235-164">My golden configuration database is in a Tier 1 sandbox environment.</span></span> <span data-ttu-id="b7235-165">実稼働環境にどのようにコピーおよび復元しますか。</span><span class="sxs-lookup"><span data-stu-id="b7235-165">How can I copy and restore it to my production environment?</span></span>
<span data-ttu-id="b7235-166">データベースをコピーして復元するには、トピック [ゴールデンコンフィギュレーションプロモーション](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md) の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="b7235-166">To copy and restore your database, follow the instructions in the topic, [Golden configuration promotion](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md).</span></span> 

> [!NOTE]
> <span data-ttu-id="b7235-167">高品質の構成がデータ パッケージにある場合、実稼働環境に手動でデータ パッケージをインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7235-167">If your golden configuration is in data packages, you must manually import the data packages to the production environment.</span></span>

## <a name="after-go-live-can-i-apply-new-code-changes-to-the-production-environment"></a><span data-ttu-id="b7235-168">Go-Live の後、実稼働環境に新しいコード変更を適用することはできますか?</span><span class="sxs-lookup"><span data-stu-id="b7235-168">After go-live, can I apply new code changes to the production environment?</span></span>

<span data-ttu-id="b7235-169">はい。</span><span class="sxs-lookup"><span data-stu-id="b7235-169">Yes.</span></span> <span data-ttu-id="b7235-170">LCS で、配置可能パッケージを実稼働環境に適用するサービス要求を送信することができます。</span><span class="sxs-lookup"><span data-stu-id="b7235-170">In LCS, you can submit a service request to apply a deployable package to your production environment.</span></span> <span data-ttu-id="b7235-171">1 つの配置可能パッケージのアプリケーションを実稼動環境に関与させると、5 時間のリード タイムと約 5 時間のダウンタイムになります。</span><span class="sxs-lookup"><span data-stu-id="b7235-171">Application of one deployable package to a production environment involves a lead time of five hours and downtime of approximately five hours.</span></span>

<span data-ttu-id="b7235-172">詳細については、[クラウド環境への更新プログラムの適用](../../dev-itpro/deployment/apply-deployable-package-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7235-172">For more information, see [Apply updates to cloud environments](../../dev-itpro/deployment/apply-deployable-package-system.md).</span></span>

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="b7235-173">実稼働環境がダウンした場合はどうすればよいでしょうか ?</span><span class="sxs-lookup"><span data-stu-id="b7235-173">What should I do if my production environment is down?</span></span>

<span data-ttu-id="b7235-174">稼働停止をレポートするには、トピック [稼働停止のレポート](../../dev-itpro/lifecycle-services/report-production-outage.md) で説明されているプロセスに従います。</span><span class="sxs-lookup"><span data-stu-id="b7235-174">To report a production outage, follow the process described in the topic, [Report a production outage](../../dev-itpro/lifecycle-services/report-production-outage.md).</span></span>

---
title: マスター プランの計画最適化への移行
description: このトピックでは、新しいマスター プラン エンジン、最適化の計画、および既存のエンジンからの移行に関する情報を提供します。
author: ChristianRytt
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: e227cabdd205b7a0c1fe784fc719b538e6ea4443
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907694"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a><span data-ttu-id="d03aa-103">マスター プランの計画最適化への移行</span><span class="sxs-lookup"><span data-stu-id="d03aa-103">Migration to Planning Optimization for master planning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d03aa-104">組み込みのマスター プラン エンジンが古いバージョンになるようにスケジュールされています (非推奨)。</span><span class="sxs-lookup"><span data-stu-id="d03aa-104">The built-in master planning engine is scheduled to be made obsolete (deprecated).</span></span> <span data-ttu-id="d03aa-105">このファイルは、Microsoft Dynamics 365 Supply Chain Management の計画最適化アドインによって置き換えられています。</span><span class="sxs-lookup"><span data-stu-id="d03aa-105">It's being replaced by the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d03aa-106">このトピックでは、新規または既存の配置への影響について説明します。</span><span class="sxs-lookup"><span data-stu-id="d03aa-106">This topic provides information about the impact on new and existing deployments.</span></span> <span data-ttu-id="d03aa-107">必要なアクションに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d03aa-107">It includes information about required actions.</span></span>

<span data-ttu-id="d03aa-108">計画の最適化により、マスター プランの計算を Supply Chain Management とその Azure SQL データベースの外部で実行できます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-108">Planning Optimization enables master planning calculations to occur outside Supply Chain Management and its Azure SQL database.</span></span> <span data-ttu-id="d03aa-109">計画の最適化に関連する利点として、マスター プランの実行時にパフォーマンスが向上し、SQL データベースへの影響が最小限に抑えられます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-109">The benefits that are associated with Planning Optimization include improved performance and minimized impact on the SQL database during master planning runs.</span></span> <span data-ttu-id="d03aa-110">迅速なプランニングを営業時間中に実行できるため、プランナーは要求またはパラメータの変更にすぐに対応できます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-110">Because quick planning runs can be done even during office hours, planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="d03aa-111">計画の最適化に関する詳細については、[計画最適化の概要](planning-optimization/planning-optimization-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d03aa-111">For more information about Planning Optimization, see [Planning Optimization overview](planning-optimization/planning-optimization-overview.md).</span></span>

## <a name="obsolescence-of-the-existing-master-planning-engine"></a><span data-ttu-id="d03aa-112">既存のマスター プラン エンジンの陳腐化</span><span class="sxs-lookup"><span data-stu-id="d03aa-112">Obsolescence of the existing master planning engine</span></span>

<span data-ttu-id="d03aa-113">Microsoft は、現在組み込みの計画エンジンを計画の最適化に対して無効にしています。</span><span class="sxs-lookup"><span data-stu-id="d03aa-113">Microsoft is in the process of making the built-in planning engine obsolete in favor of Planning Optimization.</span></span> <span data-ttu-id="d03aa-114">この変更は、すべてのクラウド環境に影響します。</span><span class="sxs-lookup"><span data-stu-id="d03aa-114">This change affects all cloud environments.</span></span> <span data-ttu-id="d03aa-115">オンプレミスのインストールは影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="d03aa-115">On-premises installations aren't affected.</span></span> <span data-ttu-id="d03aa-116">バージョン 10.0.16 では、計画製造オーダーを生成せずに組み込みのマスター プランを実行すると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-116">In version 10.0.16 and later, you will receive an error message if you run the built-in master planning without generating planned production orders.</span></span> <span data-ttu-id="d03aa-117">ただし、マスター プランの実行は、エラー メッセージにかかわらず正常に完了します。</span><span class="sxs-lookup"><span data-stu-id="d03aa-117">However, the master planning run will be successfully completed despite the error message.</span></span>

<span data-ttu-id="d03aa-118">組み込みの計画エンジンの陳腐化に関する詳細については、[Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](../get-started/removed-deprecated-features-scm-updates.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d03aa-118">For more information about the obsolescence of the built-in planning engine, see the announcements in [Removed or deprecated features in Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).</span></span>

## <a name="migration-messages-and-exceptions"></a><span data-ttu-id="d03aa-119">移行、メッセージ、および例外</span><span class="sxs-lookup"><span data-stu-id="d03aa-119">Migration, messages, and exceptions</span></span>

<span data-ttu-id="d03aa-120">計画された製造オーダーを生成せずに組み込みのマスター プラン エンジンを実行する既存の環境の所有者は、例外プロセスの詳細を提供するメールを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="d03aa-120">Owners of existing environments who run the built-in master planning engine without generating planned production orders will receive an email that provides details about the exception process.</span></span> <span data-ttu-id="d03aa-121">パートナーと協力して、計画の最適化への移行を評価および計画することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d03aa-121">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="d03aa-122">前述の通り、バージョン 10.0.16 以降では、計画製造オーダーを生成せずに組み込みのマスター プランを実行すると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-122">As has been mentioned, you will receive an error message in version 10.0.16 and later if you run the built-in master planning without generating planned production orders.</span></span> <span data-ttu-id="d03aa-123">このエラー メッセージには、移行に関するガイダンスおよび例外の要求に関する指示が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-123">This error message includes guidance about migration and instructions for requesting an exception.</span></span>

### <a name="new-deployments"></a><span data-ttu-id="d03aa-124">新しい配置</span><span class="sxs-lookup"><span data-stu-id="d03aa-124">New deployments</span></span>

<span data-ttu-id="d03aa-125">計画の最適化は、クラウド内のすべての新しい配置に対する既定のマスター プラン エンジンとして考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03aa-125">Planning Optimization should be considered the default master planning engine for all new deployments in the cloud.</span></span> <span data-ttu-id="d03aa-126">一般に、計画最適化は、マスター プラン中に計画製造オーダーを生成しないすべての新規デプロイに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03aa-126">In general, Planning Optimization should be used for all new deployments that don't generate planned production orders during master planning.</span></span> <span data-ttu-id="d03aa-127">最適化計画が現時点でサポートされていない機能に基づいて新しいデプロイを行う場合は、組み込みのマスター プラン エンジンを引き続き使用できるように、例外を要求することができます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-127">If a new deployment depends on functionality that Planning Optimization doesn't currently support, you can request an exception so that you can continue to use the built-in master planning engine.</span></span>

### <a name="existing-deployments"></a><span data-ttu-id="d03aa-128">既存の配置</span><span class="sxs-lookup"><span data-stu-id="d03aa-128">Existing deployments</span></span>

<span data-ttu-id="d03aa-129">マスター プランに依存する既存のクラウドベースのデプロイの所有者は、計画の最適化への移行を計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03aa-129">Owners of existing cloud-based deployments that depend on master planning should plan to migrate to Planning Optimization.</span></span> <span data-ttu-id="d03aa-130">最適化計画が現時点でサポートされていない機能に基づいてデプロイを行う場合は、組み込みのマスター プラン エンジンを引き続き使用できるように、例外を要求することができます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-130">If your implementation depends on functionality that Planning Optimization doesn't currently support, you can request an exception so that you can continue to use the built-in master planning engine.</span></span>

<span data-ttu-id="d03aa-131">現在陳腐化しているマスター プラン プロセスを使用している環境では、Microsoft は環境管理者にメールを送信します。このメールでは、例外を移行または要求するために必要なアクションに関する情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-131">For environments that currently use master planning processes that are being made obsolete, Microsoft will send an email to the environment admin. This email will provide information about the actions that are required to migrate or to request an exception.</span></span>

## <a name="the-exception-process"></a><span data-ttu-id="d03aa-132">例外処理</span><span class="sxs-lookup"><span data-stu-id="d03aa-132">The exception process</span></span>

<span data-ttu-id="d03aa-133">ビジネス プロセスが、現在計画中に実装されていない機能に大きく依存しているため、組み込みのマスター プラン エンジンの使用を継続する必要がある場合は、例外を要求できます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-133">You can request an exception if you must continue to use the built-in master planning engine because your business processes depends heavily on at least one feature that isn't currently implemented in Planning Optimization.</span></span> <span data-ttu-id="d03aa-134">使用可能な機能の一覧については、[計画最適化適合分析](planning-optimization/planning-optimization-fit-analysis.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d03aa-134">For a list of available features, see [Planning Optimization fit analysis](planning-optimization/planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="d03aa-135">現在、計画最適化移行の例外は、マスター プラン プロセスに生産 (つまり、マスター プランによって生成される計画製造オーダー) が含まれておらず、バージョン 10.0.15 以降の組み込みマスター プラン エンジンが必要な場合にのみ関係します。</span><span class="sxs-lookup"><span data-stu-id="d03aa-135">Currently, exceptions for Planning Optimization migration are only relevant if your master planning process doesn't include production (that is, planned production orders that are generated by master planning), and you require the built-in master planning engine beyond version 10.0.15.</span></span>

<span data-ttu-id="d03aa-136">必要な機能が使用可能になった後、例外の期限が切れるまで猶予期間が提供されます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-136">After the required features become available, Microsoft will provide a grace period until the exception expires.</span></span> <span data-ttu-id="d03aa-137">必要な機能が使用可能になり、猶予期間が開始されると、環境管理者に通知されます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-137">The environment admin will be informed when the required features have become available and the grace period has started.</span></span>

<span data-ttu-id="d03aa-138">次のフローチャートは、このトピックで提供される情報を要約しているため、例外を要求する必要があるかどうかをすばやく判断できます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-138">The following flowchart summarizes the information provided in this topic so you can quickly find out whether you should request an exception.</span></span> <span data-ttu-id="d03aa-139">例外を要求する必要がある場合は、[計画の最適化の移行と例外に関するアンケート](https://go.microsoft.com/fwlink/?linkid=2144962) に記入して送信してください。</span><span class="sxs-lookup"><span data-stu-id="d03aa-139">If you do need to request an exception, please fill out and submit the [Planning Optimization migration and exception questionnaire](https://go.microsoft.com/fwlink/?linkid=2144962).</span></span>

<span data-ttu-id="d03aa-140">![例外フローチャート](media/exception-diagram.png "例外フローチャート")</span><span class="sxs-lookup"><span data-stu-id="d03aa-140">![Exception flowchart](media/exception-diagram.png "Exception flowchart")</span></span>

> [!NOTE]
> <span data-ttu-id="d03aa-141">例外を要求できるのは、サンドボックス環境のみのテナントではなく、現在実稼動環境が含まれている、または含まれる予定のテナントのみです。</span><span class="sxs-lookup"><span data-stu-id="d03aa-141">You can only request an exception for tenants that currently include, or will include, a production environment, not for tenants with sandbox environments only.</span></span> <span data-ttu-id="d03aa-142">サービス (IaaS) サンドボックス環境としてのインフラストラクチャにおける計画の最適化例外エラーを無効にする必要がある場合は、[サンドボックス環境](#faq-sandbox)で提供されている SQL クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="d03aa-142">If you need to disable the Planning Optimization exception error on an infrastructure as a service (IaaS) sandbox environment, run the SQL query provided in [Sandbox environments](#faq-sandbox).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="d03aa-143">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="d03aa-143">Frequently asked questions</span></span>

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a><span data-ttu-id="d03aa-144">サンドボックス環境</span><span class="sxs-lookup"><span data-stu-id="d03aa-144">Sandbox environments</span></span>

<span data-ttu-id="d03aa-145">サンドボックス環境で組み込みマスター プランを使用することはできますか?</span><span class="sxs-lookup"><span data-stu-id="d03aa-145">Can I use built-in master planning on my sandbox environment?</span></span> <span data-ttu-id="d03aa-146">例外が必要ですか?</span><span class="sxs-lookup"><span data-stu-id="d03aa-146">Do I need an exception?</span></span>

<span data-ttu-id="d03aa-147">**回答:** 計画最適化例外エラーは組み込みのマスター プラン エンジンの正常な実行を妨げないため、例外は通常サンドボックス環境には関係ありません。</span><span class="sxs-lookup"><span data-stu-id="d03aa-147">**Answer:** Exceptions aren't normally relevant for sandbox environments because the Planning Optimization exception error doesn't prevent the built-in master planning engine from running successfully.</span></span> <span data-ttu-id="d03aa-148">ただし、エラー メッセージが邪魔になる場合は、データベースで次のクエリを実行することにより、IaaS (Service Fabric ではない) サンドボックス環境でエラー メッセージを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-148">However, if the error message disturbs you, you can disable it on an IaaS (not Service Fabric) sandbox environment by running the following query on your database:</span></span>

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a><span data-ttu-id="d03aa-149">オンプレミス環境</span><span class="sxs-lookup"><span data-stu-id="d03aa-149">On-premises environments</span></span>

<span data-ttu-id="d03aa-150">私の環境はオンプレミスです。</span><span class="sxs-lookup"><span data-stu-id="d03aa-150">My environment is on-premises.</span></span> <span data-ttu-id="d03aa-151">例外が必要ですか?</span><span class="sxs-lookup"><span data-stu-id="d03aa-151">Do I need an exception?</span></span>

<span data-ttu-id="d03aa-152">**回答:** いいえ。</span><span class="sxs-lookup"><span data-stu-id="d03aa-152">**Answer:** No.</span></span> <span data-ttu-id="d03aa-153">オンプレミス環境には例外は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="d03aa-153">An exception isn't required for on-premises environments.</span></span> <span data-ttu-id="d03aa-154">引き続き、組み込みマスター プランを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-154">You can continue to use the built-in master planning.</span></span> <span data-ttu-id="d03aa-155">必要なアクションがある場合は、環境管理者に通知されます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-155">Your environment admin will be informed if any action is required.</span></span>

### <a name="production-scenarios"></a><span data-ttu-id="d03aa-156">生産シナリオ</span><span class="sxs-lookup"><span data-stu-id="d03aa-156">Production scenarios</span></span>

<span data-ttu-id="d03aa-157">計画製造オーダーを使用しますが、バージョン 10.0.16 にアップグレードした場合に何が起こるか不安を感じています。</span><span class="sxs-lookup"><span data-stu-id="d03aa-157">We use planned production orders, but I'm concerned about what will happen when we upgrade to version 10.0.16.</span></span> <span data-ttu-id="d03aa-158">何らかのアクションを実行する必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="d03aa-158">Should I take any action?</span></span>

<span data-ttu-id="d03aa-159">**回答:** 心配する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d03aa-159">**Answer:** You should not be concerned.</span></span> <span data-ttu-id="d03aa-160">バージョン 10.0.16 では、引き続き組み込みマスター プランを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-160">You can continue to use the built-in master planning in version 10.0.16.</span></span> <span data-ttu-id="d03aa-161">ただし、計画の最適化への移行を現在の機能で開始できるかどうかを評価することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d03aa-161">However, we recommend that you evaluate whether migration to Planning Optimization can start with the current functionality.</span></span> <span data-ttu-id="d03aa-162">また、新しい機能について常に情報を入手することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d03aa-162">We also recommend that you remain informed about new functionality.</span></span>

### <a name="email-from-microsoft"></a><span data-ttu-id="d03aa-163">Microsoft からのメール</span><span class="sxs-lookup"><span data-stu-id="d03aa-163">Email from Microsoft</span></span>

<span data-ttu-id="d03aa-164">この環境の管理者は、Microsoft からメールを受け取っています。</span><span class="sxs-lookup"><span data-stu-id="d03aa-164">Our environment admin received an email from Microsoft.</span></span> <span data-ttu-id="d03aa-165">このメールでは、最適化の計画に移行するか、例外を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03aa-165">This email states that we should migrate to Planning Optimization or request an exception.</span></span> <span data-ttu-id="d03aa-166">何らかのアクションを実行する必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="d03aa-166">Do I need to take any action?</span></span>

<span data-ttu-id="d03aa-167">**回答:** はい。</span><span class="sxs-lookup"><span data-stu-id="d03aa-167">**Answer:** Yes.</span></span> <span data-ttu-id="d03aa-168">メールの指示に従っていない限り、環境は影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-168">Your environment will be affected unless you follow the instructions in the email.</span></span> <span data-ttu-id="d03aa-169">指定した日付まで計画の最適化に移行するか、メールのリンクを使用して例外を要求することができます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-169">You can either migrate to Planning Optimization by the date specified or request an exception by using the link in the email.</span></span> <span data-ttu-id="d03aa-170">このリンクでは、アンケートを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-170">This link opens a questionnaire.</span></span> <span data-ttu-id="d03aa-171">このアンケートを完了して提出した後に、メールで返信を受信します。</span><span class="sxs-lookup"><span data-stu-id="d03aa-171">After you've completed and submitted this questionnaire, you will receive a reply via email.</span></span> <span data-ttu-id="d03aa-172">このプロセスは手動で行われますが、Microsoft は、アンケートの送信後 1 週間以内に返信します。</span><span class="sxs-lookup"><span data-stu-id="d03aa-172">Although this process is manual, Microsoft tries to reply within a week after the questionnaire is submitted.</span></span>

### <a name="error-messages"></a><span data-ttu-id="d03aa-173">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="d03aa-173">Error messages</span></span>

<span data-ttu-id="d03aa-174">バージョン 10.0.16 以降を使用していますが、マスター プランの実行時に次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d03aa-174">I'm using version 10.0.16 or later, and I receive the following error message when I run master planning.</span></span> <span data-ttu-id="d03aa-175">マスター プランがブロックされていますか?</span><span class="sxs-lookup"><span data-stu-id="d03aa-175">Is master planning blocked?</span></span>

> <span data-ttu-id="d03aa-176">このエラー メッセージが表示されるのは、組み込みマスター プラン エンジンが、計画の最適化によってサポートされているシナリオに使用されたためです。</span><span class="sxs-lookup"><span data-stu-id="d03aa-176">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="d03aa-177">現在の組み込みのマスター プランは非推奨であるため、今すぐ計画の最適化に移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03aa-177">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="d03aa-178">このマスター プランの実行が正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d03aa-178">Note that this master planning run did complete successfully.</span></span>
>
> <span data-ttu-id="d03aa-179">移行が保留中の機能に強い依存関係がある場合は、組み込みのマスター プラン エンジンの使用を継続することはできません。</span><span class="sxs-lookup"><span data-stu-id="d03aa-179">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span>
>
> <span data-ttu-id="d03aa-180">次のアンケートに記入して、移行に関連する要求の例外を計画の最適化に適用してください。</span><span class="sxs-lookup"><span data-stu-id="d03aa-180">Please complete the following questionnaire to get started and if relevant request exception from migration to Planning Optimization.</span></span>

<span data-ttu-id="d03aa-181">**回答:** いいえ、マスター プランはブロックされていません。</span><span class="sxs-lookup"><span data-stu-id="d03aa-181">**Answer:** No, master planning isn't blocked.</span></span> <span data-ttu-id="d03aa-182">マスター プランの実行が正常に完了し、その結果を通常の方法で使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d03aa-182">Your master planning run was successfully completed, and you can use the result in the usual way.</span></span> <span data-ttu-id="d03aa-183">ただし、今後のマスター プランの実行時にこのエラー メッセージが表示されないようにするには、計画の最適化に直ちに移行するか、エラー メッセージのリンクを使用して例外を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03aa-183">However, to avoid receiving this error message during future master planning runs, you must either migrate to Planning Optimization immediately or request an exception by using the link in the error message.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

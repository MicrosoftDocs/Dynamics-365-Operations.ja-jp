---
title: AX 2012 からのアップグレード - 切替テスト (切替モック)
description: このトピックでは、Microsoft Dynamics AX 2012 環境をオフにしてから Finance and Operations をオンにするまでの切替えプロセスをテストする方法について説明します。
author: jorisdg
manager: AnnBe
ms.date: 06/06/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 2d7a53ce1304cd217d7751f855a0802965cca929
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983644"
---
# <a name="upgrade-from-ax-2012---cutover-testing-mock-cutover"></a><span data-ttu-id="92fab-103">AX 2012 からのアップグレード - 切替テスト (切替モック)</span><span class="sxs-lookup"><span data-stu-id="92fab-103">Upgrade from AX 2012 - Cutover testing (Mock cutover)</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="92fab-104">*切替*という用語は、新しいシステムを稼働させる最後のプロセスに使用します。</span><span class="sxs-lookup"><span data-stu-id="92fab-104">*Cutover* is the term that we use for the final process of getting a new system live.</span></span> <span data-ttu-id="92fab-105">切替プロセスは、Microsoft Dynamics AX 2012 をオフにした後、かつ Finance and Operations をオンにする前に発生するタスクで構成されます。</span><span class="sxs-lookup"><span data-stu-id="92fab-105">The cutover process consists of the tasks that occur after Microsoft Dynamics AX 2012 is turned off, but before Finance and Operations is turned on.</span></span> <span data-ttu-id="92fab-106">アップグレード切替テスト (切替モック) の目的は、切替プロセスを練習することで、実際の切替中に関係するすべての人がスムーズに作業できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="92fab-106">The purpose of upgrade cutover testing (mock cutover) is to practice the cutover process, to help guarantee a smooth experience for everyone who is involved during the actual cutover to go-live.</span></span>

<span data-ttu-id="92fab-107">切替中には、3 つの主要なワーク ストリームがあります。</span><span class="sxs-lookup"><span data-stu-id="92fab-107">There are three main workstreams during a cutover:</span></span>

- <span data-ttu-id="92fab-108">**技術的なワーク ストリーム** – このワーク ストリームには、データ アップグレードの実行プロセスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="92fab-108">**Technical workstream** – This workstream includes the data upgrade execution process.</span></span> <span data-ttu-id="92fab-109">業務では、許可されているダウンタイムの金額に制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="92fab-109">Your business will enforce a limit on the amount of downtime that is allowed.</span></span> <span data-ttu-id="92fab-110">このダウンタイム中には、AX 2012 および Finance and Operations のどちらの製品データベースも使用できません。</span><span class="sxs-lookup"><span data-stu-id="92fab-110">During this downtime, neither AX 2012 nor Finance and Operations will be available.</span></span> <span data-ttu-id="92fab-111">このワーク ストリームでは、業務でのダウンタイム制限を満たすために、データ アップグレード手順をチューニングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-111">This workstream might have to tune the data upgrade procedure to meet the business's downtime limit.</span></span>
- <span data-ttu-id="92fab-112">**機能的なワーク ストリーム** – このワーク ストリームには、データのアップグレードが完了した後に実行されるコンフィギュレーション タスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="92fab-112">**Functional workstream** – This workstream includes the configuration tasks that are performed after the data upgrade is completed.</span></span> <span data-ttu-id="92fab-113">機能的なワークストリームと技術的なワークストリームの両方が業務のダウンタイム制限内に収まる必要があるため、これらのタスクをすべて文書化および定量化し、リソースを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-113">All these tasks must be documented and quantified, and a resource must be assigned, because both the functional workstream and the technical workstream must fit within the business's downtime limit.</span></span>
- <span data-ttu-id="92fab-114">**AX 2012 ロールバック** - このワークストリームには AX 2012 環境へのロールバックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="92fab-114">**AX 2012 rollback** - This workstream includes rolling back to an AX 2012 environment.</span></span> <span data-ttu-id="92fab-115">ロールバックする必要はありませんが、必要な場合に備えてテスト済みのプロセスがあることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="92fab-115">Although it's unlikely that you will have to roll back, it's very important that you have a tested process in case you require it.</span></span>

<span data-ttu-id="92fab-116">次の図は、実稼動環境で発生するような、切替中の全体的なプロセスを示しています。</span><span class="sxs-lookup"><span data-stu-id="92fab-116">The following illustration shows the overall process for cutover to go-live as it will occur in the production environment.</span></span>

![切替プロセス](./media/cutover_1.png)

<span data-ttu-id="92fab-118">モック カットオーバー プロセスは、サンドボックス環境での基本的なデータ アップグレードの検証と非常によく似ています。</span><span class="sxs-lookup"><span data-stu-id="92fab-118">The mock cutover process is very similar to a basic data upgrade validation in a sandbox environment.</span></span> <span data-ttu-id="92fab-119">そのプロセスを熟知していて、そのプロセスを既に実行済みであると仮定します。</span><span class="sxs-lookup"><span data-stu-id="92fab-119">We assume that you are familiar with that process, and have already performed it.</span></span> <span data-ttu-id="92fab-120">切替モックは、次の点で異なります。</span><span class="sxs-lookup"><span data-stu-id="92fab-120">Mock cutover differs in the following ways:</span></span>

- <span data-ttu-id="92fab-121">サンドボックス環境でデータ更新を実行した後、アップグレードされたデータベースをデータ アップグレード サンドボックス環境から実稼働環境にコピーするには、他のタイプの LCS サービス リクエストが必要です。</span><span class="sxs-lookup"><span data-stu-id="92fab-121">After you perform a data upgrade in the sandbox environment, a LCS other type service requests is needed to copy your upgraded database from the data upgrade sandbox environment into your production environment.</span></span> <span data-ttu-id="92fab-122">以下の電子メール テンプレートは、ユーザーの使用のため提供されています。</span><span class="sxs-lookup"><span data-stu-id="92fab-122">The email template below is provided for your use</span></span>
>[!コピー]<span data-ttu-id="92fab-123"> これは、サンドボックス環境<source sandbox environment name>から本番環境への 2012 データ アップグレード データベース コピーの要求です。</span><span class="sxs-lookup"><span data-stu-id="92fab-123"> This is a request for 2012 data upgrade database copy from the sandbox environment <source sandbox environment name> to production.</span></span> <span data-ttu-id="92fab-124">現在稼働中のデータベースを上書きすることに同意します。</span><span class="sxs-lookup"><span data-stu-id="92fab-124">I acknowledge that this will overwrite the database currently in production.</span></span>

- <span data-ttu-id="92fab-125">次のタスクを追加しました。</span><span class="sxs-lookup"><span data-stu-id="92fab-125">We added the following tasks:</span></span>
    - <span data-ttu-id="92fab-126">スモーク テストを実行します。</span><span class="sxs-lookup"><span data-stu-id="92fab-126">Perform a smoke test.</span></span>
    - <span data-ttu-id="92fab-127">アプリケーションの設定タスクを完了します。</span><span class="sxs-lookup"><span data-stu-id="92fab-127">Complete application setup tasks.</span></span> <span data-ttu-id="92fab-128">このステップは、使用する機能に応じて大規模になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-128">This step can be large, depending on the functionality that is used.</span></span> <span data-ttu-id="92fab-129">このステップでは、機能チームは新しいアプリケーションの機能を構成して、アップグレードされたシステムで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="92fab-129">During this step, the functional team configures new application functionality so that it's ready to be used in the upgraded system.</span></span>
    - <span data-ttu-id="92fab-130">ユーザーがシステムに戻れるようにします。</span><span class="sxs-lookup"><span data-stu-id="92fab-130">Allow users back in.</span></span> <span data-ttu-id="92fab-131">アップグレードが完了して、システムを再度使用できることをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="92fab-131">Notify your user base that the upgrade is completed and that they can use the system again.</span></span>

> [!NOTE]
> <span data-ttu-id="92fab-132">この記事では、*サンドボックス* という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 または 3)、またはより高度な環境を示します。</span><span class="sxs-lookup"><span data-stu-id="92fab-132">In this article, we use the term *sandbox* to refer to a Standard or Premier Acceptance Testing (Tier 2 or 3) or higher environment connected to a SQL Azure database.</span></span>

## <a name="technical-workstream"></a><span data-ttu-id="92fab-133">技術的なワーク ストリーム</span><span class="sxs-lookup"><span data-stu-id="92fab-133">Technical workstream</span></span>

<span data-ttu-id="92fab-134">技術的なワークストリームに含まれるさまざまな技術チームのメンバー: データベース管理者 (DBA)、AX 2012 のシステム管理者、サーバー管理者、AX 2012 および Finance and Operations に精通している開発者。</span><span class="sxs-lookup"><span data-stu-id="92fab-134">The technical workstream involves various technical team members: the database administrator (DBA), the AX 2012 system administrator, server administrators, and developers who are familiar with AX 2012 and Finance and Operations.</span></span> 

<span data-ttu-id="92fab-135">切替テスト中には、技術チームは、データ アップグレード プロセスのパフォーマンスと信頼性のテストに焦点を当てて、ビジネスのダウンタイム制限を満たすようにします。</span><span class="sxs-lookup"><span data-stu-id="92fab-135">During cutover testing, the technical team is focused on performance and reliability testing of the data upgrade process, to make sure that it meets the business's downtime limit.</span></span> <span data-ttu-id="92fab-136">ハードウェアとソフトウェアの多くの要素がこのプロセスに関連しています。</span><span class="sxs-lookup"><span data-stu-id="92fab-136">Many elements of hardware and software are involved in this process.</span></span> <span data-ttu-id="92fab-137">これらの要素の一部はオンプレミスですが、他の要素は Microsoft クラウドに含まれています。</span><span class="sxs-lookup"><span data-stu-id="92fab-137">Some of these elements are on-premises, whereas others are in the Microsoft cloud.</span></span> <span data-ttu-id="92fab-138">加えて、カスタム アプリケーション コードと標準コードの多くの要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="92fab-138">In addition, many elements of custom application code and standard code are involved.</span></span> <span data-ttu-id="92fab-139">このテストの結果は、環境の切替プロセスを信頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-139">The result of this testing should be confidence in the cutover process for your environment.</span></span>

### <a name="technical-workstream-process"></a><span data-ttu-id="92fab-140">技術的なワーク ストリーム プロセス</span><span class="sxs-lookup"><span data-stu-id="92fab-140">Technical workstream process</span></span>

> [!NOTE]
> <span data-ttu-id="92fab-141">技術的なワークストリームについては、切替テストのプロセスは、実際/稼働の切替プロセスの高レベルの手順と同じです。</span><span class="sxs-lookup"><span data-stu-id="92fab-141">For the technical workstream, the cutover testing process is the same as the high-level steps of the actual/go-live cutover process.</span></span>

<span data-ttu-id="92fab-142">技術的なワークストリームについては、切替テストのプロセスは [AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード](upgrade-data-sandbox.md) で説明したものと同じです。</span><span class="sxs-lookup"><span data-stu-id="92fab-142">For the technical workstream, the cutover testing process is the same described in [Upgrade from AX 2012 - Data upgrade in sandbox environments](upgrade-data-sandbox.md).</span></span>

## <a name="functional-workstream"></a><span data-ttu-id="92fab-143">機能的なワーク ストリーム</span><span class="sxs-lookup"><span data-stu-id="92fab-143">Functional workstream</span></span>

<span data-ttu-id="92fab-144">データのアップグレード後に、新しい環境でいくつかのコンフィギュレーション タスクが必要になります。</span><span class="sxs-lookup"><span data-stu-id="92fab-144">After data upgrade, several configuration tasks will be required in the new environment.</span></span> <span data-ttu-id="92fab-145">このワーク ストリームの目的は、すべてのコンフィギュレーション タスクを文書化および定量化し、リソースを各タスクに割り当てることで、ダウンタイム期間中にこれらのタスクを機能的なワーク ストリームとともに実行できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="92fab-145">The goal of this workstream is to document and quantify all configuration tasks, and to assign a resource to each task, to help guarantee that these tasks can be done together with the technical workstream during the downtime window.</span></span>

<span data-ttu-id="92fab-146">通常、機能的なタスクでは、特定のシステム パラメータの値または他のコンフィギュレーション データの値の変更が含まれます。</span><span class="sxs-lookup"><span data-stu-id="92fab-146">Typically, functional tasks involve changing the values of specific system parameters or other configuration data.</span></span> <span data-ttu-id="92fab-147">これらのタスクは、機能テストのパス全体を通して識別されます。これは、切替テストとは別のアクティビティです。</span><span class="sxs-lookup"><span data-stu-id="92fab-147">These tasks are identified through the full functional test pass, which is a separate activity from the cutover testing.</span></span> <span data-ttu-id="92fab-148">このタイプのタスクが特定された場合、機能のリソースおよび開発者と共に確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-148">When a task of this type is identified, it should be reviewed together with the functional resource and your developer.</span></span>

<span data-ttu-id="92fab-149">より大きな変更を行うには、新しいカスタム データ アップグレード スクリプトを作成して、データのアップグレード プロセス中にデータを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-149">Larger changes might require that a new custom data upgrade script be written to update the data during the data upgrade process.</span></span> <span data-ttu-id="92fab-150">ただし、機能のリソースは、データのアップグレード後に新しいシステムを使用して、より小さな変更を手動で実行できます。</span><span class="sxs-lookup"><span data-stu-id="92fab-150">However, the functional resource can manually run smaller changes through the new system after data upgrade.</span></span>

<span data-ttu-id="92fab-151">新しいデータのアップグレード スクリプトを持つ、より大規模な変更をテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-151">Larger changes that have new data upgrade scripts must be tested.</span></span> <span data-ttu-id="92fab-152">したがって、MajorVersionDataUpgrade.zip パッケージの 1 つ以上の追加の繰り返しを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-152">Therefore, one or more additional iterations of the MajorVersionDataUpgrade.zip package will have to be run.</span></span> <span data-ttu-id="92fab-153">手動のデータ入力のコストに対して、パッケージを再度実行するコストを比較検討することが重要です。</span><span class="sxs-lookup"><span data-stu-id="92fab-153">It's important that you weigh the cost of running the package again against the cost of manual data entry.</span></span>

<span data-ttu-id="92fab-154">手動による変更のたびに、切替計画ドキュメントにタスクを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-154">For each manual change, a task must be added to the cutover plan document.</span></span> <span data-ttu-id="92fab-155">このタスクでは、次の詳細を示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-155">This task must show the following details:</span></span>

-   <span data-ttu-id="92fab-156">タスクとは何か、また必要な作業は何か。</span><span class="sxs-lookup"><span data-stu-id="92fab-156">What is the task, and what must be done?</span></span>
-   <span data-ttu-id="92fab-157">そのタスクを実行するのは誰か。</span><span class="sxs-lookup"><span data-stu-id="92fab-157">Who must do it?</span></span>
-   <span data-ttu-id="92fab-158">時間はどのくらいかかるか。</span><span class="sxs-lookup"><span data-stu-id="92fab-158">How long does it take?</span></span>

### <a name="add-users-and-perform-functionl-tests"></a><span data-ttu-id="92fab-159">ユーザーの追加、および機能テストの実行</span><span class="sxs-lookup"><span data-stu-id="92fab-159">Add users, and perform functionl tests</span></span>
<span data-ttu-id="92fab-160">環境を完全に構成したときは、ユーザーを追加し、適切なテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="92fab-160">When you have fully configured your environment, add users, and perform appropriate testing.</span></span> 

## <a name="roll-back-to-ax-2012"></a><span data-ttu-id="92fab-161">AX 2012 にロールバックする</span><span class="sxs-lookup"><span data-stu-id="92fab-161">Roll back to AX 2012</span></span>

<span data-ttu-id="92fab-162">このタスクの目的は、AX 2012 をオフにしたときのバックアップを使用してデータベースを復元し、AX 2012 を再度オンにすることです。</span><span class="sxs-lookup"><span data-stu-id="92fab-162">The goal of this task is to restore the database by using the backup that was made when AX 2012 was turned off, and then turn AX 2012 back on.</span></span> <span data-ttu-id="92fab-163">統合システムの状態も復元する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-163">The state of integrated systems might also have to be restored.</span></span> <span data-ttu-id="92fab-164">ただし、統合システムは企業間で異なるため、特定の状況に応じてこのシナリオを個別に計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92fab-164">However, because integrated systems vary from business to business, you must plan for this scenario independently, based on your specific circumstances.</span></span> <span data-ttu-id="92fab-165">ロールバックする必要はありませんが、必要な場合に備えてテスト済みのプロセスがあることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="92fab-165">Although it's unlikely that you will have to roll back, it's very important that you have a tested process in case you require it.</span></span>

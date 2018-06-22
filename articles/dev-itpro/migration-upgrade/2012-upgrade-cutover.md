---
title: "AX 2012 からのアップグレード - Go live"
description: "このトピックでは、AX 2012 をオフにしてから、Microsoft Dynamics 365 for Finance and Operations でコードとデータベースのアップグレード バージョンの実行が完了するまでの最終的な切替えプロセスについて説明します。"
author: robadawy
manager: AnnBe
ms.date: 03/22/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2018-03-31
ms.dyn365.ops.version: Platform update 12
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 383cb8909d358c75e64e89472eb36a55ac02584a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="upgrade-from-ax-2012---cutover-process-go-live"></a><span data-ttu-id="a9fbe-103">AX 2012 からのアップグレード - 切替プロセス (Go live)</span><span class="sxs-lookup"><span data-stu-id="a9fbe-103">Upgrade from AX 2012 - Cutover process (Go live)</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="a9fbe-104">標準またはプレミア承認テスト環境 (サンドボックス レベル 2 またはそれ以上) でアップグレード テストを正常に完了した場合、および正常にテスト切替を完了した後、実稼働環境をアップグレードして稼働するその時が来ました。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-104">After you have successfully completed upgrade testing in a Standard or Premier Acceptance Test environment (Sandbox Tier 2 or higher), and you have also completed a successful test cutover, the moment has arrived to upgrade your production environment and go live.</span></span>

<span data-ttu-id="a9fbe-105">*切替*という用語は、新しいシステムを稼働させる最後のプロセスに使用します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-105">*Cutover* is the term that we use for the final process of getting a new system live.</span></span> <span data-ttu-id="a9fbe-106">この切替プロセスは、Microsoft Dynamics AX 2012 をオフにした後、Microsoft Dynamics 365 for Finance and Operations をオンにする前に実行されるタスクで構成されています。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-106">This cutover process consists of the tasks that occur after Microsoft Dynamics AX 2012 is turned off but before Microsoft Dynamics 365 for Finance and Operations, is turned on.</span></span> <span data-ttu-id="a9fbe-107">最終的な切替を計画する前に、[切替テスト](./upgrade-cutover-testing.md)で説明されているように成功した切替モックを正常に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-107">Before you plan your final cutover, you need to successfully complete one successful mock cutover as described in [Cutover testing](./upgrade-cutover-testing.md)</span></span>

<span data-ttu-id="a9fbe-108">次の図は、実稼動環境で発生するような、切替中の全体的なプロセスを示しています。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-108">The following illustration shows the overall process for cutover to go-live as it will occur in the production environment.</span></span>

![切替プロセス](./media/cutover_1.png)

> [!NOTE]
> <span data-ttu-id="a9fbe-110">この記事では、*サンドボックス* という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 または 3)、またはより高度な環境を示します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-110">In this article, we use the term *sandbox* to refer to a Standard or Premier Acceptance Testing (Tier 2 or 3) or higher environment connected to a SQL Azure database.</span></span>

## <a name="overall-process"></a><span data-ttu-id="a9fbe-111">全体的なプロセス</span><span class="sxs-lookup"><span data-stu-id="a9fbe-111">Overall process</span></span>

<span data-ttu-id="a9fbe-112">これらは、実稼働環境のアップグレード プロセスの大まかな手順です。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-112">These are the high-level steps of the production environment upgrade process.</span></span>

1.  <span data-ttu-id="a9fbe-113">Lifecycle Services (LCS) を通じて **その他のタイプ** サービス要求を送信し、実稼働環境をアップグレードするという目的を Microsoft サービス エンジニア リング (DSE) チームに通知します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-113">Submit an **Other type** service request through Lifecycle Services (LCS) to notify the Microsoft Service Engineering (DSE) team of your intention to upgrade a production environment.</span></span> <span data-ttu-id="a9fbe-114">Microsoft solution architect と協力して十分の通知期間 (2、3 週間前) があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-114">Work with your Microsoft solution architect and ensure you do this with plenty of notice (2 to 3 weeks in advance).</span></span> <span data-ttu-id="a9fbe-115">これが最終的な切替であることをサービス要求で示します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-115">Indicate in the service request that this is a final cutover.</span></span>
    - <span data-ttu-id="a9fbe-116">正常に切替モックが完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-116">Make sure you have already completed a successful mock cutover.</span></span>
    - <span data-ttu-id="a9fbe-117">切替要求は DSE チームの空き状況に左右されますので、事前に計画してください。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-117">Cutover requests are subject to availability of the DSE team, please plan ahead.</span></span>
2.  <span data-ttu-id="a9fbe-118">AX 2012 AOS のすべてのインスタンスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-118">Turn off all AX 2012 AOS instances.</span></span>
3.  <span data-ttu-id="a9fbe-119">AX 2012 データベースをバックアップし、元のデータベースに対して T-SQL スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-119">Back up the AX 2012 database and run the T-SQL scripts against the original database.</span></span>
4.  <span data-ttu-id="a9fbe-120">SQLPackage.exe (ダウンロード可能な無料の SQL Server ツール) を使用して、コピーされたデータベースを bacpac ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-120">Export the copied database to a bacpac file by using the SQLPackage.exe (a free SQL Server tool available for download).</span></span> <span data-ttu-id="a9fbe-121">このツールでは、SQL データベースにインポートできる特別な種類のデータベース バックアップを提供します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-121">This tool provides a special type of database backup that can be imported into SQL Database.</span></span> 
5.  <span data-ttu-id="a9fbe-122">bacpac ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-122">Upload the bacpac file.</span></span>
6.  <span data-ttu-id="a9fbe-123">サンドボックス環境で bacpac ファイルを Application Object Server (AOS) 仮想マシンにダウンロードし、SQLPackage.exe を使用してインポートします。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-123">Download the bacpac file to the Application Object Server (AOS) virtual machine in the sandbox environment, and then import it by using SQLPackage.exe.</span></span> 
7.  <span data-ttu-id="a9fbe-124">データベースがアップグレード準備完了であることを Microsoft DSE チームに通知し、サンドボックスから実稼働環境にインポートされたデータベースをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-124">Notify the Microsoft DSE team that your database is ready for upgrade – they will copy the imported database from sandbox to the production environment.</span></span>
8.  <span data-ttu-id="a9fbe-125">Microsoft DSE チームは、インポートされたデータベースに対して適切なデータ アップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-125">The Microsoft DSE team will run the data upgrade against the imported database.</span></span>
9.  <span data-ttu-id="a9fbe-126">データ アップグレードが完了すると、Microsoft DSE チームにより通知されます。この時点で、ログインして、ポスト アップグレードに必要な機能構成タスクを完了し、エンド ユーザーが新しいシステムに戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-126">The Microsoft DSE team will notify you once the data upgrade is complete – at this point you can log in and complete any functional configuration tasks required post-upgrade before you allow the end users back into the new system.</span></span>

<span data-ttu-id="a9fbe-127">上記の手順は、モック切替中に実行した手順に似ています。詳細な手順については、「[切替テスト](./upgrade-cutover-testing.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-127">The steps above resemble the steps you have performed during the mock cutover, refer to [Cutover testing](./upgrade-cutover-testing.md) for detailed instructions.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a9fbe-128">前提条件</span><span class="sxs-lookup"><span data-stu-id="a9fbe-128">Prerequisites</span></span> 
<span data-ttu-id="a9fbe-129">実稼動環境でアップグレードを実行する前に、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-129">Before you can perform an upgrade in the production environment the following prerequisites must be met:</span></span>
-   <span data-ttu-id="a9fbe-130">サンドボックス環境でコードのアップグレードとデータのアップグレードを完了し、機能テスト パスを正常に完了しました</span><span class="sxs-lookup"><span data-stu-id="a9fbe-130">Complete the code upgrade and data upgrade in a sandbox environment and successfully completed a functional test pass</span></span>
-   <span data-ttu-id="a9fbe-131">実稼働環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-131">Deploy the production environment.</span></span> <span data-ttu-id="a9fbe-132">実稼働環境の配置を要求するオプションが点灯する前に完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-132">Before the option to request the deployment of the production environment lights up you must have completed:</span></span>
    - <span data-ttu-id="a9fbe-133">LCS のサブスクリプション見積もりツール。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-133">The Subscription estimator in LCS.</span></span> <span data-ttu-id="a9fbe-134">必要なスループットの詳細を提供しているため、これを使用して実稼働環境のサイズの変更を支援します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-134">We use this to help us size your production environment because it provides details of the throughput you’ll require.</span></span>
    - <span data-ttu-id="a9fbe-135">LCS での手法のテスト フェーズ。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-135">The Test phase of the methodology in LCS.</span></span> <span data-ttu-id="a9fbe-136">これは、プロダクション環境でテストを開始する準備ができているプロジェクトの段階にあることを確認するためです。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-136">This is to help ensure that you’re at the stage in your project where you’re ready to start testing in the production environment.</span></span>
    - <span data-ttu-id="a9fbe-137">実稼働環境を配置するために要求が Microsoft に送信された後、配置には、約 24 時間かかるので、そのために十分な時間を確保してください。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-137">After a request is submitted to Microsoft to deploy the production environment, it will take roughly 24 hours to deploy, so ensure that you leave enough time for this to happen.</span></span>
-   <span data-ttu-id="a9fbe-138">すべての必要な更新プログラムおよびカスタマイズ (AOT 配置可能パッケージ) を実稼動環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-138">Apply all necessary updates and customizations (AOT deployable packages) to the production environment.</span></span>
-   <span data-ttu-id="a9fbe-139">Microsoft Solution Architect と協力してアップグレードをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-139">Work with your Microsoft Solution Architect to schedule your upgrade.</span></span> <span data-ttu-id="a9fbe-140">アップグレードをスケジュールするには、LCS から「その他の」タイプのサービス要求を送信することで DSE チームにタイムスロットを要求します。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-140">To schedule an upgrade, request a timeslot with the DSE team by submitting “Other” type service requests from LCS.</span></span> <span data-ttu-id="a9fbe-141">これは、優先タイム スロットが使用できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-141">This is to ensure that the preferred timeslots will be available for you.</span></span> <span data-ttu-id="a9fbe-142">週末の間などスロットの需要が大幅に高くなるため注意してください。できるだけ早くこれらを要求することにより優先スケジュールを達成できます。</span><span class="sxs-lookup"><span data-stu-id="a9fbe-142">Be aware that there is significantly higher demand for slots during the weekend, so requesting these as far in advance as possible will help attain your preferred schedule.</span></span>

## <a name="related-articles"></a><span data-ttu-id="a9fbe-143">関連記事</span><span class="sxs-lookup"><span data-stu-id="a9fbe-143">Related articles</span></span>
- [<span data-ttu-id="a9fbe-144">研修</span><span class="sxs-lookup"><span data-stu-id="a9fbe-144">Onboarding</span></span>](../../fin-and-ops/imp-lifecycle/onboard.md)
- <span data-ttu-id="a9fbe-145">[サービス要求を送信する](../lifecycle-services/submit-request-dynamics-service-engineering-team.md)</span><span class="sxs-lookup"><span data-stu-id="a9fbe-145">[Submit a service request](../lifecycle-services/submit-request-dynamics-service-engineering-team.md).</span></span>
- [<span data-ttu-id="a9fbe-146">AX 2012 からのアップグレード - 切替テスト</span><span class="sxs-lookup"><span data-stu-id="a9fbe-146">Upgrade from AX 2012 - Cutover testing</span></span>](./upgrade-cutover-testing.md)


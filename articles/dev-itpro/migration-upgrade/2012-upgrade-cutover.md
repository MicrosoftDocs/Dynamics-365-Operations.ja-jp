---
title: "AX 2012 からのアップグレード - Go live"
description: "このトピックでは、AX 2012 をオフにしてから、Microsoft Dynamics 365 for Finance and Operations でコードとデータベースのアップグレード バージョンの実行が完了するまでの最終的な切替えプロセスについて説明します。"
author: robadawy
manager: AnnBe
ms.date: 06/06/2018
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
ms.sourcegitcommit: 8914723f6ef436bfc9e3a98cc82d5486042b0761
ms.openlocfilehash: 67a343973e6f35faf9fea50de8698dd968e36aa0
ms.contentlocale: ja-jp
ms.lasthandoff: 06/07/2018

---

# <a name="upgrade-from-ax-2012---cutover-process-go-live"></a><span data-ttu-id="c1593-103">AX 2012 からのアップグレード - 切替プロセス (Go live)</span><span class="sxs-lookup"><span data-stu-id="c1593-103">Upgrade from AX 2012 - Cutover process (Go live)</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="c1593-104">標準またはプレミア承認テスト環境 (サンドボックス レベル 2 またはそれ以上) でアップグレード テストを正常に完了した場合、および正常にテスト切替を完了した後、実稼働環境をアップグレードして稼働するその時が来ました。</span><span class="sxs-lookup"><span data-stu-id="c1593-104">After you have successfully completed upgrade testing in a Standard or Premier Acceptance Test environment (Sandbox Tier 2 or higher), and you have also completed a successful test cutover, the moment has arrived to upgrade your production environment and go live.</span></span>

<span data-ttu-id="c1593-105">*切替*という用語は、新しいシステムを稼働させる最後のプロセスに使用します。</span><span class="sxs-lookup"><span data-stu-id="c1593-105">*Cutover* is the term that we use for the final process of getting a new system live.</span></span> <span data-ttu-id="c1593-106">この切替プロセスは、Microsoft Dynamics AX 2012 をオフにした後、Microsoft Dynamics 365 for Finance and Operations をオンにする前に実行されるタスクで構成されています。</span><span class="sxs-lookup"><span data-stu-id="c1593-106">This cutover process consists of the tasks that occur after Microsoft Dynamics AX 2012 is turned off but before Microsoft Dynamics 365 for Finance and Operations, is turned on.</span></span> <span data-ttu-id="c1593-107">最終的な切替を計画する前に、[切替テスト](./upgrade-cutover-testing.md)で説明されているように成功した切替モックを正常に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1593-107">Before you plan your final cutover, you need to successfully complete one successful mock cutover as described in [Cutover testing](./upgrade-cutover-testing.md)</span></span>

<span data-ttu-id="c1593-108">次の図は、実稼動環境で発生するような、切替中の全体的なプロセスを示しています。</span><span class="sxs-lookup"><span data-stu-id="c1593-108">The following illustration shows the overall process for cutover to go-live as it will occur in the production environment.</span></span>

![切替プロセス](./media/cutover_1.png)

> [!NOTE]
> <span data-ttu-id="c1593-110">この記事では、*サンドボックス* という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 または 3)、またはより高度な環境を示します。</span><span class="sxs-lookup"><span data-stu-id="c1593-110">In this article, we use the term *sandbox* to refer to a Standard or Premier Acceptance Testing (Tier 2 or 3) or higher environment connected to a SQL Azure database.</span></span>

## <a name="overall-process"></a><span data-ttu-id="c1593-111">全体的なプロセス</span><span class="sxs-lookup"><span data-stu-id="c1593-111">Overall process</span></span>

<span data-ttu-id="c1593-112">実稼動環境のアップグレード プロセスの高レベルの手順は切替モック プロセスと同じであり、詳細な指示については [切替テスト](./upgrade-cutover-testing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c1593-112">The high-level steps of the production environment upgrade process are the same as the Mock cutover process, refer to [Cutover testing](./upgrade-cutover-testing.md) for detailed instructions.</span></span>


1. <span data-ttu-id="c1593-113">AX 2012 AOS インスタンスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="c1593-113">Turn off the AX 2012 AOS instances</span></span>
2. <span data-ttu-id="c1593-114">AX 2012 データベースのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="c1593-114">Create a copy of the AX 2012 database.</span></span> <span data-ttu-id="c1593-115">エクスポートするコピーの一部のオブジェクトを削除する必要があるため、コピーを使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c1593-115">We strongly recommend that you use a copy, because you must delete some objects in the copy that will be exported.</span></span>
3. <span data-ttu-id="c1593-116">SQLPackage.exe という名前の無料の SQL Server ツールを使用して、コピーされたデータベースを bacpac ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="c1593-116">Export the copied database to a bacpac file by using a free SQL Server tool that is named SQLPackage.exe.</span></span> <span data-ttu-id="c1593-117">このツールでは、SQL データベースにインポートできる特別な種類のデータベース バックアップを提供します。</span><span class="sxs-lookup"><span data-stu-id="c1593-117">This tool provides a special type of database backup that can be imported into SQL Database.</span></span>
4. <span data-ttu-id="c1593-118">Azure ストレージに bacpac ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="c1593-118">Upload the bacpac file to Azure storage.</span></span>
5. <span data-ttu-id="c1593-119">サンドボックス環境で bacpac ファイルを Application Object Server (AOS) コンピューターにダウンロードし、SQLPackage.exe を使用してインポートします。</span><span class="sxs-lookup"><span data-stu-id="c1593-119">Download the bacpac file to the Application Object Server (AOS) machine in the sandbox environment, and then import it by using SQLPackage.exe.</span></span> <span data-ttu-id="c1593-120">SQL データベースのユーザーをリセットするには、インポートされたデータベースに対してスクリプトを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1593-120">You must then run a script against the imported database to reset the SQL database users.</span></span>
6. <span data-ttu-id="c1593-121">インポートされたデータベースに対して適切なデータ アップグレード パッケージを実行します。</span><span class="sxs-lookup"><span data-stu-id="c1593-121">Run the appropriate data upgrade package against the imported database.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c1593-122">前提条件</span><span class="sxs-lookup"><span data-stu-id="c1593-122">Prerequisites</span></span> 
<span data-ttu-id="c1593-123">実稼動環境でアップグレードを実行する前に、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1593-123">Before you can perform an upgrade in the production environment the following prerequisites must be met:</span></span>
-   <span data-ttu-id="c1593-124">サンドボックス環境でコードのアップグレードとデータのアップグレードを完了し、機能テスト パスを正常に完了しました</span><span class="sxs-lookup"><span data-stu-id="c1593-124">Complete the code upgrade and data upgrade in a sandbox environment and successfully completed a functional test pass</span></span>
-   <span data-ttu-id="c1593-125">実稼働環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="c1593-125">Deploy the production environment.</span></span> <span data-ttu-id="c1593-126">実稼働環境の配置を要求するオプションが点灯する前に完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1593-126">Before the option to request the deployment of the production environment lights up you must have completed:</span></span>
    - <span data-ttu-id="c1593-127">LCS のサブスクリプション見積もりツール。</span><span class="sxs-lookup"><span data-stu-id="c1593-127">The Subscription estimator in LCS.</span></span> <span data-ttu-id="c1593-128">必要なスループットの詳細を提供しているため、これを使用して実稼働環境のサイズの変更を支援します。</span><span class="sxs-lookup"><span data-stu-id="c1593-128">We use this to help us size your production environment because it provides details of the throughput you’ll require.</span></span>
    - <span data-ttu-id="c1593-129">LCS での手法のテスト フェーズ。</span><span class="sxs-lookup"><span data-stu-id="c1593-129">The Test phase of the methodology in LCS.</span></span> <span data-ttu-id="c1593-130">これは、プロダクション環境でテストを開始する準備ができているプロジェクトの段階にあることを確認するためです。</span><span class="sxs-lookup"><span data-stu-id="c1593-130">This is to help ensure that you’re at the stage in your project where you’re ready to start testing in the production environment.</span></span>
    - <span data-ttu-id="c1593-131">実稼働環境を配置するために要求が Microsoft に送信された後、配置には、約 24 時間かかるので、そのために十分な時間を確保してください。</span><span class="sxs-lookup"><span data-stu-id="c1593-131">After a request is submitted to Microsoft to deploy the production environment, it will take roughly 24 hours to deploy, so ensure that you leave enough time for this to happen.</span></span>
-   <span data-ttu-id="c1593-132">すべての必要な更新プログラムおよびカスタマイズ (AOT 配置可能パッケージ) を実稼動環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="c1593-132">Apply all necessary updates and customizations (AOT deployable packages) to the production environment.</span></span> <span data-ttu-id="c1593-133">切替モックでサイン オフした後は、コードを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="c1593-133">There should not be any code change after signing off on a Mock cutover.</span></span>
-   <span data-ttu-id="c1593-134">アップグレードをスケジュールするには、[AX 2012 からのアップグレード- 切替テスト (切替モック) ](./upgrade-cutover-testing.md) に説明されているように、LCS から「その他」のタイプのサービスリクエストを送信して、DSE チームにタイムスロットを要求します。</span><span class="sxs-lookup"><span data-stu-id="c1593-134">To schedule an upgrade, request a timeslot with the DSE team by submitting “Other” type service requests from LCS as described in the [Upgrade from AX 2012 - Cutover testing (Mock cutover)](./upgrade-cutover-testing.md).</span></span> <span data-ttu-id="c1593-135">これは、優先タイム スロットが使用できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="c1593-135">This is to ensure that the preferred timeslots will be available for you.</span></span> <span data-ttu-id="c1593-136">週末の間などスロットの需要が大幅に高くなるため注意してください。できるだけ早くこれらを要求することにより優先スケジュールを達成できます。</span><span class="sxs-lookup"><span data-stu-id="c1593-136">Be aware that there is significantly higher demand for slots during the weekend, so requesting these as far in advance as possible will help attain your preferred schedule.</span></span>

## <a name="related-articles"></a><span data-ttu-id="c1593-137">関連記事</span><span class="sxs-lookup"><span data-stu-id="c1593-137">Related articles</span></span>
- [<span data-ttu-id="c1593-138">研修</span><span class="sxs-lookup"><span data-stu-id="c1593-138">Onboarding</span></span>](../../fin-and-ops/imp-lifecycle/onboard.md)
- <span data-ttu-id="c1593-139">[サービス要求を送信する](../lifecycle-services/submit-request-dynamics-service-engineering-team.md)</span><span class="sxs-lookup"><span data-stu-id="c1593-139">[Submit a service request](../lifecycle-services/submit-request-dynamics-service-engineering-team.md).</span></span>
- [<span data-ttu-id="c1593-140">AX 2012 からのアップグレード - 切替テスト</span><span class="sxs-lookup"><span data-stu-id="c1593-140">Upgrade from AX 2012 - Cutover testing</span></span>](./upgrade-cutover-testing.md)


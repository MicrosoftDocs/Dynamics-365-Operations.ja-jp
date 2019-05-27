---
title: 最新バージョンへのセルフサービス アップグレード
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の最新の更新バージョンに移行するプロセスについて説明します。
author: laneswenka
manager: AnnBe
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7b2fa2f75d9a018b2ffe192026eb5aefe6491994
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506202"
---
# <a name="self-service-upgrade-to-the-latest-version"></a><span data-ttu-id="2aaf8-103">最新バージョンへのセルフサービス アップグレード</span><span class="sxs-lookup"><span data-stu-id="2aaf8-103">Self-service upgrade to the latest version</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="2aaf8-104">このトピックは、次の開始バージョンに適用されます:</span><span class="sxs-lookup"><span data-stu-id="2aaf8-104">This topic applies to the following starting versions:</span></span>
>
> - <span data-ttu-id="2aaf8-105">Microsoft Dynamics AX 7.0 (2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="2aaf8-105">Microsoft Dynamics AX 7.0 (February 2016)</span></span>
> - <span data-ttu-id="2aaf8-106">Microsoft Dynamics 365 for Operations バージョン 1611 (2016 年 11 月) (バージョン 7.1 とも呼ばれます)</span><span class="sxs-lookup"><span data-stu-id="2aaf8-106">Microsoft Dynamics 365 for Operations version 1611 (November 2016) (also known as version 7.1)</span></span>
> - <span data-ttu-id="2aaf8-107">Microsoft Dynamics 365 for Finance and Operations Enterprise edition (2017 年 7 月) (バージョン 7.2 とも呼ばれます)</span><span class="sxs-lookup"><span data-stu-id="2aaf8-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) (also known as version 7.2)</span></span>
> - <span data-ttu-id="2aaf8-108">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3</span><span class="sxs-lookup"><span data-stu-id="2aaf8-108">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3</span></span>

<span data-ttu-id="2aaf8-109">このチュートリアルでは、これらのタスクを実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-109">In this tutorial, you will learn how to perform these tasks:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="2aaf8-110">選択するバージョンを把握します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-110">Understand which version to select.</span></span>
> * <span data-ttu-id="2aaf8-111">カスタマイズを拡張機能としてリファクターします。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-111">Refactor your customizations as extensions.</span></span>
> * <span data-ttu-id="2aaf8-112">開発環境でのデータ アップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-112">Run the data upgrade in a development environment.</span></span>
> * <span data-ttu-id="2aaf8-113">サンドボックス ユーザー受け入れテスト (UAT) 環境で、セルフサービス アップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-113">Do a self-service upgrade in a sandbox user acceptance testing (UAT) environment.</span></span>
> * <span data-ttu-id="2aaf8-114">実稼働環境でセルフサービス アップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-114">Do a self-service upgrade in a production environment.</span></span>

## <a name="understand-which-version-to-select-for-upgrade"></a><span data-ttu-id="2aaf8-115">アップグレードするために選択するバージョンを把握します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-115">Understand which version to select for upgrade</span></span>

<span data-ttu-id="2aaf8-116">継続的な更新をサポートするようにセルフサービス アップグレード プロセスを調整するに、新しいリリースごとに最も古いリリースバージョンが廃止されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-116">To align the self-service upgrade process to support continuous updates, each new release will cause the oldest release version to be discontinued.</span></span>

<span data-ttu-id="2aaf8-117">たとえば、プラットフォーム アップデート (PU) 23 を適用したアプリケーション バージョン 7.3 があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-117">For example, you have application version 7.3 with platform update (PU) 23.</span></span> <span data-ttu-id="2aaf8-118">現在サポートされているアップグレード バージョンは、PU 23 の 8.1.3、PU 24 の 10.0.0、そして PU 25 の 10.0.1です。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-118">Currently, the supported upgrade versions are 8.1.3 with PU 23, 10.0.0 with PU 24, and 10.0.1 with PU 25.</span></span> <span data-ttu-id="2aaf8-119">次のリリースである PU 26 の 10.0.2 が一般に利用可能になると、それは使用可能なアップグレード オプションに追加され、PU 23 の 8.1.3 は削除されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-119">When the next release, 10.0.2 with PU 26, is made generally available, it will be added to the available upgrade options, and 8.1.3 with PU 23 will be removed.</span></span>

<span data-ttu-id="2aaf8-120">新しいバージョンを追加して最も古いバージョンを削除するこの継続的なプロセスのため、顧客が利用可能な最新バージョンにアップグレードすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-120">Because of this continuous process of adding a new version and removing the oldest version, we recommend that customers upgrade to the latest version that is available.</span></span> <span data-ttu-id="2aaf8-121">このように、サンドボックス環境をアップグレードしてから、後で実稼働環境を同じバージョンにアップグレードできるようになるまで 2 か月あります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-121">In that way, you have two months in which you can upgrade your sandbox environment and then later upgrade your production environment to the same version.</span></span>

<span data-ttu-id="2aaf8-122">サンドボックス環境を PU 23 の 8.1.3 にアップグレードすることを選択して、その後 Microsoft が PU 26 のバージョン 10.0.2 をリリースし、PU 23 のバージョン 8.1.3 がアップグレード オプションとして削除されると、実稼働環境のアップグレードから **ブロックされます**。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-122">If you choose to upgrade your sandbox environment to version 8.1.3 with PU 23 and Microsoft then releases version 10.0.2 with PU 26, so that version 8.1.3 with PU 23 is removed as an upgrade option, **you will be blocked** from upgrading your production environment.</span></span> <span data-ttu-id="2aaf8-123">この場合は、サンドボックス環境からやり直し、新しいサポート対象バージョンにアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-123">In this case, you must start over in the sandbox environment and upgrade to a newer supported version.</span></span>

### <a name="targeted-release-schedule"></a><span data-ttu-id="2aaf8-124">対象となるリリース スケジュール</span><span class="sxs-lookup"><span data-stu-id="2aaf8-124">Targeted release schedule</span></span>

> [!NOTE]
> <span data-ttu-id="2aaf8-125">この表の日付は変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-125">The dates in this table are subject to change.</span></span>

| <span data-ttu-id="2aaf8-126">選択可能なバージョン</span><span class="sxs-lookup"><span data-stu-id="2aaf8-126">Selectable versions</span></span> | <span data-ttu-id="2aaf8-127">新規顧客向けの最新バージョンの一般提供 (GA)</span><span class="sxs-lookup"><span data-stu-id="2aaf8-127">General availability (GA) of the latest version for new customers</span></span> | <span data-ttu-id="2aaf8-128">アップグレードの最新バージョンの GA</span><span class="sxs-lookup"><span data-stu-id="2aaf8-128">GA of the latest version for upgrade</span></span> |
|---|---|---|
| <span data-ttu-id="2aaf8-129">7.3 の PU 23 – PU 25</span><span class="sxs-lookup"><span data-stu-id="2aaf8-129">7.3 with PU 23 – PU 25</span></span><br><span data-ttu-id="2aaf8-130">8.1.3 の PU 23 – 10.0.1 の PU 25</span><span class="sxs-lookup"><span data-stu-id="2aaf8-130">8.1.3 with PU 23 – 10.0.1 with PU 25</span></span> | <span data-ttu-id="2aaf8-131">2019年4月8日の週</span><span class="sxs-lookup"><span data-stu-id="2aaf8-131">Week of April 8, 2019</span></span> | <span data-ttu-id="2aaf8-132">2019 年 4 月 29 日の週</span><span class="sxs-lookup"><span data-stu-id="2aaf8-132">Week of April 29, 2019</span></span> |
| <span data-ttu-id="2aaf8-133">7.3 の PU 24 – PU 26</span><span class="sxs-lookup"><span data-stu-id="2aaf8-133">7.3 with PU 24 – PU 26</span></span><br><span data-ttu-id="2aaf8-134">10.0.0 の PU 24 – 10.0.2 の PU 26</span><span class="sxs-lookup"><span data-stu-id="2aaf8-134">10.0.0 with PU 24 – 10.0.2 with PU 26</span></span> | <span data-ttu-id="2aaf8-135">2019年5月13日の週</span><span class="sxs-lookup"><span data-stu-id="2aaf8-135">Week of May 13, 2019</span></span> | <span data-ttu-id="2aaf8-136">2019 年 5 月 27 日の週</span><span class="sxs-lookup"><span data-stu-id="2aaf8-136">Week of May 27, 2019</span></span> |
| <span data-ttu-id="2aaf8-137">7.3 の PU 25 – PU 27</span><span class="sxs-lookup"><span data-stu-id="2aaf8-137">7.3 with PU 25 – PU 27</span></span><br><span data-ttu-id="2aaf8-138">10.0.1 の PU 25 – 10.0.3 の PU 27</span><span class="sxs-lookup"><span data-stu-id="2aaf8-138">10.0.1 with PU 25 – 10.0.3 with PU 27</span></span> | <span data-ttu-id="2aaf8-139">2019年6月10日の週</span><span class="sxs-lookup"><span data-stu-id="2aaf8-139">Week of June 10, 2019</span></span> | <span data-ttu-id="2aaf8-140">2019 年 6 月 24 日の週</span><span class="sxs-lookup"><span data-stu-id="2aaf8-140">Week of June 24, 2019</span></span> |
| <span data-ttu-id="2aaf8-141">7.3 の PU 26 – PU 28</span><span class="sxs-lookup"><span data-stu-id="2aaf8-141">7.3 with PU 26 – PU 28</span></span><br><span data-ttu-id="2aaf8-142">10.0.2 の PU 26 – 10.0.4 の PU 28</span><span class="sxs-lookup"><span data-stu-id="2aaf8-142">10.0.2 with PU 26 – 10.0.4 with PU 28</span></span> | <span data-ttu-id="2aaf8-143">2019年7月8日の週</span><span class="sxs-lookup"><span data-stu-id="2aaf8-143">Week of July 8, 2019</span></span> | <span data-ttu-id="2aaf8-144">2019 年 7 月 29 日の週</span><span class="sxs-lookup"><span data-stu-id="2aaf8-144">Week of July 29, 2019</span></span> |

## <a name="refactor-your-customizations-as-extensions"></a><span data-ttu-id="2aaf8-145">カスタマイズを拡張機能としてリファクターします</span><span class="sxs-lookup"><span data-stu-id="2aaf8-145">Refactor your customizations as extensions</span></span>

<span data-ttu-id="2aaf8-146">アップグレードを準備するには、拡張機能としてオーバーレイされたすべてのカスタマイズをリファクターする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-146">To prepare for upgrade, you must refactor any customizations that were overlays as extensions.</span></span> <span data-ttu-id="2aaf8-147">最新バージョンに新しい開発環境を配置して、バージョン管理に新しいブランチを作成し、[オーバーレイから拡張機能への移行](../extensibility/migrate-overlayer-extension.md) のガイダンスに従うことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-147">We recommend that you deploy a new development environment on the latest version, create a new branch in version control, and follow the guidance in [Migrate from overlayering to extensions](../extensibility/migrate-overlayer-extension.md).</span></span>

<span data-ttu-id="2aaf8-148">オーバーレイがなくカスタマイズの 100 パーセントで拡張機能をすでに使用している場合は、バージョン管理におけるアップグレード作業のために新しいブランチを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-148">If you have no overlays and are already using extension for 100 percent of your customizations, we still recommend that you create a new branch for the upgrade effort in version control.</span></span> <span data-ttu-id="2aaf8-149">Microsoft X++ 修正プログラムがインストールされている場合、それらは最新バージョンに適用されないためバージョン管理から削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-149">If any Microsoft X++ hotfixes are installed, you must delete them from version control, because they aren't applicable to the latest version.</span></span>

## <a name="run-the-data-upgrade-in-a-development-environment"></a><span data-ttu-id="2aaf8-150">開発環境でのデータ アップグレードを実行します</span><span class="sxs-lookup"><span data-stu-id="2aaf8-150">Run the data upgrade in a development environment</span></span>

<span data-ttu-id="2aaf8-151">データ アップグレード プロセスを外部データベースのコピーで実行します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-151">Run the data upgrade process on a copy of your source database.</span></span> <span data-ttu-id="2aaf8-152">環境が既に実稼働状態にある場合、ソース データベースは実稼働データベースのコピーです。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-152">If your environment is already live in production, the source database is a copy of the production database.</span></span> <span data-ttu-id="2aaf8-153">それ以外の場合は、古いバージョンを実行している最新のデータベースです。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-153">Otherwise, it's your most current database that is running the old version.</span></span>

<span data-ttu-id="2aaf8-154">アップグレード対象のリリースを実行している開発環境でこのプロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-154">Run this process in the development environment that is running the release that you're upgrading to.</span></span> <span data-ttu-id="2aaf8-155">このステップは、開発者によって行われる検証プロセスです。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-155">This step is a validation process that is done by a developer.</span></span> <span data-ttu-id="2aaf8-156">これにより、手動操作を必要とせずに環境でカスタマイズの特定のセットを使用することで、データのアップグレードを完了できることの確認に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-156">It helps the developer verify that the data upgrade can be successfully completed by using the specific set of customizations in the environment, without requiring any manual intervention.</span></span>

<span data-ttu-id="2aaf8-157">実稼働データベースのコピーを作成するには [標準ユーザー受け入れテスト (UAT) データベースのコピーをエクスポートする](../database/dbmovement-scenario-exportuat.md) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-157">To make a copy of your production database, follow the steps in [Export a copy of the standard user acceptance test (UAT) database](../database/dbmovement-scenario-exportuat.md).</span></span>

<span data-ttu-id="2aaf8-158">データのアップグレード プロセスを実行するには、[開発環境やデモ環境でデータをアップグレードする](../migration-upgrade/upgrade-data-to-latest-update.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-158">To run the data upgrade process, follow the steps in [Upgrade data in development, or demo environments](../migration-upgrade/upgrade-data-to-latest-update.md).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="2aaf8-159">開発環境でのデータのアップグレードは必須ステップです。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-159">Data upgrade in a development environment is a required step.</span></span> <span data-ttu-id="2aaf8-160">これにより、サンドボックス UAT と実稼働環境をアップグレードする際に、後のダウンタイムの延長やアップグレード エラーのリスクを軽減できます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-160">It helps reduce the risk of extended downtime and upgrade errors later, when you upgrade sandbox UAT and production environments.</span></span>
> - <span data-ttu-id="2aaf8-161">データをアップグレードする前に複数のアプリケーション修正プログラムが必要なことがあります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-161">Several application hotfixes might be required before you can upgrade data.</span></span> <span data-ttu-id="2aaf8-162">既存の開発環境を再配置する前に、これらの修正プログラムが必要かどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-162">Before you redeploy your existing development environment, verify whether these hotfixes are required.</span></span> <span data-ttu-id="2aaf8-163">必要な修正プログラムをインストールし Microsoft Azure DevOps にチェックインします。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-163">Install the required hotfixes, and check them in to Microsoft Azure DevOps.</span></span> <span data-ttu-id="2aaf8-164">このステップは、開発環境の古いバージョンでのみで完了できます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-164">This step can be completed only in the old version of your development environment.</span></span> <span data-ttu-id="2aaf8-165">さまざまな状況で必要な修正プログラムの一覧については、[開発環境やデモ環境でデータをアップグレードする](upgrade-data-to-latest-update.md#before-you-begin) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-165">For a list of the hotfixes that are required in various situations, see [Upgrade data in develop, or demo environments](upgrade-data-to-latest-update.md#before-you-begin).</span></span>
 
## <a name="upgrade-your-tier-2-standard-acceptance-test-sandbox-environment"></a><span data-ttu-id="2aaf8-166">階層 2 以上のスタンダード承認テスト サンドボックス環境のアップグレード</span><span class="sxs-lookup"><span data-stu-id="2aaf8-166">Upgrade your Tier 2+ Standard Acceptance Test sandbox environment</span></span>

<span data-ttu-id="2aaf8-167">コード アップグレードを完了し、Microsoft SQL Server でデータを操作しなくても開発環境でエンド ツー エンドのデータ アップグレードを実行することができるようになったら、サンドボックス環境内でプロセスを開始することができます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-167">When you've completed the code upgrade and have been able to do an end-to-end data upgrade in your development environment without having to manipulate data in Microsoft SQL Server, you can begin the process in your sandbox environment.</span></span>

### <a name="prerequisite"></a><span data-ttu-id="2aaf8-168">前提条件</span><span class="sxs-lookup"><span data-stu-id="2aaf8-168">Prerequisite</span></span>

<span data-ttu-id="2aaf8-169">アップグレードを開始する前に、サンドボックス環境に最新の生産データがあることを確認しておくことを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-169">Before you begin your upgrade, we highly recommend that you make sure that your sandbox environment has the latest production data.</span></span> <span data-ttu-id="2aaf8-170">データ セットが最新の状態の場合、実稼働環境でアップグレードを確実に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-170">If the data set is up to date, you can have more confidence that the upgrade will work in the production environment.</span></span> <span data-ttu-id="2aaf8-171">この手順を完了するには、[トレーニング目的での更新](../database/dbmovement-scenario-general-refresh.md) のチュートリアルを使用します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-171">To complete this step, use the [Refresh for training purposes](../database/dbmovement-scenario-general-refresh.md) tutorial.</span></span>

### <a name="begin-the-upgrade"></a><span data-ttu-id="2aaf8-172">アップグレードの開始</span><span class="sxs-lookup"><span data-stu-id="2aaf8-172">Begin the upgrade</span></span>

<span data-ttu-id="2aaf8-173">サンドボックス環境で、**メンテナンス** メニューの **アップグレード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-173">In your sandbox environment, on the **Maintain** menu, select **Upgrade**.</span></span>

<img src="media/UpgradeAutomation/01_Select.png" width="700px" alt="Maintain menu" />

<span data-ttu-id="2aaf8-174">アプリケーション バージョンとプラットフォーム アップデートの最新の組み合わせを選択できるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-174">A dialog box appears, where you can select the latest combination of an application version and a platform update.</span></span>

<img src="media/UpgradeAutomation/02_Prepare.png" width="500px" alt="Prepare upgrade environment dialog box" />

> [!IMPORTANT]
> <span data-ttu-id="2aaf8-175">準備が失敗したことを示すエラーが発生した場合、このトピックの後半の[既知の問題](#known-issues)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-175">If you receive an error that states that preparation failed, see the [Known issues](#known-issues) section later in this topic.</span></span>

### <a name="preparation"></a><span data-ttu-id="2aaf8-176">準備</span><span class="sxs-lookup"><span data-stu-id="2aaf8-176">Preparation</span></span>

<span data-ttu-id="2aaf8-177">環境の詳細ページが更新され、2 つのサンドボックス環境のオプションが右上隅に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-177">The environment details page is refreshed, and options for two sandbox environments now appear in the upper-right corner.</span></span> <span data-ttu-id="2aaf8-178">オプションを選択することで、古いサンドボックス環境とアップグレード中の新しいサンドボックス環境の間で切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-178">By selecting the options, you can switch between your old sandbox environment and your new upgrade-in-progress sandbox environment.</span></span>

<img src="media/UpgradeAutomation/03_Provision.png" width="700px" alt="Old and Upgrade in progress options" />

<span data-ttu-id="2aaf8-179">フル環境配置に類似しているので、準備ステージには 8 時間以上かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-179">The preparation stage can take eight hours or longer, because it resembles a full environment deployment.</span></span> <span data-ttu-id="2aaf8-180">アップグレード中の環境は、展開を高速化するために空の Azure SQL データベースに接続され、配置対象として選択した新しいバージョンで実行されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-180">The upgrade-in-progress environment is connected to an empty Azure SQL database to speed up deployment, and it runs on the newer version that you selected to deploy.</span></span>

<span data-ttu-id="2aaf8-181">この間、元のサンドボックス環境はそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-181">During this time, your original sandbox environment is left untouched.</span></span> <span data-ttu-id="2aaf8-182">この段階では、ダウンタイムの影響はありません。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-182">There is no downtime impact at this stage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2aaf8-183">配置の失敗を示すエラーが発生した場合、Microsoft Dynamics サービス エンジニアリング (DSE) チームに通知が送信され、お客様の代わりに問題を事前に解決します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-183">If you receive an error that states that staging deployment failed, the Microsoft Dynamics Service Engineering (DSE) team will be notified and will proactively resolve the issue for you.</span></span> <span data-ttu-id="2aaf8-184">この問題は、Azure に、お客様の地域で使用できる必要なリソースがない場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-184">This issue can occur if Azure doesn't have the required resources available in your region.</span></span> <span data-ttu-id="2aaf8-185">Microsoft DSE は、より多くのリソースを割り当てるために Azure エンジニアと連携します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-185">Microsoft DSE will work with the Azure engineers to allocate more resources.</span></span> <span data-ttu-id="2aaf8-186">ステージング展開が正常に完了したら、電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-186">When staging deployment is successfully completed, you will receive an email.</span></span>

### <a name="package-application"></a><span data-ttu-id="2aaf8-187">パッケージ アプリケーション</span><span class="sxs-lookup"><span data-stu-id="2aaf8-187">Package application</span></span>

<span data-ttu-id="2aaf8-188">ステージング展開が完了したら、環境の詳細ページに戻り、**進行中のアップグレード** ビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-188">After staging deployment is completed, go back to the environment details page, and switch to the **Upgrade in progress** view.</span></span> <span data-ttu-id="2aaf8-189">このビューには、**アップグレード** メニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-189">In this view, you will now see an **Upgrade** menu.</span></span>

<span data-ttu-id="2aaf8-190">**アップグレード** メニューには、**更新プログラムの適用** オプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-190">The **Upgrade** menu includes an **Apply updates** option.</span></span> <span data-ttu-id="2aaf8-191">ソフトウェアの展開可能なパッケージを新しい環境に適用するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-191">You can select this option to apply your software deployable packages to the new environment.</span></span> <span data-ttu-id="2aaf8-192">これらのパッケージには、独立系ソフトウェア ベンダー (ISV) ソリューションによるパッケージ、独自のカスタマイズ パッケージ、プラットフォーム バイナリ更新プログラム パッケージのどれであるかに関係なく、任意のバイナリ パッケージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-192">These packages include any binary packages, whether whether they are from an independent software vendor (ISV) solution, your own customization packages, or platform binary update packages.</span></span>

<span data-ttu-id="2aaf8-193">最初の手順として、最新のプラットフォーム更新プログラムを適用することを **強くお勧めします**。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-193">**We highly recommend** that you apply the latest platform update as your first step.</span></span> <span data-ttu-id="2aaf8-194">バージョン 8.1 にアップグレードする場合は、8.1.3 など、最新のバイナリ アップデート パッケージを入手することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-194">If you're upgrading to version 8.1, we recommend that you get the latest binary update package, such as 8.1.3.</span></span> <span data-ttu-id="2aaf8-195">このパッケージはプラットフォームの最新の更新プログラムも含みます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-195">This package will also include the latest platform update.</span></span> <span data-ttu-id="2aaf8-196">このようにして、最新の修正プログラムが利用できることを保証し、プロセスの後半でエラーを減らすのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-196">In this way, you help guarantee that you have the latest hotfixes that are available and help reduce errors later in the process.</span></span>

<img src="media/UpgradeAutomation/06_ApplyUpdates.png" width="700px" alt="Apply updates option on the Upgrade menu" />

<span data-ttu-id="2aaf8-197">環境に新しいパッケージを適用する場合、プロセスは、定期的な環境保守のプロセスと同じになります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-197">When you apply a new package to the environment, the process is the same as the process for regular environment servicing.</span></span> <span data-ttu-id="2aaf8-198">パッケージ アプリケーションが完成したら、別のパッケージの適用に進む前に、そのパッケージの **サインオフ** ボタンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-198">When package application is completed, you must use the **Sign Off** button for that package before you can move on or apply another package.</span></span>

<span data-ttu-id="2aaf8-199">パッケージの展開が失敗した場合は、**ロールバック** ボタンを使用して取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-199">If package deployment fails, you can use the **Rollback** button to reverse it.</span></span> <span data-ttu-id="2aaf8-200">このボタンは、**アップグレード** メニューの **ロールバック** オプションとは同じでは**ない**ことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-200">Note that this button is **not** the same as the **Rollback** option on the **Upgrade** menu.</span></span>

### <a name="critical-hotfixes"></a><span data-ttu-id="2aaf8-201">重要な修正プログラム</span><span class="sxs-lookup"><span data-stu-id="2aaf8-201">Critical hotfixes</span></span>

<span data-ttu-id="2aaf8-202">セルフサービス アップグレード プロセスの使用が増加するにつれて、Microsoft はさまざまな対象バージョンの成功にはいくつかの修正プログラムが重大であることを確認しています。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-202">As use of the self-service upgrade process has increased, Microsoft has found that several hotfixes are critical to success for various target versions.</span></span> <span data-ttu-id="2aaf8-203">たとえば、バージョン 7.3 にアップグレードしている場合、データのアップグレード、Retail コンポーネント、またはパフォーマンスに関する問題を一貫して解決する Microsoft サポート技術情報 (KB) 記事の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-203">For example, if you're upgrading to version 7.3, a list of Microsoft Knowledge Base (KB) articles that have consistently resolved issues with data upgrade, Retail components, or performance will appear.</span></span>

<img src="media/UpgradeAutomation/Upgrade_CriticalKBs.png" width="700px" alt="Critical hotfixes" />

<span data-ttu-id="2aaf8-204">目標は、プロセスの **データ アップグレード** ステップを始める前に、この一覧が空である必要があることです。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-204">The goal is that this list should be empty before you begin the **Data Upgrade** step of the process.</span></span> <span data-ttu-id="2aaf8-205">これらのサポート技術情報の記事の修正プログラムは、アップグレードが進行中の環境にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-205">The hotfixes in these KB articles must be installed in your upgrade-in-progress environment.</span></span>

### <a name="data-upgrade-and-environment-swap"></a><span data-ttu-id="2aaf8-206">データ アップグレードと開発スワップ</span><span class="sxs-lookup"><span data-stu-id="2aaf8-206">Data upgrade and environment swap</span></span>

<span data-ttu-id="2aaf8-207">すべてのパッケージがアップグレード中のサンドボックス環境に適用され、それらをサインオフしたら、データ アップグレードを開始することができます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-207">After all packages are applied to your upgrade-in-progress sandbox environment, and you've signed off on them, you can begin the data upgrade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2aaf8-208">このステージにより、元のサンドボックス環境のダウンタイムが開始されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-208">This stage begins the downtime for your original sandbox environment.</span></span>

<span data-ttu-id="2aaf8-209">**アップグレード** メニューで、**データ アップグレード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-209">On the **Upgrade** menu, select **Data upgrade**.</span></span>

<img src="media/UpgradeAutomation/08_DataUpgrade.png" width="700px" alt="Data upgrade option on the Upgrade menu" />

<span data-ttu-id="2aaf8-210">元のサンドボックス環境がオフになり、新しい環境が元のデータベースに接続されるようにデータベース接続がスワップされます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-210">Your original sandbox environment is turned off, and the database connection is swapped so that your new environment is connected to the original database.</span></span> <span data-ttu-id="2aaf8-211">この処理は、最大 1 時間かかります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-211">This process can take up to one hour.</span></span>

<img src="media/UpgradeAutomation/09_Swap.png" width="500px" alt="Confirmation message about the environment swap" />

<span data-ttu-id="2aaf8-212">次に、対象バージョンのデータ アップグレード パッケージが自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-212">Next, the data upgrade package for your target version is automatically applied.</span></span> <span data-ttu-id="2aaf8-213">データ アップグレード パッケージを適用するために必要な時間は、データベースのサイズによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-213">The time that is required to apply the data upgrade package varies, depending on the size of your database.</span></span>

<span data-ttu-id="2aaf8-214">データのアップグレードが失敗した場合は、**アップグレード** メニューの **ロールバック** を選択して、データのアップグレードが開始される前の時点にデータベースを復元する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-214">If the data upgrade fails, you must select **Rollback** on the **Upgrade** menu to restore your database to the point that it was at before the data upgrade began.</span></span> <span data-ttu-id="2aaf8-215">ロールバックの実行前に、ログをダウンロードして失敗の根本原因を特定することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-215">Before you do a rollback, we highly recommend that you download the logs to determine the root cause of the failure.</span></span> <span data-ttu-id="2aaf8-216">これにより次回のデータ アップグレードの実行がより円滑に行われることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-216">In this way, you can help guarantee that your next data upgrade execution will go more smoothly.</span></span>

### <a name="upgrade-days-remaining"></a><span data-ttu-id="2aaf8-217">アップグレードの残り日数</span><span class="sxs-lookup"><span data-stu-id="2aaf8-217">Upgrade days remaining</span></span>

<span data-ttu-id="2aaf8-218">セルフサービスのアップグレード プロセスは追加費用なしで並列環境を提供するため、この環境を使用できる期間には時間制限があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-218">Because the self-service upgrade process provides a parallel environment at no additional cost to you, there is a time limit on how long this environment can be used.</span></span> <span data-ttu-id="2aaf8-219">現在、この時間制限は 10 カレンダー日に設定されており、プロセスを開始するために **管理** メニューで **アップグレード** を選択したときに開始します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-219">Currently, this time limit is set to 10 calendar days and begins when you select **Upgrade** on the **Maintain** menu to start the process.</span></span>

#### <a name="what-happens-when-the-time-limit-expires"></a><span data-ttu-id="2aaf8-220">制限を超過した場合。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-220">What happens when the time limit expires?</span></span>

<span data-ttu-id="2aaf8-221">タイマーが 0 (ゼロ) に達したとき考えられる結果は 3 つあります:</span><span class="sxs-lookup"><span data-stu-id="2aaf8-221">There are three possible outcomes when the timer reaches 0 (zero):</span></span>

<img src="media/UpgradeAutomation/Upgrade_Timer.png" width="300px" alt="Upgrade timer has reached 0 (zero) days" />

- <span data-ttu-id="2aaf8-222">**データのアップグレード** 手順をまだ開始していない場合、新しい環境はキューに入り削除されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-222">If you haven't yet started the **Data Upgrade** step, the new environment is queued for deletion.</span></span> <span data-ttu-id="2aaf8-223">このシナリオでは、アップグレード進行中の環境がプロビジョニングされ、カスタマイズとパッケージがオプションで適用されました。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-223">In this scenario, the upgrade-in-progress environment was provisioned, and customizations and packages were optionally applied.</span></span> <span data-ttu-id="2aaf8-224">ただし、データがアップグレードされておらず、元の環境でダウンタイムが発生しませんでした。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-224">However, no data was upgraded, and the original environment never incurred downtime.</span></span>
- <span data-ttu-id="2aaf8-225">**データ アップグレード** 手順を実行した後でロールバックした場合、新しい環境は削除のためにキューに入れられます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-225">If you ran the **Data Upgrade** step but then later performed a rollback, the new environment is queued for deletion.</span></span> <span data-ttu-id="2aaf8-226">このシナリオでは、データ アップグレードがロールバックされたため、古い環境が基本環境になります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-226">In this scenario, the old environment is the primary environment, because the data upgrade was rolled back.</span></span>
- <span data-ttu-id="2aaf8-227">**データ アップグレード** 手順を実行してもアップグレードをまだコミットしていない場合、アクションは実行されず、環境も削除されません。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-227">If you've run the **Data Upgrade** step but haven't yet committed the upgrade, no actions are performed, and no environments are deleted.</span></span> <span data-ttu-id="2aaf8-228">ロールバックをコミットまたは実行するまで、この状態のままにしておくことができます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-228">You can remain in this state until you commit or do a rollback.</span></span> <span data-ttu-id="2aaf8-229">ロールバックを行うことを決めてタイマーが 0 (ゼロ) の場合、新しい環境が削除されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-229">If you decide to do a rollback, and the timer is at 0 (zero), the new environment will be deleted.</span></span>

<span data-ttu-id="2aaf8-230">アップグレードを成功としてコミットした場合にのみ、元の環境はキューに入り削除されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-230">The original environment is queued for deletion only after you commit the upgrade as a success.</span></span>

### <a name="commit-or-roll-back"></a><span data-ttu-id="2aaf8-231">コミットまたはロールバック</span><span class="sxs-lookup"><span data-stu-id="2aaf8-231">Commit or roll back</span></span>

<span data-ttu-id="2aaf8-232">データ アップグレード パッケージが適用された後、環境を確認することができます。ユーザーは、ビジネス検証アクティビティを実行できます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-232">After the data upgrade package is applied, you can review the environment, and your users can perform business validation activities.</span></span> <span data-ttu-id="2aaf8-233">この検証に成功した場合は、**アップグレード** メニューで **コミット** を選択することにより、アップグレード全体を成功とマークできます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-233">If this validation is successful, you can mark the whole upgrade as a success by selecting **Commit** on the **Upgrade** menu.</span></span> <span data-ttu-id="2aaf8-234">実稼働環境に移行する前にアップグレードをコミットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-234">You must commit the upgrade before you can move on to your production environment.</span></span> <span data-ttu-id="2aaf8-235">アップグレードをコミットした後で、元の環境はキューに入り削除されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-235">After you commit the upgrade, the original environment is queued for deletion.</span></span>

<img src="media/UpgradeAutomation/10_CommitRollback.png" width="700px" alt="Commit option on the Upgrade menu" />

<span data-ttu-id="2aaf8-236">ビジネス検証が失敗すると、**アップグレード** メニューで **ロールバック** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-236">If the business validation fails, you can select **Rollback** on the **Upgrade** menu.</span></span> <span data-ttu-id="2aaf8-237">このオプションは、データベースのポイント イン タイムの復元を実行し、元のサンドボックス環境にデータベース接続を戻して、元のサンドボックス環境をオンラインに戻します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-237">This option will do a point-in-time restore of the database, swap the database connection back to your original sandbox environment, and bring your original sandbox environment back online.</span></span> <span data-ttu-id="2aaf8-238">その後、サンドボックス環境が元の状態になります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-238">The sandbox environment will then be back in its previous state.</span></span>

### <a name="post-upgrade-actions"></a><span data-ttu-id="2aaf8-239">アップグレード後のアクション</span><span class="sxs-lookup"><span data-stu-id="2aaf8-239">Post-upgrade actions</span></span>

<span data-ttu-id="2aaf8-240">アップグレードをサインオフした後で、集計の測定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-240">After you've signed off on your upgrade, you must update aggregate measurements.</span></span> <span data-ttu-id="2aaf8-241">メジャー アップグレードのたびに集約の測定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-241">Aggregate measurements must be updated after every major upgrade.</span></span> <span data-ttu-id="2aaf8-242">それらを更新するには **システム管理** \> **設定** \> **エンティティ格納** に移動して、そして **更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-242">To update them, go to **System Administration** \> **Setup** \> **Entity Store**, and then select **Refresh**.</span></span>

> [!NOTE]
> <span data-ttu-id="2aaf8-243">バッチ処理を使用して、この更新プログラムを実行するようにスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-243">You can schedule this update to run by using batch processing.</span></span>

### <a name="upgrade-production"></a><span data-ttu-id="2aaf8-244">実稼動環境のアップグレード</span><span class="sxs-lookup"><span data-stu-id="2aaf8-244">Upgrade production</span></span>

<span data-ttu-id="2aaf8-245">サンドボックス UAT 環境でアップグレードをコミットした後、サンドボックス環境でアップグレード プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-245">After you've committed the upgrade in the sandbox UAT environment, you've finished the upgrade process in the sandbox environment.</span></span> <span data-ttu-id="2aaf8-246">実稼働環境で、同じプロセスを開始できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-246">You can now begin the same process in your production environment.</span></span> <span data-ttu-id="2aaf8-247">実行する手順は同じです。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-247">The steps that you follow are the same.</span></span>

<span data-ttu-id="2aaf8-248">実稼働環境のアップグレード時に非常に長いダウンタイムを引き起こす問題が発生した場合、[実稼働環境の停止の報告](https://docs.microsoft.com/business-applications-release-notes/April18/dynamics365-finance-operations/report-production-outage)プロセスを使用して、Microsoft に知らせてサポートを受けます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-248">If you encounter an issue that causes excessive downtime during your production upgrade, use the [Report production outage](https://docs.microsoft.com/business-applications-release-notes/April18/dynamics365-finance-operations/report-production-outage) process to alert Microsoft and get help.</span></span>

### <a name="upgrade-additional-environments"></a><span data-ttu-id="2aaf8-249">追加の環境のアップグレード</span><span class="sxs-lookup"><span data-stu-id="2aaf8-249">Upgrade additional environments</span></span>

<span data-ttu-id="2aaf8-250">同じ方法で追加のサンドボックス環境をアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-250">You can upgrade additional sandbox environments in the same way.</span></span> <span data-ttu-id="2aaf8-251">その他のサンドボックス環境の割り当てを解除して削除し、新しいバージョンで再展開できます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-251">You also can deallocate and delete your other sandbox environments, and then redeploy on the newer version.</span></span> <span data-ttu-id="2aaf8-252">[データベースの更新](../database/database-refresh.md)セルフサービス アクションを使用することで、別のサンドボックスまたは実稼働環境からアップグレードするデータベースにコピーできます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-252">By using the [Database Refresh](../database/database-refresh.md) self-service action, you can copy in the upgraded database from another sandbox or production environment.</span></span>

### <a name="known-issues"></a><span data-ttu-id="2aaf8-253">既知の問題</span><span class="sxs-lookup"><span data-stu-id="2aaf8-253">Known issues</span></span>

<span data-ttu-id="2aaf8-254">**準備操作を開始できませんでした。Microsoft サポートに通知されました。問題が解消しない場合は、次の ID でサポートにお問い合わせください。**</span><span class="sxs-lookup"><span data-stu-id="2aaf8-254">**Prepare operation could not start. Microsoft support has been notified. If the issue persists, please contact support with this ID.**</span></span>

<span data-ttu-id="2aaf8-255">この既知の問題には Microsoft Dynamics Lifecycle Services (LCS) バック エンドの環境証明書が関係しています。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-255">This known issue involves environment certificates on the Microsoft Dynamics Lifecycle Services (LCS) back end.</span></span> <span data-ttu-id="2aaf8-256">この影響を受けた場合、サポート チケットを送信し、エラー メッセージに表示されたアクティビティ ID を含めます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-256">If it affects you, submit a support ticket, and include the activity ID from the error message.</span></span> <span data-ttu-id="2aaf8-257">Microsoft が問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-257">Microsoft will work to resolve the issue.</span></span> <span data-ttu-id="2aaf8-258">Microsoft は影響される環境の一覧を編集しており、今後はこの問題を積極的に解決しようとしています。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-258">Microsoft is compiling a list of affected environments and intends to proactively fix this issue in the future.</span></span>

<span data-ttu-id="2aaf8-259">**アップグレードをキャンセルしてからもう一度やり直したいと思っています。**</span><span class="sxs-lookup"><span data-stu-id="2aaf8-259">**I want to cancel the upgrade and try again later.**</span></span>

<span data-ttu-id="2aaf8-260">アップグレードをキャンセルするには、**メンテナンス** メニューの **アップグレードのキャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-260">To cancel an upgrade, you can select **Cancel Upgrade** on the **Maintain** menu.</span></span> <span data-ttu-id="2aaf8-261">**メンテナンス** メニューは、**アップグレードを実行中です** ビュー (新しいサンドボックス環境) ではなく、**古い** ビュー (元のサンドボックス環境) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-261">The **Maintain** menu is available in the **Old** view (for the original sandbox environment), not in the **Upgrade in progress** view (for the new sandbox environment).</span></span>

<span data-ttu-id="2aaf8-262">**手順 X でアップグレードが失敗しました: サービス モデルの DVT スクリプト: MRProcessServiceします。**</span><span class="sxs-lookup"><span data-stu-id="2aaf8-262">**Upgrade failed at step X: DVT script for service model: MRProcessService.**</span></span>

<span data-ttu-id="2aaf8-263">この DVT エラーは断続的であり、データ アップグレード パッケージの **再開** ボタンを使用して解決できます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-263">This DVT error is intermittent and can be resolved by using the **Resume** button for your data upgrade package.</span></span> <span data-ttu-id="2aaf8-264">**再開** を選択すると、同じ段階でプロセスが再開されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-264">When you select **Resume**, the process resumes at the same step.</span></span> <span data-ttu-id="2aaf8-265">Microsoft では、この問題を確実に再現しようとしており、今後修正プログラムを作成する予定です。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-265">Microsoft is trying to reliably reproduce this issue and intends to produce a fix in the future.</span></span>

<span data-ttu-id="2aaf8-266">**アプリケーション構成の同期に失敗しました。最初に TTSBEGIN を呼び出さずに TTSCOMMIT の呼び出してください。**</span><span class="sxs-lookup"><span data-stu-id="2aaf8-266">**Application configuration sync failed. Call to TTSCOMMIT without first calling TTSBEGIN.**</span></span>

<span data-ttu-id="2aaf8-267">この TTSCOMMIT エラーは断続的であり、データ アップグレード パッケージの **再開** ボタンを使用して解決できます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-267">This TTSCOMMIT error is intermittent and can be resolved by using the **Resume** button for your data upgrade package.</span></span> <span data-ttu-id="2aaf8-268">**再開** を選択すると、同じ段階でプロセスが再開されます。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-268">When you select **Resume**, the process resumes at the same step.</span></span> <span data-ttu-id="2aaf8-269">(この問題は PU 21 で修正されます。)</span><span class="sxs-lookup"><span data-stu-id="2aaf8-269">(This issue is fixed in PU 21.)</span></span>

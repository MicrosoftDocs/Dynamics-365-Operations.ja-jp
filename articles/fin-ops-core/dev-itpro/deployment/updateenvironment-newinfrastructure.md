---
title: 環境の更新
description: このトピックでは、セルフ サービス配置エクスペリエンスを使用して配置された環境を、更新する方法について説明します。
author: laneswenka
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: c64d30375cee7e0367975aa8c53efad129b2cea6
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096847"
---
# <a name="update-an-environment"></a><span data-ttu-id="cb70c-103">環境の更新</span><span class="sxs-lookup"><span data-stu-id="cb70c-103">Update an environment</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="cb70c-104">このトピックでは、[セルフサービス配置](infrastructure-stack.md) エクスペリエンスを使用して配置した環境に、更新を適用するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-104">This topic walks through the process of applying updates to an environment that was deployed by using the [self-service deployment](infrastructure-stack.md) experience.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb70c-105">次世代のインフラストラクチャでは、現在のフローで適用されるものとは異なる方法で更新が適用されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-105">In the next-generation infrastructure, updates are applied differently than they are applied in the current flow.</span></span> <span data-ttu-id="cb70c-106">*パッケージに含まれているものはすべて環境に適用され、既に環境に存在するものはすべて**上書き**されます。*</span><span class="sxs-lookup"><span data-stu-id="cb70c-106">*Whatever is provided in the package is applied to the environment, and it **overwrites** whatever is already present in that environment.*</span></span> <span data-ttu-id="cb70c-107">つまり、ビルド環境からのすべてのカスタマイズおよび独立系ソフトウェア ベンダー (ISV) ソリューションを含む 1 つの配置可能パッケージを作成する**必要があります**。</span><span class="sxs-lookup"><span data-stu-id="cb70c-107">Therefore, you **must** create a single deployable package that contains all customizations and independent software vendor (ISV) solutions from your build environment.</span></span> <span data-ttu-id="cb70c-108">環境内のモデルの一覧がパッケージ内のモデルの一覧と異なる場合は、更新が適用される前に警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-108">If the list of models in the environment differs from the list of models in in the package, you receive a warning before the update is applied.</span></span> <span data-ttu-id="cb70c-109">単一のパッケージを作成する方法については、[ソース コントロールを使用することでサード パーティ モデルとランタイム パッケージを管理する](../dev-tools/manage-runtime-packages.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb70c-109">For information about how to create a single package, see [Manage third-party models and runtime packages by using source control](../dev-tools/manage-runtime-packages.md).</span></span>

## <a name="supported-package-types"></a><span data-ttu-id="cb70c-110">サポートされているパッケージの種類</span><span class="sxs-lookup"><span data-stu-id="cb70c-110">Supported package types</span></span>

<span data-ttu-id="cb70c-111">[セルフサービス配置](infrastructure-stack.md) エクスペリエンスを使用して配置される環境は、バージョン8.1 (2018 年 10 月) 以降のバージョンで実行されるため、次のパッケージ タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-111">Because environments that are deployed by using the [self-service deployment](infrastructure-stack.md) experience will be running on version 8.1 (October 2018) or a later version, the following package types are supported:</span></span>

- <span data-ttu-id="cb70c-112">**AOT の配置可能パッケージ** - アプリケーション メタデータおよびソース コードから生成される配置可能なパッケージ。</span><span class="sxs-lookup"><span data-stu-id="cb70c-112">**AOT deployable package** – A deployable package that is generated from application metadata and source code.</span></span> <span data-ttu-id="cb70c-113">このタイプの展開可能なパッケージは、**ビルド**環境で作成されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-113">This type of deployable package is created in a **build** environment.</span></span>
- <span data-ttu-id="cb70c-114">**バイナリ更新プログラム パッケージ** - ダイナミック リンク ライブラリ (DLL) と、プラットフォームとアプリケーションが依存するその他のバイナリとメタデータを含む配置可能パッケージ。</span><span class="sxs-lookup"><span data-stu-id="cb70c-114">**Binary update package** – A deployable package that contains dynamic-link libraries (DLLs), and other binaries and metadata that the platform and application depend on.</span></span> <span data-ttu-id="cb70c-115">このタイプのパッケージは、Microsoft によってリリースされています。</span><span class="sxs-lookup"><span data-stu-id="cb70c-115">This type of package is released by Microsoft.</span></span>

## <a name="development-application-lifecycle-management-alm-flow"></a><span data-ttu-id="cb70c-116">開発アプリケーション ライフ サイクル管理 (ALM) フロー</span><span class="sxs-lookup"><span data-stu-id="cb70c-116">Development Application Lifecycle Management (ALM) flow</span></span>

<span data-ttu-id="cb70c-117">コード カスタマイズをサンドボックスおよび製造環境に適用するには、ビルド環境から配置可能なコード パッケージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb70c-117">To apply code customizations to your sandbox and production environments, you must create a deployable code package from your build environment.</span></span> <span data-ttu-id="cb70c-118">詳細については、[配置可能パッケージの作成](create-apply-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb70c-118">For more information, see [Create deployable packages of models](create-apply-deployable-package.md).</span></span>

## <a name="microsoft-updates"></a><span data-ttu-id="cb70c-119">Microsoft の更新プログラム</span><span class="sxs-lookup"><span data-stu-id="cb70c-119">Microsoft updates</span></span>

<span data-ttu-id="cb70c-120">Microsoft の更新プログラムへのアクセスを取得するには、 Microsoft Dynamics Lifecycle Services (LCS) 環境の環境詳細ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-120">To access Microsoft updates, go to the environment details page for your environment in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="cb70c-121">すべてのアプリケーションとプラットフォーム修正の累積的なバイナリ更新を示す **1 つのタイル** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-121">You will see a **single tile** that shows a cumulative binary update of all the application and platform fixes.</span></span> <span data-ttu-id="cb70c-122">この更新プログラムを適用するには、パッケージを選択して、 **パッケージの保存** を選択し、プロジェクト アセット ライブラリに Microsoft の更新プログラムを保存します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-122">To apply this update, select the package, and then select **Save Package** to save the Microsoft update to the project asset library.</span></span>

## <a name="apply-updates"></a><span data-ttu-id="cb70c-123">更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="cb70c-123">Apply updates</span></span>

### <a name="tier-1-sandboxdevelop-and-testdemobuild-environments"></a><span data-ttu-id="cb70c-124">レベル 1 サンドボックス/開発およびテスト/デモ/ビルド環境</span><span class="sxs-lookup"><span data-stu-id="cb70c-124">Tier 1 sandbox/develop and test/demo/build environments</span></span>

<span data-ttu-id="cb70c-125">Lifecycle Services (LCS) を通じて配置されたレベル 1 サンドボックス/開発およびテスト/デモ/ビルド環境に更新を適用するには、[クラウド環境に更新を適用する](apply-deployable-package-system.md)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cb70c-125">To apply updates to a Tier 1 sandbox/develop and test/demo/build environment that was deployed through LCS, follow the steps in [Apply updates to cloud environments](apply-deployable-package-system.md).</span></span>

### <a name="tier-2-and-above-standard-acceptance-testsandbox-environments"></a><span data-ttu-id="cb70c-126">レベル 2 以上のスタンダード承認テスト/サンドボックス環境</span><span class="sxs-lookup"><span data-stu-id="cb70c-126">Tier 2 and above Standard Acceptance Test/sandbox environments</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb70c-127">パッケージ アプリケーションは、システムのダウンタイムを引き起こします。</span><span class="sxs-lookup"><span data-stu-id="cb70c-127">Package application causes system downtime.</span></span> <span data-ttu-id="cb70c-128">すべて関連するサービスを停止、およびパッケージを適用中のときには環境を使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="cb70c-128">All relevant services will be stopped, and you won't be able to use your environments while the package is being applied.</span></span>

<span data-ttu-id="cb70c-129">開始する前に、配置可能パッケージが LCS のプロジェクト アセット ライブラリにアップロードされており、検証が成功したことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="cb70c-129">Before you begin, verify that the deployable package has been uploaded to the project asset library in LCS, and that validations have succeeded.</span></span>

<span data-ttu-id="cb70c-130">パッケージが、プロジェクト アセット ライブラリに入ったら、以下の手順に従って、環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-130">After the package is in the project asset library, follow these steps to update your environment.</span></span>

1. <span data-ttu-id="cb70c-131">パッケージを適用する環境の環境の詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-131">Open the environment details page for the environment where you want to apply the package.</span></span>
2. <span data-ttu-id="cb70c-132">**メンテナンス \> 更新プログラムの適用**を選択し、更新プログラムを適用します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-132">Select **Maintain \> Apply updates** to apply an update.</span></span>
3. <span data-ttu-id="cb70c-133">更新プログラムに対して**一意の名前**を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-133">Enter a **unique name** for the update.</span></span> <span data-ttu-id="cb70c-134">この名前は、実稼働環境に移動する更新を識別するために使用します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-134">You will use this name to identify the update that you want to move to the production environment.</span></span>
4. <span data-ttu-id="cb70c-135">パッケージを選択して適用します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-135">Select the package to apply.</span></span> <span data-ttu-id="cb70c-136">上部にあるフィルターを使用してパッケージを探します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-136">Use the filter at the top to find your package.</span></span> <span data-ttu-id="cb70c-137">このリストには、アセット ライブラリから検証に合格したアプリケーションおよびプラットフォーム バイナリ パッケージと、アプリケーション配置可能パッケージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-137">The list will include application and platform binary packages and application deployable packages that have passed validation from the asset library.</span></span>
5. <span data-ttu-id="cb70c-138">**適用**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-138">Select **Apply**.</span></span>

    <span data-ttu-id="cb70c-139">環境詳細ページの右上隅にあるステータスが、 **キュー** から **サービス** に変わります。</span><span class="sxs-lookup"><span data-stu-id="cb70c-139">The status in the upper-right corner of the environment details page changes from **Queued** to **Servicing**.</span></span> <span data-ttu-id="cb70c-140">その後、パッケージ アプリケーションが完了すると、ステータスが **配置済み** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-140">Then, when package application is completed, the status changes to **Deployed**.</span></span>

6. <span data-ttu-id="cb70c-141">パッケージ アプリケーションが完了すると、環境履歴が更新されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-141">After package application is completed, the environment history is updated.</span></span> <span data-ttu-id="cb70c-142">環境履歴を表示するには、環境の詳細ページで **履歴 \> 環境の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-142">To view the environment history, select **History \> Environment changes** on the environment details page.</span></span>
7. <span data-ttu-id="cb70c-143">環境履歴ページからログをダウンロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-143">You can also download the logs from the environment history page.</span></span>
8. <span data-ttu-id="cb70c-144">検証が完了すると、 **サインオフ** または **払出サイン オフ** のいずれかを選択して、環境の履歴ページから更新プログラムをサインオフできます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-144">After the validations are completed, you can sign-off on the update from the environment history page by selecting either **Sign off** or **Sign off with issues**.</span></span>

### <a name="production-environment"></a><span data-ttu-id="cb70c-145">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="cb70c-145">Production environment</span></span>

<span data-ttu-id="cb70c-146">運用環境に適用される更新プログラムの信頼性を向上させるために、サンドボックス環境で実行される特定の更新プログラムを**リリース候補**として指定 ("マーク") し、実稼働環境に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-146">To improve the reliability of updates that are applied to a production environment, a specific update that is done in the sandbox environment is designated ("marked") as a **release candidate** and moved to the production environment.</span></span> <span data-ttu-id="cb70c-147">この更新プログラムには、基本製品とカスタマイズの両方が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb70c-147">This update contains both the base product and the customization.</span></span> <span data-ttu-id="cb70c-148">したがって、選択した更新プログラムを実稼働環境に適用したときに、両方が移動します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-148">Therefore, both will be moved over when the selected update is applied to the production environment.</span></span> <span data-ttu-id="cb70c-149">この動作は現在のサービスとは異なります。</span><span class="sxs-lookup"><span data-stu-id="cb70c-149">This behavior differs from the current servicing behavior.</span></span> <span data-ttu-id="cb70c-150">現時点では、カスタマイズのみを移動できますが、基本製品は変更 **されません** 。</span><span class="sxs-lookup"><span data-stu-id="cb70c-150">Currently, you can move only the customization, but the base product **will not** change.</span></span> <span data-ttu-id="cb70c-151">セルフサービス配置環境では、サンドボックス環境でリリース候補としてマークされている更新によって、基本製品バージョンが**変わる場合があります**。</span><span class="sxs-lookup"><span data-stu-id="cb70c-151">In the case of a self-service deployment environment, the base product version **might change**, depending on the update that is marked as a release candidate in the sandbox environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb70c-152">パッケージ アプリケーションは、システムのダウンタイムを引き起こします。</span><span class="sxs-lookup"><span data-stu-id="cb70c-152">Package application causes system downtime.</span></span> <span data-ttu-id="cb70c-153">すべて関連するサービスを停止、およびパッケージを適用中のときには環境を使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="cb70c-153">All relevant services will be stopped, and you won't be able to use your environments while the package is being applied.</span></span>

<span data-ttu-id="cb70c-154">サンドボックス環境での更新プログラムの適用が成功し、更新プログラムを実稼働環境に移行する準備ができたら、次の手順に従って、更新をリリース候補としてマークします。</span><span class="sxs-lookup"><span data-stu-id="cb70c-154">After you've successfully applied the update in the sandbox environment and are ready to move the update over to the production environment, follow these steps to mark an update as a release candidate.</span></span>

1. <span data-ttu-id="cb70c-155">環境履歴ページを開くには、環境の詳細ページで **履歴 \> 環境の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-155">Open the environment history page by selecting **History \> Environment changes** on the environment details page.</span></span>
2. <span data-ttu-id="cb70c-156">実稼働環境に移動するため更新プログラムを選択します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-156">Select the update to move over to the production environment.</span></span>
3. <span data-ttu-id="cb70c-157">更新プログラムの詳細で、 **リリース候補としてマーク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-157">In the details for the update, select **Mark as release candidate**.</span></span>

    <span data-ttu-id="cb70c-158">**リリース候補** オプションが **はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="cb70c-158">The **Is Release Candidate** option is set to **Yes**.</span></span>

<span data-ttu-id="cb70c-159">更新プログラムをリリース候補としてマークしたら、次の手順に従って環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-159">After you've marked an update as a release candidate, follow these steps to update your environment.</span></span>

1. <span data-ttu-id="cb70c-160">実稼働環境の環境の詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-160">Open the environment details page for the production environment.</span></span>
2. <span data-ttu-id="cb70c-161">**メンテナンス \> 更新プログラムの環境**を選択し、更新プログラムを適用します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-161">Select **Maintain \> Update environment** to apply an update.</span></span>
3. <span data-ttu-id="cb70c-162">**使用可能なサンドボックス**の一覧で、更新プログラムが適用され、検証されて、リリース候補としてマークされているソースサンドボックス環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-162">In the **Available sandboxes** list, select the source sandbox environment where the update was applied, validated, and marked as a release candidate.</span></span>
4. <span data-ttu-id="cb70c-163">グリッドで、実稼働環境に適用する更新プログラムを選択します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-163">In the grid, select the update to apply to the production environment.</span></span> <span data-ttu-id="cb70c-164">このグリッドには、リリース候補としてマークされている更新プログラムのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-164">This grid shows only updates that have been marked as release candidates.</span></span>
5. <span data-ttu-id="cb70c-165">**ダウンタイム開始** フィールドで、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-165">In the **Downtime start** field, select a date and time.</span></span> <span data-ttu-id="cb70c-166">環境は、指定された日の指定された時間に停止されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-166">The environment will be taken down for servicing at the specified time on the specified date.</span></span> <span data-ttu-id="cb70c-167">**ダウンタイムの終了** フィールドは、ダウンタイムの開始から数時間に設定されています。</span><span class="sxs-lookup"><span data-stu-id="cb70c-167">The **Downtime end** field is set to through hours from the start of the downtime.</span></span>

    <span data-ttu-id="cb70c-168">この更新プログラムにはリードタイムは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="cb70c-168">No lead time is required for this update.</span></span>

6. <span data-ttu-id="cb70c-169">**スケジュール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-169">Select **Schedule**.</span></span> <span data-ttu-id="cb70c-170">LCSは、選択された更新プログラムが環境に適用可能であることを確認する検証を実行します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-170">LCS runs validations to make sure that the selected update is applicable to the environment.</span></span> <span data-ttu-id="cb70c-171">環境のダウングレードを回避するために、更新プログラムは、そのアプリケーションのバージョンが現在の環境のバージョンよりも低い場合は許可されません。</span><span class="sxs-lookup"><span data-stu-id="cb70c-171">To prevent downgrade of the environment, the update isn't allowed if its application version is lower than the current environment version.</span></span> <span data-ttu-id="cb70c-172">また、更新プログラムを続行するかどうかを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-172">Additionally, customers are asked to confirm that they want the update to proceed.</span></span>

    <span data-ttu-id="cb70c-173">更新プログラムが**正常に**スケジュールされると、すべてのプロジェクト関係者に電子メール通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-173">If the update is **successfully** scheduled, an email notification is sent to all project stakeholders.</span></span>

    <span data-ttu-id="cb70c-174">環境詳細ページの右上隅にあるステータスが、 **キュー** から **サービス** に変わります。</span><span class="sxs-lookup"><span data-stu-id="cb70c-174">The status in the upper-right corner of the environment details page changes from **Queued** to **Servicing**.</span></span> <span data-ttu-id="cb70c-175">その後、更新プログラムが完了すると、ステータスが **配置済み** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-175">Then, when the update is completed, the status changes to **Deployed**.</span></span>

    <span data-ttu-id="cb70c-176">すべての関係者に、工程の進捗状況が通知されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-176">All stakeholders are notified of the progress of the operation.</span></span>

7. <span data-ttu-id="cb70c-177">更新プログラムが完了すると、環境履歴が更新されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-177">After the update is completed, the environment history is updated.</span></span> <span data-ttu-id="cb70c-178">環境履歴を表示するには、環境の詳細ページで **履歴 \> 環境の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb70c-178">To view the environment history, select **History \> Environment changes** on the environment details page.</span></span>
8. <span data-ttu-id="cb70c-179">環境履歴ページからログをダウンロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-179">You can also download the logs from the environment history page.</span></span>
9. <span data-ttu-id="cb70c-180">検証が完了すると、 **サインオフ** または **払出サイン オフ** のいずれかを選択して、環境の履歴ページから更新プログラムをサインオフできます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-180">After the validations are completed, you can sign-off on the update from the environment history page by selecting either **Sign off** or **Sign off with issues**.</span></span>

> [!NOTE]
> <span data-ttu-id="cb70c-181">環境内で進行中の操作がある場合、または環境が同じバージョンまたはそれ以降のバージョンで既に実行されている場合、スケジュールされた更新は取り消されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-181">If there is an on-going operation in the environment, or if the environment is already running on the same version or a later version, the scheduled update is canceled.</span></span> <span data-ttu-id="cb70c-182">予定された更新プログラムがキャンセルされると、すべてのプロジェクト関係者に電子メール通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-182">When a scheduled update is canceled, an email notification is sent to all project stakeholders.</span></span> <span data-ttu-id="cb70c-183">また、環境の詳細 ページで **キャンセル** を選択することにより、更新プログラムを取り消すこともできます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-183">Customers can also cancel an update by selecting **Cancel** on the environment details page.</span></span> <span data-ttu-id="cb70c-184">顧客が更新を再スケジューリングしたり変更したりする場合は、現在の工程をキャンセルして、新しい更新をスケジュールすることができます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-184">If customers want to reschedule or change an update, they can cancel the current operation and schedule a new one.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb70c-185">最新のインフラストラクチャ スタックに配置されている環境では、サービスが失敗した場合、その環境は自動的にロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-185">For environments that are deployed in the modern infrastructure stack, if servicing is unsuccessful, the environment is automatically rolled back.</span></span> <span data-ttu-id="cb70c-186">工程が失敗した理由については、環境履歴ページからログをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="cb70c-186">To learn why the operation was unsuccessful, you can download the logs from the environment history page.</span></span>

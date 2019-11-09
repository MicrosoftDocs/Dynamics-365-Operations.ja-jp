---
title: 他のコンポーネントの ER コンフィギュレーションの依存関係の定義
description: これらの手順を完了するには、最初にタスク ガイドでの手順を実行し、ER モデル マッピング コンフィギュレーションを管理し、および Microsoft Dynamics Lifecycle Services (LCS) にアクセスする必要があります。
author: NickSelin
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d949be57d9e9fe744860f5c4045bef2923b7f284
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249184"
---
# <a name="define-the-dependency-of-er-configurations-on-other-components"></a><span data-ttu-id="22edf-103">他のコンポーネントの ER コンフィギュレーションの依存関係の定義</span><span class="sxs-lookup"><span data-stu-id="22edf-103">Define the dependency of ER configurations on other components</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22edf-104">これらの手順を完了するには、最初にタスク ガイドでの手順を実行し、ER モデル マッピング コンフィギュレーションを管理し、および Microsoft Dynamics Lifecycle Services (LCS) にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="22edf-104">To complete these steps, you must first complete the steps in the task guide, ER Manage model mapping configurations, and you must have access to Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="22edf-105">この手順は、電子申告 (ER) コンフィギュレーションをどのように設計し、および他のソフトウェア コンポーネントからその依存関係を指定する方法を説明します。それによりコンフィギュレーションが Finance and Operations の特定のバージョンに正しくダウンロードされるのを保証できるようにします。</span><span class="sxs-lookup"><span data-stu-id="22edf-105">This procedure shows how to design an Electronic reporting (ER) configuration and specify its dependency from other software components, so that you can help guarantee that the configuration is correctly downloaded to a specific version of Finance and Operations.</span></span> <span data-ttu-id="22edf-106">この例では、サンプル会社 Litware, Inc. に必要な ER コンフィギュレーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="22edf-106">In this example, you will create required ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="22edf-107">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="22edf-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="22edf-108">ER コンフィギュレーションは会社間で共有されるため、手順はすべての会社で実行されます。</span><span class="sxs-lookup"><span data-stu-id="22edf-108">The steps can be performed in any company, because ER configurations are shared among companies.</span></span> 

1. <span data-ttu-id="22edf-109">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="22edf-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
    * <span data-ttu-id="22edf-110">コンフィギュレーション ツリーに「サンプルのデータ モデル」コンフィギュレーションと下位項目が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="22edf-110">Make sure that the configurations tree contains the ‘Sample data model’ configuration and subordinate items.</span></span> <span data-ttu-id="22edf-111">含まれていない場合は、タスク ガイド「ER モデル マッピングの構成を管理する」内のステップを完了してから、このガイドを再度開始します。</span><span class="sxs-lookup"><span data-stu-id="22edf-111">Otherwise, complete the steps in the task guide, ER Manage model mapping configurations, and then start this guide again.</span></span>   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a><span data-ttu-id="22edf-112">他のコンポーネントの ER コンフィギュレーションの依存関係を定義する</span><span class="sxs-lookup"><span data-stu-id="22edf-112">Define the dependency of ER configurations from other components</span></span>
1. <span data-ttu-id="22edf-113">ツリーで、「サンプル データ モデル」を展開します。</span><span class="sxs-lookup"><span data-stu-id="22edf-113">In the tree, expand 'Sample data model'.</span></span>
2. <span data-ttu-id="22edf-114">ツリーで、「サンプル データ モデル\サンプル マッピング」を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-114">In the tree, select 'Sample data model\Sample mapping'.</span></span>
    * <span data-ttu-id="22edf-115">「サンプル マッピング」のモデル マッピング コンフィギュレーションのドラフト バージョンを選択してあります。</span><span class="sxs-lookup"><span data-stu-id="22edf-115">We selected the draft version of the ‘Sample mapping’ model mapping configuration.</span></span> <span data-ttu-id="22edf-116">他のソフトウェア コンポーネントからその依存関係を定義していきます。</span><span class="sxs-lookup"><span data-stu-id="22edf-116">We will now define its dependency from other software components.</span></span> <span data-ttu-id="22edf-117">このステップは、ER リポジトリからのこのコンフィギュレーションのバージョンのダウンロード制御、およびこのバージョンのさらなる使用の前提条件とみなされます。</span><span class="sxs-lookup"><span data-stu-id="22edf-117">This step is considered a prerequisite for controlling the download of this configuration’s version from an ER repository and any further use of this version.</span></span>   
3. <span data-ttu-id="22edf-118">[前提条件] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="22edf-118">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="22edf-119">このステージで、「実装」前提条件グループが自動的に追加されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="22edf-119">Note that the ‘Implementations’ prerequisites group has been added automatically at this stage.</span></span> <span data-ttu-id="22edf-120">このグループには、データ モデル コンフィギュレーションを参照し「実装」フラグがオンになっている、前提条件コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="22edf-120">This group contains the prerequisite component that refers to the data model configuration and has the Implementation flag turned on.</span></span> <span data-ttu-id="22edf-121">このフラグは、「サンプル マッピング」マッピング コンフィギュレーションが、「サンプル データ モデル」データ モデルの実装とみなされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="22edf-121">This flag indicates that the ‘Sample mapping’ mapping configuration is considered the implementation of the ‘Sample data model’ data model.</span></span> <span data-ttu-id="22edf-122">「サンプル データ モデル」モデル コンフィギュレーションがダウンロードされるときは常に、このコンポーネントは強制的に ER に ER リポジトリから「サンプル マッピング」マッピング コンフィギュレーションをダウンロードさせます。</span><span class="sxs-lookup"><span data-stu-id="22edf-122">This component will force ER to download the ‘Sample mapping’ mapping configuration from an ER repository whenever the ‘Sample data model’ model configuration is downloaded.</span></span>   
4. <span data-ttu-id="22edf-123">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-123">Click Edit.</span></span>
    * <span data-ttu-id="22edf-124">ソフトウェア コンポーネントからのコンフィギュレーションの現バージョンの単一の依存関係は、コンポーネントのタイプの定義、およびコンポーネント バージョンまたはコンポーネント バージョンの範囲のいずれかを使用して指定できます。</span><span class="sxs-lookup"><span data-stu-id="22edf-124">A single dependency of the current version of a configuration from a software component can be specified by using the definition of the component’s type, and either the component version or a range of component versions.</span></span>  
    * <span data-ttu-id="22edf-125">必要な依存関係はグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="22edf-125">Desired dependencies can be grouped together.</span></span> <span data-ttu-id="22edf-126">「すべて」というグループ タイプが選択されている場合、このグループと下位グループからの各依存条件が満たされると、このグループの依存関係条件が満たされたとみなされます。</span><span class="sxs-lookup"><span data-stu-id="22edf-126">When the ‘All of’ grouping type is selected, the dependency condition of this group is considered satisfied when each dependency condition from this group and subordinate group is satisfied.</span></span> <span data-ttu-id="22edf-127">「いずれか」というグループ タイプが選択されている場合、このグループからの少なくとも 1 つの依存条件が満たされると、このグループの依存関係条件が満たされたとみなされます。</span><span class="sxs-lookup"><span data-stu-id="22edf-127">When the ‘One of’ grouping type is selected, the dependency condition of this group is considered satisfied when at least one dependency condition from this group is satisfied.</span></span>   
5. <span data-ttu-id="22edf-128">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-128">Click New.</span></span>
6. <span data-ttu-id="22edf-129">[製品の前提条件コンポーネント] を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-129">Select Product prerequisite component.</span></span>
7. <span data-ttu-id="22edf-130">Microsoft Dynamics 365 for Operations (1611) を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-130">Select Microsoft Dynamics 365 for Operations (1611).</span></span>
8. <span data-ttu-id="22edf-131">[バージョン] フィールドで、「[7.1.1541.3036,8]」を入力します。</span><span class="sxs-lookup"><span data-stu-id="22edf-131">In the Version field, type '[7.1.1541.3036,8)'.</span></span>
    * <span data-ttu-id="22edf-132">[7.1.1541.3036,8]</span><span class="sxs-lookup"><span data-stu-id="22edf-132">[7.1.1541.3036,8)</span></span>  
    * <span data-ttu-id="22edf-133">入力した依存関係は、このコンフィギュレーションが ER リポジトリからダウンロードされるときに評価されます。</span><span class="sxs-lookup"><span data-stu-id="22edf-133">Dependencies that you enter will be evaluated when this configuration is downloaded from any ER repository.</span></span> <span data-ttu-id="22edf-134">このコンフィギュレーション バージョンは、「サンプル データ モデル」コンフィギュレーションのバージョン 1 が既に存在するか事前にダウンロードされている場合は、ER リポジトリからダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="22edf-134">This configuration version will be downloaded from the ER repository when version 1 of the ‘Sample data model’ configuration is either already in place or downloaded in advance.</span></span> <span data-ttu-id="22edf-135">それが事前にダウンロードされている場合は、Finance and Operations バージョン 7.1.1541.3036 か、それ以降のバージョンで完了する必要があります。但し、メジャー バージョン 8 を超えてはなりません。</span><span class="sxs-lookup"><span data-stu-id="22edf-135">If it’s downloaded in advance, it must be completed in Finance and Operations version 7.1.1541.3036 or later, but must not exceed major version 8.</span></span>   
9. <span data-ttu-id="22edf-136">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-136">Click Save.</span></span>
10. <span data-ttu-id="22edf-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="22edf-137">Close the page.</span></span>
11. <span data-ttu-id="22edf-138">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-138">Click Change status.</span></span>
12. <span data-ttu-id="22edf-139">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-139">Click Complete.</span></span>
13. <span data-ttu-id="22edf-140">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-140">Click OK.</span></span>
14. <span data-ttu-id="22edf-141">ツリーで、「サンプルのデータ モデル\サンプルのマッピング (代替)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-141">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
15. <span data-ttu-id="22edf-142">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-142">Click Edit.</span></span>
16. <span data-ttu-id="22edf-143">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-143">Click New.</span></span>
17. <span data-ttu-id="22edf-144">[製品の前提条件コンポーネント] を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-144">Select Product prerequisite component.</span></span>
18. <span data-ttu-id="22edf-145">Microsoft Dynamics AX 7.0 RTW を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-145">Select Microsoft Dynamics AX 7.0 RTW.</span></span>
19. <span data-ttu-id="22edf-146">[バージョン] フィールドで、「[7.0.1265.3015,7.1]」を入力します。</span><span class="sxs-lookup"><span data-stu-id="22edf-146">In the Version field, type '[7.0.1265.3015,7.1)'.</span></span>
    * <span data-ttu-id="22edf-147">[7.0.1265.3015,7.1]</span><span class="sxs-lookup"><span data-stu-id="22edf-147">[7.0.1265.3015,7.1)</span></span>  
    * <span data-ttu-id="22edf-148">依存関係は、コンフィギュレーションが ER リポジトリからダウンロードされるときに評価されます。</span><span class="sxs-lookup"><span data-stu-id="22edf-148">Dependencies will be evaluated when the configuration is downloaded from any ER repository.</span></span> <span data-ttu-id="22edf-149">このコンフィギュレーション バージョンは、「サンプル データ モデル」コンフィギュレーションのバージョン 1 が既に存在するか事前にダウンロードされている場合は、ER リポジトリからダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="22edf-149">This configuration version will be downloaded from the ER repository when version 1 of the ‘Sample data model’ configuration is either already in place or downloaded in advance.</span></span> <span data-ttu-id="22edf-150">それが事前にダウンロードされている場合は、Microsoft Dynamics 365 for Finance and Operations Enterprise edition で完了する必要があります。またそのバージョンは 7.0.1265.3015 以降である必要がありますが、マイナー バージョン 1 を超えてはなりません。</span><span class="sxs-lookup"><span data-stu-id="22edf-150">If it’s downloaded in advance, it must be completed in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, the version of which must be 7.0.1265.3015 or later, but must not exceed minor version 1.</span></span>   
20. <span data-ttu-id="22edf-151">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-151">Click Save.</span></span>
21. <span data-ttu-id="22edf-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="22edf-152">Close the page.</span></span>
22. <span data-ttu-id="22edf-153">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-153">Click Change status.</span></span>
23. <span data-ttu-id="22edf-154">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-154">Click Complete.</span></span>
24. <span data-ttu-id="22edf-155">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-155">Click OK.</span></span>

## <a name="configure-the-er-repository"></a><span data-ttu-id="22edf-156">ER リポジトリをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="22edf-156">Configure the ER repository</span></span>
1. <span data-ttu-id="22edf-157">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="22edf-157">Close the page.</span></span>
2. <span data-ttu-id="22edf-158">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="22edf-158">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="22edf-159">現在の ER プロバイダーである Litware, Inc. の ER リポジトリの一覧を開きます。</span><span class="sxs-lookup"><span data-stu-id="22edf-159">Open the list of ER repositories for the current ER provider, Litware, Inc.</span></span>  
3. <span data-ttu-id="22edf-160">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="22edf-160">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="22edf-161">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-161">Click Repositories.</span></span>
5. <span data-ttu-id="22edf-162">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-162">Click Show filters.</span></span>
6. <span data-ttu-id="22edf-163">「包含する」フィルター演算子を使用して、「タイプ名」フィールドに「LCS」フィルター値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22edf-163">Enter a filter value of "LCS" on the "Type name" field using the "contains" filter operator.</span></span>
    * <span data-ttu-id="22edf-164">LCS リポジトリがすでに現在の ER プロバイダーに登録されている場合は、この下位タスクの残りの手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="22edf-164">If the LCS repository is already registered for the current ER provider, you can skip the remaining steps in this sub-task.</span></span> <span data-ttu-id="22edf-165">LCS リポジトリがまだ登録されていない場合は、残りの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="22edf-165">If the LCS repository isn’t already registered, complete the remaining steps.</span></span>   
7. <span data-ttu-id="22edf-166">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="22edf-166">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="22edf-167">[コンフィギュレーション リポジトリ タイプ] フィールドで「LCS」を入力します。</span><span class="sxs-lookup"><span data-stu-id="22edf-167">In the Configuration repository type field, enter 'LCS'.</span></span>
9. <span data-ttu-id="22edf-168">[リポジトリの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-168">Click Create repository.</span></span>
10. <span data-ttu-id="22edf-169">[プロジェクト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-169">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="22edf-170">[プロジェクト] フィールドのルックアップから、目的の LCS プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-170">Select the desired LCS project from the lookup of the ‘Project’ field.</span></span>  
11. <span data-ttu-id="22edf-171">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-171">Click OK.</span></span>
12. <span data-ttu-id="22edf-172">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="22edf-172">Close the page.</span></span>

## <a name="upload-configurations-to-lcs"></a><span data-ttu-id="22edf-173">コンフィギュレーションの LCS へのアップロード</span><span class="sxs-lookup"><span data-stu-id="22edf-173">Upload configurations to LCS</span></span>
1. <span data-ttu-id="22edf-174">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-174">Click Reporting configurations.</span></span>
2. <span data-ttu-id="22edf-175">ツリーで、「サンプルのデータ モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-175">In the tree, select 'Sample data model'.</span></span>
3. <span data-ttu-id="22edf-176">このコンフィギュレーションの完了したバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-176">Select the completed version of this configuration.</span></span>
4. <span data-ttu-id="22edf-177">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-177">Click Change status.</span></span>
5. <span data-ttu-id="22edf-178">[共有] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-178">Click Share.</span></span>
6. <span data-ttu-id="22edf-179">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-179">Click OK.</span></span>
    * <span data-ttu-id="22edf-180">このモデル コンフィギュレーションのバージョン 1 は、以前にコンフィギュレーションされた ER リポジトリ用の LCS プロジェクトを使用して LCS にアップロードされています。</span><span class="sxs-lookup"><span data-stu-id="22edf-180">Version 1 of this model configuration has been uploaded to LCS by using the LCS project for the ER repository that was previously configured.</span></span>   
7. <span data-ttu-id="22edf-181">ツリーで、「サンプル データ モデル」を展開します。</span><span class="sxs-lookup"><span data-stu-id="22edf-181">In the tree, expand 'Sample data model'.</span></span>
8. <span data-ttu-id="22edf-182">ツリーで、「サンプル データ モデル\サンプル マッピング」を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-182">In the tree, select 'Sample data model\Sample mapping'.</span></span>
9. <span data-ttu-id="22edf-183">このコンフィギュレーションの完了したバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-183">Select the completed version of this configuration.</span></span>
10. <span data-ttu-id="22edf-184">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-184">Click Change status.</span></span>
11. <span data-ttu-id="22edf-185">[共有] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-185">Click Share.</span></span>
12. <span data-ttu-id="22edf-186">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-186">Click OK.</span></span>
    * <span data-ttu-id="22edf-187">このモデル マッピング コンフィギュレーションのバージョン 1.1 は、以前にコンフィギュレーションされた ER リポジトリ用の LCS プロジェクトを使用して LCS にアップロードされています。</span><span class="sxs-lookup"><span data-stu-id="22edf-187">Version 1.1 of this model mapping configuration has been uploaded to LCS by using the LCS project for the ER repository that was previously configured.</span></span>   
13. <span data-ttu-id="22edf-188">ツリーで、「サンプルのデータ モデル\サンプルのマッピング (代替)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-188">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
14. <span data-ttu-id="22edf-189">このコンフィギュレーションの完了したバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-189">Select the completed version of this configuration.</span></span>
15. <span data-ttu-id="22edf-190">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-190">Click Change status.</span></span>
16. <span data-ttu-id="22edf-191">[共有] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-191">Click Share.</span></span>
17. <span data-ttu-id="22edf-192">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-192">Click OK.</span></span>
    * <span data-ttu-id="22edf-193">このモデル マッピング コンフィギュレーションのバージョン 1.1 は、以前にコンフィギュレーションされた ER リポジトリ用の LCS プロジェクトを使用して LCS にアップロードされています。</span><span class="sxs-lookup"><span data-stu-id="22edf-193">Version 1.1 of this model mapping configuration has been uploaded to LCS by using the LCS project for the ER repository that was previously configured.</span></span>   

## <a name="evaluate-er-configuration-dependencies"></a><span data-ttu-id="22edf-194">ER コンフィギュレーションの依存関係を評価します。</span><span class="sxs-lookup"><span data-stu-id="22edf-194">Evaluate ER configuration dependencies</span></span>
    * <span data-ttu-id="22edf-195">作成したコンフィギュレーションをシステムから削除し、LCS リポジトリからダウンロードしなおします。</span><span class="sxs-lookup"><span data-stu-id="22edf-195">We will delete created configurations from the system and download them back from the LCS repository.</span></span>  
1. <span data-ttu-id="22edf-196">ツリーで、「サンプル データ モデル\サンプル マッピング」を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-196">In the tree, select 'Sample data model\Sample mapping'.</span></span>
2. <span data-ttu-id="22edf-197">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-197">Click Delete.</span></span>
3. <span data-ttu-id="22edf-198">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-198">Click Yes.</span></span>
4. <span data-ttu-id="22edf-199">ツリーで、「サンプルのデータ モデル\サンプルのマッピング (代替)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-199">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
5. <span data-ttu-id="22edf-200">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-200">Click Delete.</span></span>
6. <span data-ttu-id="22edf-201">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-201">Click Yes.</span></span>
7. <span data-ttu-id="22edf-202">ツリーで、「サンプルのデータ モデル\サンプルの形式」を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-202">In the tree, select 'Sample data model\Sample format'.</span></span>
8. <span data-ttu-id="22edf-203">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-203">Click Delete.</span></span>
9. <span data-ttu-id="22edf-204">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-204">Click Yes.</span></span>
10. <span data-ttu-id="22edf-205">ツリーで、「サンプルのデータ モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-205">In the tree, select 'Sample data model'.</span></span>
11. <span data-ttu-id="22edf-206">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-206">Click Delete.</span></span>
12. <span data-ttu-id="22edf-207">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-207">Click Yes.</span></span>
13. <span data-ttu-id="22edf-208">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="22edf-208">Close the page.</span></span>
    * <span data-ttu-id="22edf-209">現在の ER プロバイダーである Litware, Inc. の ER リポジトリの一覧を開きます。</span><span class="sxs-lookup"><span data-stu-id="22edf-209">Open the list of ER repositories for the current ER provider, Litware, Inc.</span></span>  
14. <span data-ttu-id="22edf-210">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-210">Click Repositories.</span></span>
15. <span data-ttu-id="22edf-211">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-211">Click Show filters.</span></span>
16. <span data-ttu-id="22edf-212">「包含する」フィルター演算子を使用して、「タイプ名」フィールドに「LCS」フィルター値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22edf-212">Enter a filter value of "LCS" on the "Type name" field using the "contains" filter operator.</span></span>
17. <span data-ttu-id="22edf-213">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-213">Click Open.</span></span>
18. <span data-ttu-id="22edf-214">ツリーで、「サンプルのデータ モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="22edf-214">In the tree, select 'Sample data model'.</span></span>
    * <span data-ttu-id="22edf-215">現在のリポジトリの ER コンフィギュレーションの各バージョンに対して、前提条件が満たされているかどうかに関する評価を表示できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="22edf-215">Note that you can view an evaluation of whether prerequisite conditions have been satisfied for each version of the ER configurations for the current repository.</span></span> <span data-ttu-id="22edf-216">この評価を表示するには、前提条件の [確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-216">To view this evaluation, click Check prerequisites.</span></span>   
19. <span data-ttu-id="22edf-217">[前提条件の確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-217">Click Check prerequisites.</span></span>
20. <span data-ttu-id="22edf-218">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-218">Click Import.</span></span>
21. <span data-ttu-id="22edf-219">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22edf-219">Click Yes.</span></span>
22. <span data-ttu-id="22edf-220">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="22edf-220">Close the page.</span></span>
23. <span data-ttu-id="22edf-221">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="22edf-221">Close the page.</span></span>
24. <span data-ttu-id="22edf-222">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="22edf-222">Close the page.</span></span>
25. <span data-ttu-id="22edf-223">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="22edf-223">Go to Organization administration > Electronic reporting > Configurations.</span></span>
26. <span data-ttu-id="22edf-224">ツリーで、「サンプル データ モデル」を展開します。</span><span class="sxs-lookup"><span data-stu-id="22edf-224">In the tree, expand 'Sample data model'.</span></span>
    * <span data-ttu-id="22edf-225">モデル「サンプル マッピング」マッピング コンフィギュレーションが、選択されたデータ モデル コンフィギュレーションと共にダウンロードされたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="22edf-225">Note that the model ‘Sample mapping’ mapping configuration has been downloaded together with the selected data model configuration.</span></span> <span data-ttu-id="22edf-226">「サンプル マッピング」が選択したデータ モデルを実装するため、およびそれがアプリケーションに適用されるため、2 つのファイルが一括してダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="22edf-226">The two files are downloaded together because ‘Sample mapping’ has been defined as implementing the selected data model, and because it’s applicable for the application.</span></span> <span data-ttu-id="22edf-227">「サンプル マッピング (代替)」コンフィギュレーションは、必要なアプリケーション バージョンの条件が満たされていないためにダウンロードされていません。</span><span class="sxs-lookup"><span data-stu-id="22edf-227">The ‘Sample mapping (alternative)’ configuration hasn’t been downloaded because the condition for the required application version isn’t satisfied.</span></span>   
    * <span data-ttu-id="22edf-228">Finance and Operations にログインする場合は、同じプロバイダーを登録し、同じ LCS プロジェクトへアクセスし、同じデータ モデル コンフィギュレーションをダウンロードし、「サンプル マッピング (代替)」コンフィギュレーションがダウンロードされますが、「サンプル マッピング」コンフィギュレーションはスキップされます。</span><span class="sxs-lookup"><span data-stu-id="22edf-228">If you sign in to Finance and Operations, register the same provider, access the same LCS project, and download the same data model configuration, the ‘Sample mapping (alternative)’ configuration will download, whereas the ‘Sample mapping’ configuration will be skipped.</span></span>  

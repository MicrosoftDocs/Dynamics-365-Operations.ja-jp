---
title: 自動ビルドのモデル バージョンの更新
description: このトピックでは、ビルド出力のソース パッケージと配置可能なパッケージのモデルを、それらを生成したビルドのバージョンで更新する方法について説明します。
author: jorisdg
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 26731
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8b154607cb7d7695da3363b65c11fe1aeb3d1b0
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833498"
---
# <a name="update-model-versions-in-the-automated-build"></a><span data-ttu-id="a94aa-103">自動ビルドのモデル バージョンの更新</span><span class="sxs-lookup"><span data-stu-id="a94aa-103">Update model versions in the automated build</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a94aa-104">プラットフォーム更新プログラム 6 では、自動ビルド定義の新しいタスクが、作成したビルドのバージョンを持つビルド出力のソース パッケージと配置可能パッケージのモデルを更新します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-104">In Platform update 6, a new task in the automated build definition updates the models in the source package and deployable package of the build output with the version of the build that produced them.</span></span>

<span data-ttu-id="a94aa-105">プラットフォーム更新プログラム 6 以前に作成されたビルド定義はこのタスクを含めるために手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a94aa-105">Build definitions that were created before Platform update 6 must be manually updated to include this task.</span></span> <span data-ttu-id="a94aa-106">このトピックで後述する[既存のビルド定義の更新](#updating-an-existing-build-definition)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a94aa-106">See the [Updating an existing build definition](#updating-an-existing-build-definition) section later in this topic.</span></span>

## <a name="version-numbers"></a><span data-ttu-id="a94aa-107">バージョン番号</span><span class="sxs-lookup"><span data-stu-id="a94aa-107">Version numbers</span></span> 
<span data-ttu-id="a94aa-108">モデルは 1 つのパッケージにコンパイルされますが、すべてのモデルのメタデータ情報は Binary パッケージ内に保持されます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-108">Even though models are compiled into one package, the metadata information of all models is retained inside the binary package.</span></span> <span data-ttu-id="a94aa-109">この情報は、Microsoft Dynamics Lifecycle Services (LCS) またはクライアントから確認できます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-109">This information can be reviewed from Microsoft Dynamics Lifecycle Services (LCS) or from the client.</span></span>

<span data-ttu-id="a94aa-110">LCS で、次の手順に従い、環境にインストールされているモデルのバージョン番号を検索します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-110">In LCS, follow these steps to find the version numbers of models that are installed in an environment.</span></span>

1. <span data-ttu-id="a94aa-111">環境の**完全な詳細**ページで、**環境バージョン情報**の下にある、**詳細バージョン情報の表示**リンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94aa-111">On the **Full details** page for the environment, under **Environment Version Information**, click the **View detailed version information** link.</span></span> 
1. <span data-ttu-id="a94aa-112">**インストールされた更新**ページの、**コンピューター名**フィールドで、Application Object Server (AOS) コンピューターを選択します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-112">On the **Installed updates** page, in the **Machine name** field, select an Application Object Server (AOS) computer.</span></span> 
1. <span data-ttu-id="a94aa-113">テーブルの一覧で、モデルの**パブリッシャー名**フィールドを探して、矢印アイコンをクリックして一覧を展開します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-113">In the table list, find the **Publisher name** field of the model, and expand the list by clicking the arrow icon.</span></span> <span data-ttu-id="a94aa-114">その発行元からのすべてのモデルの完全な一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-114">A full list of all models from that publisher is shown.</span></span> <span data-ttu-id="a94aa-115">バージョン番号は、**バージョン** 列に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-115">The version number is shown in the **Version** column.</span></span>

<span data-ttu-id="a94aa-116">クライアントで、次の手順に従い、環境にインストールされているモデルのバージョン番号を検索します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-116">In the client, follow these steps to find the version numbers of models that are installed in an environment.</span></span>

1. <span data-ttu-id="a94aa-117">環境の URL を開いて、サインインします。</span><span class="sxs-lookup"><span data-stu-id="a94aa-117">Open the URL for the environment, and sign in.</span></span> 
1. <span data-ttu-id="a94aa-118">ダッシュ ボードが読み込まれた後、ページの右上にあるギヤ記号をクリックして、**About** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94aa-118">After the dashboard is loaded, click the gear symbol at the upper right of the page, and then click **About**.</span></span> 
1. <span data-ttu-id="a94aa-119">表示されるダイアログ ボックスで、**読み込み済みパッケージとそのモデル**を展開します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-119">In the dialog box that appears, expand **Loaded Packages and their Models**.</span></span> <span data-ttu-id="a94aa-120">モデルが存在するパッケージを検索し、矢印アイコンをクリックして一覧を展開します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-120">Find the package where the model resides, and expand the list by clicking the arrow icon.</span></span> <span data-ttu-id="a94aa-121">パッケージのモデル一覧とバージョン番号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-121">The list of models for the package is shown, together with the version number.</span></span>

<span data-ttu-id="a94aa-122">すべてのバージョン番号は .NET アセンブリ形式です。</span><span class="sxs-lookup"><span data-stu-id="a94aa-122">All version numbers are in .NET assembly format.</span></span> <span data-ttu-id="a94aa-123">それらは、**1.2.3.4** のようにドット (.) で区切られた 4 つの数字で構成されています。</span><span class="sxs-lookup"><span data-stu-id="a94aa-123">They consist of four numbers that are separated by a dot (.), such as **1.2.3.4**.</span></span>

## <a name="the-purpose-of-model-versioning"></a><span data-ttu-id="a94aa-124">モデル バージョン管理の目的</span><span class="sxs-lookup"><span data-stu-id="a94aa-124">The purpose of model versioning</span></span>
<span data-ttu-id="a94aa-125">コードが更新されると、環境に配置できる新しいパッケージを作成するためにビルドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-125">As code is updated, the build is used to produce new packages that can be deployed to environments.</span></span> <span data-ttu-id="a94aa-126">Microsoft Azure DevOps は、前回のビルド以降に各ビルドに含まれた変更を追跡します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-126">Microsoft Azure DevOps tracks the changes that have been included in each build since the previous build.</span></span> <span data-ttu-id="a94aa-127">ビルドのバージョン番号が生成されるモデルに含まれている場合、その番号によって、特定の環境で使用できるコードの変更の徹底した追跡可能性が提供されます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-127">When the version number of the build is included in the models that are produced, it provides end-to-end traceability of the code changes that are available in a specific environment.</span></span> <span data-ttu-id="a94aa-128">ビルド番号を見つけてから、Azure DevOps でそのビルドに含まれている変更を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-128">You can find the build number and then review the changes that are included in that build in Azure DevOps.</span></span> <span data-ttu-id="a94aa-129">異なる分岐でビルドを使用する、または夜間ビルド、ゲート チェックイン ビルドまたは配置ビルド用の異なるビルド定義を使用する顧客およびパートナーについては、ビルドごとに異なるバージョン スキームを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-129">For customers and partners that use builds on different branches, or that use different build definitions for nightly builds, gated check-in builds, or deployment builds, each build can have a different versioning scheme.</span></span> <span data-ttu-id="a94aa-130">この方法は、展開可能なパッケージのモデルメタデータを区別し、元のビルド定義に戻します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-130">This approach helps differentiate the model metadata in the deployable packages and tie them back to their originating build definition.</span></span>

## <a name="setting-up-versioning"></a><span data-ttu-id="a94aa-131">バージョン管理の設定</span><span class="sxs-lookup"><span data-stu-id="a94aa-131">Setting up versioning</span></span>
<span data-ttu-id="a94aa-132">プラットフォーム更新プログラム 6 または新しい配置により作成されるビルド定義については、モデルにビルド バージョンを含めるためのタスクが自動的に追加され有効になります。</span><span class="sxs-lookup"><span data-stu-id="a94aa-132">For build definitions that are created by Platform update 6 or newer deployments, the task to include build version in models is automatically added and active.</span></span> <span data-ttu-id="a94aa-133">Azure DevOps の新しいビルド定義の既定のビルド番号は、年、月、日、およびその日のビルドの増分番号で構成されます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-133">The default build number of a new build definition in Azure DevOps consists of the year, month, and day, and the incremental number of the build for that day.</span></span> <span data-ttu-id="a94aa-134">Azure DevOps のビルド番号、および使用できるオプションの詳細については、Microsoft Visual Studio ドキュメント サイトの[ビルド定義オプション](https://www.visualstudio.com/docs/build/define/options#Buildnumberformat) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a94aa-134">For more information about build numbers in Azure DevOps, and the options that are available, see [Build definition options](https://www.visualstudio.com/docs/build/define/options#Buildnumberformat) on the Microsoft Visual Studio docs site.</span></span>

<span data-ttu-id="a94aa-135">自動ビルドは、構築されたモデルにビルド バージョン番号を適用します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-135">The automated build will apply the build version number to the models that are built.</span></span>

## <a name="preventing-models-from-being-updated"></a><span data-ttu-id="a94aa-136">モデルが更新されるのを防ぐ</span><span class="sxs-lookup"><span data-stu-id="a94aa-136">Preventing models from being updated</span></span>
<span data-ttu-id="a94aa-137">既定では、ビルド タスクは ISP レイヤーより上位にあるレイヤー内のモデルにのみバージョンを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-137">By default, the build task assigns versions only to models that are in layers above the ISP layer.</span></span> <span data-ttu-id="a94aa-138">したがって、モデルで提供されているバージョン番号を上書きしなくても、サード パーティ ベンダーのコード モデルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-138">Therefore, customers can consume code models from third-party vendors without overwriting the version numbers that are supplied in their models.</span></span> <span data-ttu-id="a94aa-139">ただし、レイヤーに関係なく、ビルド中に他のモデルのバージョン番号が上書きされないようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-139">However, you can also prevent other models from having their version numbers overwritten during the build, regardless of layer.</span></span> <span data-ttu-id="a94aa-140">ビルド定義を編集するときは、**変数** タブの **ModelVersionExclusions** 変数で、除外するモデル名のコンマ区切りの一覧を供給します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-140">When you edit the build definition, on the **Variables** tab, in the **ModelVersionExclusions** variable, supply a comma-separated list of model names to exclude.</span></span>

## <a name="updating-models-in-lower-layers"></a><span data-ttu-id="a94aa-141">下位レイヤーのモデルの更新</span><span class="sxs-lookup"><span data-stu-id="a94aa-141">Updating models in lower layers</span></span>
<span data-ttu-id="a94aa-142">ISV または ISP レイヤーでソリューションを開発するサード パーティについては、それらのレイヤーでモデル バージョンを自動で設定するため、手動変更がビルド定義に対して加えられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a94aa-142">For third parties that develop solutions in the ISV or ISP layer, a manual change must be made to the build definition to automatically set model versions in those layers.</span></span> 

1. <span data-ttu-id="a94aa-143">ビルド定義を編集します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-143">Edit the build definition.</span></span> <span data-ttu-id="a94aa-144">**タスク**タブで、**モデル バージョンの設定**タスクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94aa-144">On the **Tasks** tab, click the **Set Model Versions** task.</span></span> 
1. <span data-ttu-id="a94aa-145">**引数**フィールドで、既存の引数のリストの最後に **-UpdateLayersAbove 7** のオプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-145">In the **Arguments** field, add the following option at the end of the existing list of arguments: **-UpdateLayersAbove 7**</span></span>

## <a name="updating-an-existing-build-definition"></a><span data-ttu-id="a94aa-146">既存のビルド定義の更新</span><span class="sxs-lookup"><span data-stu-id="a94aa-146">Updating an existing build definition</span></span>
<span data-ttu-id="a94aa-147">プラットフォーム更新プログラム 6 以前に作成されたビルド定義では、新しいタスクをビルド定義に手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a94aa-147">For build definitions that were created before Platform update 6, a new task must be manually added to the build definition.</span></span>

> [!NOTE]
> <span data-ttu-id="a94aa-148">この機能は、ビルド仮想マシン (VM) がプラットフォーム更新プログラム 6 以降に更新された後にのみ、ビルド定義に追加できます。</span><span class="sxs-lookup"><span data-stu-id="a94aa-148">This feature can be added to a build definition only after the build virtual machine (VM) has been updated to Platform update 6 or later.</span></span>

1. <span data-ttu-id="a94aa-149">Azure DevOps で、**ビルドおよびリリース** ページの**ビルド**にある**すべての定義**タブでビルド定義を検索します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-149">In Azure DevOps, on the **Build & Release** page, under **Builds**, on the **All Definitions** tab, find your build definition.</span></span> 
1. <span data-ttu-id="a94aa-150">省略記号 (...)、**編集**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94aa-150">Click the ellipsis (…), and then click **Edit**.</span></span>

    ![ビルド定義を編集](media/builddef_edit.png)

1. <span data-ttu-id="a94aa-152">**タスク**タブで、ページの下部にある **+ タスクの追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94aa-152">On the **Tasks** tab, click **+ Add Task** at the bottom of the page.</span></span>
1. <span data-ttu-id="a94aa-153">ページの右側にある**タスクの追加**ウィンドウの**ユーティリティ** タブで、下にスクロールして **PowerShell** タスクを表示します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-153">In the **Add tasks** pane on the right side of the page, on the **Utility** tab, scroll down to find the **PowerShell** task.</span></span> 
1. <span data-ttu-id="a94aa-154">マウス ポインタをタスク上にポイントして、表示する**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94aa-154">Hover the mouse pointer over the task, and click the **Add** button that appears.</span></span>

    ![PowerShell タスクの追加](media/builddef_addpowershelltask.png)

1. <span data-ttu-id="a94aa-156">ページの左側にあるタスクの一覧で、追加される **PowerShell スクリプト** タスクをクリックして選択します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-156">In the list of tasks on the left side of the page, click to select the **PowerShell Script** task that is added.</span></span>
1. <span data-ttu-id="a94aa-157">ページの右側で、**表示名**、**スクリプト パス**、および**引数**プロパティを変更して必要な設定を反映します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-157">On the right side of the page, change the **Display name**, **Script Path**, and **Arguments** properties to reflect the required settings.</span></span>

    ![モデル バージョンの設定作業のプロパティを設定](media/builddef_setmodelversions_settings.png)

1. <span data-ttu-id="a94aa-159">ページの左側にあるタスクの一覧で、**モデル バージョンの設定**タスクを、**ビルドの準備**と**ソリューションのビルド** タスクの間にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="a94aa-159">In the list of tasks on the left side of the page, drag the **Set Model Versions** task so that it's between the **Prepare for build** and **Build the solution** tasks.</span></span>

    ![モデル バージョンの設定作業の順序を設定](media/builddef_setmodelversions_order.png)

1. <span data-ttu-id="a94aa-161">**変数**タブで、変数のリストの下部にある **+ 追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94aa-161">On the **Variables** tab, click **+ Add** at the bottom of the list of variables.</span></span> <span data-ttu-id="a94aa-162">最初の列で、**名前**の変数に **ModelVersionExclusions** と入力します。</span><span class="sxs-lookup"><span data-stu-id="a94aa-162">In the first column, for the **Name** variable, enter **ModelVersionExclusions**.</span></span>
1. <span data-ttu-id="a94aa-163">新しいタスクを保存するには、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a94aa-163">Click **Save** to save the new task.</span></span>

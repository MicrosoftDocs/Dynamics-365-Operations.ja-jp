---
title: ビルド出力からテスト パッケージを除外
description: このトピックでは、自動ビルドプロセスが生成するビルド出力で、特定のパッケージが展開可能パッケージに含まれないようにする方法について説明します。
author: jorisdg
manager: AnnBe
ms.date: 05/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 26731
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3452f9a8fb317ce9948d56153515c6f2d3572f1c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536990"
---
# <a name="exclude-test-packages-from-build-output"></a><span data-ttu-id="bd510-103">ビルド出力からテスト パッケージを除外</span><span class="sxs-lookup"><span data-stu-id="bd510-103">Exclude test packages from build output</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd510-104">プラットフォーム更新プログラム 4 では、自動ビルド プロセスにより、ビルド出力で特定のパッケージが配置可能パッケージに含まれないようにできます。</span><span class="sxs-lookup"><span data-stu-id="bd510-104">In Platform update 4, the automated build process lets you prevent specific packages from being included in the deployable package in the build output.</span></span> <span data-ttu-id="bd510-105">この機能は、自動化されたテストを使用する顧客にとって重要なことです。</span><span class="sxs-lookup"><span data-stu-id="bd510-105">This capability can be important for customers that use automated testing.</span></span> <span data-ttu-id="bd510-106">これらの顧客は、テストをビルドして実行したいが、ビルドが出力として生成する配置可能なパッケージにテストが追加したくないと考えている場合があります。</span><span class="sxs-lookup"><span data-stu-id="bd510-106">These customers might want to build and run their tests, but prevent them from being added to the deployable package that the build generates as output.</span></span>

<span data-ttu-id="bd510-107">プラットフォーム更新プログラム 3 またはそれ以前の既存のビルド定義を持っている顧客がアップグレードするとき、ビルド定義が自動的に更新されることが表示されません。</span><span class="sxs-lookup"><span data-stu-id="bd510-107">When customers that have an existing build definition from Platform update 3 or earlier upgrade, they won't see the build definition automatically updated.</span></span> <span data-ttu-id="bd510-108">新しい機能を使用するには、これらの顧客はビルド定義を手動で編集する必要があります (詳細は下記参照)。</span><span class="sxs-lookup"><span data-stu-id="bd510-108">To use the new feature, these customers must make a few manual edits to the build definition (see below for details).</span></span> 

<span data-ttu-id="bd510-109">この新機能は、ビルド プロセスにおけるパッケージ作成ステップの新しいオプション パラメーターを公開します。</span><span class="sxs-lookup"><span data-stu-id="bd510-109">The new feature exposes a new optional parameter for the package creation step in the build process.</span></span> <span data-ttu-id="bd510-110">このパラメーターはビルド変数で管理されるため、簡単に調整できます。</span><span class="sxs-lookup"><span data-stu-id="bd510-110">Because this parameter is managed by a build variable, you can easily adjust it.</span></span>

1. <span data-ttu-id="bd510-111">Microsoft Azure DevOps で、**ビルドおよびリリース** ページの**ビルド**にある**すべての定義タブ**でビルド定義を検索します。</span><span class="sxs-lookup"><span data-stu-id="bd510-111">In Microsoft Azure DevOps, on the **Build & Release** page, under **Builds**, on the **All Definitions** tab, find your build definition.</span></span> <span data-ttu-id="bd510-112">省略記号 (...)、**編集**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="bd510-112">Click the ellipsis (…), and then click **Edit**.</span></span>

    ![ビルド定義を編集](media/builddef_edit.png)

1. <span data-ttu-id="bd510-114">**変数**タブで、新しいビルド定義が **PackagingExclusions** という名前の変数を持つこと通知します。</span><span class="sxs-lookup"><span data-stu-id="bd510-114">On the **Variables** tab, notice that the new build definition has a variable that is named **PackagingExclusions**.</span></span>

    ![PackagingExclusions 変数](media/builddef_packexclvariable.png)

1. <span data-ttu-id="bd510-116">**PackagingExclusions** 変数で、配置可能パッケージにパッケージする必要がないパッケージの名前をコンマで区切ったリストで指定します。</span><span class="sxs-lookup"><span data-stu-id="bd510-116">In the **PackagingExclusions** variable, specify a comma-separated list of the names of packages that should not be packaged into the deployable package.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bd510-117">パッケージの名前は必ずしもモデルの名前ではありません。</span><span class="sxs-lookup"><span data-stu-id="bd510-117">The name of a package isn't necessarily the name of the model.</span></span> <span data-ttu-id="bd510-118">代わりに、パッケージ名は通常、モデルがあるフォルダーの名前です。</span><span class="sxs-lookup"><span data-stu-id="bd510-118">Instead, the package name is typically the name of the folder where the model resides.</span></span> <span data-ttu-id="bd510-119">または、パッケージ モデルのいずれかの記述子ファイルからパッケージ名をコピーして貼り付けることができます。</span><span class="sxs-lookup"><span data-stu-id="bd510-119">Alternatively, you can copy and paste the package name from the descriptor file of one of the package's models.</span></span> <span data-ttu-id="bd510-120">(XML では、**ModelModule** フィールドでパッケージ名を検索できます。)</span><span class="sxs-lookup"><span data-stu-id="bd510-120">(In the XML, you can find the package name in the **ModelModule** field.)</span></span>

    <span data-ttu-id="bd510-121">たとえば、MyCompanysAwesomeTests という名前の 1 つのパッケージおよび ContosoTaskRecordingTests という名前の別のパッケージがあり、配置可能なパッケージからこれら両方のパッケージを除外します。</span><span class="sxs-lookup"><span data-stu-id="bd510-121">For example, you have one package that is named MyCompanysAwesomeTests and another package that is named ContosoTaskRecordingTests, and you want to exclude both these packages from the deployable package.</span></span> <span data-ttu-id="bd510-122">この場合、**PackagingExclusions** 変数の値はこのようになります。</span><span class="sxs-lookup"><span data-stu-id="bd510-122">In this case, the value for the **PackagingExclusions** variable will look like this.</span></span>

    ![PackagingExclusions の例](media/builddef_packexclexample.png)

    <span data-ttu-id="bd510-124">この設定を完了すると、ビルド プロセスはコードをビルドしながらパッケージに含まれているすべてのテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="bd510-124">After you complete this setup, the build process will still build the code and run any tests that the packages contain.</span></span> <span data-ttu-id="bd510-125">ただし、ビルドが作成する配置可能なパッケージには、それらのパッケージは含まれません。</span><span class="sxs-lookup"><span data-stu-id="bd510-125">However, the deployable package that the build creates won't include those packages.</span></span>

## <a name="update-an-existing-build-definition-after-upgrade-to-platform-update-4-or-later"></a><span data-ttu-id="bd510-126">プラットフォーム更新プログラム 4 以降へのアップグレード後に既存のビルド定義を更新する</span><span class="sxs-lookup"><span data-stu-id="bd510-126">Update an existing build definition after upgrade to Platform update 4 or later</span></span>

<span data-ttu-id="bd510-127">新しい機能を使用するには、Platform update 4 より前に展開した既存のビルド定義を手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd510-127">To use the new feature, you must manually update any existing build definitions that you deployed before Platform update 4.</span></span>

> [!NOTE]
> <span data-ttu-id="bd510-128">この機能は、ビルド仮想マシン (VM) をプラットフォーム更新プログラム 4 以降に更新した後でのみ、ビルド定義に追加できます。</span><span class="sxs-lookup"><span data-stu-id="bd510-128">The feature can be added to a build definition only after you update the build virtual machine (VM) to Platform update 4 or later.</span></span>

1. <span data-ttu-id="bd510-129">**変数**タブで、ページの下部にある **+ 追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bd510-129">On the **Variables** tab, click **+ Add** at the bottom of the page.</span></span>
1. <span data-ttu-id="bd510-130">**名前**列に、**PackagingExclusions** と入力します。</span><span class="sxs-lookup"><span data-stu-id="bd510-130">In the **Name** column, enter **PackagingExclusions**.</span></span> <span data-ttu-id="bd510-131">最後の列で、**キュー時に設定可能**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="bd510-131">In the last column, select the **Settable at queue time** check box.</span></span>
1. <span data-ttu-id="bd510-132">**タスク**タブで、**生成パッケージ**タスクを検索します。</span><span class="sxs-lookup"><span data-stu-id="bd510-132">On the **Tasks** tab, find the **Generate Packages** task.</span></span> <span data-ttu-id="bd510-133">クリックして選択します。</span><span class="sxs-lookup"><span data-stu-id="bd510-133">Click to select it.</span></span>
1. <span data-ttu-id="bd510-134">ページの右側で、**引数**パラメーターを見つけます。</span><span class="sxs-lookup"><span data-stu-id="bd510-134">On the right side of the page, find the **Arguments** parameter.</span></span> <span data-ttu-id="bd510-135">テキスト ボックスをクリックし、End キーを押すか、テキスト ボックスの最後までスクロールします。</span><span class="sxs-lookup"><span data-stu-id="bd510-135">Click in the text box, and then press the End key or scroll to the end of the text box.</span></span> <span data-ttu-id="bd510-136">新しいビルド定義には、前に定義した **PackagingExclusions** 変数を渡す新しい引数があります。</span><span class="sxs-lookup"><span data-stu-id="bd510-136">The new build definition will have a new argument that passes the **PackagingExclusions** variable that you defined earlier.</span></span> <span data-ttu-id="bd510-137">ただし、既存のビルド定義については、スペースを追加し、さらにパラメーターの末尾に次のテキストを追加します: **-ExclusionList "$(PackagingExclusions)"**</span><span class="sxs-lookup"><span data-stu-id="bd510-137">However, for an existing build definition, add a space and then the following text to the end of the parameter: **-ExclusionList "$(PackagingExclusions)"**</span></span>

    <span data-ttu-id="bd510-138">**引数** テキスト ボックスは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="bd510-138">The **Arguments** text box should now look like this.</span></span>

    ![パッケージ タスクを生成します](media/builddef_generatepack.png)

1. <span data-ttu-id="bd510-140">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bd510-140">Click **Save**.</span></span>

<span data-ttu-id="bd510-141">説明の通りに、新しいフィーチャーを使用することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="bd510-141">You can now use the new feature as described.</span></span>

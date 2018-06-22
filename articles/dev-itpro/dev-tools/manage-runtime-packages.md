---
title: "ソース コントロールを使用してサード パーティ モデルとランタイム パッケージを管理"
description: "このトピックでは、サードパーティ ソリューションを管理、配布、展開するうえで推奨される戦略について説明します。"
author: jorisdg
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 26731
ms.assetid: 
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 764ec7906f55a9e9b41db0f33fe2e6335382637f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="manage-third-party-models-and-runtime-packages-by-using-source-control"></a><span data-ttu-id="00614-103">ソース コントロールを使用してサード パーティ モデルとランタイム パッケージを管理</span><span class="sxs-lookup"><span data-stu-id="00614-103">Manage third-party models and runtime packages by using source control</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00614-104">サード パーティのソリューションを使用する顧客は、ソリューションで使用するさまざまなソリューション コンポーネントを受け取ることがあります。</span><span class="sxs-lookup"><span data-stu-id="00614-104">Customers that work with solutions from third parties might receive different solution artifacts to use in their solution.</span></span> <span data-ttu-id="00614-105">通常、これらのアーティファクトはコード (モデルの形式) またはバイナリ (展開可能なパッケージの形式) で配布されます。</span><span class="sxs-lookup"><span data-stu-id="00614-105">Typically, these artifacts are distributed as code (in the form of models) or binaries (in the form of deployable packages).</span></span> <span data-ttu-id="00614-106">場合によっては、サード パーティは、ソリューションの一部をバイナリのコードとその他のパーツとして提供する場合があります。</span><span class="sxs-lookup"><span data-stu-id="00614-106">In some cases, third parties might provide some parts of their solution as code and other parts as a binary.</span></span>

<span data-ttu-id="00614-107">このトピックでは、これらのサードパーティ ソリューションを管理、配布、展開するための推奨される戦略について説明します。</span><span class="sxs-lookup"><span data-stu-id="00614-107">This topic outlines a recommended strategy for managing, distributing, and deploying these third-party solutions.</span></span>

## <a name="models-from-third-parties"></a><span data-ttu-id="00614-108">サード パーティからのモデル</span><span class="sxs-lookup"><span data-stu-id="00614-108">Models from third parties</span></span>
<span data-ttu-id="00614-109">サード パーティから受け取ったソース コードは、バイナリにコンパイルし、配置可能パッケージに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="00614-109">Any source code that is received from third parties must be compiled into a binary and included in a deployable package.</span></span> <span data-ttu-id="00614-110">モデルは、開発仮想マシン (VM) にインストールしてソース管理に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00614-110">Models should be installed on a development virtual machine (VM) and added to source control.</span></span> <span data-ttu-id="00614-111">そこからは、ビルド VM はソース コードをピッキング、構築、および配置可能パッケージに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="00614-111">From there, the build VM can pick up the source code, build it, and include it in a deployable package.</span></span> <span data-ttu-id="00614-112">他の開発者は、Microsoft Visual Studio チーム サービス (VSTS) のモデルをそのまま開発 VM に同期できます。</span><span class="sxs-lookup"><span data-stu-id="00614-112">Other developers can just synchronize the model from Microsoft Visual Studio Team Services (VSTS) to their development VMs.</span></span> <span data-ttu-id="00614-113">手動でインストールする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="00614-113">They don't have to manually install it.</span></span>

<span data-ttu-id="00614-114">開発 VM でモデルをインストールする方法の詳細については、[モデルのエクスポートとインポート](models-export-import.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00614-114">For information about how to install a model on a development VM, see [Export and import a model](models-export-import.md).</span></span>

<span data-ttu-id="00614-115">モデルをインストールしたら、以下の手順に従いソース管理に新しいモデルを追加します。</span><span class="sxs-lookup"><span data-stu-id="00614-115">After you install the model, follow these steps to add the new model to source control.</span></span>

1. <span data-ttu-id="00614-116">Microsoft Visual Studio の **Dynamics 365** メニューで、**モデル管理** > **モデルの更新**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-116">In Microsoft Visual Studio, on the **Dynamics 365** menu, click **Model Management** > **Refresh Models**.</span></span>
2. <span data-ttu-id="00614-117">**表示** > **アプリケーション エクスプローラー**をクリックして、アプリケーション エクスプ ローラーを開きます。</span><span class="sxs-lookup"><span data-stu-id="00614-117">Open Application Explorer by clicking **View** > **Application Explorer**.</span></span>
3. <span data-ttu-id="00614-118">**AOT**ルート ノードを右クリックし、、**モデル ビュー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-118">Right-click the **AOT** root node, and then click **Model view**.</span></span>
4. <span data-ttu-id="00614-119">モデルの一覧で、インストールした新しいモデルを検索します。</span><span class="sxs-lookup"><span data-stu-id="00614-119">In the list of models, find the new model that you installed.</span></span> <span data-ttu-id="00614-120">モデルを含むパッケージの名前をメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="00614-120">Make a note of the name of the package that contains the model.</span></span> <span data-ttu-id="00614-121">パッケージ名はモデル名の後にかっこ付きで表示されます。</span><span class="sxs-lookup"><span data-stu-id="00614-121">The package name appears in parentheses after the model name.</span></span> <span data-ttu-id="00614-122">たとえば、次の図では、**税帳簿**、**税エンジン コンフィギュレーション**、および**税エンジン インターフェイス**モデルはすべて **TaxEngine** という名前のパッケージに属します。</span><span class="sxs-lookup"><span data-stu-id="00614-122">For example, in the following illustration, the **Tax Books**, **Tax Engine Configuration**, and **Tax Engine Interface** models all belong to the package that is named **TaxEngine**.</span></span>

    ![各モデルのパッケージ名](media/appexplorer_modelpackagename.png)

5. <span data-ttu-id="00614-124">**表示** > **その他の Windows** > **ソース管理エクスプローラー**をクリックして、ソース管理エクスプローラーを開きます</span><span class="sxs-lookup"><span data-stu-id="00614-124">Open Source Control Explorer by clicking **View** > **Other Windows** > **Source Control Explorer**.</span></span>
6. <span data-ttu-id="00614-125">**MyProject/Trunk/Main/Metadata** など、この開発 VM にマップされているメタデータ フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="00614-125">Navigate to the metadata folder that is mapped on this development VM, such as **MyProject/Trunk/Main/Metadata**.</span></span>
7. <span data-ttu-id="00614-126">メタデータ フォルダーで、新しいモデルを含むパッケージのフォルダーを探します。</span><span class="sxs-lookup"><span data-stu-id="00614-126">In the metadata folder, find the folder for the package that contains the new model.</span></span> <span data-ttu-id="00614-127">パッケージ フォルダーを右クリックし、**フォルダーへの品目の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-127">Right-click the package folder, and then click **Add Items to Folder**.</span></span>
9. <span data-ttu-id="00614-128">**ソース管理に追加**ダイアログ ボックスで、**記述子**フォルダーとモデルの名前があるフォルダーを選択してから**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-128">In the **Add to Source Control** dialog box, select the **Descriptor** folder and the folder that has the name of the model, and then click **Next**.</span></span>
10. <span data-ttu-id="00614-129">追加する品目を確認し、準備ができたら **完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-129">Review the items that will be added, and then, when you're ready, click **Finish**.</span></span>
11. <span data-ttu-id="00614-130">**保留中の変更**ウィンドウを、**チーム エクスプローラー**ウィンドウから、または**表示** > **その他の Windows** > **保留中の変更**をクリックして開きます。</span><span class="sxs-lookup"><span data-stu-id="00614-130">Open the **Pending Changes** window from the **Team Explorer** pane or by clicking **View** > **Other Windows** > **Pending Changes**.</span></span>
12. <span data-ttu-id="00614-131">変更を確認してチェックイン コメントを入力し、**チェック イン** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-131">Review the changes, enter a check-in comment, and then click **Check In**.</span></span>

## <a name="deployable-packages-from-third-parties"></a><span data-ttu-id="00614-132">サード パーティから展開可能なパッケージ</span><span class="sxs-lookup"><span data-stu-id="00614-132">Deployable packages from third parties</span></span>
<span data-ttu-id="00614-133">サード パーティの展開可能パッケージを開発用 VM に手動でインストールし、インストールされたコンポーネントをソース管理に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="00614-133">Deployable packages from third parties can be manually installed on a development VM, and the installed artifacts can then be added to source control.</span></span> <span data-ttu-id="00614-134">その後、ローカル ワークスペースを同期させることで、他の開発者が、展開可能なパッケージをインストールしなくても、VM 上でランタイム パッケージを受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="00614-134">Then, by synchronizing their local workspace, other developers can receive the runtime package on their VMs without having to install the deployable package.</span></span> <span data-ttu-id="00614-135">ビルド VM でのビルド プロセスは、ビルド VM 上で拡張機能やその他の依存関係のランタイム パッケージを使用できるようにするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="00614-135">The build process on the build VM will help guarantee that the runtime packages for any extensions or other dependencies are available on the build VM.</span></span> <span data-ttu-id="00614-136">プラットフォーム更新プログラム 6 以降では、既定でビルド VM から作成される最終的な配置可能パッケージにこれらのランタイム パッケージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="00614-136">In Platform update 6 and later, by default, these runtime packages will be included in the final deployable package that is created from the build VM.</span></span> <span data-ttu-id="00614-137">詳細については、このトピックの後半の [サード パーティ コードを展開する](#deploying-third-party-code) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="00614-137">For more information, see the  [Deploying third-party code](#deploying-third-party-code) section later in this topic.</span></span>

<span data-ttu-id="00614-138">開発 VM で配置可能パッケージをインストールする方法の詳細については、[配置可能パッケージのインストール](../deployment/install-deployable-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00614-138">For information about how to install a deployable package on a development VM, see [Install a deployable package](../deployment/install-deployable-package.md).</span></span>

> [!NOTE]
> <span data-ttu-id="00614-139">ビルド VM にソフトウェア配置可能パッケージを直接インストールしないでください。</span><span class="sxs-lookup"><span data-stu-id="00614-139">Don't install a software deployable package directly on the build VM.</span></span> <span data-ttu-id="00614-140">このトピックで説明するソース管理を使用します。</span><span class="sxs-lookup"><span data-stu-id="00614-140">Use source control as described in this topic.</span></span> <span data-ttu-id="00614-141">バイナリ更新プログラムのみビルド VM にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="00614-141">Only binary updates should be installed on build VMs.</span></span>

<span data-ttu-id="00614-142">開発 VM に配置可能パッケージをインストールした後は、以下の手順に従いソース管理にランタイム パッケージを追加します。</span><span class="sxs-lookup"><span data-stu-id="00614-142">After you install the deployable package on a development VM, follow these steps to add the runtime package to source control.</span></span>

1. <span data-ttu-id="00614-143">**表示** > **その他の Windows** > **ソース管理エクスプローラー**をクリックして、ソース管理エクスプローラーを開きます</span><span class="sxs-lookup"><span data-stu-id="00614-143">Open Source Control Explorer by clicking **View** > **Other Windows** > **Source Control Explorer**.</span></span>
2. <span data-ttu-id="00614-144">**MyProject/Trunk/Main/Metadata** など、この開発 VM にマップされているメタデータ フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="00614-144">Navigate to the metadata folder that is mapped on this development VM, such as **MyProject/Trunk/Main/Metadata**.</span></span>
3. <span data-ttu-id="00614-145">**メタデータ** フォルダーを右クリックし、**フォルダーへの品目の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-145">Right-click the **Metadata** folder, and then click **Add Items to Folder**.</span></span>
4. <span data-ttu-id="00614-146">**ソース管理に追加**ダイアログ ボックスで、ソース管理に追加するパッケージ名があるフォルダーをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-146">In the **Add to Source Control** dialog box, double-click the folder that has the package name that you want to add to source control.</span></span>
5. <span data-ttu-id="00614-147">**XppMetadata** および **Descriptor** (存在する場合) を除くすべてのフォルダーを選択し、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-147">Select all the folders except **XppMetadata** and **Descriptor**, if they exist, and then click **Next**.</span></span>
6. <span data-ttu-id="00614-148">次のページで、**除外した項目**タブで、ファイルのいずれかをクリックし Ctrl + A キーを押してすべてのファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="00614-148">On the next page, on the **Excluded items** tab, select all files by clicking one of the files and then pressing Ctrl+A.</span></span> <span data-ttu-id="00614-149">選択ウィンドウの下部にある**項目を含める**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-149">At the bottom of the selection window, click **Include item(s)**.</span></span> <span data-ttu-id="00614-150">準備ができたら、**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-150">When you're ready, click **Finish**.</span></span>
7. <span data-ttu-id="00614-151">**保留中の変更**ウィンドウを、**チーム エクスプローラー**ウィンドウから、または**表示** > **その他の Windows** > **保留中の変更**をクリックして開きます。</span><span class="sxs-lookup"><span data-stu-id="00614-151">Open the **Pending Changes** window from the **Team Explorer** pane or by clicking **View** > **Other Windows** > **Pending Changes**.</span></span>
8. <span data-ttu-id="00614-152">変更を確認してチェックイン コメントを入力し、**チェック イン** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00614-152">Review the changes, enter a check-in comment, and then click **Check In**.</span></span>

## <a name="deploying-third-party-code"></a><span data-ttu-id="00614-153">サード パーティのコードを展開する</span><span class="sxs-lookup"><span data-stu-id="00614-153">Deploying third-party code</span></span>
<span data-ttu-id="00614-154">モデルとランタイム パッケージはソース管理のため、他の開発環境を使用する他の開発者はソース管理の**最新を取得**機能を使用してモデルとパッケージをワークスペースに同期させることができます。</span><span class="sxs-lookup"><span data-stu-id="00614-154">Because the models and runtime packages are in source control, other developers who use other development environments can just synchronize the models and packages to their workspace by using the **Get latest** feature of source control.</span></span>

<span data-ttu-id="00614-155">現在のプラットフォーム更新プログラム 4 では、自動ビルド プロセスはランタイム パッケージも取得します。</span><span class="sxs-lookup"><span data-stu-id="00614-155">As of Platform update 4, the automated build process will also pick up the runtime packages.</span></span> <span data-ttu-id="00614-156">したがって、ビルドされたパッケージの依存関係は正しく解決されます。</span><span class="sxs-lookup"><span data-stu-id="00614-156">Therefore, dependencies in packages that are built will be resolved correctly.</span></span> <span data-ttu-id="00614-157">この機能は、修正プログラムを介してプラットフォーム更新プログラム 3 およびプラットフォーム更新プログラム 2 でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="00614-157">This feature is also available for Platform update 3 and Platform update 2 through a hotfix.</span></span>

<span data-ttu-id="00614-158">プラットフォーム更新プログラム 6 では、ビルド プロセスで最終的な配置可能パッケージにこのランタイム パッケージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="00614-158">In Platform update 6, the build process will include this runtime package in the final deployable package.</span></span> <span data-ttu-id="00614-159">これにより、お客様は、展開可能なパッケージをビルドから取り出し、1 つのパッケージを環境に展開できます。</span><span class="sxs-lookup"><span data-stu-id="00614-159">This allows customers to take the deployable package from the build and have one package to deploy to their environments.</span></span> <span data-ttu-id="00614-160">1 つのパッケージにはカスタム ソリューションとすべてのサード パーティ ソリューションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="00614-160">The one package includes both custom solutions and all the third party solutions.</span></span>


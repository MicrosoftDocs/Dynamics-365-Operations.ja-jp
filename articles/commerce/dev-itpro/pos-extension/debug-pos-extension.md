---
title: POS 拡張機能のデバッグ
description: このトピックでは、POS 拡張機能のデバッグ方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 0f114824b36cd1400432ee2958403af9bfafe3fc
ms.sourcegitcommit: fd15b02fc9caa1c05e56abdc276a7f4b23b0d8f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5960154"
---
# <a name="debugging-pos-extensions"></a><span data-ttu-id="d2305-103">POS 拡張機能のデバッグ</span><span class="sxs-lookup"><span data-stu-id="d2305-103">Debugging POS extensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2305-104">このトピックでは、POS 拡張機能のデバッグ方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d2305-104">This topic explains how to debug a POS extension.</span></span> <span data-ttu-id="d2305-105">これは、Retail SDK バージョン 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d2305-105">It applies to the Retail SDK, version 10.0.18 and later.</span></span>

## <a name="debugging-modern-pos-using-visual-studio-2017"></a><span data-ttu-id="d2305-106">Visual Studio 2017 を使用した Modern POS のデバッグ</span><span class="sxs-lookup"><span data-stu-id="d2305-106">Debugging Modern POS using Visual Studio 2017</span></span>

<span data-ttu-id="d2305-107">次の手順に従って拡張機能をデバッグします。</span><span class="sxs-lookup"><span data-stu-id="d2305-107">Debug your extension by following these steps:</span></span>

1. <span data-ttu-id="d2305-108">シールドされた MPOS インストーラーを使用して、開発マシンでシールドされた Modern POS をインストールします。</span><span class="sxs-lookup"><span data-stu-id="d2305-108">Install Sealed Modern POS on the development machine using the Sealed MPOS installer.</span></span>
2. <span data-ttu-id="d2305-109">デスクトップ上のショートカットをクリックして UWP アプリをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d2305-109">Install the UWP app by clicking the shortcut on the desktop.</span></span>
3. <span data-ttu-id="d2305-110">Visual Studio で、Modern POS 拡張機能パッケージ プロジェクト (**jsproj**) を構築します。</span><span class="sxs-lookup"><span data-stu-id="d2305-110">In Visual Studio, build your Modern POS Extension Package Project (**jsproj**).</span></span>
4. <span data-ttu-id="d2305-111">Visual Studio で、Modern POS 拡張機能パッケージを展開します。</span><span class="sxs-lookup"><span data-stu-id="d2305-111">In Visual Studio, deploy your Modern POS Extension Package.</span></span> <span data-ttu-id="d2305-112">ソリューション エクスプローラーで ModernPOS JavaScript プロジェクト ファイルを右クリックしてから、**展開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d2305-112">Right-click the ModernPOS JavaScript project file in Solution Explorer and select **Deploy**.</span></span>
5. <span data-ttu-id="d2305-113">次の手順に従って、デバッガーが関連付けられた POS を起動します。</span><span class="sxs-lookup"><span data-stu-id="d2305-113">Launch POS with the debugger attached, by following these steps:</span></span>

    1. <span data-ttu-id="d2305-114">**デバッグ** メニューで、**その他のデバッグ ターゲット &gt; インストールされたアプリをデバッグする**。</span><span class="sxs-lookup"><span data-stu-id="d2305-114">In the **Debug** menu, select **Other Debug Targets &gt; Debug Installed App Package**.</span></span>
    2. <span data-ttu-id="d2305-115">**Commerce Modern POS** を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="d2305-115">Search for and Select **Commerce Modern POS**.</span></span>
    3. <span data-ttu-id="d2305-116">**開始** をクリックしてアプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="d2305-116">Click **Start** to launch the application.</span></span>

## <a name="running-and-debugging-cloud-pos"></a><span data-ttu-id="d2305-117">Cloud POS の実行およびデバッグ</span><span class="sxs-lookup"><span data-stu-id="d2305-117">Running and Debugging Cloud POS</span></span>

### <a name="configuring-the-cloud-pos-extension-development-environment"></a><a name="configure-cloud-pos"></a> <span data-ttu-id="d2305-118">Cloud POS 拡張機能の開発環境の構成</span><span class="sxs-lookup"><span data-stu-id="d2305-118">Configuring the Cloud POS extension development environment</span></span>

<span data-ttu-id="d2305-119">拡張機能パッケージがマシン上で初めて開発されたとき、またはリンクが削除された場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d2305-119">Run the following steps the first time that an extension package is developed on the machine or if the link is deleted.</span></span> <span data-ttu-id="d2305-120">Cloud POS 拡張機能ディレクトリに、拡張機能パッケージ ルート ディレクトリへのディレクトリ シンボル リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="d2305-120">Create a directory symbolic link in the Cloud POS extensions directory to the extension package root directory.</span></span>

1. <span data-ttu-id="d2305-121">Cloud POS がマシンに配置されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2305-121">Make sure that Cloud POS is deployed on your machine.</span></span> <span data-ttu-id="d2305-122">インストールされていない場合は、CSU 自己ホスト型インストーラーを使用して Cloud POS を配置します。</span><span class="sxs-lookup"><span data-stu-id="d2305-122">If it isn't, use the CSU Self-Hosted installer to Deploy Cloud POS.</span></span>
2. <span data-ttu-id="d2305-123">IIS を開きます。</span><span class="sxs-lookup"><span data-stu-id="d2305-123">Open IIS.</span></span> <span data-ttu-id="d2305-124">**実行** メニュー (**Windows キー + R**) を開き、**inetmgr** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d2305-124">Open the **Run** menu (**Windows key + R**), and then type: **inetmgr**.</span></span> <span data-ttu-id="d2305-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d2305-125">Select **OK**.</span></span>
3. <span data-ttu-id="d2305-126">**サイト &gt; RetailCloudPos を選択** を展開し、右クリックして **エクスプローラ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d2305-126">Expand **Sites &gt; Select RetailCloudPos** and then right-click it and select **Explore**.</span></span>
4. <span data-ttu-id="d2305-127">**ファイル** を選択し、**管理者として Windows PowerShell を開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d2305-127">Select **File** and then select **Open Windows PowerShell as administrator**.</span></span>
5. <span data-ttu-id="d2305-128">コマンド `cmd .` を実行して、PowerShell ウィンドウでウィンドウ コマンド プロンプトを開きます。</span><span class="sxs-lookup"><span data-stu-id="d2305-128">Open the Windows Command Prompt in the PowerShell Window by running the command `cmd .`.</span></span>
6. <span data-ttu-id="d2305-129">コマンド `cd Extensions` を実行して、現在のディレクトリを拡張機能のルート ディレクトリに変更します。</span><span class="sxs-lookup"><span data-stu-id="d2305-129">Change the current directory to the extensions root directory by running the command `cd Extensions`.</span></span>
7. <span data-ttu-id="d2305-130">コマンド `set ExtensionPackageName=Contoso.Pos.Developer.Samples` を実行して、拡張機能パッケージの名前でセッション変数を作成</span><span class="sxs-lookup"><span data-stu-id="d2305-130">Create a session variable with the name of your extension package by running the command `set ExtensionPackageName=Contoso.Pos.Developer.Samples`</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2305-131">上記のコマンドの **Contoso.Pos.Developer.Samples** を POS 拡張機能パッケージの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d2305-131">Replace **Contoso.Pos.Developer.Samples** in the command above with the name of your POS extension package.</span></span> <span data-ttu-id="d2305-132">拡張機能パッケージ名は、POS 拡張機能パッケージを構成する Commerce Runtime トリガー拡張機能の **ExtensionPackageDefinition** で指定された名前と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2305-132">The extension package name must match the name specified in the **ExtensionPackageDefinition** in the Commerce Runtime trigger extension that configures the POS extension package.</span></span>

8. <span data-ttu-id="d2305-133">コマンド `set AbsolutePathToExtensionPackageProject=%FullPathToPOSExtensionProjectRootDirectory%` を実行して、POS 拡張機能パッケージ プロジェクト ディレクトリへの絶対パスを使用してセッション変数を作成</span><span class="sxs-lookup"><span data-stu-id="d2305-133">Create a session variable with the absolute path to your POS extension package project directory by running the command `set AbsolutePathToExtensionPackageProject=%FullPathToPOSExtensionProjectRootDirectory%`</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2305-134">**%FullPathToPOSExtensionProjectRootDirectory%** を POS 拡張機能パッケージ プロジェクトへの絶対パスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d2305-134">Replace **%FullPathToPOSExtensionProjectRootDirectory%** with the absolute path to your POS Extension Package project.</span></span>

    <span data-ttu-id="d2305-135">例: </span><span class="sxs-lookup"><span data-stu-id="d2305-135">Example:</span></span>

    ```powershell
    set AbsolutePathToExtensionPackageProject=K:\RetailCloudPos\WebRoot\Extensions\ Contoso.Pos.Developer.Samples
    ```

9. <span data-ttu-id="d2305-136">次のコマンドを実行して、拡張機能ディレクトリから拡張機能パッケージ プロジェクトのルート ディレクトリへのリンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="d2305-136">Create a link from the Extensions directory to the extension package project root directory by running the command:</span></span>

    ```powershell
     mklink /D %ExtensionPackageName% %AbsolutePathToExtensionPackageProject%
    ```

10. <span data-ttu-id="d2305-137">拡張機能パッケージのリンク フォルダーが Cloud POS 拡張機能パッケージ ディレクトリに作成されているかどうかを確認します。次の画像のようになります。</span><span class="sxs-lookup"><span data-stu-id="d2305-137">Verify the whether the link folder for your extension package is created in the Cloud POS extension package directory looks like the image below.</span></span>

## <a name="debugging-cloud-pos-using-edge-developer-tools"></a><span data-ttu-id="d2305-138">Edge 開発者ツールを使用した Cloud POS のデバッグ</span><span class="sxs-lookup"><span data-stu-id="d2305-138">Debugging Cloud POS using Edge developer tools</span></span>

1. <span data-ttu-id="d2305-139">[Cloud POS 拡張機能の開発環境の構成](#configure-cloud-pos) の手順を完了しました。</span><span class="sxs-lookup"><span data-stu-id="d2305-139">Completed the steps in [Configuring the Cloud POS extension development environment](#configure-cloud-pos).</span></span>
2. <span data-ttu-id="d2305-140">Cloud POS 拡張機能プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="d2305-140">Build your Cloud POS extension project.</span></span>
3. <span data-ttu-id="d2305-141">Edge の Cloud POS Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="d2305-141">Navigate to the Cloud POS website in Edge.</span></span>
4. <span data-ttu-id="d2305-142">F12 キーを押し、Edge 開発者ツールを起動します。</span><span class="sxs-lookup"><span data-stu-id="d2305-142">Press F12 to launch the Edge developer tools.</span></span>
5. <span data-ttu-id="d2305-143">Cloud POS 拡張機能パッケージのルート ディレクトリを指すワークスペースを設定します。</span><span class="sxs-lookup"><span data-stu-id="d2305-143">Set up a workspace that points to the root directory of your Cloud POS Extension package.</span></span> <span data-ttu-id="d2305-144">ワークスペースを設定するのは最初だけです。</span><span class="sxs-lookup"><span data-stu-id="d2305-144">You only have to setup the workspace the first time.</span></span>
6. <span data-ttu-id="d2305-145">**JavaScript ソース マッピング** が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d2305-145">Make sure that **JavaScript Source Mapping** is enabled.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: POS 拡張機能のデバッグ
description: このトピックでは、販売時点管理 (POS) 拡張機能のデバッグ方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: d0a1017b983bb22a390b3d975adfd0d3516a36b6
ms.sourcegitcommit: d84329f903d359ae042e8c0a4594982a7e06756f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2021
ms.locfileid: "5984232"
---
# <a name="debug-pos-extensions"></a><span data-ttu-id="a4189-103">POS 拡張機能のデバッグ</span><span class="sxs-lookup"><span data-stu-id="a4189-103">Debug POS extensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4189-104">このトピックでは、販売時点管理 (POS) 拡張機能のデバッグ方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a4189-104">This topic explains how to debug Point of Sale (POS) extensions.</span></span> <span data-ttu-id="a4189-105">Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="a4189-105">It applies to version 10.0.18 and later of the Retail software development kit (SDK).</span></span>

## <a name="debug-modern-pos-by-using-visual-studio-2017"></a><span data-ttu-id="a4189-106">Visual Studio 2017 を使用した Modern POS のデバッグ</span><span class="sxs-lookup"><span data-stu-id="a4189-106">Debug Modern POS by using Visual Studio 2017</span></span>

<span data-ttu-id="a4189-107">次の手順に従って拡張機能をデバッグします。</span><span class="sxs-lookup"><span data-stu-id="a4189-107">Follow these steps to debug your extension.</span></span>

1. <span data-ttu-id="a4189-108">シールドされた MPOS インストーラーを使用して、開発マシンでシールドされた Modern POS をインストールします。</span><span class="sxs-lookup"><span data-stu-id="a4189-108">Install Sealed Modern POS (MPOS) on the development machine by using the Sealed MPOS installer.</span></span>
2. <span data-ttu-id="a4189-109">デスクトップ上のショートカットをクリックして Universal Windows Platform (UWP) アプリをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a4189-109">Install the Universal Windows Platform (UWP) app by selecting the shortcut on the desktop.</span></span>
3. <span data-ttu-id="a4189-110">Microsoft Visual Studio で、MPOS 拡張機能パッケージ プロジェクト (JavaScript プロジェクト ファイル \[.jsproj file\]) を構築します。</span><span class="sxs-lookup"><span data-stu-id="a4189-110">In Microsoft Visual Studio, build your MPOS extension package project (the JavaScript project file \[.jsproj file\]).</span></span>
4. <span data-ttu-id="a4189-111">MPOS 拡張機能パッケージを配置します。</span><span class="sxs-lookup"><span data-stu-id="a4189-111">Deploy your MPOS extension package.</span></span> <span data-ttu-id="a4189-112">ソリューション エクスプローラーで、MPOS .jsproj ファイルを選択したまま (または右クリック) にして、**配置** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4189-112">In Solution Explorer, select and hold (or right-click) the MPOS .jsproj file, and then select **Deploy**.</span></span>
5. <span data-ttu-id="a4189-113">デバッガーが関連付けられるように POS を開きます。</span><span class="sxs-lookup"><span data-stu-id="a4189-113">Open POS so that the debugger is attached:</span></span>

    1. <span data-ttu-id="a4189-114">**デバッグ** メニューで、**その他のデバッグ ターゲット &gt; インストールされたアプリ パッケージをデバッグする**。</span><span class="sxs-lookup"><span data-stu-id="a4189-114">On the **Debug** menu, select **Other Debug Targets &gt; Debug Installed App Package**.</span></span>
    2. <span data-ttu-id="a4189-115">**Commerce Modern POS** を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="a4189-115">Search for and select **Commerce Modern POS**.</span></span>
    3. <span data-ttu-id="a4189-116">**開始** を選択すると、アプリケーションが開きます。</span><span class="sxs-lookup"><span data-stu-id="a4189-116">Select **Start** to open the app.</span></span>

## <a name="run-and-debug-cloud-pos"></a><span data-ttu-id="a4189-117">Cloud POS の実行およびデバッグ</span><span class="sxs-lookup"><span data-stu-id="a4189-117">Run and debug Cloud POS</span></span>

### <a name="configure-the-cloud-pos-extension-development-environment"></a><a name="configure-cloud-pos"></a><span data-ttu-id="a4189-118">Cloud POS 拡張機能の開発環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a4189-118">Configure the Cloud POS extension development environment</span></span>

<span data-ttu-id="a4189-119">拡張機能パッケージがマシン上で初めて開発されたとき、またはリンクが削除された場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a4189-119">Follow these steps the first time that an extension package is developed on the machine or if the link is deleted.</span></span> <span data-ttu-id="a4189-120">Cloud POS (CPOS) **拡張機能** ディレクトリに、拡張機能パッケージ ルート ディレクトリへのディレクトリ シンボル リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="a4189-120">In the Cloud POS (CPOS) **Extensions** directory, create a directory symbolic link to the root directory of the extension package.</span></span>

1. <span data-ttu-id="a4189-121">CPOS がマシンに配置されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a4189-121">Make sure that CPOS is deployed on the machine.</span></span> <span data-ttu-id="a4189-122">配置されていない場合は、Commerce Scale Unit (自己ホスト) インストーラーを使用して配置します。</span><span class="sxs-lookup"><span data-stu-id="a4189-122">If it isn't deployed, use the Commerce Scale Unit (self-hosted) installer to deploy it.</span></span>
2. <span data-ttu-id="a4189-123">インターネット インフォメーション サービス (IIS) を開きます。</span><span class="sxs-lookup"><span data-stu-id="a4189-123">Open Internet Information Services (IIS).</span></span> <span data-ttu-id="a4189-124">**Windows ロゴ キーと R キー** を同時に押して、**実行** ダイアログ ボックスに **inetmgr** と入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4189-124">Select **Windows logo key+R** to open the **Run** dialog box, enter **inetmgr**, and then select **OK**.</span></span>
3. <span data-ttu-id="a4189-125">**サイト** を展開し、**RetailCloudPos** を選択したまま (または右クリック) にして、**エクスプローラー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4189-125">Expand **Sites**, select and hold (or right-click) **RetailCloudPos**, and then select **Explore**.</span></span>
4. <span data-ttu-id="a4189-126">**ファイル** を選択し、**管理者として Windows PowerShell を開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4189-126">Select **File**, and then select **Open Windows PowerShell as administrator**.</span></span>
5. <span data-ttu-id="a4189-127">**Windows PowerShell** ウィンドウで次のコマンドを実行し、Windows コマンド プロンプトを開きます。</span><span class="sxs-lookup"><span data-stu-id="a4189-127">In the **Windows PowerShell** window, run the following command to open a Windows command prompt.</span></span>

    ```powershell
    cmd .
    ```

6. <span data-ttu-id="a4189-128">次のコマンド を実行して、現在のディレクトリを **拡張機能** のルート ディレクトリに変更します。</span><span class="sxs-lookup"><span data-stu-id="a4189-128">Run the following command to change the current directory to the **Extensions** root directory.</span></span>

   ```powershell
   cd Extensions
   ```

7. <span data-ttu-id="a4189-129">次のコマンドを実行して、拡張機能パッケージの名前を持つセッション変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="a4189-129">Run the following command to create a session variable that has the name of your extension package.</span></span>

    ```powershell
    set ExtensionPackageName=Contoso.Pos.Developer.Samples
    ```

    > [!NOTE]
    > <span data-ttu-id="a4189-130">**Contoso.Pos.Developer.Samples** を POS 拡張機能パッケージの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a4189-130">Replace **Contoso.Pos.Developer.Samples** with the name of your POS extension package.</span></span> <span data-ttu-id="a4189-131">拡張機能パッケージ名は、POS 拡張機能パッケージを構成する Commerce Runtime  CRT トリガー拡張機能の **ExtensionPackageDefinition** で指定された名前と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4189-131">The name of the extension package must match the name that is specified in **ExtensionPackageDefinition** in the Commerce runtime (CRT) trigger extension that configures the POS extension package.</span></span>

8. <span data-ttu-id="a4189-132">次のコマンドを実行して、POS 拡張機能パッケージ プロジェクト ディレクトリへの絶対パスを持つセッション変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="a4189-132">Run the following command to create a session variable that has the absolute path of the directory for your POS extension package project.</span></span>

    ```powershell
    set AbsolutePathToExtensionPackageProject=%FullPathToPOSExtensionProjectRootDirectory%
    ```

    > [!NOTE]
    > <span data-ttu-id="a4189-133">**%FullPathToPOSExtensionProjectRootDirectory%** を POS 拡張機能パッケージ プロジェクトへの絶対パスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a4189-133">Replace **%FullPathToPOSExtensionProjectRootDirectory%** with the absolute path of your POS extension package project.</span></span> <span data-ttu-id="a4189-134">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="a4189-134">Here is an example.</span></span>
    >
    > ```powershell
    > set AbsolutePathToExtensionPackageProject=K:\RetailCloudPos\WebRoot\Extensions\ Contoso.Pos.Developer.Samples
    > ```

9. <span data-ttu-id="a4189-135">次のコマンドを実行して、**拡張機能** ディレクトリから拡張機能パッケージ プロジェクトのルート ディレクトリへのリンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="a4189-135">Run the following command to create a link from the **Extensions** directory to the root directory of the extension package project.</span></span>

    ```powershell
    mklink /D %ExtensionPackageName% %AbsolutePathToExtensionPackageProject%
    ```

10. <span data-ttu-id="a4189-136">拡張機能パッケージのリンク フォルダーが CPOS 拡張機能パッケージ ディレクトリに作成されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a4189-136">Verify that the linked folder for your extension package is created in the directory for the CPOS extension package.</span></span>

## <a name="debug-cpos-by-using-the-microsoft-edge-developer-tools"></a><span data-ttu-id="a4189-137">Microsoft Edge 開発者ツールを使用した CPOS のデバッグ</span><span class="sxs-lookup"><span data-stu-id="a4189-137">Debug CPOS by using the Microsoft Edge developer tools</span></span>

1. <span data-ttu-id="a4189-138">このトピックで前述されている [Cloud POS 拡張機能の開発環境のコンフィギュレーション](#configure-cloud-pos) セクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a4189-138">Follow the steps in the [Configure the Cloud POS extension development environment](#configure-cloud-pos) section earlier in this topic.</span></span>
2. <span data-ttu-id="a4189-139">CPOS 拡張機能プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="a4189-139">Build your CPOS extension project.</span></span>
3. <span data-ttu-id="a4189-140">Microsoft Edge で、CPOS Web サイトを開きます。</span><span class="sxs-lookup"><span data-stu-id="a4189-140">In Microsoft Edge, open the CPOS website.</span></span>
4. <span data-ttu-id="a4189-141">**F12** キーを選択して、Microsoft Edge 開発者ツールを開きます。</span><span class="sxs-lookup"><span data-stu-id="a4189-141">Select the **F12** key to open the Microsoft Edge developer tools.</span></span>
5. <span data-ttu-id="a4189-142">CPOS 拡張機能パッケージのルート ディレクトリを指すワークスペースを設定します。</span><span class="sxs-lookup"><span data-stu-id="a4189-142">Set up a workspace that points to the root directory of your CPOS extension package.</span></span> <span data-ttu-id="a4189-143">この手順を初めて実行する場合は、ワークスペースを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4189-143">You have to set up the workspace only the first time that you complete this procedure.</span></span>
6. <span data-ttu-id="a4189-144">**JavaScript ソース マッピング** が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a4189-144">Make sure that **JavaScript Source Mapping** is enabled.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Modern POS 拡張パッケージの .appx ファイルの作成
description: このトピックでは、Microsoft Visual Studio 2017 を使用して、Modern 販売時点管理 (MPOS) のパッケージ プロジェクトの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 820410933035d80b137fe4415bfb2c2be49d6588
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193688"
---
# <a name="create-an-appx-file-for-a-modern-pos-extension-package"></a><span data-ttu-id="8be75-103">Modern POS 拡張パッケージの .appx ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="8be75-103">Create an .appx file for a Modern POS extension package</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8be75-104">このトピックでは、 Visual Studio 2017 を使用して、Modern 販売時点管理 (MPOS) のパッケージ プロジェクトの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8be75-104">This topic explains how to create a Modern Point of Sale (MPOS) packaging project by using Visual Studio 2017.</span></span> <span data-ttu-id="8be75-105">これらの手順は、MPOS の拡張機能を開発する場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="8be75-105">These steps are required only if you're developing extensions for MPOS.</span></span> <span data-ttu-id="8be75-106">MPOS 拡張機能パッケージ プロジェクトは、MPOS アプリを拡張する[MSIX Windows アプリ パッケージ](/windows/msix/overview) を生成します。</span><span class="sxs-lookup"><span data-stu-id="8be75-106">The MPOS extension packaging project generates the [MSIX Windows app package](/windows/msix/overview) that will extend the MPOS app.</span></span>

1. <span data-ttu-id="8be75-107">新しい JavaScript Universal Windows Platform (UWP) アプリ プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="8be75-107">Create a new JavaScript Universal Windows Platform (UWP) app project:</span></span>

    1. <span data-ttu-id="8be75-108">ソリューション エクスプローラーで、ソリューションを保留 (または右クリック)し、**追加** から **新しいプロジェクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-108">In Solution Explorer, select and hold (or right-click) the solution, select **Add**, and then select **New Project**.</span></span>
    2. <span data-ttu-id="8be75-109">**Windows JavaScript** を検索し、**空白のアプリ (Universal Windows)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-109">Find **Windows JavaScript**, and select **Blank App (Universal Windows)**.</span></span>
    3. <span data-ttu-id="8be75-110">プロジェクトに **ModernPos** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="8be75-110">Name the project **ModernPos**.</span></span>
    4. <span data-ttu-id="8be75-111">**ターゲット バージョン** フィールドを **Windows 10、バージョン 1809 (10.0; ビルド 17763)** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8be75-111">Set the **Target version** field to **Windows 10, version 1809 (10.0; Build 17763)**.</span></span>
    5. <span data-ttu-id="8be75-112">**ミニマム バージョン** フィールドを **Windows 10、バージョン 1809 (10.0; ビルド 17763)** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8be75-112">Set the **Minimum version** field to **Windows 10, version 1809 (10.0; Build 17763)**.</span></span>

2. <span data-ttu-id="8be75-113">生成される次のソース フォルダおよびファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="8be75-113">Delete the following source folders and files that are generated:</span></span>

    + <span data-ttu-id="8be75-114">**js** フォルダー</span><span class="sxs-lookup"><span data-stu-id="8be75-114">**js** folder</span></span>
    + <span data-ttu-id="8be75-115">**css** フォルダー</span><span class="sxs-lookup"><span data-stu-id="8be75-115">**css** folder</span></span>
    + <span data-ttu-id="8be75-116">**index.html** ファイル</span><span class="sxs-lookup"><span data-stu-id="8be75-116">**index.html** file</span></span>
    + <span data-ttu-id="8be75-117">**package.appxmanifest** ファイル</span><span class="sxs-lookup"><span data-stu-id="8be75-117">**package.appxmanifest** file</span></span>

    > [!NOTE]
    > <span data-ttu-id="8be75-118">交換するロゴが含まれる場合に限り、アプリ パッケージのロゴとして使用する画像ファイル (**images\\StoreLogo.png**) は削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="8be75-118">Don't delete the image file that is used as the logo for the app package (**images\\StoreLogo.png**), unless you include a replacement logo.</span></span>

3. <span data-ttu-id="8be75-119">プロジェクトを編集し、カスタマイズ パッケージ用に作成されたプロパティ (.props) ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="8be75-119">Edit the project, and import the properties (.props) file that was created for the customization package.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8be75-120">**package.appxmanifest** ファイルの世代は、カスタマイズ パッケージの .props ファイルによって異なります。</span><span class="sxs-lookup"><span data-stu-id="8be75-120">Generation of the **package.appxmanifest** file depends on the properties from the customization package's .props file.</span></span> <span data-ttu-id="8be75-121">.props ファイルをプロジェクトにインポートすることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8be75-121">Make sure that you import the .props file into the project.</span></span>

4. <span data-ttu-id="8be75-122">POS SDK NuGet パッケージへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="8be75-122">Add a reference to the POS SDK NuGet package:</span></span>

    1. <span data-ttu-id="8be75-123">ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**NuGet パッケージの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-123">In Solution Explorer, select and hold (or right-click) the project, and then select **Manage NuGet packages**.</span></span>
    2. <span data-ttu-id="8be75-124">**NuGet パッケージ マネージャー** ウィンドウの **閲覧** タブで、**Microsoft.Dynamics.Commerce.Sdk.Pos** を検索します。</span><span class="sxs-lookup"><span data-stu-id="8be75-124">In the **NuGet Package Manager** window, on the **Browse** tab, search for **Microsoft.Dynamics.Commerce.Sdk.Pos**.</span></span>
    3. <span data-ttu-id="8be75-125">パッケージを選択し、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-125">Select the package, and then select **Install**.</span></span>

5. <span data-ttu-id="8be75-126">ソリューション コンフィギュレーションを更新して、x86 プラットフォームのみをターゲットとします。</span><span class="sxs-lookup"><span data-stu-id="8be75-126">Update the solution configuration so that it targets only x86 platforms:</span></span>

    1. <span data-ttu-id="8be75-127">ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-127">In Solution Explorer, select and hold (or right-click) the project, and then select **Properties**.</span></span>
    2. <span data-ttu-id="8be75-128">構成マネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="8be75-128">Open Configuration Manager.</span></span>
    3. <span data-ttu-id="8be75-129">**有効なソリューション プラットフォーム** メニューで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-129">On the **Active solution platform** menu, select **Edit**.</span></span>
    4. <span data-ttu-id="8be75-130">**x86** を除くすべてのプラットフォームを削除します。</span><span class="sxs-lookup"><span data-stu-id="8be75-130">Remove all platforms except **x86**.</span></span>

    ![プラットフォーム コンフィギュレーション](media/platform.png)

6. <span data-ttu-id="8be75-132">サポートされていないプラットフォーム コンフィギュレーションを削除するには、JavaScript プロジェクト ファイル (.jsproj ファイル) を編集してください。</span><span class="sxs-lookup"><span data-stu-id="8be75-132">Edit the JavaScript project file (.jsproj file) file to remove unsupported platform configurations:</span></span>

    1. <span data-ttu-id="8be75-133">プロジェクト ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="8be75-133">Save the project file.</span></span>
    2. <span data-ttu-id="8be75-134">ソリューション エクスプローラを使用してプロジェクトをアンロードします。</span><span class="sxs-lookup"><span data-stu-id="8be75-134">Unload the project by using Solution Explorer.</span></span>
    3. <span data-ttu-id="8be75-135">ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-135">In Solution Explorer, select and hold (or right-click) the project, and then select **Edit**.</span></span>
    4. <span data-ttu-id="8be75-136">**x86** を除くすべてのプラットフォームが含まれる **ProjectConfiguration** を削除します。</span><span class="sxs-lookup"><span data-stu-id="8be75-136">Delete the **ProjectConfiguration** includes for all platforms except **x86**.</span></span> <span data-ttu-id="8be75-137">完了すると、**ProjectConfiguration** エレメントは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="8be75-137">When you've finished, the **ProjectConfiguration** elements should resemble the following example.</span></span>

        ```xml
        <ItemGroup Label="ProjectConfigurations">
            <ProjectConfiguration Include="Debug|x86">
                <Configuration>Debug</Configuration>
                <Platform>x86</Platform>
            </ProjectConfiguration>
            <ProjectConfiguration Include="Release|x86">
                <Configuration>Release</Configuration>
                <Platform>x86</Platform>
                <UseDotNetNativeToolchain>true</UseDotNetNativeToolchain>
            </ProjectConfiguration>
        </ItemGroup>
        ```

    5. <span data-ttu-id="8be75-138">プロジェクトをリロードします。</span><span class="sxs-lookup"><span data-stu-id="8be75-138">Reload the project.</span></span>

7. <span data-ttu-id="8be75-139">参照を MPOS .jsproj ファイルから以前作成した **POS. 拡張機能パッケージ** プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="8be75-139">Add a reference from the MPOS .jsproj file to the **POS.Extension Package** project that you created earlier:</span></span>

    1. <span data-ttu-id="8be75-140">ソリューション エクスプローラーで、MPOS プロジェクトを保留 (または右クリック)し、**追加** から **参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-140">In Solution Explorer, select and hold (or right-click) the MPOS project, select **Add**, and then select **Reference**.</span></span>
    2. <span data-ttu-id="8be75-141">照会マネージャーの左側の **プロジェクト** タブで、以前作成した **POS 拡張機能パッケージ** プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-141">On the **Projects** tab on the left side of Reference Manager, select the **POS Extension Package** project that you created earlier.</span></span>
    3. <span data-ttu-id="8be75-142">サポートされていない参照を確認するメッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-142">When you're prompted to confirm the unsupported reference, select **Yes**.</span></span>

8. <span data-ttu-id="8be75-143">ソリューションに Commerce Runtime (CRT) 拡張機能プロジェクトが含まれている場合、プロジェクト参照をソリューションの各 CRT 拡張機能プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="8be75-143">If your solution contains Commerce runtime (CRT) extension projects, add project references to each CRT extension project in the solution:</span></span>

    1. <span data-ttu-id="8be75-144">ソリューション エクスプローラーで、MPOS プロジェクトを保留 (または右クリック)し、**追加** から **参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-144">In Solution Explorer, select and hold (or right-click) the MPOS project, select **Add**, and then select **Reference**.</span></span>
    2. <span data-ttu-id="8be75-145">参照マネージャーの左側の **プロジェクト** タブで、CRT 拡張機能プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-145">On the **Projects** tab on the left side of Reference Manager, select the CRT extension projects.</span></span>

9. <span data-ttu-id="8be75-146">ソリューションに Hardware Station 拡張機能プロジェクトが含まれている場合は、ソリューションで各 Hardware Station 拡張機能プロジェクトにプロジェクト参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="8be75-146">If your solution contains Hardware Station extension projects, add project references to each Hardware Station extension project in the solution:</span></span>

    1. <span data-ttu-id="8be75-147">ソリューション エクスプローラーで、MPOS プロジェクトを保留 (または右クリック)し、**追加** から **参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-147">In Solution Explorer, select and hold (or right-click) the MPOS project, select **Add**, and then select **Reference**.</span></span>
    2. <span data-ttu-id="8be75-148">参照マネージャーの左側の **プロジェクト** タブで、Hardware Station 拡張機能プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="8be75-148">On the **Projects** tab on the left side of Reference Manager, select the Hardware Station extension projects.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

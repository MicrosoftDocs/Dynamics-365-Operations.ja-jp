---
title: Modern POS 拡張パッケージ appx ファイルの作成
description: このトピックでは、Visual Studio 2017 を使用した Modern POS のパッケージ プロジェクトの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 68f77ab9a2c821828e3ec397b84da98aeb0bc104
ms.sourcegitcommit: fd15b02fc9caa1c05e56abdc276a7f4b23b0d8f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5960155"
---
# <a name="create-a-modern-pos-extension-package-appx-file"></a><span data-ttu-id="34451-103">Modern POS 拡張パッケージ appx ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="34451-103">Create a Modern POS extension package appx file</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34451-104">次の手順では、Visual Studio 2017 を使用して Modern POS のパッケージ プロジェクトを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="34451-104">The following steps show you how to create a Modern POS packaging project using Visual Studio 2017.</span></span> <span data-ttu-id="34451-105">これらの手順は、Modern POS の拡張機能を開発する場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="34451-105">These steps are only required if you are developing extensions for Modern POS.</span></span> <span data-ttu-id="34451-106">Modern POS 拡張機能パッケージ プロジェクトは、Modern POS アプリを拡張する[MSIX Windows アプリ パッケージ](https://docs.microsoft.com/windows/msix/overview) を生成します。</span><span class="sxs-lookup"><span data-stu-id="34451-106">The Modern POS extension packaging project generates the [MSIX Windows app package](https://docs.microsoft.com/windows/msix/overview) that will extend the Modern POS app.</span></span>

1. <span data-ttu-id="34451-107">次の手順に従って、新しい JavaScript Universal Windows Platform アプリ プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="34451-107">Create a new JavaScript Universal Windows Platform App project by following these steps:</span></span>

    1. <span data-ttu-id="34451-108">ソリューション エクスプローラーで、ソリューションを右クリックし、**追加** を選択してから **新しいプロジェクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-108">Right-click the solution in Solution explorer and select **Add** and then **New Project**.</span></span> <span data-ttu-id="34451-109">**Windows JavaScript** を検索し、**空白のアプリ (Universal Windows)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-109">Find **Windows JavaScript** and select **Blank App (Universal Windows)**.</span></span> <span data-ttu-id="34451-110">プロジェクトに **ModernPos** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="34451-110">Name the project **ModernPos**.</span></span>
    2. <span data-ttu-id="34451-111">**ターゲット バージョン** を **Windows 10、バージョン 1809 (10.0; ビルド 17763)** に設定します。</span><span class="sxs-lookup"><span data-stu-id="34451-111">Set **Target version** to **Windows 10, version 1809 (10.0; Build 17763)**.</span></span>
    3. <span data-ttu-id="34451-112">**最小 バージョン** を **Windows 10、バージョン 1809 (10.0; ビルド 17763)** に設定します。</span><span class="sxs-lookup"><span data-stu-id="34451-112">Set **Minimum version** to **Windows 10, version 1809 (10.0; Build 17763)**.</span></span>

2. <span data-ttu-id="34451-113">生成されたソース フォルダーおよびファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="34451-113">Delete these generated source folders and files:</span></span>

    + <span data-ttu-id="34451-114">**js** フォルダー。</span><span class="sxs-lookup"><span data-stu-id="34451-114">**js** folder.</span></span>
    + <span data-ttu-id="34451-115">**css** フォルダー。</span><span class="sxs-lookup"><span data-stu-id="34451-115">**css** folder.</span></span>
    + <span data-ttu-id="34451-116">**index.html** ファイル。</span><span class="sxs-lookup"><span data-stu-id="34451-116">**index.html** file.</span></span>
    + <span data-ttu-id="34451-117">**package.appxmanifest** ファイル。</span><span class="sxs-lookup"><span data-stu-id="34451-117">**package.appxmanifest** file.</span></span>

    > [!NOTE]
    > <span data-ttu-id="34451-118">交換するロゴが含まれる場合に限り、アプリ パッケージのロゴとして使用する画像ファイル (**images\\StoreLogo.png**) は削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="34451-118">Don't delete the image file used as the logo for the app package (**images\\StoreLogo.png**) unless you include a replacement logo.</span></span>

3. <span data-ttu-id="34451-119">プロジェクトを編集し、上記の手順で作成したカスタマイズ パッケージ **props** ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="34451-119">Edit the project and import the customization package **props** file created in the steps above.</span></span>

    > [!NOTE]
    > <span data-ttu-id="34451-120">**package.appxmanifest** ファイルの生成は、カスタマイズ パッケージ **props** ファイルのプロパティによって異なります。</span><span class="sxs-lookup"><span data-stu-id="34451-120">Generating the **package.appxmanifest** file depends on the properties from the customization package **props** file.</span></span> <span data-ttu-id="34451-121">プロジェクトにインポートする必要があります。\*\*</span><span class="sxs-lookup"><span data-stu-id="34451-121">Make sure that you import it into the project.\*\*</span></span>

4. <span data-ttu-id="34451-122">POS SDK NuGet パッケージへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="34451-122">Add a reference to the POS SDK NuGet Package.</span></span>

    1. <span data-ttu-id="34451-123">プロジェクト ソリューション エクスプローラーを選択し、**NuGet パッケージの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-123">Right-click the project Solution Explorer and select **Manage NuGet packages**.</span></span>
    2. <span data-ttu-id="34451-124">NuGet パッケージ マネージャー ウィンドウで **参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-124">Select the **Browse** tab in the NuGet Package Manager window.</span></span>
    3. <span data-ttu-id="34451-125">**Microsoft.Dynamics.Commerce.Sdk.Pos** を検索します。</span><span class="sxs-lookup"><span data-stu-id="34451-125">Search for **Microsoft.Dynamics.Commerce.Sdk.Pos**.</span></span>
    4. <span data-ttu-id="34451-126">パッケージを選択し、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-126">Select the package and select **Install**.</span></span>

5. <span data-ttu-id="34451-127">**x86** のみを対象とするようにソリューション コンフィギュレーションを更新します。</span><span class="sxs-lookup"><span data-stu-id="34451-127">Update the solution configuration to target only **x86**.</span></span>

    1. <span data-ttu-id="34451-128">プロジェクト ソリューション エクスプローラーを選択し、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-128">Right-click the project Solution Explorer and select **Properties**.</span></span>
    2. <span data-ttu-id="34451-129">構成マネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="34451-129">Open the Configuration Manager.</span></span>
    3. <span data-ttu-id="34451-130">**有効なソリューション プラットフォーム** ドロップダウンで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-130">In the **Active solution platform** drop-down, select **Edit**.</span></span>
    4. <span data-ttu-id="34451-131">**x86** を除く他のすべてのプラットフォームを削除します。</span><span class="sxs-lookup"><span data-stu-id="34451-131">Remove all other platforms except for **x86**.</span></span>

         ![プラットフォーム コンフィギュレーション](media/platform.png)

6. <span data-ttu-id="34451-133">サポートされていないプラットフォーム コンフィギュレーションを削除するには、**jsproj** ファイルを編集してください。</span><span class="sxs-lookup"><span data-stu-id="34451-133">Edit the **jsproj** file to remove unsupported platform configurations.</span></span>

    1. <span data-ttu-id="34451-134">プロジェクト ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="34451-134">Save the project file.</span></span>
    2. <span data-ttu-id="34451-135">ソリューション エクスプローラを使用してプロジェクトをアンロードします。</span><span class="sxs-lookup"><span data-stu-id="34451-135">Unload the project using Solution Explorer.</span></span>
    3. <span data-ttu-id="34451-136">ソリューション エクスプローラーでプロジェクトを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-136">Right-click the project in Solution Explorer and select **Edit**.</span></span>
    4. <span data-ttu-id="34451-137">**x86** 以外のすべてのプラットフォームが含まれる **ProjectConfiguration** を削除します。</span><span class="sxs-lookup"><span data-stu-id="34451-137">Delete the **ProjectConfiguration** includes for all platforms other than **x86**.</span></span> <span data-ttu-id="34451-138">**ProjectConfigurations** は次の Xml のようになります。</span><span class="sxs-lookup"><span data-stu-id="34451-138">The **ProjectConfigurations** should look like the following Xml:</span></span>

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

    5. <span data-ttu-id="34451-139">プロジェクトをリロードします。</span><span class="sxs-lookup"><span data-stu-id="34451-139">Reload the project.</span></span>

7. <span data-ttu-id="34451-140">次の手順に従って、Modern POS **jsproj** から上記で作成した **POS.Extension パッケージ** プロジェクトへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="34451-140">Add a reference from the Modern POS **jsproj** to the **POS.Extension Package** project created above, by following these steps:</span></span>

    1. <span data-ttu-id="34451-141">ソリューション エクスプローラーで、Modern POS プロジェクトを右クリックし、**追加** を選択してから、**参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-141">Right-click the Modern POS project in Solution Explorer and select **Add** and then **Reference**.</span></span>
    2. <span data-ttu-id="34451-142">参照マネージャの左側にある **プロジェクト** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-142">Select the **Projects** tab on the left side of the Reference Manager.</span></span>
    3. <span data-ttu-id="34451-143">上記で **作成した POS 拡張機能パッケージ** プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-143">Select the **POS Extension Package** project created above.</span></span> <span data-ttu-id="34451-144">プロジェクトを選択すると、Visual Studio はサポートされていない参照を確認するように求めます。</span><span class="sxs-lookup"><span data-stu-id="34451-144">When you select the project, Visual Studio asks you confirm the unsupported reference.</span></span> <span data-ttu-id="34451-145">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-145">Select **Yes**.</span></span>

8. <span data-ttu-id="34451-146">ソリューションに Commerce Runtime 拡張機能プロジェクトが含まれている場合は、ソリューションで各 Commerce Runtime 拡張機能プロジェクトをプロジェクト参照に追加します。</span><span class="sxs-lookup"><span data-stu-id="34451-146">If your solution contains Commerce Runtime extension projects, then add project references to each of the Commerce Runtime extension projects in the solution.</span></span>

    1. <span data-ttu-id="34451-147">ソリューション エクスプローラーで、Modern POS を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="34451-147">Right-click the Modern POS project in Solution Explorer.</span></span> <span data-ttu-id="34451-148">**追加** を選択してから **参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-148">Select **Add** and then **Reference**.</span></span>
    2. <span data-ttu-id="34451-149">参照マネージャの左側にある **プロジェクト** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-149">Select the **Projects** tab on the left side of the Reference Manager.</span></span>
    3. <span data-ttu-id="34451-150">Commerce Runtime 拡張機能プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-150">Select the Commerce Runtime extension projects.</span></span>

9. <span data-ttu-id="34451-151">ソリューションに Hardware Station 拡張機能プロジェクトが含まれている場合は、ソリューションで各 Hardware Station 拡張機能プロジェクトをプロジェクト参照に追加します。</span><span class="sxs-lookup"><span data-stu-id="34451-151">If your solution contains Hardware Station extension projects, then add project references to each of the Hardware Station extension projects in the solution.</span></span>

    1. <span data-ttu-id="34451-152">ソリューション エクスプローラーで、Modern POS を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="34451-152">Right-click the Modern POS project in Solution Explorer.</span></span> <span data-ttu-id="34451-153">**追加** を選択してから **参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-153">Select **Add** and then **Reference**.</span></span>
    2. <span data-ttu-id="34451-154">参照マネージャの左側にある **プロジェクト** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-154">Select the **Projects** tab on the left side of the Reference Manager.</span></span>
    3. <span data-ttu-id="34451-155">Hardware Station の拡張機能プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="34451-155">Select the Hardware Station Extension projects.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

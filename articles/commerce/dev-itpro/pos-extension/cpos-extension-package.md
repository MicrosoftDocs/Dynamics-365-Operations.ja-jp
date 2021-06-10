---
title: Cloud POS 拡張機能パッケージの作成
description: このトピックでは、Cloud POS 拡張機能パッケージの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 66b567b98cda98e44646af95b946a03b39a1ff0e
ms.sourcegitcommit: 4c880b152e81350f023b944c2ab13e60498e2c7b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2021
ms.locfileid: "6093902"
---
# <a name="create-a-cloud-pos-extension-package"></a><span data-ttu-id="b1569-103">Cloud POS 拡張機能パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="b1569-103">Create a Cloud POS extension package</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="b1569-104">このトピックでは、Cloud POS 拡張機能パッケージの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1569-104">This topic explains how to create a Cloud POS extension package.</span></span> <span data-ttu-id="b1569-105">Cloud POS 配置トポロジに基づいて、Cloud POS を Cloud スケール ユニット (CSU) または Cloud スケール ユニット (CSU) – セルフ ホストに配置できます。</span><span class="sxs-lookup"><span data-stu-id="b1569-105">Based on the Cloud POS deployment topology, the Cloud POS can be deployed to Cloud Scale unit (CSU) or Cloud Scale unit (CSU) – Self hosted.</span></span>

## <a name="packaging-for-cloud-scale-unit-csu-cpos"></a><span data-ttu-id="b1569-106">Cloud スケール ユニット (CSU) CPOS のパッケージング</span><span class="sxs-lookup"><span data-stu-id="b1569-106">Packaging for Cloud Scale unit (CSU) CPOS</span></span>

<span data-ttu-id="b1569-107">CSU の配置パッケージは、**Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** パッケージを消費することで作成できます。</span><span class="sxs-lookup"><span data-stu-id="b1569-107">The deployment package for CSU can be created by consuming the **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** package.</span></span>

<span data-ttu-id="b1569-108">パッケージを作成するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b1569-108">Follow these steps to create the package:</span></span>

1. <span data-ttu-id="b1569-109">Visual Studio 2017 を開き、**ターゲット フレームワーク** で **.NET Standard 2.0** を設定して新しい C\# クラス ライブラリー プロジェクトを作成し、プロジェクト名を **ScaleUnit** に変更します。</span><span class="sxs-lookup"><span data-stu-id="b1569-109">Open Visual Studio 2017, create a new C\# class library project with the **Target framework** set to **.NET Standard 2.0**, and rename the project to **ScaleUnit**.</span></span>

2. <span data-ttu-id="b1569-110">生成された **クラス 1.cs** ファイルは削除します。</span><span class="sxs-lookup"><span data-stu-id="b1569-110">Delete the generated **Class1.cs** file.</span></span>

3. <span data-ttu-id="b1569-111">依存関係として **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** NuGet パッケージをプロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="b1569-111">Add the **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** NuGet package as a dependency to the project.</span></span>

4. <span data-ttu-id="b1569-112">**Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** NuGet バージョンを選択し、使用している SDK/アプリケーションのバージョンに一致させます。</span><span class="sxs-lookup"><span data-stu-id="b1569-112">Select the version of the **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** NuGet version to match your SDK/application version.</span></span> <span data-ttu-id="b1569-113">`https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json` から、**Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** パッケージを使用します。</span><span class="sxs-lookup"><span data-stu-id="b1569-113">Use the **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** package from `https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json`.</span></span> <span data-ttu-id="b1569-114">パッケージのソースの場所を拡張機能プロジェクト ファイルの **nuget.config** ファイルに追加できます。</span><span class="sxs-lookup"><span data-stu-id="b1569-114">You can add the package source location to the **nuget.config** file of your extension project file.</span></span>

5. <span data-ttu-id="b1569-115">プロジェクト参照として、**POS.Extension** プロジェクトを **ScaleUnit** プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="b1569-115">Add the **POS.Extension** project as a project reference to the **ScaleUnit** project.</span></span>

6. <span data-ttu-id="b1569-116">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="b1569-116">Compile and build the project.</span></span> <span data-ttu-id="b1569-117">このプロジェクトの出力には、CSU 配置パッケージが zip ファイルとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1569-117">The output of this project contains the CSU deployment package as a zip file.</span></span>

> [!NOTE]
> <span data-ttu-id="b1569-118">Commerce Runtime、Retail Server、またはデーターベース拡張機能がある場合は、すべての拡張機能のプロジェクトを参照として **ScaleUnit** プロジェクトに含みます。</span><span class="sxs-lookup"><span data-stu-id="b1569-118">If you have Commerce Runtime, Retail Server, or a Database extension then you must include all these extension projects as references to the **ScaleUnit** project.</span></span> <span data-ttu-id="b1569-119">これらのパッケージを追加すると、すべての拡張機能を含む複合配置パッケージが生成されます。</span><span class="sxs-lookup"><span data-stu-id="b1569-119">Adding them generates a combined deployment package that contains all your extensions.</span></span>

<span data-ttu-id="b1569-120">配置するには、[パッケージを CSU に配置](../retail-sdk/retail-sdk-packaging.md#deploy-the-package-to-csu) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b1569-120">To deploy, follow the steps in [Deploy the package to CSU](../retail-sdk/retail-sdk-packaging.md#deploy-the-package-to-csu).</span></span>

## <a name="packaging-for-cloud-scale-unit--self-hosted-cpos"></a><span data-ttu-id="b1569-121">Cloud スケール ユニット – セルフ ホスト CPOS のパッケージング</span><span class="sxs-lookup"><span data-stu-id="b1569-121">Packaging for Cloud Scale unit – Self hosted CPOS</span></span>

<span data-ttu-id="b1569-122">CSU の配置パッケージは、**Microsoft.Dynamics.Commerce.Sdk.Installers.ScaleUnit** パッケージを消費することで作成できます。</span><span class="sxs-lookup"><span data-stu-id="b1569-122">The deployment package for CSU can be created by consuming the **Microsoft.Dynamics.Commerce.Sdk.Installers.ScaleUnit** package.</span></span>

1. <span data-ttu-id="b1569-123">Visual Studio 2017 を開いて新しいコンソール アプリケーション (.NET Core) を作成し、**ScaleUnit.Installer** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="b1569-123">Open Visual Studio 2017, create a new console application (.NET Core), and name it **ScaleUnit.Installer**.</span></span>

2. <span data-ttu-id="b1569-124">.proj ファイルを編集し、**ターゲット フレームワーク** を **.NET Framework 4.6.1** へ変更します。</span><span class="sxs-lookup"><span data-stu-id="b1569-124">Edit the .proj file and change the **Target Framework** to **.NET Framework 4.6.1**.</span></span> <span data-ttu-id="b1569-125">Xml は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="b1569-125">The Xml looks like this:</span></span>

    ```xml
    <Project Sdk="Microsoft.NET.Sdk">
        <PropertyGroup>
            <OutputType>Exe</OutputType>
            <TargetFramework>net461</TargetFramework>
        </PropertyGroup>
    </Project>
    ```

3. <span data-ttu-id="b1569-126">生成された **Program.cs** ファイルは削除します。</span><span class="sxs-lookup"><span data-stu-id="b1569-126">Delete the generated **Program.cs** file.</span></span>

4. <span data-ttu-id="b1569-127">Installer SDK NuGet パッケージへの参照を追加</span><span class="sxs-lookup"><span data-stu-id="b1569-127">Add a reference to the Installer SDK NuGet Package</span></span>

    1. <span data-ttu-id="b1569-128">ソリューション エクスプローラーのプロジェクトを選択し、**NuGet パッケージの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1569-128">Right-click the project in Solution Explorer and select **Manage NuGet packages**.</span></span>
    2. <span data-ttu-id="b1569-129">NuGet パッケージ マネージャー ウィンドウで **参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1569-129">Select the **Browse** tab in the NuGet Package Manager window.</span></span>
    3. <span data-ttu-id="b1569-130">**Microsoft.Dynamics.Commerce.Sdk.Installers.ScaleUnit** を検索します。</span><span class="sxs-lookup"><span data-stu-id="b1569-130">Search for **Microsoft.Dynamics.Commerce.Sdk.Installers.ScaleUnit**.</span></span>
    4. <span data-ttu-id="b1569-131">パッケージを選択し、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1569-131">Select the package and then select **Install**.</span></span>
    5. <span data-ttu-id="b1569-132">Go-Live バージョンと一致するバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1569-132">Select the version that matches your go-live version.</span></span>

5. <span data-ttu-id="b1569-133">上記のとおりに作成した POS.Extension プロジェクトへ、**ScaleUnit.Installer** プロジェクトから参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="b1569-133">Add a reference from the **ScaleUnit.Installer** project to the POS.Extension project created above.</span></span>

    1. <span data-ttu-id="b1569-134">Solution Explorer で **ScaleUnit.Installer** プロジェクトを右クリックして、**追加** から **参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1569-134">Right-click the **ScaleUnit.Installer** project in the Solution Explorer, select **Add** and then **Reference**.</span></span>
    2. <span data-ttu-id="b1569-135">参照マネージャの左側にある **プロジェクト** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1569-135">Select the **Projects** tab on the left side of the Reference Manager.</span></span>
    3. <span data-ttu-id="b1569-136">上記で作成した POS.Extension プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1569-136">Select the POS.Extension project created above.</span></span>

6. <span data-ttu-id="b1569-137">**Extension.Config** ファイルをプロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="b1569-137">Add the **Extension.Config** file to the project.</span></span>

    1. <span data-ttu-id="b1569-138">プロジェクトを右クリックし、**追加** から **新しい項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1569-138">Right-click the project and select **Add** and then **New Item**.</span></span>
    2. <span data-ttu-id="b1569-139">**アプリケーション構成ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1569-139">Select **Application Configuration File**.</span></span>
    3. <span data-ttu-id="b1569-140">**Extension.Config** 名のファイルを作成し、追加します。</span><span class="sxs-lookup"><span data-stu-id="b1569-140">Name file as **Extension.Config** and add it.</span></span>

7. <span data-ttu-id="b1569-141">**Extension.Config** ファイルを Commerce Runtime 拡張機能で更新します。</span><span class="sxs-lookup"><span data-stu-id="b1569-141">Update the **Extension.Config** file with the Commerce Runtime extensions.</span></span> <span data-ttu-id="b1569-142">Commerce Runtime 拡張機能が無い場合は、**合成** セクションを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="b1569-142">If you don’t have any Commerce Runtime extensions, leave the **composition** section empty.</span></span> <span data-ttu-id="b1569-143">Xml は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="b1569-143">The Xml looks like this:</span></span>

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <commerceRuntimeExtensions>
        <composition>
            <add source="assembly" value="CommerceRuntime" />
          </composition>
    ```

8. <span data-ttu-id="b1569-144">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="b1569-144">Compile and build the project.</span></span> <span data-ttu-id="b1569-145">このプロジェクトの出力に、**ScaleUnit** インストーラー .exe ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1569-145">The output of this project contains the **ScaleUnit** installer .exe file.</span></span>

9. <span data-ttu-id="b1569-146">拡張機能を手動でインストールするには、管理者モードで PowerShell を開き、拡張機能インストーラーのフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="b1569-146">To manually install the extension, open PowerShell in administrator mode and navigate to the extension installer folder.</span></span> <span data-ttu-id="b1569-147">install コマンドを実行して拡張機能をインストールします。</span><span class="sxs-lookup"><span data-stu-id="b1569-147">Run the install command to install the extensions.</span></span>

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ScaleUnit.Installer.exe install    
    ```

    <span data-ttu-id="b1569-148">拡張機能をアンインストールするには:</span><span class="sxs-lookup"><span data-stu-id="b1569-148">To uninstall the extension:</span></span>

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ScaleUnit.Installer.exe uninstall
    ```

    > [!NOTE]
    > <span data-ttu-id="b1569-149">拡張機能インストーラーをインストールする前に、シールドされた **ScaleUnit** パッケージを最初にインストールします。</span><span class="sxs-lookup"><span data-stu-id="b1569-149">Before installing the extension installer, install the sealed **ScaleUnit** package.</span></span> <span data-ttu-id="b1569-150">Commerce Runtime、Retail Server、またはデーターベース拡張機能がある場合は、すべての拡張機能のプロジェクトを参照として **ScaleUnit.Installer** プロジェクトに含みます。</span><span class="sxs-lookup"><span data-stu-id="b1569-150">If you have Commerce Runtime, Retail Server, or a Database extension, then you must include all these extension projects as references to the **ScaleUnit.Installer** project.</span></span> <span data-ttu-id="b1569-151">プロジェクトを追加すると、すべての拡張機能を含む複合配置パッケージが生成されます。</span><span class="sxs-lookup"><span data-stu-id="b1569-151">Adding the projects generates a combined deployment package that contains all your extensions.</span></span>
    > <span data-ttu-id="b1569-152">拡張機能によって複数のスケール ユニット インストーラーを作成し、それらを個別に管理することもできます。</span><span class="sxs-lookup"><span data-stu-id="b1569-152">You can also create multiple Scale unit installers by extensions and manage them separately.</span></span> <span data-ttu-id="b1569-153">拡張機能をすべてパッケージで結合する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b1569-153">You don’t have to combine all the extensions in one package.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

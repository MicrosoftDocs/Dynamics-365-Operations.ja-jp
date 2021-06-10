---
title: Modern POS 拡張機能パッケージの作成
description: このトピックでは、Modern POS 拡張機能パッケージの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: c28e23f973dc275cf2f13f12ee210dff1af2f6ac
ms.sourcegitcommit: 4c880b152e81350f023b944c2ab13e60498e2c7b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2021
ms.locfileid: "6093894"
---
# <a name="create-a-modern-pos-extension-package"></a><span data-ttu-id="24f7b-103">Modern POS 拡張機能パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="24f7b-103">Create a Modern POS extension package</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="24f7b-104">Modern POS 拡張機能用の拡張機能インストーラーを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="24f7b-104">To create the extension installer for a Modern POS extension, follow these steps:</span></span>

1. <span data-ttu-id="24f7b-105">Visual studio 2017 を開いて新しいコンソール アプリケーション (.NET Core) を作成し、**ModernPos.Installer** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="24f7b-105">Open Visual studio 2017, create a new console application (.NET Core), and name it **ModernPos.Installer**.</span></span>

2. <span data-ttu-id="24f7b-106">**.proj** ファイルを編集し、**ターゲット フレームワーク** を **.NET Framework 4.6.1** に変更します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-106">Edit the **.proj** file and change the **Target Framework** to **.NET Framework 4.6.1**.</span></span> <span data-ttu-id="24f7b-107">XML はここに表示されます。</span><span class="sxs-lookup"><span data-stu-id="24f7b-107">The Xml is shown here:</span></span>

    ```Javascript
    <Project Sdk="Microsoft.NET.Sdk">
      <PropertyGroup>
        <OutputType>Exe</OutputType>
        <TargetFramework>net461</TargetFramework>
      </PropertyGroup>
    </Project>
    ```

3. <span data-ttu-id="24f7b-108">生成された **Program.cs** ファイルは削除します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-108">Delete the generated **Program.cs** file.</span></span>

4. <span data-ttu-id="24f7b-109">**Microsoft.Dynamics.Commerce.Sdk.Installers.ModernPos** NuGet パッケージへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-109">Add a reference to the **Microsoft.Dynamics.Commerce.Sdk.Installers.ModernPos** NuGet Package.</span></span>

    1. <span data-ttu-id="24f7b-110">ソリューション エクスプローラーのプロジェクトを選択し、**NuGet パッケージの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-110">Right-click the project in Solution Explorer and select **Manage NuGet packages**.</span></span>
    2. <span data-ttu-id="24f7b-111">NuGet パッケージ マネージャー ウィンドウで **参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-111">Select the **Browse** tab in the NuGet Package Manager window.</span></span>
    3. <span data-ttu-id="24f7b-112">**Microsoft.Dynamics.Commerce.Sdk.Installers.ModernPos** を検索します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-112">Search for **Microsoft.Dynamics.Commerce.Sdk.Installers.ModernPos**.</span></span>
    4. <span data-ttu-id="24f7b-113">パッケージを選択し、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-113">Select the package and then select **Install**.</span></span>
    5. <span data-ttu-id="24f7b-114">Go-Live バージョンと一致するバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-114">select the version that matches your go-live version.</span></span>

5. <span data-ttu-id="24f7b-115">上記のとおりに作成した **ModernPos.Installer** プロジェクトへ Modern POS プロジェクト からの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-115">Add a reference from your Modern POS project to the **ModernPos.Installer** project created above.</span></span>

    1. <span data-ttu-id="24f7b-116">ソリューション エクスプローラーで、Modern POS プロジェクトを右クリックし、**追加 -&gt; 参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-116">Right-click the Modern POS project in Solution Explorer and select **Add -&gt; Reference**.</span></span>
    2. <span data-ttu-id="24f7b-117">参照マネージャの左側にある **プロジェクト** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-117">Select the **Projects** tab on the left side of the Reference Manager.</span></span>
    3. <span data-ttu-id="24f7b-118">上記の通りに作成した **ModernPos.Installer** プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-118">Select the **ModernPos.Installer** project created above.</span></span>

6. <span data-ttu-id="24f7b-119">\[オフライン チャンネル データベースの拡張スクリプト プロジェクトのみ\]: Modern POS プロジェクトからの参照をチャンネル データベース プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-119">For \[Offline channel database extension script projects only\]: add a reference from the Modern POS project to the Channel database project.</span></span>

    1. <span data-ttu-id="24f7b-120">ソリューション エクスプローラーで、Modern POS プロジェクトを右クリックし、**追加 -&gt; 参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-120">Right-click the Modern POS project in Solution Explorer and select **Add -&gt; Reference**.</span></span>
    2. <span data-ttu-id="24f7b-121">参照マネージャの左側にある **プロジェクト** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-121">Select the **Projects** tab on the left side of the Reference Manager.</span></span>
    3. <span data-ttu-id="24f7b-122">上記のとおりに作成したチャネル データベース拡張機能プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-122">Select the Channel database extension project created above.</span></span>

7. <span data-ttu-id="24f7b-123">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="24f7b-123">Compile and build the project.</span></span> <span data-ttu-id="24f7b-124">このプロジェクトの出力に、Modern POS 拡張機能インストーラーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="24f7b-124">The output of this project contains the Modern POS extension installer.</span></span>

8. <span data-ttu-id="24f7b-125">拡張機能を手動でインストールするには、管理者モードで PowerShell を開き、拡張機能インストーラーのフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="24f7b-125">To manually install the extension, open PowerShell in administrator mode and navigate to the extension installer folder.</span></span> <span data-ttu-id="24f7b-126">install コマンドを実行して拡張機能をインストールします。</span><span class="sxs-lookup"><span data-stu-id="24f7b-126">Run the install command to install the extensions.</span></span>

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ModernPos.Installer.exe install
    ```

    <span data-ttu-id="24f7b-127">拡張機能をアンインストールするには:</span><span class="sxs-lookup"><span data-stu-id="24f7b-127">To uninstall the extension:</span></span>

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ModernPos.Installer.exe uninstall
    ```

    > [!NOTE]
    > <span data-ttu-id="24f7b-128">拡張機能インストーラーをインストールする前に、シールドされた Modern POS を最初にインストールします。</span><span class="sxs-lookup"><span data-stu-id="24f7b-128">Before installing the extension installer, install the sealed Modern POS first.</span></span>

9. <span data-ttu-id="24f7b-129">拡張機能をインストールした後、実行されている場合は Modern POS を閉じます。</span><span class="sxs-lookup"><span data-stu-id="24f7b-129">After installing the extension, close Modern POS if it's running.</span></span> <span data-ttu-id="24f7b-130">**Modern POS のインストール/更新** のデスクトップ ショートカットから Modern POS Modern POS を起動し、拡張機能を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="24f7b-130">Launch Modern POS from the **Install/Update Modern POS** desktop shortcut icon to load the extension.</span></span> <span data-ttu-id="24f7b-131">拡張子が .appx のファイルは、デスクトップ アイコンをクリックした後にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="24f7b-131">The extension .appx file will be installed after clicking the desktop icon.</span></span> <span data-ttu-id="24f7b-132">前の手順で .appx とファイルを正しい場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="24f7b-132">The previous steps copy the .appx and files to the correct location.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

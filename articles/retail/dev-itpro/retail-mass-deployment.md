---
title: Retail セルフサービス コンポーネントの一括配置
description: このトピックでは、セルフ サービスを使用してサイレント サービスの更新と初期展開を行う方法について説明します。 また、特別な配置のいくつかの側面についても説明します。
author: jashanno
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2017-09-31
ms.dyn365.ops.version: Application update 3
ms.openlocfilehash: 515b79044364a30d24781725101d779da71d541e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368344"
---
# <a name="mass-deployment-of-retail-self-service-components"></a><span data-ttu-id="7c960-104">Retail セルフサービス コンポーネントの一括配置</span><span class="sxs-lookup"><span data-stu-id="7c960-104">Mass deployment of Retail self-service components</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c960-105">このトピックでは、セルフ サービスを使用してサイレント サービスの更新と初期展開を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7c960-105">This topic explains how you can use self-service to do silent servicing updates and initial deployments.</span></span> <span data-ttu-id="7c960-106">また、特別な配置のいくつかの側面についても説明します。</span><span class="sxs-lookup"><span data-stu-id="7c960-106">It also explains some aspects of special deployment.</span></span> <span data-ttu-id="7c960-107">このトピックは、機能が開発され、より多くの機能が利用可能になると更新されます。</span><span class="sxs-lookup"><span data-stu-id="7c960-107">This topic will be updated as the feature is developed and more functionality becomes available.</span></span> <span data-ttu-id="7c960-108">現在、サイレント サービス更新の機能のみが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="7c960-108">Currently, only the capability for silent servicing updates is available.</span></span>

## <a name="delimiters-for-mass-deployment"></a><span data-ttu-id="7c960-109">一括配置の区切り記号</span><span class="sxs-lookup"><span data-stu-id="7c960-109">Delimiters for mass deployment</span></span>

<span data-ttu-id="7c960-110">次のテーブルに、一括配置の実行コマンドで現在使用できる区切り記号を示します。</span><span class="sxs-lookup"><span data-stu-id="7c960-110">The following table shows the delimiters that can currently be used in execution commands for mass deployment.</span></span> <span data-ttu-id="7c960-111">これらの区切り文字は、アプリケーションの更新プログラム 3、2017 年 7 月版以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7c960-111">These delimiters apply to the July 2017 version with Application update 3 or later.</span></span>

| <span data-ttu-id="7c960-112">区切り記号</span><span class="sxs-lookup"><span data-stu-id="7c960-112">Delimiter</span></span>                 | <span data-ttu-id="7c960-113">説明</span><span class="sxs-lookup"><span data-stu-id="7c960-113">Description</span></span> |
|---------------------------|-------------|
| <span data-ttu-id="7c960-114">-S または -サイレント</span><span class="sxs-lookup"><span data-stu-id="7c960-114">-S or -Silent</span></span>             | <span data-ttu-id="7c960-115">インストーラーをサイレントで実行します。</span><span class="sxs-lookup"><span data-stu-id="7c960-115">Silently run the installer.</span></span> <span data-ttu-id="7c960-116">グラフィカル ユーザー インターフェイス (GUI) を使用しません。</span><span class="sxs-lookup"><span data-stu-id="7c960-116">No graphical user interface (GUI) is used.</span></span> <span data-ttu-id="7c960-117">**-Q** および **-Quiet** 区切り記号には同じ効果があり、使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="7c960-117">The **-Q** and **-Quiet** delimiters have the same effect and can also be used.</span></span> |
| <span data-ttu-id="7c960-118">-C または -Config</span><span class="sxs-lookup"><span data-stu-id="7c960-118">-C or -Config</span></span>             | <span data-ttu-id="7c960-119">このインストールの一部として使用するコンフィギュレーション ファイルの場所とファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="7c960-119">Specify the location and file name of the configuration file to use as part of this installation.</span></span> |
| <span data-ttu-id="7c960-120">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7c960-120">-FilePath</span></span>                 | <span data-ttu-id="7c960-121">カスタム インストールの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="7c960-121">Specify a custom installation location.</span></span><p><p><span data-ttu-id="7c960-122">標準のインストールにこの区切り記号を使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="7c960-122">We don't recommend that you use this delimiter for a standard installation.</span></span></p> |
| <span data-ttu-id="7c960-123">-LogFile</span><span class="sxs-lookup"><span data-stu-id="7c960-123">-LogFile</span></span>                  | <span data-ttu-id="7c960-124">インストール ログのカスタム ファイルの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="7c960-124">Specify a custom file location for the installation logs.</span></span><p><p><span data-ttu-id="7c960-125">標準のインストールにこの区切り記号を使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="7c960-125">We don't recommend that you use this delimiter for a standard installation.</span></span></p> |
| <span data-ttu-id="7c960-126">-SkipPrerequisiteCheck</span><span class="sxs-lookup"><span data-stu-id="7c960-126">-SkipPrerequisiteCheck</span></span>    | <span data-ttu-id="7c960-127">前提条件および必須コンポーネントのインストールのチェックをスキップします。</span><span class="sxs-lookup"><span data-stu-id="7c960-127">Skip the check for prerequisites and prerequisite installation.</span></span><p><p><span data-ttu-id="7c960-128">この区切り記号は、開発とテストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c960-128">You should use this delimiter only for development and testing.</span></span> <span data-ttu-id="7c960-129">標準のインストールにそれを使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="7c960-129">We don't recommend that you use it for a standard installation.</span></span></p> |
| <span data-ttu-id="7c960-130">-SkipSystemInfoCollection</span><span class="sxs-lookup"><span data-stu-id="7c960-130">-SkipSystemInfoCollection</span></span> | <span data-ttu-id="7c960-131">インストールの開始時にシステム情報を収集するプロセスをスキップします。</span><span class="sxs-lookup"><span data-stu-id="7c960-131">Skip the process of collecting system information at the beginning of the installation.</span></span><p><p><span data-ttu-id="7c960-132">この区切り記号は、開発とテストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c960-132">You should use this delimiter only for development and testing.</span></span> <span data-ttu-id="7c960-133">標準のインストールにそれを使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="7c960-133">We don't recommend that you use it for a standard installation.</span></span></p> |
| <span data-ttu-id="7c960-134">-SkipMerchantInfo</span><span class="sxs-lookup"><span data-stu-id="7c960-134">-SkipMerchantInfo</span></span>         | <span data-ttu-id="7c960-135">ハードウェア ステーションのセルフ サービス インストーラーの終わりにマーチャント アカウント情報のインストールをスキップします。</span><span class="sxs-lookup"><span data-stu-id="7c960-135">Skip the installation of merchant account information at the end of the self-service installer for Hardware station.</span></span><p><p><span data-ttu-id="7c960-136">この区切り記号は、開発とテストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c960-136">You should use this delimiter only for development and testing.</span></span> <span data-ttu-id="7c960-137">標準のインストールにそれを使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="7c960-137">We don't recommend that you use it for a standard installation.</span></span></p> |

## <a name="silent-servicing"></a><span data-ttu-id="7c960-138">サイレント サービス</span><span class="sxs-lookup"><span data-stu-id="7c960-138">Silent servicing</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="7c960-139">準備</span><span class="sxs-lookup"><span data-stu-id="7c960-139">Before you begin</span></span>

<span data-ttu-id="7c960-140">この機能を使用するには、アプリケーションの更新プログラム 3 の 2017 年 7 月のバージョン以降を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c960-140">To use this functionality, you must be using the July 2017 version with Application update 3 or later.</span></span> <span data-ttu-id="7c960-141">サイレント サービスが現在インストールされているすべてのコンポーネントを維持していることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7c960-141">Note that silent servicing maintains all components that are currently installed.</span></span> <span data-ttu-id="7c960-142">任意のコンフィギュレーションがまだ必要な場合は、このトピックの手順を開始する前に実行します。</span><span class="sxs-lookup"><span data-stu-id="7c960-142">If any configuration is still required, complete it before you begin to follow the instructions in this topic.</span></span>

### <a name="examples-of-commands-for-silent-servicing"></a><span data-ttu-id="7c960-143">サイレント サービスのコマンド例</span><span class="sxs-lookup"><span data-stu-id="7c960-143">Examples of commands for silent servicing</span></span>

<span data-ttu-id="7c960-144">このセクションでは、セルフサービスの大量展開に使用されるコマンドの例を示します。</span><span class="sxs-lookup"><span data-stu-id="7c960-144">This section shows examples of commands that are used for self-service mass deployment.</span></span> <span data-ttu-id="7c960-145">これらのコマンドは、Retail Modern POS (オフラインでサポートされているインストーラーとオフラインでサポートされていないインストーラーの両方) 用インストーラー、ハードウェア ステーション、Retail Store Scale Unit など、すべての標準セルフサービス インストーラーで動作します。</span><span class="sxs-lookup"><span data-stu-id="7c960-145">These commands work for all the standard self-service installers, such as the installers for Retail Modern POS (both the installer that has offline support and the installer that doesn't have offline support), Hardware station, and Retail Store Scale Unit.</span></span>

#### <a name="silently-update-the-current-installation-of-retail-modern-pos"></a><span data-ttu-id="7c960-146">Retail Modern POS の現在のインストールをサイレントに更新</span><span class="sxs-lookup"><span data-stu-id="7c960-146">Silently update the current installation of Retail Modern POS</span></span>

<span data-ttu-id="7c960-147">次のコマンドは、Retail Modern POS の現在のインストールをサイレント更新します。</span><span class="sxs-lookup"><span data-stu-id="7c960-147">The following command silently updates the current installation of Retail Modern POS.</span></span> <span data-ttu-id="7c960-148">このコマンドには、現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。</span><span class="sxs-lookup"><span data-stu-id="7c960-148">This command has the standard command structure that is used for silent servicing of components that are currently installed.</span></span> <span data-ttu-id="7c960-149">この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。</span><span class="sxs-lookup"><span data-stu-id="7c960-149">The structure uses the basic values of **&lt;InstallerName&gt;.exe** and the command for silent installation, **-S**.</span></span> <span data-ttu-id="7c960-150">このコマンドは、構成ファイルが存在する場合は、インストーラーと同じファイルの場所にある構成ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c960-150">This command uses the configuration file that is located in the same file location as the installer, if a configuration file exists there.</span></span>

```
ModernPOSSetup_V72.exe -S
```

> [!NOTE]
> <span data-ttu-id="7c960-151">Retail Store Scale Unit ではコンフィギュレーション ファイルがまだ必要とされます。</span><span class="sxs-lookup"><span data-stu-id="7c960-151">A configuration file is still required for Retail Store Scale Unit.</span></span> <span data-ttu-id="7c960-152">ただし、インストーラーは可能な場合はいつでも、現在インストールされているすべての値を保持します。</span><span class="sxs-lookup"><span data-stu-id="7c960-152">However, the installer keeps all the values that are currently installed, whenever it can.</span></span>

#### <a name="silently-update-the-current-installation-of-retail-store-scale-unit"></a><span data-ttu-id="7c960-153">Retail Store Scale Unit の現在のインストールをサイレントに更新</span><span class="sxs-lookup"><span data-stu-id="7c960-153">Silently update the current installation of Retail Store Scale Unit</span></span>

<span data-ttu-id="7c960-154">次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Retail Store Scale Unit の現在のインストールをサイレント更新します。</span><span class="sxs-lookup"><span data-stu-id="7c960-154">The following command silently updates the current installation of Retail Store Scale Unit by using a specific configuration file.</span></span> <span data-ttu-id="7c960-155">(このコンフィギュレーション ファイルは、インストーラーの実行可能ファイルと同じ場所にない可能性があります。) このコマンドは、前提条件のチェックをスキップし、インストール手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="7c960-155">(This configuration file might not be in the same location as the executable file for the installer.) This command skips the prerequisite check and moves on to the installation steps.</span></span> <span data-ttu-id="7c960-156">テストおよび開発の目的にのみ、このコマンドを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7c960-156">We recommend that you use this command only for testing and development purposes.</span></span>

```
StoreSystemSetup_V72.exe -S -C "C:\Temp\StoreSystemSetup_V72_Houston.xml" -SkipPrerequisiteCheck
```

## <a name="mass-deployment-of-retail-modern-pos"></a><span data-ttu-id="7c960-157">Retail Modern POS の一括配置</span><span class="sxs-lookup"><span data-stu-id="7c960-157">Mass deployment of Retail Modern POS</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="7c960-158">準備</span><span class="sxs-lookup"><span data-stu-id="7c960-158">Before you begin</span></span>

<span data-ttu-id="7c960-159">この機能を使用するには、バージョン 7.3 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="7c960-159">To use this functionality, you must be using version 7.3 or later.</span></span> <span data-ttu-id="7c960-160">本社でのすべての店舗、レジスター、およびデバイスのコンフィギュレーション、およびその他のコンフィギュレーションが既に完了したとみなされます。</span><span class="sxs-lookup"><span data-stu-id="7c960-160">It's assumed that the configuration of all stores, registers, and devices, and other configurations in the headquarters have already been completed.</span></span> <span data-ttu-id="7c960-161">任意のコンフィギュレーションがまだ必要な場合は、このトピックの手順を実行する前に実行します。</span><span class="sxs-lookup"><span data-stu-id="7c960-161">If any configuration is still required, complete it before you follow the instructions in this topic.</span></span>

### <a name="examples-of-commands-for-silent-mass-deployment"></a><span data-ttu-id="7c960-162">サイレント マス展開のコマンド例</span><span class="sxs-lookup"><span data-stu-id="7c960-162">Examples of commands for silent mass deployment</span></span>

<span data-ttu-id="7c960-163">このセクションでは、Retail Modern POS、オフラインの Retail Modern POS、およびオフライン サポートのないインストーラのセルフサービスの大量展開に使用されるコマンドの例を示します。</span><span class="sxs-lookup"><span data-stu-id="7c960-163">This section shows examples of commands that are used for self-service mass deployment of Retail Modern POS, even Retail Modern POS with offline and the installer without offline support.</span></span> <span data-ttu-id="7c960-164">Windows PowerShell スクリプトの例では、ユーザーがインストールを実行する支援も含まれます。</span><span class="sxs-lookup"><span data-stu-id="7c960-164">Examples of Windows PowerShell scripts are also included to help users do the installations.</span></span>

#### <a name="silently-install-retail-modern-pos"></a><span data-ttu-id="7c960-165">Retail Modern POS のサイレント インストール</span><span class="sxs-lookup"><span data-stu-id="7c960-165">Silently install Retail Modern POS</span></span>

<span data-ttu-id="7c960-166">次のコマンドは、Retail Modern POS の現在のインストールをサイレント更新します。</span><span class="sxs-lookup"><span data-stu-id="7c960-166">The following command silently updates the current installation of Retail Modern POS.</span></span> <span data-ttu-id="7c960-167">このコマンドには、現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。</span><span class="sxs-lookup"><span data-stu-id="7c960-167">This command has the standard command structure that is used for silent servicing of components that are currently installed.</span></span> <span data-ttu-id="7c960-168">この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。</span><span class="sxs-lookup"><span data-stu-id="7c960-168">The structure uses the basic values of **&lt;InstallerName&gt;.exe** and the command for silent installation, **-S**.</span></span> <span data-ttu-id="7c960-169">このコマンドは、構成ファイルが存在する場合は、インストーラーと同じファイルの場所にある構成ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c960-169">This command uses the configuration file that is located in the same file location as the installer, if a configuration file exists there.</span></span> <span data-ttu-id="7c960-170">このコマンドは、複数の構成ファイルを選択できる場合には使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="7c960-170">This command should not be used if multiple configuration files are available for selection.</span></span>

```
ModernPOSSetup_V73.exe -S
```

> [!NOTE]
> <span data-ttu-id="7c960-171">Retail Modern POS ではコンフィギュレーション ファイルは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="7c960-171">A configuration file isn't required for Retail Modern POS.</span></span> <span data-ttu-id="7c960-172">ただし、関連付けられている構成ファイルを読み込めない限り、インストールされた Retail Modern POS アプリは適切な方法では有効化されません。</span><span class="sxs-lookup"><span data-stu-id="7c960-172">However, the Retail Modern POS application that is installed can't be activated in the appropriate manner unless the associated configuration file can be read from.</span></span>

#### <a name="silently-install-retail-modern-pos-by-using-a-specific-configuration-file"></a><span data-ttu-id="7c960-173">特定のコンフィギュレーション ファイルを使用して Retail Modern POS をサイレント インストール</span><span class="sxs-lookup"><span data-stu-id="7c960-173">Silently install Retail Modern POS by using a specific configuration file</span></span>

<span data-ttu-id="7c960-174">次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Retail Modern POS の現在のインストールをサイレント インストールします。</span><span class="sxs-lookup"><span data-stu-id="7c960-174">The following command silently installs the current installation of Retail Modern POS by using a specific configuration file.</span></span> <span data-ttu-id="7c960-175">この構成ファイルは、インストーラーの実行可能ファイルと同じ場所にないか、複数の構成ファイルが使用可能な場合があります。</span><span class="sxs-lookup"><span data-stu-id="7c960-175">This configuration file might not be in the same location as the executable file for the installer, or multiple configuration files might be available.</span></span>

```
ModernPOSSetup_V72.exe -S -C "C:\Temp\ModernPOSSetup_V73_Houston-3.xml"
```

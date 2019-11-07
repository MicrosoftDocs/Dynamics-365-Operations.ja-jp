---
title: Retail セルフサービス コンポーネントの一括配置
description: このトピックでは、セルフ サービスを使用してサイレント サービスの更新と初期展開を行う方法について説明します。 また、特別な配置のいくつかの側面についても説明します。
author: jashanno
manager: AnnBe
ms.date: 10/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2017-09-31
ms.dyn365.ops.version: Application update 3
ms.openlocfilehash: 036b9458e9fa6c6f57a9db26706ca3e6784858e9
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658895"
---
# <a name="mass-deployment-of-retail-self-service-components"></a><span data-ttu-id="53eee-104">Retail セルフサービス コンポーネントの一括配置</span><span class="sxs-lookup"><span data-stu-id="53eee-104">Mass deployment of Retail self-service components</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="53eee-105">このトピックでは、セルフ サービスを使用してサイレント サービスの更新と初期展開を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="53eee-105">This topic explains how you can use self-service to do silent servicing updates and initial deployments.</span></span> <span data-ttu-id="53eee-106">また、特別な配置のいくつかの側面についても説明します。</span><span class="sxs-lookup"><span data-stu-id="53eee-106">It also explains some aspects of special deployment.</span></span> <span data-ttu-id="53eee-107">このトピックは、機能が開発され、より多くの機能が利用可能になると更新されます。</span><span class="sxs-lookup"><span data-stu-id="53eee-107">This topic will be updated as the feature is developed and more functionality becomes available.</span></span> <span data-ttu-id="53eee-108">現在、サイレント サービス更新の機能のみが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="53eee-108">Currently, only the capability for silent servicing updates is available.</span></span>

## <a name="delimiters-for-mass-deployment"></a><span data-ttu-id="53eee-109">一括配置の区切り記号</span><span class="sxs-lookup"><span data-stu-id="53eee-109">Delimiters for mass deployment</span></span>

<span data-ttu-id="53eee-110">次のテーブルに、一括配置の実行コマンドで現在使用できる区切り記号を示します。</span><span class="sxs-lookup"><span data-stu-id="53eee-110">The following table shows the delimiters that can currently be used in execution commands for mass deployment.</span></span> 


| <span data-ttu-id="53eee-111">区切り記号</span><span class="sxs-lookup"><span data-stu-id="53eee-111">Delimiter</span></span>                 | <span data-ttu-id="53eee-112">説明</span><span class="sxs-lookup"><span data-stu-id="53eee-112">Description</span></span> |
|---------------------------|-------------|
| <span data-ttu-id="53eee-113">-S または -サイレント</span><span class="sxs-lookup"><span data-stu-id="53eee-113">-S or -Silent</span></span>             | <span data-ttu-id="53eee-114">インストーラーをサイレントで実行します。</span><span class="sxs-lookup"><span data-stu-id="53eee-114">Silently run the installer.</span></span> <span data-ttu-id="53eee-115">グラフィカル ユーザー インターフェイス (GUI) を使用しません。</span><span class="sxs-lookup"><span data-stu-id="53eee-115">No graphical user interface (GUI) is used.</span></span> <span data-ttu-id="53eee-116">**-Q** および **-Quiet** 区切り記号には同じ効果があり、使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="53eee-116">The **-Q** and **-Quiet** delimiters have the same effect and can also be used.</span></span> |
| <span data-ttu-id="53eee-117">-C または -Config</span><span class="sxs-lookup"><span data-stu-id="53eee-117">-C or -Config</span></span>             | <span data-ttu-id="53eee-118">このインストールの一部として使用するコンフィギュレーション ファイルの場所とファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="53eee-118">Specify the location and file name of the configuration file to use as part of this installation.</span></span> |
| <span data-ttu-id="53eee-119">-FilePath</span><span class="sxs-lookup"><span data-stu-id="53eee-119">-FilePath</span></span>                 | <span data-ttu-id="53eee-120">カスタム インストールの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="53eee-120">Specify a custom installation location.</span></span><p><span data-ttu-id="53eee-121">標準のインストールにこの区切り記号を使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="53eee-121">We don't recommend that you use this delimiter for a standard installation.</span></span></p> |
| <span data-ttu-id="53eee-122">-LogFile</span><span class="sxs-lookup"><span data-stu-id="53eee-122">-LogFile</span></span>                  | <span data-ttu-id="53eee-123">インストール ログのカスタム ファイルの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="53eee-123">Specify a custom file location for the installation logs.</span></span><p><span data-ttu-id="53eee-124">標準のインストールにこの区切り記号を使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="53eee-124">We don't recommend that you use this delimiter for a standard installation.</span></span></p> |
| <span data-ttu-id="53eee-125">-SkipPrerequisiteCheck</span><span class="sxs-lookup"><span data-stu-id="53eee-125">-SkipPrerequisiteCheck</span></span>    | <span data-ttu-id="53eee-126">前提条件および必須コンポーネントのインストールのチェックをスキップします。</span><span class="sxs-lookup"><span data-stu-id="53eee-126">Skip the check for prerequisites and prerequisite installation.</span></span><p><span data-ttu-id="53eee-127">この区切り記号は、開発とテストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53eee-127">You should use this delimiter only for development and testing.</span></span> <span data-ttu-id="53eee-128">標準のインストールにそれを使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="53eee-128">We don't recommend that you use it for a standard installation.</span></span></p> |
| <span data-ttu-id="53eee-129">-SkipSystemInfoCollection</span><span class="sxs-lookup"><span data-stu-id="53eee-129">-SkipSystemInfoCollection</span></span> | <span data-ttu-id="53eee-130">インストールの開始時にシステム情報を収集するプロセスをスキップします。</span><span class="sxs-lookup"><span data-stu-id="53eee-130">Skip the process of collecting system information at the beginning of the installation.</span></span><p><span data-ttu-id="53eee-131">この区切り記号は、開発とテストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53eee-131">You should use this delimiter only for development and testing.</span></span> <span data-ttu-id="53eee-132">標準のインストールにそれを使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="53eee-132">We don't recommend that you use it for a standard installation.</span></span></p> |
| <span data-ttu-id="53eee-133">-SkipMerchantInfo</span><span class="sxs-lookup"><span data-stu-id="53eee-133">-SkipMerchantInfo</span></span>         | <span data-ttu-id="53eee-134">ハードウェア ステーションのセルフ サービス インストーラーの終わりにマーチャント アカウント情報のインストールをスキップします。</span><span class="sxs-lookup"><span data-stu-id="53eee-134">Skip the installation of merchant account information at the end of the self-service installer for Hardware station.</span></span><p><span data-ttu-id="53eee-135">この区切り記号は、開発とテストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53eee-135">You should use this delimiter only for development and testing.</span></span> <span data-ttu-id="53eee-136">標準のインストールにそれを使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="53eee-136">We don't recommend that you use it for a standard installation.</span></span></p> |
| <span data-ttu-id="53eee-137">-SkipAppxInstallation</span><span class="sxs-lookup"><span data-stu-id="53eee-137">-SkipAppxInstallation</span></span>     | <span data-ttu-id="53eee-138">Dynamics 365 の2018 年 10 月のリリースから、この区切り記号は APPX Retail Modern POS アプリケーションのインストールをスキップします。</span><span class="sxs-lookup"><span data-stu-id="53eee-138">Beginning in the October 2018 release of Dynamics 365, this delimiter will skip the installation of the APPX Retail Modern POS application.</span></span> <span data-ttu-id="53eee-139">この区切り記号は、システム アカウントまたはサービス アカウント (ユーザー プロファイルがないアカウント) を使用してアプリケーションのインストールを実行するために必要です。</span><span class="sxs-lookup"><span data-stu-id="53eee-139">This delimiter is required to perform the application installation through the SYSTEM account or a service account (Any account that does not have a user profile).</span></span> |

## <a name="silent-servicing"></a><span data-ttu-id="53eee-140">サイレント サービス</span><span class="sxs-lookup"><span data-stu-id="53eee-140">Silent servicing</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="53eee-141">準備</span><span class="sxs-lookup"><span data-stu-id="53eee-141">Before you begin</span></span>

<span data-ttu-id="53eee-142">サイレント サービスが現在インストールされているすべてのコンポーネントを維持していることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="53eee-142">Note that silent servicing maintains all components that are currently installed.</span></span> <span data-ttu-id="53eee-143">任意のコンフィギュレーションがまだ必要な場合は、このトピックの手順を開始する前に実行します。</span><span class="sxs-lookup"><span data-stu-id="53eee-143">If any configuration is still required, complete it before you begin to follow the instructions in this topic.</span></span>

### <a name="examples-of-commands-for-silent-servicing"></a><span data-ttu-id="53eee-144">サイレント サービスのコマンド例</span><span class="sxs-lookup"><span data-stu-id="53eee-144">Examples of commands for silent servicing</span></span>

<span data-ttu-id="53eee-145">このセクションでは、セルフサービスの大量展開に使用されるコマンドの例を示します。</span><span class="sxs-lookup"><span data-stu-id="53eee-145">This section shows examples of commands that are used for self-service mass deployment.</span></span> <span data-ttu-id="53eee-146">これらのコマンドは、Retail Modern POS (オフラインでサポートされているインストーラーとオフラインでサポートされていないインストーラーの両方) 用インストーラー、ハードウェア ステーション、Retail Store Scale Unit など、すべての標準セルフサービス インストーラーで動作します。</span><span class="sxs-lookup"><span data-stu-id="53eee-146">These commands work for all the standard self-service installers, such as the installers for Retail Modern POS (both the installer that has offline support and the installer that doesn't have offline support), Hardware station, and Retail Store Scale Unit.</span></span>

#### <a name="silently-update-the-current-installation-of-retail-modern-pos"></a><span data-ttu-id="53eee-147">Retail Modern POS の現在のインストールをサイレントに更新</span><span class="sxs-lookup"><span data-stu-id="53eee-147">Silently update the current installation of Retail Modern POS</span></span>

<span data-ttu-id="53eee-148">次のコマンドは、Retail Modern POS の現在のインストールをサイレント更新します。</span><span class="sxs-lookup"><span data-stu-id="53eee-148">The following command silently updates the current installation of Retail Modern POS.</span></span> <span data-ttu-id="53eee-149">このコマンドには、現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。</span><span class="sxs-lookup"><span data-stu-id="53eee-149">This command has the standard command structure that is used for silent servicing of components that are currently installed.</span></span> <span data-ttu-id="53eee-150">この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。</span><span class="sxs-lookup"><span data-stu-id="53eee-150">The structure uses the basic values of **&lt;InstallerName&gt;.exe** and the command for silent installation, **-S**.</span></span> <span data-ttu-id="53eee-151">このコマンドは、構成ファイルが存在する場合は、インストーラーと同じファイルの場所にある構成ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="53eee-151">This command uses the configuration file that is located in the same file location as the installer, if a configuration file exists there.</span></span>

```
ModernPOSSetup_V72.exe -S
```

> [!NOTE]
> <span data-ttu-id="53eee-152">Retail Store Scale Unit ではコンフィギュレーション ファイルがまだ必要とされます。</span><span class="sxs-lookup"><span data-stu-id="53eee-152">A configuration file is still required for Retail Store Scale Unit.</span></span> <span data-ttu-id="53eee-153">ただし、インストーラーは可能な場合はいつでも、現在インストールされているすべての値を保持します。</span><span class="sxs-lookup"><span data-stu-id="53eee-153">However, the installer keeps all the values that are currently installed, whenever it can.</span></span>

#### <a name="silently-update-the-current-installation-of-retail-store-scale-unit"></a><span data-ttu-id="53eee-154">Retail Store Scale Unit の現在のインストールをサイレントに更新</span><span class="sxs-lookup"><span data-stu-id="53eee-154">Silently update the current installation of Retail Store Scale Unit</span></span>

<span data-ttu-id="53eee-155">次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Retail Store Scale Unit の現在のインストールをサイレント更新します。</span><span class="sxs-lookup"><span data-stu-id="53eee-155">The following command silently updates the current installation of Retail Store Scale Unit by using a specific configuration file.</span></span> <span data-ttu-id="53eee-156">(このコンフィギュレーション ファイルは、インストーラーの実行可能ファイルと同じ場所にない可能性があります。) このコマンドは、前提条件のチェックをスキップし、インストール手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="53eee-156">(This configuration file might not be in the same location as the executable file for the installer.) This command skips the prerequisite check and moves on to the installation steps.</span></span> <span data-ttu-id="53eee-157">テストおよび開発の目的にのみ、このコマンドを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="53eee-157">We recommend that you use this command only for testing and development purposes.</span></span>

```
StoreSystemSetup_V72.exe -S -C "C:\Temp\StoreSystemSetup_V72_Houston.xml" -SkipPrerequisiteCheck
```

## <a name="mass-deployment-of-retail-modern-pos"></a><span data-ttu-id="53eee-158">Retail Modern POS の一括配置</span><span class="sxs-lookup"><span data-stu-id="53eee-158">Mass deployment of Retail Modern POS</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="53eee-159">準備</span><span class="sxs-lookup"><span data-stu-id="53eee-159">Before you begin</span></span>

<span data-ttu-id="53eee-160">この機能を使用するには、バージョン 7.3 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="53eee-160">To use this functionality, you must be using version 7.3 or later.</span></span> <span data-ttu-id="53eee-161">本社でのすべての店舗、レジスター、およびデバイスのコンフィギュレーション、およびその他のコンフィギュレーションが既に完了したとみなされます。</span><span class="sxs-lookup"><span data-stu-id="53eee-161">It's assumed that the configuration of all stores, registers, and devices, and other configurations in the headquarters have already been completed.</span></span> <span data-ttu-id="53eee-162">任意のコンフィギュレーションがまだ必要な場合は、このトピックの手順を実行する前に実行します。</span><span class="sxs-lookup"><span data-stu-id="53eee-162">If any configuration is still required, complete it before you follow the instructions in this topic.</span></span>

### <a name="examples-of-commands-for-silent-mass-deployment"></a><span data-ttu-id="53eee-163">サイレント マス展開のコマンド例</span><span class="sxs-lookup"><span data-stu-id="53eee-163">Examples of commands for silent mass deployment</span></span>

<span data-ttu-id="53eee-164">このセクションでは、Retail Modern POS、オフラインの Retail Modern POS、およびオフライン サポートのないインストーラのセルフサービスの大量展開に使用されるコマンドの例を示します。</span><span class="sxs-lookup"><span data-stu-id="53eee-164">This section shows examples of commands that are used for self-service mass deployment of Retail Modern POS, even Retail Modern POS with offline and the installer without offline support.</span></span> <span data-ttu-id="53eee-165">Windows PowerShell スクリプトの例では、ユーザーがインストールを実行する支援も含まれます。</span><span class="sxs-lookup"><span data-stu-id="53eee-165">Examples of Windows PowerShell scripts are also included to help users do the installations.</span></span>

#### <a name="silently-install-retail-modern-pos"></a><span data-ttu-id="53eee-166">Retail Modern POS のサイレント インストール</span><span class="sxs-lookup"><span data-stu-id="53eee-166">Silently install Retail Modern POS</span></span>

<span data-ttu-id="53eee-167">次のコマンドにより、Retail Modern POS がサイレントでインストール (または更新) されます。</span><span class="sxs-lookup"><span data-stu-id="53eee-167">The following command silently installs (or updates) Retail Modern POS.</span></span> <span data-ttu-id="53eee-168">現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。</span><span class="sxs-lookup"><span data-stu-id="53eee-168">It has the standard command structure that is used for silent servicing of components that are currently installed.</span></span> <span data-ttu-id="53eee-169">この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。</span><span class="sxs-lookup"><span data-stu-id="53eee-169">The structure uses the basic values of **&lt;InstallerName&gt;.exe** and the command for silent installation, **-S**.</span></span>

<span data-ttu-id="53eee-170">このコマンドは、構成ファイルが存在する場合、インストーラーの実行可能ファイルと同じ場所にある構成ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="53eee-170">This command uses the configuration file that is in the same location as the executable file for the installer, if a configuration file exists there.</span></span> <span data-ttu-id="53eee-171">複数の構成ファイルが使用可能な場合は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="53eee-171">It should not be used if multiple configuration files are available.</span></span>

```
ModernPOSSetup_V73.exe -S
```

> [!NOTE]
> <span data-ttu-id="53eee-172">Retail Modern POS ではコンフィギュレーション ファイルは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="53eee-172">A configuration file isn't required for Retail Modern POS.</span></span> <span data-ttu-id="53eee-173">ただし、関連付けられている構成ファイルを読み込めない限り、インストールされた Retail Modern POS アプリは適切な方法では有効化されません。</span><span class="sxs-lookup"><span data-stu-id="53eee-173">However, the Retail Modern POS application that is installed can't be activated in the appropriate manner unless the associated configuration file can be read from.</span></span>

#### <a name="silently-install-retail-modern-pos-by-using-a-specific-configuration-file"></a><span data-ttu-id="53eee-174">特定のコンフィギュレーション ファイルを使用して Retail Modern POS をサイレント インストール</span><span class="sxs-lookup"><span data-stu-id="53eee-174">Silently install Retail Modern POS by using a specific configuration file</span></span>

<span data-ttu-id="53eee-175">次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Retail Modern POS の現在のインストールをサイレント インストールします。</span><span class="sxs-lookup"><span data-stu-id="53eee-175">The following command silently installs the current installation of Retail Modern POS by using a specific configuration file.</span></span> <span data-ttu-id="53eee-176">この構成ファイルは、インストーラーの実行可能ファイルと同じ場所にないか、複数の構成ファイルが使用可能な場合があります。</span><span class="sxs-lookup"><span data-stu-id="53eee-176">This configuration file might not be in the same location as the executable file for the installer, or multiple configuration files might be available.</span></span>

```
ModernPOSSetup_V72.exe -S -C "C:\Temp\ModernPOSSetup_V73_Houston-3.xml"
```

#### <a name="silently-install-retail-hardware-station"></a><span data-ttu-id="53eee-177">Retail ハードウェア ステーションのサイレント インストール</span><span class="sxs-lookup"><span data-stu-id="53eee-177">Silently install Retail hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="53eee-178">Retail ハードウェア ステーションをインストールすのに、**-SkipMerchantInfo** の区切り記号が必要です。</span><span class="sxs-lookup"><span data-stu-id="53eee-178">The **-SkipMerchantInfo** delimiter is required to install Retail hardware station.</span></span> <span data-ttu-id="53eee-179">GUI ベースのハードウェア ステーションのインストールの最後に開く、Merchant Account Information Utility を使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="53eee-179">The Merchant Account Information Utility that is opened at the end of a GUI-based installation of Hardware station no longer has to be used.</span></span> <span data-ttu-id="53eee-180">機能上の理由で、Retail Modern POS がハードウェア ステーションにペアリングされている場合、最新のマーチャント口座情報もコンポーネントにプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="53eee-180">Because of feature functionality, when Retail Modern POS is paired to Hardware station, it also pushes the latest merchant account information to the component.</span></span>

<span data-ttu-id="53eee-181">次のコマンドにより、Retail ハードウェア ステーションがサイレントでインストール (または更新) されます。</span><span class="sxs-lookup"><span data-stu-id="53eee-181">The following command silently installs (or updates) Retail hardware station.</span></span> <span data-ttu-id="53eee-182">現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。</span><span class="sxs-lookup"><span data-stu-id="53eee-182">It has the standard command structure that is used for silent servicing of components that are currently installed.</span></span> <span data-ttu-id="53eee-183">この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。</span><span class="sxs-lookup"><span data-stu-id="53eee-183">The structure uses the basic values of **&lt;InstallerName&gt;.exe** and the command for silent installation, **-S**.</span></span> <span data-ttu-id="53eee-184">また、**-SkipMerchantInfo** の区切り記号を使用して、ユーティリティを通じたマーチャント口座情報のダウンロードをスキップすることもできます。</span><span class="sxs-lookup"><span data-stu-id="53eee-184">It also uses the **-SkipMerchantInfo** delimiter to skip the download of merchant account information through the utility.</span></span> <span data-ttu-id="53eee-185">このコマンドは、インストーラーの実行可能ファイルと同じ場所にある構成ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="53eee-185">This command uses the configuration file that is in the same location as the executable file for the installer.</span></span>

```
HardwareStationSetup_V10.exe -S -SkipMerchantInfo
```

> [!NOTE]
> <span data-ttu-id="53eee-186">Retail ハードウェア ステーションをサイレントで配置するのに、構成ファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="53eee-186">A configuration file is required to silently deploy Retail hardware station.</span></span>

#### <a name="silently-install-retail-hardware-station-by-using-a-specific-configuration-file"></a><span data-ttu-id="53eee-187">特定の構成ファイルを使用して Retail ハードウェア ステーションをサイレント インストール</span><span class="sxs-lookup"><span data-stu-id="53eee-187">Silently install Retail hardware station by using a specific configuration file</span></span>

<span data-ttu-id="53eee-188">次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Retail ハードウェア ステーションの現在のインストールをサイレント インストールします。</span><span class="sxs-lookup"><span data-stu-id="53eee-188">The following command silently installs the current installation of Retail hardware station by using a specific configuration file.</span></span> <span data-ttu-id="53eee-189">この構成ファイルは、インストーラーの実行可能ファイルと同じ場所にないか、複数の構成ファイルが使用可能な場合があります。</span><span class="sxs-lookup"><span data-stu-id="53eee-189">This configuration file might not be in the same location as the executable file for the installer, or multiple configuration files might be available.</span></span>

```
HardwareStationSetup_V10.exe -S -SkipMerchantInfo -C "C:\Temp\HardwareStationSetup_V10__20-19-35.xml"
```

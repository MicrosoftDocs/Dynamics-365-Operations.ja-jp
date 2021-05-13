---
title: レガシ セルフサービス コンポーネントの一括配置
description: このトピックでは、セルフ サービスを使用してサイレント サービスの更新と初期展開を行う方法について説明します。 また、特別な配置のいくつかの側面についても説明します。
author: jashanno
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Application update 3
ms.openlocfilehash: 369d60cdb1ba84c35f38e7a28c1bbac41f0a19b3
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864338"
---
# <a name="mass-deployment-of-legacy-self-service-components"></a><span data-ttu-id="796f1-104">レガシ セルフサービス コンポーネントの一括配置</span><span class="sxs-lookup"><span data-stu-id="796f1-104">Mass deployment of legacy self-service components</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="796f1-105">このトピックは、レガシ セルフサービス インストーラーに対応しています。</span><span class="sxs-lookup"><span data-stu-id="796f1-105">This topic is for legacy self-service installers.</span></span> <span data-ttu-id="796f1-106">レガシ セルフサービスを使用してサイレント サービスの更新と初期展開を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="796f1-106">It explains how you can use legacy self-service to do silent servicing updates and initial deployments.</span></span> <span data-ttu-id="796f1-107">また、特別な配置のいくつかの側面についても説明します。</span><span class="sxs-lookup"><span data-stu-id="796f1-107">It also explains some aspects of special deployment.</span></span> <span data-ttu-id="796f1-108">このトピックは、機能が開発され、より多くの機能が利用可能になると更新されます。</span><span class="sxs-lookup"><span data-stu-id="796f1-108">This topic will be updated as the feature is developed and more functionality becomes available.</span></span> <span data-ttu-id="796f1-109">現在、サイレント サービス更新の機能のみが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="796f1-109">Currently, only the capability for silent servicing updates is available.</span></span> 

## <a name="delimiters-for-mass-deployment"></a><span data-ttu-id="796f1-110">一括配置の区切り記号</span><span class="sxs-lookup"><span data-stu-id="796f1-110">Delimiters for mass deployment</span></span>

<span data-ttu-id="796f1-111">次のテーブルに、一括配置の実行コマンドで現在使用できる区切り記号を示します。</span><span class="sxs-lookup"><span data-stu-id="796f1-111">The following table shows the delimiters that can currently be used in execution commands for mass deployment.</span></span> 


| <span data-ttu-id="796f1-112">区切り記号</span><span class="sxs-lookup"><span data-stu-id="796f1-112">Delimiter</span></span>                 | <span data-ttu-id="796f1-113">説明</span><span class="sxs-lookup"><span data-stu-id="796f1-113">Description</span></span> |
|---------------------------|-------------|
| <span data-ttu-id="796f1-114">-S または -サイレント</span><span class="sxs-lookup"><span data-stu-id="796f1-114">-S or -Silent</span></span>             | <span data-ttu-id="796f1-115">インストーラーをサイレントで実行します。</span><span class="sxs-lookup"><span data-stu-id="796f1-115">Silently run the installer.</span></span> <span data-ttu-id="796f1-116">グラフィカル ユーザー インターフェイス (GUI) を使用しません。</span><span class="sxs-lookup"><span data-stu-id="796f1-116">No graphical user interface (GUI) is used.</span></span> <span data-ttu-id="796f1-117">**-Q** および **-Quiet** 区切り記号には同じ効果があり、使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="796f1-117">The **-Q** and **-Quiet** delimiters have the same effect and can also be used.</span></span> |
| <span data-ttu-id="796f1-118">-C または -Config</span><span class="sxs-lookup"><span data-stu-id="796f1-118">-C or -Config</span></span>             | <span data-ttu-id="796f1-119">このインストールの一部として使用するコンフィギュレーション ファイルの場所とファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="796f1-119">Specify the location and file name of the configuration file to use as part of this installation.</span></span> |
| <span data-ttu-id="796f1-120">-FilePath</span><span class="sxs-lookup"><span data-stu-id="796f1-120">-FilePath</span></span>                 | <span data-ttu-id="796f1-121">カスタム インストールの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="796f1-121">Specify a custom installation location.</span></span><p><span data-ttu-id="796f1-122">標準のインストールにこの区切り記号を使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="796f1-122">We don't recommend that you use this delimiter for a standard installation.</span></span></p> |
| <span data-ttu-id="796f1-123">-LogFile</span><span class="sxs-lookup"><span data-stu-id="796f1-123">-LogFile</span></span>                  | <span data-ttu-id="796f1-124">インストール ログのカスタム ファイルの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="796f1-124">Specify a custom file location for the installation logs.</span></span><p><span data-ttu-id="796f1-125">標準のインストールにこの区切り記号を使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="796f1-125">We don't recommend that you use this delimiter for a standard installation.</span></span></p> |
| <span data-ttu-id="796f1-126">-SkipPrerequisiteCheck</span><span class="sxs-lookup"><span data-stu-id="796f1-126">-SkipPrerequisiteCheck</span></span>    | <span data-ttu-id="796f1-127">前提条件および必須コンポーネントのインストールのチェックをスキップします。</span><span class="sxs-lookup"><span data-stu-id="796f1-127">Skip the check for prerequisites and prerequisite installation.</span></span><p><span data-ttu-id="796f1-128">この区切り記号は、開発とテストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="796f1-128">You should use this delimiter only for development and testing.</span></span> <span data-ttu-id="796f1-129">標準のインストールにそれを使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="796f1-129">We don't recommend that you use it for a standard installation.</span></span></p> |
| <span data-ttu-id="796f1-130">-SkipSystemInfoCollection</span><span class="sxs-lookup"><span data-stu-id="796f1-130">-SkipSystemInfoCollection</span></span> | <span data-ttu-id="796f1-131">インストールの開始時にシステム情報を収集するプロセスをスキップします。</span><span class="sxs-lookup"><span data-stu-id="796f1-131">Skip the process of collecting system information at the beginning of the installation.</span></span><p><span data-ttu-id="796f1-132">この区切り記号は、開発とテストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="796f1-132">You should use this delimiter only for development and testing.</span></span> <span data-ttu-id="796f1-133">標準のインストールにそれを使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="796f1-133">We don't recommend that you use it for a standard installation.</span></span></p> |
| <span data-ttu-id="796f1-134">-SkipMerchantInfo</span><span class="sxs-lookup"><span data-stu-id="796f1-134">-SkipMerchantInfo</span></span>         | <span data-ttu-id="796f1-135">ハードウェア ステーションのレガシ セルフサービス インストーラーの終わりにマーチャント アカウント情報のインストールをスキップします。</span><span class="sxs-lookup"><span data-stu-id="796f1-135">Skip the installation of merchant account information at the end of the legacy self-service installer for Hardware station.</span></span><p><span data-ttu-id="796f1-136">この区切り記号は、開発とテストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="796f1-136">You should use this delimiter only for development and testing.</span></span> <span data-ttu-id="796f1-137">標準のインストールにそれを使用することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="796f1-137">We don't recommend that you use it for a standard installation.</span></span></p> |
| <span data-ttu-id="796f1-138">-SkipAppxInstallation</span><span class="sxs-lookup"><span data-stu-id="796f1-138">-SkipAppxInstallation</span></span>     | <span data-ttu-id="796f1-139">Dynamics 365 の2018 年 10 月のリリースから、この区切り記号は APPX Retail Modern POS アプリケーションのインストールをスキップします。</span><span class="sxs-lookup"><span data-stu-id="796f1-139">Beginning in the October 2018 release of Dynamics 365, this delimiter will skip the installation of the APPX Retail Modern POS application.</span></span> <span data-ttu-id="796f1-140">この区切り記号は、システム アカウントまたはサービス アカウント (ユーザー プロファイルがないアカウント) を使用してアプリケーションのインストールを実行するために必要です。</span><span class="sxs-lookup"><span data-stu-id="796f1-140">This delimiter is required to perform the application installation through the SYSTEM account or a service account (Any account that does not have a user profile).</span></span> |

## <a name="silent-servicing"></a><span data-ttu-id="796f1-141">サイレント サービス</span><span class="sxs-lookup"><span data-stu-id="796f1-141">Silent servicing</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="796f1-142">準備</span><span class="sxs-lookup"><span data-stu-id="796f1-142">Before you begin</span></span>

<span data-ttu-id="796f1-143">サイレント サービスが現在インストールされているすべてのコンポーネントを維持していることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="796f1-143">Note that silent servicing maintains all components that are currently installed.</span></span> <span data-ttu-id="796f1-144">任意のコンフィギュレーションがまだ必要な場合は、このトピックの手順を開始する前に実行します。</span><span class="sxs-lookup"><span data-stu-id="796f1-144">If any configuration is still required, complete it before you begin to follow the instructions in this topic.</span></span>

### <a name="examples-of-commands-for-silent-servicing"></a><span data-ttu-id="796f1-145">サイレント サービスのコマンド例</span><span class="sxs-lookup"><span data-stu-id="796f1-145">Examples of commands for silent servicing</span></span>

<span data-ttu-id="796f1-146">このセクションでは、レガシ セルフサービスの大量展開に使用されるコマンドの例を示します。</span><span class="sxs-lookup"><span data-stu-id="796f1-146">This section shows examples of commands that are used for legacy self-service mass deployment.</span></span> <span data-ttu-id="796f1-147">これらのコマンドは、Modern POS (オフラインでサポートされているインストーラーとオフラインでサポートされていないインストーラーの両方) 用インストーラー、ハードウェア ステーション、Commerce Scale Unit (自己ホスト) など、すべての標準インストーラーで動作します。</span><span class="sxs-lookup"><span data-stu-id="796f1-147">These commands work for all the standard installers, such as the installers for Modern POS (both the installer that has offline support and the installer that doesn't have offline support), Hardware station, and Commerce Scale Unit (self-hosted).</span></span>

#### <a name="silently-update-the-current-installation-of-modern-pos"></a><span data-ttu-id="796f1-148">Modern POS の現在のインストールをサイレントに更新</span><span class="sxs-lookup"><span data-stu-id="796f1-148">Silently update the current installation of Modern POS</span></span>

<span data-ttu-id="796f1-149">次のコマンドは、Modern POS の現在のインストールをサイレント更新します。</span><span class="sxs-lookup"><span data-stu-id="796f1-149">The following command silently updates the current installation of Modern POS.</span></span> <span data-ttu-id="796f1-150">このコマンドには、現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。</span><span class="sxs-lookup"><span data-stu-id="796f1-150">This command has the standard command structure that is used for silent servicing of components that are currently installed.</span></span> <span data-ttu-id="796f1-151">この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。</span><span class="sxs-lookup"><span data-stu-id="796f1-151">The structure uses the basic values of **&lt;InstallerName&gt;.exe** and the command for silent installation, **-S**.</span></span> <span data-ttu-id="796f1-152">このコマンドは、構成ファイルが存在する場合は、インストーラーと同じファイルの場所にある構成ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="796f1-152">This command uses the configuration file that is located in the same file location as the installer, if a configuration file exists there.</span></span>

```Console
ModernPOSSetup_V72.exe -S
```

> [!NOTE]
> <span data-ttu-id="796f1-153">Retail Store Scale Unit ではコンフィギュレーション ファイルがまだ必要とされます。</span><span class="sxs-lookup"><span data-stu-id="796f1-153">A configuration file is still required for Retail Store Scale Unit.</span></span> <span data-ttu-id="796f1-154">ただし、インストーラーは可能な場合はいつでも、現在インストールされているすべての値を保持します。</span><span class="sxs-lookup"><span data-stu-id="796f1-154">However, the installer keeps all the values that are currently installed, whenever it can.</span></span>

#### <a name="silently-update-the-current-installation-of-commerce-scale-unit-self-hosted"></a><span data-ttu-id="796f1-155">Commerce Scale Unit (自己ホスト) の現在のインストールを自動的に更新</span><span class="sxs-lookup"><span data-stu-id="796f1-155">Silently update the current installation of Commerce Scale Unit (self-hosted)</span></span>

<span data-ttu-id="796f1-156">次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Commerce Scale Unit (自己ホスト) の現在のインストールをサイレント更新します。</span><span class="sxs-lookup"><span data-stu-id="796f1-156">The following command silently updates the current installation of Commerce Scale Unit (self-hosted) by using a specific configuration file.</span></span> <span data-ttu-id="796f1-157">(このコンフィギュレーション ファイルは、インストーラーの実行可能ファイルと同じ場所にない可能性があります。) このコマンドは、前提条件のチェックをスキップし、インストール手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="796f1-157">(This configuration file might not be in the same location as the executable file for the installer.) This command skips the prerequisite check and moves on to the installation steps.</span></span> <span data-ttu-id="796f1-158">テストおよび開発の目的にのみ、このコマンドを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="796f1-158">We recommend that you use this command only for testing and development purposes.</span></span>

```Console
StoreSystemSetup_V72.exe -S -C "C:\Temp\StoreSystemSetup_V72_Houston.xml" -SkipPrerequisiteCheck
```

## <a name="mass-deployment-of-modern-pos"></a><span data-ttu-id="796f1-159">Modern POS の一括配置</span><span class="sxs-lookup"><span data-stu-id="796f1-159">Mass deployment of Modern POS</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="796f1-160">準備</span><span class="sxs-lookup"><span data-stu-id="796f1-160">Before you begin</span></span>

<span data-ttu-id="796f1-161">この機能を使用するには、バージョン 7.3 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="796f1-161">To use this functionality, you must be using version 7.3 or later.</span></span> <span data-ttu-id="796f1-162">本社でのすべての店舗、レジスター、およびデバイスのコンフィギュレーション、およびその他のコンフィギュレーションが既に完了したとみなされます。</span><span class="sxs-lookup"><span data-stu-id="796f1-162">It's assumed that the configuration of all stores, registers, and devices, and other configurations in the headquarters have already been completed.</span></span> <span data-ttu-id="796f1-163">任意のコンフィギュレーションがまだ必要な場合は、このトピックの手順を実行する前に実行します。</span><span class="sxs-lookup"><span data-stu-id="796f1-163">If any configuration is still required, complete it before you follow the instructions in this topic.</span></span>

### <a name="examples-of-commands-for-silent-mass-deployment"></a><span data-ttu-id="796f1-164">サイレント マス展開のコマンド例</span><span class="sxs-lookup"><span data-stu-id="796f1-164">Examples of commands for silent mass deployment</span></span>

<span data-ttu-id="796f1-165">このセクションでは、Modern POS、オフラインでの Modern POS およびオフライン サポートのないインストーラーのレガシ セルフサービスの一括配置に使用されるコマンドの例を示します。</span><span class="sxs-lookup"><span data-stu-id="796f1-165">This section shows examples of commands that are used for legacy self-service mass deployment of Modern POS, even Modern POS with offline and the installer without offline support.</span></span> <span data-ttu-id="796f1-166">Windows PowerShell スクリプトの例では、ユーザーがインストールを実行する支援も含まれます。</span><span class="sxs-lookup"><span data-stu-id="796f1-166">Examples of Windows PowerShell scripts are also included to help users do the installations.</span></span>

#### <a name="silently-install-modern-pos"></a><span data-ttu-id="796f1-167">Modern POS をサイレント インストール</span><span class="sxs-lookup"><span data-stu-id="796f1-167">Silently install Modern POS</span></span>

<span data-ttu-id="796f1-168">次のコマンドにより、Modern POS がサイレントでインストール (または更新) されます。</span><span class="sxs-lookup"><span data-stu-id="796f1-168">The following command silently installs (or updates) Modern POS.</span></span> <span data-ttu-id="796f1-169">現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。</span><span class="sxs-lookup"><span data-stu-id="796f1-169">It has the standard command structure that is used for silent servicing of components that are currently installed.</span></span> <span data-ttu-id="796f1-170">この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。</span><span class="sxs-lookup"><span data-stu-id="796f1-170">The structure uses the basic values of **&lt;InstallerName&gt;.exe** and the command for silent installation, **-S**.</span></span>

<span data-ttu-id="796f1-171">このコマンドは、構成ファイルが存在する場合、インストーラーの実行可能ファイルと同じ場所にある構成ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="796f1-171">This command uses the configuration file that is in the same location as the executable file for the installer, if a configuration file exists there.</span></span> <span data-ttu-id="796f1-172">複数の構成ファイルが使用可能な場合は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="796f1-172">It should not be used if multiple configuration files are available.</span></span>

```Console
ModernPOSSetup_V73.exe -S
```

> [!NOTE]
> <span data-ttu-id="796f1-173">Modern POS ではコンフィギュレーション ファイルは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="796f1-173">A configuration file isn't required for Modern POS.</span></span> <span data-ttu-id="796f1-174">ただし、関連付けられている構成ファイルを読み込めない限り、インストールされた Modern POS アプリケーションは適切な方法では有効化されません。</span><span class="sxs-lookup"><span data-stu-id="796f1-174">However, the Modern POS application that is installed can't be activated in the appropriate manner unless the associated configuration file can be read from.</span></span>

#### <a name="silently-install-modern-pos-by-using-a-specific-configuration-file"></a><span data-ttu-id="796f1-175">特定のコンフィギュレーション ファイルを使用して Modern POS をサイレント インストール</span><span class="sxs-lookup"><span data-stu-id="796f1-175">Silently install Modern POS by using a specific configuration file</span></span>

<span data-ttu-id="796f1-176">次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Modern POS の現在のインストールをサイレント インストールします。</span><span class="sxs-lookup"><span data-stu-id="796f1-176">The following command silently installs the current installation of Modern POS by using a specific configuration file.</span></span> <span data-ttu-id="796f1-177">この構成ファイルは、インストーラーの実行可能ファイルと同じ場所にないか、複数の構成ファイルが使用可能な場合があります。</span><span class="sxs-lookup"><span data-stu-id="796f1-177">This configuration file might not be in the same location as the executable file for the installer, or multiple configuration files might be available.</span></span>

```Console
ModernPOSSetup_V72.exe -S -C "C:\Temp\ModernPOSSetup_V73_Houston-3.xml"
```

#### <a name="silently-install-retail-hardware-station"></a><span data-ttu-id="796f1-178">Retail ハードウェア ステーションのサイレント インストール</span><span class="sxs-lookup"><span data-stu-id="796f1-178">Silently install Retail hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="796f1-179">Retail ハードウェア ステーションをインストールすのに、**-SkipMerchantInfo** の区切り記号が必要です。</span><span class="sxs-lookup"><span data-stu-id="796f1-179">The **-SkipMerchantInfo** delimiter is required to install Retail hardware station.</span></span> <span data-ttu-id="796f1-180">GUI ベースのハードウェア ステーションのインストールの最後に開く、Merchant Account Information Utility を使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="796f1-180">The Merchant Account Information Utility that is opened at the end of a GUI-based installation of Hardware station no longer has to be used.</span></span> <span data-ttu-id="796f1-181">機能上の理由で、Modern POS がハードウェア ステーションにペアリングされている場合、最新のマーチャント口座情報もコンポーネントにプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="796f1-181">Because of feature functionality, when Modern POS is paired to Hardware station, it also pushes the latest merchant account information to the component.</span></span>

<span data-ttu-id="796f1-182">次のコマンドにより、Retail ハードウェア ステーションがサイレントでインストール (または更新) されます。</span><span class="sxs-lookup"><span data-stu-id="796f1-182">The following command silently installs (or updates) Retail hardware station.</span></span> <span data-ttu-id="796f1-183">現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。</span><span class="sxs-lookup"><span data-stu-id="796f1-183">It has the standard command structure that is used for silent servicing of components that are currently installed.</span></span> <span data-ttu-id="796f1-184">この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。</span><span class="sxs-lookup"><span data-stu-id="796f1-184">The structure uses the basic values of **&lt;InstallerName&gt;.exe** and the command for silent installation, **-S**.</span></span> <span data-ttu-id="796f1-185">また、**-SkipMerchantInfo** の区切り記号を使用して、ユーティリティを通じたマーチャント口座情報のダウンロードをスキップすることもできます。</span><span class="sxs-lookup"><span data-stu-id="796f1-185">It also uses the **-SkipMerchantInfo** delimiter to skip the download of merchant account information through the utility.</span></span> <span data-ttu-id="796f1-186">このコマンドは、インストーラーの実行可能ファイルと同じ場所にある構成ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="796f1-186">This command uses the configuration file that is in the same location as the executable file for the installer.</span></span>

```Console
HardwareStationSetup_V10.exe -S -SkipMerchantInfo
```

> [!NOTE]
> <span data-ttu-id="796f1-187">Retail ハードウェア ステーションをサイレントで配置するのに、構成ファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="796f1-187">A configuration file is required to silently deploy Retail hardware station.</span></span>

#### <a name="silently-install-retail-hardware-station-by-using-a-specific-configuration-file"></a><span data-ttu-id="796f1-188">特定の構成ファイルを使用して Retail ハードウェア ステーションをサイレント インストール</span><span class="sxs-lookup"><span data-stu-id="796f1-188">Silently install Retail hardware station by using a specific configuration file</span></span>

<span data-ttu-id="796f1-189">次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Retail ハードウェア ステーションの現在のインストールをサイレント インストールします。</span><span class="sxs-lookup"><span data-stu-id="796f1-189">The following command silently installs the current installation of Retail hardware station by using a specific configuration file.</span></span> <span data-ttu-id="796f1-190">この構成ファイルは、インストーラーの実行可能ファイルと同じ場所にないか、複数の構成ファイルが使用可能な場合があります。</span><span class="sxs-lookup"><span data-stu-id="796f1-190">This configuration file might not be in the same location as the executable file for the installer, or multiple configuration files might be available.</span></span>

```Console
HardwareStationSetup_V10.exe -S -SkipMerchantInfo -C "C:\Temp\HardwareStationSetup_V10__20-19-35.xml"
```


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

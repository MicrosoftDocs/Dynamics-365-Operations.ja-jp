---
title: 管理者以外のユーザーが Regression suite automation tool (RSAT) を使用するように構成する
description: このトピックでは、RSAT バージョン 2.2 およびそれ以降のユーザーに特権リソースを付与する方法について説明します。
author: FrankDahl
ms.date: 03/09/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2021-03-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d477ca0326911cd4d5b60b94fd57fd76863a643
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752682"
---
# <a name="configure-non-administrator-users-to-use-rsat"></a><span data-ttu-id="2000c-103">管理者以外のユーザーが RSAT を使用するように構成する</span><span class="sxs-lookup"><span data-stu-id="2000c-103">Configure non-administrator users to use RSAT</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="2000c-104">Regression suite automation tool (RSAT) は、実行しているコンピューターの特権リソースを使用します。</span><span class="sxs-lookup"><span data-stu-id="2000c-104">The Regression suite automation tool (RSAT) uses privileged resources on the machine that it is running on.</span></span> <span data-ttu-id="2000c-105">RSAT のテストを実行するには、ユーザーはコンピューターの管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2000c-105">A user must be an administrator on the machine to run RSAT tests.</span></span> <span data-ttu-id="2000c-106">このトピックでは、RSAT バージョン 2.2 および **それ以降** を使用している場合、これらの特権リソースを付与する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2000c-106">This topic explains how to grant these privileged resources to users if you are using **RSAT version 2.2 or later**.</span></span> <span data-ttu-id="2000c-107">管理者以外のユーザーは、コンピューターの管理者になることなく、RSAT テストを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="2000c-107">The non-administrator user can run RSAT tests without being an administrator on the machine.</span></span>

<span data-ttu-id="2000c-108">これらの指示は、管理者以外のユーザーが RSAT をインストールできるようにするものではありません。</span><span class="sxs-lookup"><span data-stu-id="2000c-108">These instructions will not allow a non-administrator user to install RSAT.</span></span> <span data-ttu-id="2000c-109">この指示は、インストール後に RSAT の使用を有効にするだけです。</span><span class="sxs-lookup"><span data-stu-id="2000c-109">The instructions only enable using RSAT after it has been installed.</span></span> <span data-ttu-id="2000c-110">この状況には、Selenium フレームワークがインストールされているか、またはブラウザーのバージョンを更新した後に新しいブラウザーのドライバー インストールを使用している RSAT を初めて使用するときにが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2000c-110">This situation includes first-time use of RSAT where the Selenium framework is installed, or with new browser driver installation after updating browser versions.</span></span> <span data-ttu-id="2000c-111">これらのインストール手順には、RSAT を管理者権限で実行していることが必要です。</span><span class="sxs-lookup"><span data-stu-id="2000c-111">Those installation steps still require running RSAT with administrator privileges.</span></span>

<span data-ttu-id="2000c-112">複数のユーザーが共有する仮想マシン (VM) に RSAT がインストールされている場合、複数のユーザーが同時に RSAT を実行すると、ユーザーがブロックされることがあります。</span><span class="sxs-lookup"><span data-stu-id="2000c-112">When RSAT is installed on a virtual machine (VM) that is shared by multiple users, then users can become blocked when multiple users run RSAT at the same time.</span></span> <span data-ttu-id="2000c-113">たとえば、ユーザーがテスト ケースを実行中のリソースを保留にし、他のユーザーへのアクセスがブロックされることがあります。</span><span class="sxs-lookup"><span data-stu-id="2000c-113">For example, a user might hold resources while running tests cases, which then blocks access to other users.</span></span> <span data-ttu-id="2000c-114">これらの指示は、動作を変更しません。</span><span class="sxs-lookup"><span data-stu-id="2000c-114">These instructions do not change that behavior.</span></span>

## <a name="enable-non-administrator-rsat-use"></a><span data-ttu-id="2000c-115">管理者以外の RSAT の使用を有効にする</span><span class="sxs-lookup"><span data-stu-id="2000c-115">Enable non-administrator RSAT use</span></span>

<span data-ttu-id="2000c-116">管理者以外の RSAT の使用を有効にするには、2 つの PowerShell スクリプトと新しいショートカット ファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="2000c-116">To enable non-administrator RSAT use, you need two PowerShell scripts and a new shortcut file.</span></span> <span data-ttu-id="2000c-117">これらのファイルは、**管理者以外を有効にする** という名前のサブフォルダーにある RSAT インストール フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="2000c-117">These files are in the RSAT installation folder in the subfolder named **Enable non admin**.</span></span>

1. <span data-ttu-id="2000c-118">Windows PowerShell を管理者として開きます。</span><span class="sxs-lookup"><span data-stu-id="2000c-118">Open Windows PowerShell as Administrator.</span></span>
2. <span data-ttu-id="2000c-119">フォルダーを RSAT インストール フォルダーの **管理者以外を有効にする** に変更します。</span><span class="sxs-lookup"><span data-stu-id="2000c-119">Change the folder to **Enable non admin** in the RSAT installation folder.</span></span> <span data-ttu-id="2000c-120">インストール フォルダーは、コンピューターで実行しているローカライズされた Windows にしたがって、**C:\Program Files (x86)\Regression Suite Automation Tool\Enable non admin** のように名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="2000c-120">The installation folder is named according to the localized Windows running on the machine, for example **C:\Program Files (x86)\Regression Suite Automation Tool\Enable non admin**.</span></span>

    ![PowerShell のファイルの一覧](media/config-file-list.png)

3. <span data-ttu-id="2000c-122">**管理者以外を有効にする** フォルダーに、これらのファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2000c-122">In the folder **Enable non admin** you will find these files:</span></span>

    + <span data-ttu-id="2000c-123">Enable-non-admin-mode.ps1</span><span class="sxs-lookup"><span data-stu-id="2000c-123">Enable-non-admin-mode.ps1</span></span>
    + <span data-ttu-id="2000c-124">Enable-non-admin-user.ps1</span><span class="sxs-lookup"><span data-stu-id="2000c-124">Enable-non-admin-user.ps1</span></span>
    + <span data-ttu-id="2000c-125">Regression Suite Automation Tool (Non admin).lnk</span><span class="sxs-lookup"><span data-stu-id="2000c-125">Regression Suite Automation Tool (Non admin).lnk</span></span>

4. <span data-ttu-id="2000c-126">最初のファイル **Enable-non-admin-mode.ps1** は、コンピューターに対して管理者以外のモードを有効にする PowerShell スクリプトです。</span><span class="sxs-lookup"><span data-stu-id="2000c-126">The first file, **Enable-non-admin-mode.ps1** is a PowerShell script that enables non-administrator mode for the machine.</span></span> <span data-ttu-id="2000c-127">このファイルを各コンピューターで 1 回実行します。</span><span class="sxs-lookup"><span data-stu-id="2000c-127">Run this file once on each machine.</span></span>

    <span data-ttu-id="2000c-128">これらの必須パラメーターを使用して、**管理者以外を有効にする** フォルダーからスクリプト **Enable-non-admin-mode.ps1** を直接実行します。</span><span class="sxs-lookup"><span data-stu-id="2000c-128">Run the script **Enable-non-admin-mode.ps1** directly from the **Enable non admin** folder, using these required parameters:</span></span>

    + <span data-ttu-id="2000c-129">**action**: (文字列) 管理者以外のモードを有効または無効にするオプション。</span><span class="sxs-lookup"><span data-stu-id="2000c-129">**action**: (string) Option to enable or disable non-administrator mode.</span></span> <span data-ttu-id="2000c-130">有効な値は、**有効** または **無効** です。</span><span class="sxs-lookup"><span data-stu-id="2000c-130">Valid values are **enable** and **disable**.</span></span>
    + <span data-ttu-id="2000c-131">**thumbprint**: (文字列) 証明書の拇印。</span><span class="sxs-lookup"><span data-stu-id="2000c-131">**thumbprint**: (string) Certificate thumbprint.</span></span> <span data-ttu-id="2000c-132">この値は、一般設定の RSAT で指定したのと同じ値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2000c-132">This value must be the same value that is specified in RSAT under General settings.</span></span>

    <span data-ttu-id="2000c-133">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="2000c-133">Here's an example.</span></span>

    ```powershell
    .\Enable-non-admin-mode.ps1 "enable" "23055S5DXXXXXXXXXXXXXXXXXXXXXX"
    ```

    <span data-ttu-id="2000c-134">ヘルプを入手するには、このコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2000c-134">To get help, execute this command.</span></span>

    ```powershell
    help .\Enable-non-admin-mode.ps1 -full
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="2000c-135">**管理者以外を有効にする** フォルダーからこの PowerShell スクリプトを削除したり、コピーしないでください。</span><span class="sxs-lookup"><span data-stu-id="2000c-135">DO NOT remove or copy this PowerShell script from the **Enable non admin** folder.</span></span> <span data-ttu-id="2000c-136">このフォルダーからのみ実行してください。</span><span class="sxs-lookup"><span data-stu-id="2000c-136">Run it only from this folder.</span></span>

5. <span data-ttu-id="2000c-137">2 つ目のファイル **Enable-non-admin-user.ps1** は、ユーザーに対して管理者以外のモードを有効にする PowerShell スクリプトです。</span><span class="sxs-lookup"><span data-stu-id="2000c-137">The second file, **Enable-non-admin-user.ps1** is a PowerShell script that enables non-administrator mode for a user.</span></span> <span data-ttu-id="2000c-138">コンピューターで RSAT を使用する各ユーザーに対してこのスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="2000c-138">Run this script for each user that is going to use RSAT on the machine.</span></span>

    <span data-ttu-id="2000c-139">これらの必須パラメーターを使用して、**管理者以外を有効にする** フォルダーからスクリプト **Enable-non-admin-user.ps1** を直接実行します。</span><span class="sxs-lookup"><span data-stu-id="2000c-139">Run the script **Enable-non-admin-user.ps1** directly from the **Enable non admin** folder, using these required parameters:</span></span>

    + <span data-ttu-id="2000c-140">**action**: (文字列) 管理者以外のモードを有効または無効にするオプション。</span><span class="sxs-lookup"><span data-stu-id="2000c-140">**action**: (string) Option to enable or disable non-administrator mode.</span></span> <span data-ttu-id="2000c-141">有効な値は、**有効** または **無効** です。</span><span class="sxs-lookup"><span data-stu-id="2000c-141">Valid values are **enable** and **disable**.</span></span>
    + <span data-ttu-id="2000c-142">**thumbprint**: (文字列) 証明書の拇印。</span><span class="sxs-lookup"><span data-stu-id="2000c-142">**thumbprint**: (string) Certificate thumbprint.</span></span> <span data-ttu-id="2000c-143">この値は、一般設定の RSAT で指定したのと同じ値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2000c-143">This value must be the same value that is specified in RSAT under General settings.</span></span>
    + <span data-ttu-id="2000c-144">**user**: (文字列) `domain\userName` 形式のローカル ユーザー名。</span><span class="sxs-lookup"><span data-stu-id="2000c-144">**user**: (string) The local username in the format `domain\userName`.</span></span>

    <span data-ttu-id="2000c-145">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="2000c-145">Here's an example.</span></span>

    ```powershell
    .\Enable-non-admin-user.ps1 "enable" "TESTDOMAIN\testuser" "23055S5DXXXXXXXXXXXXXXXXXXXXXX"
    ```

    <span data-ttu-id="2000c-146">ヘルプを入手するには、このコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2000c-146">To get help, execute this command.</span></span>

    ```powershell
    help .\Enable-non-admin-user.ps1 -full
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="2000c-147">**管理者以外を有効にする** フォルダーからこの PowerShell スクリプトを削除したり、コピーしないでください。</span><span class="sxs-lookup"><span data-stu-id="2000c-147">DO NOT remove or copy this PowerShell script from the **Enable non admin** folder.</span></span> <span data-ttu-id="2000c-148">このフォルダーからのみ実行してください。</span><span class="sxs-lookup"><span data-stu-id="2000c-148">Run it only from this folder.</span></span>

6. <span data-ttu-id="2000c-149">PowerShell を閉じます。</span><span class="sxs-lookup"><span data-stu-id="2000c-149">Close PowerShell.</span></span>

7. <span data-ttu-id="2000c-150">ショートカット ファイル **Regression Suite Automation Tool (Non admin).lnk** をユーザーのデスクトップにコピーします。</span><span class="sxs-lookup"><span data-stu-id="2000c-150">Copy the shortcut file **Regression Suite Automation Tool (Non admin).lnk** to the user's desktop.</span></span> <span data-ttu-id="2000c-151">(古いショートカットは、一部のユーザーは実行を許可されていない Visual Basic スクリプトを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2000c-151">(The old shortcut calls a Visual Basic script that some users may not be allowed to execute.</span></span> <span data-ttu-id="2000c-152">新しいショートカットは、実行可能ファイルを直接呼び出します。)</span><span class="sxs-lookup"><span data-stu-id="2000c-152">The new shortcut will call the executable file directly.)</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2000c-153">古いショートカットは、コンピューターのすべてのユーザーが使用できる共有ファイルなので、削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="2000c-153">DO NOT remove the old shortcut, because it is a shared file that is used by all users on the machine.</span></span> <span data-ttu-id="2000c-154">ファイルを削除すると、すべてのユーザーに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="2000c-154">If you remove the file, then it will disappear for all users.</span></span> <span data-ttu-id="2000c-155">すべてのユーザーに対して管理者以外のユーザーとしての実行が有効にされる場合、古いショートカットを削除しても問題ありません。</span><span class="sxs-lookup"><span data-stu-id="2000c-155">It is fine to remove the old shortcut if all users will be enabled to run as a non-administrator.</span></span> <span data-ttu-id="2000c-156">ただし、ショートカットは、新しいバージョンの RSAT がインストールされるたびに再び表示されます。</span><span class="sxs-lookup"><span data-stu-id="2000c-156">However, the shortcut will reappear every time a new version of RSAT is installed.</span></span>

8. <span data-ttu-id="2000c-157">RSAT を最初に開始するとき、Selenium フレームワークとブラウザーのバージョンに一致するドライバーをダウンロードし、インストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2000c-157">When you start RSAT the first time, you must download and install the Selenium framework and the drivers that match the version of your browser.</span></span> <span data-ttu-id="2000c-158">管理者ではないユーザーは、これらのコンポーネントのダウンロードとインストールができない場合があります。</span><span class="sxs-lookup"><span data-stu-id="2000c-158">Users that are not administrators might not be able to download and install these components.</span></span> <span data-ttu-id="2000c-159">この場合、RSAT は失敗し、例外が生成されることがあります。</span><span class="sxs-lookup"><span data-stu-id="2000c-159">In this case, RSAT might fail and generate exceptions.</span></span> <span data-ttu-id="2000c-160">コンポーネントをダウンロードし、インストールするには、管理者権限で RSAT を実行し、インストールを完了してください。</span><span class="sxs-lookup"><span data-stu-id="2000c-160">To download and install the components, run RSAT with administrator privileges to complete the installation.</span></span> <span data-ttu-id="2000c-161">管理者権限で実行するには、新しいショートカット **Regression Suite Automation Tool (Non admin)** を右クリックし、**管理者として実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2000c-161">To run with administrator privileges, right-click the new shortcut **Regression Suite Automation Tool (Non admin)** and select **Run as administrator**.</span></span> <span data-ttu-id="2000c-162">インストールが完了した後、RSAT を閉じ、もう一度ユーザーに RSAT を実行させます。</span><span class="sxs-lookup"><span data-stu-id="2000c-162">After the installation finishes, close RSAT and then have the user start RSAT again.</span></span>

9. <span data-ttu-id="2000c-163">新しいショートカット **Regression Suite Automation Tool (Non admin)** を使用して RSAT を開始します。</span><span class="sxs-lookup"><span data-stu-id="2000c-163">Use the new shortcut **Regression Suite Automation Tool (Non admin)** to starting RSAT.</span></span>

## <a name="disable-non-administrator-rsat-use"></a><span data-ttu-id="2000c-164">管理者以外の RSAT の使用を無効にする</span><span class="sxs-lookup"><span data-stu-id="2000c-164">Disable non-administrator RSAT use</span></span>

<span data-ttu-id="2000c-165">管理者を使用して実行するようにコンピューターを元に戻す必要がある場合は、**action** パラメーターを **無効** にして、PowerShell スクリプト **Enable-non-admin-mode.ps1** を実行してください。</span><span class="sxs-lookup"><span data-stu-id="2000c-165">If you need to revert the machine back to run with administrator use, then run the PowerShell script **Enable-non-admin-mode.ps1** with the **action** parameter set to **disable**.</span></span>

```powershell
.\Enable-non-admin-mode.ps1 "disable"
```

## <a name="future-versions-of-rsat"></a><span data-ttu-id="2000c-166">RSAT の今後のバージョン</span><span class="sxs-lookup"><span data-stu-id="2000c-166">Future versions of RSAT</span></span>

<span data-ttu-id="2000c-167">現在、この管理者以外のモードで RSAT を実行しているユーザーからのフィードバックを収集しています。</span><span class="sxs-lookup"><span data-stu-id="2000c-167">Currently, we are collecting feedback from users running RSAT with this non-administrator mode.</span></span> <span data-ttu-id="2000c-168">今後、インストール プロセスを変更し、管理者以外のユーザーを有効にする手順を自動的に含める可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2000c-168">In the future, we might change the installation process to automatically include the steps that enable non-administrator users.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

---
title: コマンド ラインからの配置可能パッケージのインストール
description: このトピックでは、開発環境またはビルド環境で作成されたバイナリ更新プログラムまたはアプリケーション (AOT) の展開可能パッケージのいずれかをコマンドラインを使用して適用する手順について説明します。
author: jorisdg
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 24191
ms.assetid: 42d238d6-ff03-41b6-b2d5-c94bcdc37576
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 449f21f32c3a7702f6f25aa83a44a7271f9824e5
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2020
ms.locfileid: "3497344"
---
# <a name="install-deployable-packages-from-the-command-line"></a><span data-ttu-id="db198-103">コマンド ラインからの配置可能パッケージのインストール</span><span class="sxs-lookup"><span data-stu-id="db198-103">Install deployable packages from the command line</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db198-104">このトピックでは、開発環境またはビルド環境で作成されたバイナリ更新プログラムまたはアプリケーション (AOT) の展開可能パッケージのいずれかをコマンドラインを使用して適用する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="db198-104">This topic walks you through the steps for using the command line to apply either a binary update or an application (AOT) deployable package that was created in your development or build environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db198-105">ほとんどのタイプの環境については、配置可能パッケージを Microsoft Dynamics  Lifecycle Services (LCS) から直接環境に適用できます。</span><span class="sxs-lookup"><span data-stu-id="db198-105">For most types of environments, you can apply a deployable package to an environment directly from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="db198-106">詳細については、[クラウド環境への更新プログラムの適用](apply-deployable-package-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db198-106">For more information, see [Apply updates to cloud environments](apply-deployable-package-system.md).</span></span> <span data-ttu-id="db198-107">したがって、このトピックは主に、LCS による更新の適用をサポートしていない環境タイプに適用されます。</span><span class="sxs-lookup"><span data-stu-id="db198-107">Therefore, this topic applies primarily to environment types that don't support the application of updates via LCS.</span></span> <span data-ttu-id="db198-108">例としては、Microsoft Azure のローカル開発環境 (ダウンロード可能な仮想ハード ディスク [VHD])、マルチボックス開発/テスト環境 (LCS パートナーおよび試用プロジェクト) およびビルド環境があります。</span><span class="sxs-lookup"><span data-stu-id="db198-108">Examples include local development environments (downloadable virtual hard disks [VHDs]), multi-box development/test environments in Microsoft Azure (LCS Partner and trial projects), and build environments.</span></span> <span data-ttu-id="db198-109">ただし、LCS ではなくコマンド ラインを使用して展開可能パッケージをインストールする場合は、いつでもこのトピックを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="db198-109">However, you can also use this topic any time that you want to install deployable packages by using the command line instead of LCS.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="db198-110">重要な概念</span><span class="sxs-lookup"><span data-stu-id="db198-110">Key concepts</span></span>
- <span data-ttu-id="db198-111">**配置可能パッケージ** - 配置可能パッケージとは、任意の環境に適用できる配置の単位です。</span><span class="sxs-lookup"><span data-stu-id="db198-111">**Deployable package** – A deployable package is a unit of deployment that can be applied to any environment.</span></span> <span data-ttu-id="db198-112">Application Object Server (AOS)、更新されたアプリケーション パッケージ、または新しいアプリケーション パッケージのランタイム コンポーネントに対するバイナリの修正プログラムで構成できます。</span><span class="sxs-lookup"><span data-stu-id="db198-112">It can consist of a binary hotfix to the runtime components of Application Object Server (AOS), an updated application package, or a new application package.</span></span>
- <span data-ttu-id="db198-113">**AXUpdateInstaller** - AXUpdateInstaller は実行可能プログラムで、配置可能パッケージにバンドルされています。</span><span class="sxs-lookup"><span data-stu-id="db198-113">**AXUpdateInstaller** – AXUpdateInstaller is an executable program that is bundled in the deployable package.</span></span> <span data-ttu-id="db198-114">パッケージがコンピューターにダウンロードされると、インストーラーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="db198-114">When the package is downloaded to a computer, the installer is available.</span></span>
- <span data-ttu-id="db198-115">**Runbook** – 展開ランブックは展開可能なパッケージを対象となる環境に適用させるために生成され、使われる一連の手順です。</span><span class="sxs-lookup"><span data-stu-id="db198-115">**Runbook** – The deployment runbook is a series of steps that is generated and used to apply the deployable package to the target environment.</span></span> <span data-ttu-id="db198-116">ステップの一部が自動化され、一部は手動です。</span><span class="sxs-lookup"><span data-stu-id="db198-116">Some of the steps are automated, and some are manual.</span></span> <span data-ttu-id="db198-117">AXUpdateInstaller は、これらの手順を一度に 1 つずつ正しい順序で実行できます。</span><span class="sxs-lookup"><span data-stu-id="db198-117">AXUpdateInstaller enables these steps to be run one at a time and in the correct order.</span></span>

## <a name="install-an-application-aot-deployable-package-on-a-development-environment"></a><span data-ttu-id="db198-118">開発環境でのアプリケーション (AOT) 配置可能パッケージのインストール</span><span class="sxs-lookup"><span data-stu-id="db198-118">Install an application (AOT) deployable package on a development environment</span></span>
> [!NOTE]
> <span data-ttu-id="db198-119">次の手順は、カスタマイズ パッケージに対してのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="db198-119">The steps listed below are for customization packages only.</span></span> <span data-ttu-id="db198-120">Microsoft Dynamics AX 2012 から Finance and Operations アプリへのアップグレードの一環として、データ アップグレード展開可能なパッケージを実行する場合は、**devinstall** パラメーターを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="db198-120">Do not use the **devinstall** parameter when running the Data Upgrade deployable package as part of an upgrade from Microsoft Dynamics AX 2012 to a Finance and Operations app.</span></span>

<span data-ttu-id="db198-121">AOT 配置可能パッケージはアプリケーションのカスタマイズおよび拡張機能を含むパッケージです。</span><span class="sxs-lookup"><span data-stu-id="db198-121">An AOT deployable package is a package that contains customizations and extensions to your application.</span></span> <span data-ttu-id="db198-122">開発またはデモ環境で AOT 配置可能パッケージをインストールするためだけにコマンド ラインを使用する場合、このセクションの指示に従います。</span><span class="sxs-lookup"><span data-stu-id="db198-122">If you want to use the command line just to install an AOT deployable package on a development or demo environment, follow the instructions in this section.</span></span> <span data-ttu-id="db198-123">このトピックの残りをスキップすることができます。</span><span class="sxs-lookup"><span data-stu-id="db198-123">You can then skip the rest of this topic.</span></span>

1. <span data-ttu-id="db198-124">仮想マシン (VM) で、配置可能パッケージの zip ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="db198-124">On the virtual machine (VM), download the zip file for the deployable package.</span></span> <span data-ttu-id="db198-125">非ユーザー フォルダーに zip ファイルが保存されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="db198-125">Make sure that the zip file is stored in a non-user folder.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db198-126">ZIP ファイルをダウンロードした後、右クリックし**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="db198-126">After you download the zip file, right-click it, and then select **Properties**.</span></span> <span data-ttu-id="db198-127">その後、**プロパティ** ダイアログ ボックスの **全般** タブで、**ブロック解除** を選択してファイルのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="db198-127">Then, in the **Properties** dialog box, on the **General** tab, select **Unblock** to unlock the files.</span></span>

2. <span data-ttu-id="db198-128">ファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="db198-128">Extract the files.</span></span>
3. <span data-ttu-id="db198-129">コマンド プロンプト ウィンドウを開き、配置可能パッケージを展開したフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="db198-129">Open a Command Prompt window, and go to the folder where you extracted the deployable package.</span></span>
4. <span data-ttu-id="db198-130">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="db198-130">Run the following command.</span></span>

    ```Console
    AXUpdateInstaller.exe devinstall
    ```

    <span data-ttu-id="db198-131">**devinstall** オプションは、AOT の可能なパッケージを VM にインストールします。</span><span class="sxs-lookup"><span data-stu-id="db198-131">The **devinstall** option installs the AOT deployable package on the VM.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="db198-132">このコマンドは、データベース同期を実行しません。</span><span class="sxs-lookup"><span data-stu-id="db198-132">This command doesn't run database synchronization.</span></span> <span data-ttu-id="db198-133">配置可能なパッケージをインストールした後、Microsoft Visual Studio からデータベースの同期を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db198-133">You must run database synchronization from Microsoft Visual Studio after you install the deployable package.</span></span>

## <a name="collect-topology-configuration-data"></a><span data-ttu-id="db198-134">トポロジ コンフィギュレーション データを収集する</span><span class="sxs-lookup"><span data-stu-id="db198-134">Collect topology configuration data</span></span>
1. <span data-ttu-id="db198-135">LCS で、**環境**ページの VM の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="db198-135">In LCS, on the **Environment** page, select the name of a VM.</span></span> <span data-ttu-id="db198-136">**環境**ページで提供されているユーザー名とパスワードを使用して、VM へのリモート デスクトップの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="db198-136">Establish a Remote Desktop connection to the VM by using the user name and password that are provided on the **Environment** page.</span></span>
2. <span data-ttu-id="db198-137">VM で、LCS から配置可能パッケージの zip ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="db198-137">On the VM, download the zip file for the deployable package from LCS.</span></span> <span data-ttu-id="db198-138">非ユーザー フォルダーに zip ファイルが保存されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="db198-138">Make sure that the zip file is stored in a non-user folder.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db198-139">ZIP ファイルをダウンロードした後、右クリックし**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="db198-139">After you download the zip file, right-click it, and then select **Properties**.</span></span> <span data-ttu-id="db198-140">その後、**プロパティ** ダイアログ ボックスの **全般** タブで、**ブロック解除** を選択してファイルのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="db198-140">Then, in the **Properties** dialog box, on the **General** tab, select **Unblock** to unlock the files.</span></span>
    
3. <span data-ttu-id="db198-141">ファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="db198-141">Extract the files.</span></span>
4. <span data-ttu-id="db198-142">配置可能パッケージを展開したフォルダーで、**DefaultTopologyData.xml** というファイルを検索して開きます。</span><span class="sxs-lookup"><span data-stu-id="db198-142">In the folder where you extracted the deployable package, find and open the file that is named **DefaultTopologyData.xml**.</span></span> <span data-ttu-id="db198-143">このファイルには、VM 名とインストール済みコンポーネントを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db198-143">You must specify the VM name and the installed components in this file.</span></span>

   - <span data-ttu-id="db198-144">VM 名を指定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="db198-144">To specify the VM name, follow these steps:</span></span>

       1. <span data-ttu-id="db198-145">ファイル エクスプローラーで、**この PC** を右クリックしてから、**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="db198-145">In File Explorer, right-click **This PC**, and then select **Properties**.</span></span>
       2. <span data-ttu-id="db198-146">システム プロパティで、コンピューター名を検索して記録します (たとえば、**AOS 950ed2c3e7b**)。</span><span class="sxs-lookup"><span data-stu-id="db198-146">In the system properties, find and make a note of the computer name (for example, **AOS-950ed2c3e7b**).</span></span>
       3. <span data-ttu-id="db198-147">DefaultTopologyData.xml ファイルで、前の手順で示されているコンピューター名にマシン名を変更します。</span><span class="sxs-lookup"><span data-stu-id="db198-147">In the DefaultTopologyData.xml file, replace the machine name with the computer name that you found in the previous step.</span></span>

   - <span data-ttu-id="db198-148">インストールされたコンポーネントを指定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="db198-148">To specify the installed components, follow these steps:</span></span>

       1. <span data-ttu-id="db198-149">管理者としてコマンド プロンプト ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="db198-149">Open a Command Prompt window as an administrator.</span></span>
       2. <span data-ttu-id="db198-150">展開したフォルダーに移動し、コンピューターにインストールされているすべてのコンポーネントの一覧を表示するため、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="db198-150">Go to the extracted folder, and run the following command to see a list of all the components that are installed on the computer.</span></span>

           ```Console
           AXUpdateInstaller.exe list
           ```

       3. <span data-ttu-id="db198-151">コンポーネントの一覧で DefaultTopologyData.xml ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="db198-151">Update the DefaultTopologyData.xml file with the list of components.</span></span>

     <span data-ttu-id="db198-152">VM 名とインストールされているコンポーネントの指定が完了したら、DefaultTopologyData.xml ファイルは次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="db198-152">When you've finished specifying the VM name and the installed components, the DefaultTopologyData.xml file should resemble the following illustration.</span></span>
    
     ![トポロジ構成データ](./media/defaulttopology.png)

5. <span data-ttu-id="db198-154">**環境** ページに記載されているその他のすべて VM に対して 手順 1 ～ 4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="db198-154">Repeat steps 1 through 4 for every other VM that is listed on the **Environment** page.</span></span>

## <a name="generate-a-runbook-from-the-topology"></a><span data-ttu-id="db198-155">トポロジから Runbook を生成します</span><span class="sxs-lookup"><span data-stu-id="db198-155">Generate a runbook from the topology</span></span>
<span data-ttu-id="db198-156">DefaultTopologyData.xml ファイルのトポロジの情報に基づいて、各 VM の更新手順を示す Runbook ファイルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db198-156">Based on the topology information in the DefaultTopologyData.xml file, you must generate the runbook file that will provide step-by-step instructions for updating each VM.</span></span>

- <span data-ttu-id="db198-157">すべての VM で、次のコマンドを実行して Runbook を生成します。</span><span class="sxs-lookup"><span data-stu-id="db198-157">On any VM, run the following command to generate the runbook.</span></span>

    ```Console
    AXUpdateInstaller.exe generate -runbookid=[runbookID] -topologyfile=[topologyFile] -servicemodelfile=[serviceModelFile] -runbookfile=[runbookFile]
    ```

    <span data-ttu-id="db198-158">このコマンドで使用されるパラメータの説明を次に示します。</span><span class="sxs-lookup"><span data-stu-id="db198-158">Here is an explanation of the parameters that are used in this command:</span></span>

  - <span data-ttu-id="db198-159">**\[runbookID\]**- 配置可能パッケージを適用する開発者が指定するパラメータ。</span><span class="sxs-lookup"><span data-stu-id="db198-159">**\[runbookID\]**– A parameter that is specified by the developer who applies the deployable package.</span></span>
  - <span data-ttu-id="db198-160">**\[topologyFile\]**- DefaultTopologyData.xml ファイルのパス。</span><span class="sxs-lookup"><span data-stu-id="db198-160">**\[topologyFile\]**– The path of the DefaultTopologyData.xml file.</span></span>
  - <span data-ttu-id="db198-161">**\[serviceModelFile\]**- DefaultServiceModelData.xml ファイルのパス。</span><span class="sxs-lookup"><span data-stu-id="db198-161">**\[serviceModelFile\]**– The path of the DefaultServiceModelData.xml file.</span></span>
  - <span data-ttu-id="db198-162">**\[runbookFile\]** - 生成する Runbook クファイルの名前 (たとえば、**AOSRunbook.xml**)。</span><span class="sxs-lookup"><span data-stu-id="db198-162">**\[runbookFile\]**– The name of the runbook file to generate (for example, **AOSRunbook.xml**).</span></span>

    <span data-ttu-id="db198-163">**例**</span><span class="sxs-lookup"><span data-stu-id="db198-163">**Example**</span></span>

    ```Console
    AXUpdateInstaller.exe generate -runbookid="VAL200AA2BMEDIU-runbook" -topologyfile="DefaultTopologyData.xml" -servicemodelfile="DefaultServiceModelData.xml" -runbookfile="VAL200AA2BMEDIU-runbook.xml"
    ```

<span data-ttu-id="db198-164">Runbook には、環境を更新するために実行する必要がある一連のステップが備わっています。</span><span class="sxs-lookup"><span data-stu-id="db198-164">The runbook provides the sequence of steps that must be run to update the environment.</span></span> <span data-ttu-id="db198-165">次の図は、Runbook ファイルの例を示します。</span><span class="sxs-lookup"><span data-stu-id="db198-165">The following illustration shows an example of a runbook file.</span></span> <span data-ttu-id="db198-166">Runbook の各ステップは、ID、マシン名、およびステップ実行の詳細に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="db198-166">Each step in a runbook is associated with an ID, a machine name, and step execution details.</span></span>

<span data-ttu-id="db198-167">[![Runbook ファイルの例](./media/runbook-steps-1024x624.jpg)](./media/runbook-steps.jpg)</span><span class="sxs-lookup"><span data-stu-id="db198-167">[![Example of a runbook file](./media/runbook-steps-1024x624.jpg)](./media/runbook-steps.jpg)</span></span>

## <a name="install-a-deployable-package"></a><span data-ttu-id="db198-168">配置可能パッケージのインストール</span><span class="sxs-lookup"><span data-stu-id="db198-168">Install a deployable package</span></span>
1. <span data-ttu-id="db198-169">Runbook ファイルに記載されている最初のマシン (VM) で、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="db198-169">On the first machine (VM) that is listed in the runbook file, follow these steps:</span></span>

    1. <span data-ttu-id="db198-170">次のコマンドを実行して、Runbook をインポートします。</span><span class="sxs-lookup"><span data-stu-id="db198-170">Import the runbook by running the following command.</span></span>

        ```Console
        AXUpdateInstaller.exe import -runbookfile=[runbookFile]
        ```

        <span data-ttu-id="db198-171">**例**</span><span class="sxs-lookup"><span data-stu-id="db198-171">**Example**</span></span>

        ```Console
        AXUpdateInstaller.exe import -runbookfile="VAL200AA2BMEDIU-runbook.xml"
        ```

    2. <span data-ttu-id="db198-172">Runbook を確認します。</span><span class="sxs-lookup"><span data-stu-id="db198-172">Verify the runbook.</span></span>

        ```Console
        AXUpdateInstaller.exe list
        ```

    3. <span data-ttu-id="db198-173">runbook を実行します。</span><span class="sxs-lookup"><span data-stu-id="db198-173">Run the runbook.</span></span>

        ```Console
        AXUpdateInstaller.exe execute -runbookid=[runbookID]
        ```

        <span data-ttu-id="db198-174">**例**</span><span class="sxs-lookup"><span data-stu-id="db198-174">**Example**</span></span>

        ```Console
        AXUpdateInstaller.exe execute -runbookid="VAL200AA2BMEDIU-runbook"
        ```

        <span data-ttu-id="db198-175">AXUpdateInstaller は、各ステップが VM で実行された後に Runbook ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="db198-175">AXUpdateInstaller updates the runbook file after each step is run on a VM.</span></span> <span data-ttu-id="db198-176">Runbook には、各ステップに関する情報も記録されます。</span><span class="sxs-lookup"><span data-stu-id="db198-176">The runbook also logs information about each step.</span></span>

        <span data-ttu-id="db198-177">手動ステップについては、指示に従い、Runbook でステップを完了済とマークする以下のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="db198-177">For manual steps, follow the instructions, and then run the following command to mark the step as completed in the runbook.</span></span>

        ```Console
        AXUpdateInstaller.exe execute -runbookID=[runbookID] -setstepcomplete=[stepID]
        ```

        <span data-ttu-id="db198-178">**例**</span><span class="sxs-lookup"><span data-stu-id="db198-178">**Example**</span></span>

        ```Console
        AXUpdateInstaller.exe execute -runbookid="VAL200AA2BMEDIU-runbook" -setstepcomplete=2
        ```

        <span data-ttu-id="db198-179">どの段階中でもエラーが発生した場合は、そのステップのスクリプトまたは指示をデバッグし、それに応じて更新します。</span><span class="sxs-lookup"><span data-stu-id="db198-179">If errors occur during any step, debug the script or the instructions in the step, and update accordingly.</span></span>

    4. <span data-ttu-id="db198-180">Runbook をエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="db198-180">Export the runbook.</span></span>

        ```Console
        AXUpdateInstaller.exe export -runbookid=[runbookID] -runbookfile=[runbookFile]
        ```

        <span data-ttu-id="db198-181">**例**</span><span class="sxs-lookup"><span data-stu-id="db198-181">**Example**</span></span>

        ```Console
        AXUpdateInstaller.exe export -runbookid="VAL200AA2BMEDIU-runbook" -runbookfile="VAL200AA2BMEDIU-runbook.xml"
        ```

2. <span data-ttu-id="db198-182">Runbook ファイルに記載されているその他のすべての VM で手順 1 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="db198-182">Repeat step 1 on every other VM that is listed in the runbook file.</span></span> <span data-ttu-id="db198-183">1 ボックス環境では、開発、構築、およびデモ環境など、1 つの VM のみがあります。</span><span class="sxs-lookup"><span data-stu-id="db198-183">For one-box environments, such as development, build, and demo environments, there is only one VM.</span></span>

## <a name="verify-installation"></a><span data-ttu-id="db198-184">インストールの確認</span><span class="sxs-lookup"><span data-stu-id="db198-184">Verify installation</span></span>
1. <span data-ttu-id="db198-185">新しい更新プログラムがインストールされていることを確認するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="db198-185">Run the following command to verify that the new updates are installed.</span></span>

    ```Console
    AXUpdateInstaller.exe list
    ```

2. <span data-ttu-id="db198-186">Runbook を表示して、完了したステップを確認します。</span><span class="sxs-lookup"><span data-stu-id="db198-186">View the runbook to see the completed steps.</span></span> <span data-ttu-id="db198-187">手順が完了した runbook ファイルの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="db198-187">Here is an example of a runbook file where the steps have been completed.</span></span>

    <span data-ttu-id="db198-188">[![runbook の完了したステップの例](./media/image013-1024x978.png)](./media/image013.png)</span><span class="sxs-lookup"><span data-stu-id="db198-188">[![Example of completed steps in a runbook](./media/image013-1024x978.png)](./media/image013.png)</span></span>

## <a name="backup-the-runbook-file"></a><span data-ttu-id="db198-189">Runbook ファイルをバックアップします</span><span class="sxs-lookup"><span data-stu-id="db198-189">Backup the runbook file</span></span>
- <span data-ttu-id="db198-190">Runbook のすべての手順を完了した後、Runbook をエクスポートし、後で参照できるようにファイルをコンピューターの外部に保存します。</span><span class="sxs-lookup"><span data-stu-id="db198-190">After all the steps in the runbook are completed and you've exported the runbook, save the file outside the computer for future reference.</span></span> <span data-ttu-id="db198-191">たとえば、このような状況で Runbook ファイルを使用する必要が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="db198-191">For example, you might have to use the runbook file in these situations:</span></span>

    - <span data-ttu-id="db198-192">生産などのダウンタイム要件を分析する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db198-192">You must analyze the downtime requirements for production, and so on.</span></span>
    - <span data-ttu-id="db198-193">配置可能パッケージをインストールすることはできないため、マイクロソフトにファイルを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db198-193">You must send the file to Microsoft because a deployable package can't be installed.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="db198-194">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="db198-194">Troubleshooting</span></span>
- <span data-ttu-id="db198-195">runbook の段階で失敗した場合は、次のコマンドを実行して再実行できます。</span><span class="sxs-lookup"><span data-stu-id="db198-195">If any step in the runbook fails, you can rerun it by running the following command.</span></span>

    ```Console
    AXUpdateInstaller.exe execute -runbookid=[runbookID] -rerunstep=[stepID]
    ```

- <span data-ttu-id="db198-196">バージョンの不一致やダウングレード、または同じ展開可能パッケージのインストールを防止するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="db198-196">To prevent version mismatch or downgrade, or installation of the same deployable package, run the following command.</span></span>

    ```Console
    AXUpdateInstaller.exe execute -runbookid=[runbook ID] -versioncheck=true
    ```

- <span data-ttu-id="db198-197">データベースの同期を確認するには **aosservice\\scripts\\** フォルダー内の **dbsync.error.txt** ファイルを見つけて開き、エラーを探します。</span><span class="sxs-lookup"><span data-stu-id="db198-197">To verify database synchronization, in the **aosservice\\scripts\\** folder, find and open the **dbsync.error.txt** file, and look for any errors.</span></span>

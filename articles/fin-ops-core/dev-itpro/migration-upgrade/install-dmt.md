---
title: AX 2009 の移行 － データ移行ツールのインストール
description: このトピックでは、Microsoft Dynamics AX 2009 からデータを移行できるように、データ移行ツール (DMT) を設定する方法について説明します。
author: kfend
ms.date: 09/13/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: 4e3786e87c21179306c8f94ecc96d94f2d1471f3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745637"
---
# <a name="ax-2009-migration--install-the-data-migration-tool"></a><span data-ttu-id="a919b-103">AX 2009 の移行 – データ移行ツールのインストール</span><span class="sxs-lookup"><span data-stu-id="a919b-103">AX 2009 migration – Install the Data migration tool</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a919b-104">このトピックでは、Microsoft Dynamics AX 2009 から Finance and Operations にデータを移行できるように、データ移行ツール (DMT) を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a919b-104">This topic explains how to set up the Data migration tool (DMT) so that you can migrate data from Microsoft Dynamics AX 2009 to Finance and Operations.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="a919b-105">現時点で、DMT はプライベート プレビューです。</span><span class="sxs-lookup"><span data-stu-id="a919b-105">At this time, the DMT is in private preview.</span></span> <span data-ttu-id="a919b-106">関心をお持ちの場合、[プレビュー プログラム](https://microsoft.qualtrics.com/jfe/form/SV_brOLCioQ7mmeykB)にサインアップすることができます。</span><span class="sxs-lookup"><span data-stu-id="a919b-106">If you are interested you can sign up for the [Preview Program](https://microsoft.qualtrics.com/jfe/form/SV_brOLCioQ7mmeykB).</span></span> <span data-ttu-id="a919b-107">DMT の公開リリース日は設定されていません。</span><span class="sxs-lookup"><span data-stu-id="a919b-107">The public release date for the DMT has not been set.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="a919b-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="a919b-108">Prerequisites</span></span>

- <span data-ttu-id="a919b-109">Microsoft SQL Server 2008/2012/2014/2016。</span><span class="sxs-lookup"><span data-stu-id="a919b-109">Microsoft SQL Server 2008/2012/2014/2016.</span></span>
- <span data-ttu-id="a919b-110">Microsoft .NET Framework バージョン 4.5 またはそれ以降。</span><span class="sxs-lookup"><span data-stu-id="a919b-110">The Microsoft .NET Framework version 4.5 or later.</span></span>
- <span data-ttu-id="a919b-111">Microsoft SQL 2012 Native Client がインストールされている Microsoft SQL Server コンピューター。</span><span class="sxs-lookup"><span data-stu-id="a919b-111">Microsoft SQL Server machine that has Microsoft SQL 2012 Native Client installed.</span></span>
- <span data-ttu-id="a919b-112">Microsoft SQL Server Integration Services (SSIS) サービスがインストールされ、DMT サービスがインストールされるコンピューターで実行されています。</span><span class="sxs-lookup"><span data-stu-id="a919b-112">The Microsoft SQL Server Integration Services (SSIS) service is installed and running on the machine where the DMT service will be installed.</span></span>
- <span data-ttu-id="a919b-113">SQL Server 認証は、SQL 認証と Microsoft Windows 認証の両方をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a919b-113">SQL Server authentication must support both SQL authentication and Microsoft Windows authentication.</span></span>
- <span data-ttu-id="a919b-114">次の表のバージョン ガイダンスに従っている Microsoft Access データベース エンジン。</span><span class="sxs-lookup"><span data-stu-id="a919b-114">Microsoft Access database engines that follows the version guidance in the following table.</span></span>

    |                                   | <span data-ttu-id="a919b-115">SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="a919b-115">SQL Server 2008</span></span>                 | <span data-ttu-id="a919b-116">SQL Server 2012 以降</span><span class="sxs-lookup"><span data-stu-id="a919b-116">SQL Server 2012 and later</span></span> |
    |-----------------------------------|---------------------------------|---------------------------|
    | <span data-ttu-id="a919b-117">**VM に Microsoft Office がない**</span><span class="sxs-lookup"><span data-stu-id="a919b-117">**No Microsoft Office on the VM**</span></span> | <span data-ttu-id="a919b-118">Access エンジン 32 ビット</span><span class="sxs-lookup"><span data-stu-id="a919b-118">Access engine 32-bit</span></span>            | <span data-ttu-id="a919b-119">Access エンジン 64 ビット</span><span class="sxs-lookup"><span data-stu-id="a919b-119">Access engine 64-bit</span></span>      |
    | <span data-ttu-id="a919b-120">**Microsoft Office 32 ビット**</span><span class="sxs-lookup"><span data-stu-id="a919b-120">**Microsoft Office 32-bit**</span></span>       | <span data-ttu-id="a919b-121">Access エンジン 32 ビット</span><span class="sxs-lookup"><span data-stu-id="a919b-121">Access engine 32-bit</span></span>            | <span data-ttu-id="a919b-122">Access エンジン 64 ビット</span><span class="sxs-lookup"><span data-stu-id="a919b-122">Access engine 64-bit</span></span>      |
    | <span data-ttu-id="a919b-123">**Microsoft Office 64 ビット**</span><span class="sxs-lookup"><span data-stu-id="a919b-123">**Microsoft Office 64-bit**</span></span>       | <span data-ttu-id="a919b-124">Access エンジン 32 ビットおよび 64 ビット</span><span class="sxs-lookup"><span data-stu-id="a919b-124">Access engine 32-bit and 64-bit</span></span> | <span data-ttu-id="a919b-125">Access エンジン 64 ビット</span><span class="sxs-lookup"><span data-stu-id="a919b-125">Access engine 64-bit</span></span>      |

- <span data-ttu-id="a919b-126">Microsoft Dynamics AX 2009 SP1 5.0.1000.52 以降。</span><span class="sxs-lookup"><span data-stu-id="a919b-126">Microsoft Dynamics AX 2009 SP1 5.0.1000.52 or later.</span></span>
- <span data-ttu-id="a919b-127">前提条件となる修正プログラム (axpatch.exe) がインストールされている。</span><span class="sxs-lookup"><span data-stu-id="a919b-127">The prerequisite patch (axpatch.exe) installed.</span></span> <span data-ttu-id="a919b-128">修正プログラムを見つけるには、ZIP ファイルをダウンロードして抽出した場所から、<pre-requisiteforpatch\>\<application\> に移動します。</span><span class="sxs-lookup"><span data-stu-id="a919b-128">To find the patch, from the location where you downloaded and extracted the zip file, go to <pre-requisiteforpatch\>\<application\>.</span></span>

## <a name="install-dixf-service"></a><span data-ttu-id="a919b-129">DIXF サービスのインストール</span><span class="sxs-lookup"><span data-stu-id="a919b-129">Install DIXF service</span></span>

1. <span data-ttu-id="a919b-130">ZIP ファイルを展開した場所に移動し、**DIXF msi** フォルダーで **DIXF\_Service\_x64.msi** を右クリックし、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-130">Go to the location where you extracted the zip file, and then, in the **DIXF msi** folder, right-click **DIXF\_Service\_x64.msi**, and select **Run**.</span></span>
2. <span data-ttu-id="a919b-131">ウィザードが開始したら、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-131">When the wizard starts, select **Next**.</span></span>
3. <span data-ttu-id="a919b-132">ライセンス条項を受け入れ、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-132">Accept the license terms, and then select **Next**.</span></span>
4. <span data-ttu-id="a919b-133">サービスのアカウントを選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-133">Select an account for the service, and then select **Next**.</span></span> <span data-ttu-id="a919b-134">アカウントは、管理者権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a919b-134">The account should have admin rights.</span></span> <span data-ttu-id="a919b-135">**ネットワーク サービス** チェック ボックスをオンにした場合、ネットワーク サービス アカウントに管理者権限があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a919b-135">If you select the **Network Service** check box, verify that the network service account has admin rights.</span></span> <span data-ttu-id="a919b-136">それ以外の場合、チェック ボックスをオフにし、管理者アカウントのユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="a919b-136">Otherwise, clear the check box, and enter an admin account user name and password.</span></span> <span data-ttu-id="a919b-137">その後、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-137">Then select **Next**.</span></span>
5. <span data-ttu-id="a919b-138">SQL Server のバージョンを選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-138">Select the SQL Server version, and then select **Next**.</span></span>
6. <span data-ttu-id="a919b-139">**インストール** を選択し、ウィザードが完了したら **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-139">Select **Install**, and then, when the wizard is completed, select **Finish**.</span></span>

## <a name="copy-binaries"></a><span data-ttu-id="a919b-140">バイナリのコピー</span><span class="sxs-lookup"><span data-stu-id="a919b-140">Copy binaries</span></span>
<span data-ttu-id="a919b-141">ZIP ファイルを展開した場所に移動し、以下のファイルを **Program Files (x86)\\Microsoft Dynamics AX\\50\\Client\\Bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a919b-141">Go to the location where you extracted the zip file, and copy the following files to the **Program Files (x86)\\Microsoft Dynamics AX\\50\\Client\\Bin** folder:</span></span>

- <span data-ttu-id="a919b-142">Microsoft.Dynamics.AX.Framework.Tools.DMT.dll</span><span class="sxs-lookup"><span data-stu-id="a919b-142">Microsoft.Dynamics.AX.Framework.Tools.DMT.dll</span></span>
- <span data-ttu-id="a919b-143">Interop.Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="a919b-143">Interop.Shell32.dll</span></span>

## <a name="install-dmt-components-for-ax-2009"></a><span data-ttu-id="a919b-144">AX 2009 の DMT コンポーネントのインストール</span><span class="sxs-lookup"><span data-stu-id="a919b-144">Install DMT components for AX 2009</span></span>
<span data-ttu-id="a919b-145">DMT をインストールする方法は 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="a919b-145">There are two ways to install the DMT.</span></span> <span data-ttu-id="a919b-146">結合された XPO ファイルまたはアプリケーション修正プログラムを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a919b-146">You can use the combined XPO file or an application hotfix.</span></span> <span data-ttu-id="a919b-147">Microsoft Dynamics Lifecycle Services (LCS) 実装プロジェクトを使用している場合、アプリケーション修正プログラムを使用します。</span><span class="sxs-lookup"><span data-stu-id="a919b-147">If you're using a Microsoft Dynamics Lifecycle Services (LCS) Implementation project, use the application hotfix.</span></span> <span data-ttu-id="a919b-148">インストールには、約 7 時間かかります。</span><span class="sxs-lookup"><span data-stu-id="a919b-148">Installation takes approximately seven hours.</span></span>

### <a name="combined-xpo-file"></a><span data-ttu-id="a919b-149">結合された XPO ファイル</span><span class="sxs-lookup"><span data-stu-id="a919b-149">Combined XPO file</span></span>
1. <span data-ttu-id="a919b-150">結合された XPO ファイルを **DMT_V1.0\CombinedXPO** から展開します。</span><span class="sxs-lookup"><span data-stu-id="a919b-150">Extract the combined XPO file from **DMT_V1.0\CombinedXPO**.</span></span>
2. <span data-ttu-id="a919b-151">AX 2009 に結合された XPO ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="a919b-151">Import the combined XPO file into AX 2009.</span></span>
3. <span data-ttu-id="a919b-152">**DMT_V1.0\Label file** ファイルから  **Program Files\\Microsoft Dynamics AX\\50\\Application\\Appl\\<NameOfYourDeployment\>** フォルダーにラベル ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a919b-152">Copy the label file from **DMT_V1.0\Label file** to the **Program Files\\Microsoft Dynamics AX\\50\\Application\\Appl\\<NameOfYourDeployment\>** folder.</span></span>
4. <span data-ttu-id="a919b-153">Application Object Server (AOS) インスタンスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="a919b-153">Restart the Application Object Server (AOS) instance.</span></span>
5. <span data-ttu-id="a919b-154">AX 2009 で、**データ移行** \> **設定** \> **DMT アプリケーションのコンパイルと同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-154">In AX 2009, select **Data migration** \> **Setup** \> **Compile and synchronize DMT application**.</span></span>

<span data-ttu-id="a919b-155">ユーザーがログインしているレイヤーに結合された XPO ファイルがインポートされることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a919b-155">Note that the combined XPO file is imported into the layer that the user is signed in to.</span></span>

### <a name="application-hotfix"></a><span data-ttu-id="a919b-156">アプリケーションの修正プログラム</span><span class="sxs-lookup"><span data-stu-id="a919b-156">Application hotfix</span></span>
1. <span data-ttu-id="a919b-157">**DMT_V1.0\\ApplicationHotfix\\DynamicsAX2009-KB4010403-SP1** に移動し、**setup.exe** を右クリックして **実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-157">Go to **DMT_V1.0\\ApplicationHotfix\\DynamicsAX2009-KB4010403-SP1**, right-click **setup.exe**, and then select **Run**.</span></span>
2. <span data-ttu-id="a919b-158">AX 2009 のアプリケーション オブジェクト ツリー (AOT) で、**LegalEntityId** フィールドが **DMTCustomerAddressView** ビューと **DMTVendorAddressView** ビューに追加されていることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="a919b-158">In AX 2009, in the Application Object Tree (AOT), notice that the **LegalEntityId** field has been added to the **DMTCustomerAddressView** and **DMTVendorAddressView** views.</span></span>
3. <span data-ttu-id="a919b-159">**データ移行** \> **設定** \> **DMT アプリケーションのコンパイルと同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-159">Select **Data migration** \> **Setup** \> **Compile and synchronize DMT application**.</span></span>

## <a name="parameter-setup"></a><span data-ttu-id="a919b-160">パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="a919b-160">Parameter setup</span></span>
<span data-ttu-id="a919b-161">ZIP ファイルを展開した場所に移動し、**defaultvalue.xlsx** を検索します。</span><span class="sxs-lookup"><span data-stu-id="a919b-161">Go to the location to where you extracted the zip file, and find **defaultvalue.xlsx**.</span></span>

> [!NOTE]
> <span data-ttu-id="a919b-162">ファイルは .xlsx 形式に保存されます。</span><span class="sxs-lookup"><span data-stu-id="a919b-162">The file is saved in .xlsx format.</span></span> <span data-ttu-id="a919b-163">拡張機能を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="a919b-163">Don't change the extension.</span></span> <span data-ttu-id="a919b-164">このファイルを **既定のコンフィギュレーション** パラメーターの入力として入力したら、**すべてのファイル** を選択して .xlsx 形式を選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a919b-164">When you provide this file as input for the **Default configuration** parameter, select **All Files** so that you can select the .xlsx format.</span></span> <span data-ttu-id="a919b-165">この形式を選択しない場合、マッピングの生成を開始するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a919b-165">If you don't select this format, errors will occur when you start to generate mappings.</span></span>

1. <span data-ttu-id="a919b-166">AX 2009 で、**データ移行** \> **設定** \> **既定のマップを構成する** を選択し、次のフィールドに適切な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="a919b-166">In AX 2009, select **Data migration** \> **Setup** \> **Configure default maps**, and enter the appropriate information in the following fields:</span></span>

    - <span data-ttu-id="a919b-167">**既定のコンフィギュレーション**: Microsoft Excel ファイルのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a919b-167">**Default configuration** – Enter the path of the Microsoft Excel file.</span></span>
    - <span data-ttu-id="a919b-168">**エクスポート ファイルのパス**: サービスがアクセスできるサーバーのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a919b-168">**Export file path** – Enter the server path that can be accessed by the service.</span></span>
    - <span data-ttu-id="a919b-169">**SQL Server のユーザー名とパスワード**: AX 2009 データベースの SQL 認証資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="a919b-169">**SQL Server user and password** – Enter the SQL authentication credentials for the AX 2009 database.</span></span>

2. <span data-ttu-id="a919b-170">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a919b-170">Close the form.</span></span>
3. <span data-ttu-id="a919b-171">**設定** で、**接続の構成** を選択し、次のフィールドに適切な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="a919b-171">Under **Setup**, select **Configure connections**, and enter the appropriate information on the following fields:</span></span>

    - <span data-ttu-id="a919b-172">**DIXF サービス ホスト**: DIXF サービスのインストールのホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="a919b-172">**DIXF service host** – Enter the host name of the DIXF service installation.</span></span>
    - <span data-ttu-id="a919b-173">**テナント URL** – アプリケーション テナントの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="a919b-173">**Tenant URL** – Enter the URL for the application tenant.</span></span> <span data-ttu-id="a919b-174">テナントが不明な場合は、Finance and Operations アプリケーションの web.config ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a919b-174">If you aren't sure of the tenant, see the web.config file for the Finance and Operations application.</span></span>

    > <span data-ttu-id="a919b-175">[!注意} Azure ポータルでは、Azure Active Directory (AAD) で新しいアプリケーションを作成するときは、2 つのオプションから選択できます。</span><span class="sxs-lookup"><span data-stu-id="a919b-175">[!NOTE} In the Azure Portal, when you create a new app in the Azure Active Directory (AAD), you can select from two options.</span></span> <span data-ttu-id="a919b-176">**Web API** と **ネイティブ**。</span><span class="sxs-lookup"><span data-stu-id="a919b-176">**Web API** and **Native**.</span></span> <span data-ttu-id="a919b-177">このインスタンスでは、**ネイティブ** を選択し、ネイティブ AAD アプリケーションへのアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="a919b-177">In this instance, select **Native** and grant permissions to native AAD app.</span></span>

## <a name="multi-box-setup"></a><span data-ttu-id="a919b-178">マルチボックスの設定</span><span class="sxs-lookup"><span data-stu-id="a919b-178">Multi-box setup</span></span>
<span data-ttu-id="a919b-179">マルチボックスの設定の場合、次のコンピューターが必要です。</span><span class="sxs-lookup"><span data-stu-id="a919b-179">For a multi-box setup, you must have the following machines:</span></span>

- <span data-ttu-id="a919b-180">AX 2009 データベースおよび DIXF サービスがインストールされているコンピューター A</span><span class="sxs-lookup"><span data-stu-id="a919b-180">Machine A, where the AX 2009 database and DIXF service are installed</span></span>
- <span data-ttu-id="a919b-181">AX 2009 AOS インスタンスがインストールされているコンピューター B</span><span class="sxs-lookup"><span data-stu-id="a919b-181">Machine B, where the AX 2009 AOS instance is installed</span></span>
- <span data-ttu-id="a919b-182">AX 2009 クライアントがインストールされているコンピューター C</span><span class="sxs-lookup"><span data-stu-id="a919b-182">Machine C, where the AX 2009 client is installed</span></span>

<span data-ttu-id="a919b-183">この 3 コンピューター設定では、コンピューター C はコンピューター B の AOS インスタンスに接続するように構成されています。コンピューター B は、コンピューター A で構成されているデータベースに接続されます。</span><span class="sxs-lookup"><span data-stu-id="a919b-183">In this three-machine setup, machine C is configured to connect to the AOS instance on machine B. Machine B is connected to the database that is configured on machine A.</span></span>

### <a name="dixf-service-machine-prerequisites-machine-a"></a><span data-ttu-id="a919b-184">DIXF サービス コンピューターの前提条件 (コンピューター A)</span><span class="sxs-lookup"><span data-stu-id="a919b-184">DIXF service machine prerequisites (machine A)</span></span>
<span data-ttu-id="a919b-185">コンピューター A の DIXF サービスには、次の前提条件があります。</span><span class="sxs-lookup"><span data-stu-id="a919b-185">The DIXF service on machine A has the following prerequisites:</span></span>

- <span data-ttu-id="a919b-186">SQL Server 2008/2012/2014</span><span class="sxs-lookup"><span data-stu-id="a919b-186">SQL Server 2008/2012/2014</span></span>
- <span data-ttu-id="a919b-187">.NET Framework バージョン 4.5</span><span class="sxs-lookup"><span data-stu-id="a919b-187">The .NET Framework version 4.5</span></span>
- <span data-ttu-id="a919b-188">Access データベース エンジン</span><span class="sxs-lookup"><span data-stu-id="a919b-188">Access database engines</span></span>

    - <span data-ttu-id="a919b-189">**SQL Server 2008 の場合:** Access エンジン 32 ビットおよび 64 ビット (Microsoft Excel が 64 ビットの場合)</span><span class="sxs-lookup"><span data-stu-id="a919b-189">**For SQL Server 2008:** Access engine 32-bit and 64-bit (if Microsoft Excel is 64-bit)</span></span>
    - <span data-ttu-id="a919b-190">**SQL Server 2012 以降の場合:** Access エンジン 64 ビット</span><span class="sxs-lookup"><span data-stu-id="a919b-190">**For SQL Server 2012 or later:** Access engine 64-bit</span></span>

- <span data-ttu-id="a919b-191">AX 2009 データベース (SQL Server で構成)</span><span class="sxs-lookup"><span data-stu-id="a919b-191">AX 2009 database (configured on SQL Server)</span></span>

### <a name="aos-machine-prerequisites-machine-b"></a><span data-ttu-id="a919b-192">AOS コンピューターの前提条件 (コンピューター B)</span><span class="sxs-lookup"><span data-stu-id="a919b-192">AOS machine prerequisites (machine B)</span></span>
<span data-ttu-id="a919b-193">コンピューター B の AOS のインストールには、次の前提条件があります。</span><span class="sxs-lookup"><span data-stu-id="a919b-193">The AOS installation on machine B has the following prerequisites:</span></span>

- <span data-ttu-id="a919b-194">AX 2009 AOS サーバー</span><span class="sxs-lookup"><span data-stu-id="a919b-194">AX 2009 AOS Server</span></span>
- <span data-ttu-id="a919b-195">アプリケーション ファイル</span><span class="sxs-lookup"><span data-stu-id="a919b-195">Application files</span></span>

### <a name="client-machine-prerequisites-machine-c"></a><span data-ttu-id="a919b-196">クライアント コンピューターの前提条件 (コンピューター C)</span><span class="sxs-lookup"><span data-stu-id="a919b-196">Client machine prerequisites (machine C)</span></span>
<span data-ttu-id="a919b-197">コンピューター C のクライアントのインストールには、次の前提条件があります。</span><span class="sxs-lookup"><span data-stu-id="a919b-197">The client installation on machine C has the following prerequisites:</span></span>

- <span data-ttu-id="a919b-198">AX 2009 クライアント</span><span class="sxs-lookup"><span data-stu-id="a919b-198">AX 2009 client</span></span>

### <a name="shared-folder-permissions"></a><span data-ttu-id="a919b-199">共有フォルダーのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="a919b-199">Shared folder permissions</span></span>

<span data-ttu-id="a919b-200">既定のコンフィギュレーション ファイルとエクスポート パッケージ ファイルのパスは共有する必要があり、クライアント ユーザーおよび DIXF サービスにはこれらのファイルへの読み取り/書き込みアクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="a919b-200">The path of the default configuration file and the export package file should be shared, and client users and the DIXF service should have read/write access to these files.</span></span> <span data-ttu-id="a919b-201">アクセス権を付与するには、**データ移行** \> **設定** \> **マップの構成と生成** を選択し、**パスの検証** を選択して必要なアクセス権があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a919b-201">To grant this access, select **Data migration** \> **Setup** \> **Configure and generate maps**, and then select **Validate path** to verify that the required access is available.</span></span>

### <a name="set-up-parameters"></a><span data-ttu-id="a919b-202">パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="a919b-202">Set up parameters</span></span>

1. <span data-ttu-id="a919b-203">**データ移行** \> **設定** \> **接続の構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-203">Select **Data migration** \> **Setup** \> **Configure connections**.</span></span>
2. <span data-ttu-id="a919b-204">**DIXF サービス ホスト** フィールドに、DIXF サービスがインストールされているリモート コンピューターの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a919b-204">In the **DIXF service host** field, enter the name of the remote machine where the DIXF service is installed.</span></span> <span data-ttu-id="a919b-205">既定では、名前は **localhost** です。</span><span class="sxs-lookup"><span data-stu-id="a919b-205">By default, the name is **localhost**.</span></span>
3. <span data-ttu-id="a919b-206">**検証** を選択し、クライアントが DIXF サービスにアクセスできることを検証します。</span><span class="sxs-lookup"><span data-stu-id="a919b-206">Select **Validate** to validate that the client can access the DIXF service.</span></span>

### <a name="workarounds"></a><span data-ttu-id="a919b-207">回避策</span><span class="sxs-lookup"><span data-stu-id="a919b-207">Workarounds</span></span>
<span data-ttu-id="a919b-208">"DIXF サービスを利用できません" というエラー メッセージが表示される場合、次の回避方法を実行してポート 7000 のサービスの接続を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a919b-208">If you receive an error message that states, "DIXF service is unavailable," complete the following workaround to enable a service connection for port 7000.</span></span>

1. <span data-ttu-id="a919b-209">ポート 7000 を開いた後、DMT サービス コンピューターの受信ルールで **ファイアウォール設定** を選択して **実行** \> **wf.msc** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-209">Open port 7000, and then, for inbound rules on the DMT service machine, select **Firewall settings**, and then select **Run** \> **wf.msc**.</span></span>
2. <span data-ttu-id="a919b-210">**受信ルール** \> **新しいルール** を選択した後、**ルール タイプ** タブで、**ポート** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-210">Select **Inbound Rules** \> **New rule**, and then, on the **Rule Type** tab, select **Port**, and then select **Next**.</span></span>
3. <span data-ttu-id="a919b-211">**特定のローカル ポート** フィールドに、**7000** と入力し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-211">In the **Specific local ports** field, enter **7000**, and then select **Next**.</span></span>
4. <span data-ttu-id="a919b-212">**接続を許可する** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-212">Select **Allow the connection**, and then select **Next**.</span></span>
5. <span data-ttu-id="a919b-213">3 つのチェック ボックスをすべてオンにしてすべてのルールを適用し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-213">Select all three check boxes to apply all the rules, and then select **Next**.</span></span>
6. <span data-ttu-id="a919b-214">ルールの名前を入力し、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a919b-214">Enter the name of the rule, and then select **Finish**.</span></span>
7. <span data-ttu-id="a919b-215">送信ルールでこれらの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="a919b-215">Repeat these steps for outbound rules.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: "AX 2009 の移行 － データ移行ツールのインストール"
description: "このトピックでは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations にデータを移行できるように、データ移行ツール (DMT) を設定する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 09/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: df8739623b49cb35c8d8ce56c1e7fa26a29635a8
ms.contentlocale: ja-jp
ms.lasthandoff: 09/20/2018

---

# <a name="ax-2009-migration--install-the-data-migration-tool"></a><span data-ttu-id="8c0f1-103">AX 2009 の移行 - データ移行ツールのインストール</span><span class="sxs-lookup"><span data-stu-id="8c0f1-103">AX 2009 migration – Install the Data migration tool</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c0f1-104">このトピックでは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations にデータを移行できるように、データ移行ツール (DMT) を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-104">This topic explains how to set up the Data migration tool (DMT) so that you can migrate data from Microsoft Dynamics AX 2009 to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8c0f1-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="8c0f1-105">Prerequisites</span></span>

- <span data-ttu-id="8c0f1-106">Microsoft SQL Server 2008/2012/2014/2016。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-106">Microsoft SQL Server 2008/2012/2014/2016.</span></span>
- <span data-ttu-id="8c0f1-107">Microsoft .NET Framework バージョン 4.5 またはそれ以降。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-107">The Microsoft .NET Framework version 4.5 or later.</span></span>
- <span data-ttu-id="8c0f1-108">Microsoft SQL 2012 Native Client がインストールされている Microsoft SQL Server コンピューター。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-108">Microsoft SQL Server machine that has Microsoft SQL 2012 Native Client installed.</span></span>
- <span data-ttu-id="8c0f1-109">Microsoft SQL Server Integration Services (SSIS) サービスがインストールされ、DMT サービスがインストールされるコンピューターで実行されます。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-109">The Microsoft SQL Server Integration Services (SSIS) service is installed and running on the machine where the DMT service will be installed.</span></span>
- <span data-ttu-id="8c0f1-110">SQL Server 認証は、SQL 認証と Microsoft Windows 認証の両方をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-110">SQL Server authentication must support both SQL authentication and Microsoft Windows authentication.</span></span>
- <span data-ttu-id="8c0f1-111">次の表のバージョン ガイダンスに従っている Microsoft Access データベース エンジン。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-111">Microsoft Access database engines that follows the version guidance in the following table.</span></span>

    |                                   | <span data-ttu-id="8c0f1-112">SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c0f1-112">SQL Server 2008</span></span>                 | <span data-ttu-id="8c0f1-113">SQL Server 2012 以降</span><span class="sxs-lookup"><span data-stu-id="8c0f1-113">SQL Server 2012 and later</span></span> |
    |-----------------------------------|---------------------------------|---------------------------|
    | <span data-ttu-id="8c0f1-114">**VM に Microsoft Office がない**</span><span class="sxs-lookup"><span data-stu-id="8c0f1-114">**No Microsoft Office on the VM**</span></span> | <span data-ttu-id="8c0f1-115">Access エンジン 32 ビット</span><span class="sxs-lookup"><span data-stu-id="8c0f1-115">Access engine 32-bit</span></span>            | <span data-ttu-id="8c0f1-116">Access エンジン 64 ビット</span><span class="sxs-lookup"><span data-stu-id="8c0f1-116">Access engine 64-bit</span></span>      |
    | <span data-ttu-id="8c0f1-117">**Microsoft Office 32 ビット**</span><span class="sxs-lookup"><span data-stu-id="8c0f1-117">**Microsoft Office 32-bit**</span></span>       | <span data-ttu-id="8c0f1-118">Access エンジン 32 ビット</span><span class="sxs-lookup"><span data-stu-id="8c0f1-118">Access engine 32-bit</span></span>            | <span data-ttu-id="8c0f1-119">Access エンジン 64 ビット</span><span class="sxs-lookup"><span data-stu-id="8c0f1-119">Access engine 64-bit</span></span>      |
    | <span data-ttu-id="8c0f1-120">**Microsoft Office 64 ビット**</span><span class="sxs-lookup"><span data-stu-id="8c0f1-120">**Microsoft Office 64-bit**</span></span>       | <span data-ttu-id="8c0f1-121">Access エンジン 32 ビットおよび 64 ビット</span><span class="sxs-lookup"><span data-stu-id="8c0f1-121">Access engine 32-bit and 64-bit</span></span> | <span data-ttu-id="8c0f1-122">Access エンジン 64 ビット</span><span class="sxs-lookup"><span data-stu-id="8c0f1-122">Access engine 64-bit</span></span>      |

- <span data-ttu-id="8c0f1-123">Microsoft Dynamics AX 2009 SP1 5.0.1000.52 以降。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-123">Microsoft Dynamics AX 2009 SP1 5.0.1000.52 or later.</span></span>
- <span data-ttu-id="8c0f1-124">前提条件となる修正プログラム (axpatch.exe) がインストールされている。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-124">The prerequisite patch (axpatch.exe) installed.</span></span> <span data-ttu-id="8c0f1-125">修正プログラムを見つけるには、ZIP ファイルをダウンロードして展開した場所から、<pre-requisiteforpatch\>\<application\> に移動します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-125">To find the patch, from the location where you downloaded and extracted the zip file, go to <pre-requisiteforpatch\>\<application\>.</span></span>

## <a name="install-dixf-service"></a><span data-ttu-id="8c0f1-126">DIXF サービスのインストール</span><span class="sxs-lookup"><span data-stu-id="8c0f1-126">Install DIXF service</span></span>

1. <span data-ttu-id="8c0f1-127">ZIP ファイルを展開した場所に移動し、**DIXF msi** フォルダーで **DIXF\_Service\_x64.msi** を右クリックし、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-127">Go to the location where you extracted the zip file, and then, in the **DIXF msi** folder, right-click **DIXF\_Service\_x64.msi**, and select **Run**.</span></span>
2. <span data-ttu-id="8c0f1-128">ウィザードが開始したら、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-128">When the wizard starts, select **Next**.</span></span>
3. <span data-ttu-id="8c0f1-129">ライセンス条項を受け入れ、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-129">Accept the license terms, and then select **Next**.</span></span>
4. <span data-ttu-id="8c0f1-130">サービスのアカウントを選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-130">Select an account for the service, and then select **Next**.</span></span> <span data-ttu-id="8c0f1-131">アカウントは、管理者権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-131">The account should have admin rights.</span></span> <span data-ttu-id="8c0f1-132">**ネットワーク サービス** チェック ボックスをオンにした場合、ネットワーク サービス アカウントに管理者権限があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-132">If you select the **Network Service** check box, verify that the network service account has admin rights.</span></span> <span data-ttu-id="8c0f1-133">それ以外の場合、チェック ボックスをオフにし、管理者アカウントのユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-133">Otherwise, clear the check box, and enter an admin account user name and password.</span></span> <span data-ttu-id="8c0f1-134">その後、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-134">Then select **Next**.</span></span>
5. <span data-ttu-id="8c0f1-135">SQL Server のバージョンを選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-135">Select the SQL Server version, and then select **Next**.</span></span>
6. <span data-ttu-id="8c0f1-136">**インストール** を選択し、ウィザードが完了したら **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-136">Select **Install**, and then, when the wizard is completed, select **Finish**.</span></span>

## <a name="copy-binaries"></a><span data-ttu-id="8c0f1-137">バイナリのコピー</span><span class="sxs-lookup"><span data-stu-id="8c0f1-137">Copy binaries</span></span>
<span data-ttu-id="8c0f1-138">ZIP ファイルを展開した場所に移動し、以下のファイルを **Program Files (x86)\\Microsoft Dynamics AX\\50\\Client\\Bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-138">Go to the location where you extracted the zip file, and copy the following files to the **Program Files (x86)\\Microsoft Dynamics AX\\50\\Client\\Bin** folder:</span></span>

- <span data-ttu-id="8c0f1-139">Microsoft.Dynamics.AX.Framework.Tools.DMT.dll</span><span class="sxs-lookup"><span data-stu-id="8c0f1-139">Microsoft.Dynamics.AX.Framework.Tools.DMT.dll</span></span>
- <span data-ttu-id="8c0f1-140">Interop.Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="8c0f1-140">Interop.Shell32.dll</span></span>

## <a name="install-dmt-components-for-ax-2009"></a><span data-ttu-id="8c0f1-141">AX 2009 の DMT コンポーネントのインストール</span><span class="sxs-lookup"><span data-stu-id="8c0f1-141">Install DMT components for AX 2009</span></span>
<span data-ttu-id="8c0f1-142">DMT をインストールする方法は 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-142">There are two ways to install the DMT.</span></span> <span data-ttu-id="8c0f1-143">結合された XPO ファイルまたはアプリケーション修正プログラムを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-143">You can use the combined XPO file or an application hotfix.</span></span> <span data-ttu-id="8c0f1-144">Microsoft Dynamics Lifecycle Services (LCS) 実装プロジェクトを使用している場合、アプリケーション修正プログラムを使用します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-144">If you're using a Microsoft Dynamics Lifecycle Services (LCS) Implementation project, use the application hotfix.</span></span> <span data-ttu-id="8c0f1-145">インストールには、約 7 時間かかります。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-145">Installation takes approximately seven hours.</span></span>

### <a name="combined-xpo-file"></a><span data-ttu-id="8c0f1-146">結合された XPO ファイル</span><span class="sxs-lookup"><span data-stu-id="8c0f1-146">Combined XPO file</span></span>
1. <span data-ttu-id="8c0f1-147">結合された XPO ファイルを **DMT_V1.0\CombinedXPO** から展開します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-147">Extract the combined XPO file from **DMT_V1.0\CombinedXPO**.</span></span>
2. <span data-ttu-id="8c0f1-148">AX 2009 に結合された XPO ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-148">Import the combined XPO file into AX 2009.</span></span>
3. <span data-ttu-id="8c0f1-149">**DMT_V1.0\Label ファイル**から **Program Files\\Microsoft Dynamics AX\\50\\Application\\Appl\\<NameOfYourDeployment\>** フォルダーにラベル ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-149">Copy the label file from **DMT_V1.0\Label file** to the **Program Files\\Microsoft Dynamics AX\\50\\Application\\Appl\\<NameOfYourDeployment\>** folder.</span></span>
4. <span data-ttu-id="8c0f1-150">Application Object Server (AOS) インスタンスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-150">Restart the Application Object Server (AOS) instance.</span></span>
5. <span data-ttu-id="8c0f1-151">AX 2009 で、**データ移行** \> **設定** \> **DMT アプリケーションのコンパイルと同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-151">In AX 2009, select **Data migration** \> **Setup** \> **Compile and synchronize DMT application**.</span></span>

<span data-ttu-id="8c0f1-152">ユーザーがログインしているレイヤーに結合された XPO ファイルがインポートされることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-152">Note that the combined XPO file is imported into the layer that the user is signed in to.</span></span>

### <a name="application-hotfix"></a><span data-ttu-id="8c0f1-153">アプリケーションの修正プログラム</span><span class="sxs-lookup"><span data-stu-id="8c0f1-153">Application hotfix</span></span>
1. <span data-ttu-id="8c0f1-154">**DMT_V1.0\\ApplicationHotfix\\DynamicsAX2009-KB4010403-SP1** に移動し、**setup.exe** を右クリックして **実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-154">Go to **DMT_V1.0\\ApplicationHotfix\\DynamicsAX2009-KB4010403-SP1**, right-click **setup.exe**, and then select **Run**.</span></span>
2. <span data-ttu-id="8c0f1-155">AX 2009 のアプリケーション オブジェクト ツリー (AOT) で、**LegalEntityId** フィールドが **DMTCustomerAddressView** ビューと **DMTVendorAddressView** ビューに追加されていることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-155">In AX 2009, in the Application Object Tree (AOT), notice that the **LegalEntityId** field has been added to the **DMTCustomerAddressView** and **DMTVendorAddressView** views.</span></span>
3. <span data-ttu-id="8c0f1-156">**データ移行** \> **設定** \> **DMT アプリケーションのコンパイルと同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-156">Select **Data migration** \> **Setup** \> **Compile and synchronize DMT application**.</span></span>

## <a name="parameter-setup"></a><span data-ttu-id="8c0f1-157">パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="8c0f1-157">Parameter setup</span></span>
<span data-ttu-id="8c0f1-158">ZIP ファイルを展開した場所に移動し、**defaultvalue.xlsx** を検索します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-158">Go to the location to where you extracted the zip file, and find **defaultvalue.xlsx**.</span></span>

> [!NOTE]
> <span data-ttu-id="8c0f1-159">ファイルは .xlsx 形式に保存されます。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-159">The file is saved in .xlsx format.</span></span> <span data-ttu-id="8c0f1-160">拡張機能を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-160">Don't change the extension.</span></span> <span data-ttu-id="8c0f1-161">このファイルを **既定のコンフィギュレーション** パラメーターの入力として入力したら、**すべてのファイル** を選択して .xlsx 形式を選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-161">When you provide this file as input for the **Default configuration** parameter, select **All Files** so that you can select the .xlsx format.</span></span> <span data-ttu-id="8c0f1-162">この形式を選択しない場合、マッピングの生成を開始するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-162">If you don't select this format, errors will occur when you start to generate mappings.</span></span>

1. <span data-ttu-id="8c0f1-163">AX 2009 で、**データ移行**\>**設定**\>**既定のマップを構成する** を選択し、次のフィールドに適切な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-163">In AX 2009, select **Data migration** \> **Setup** \> **Configure default maps**, and enter the appropriate information in the following fields:</span></span>

    - <span data-ttu-id="8c0f1-164">**既定のコンフィギュレーション**: Microsoft Excel ファイルのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-164">**Default configuration** – Enter the path of the Microsoft Excel file.</span></span>
    - <span data-ttu-id="8c0f1-165">**エクスポート ファイルのパス**: サービスがアクセスできるサーバーのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-165">**Export file path** – Enter the server path that can be accessed by the service.</span></span>
    - <span data-ttu-id="8c0f1-166">**SQL Server のユーザー名とパスワード**: AX 2009 データベースの SQL 認証資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-166">**SQL Server user and password** – Enter the SQL authentication credentials for the AX 2009 database.</span></span>

2. <span data-ttu-id="8c0f1-167">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-167">Close the form.</span></span>
3. <span data-ttu-id="8c0f1-168">**設定** で、**接続の構成** を選択し、次のフィールドに適切な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-168">Under **Setup**, select **Configure connections**, and enter the appropriate information on the following fields:</span></span>

    - <span data-ttu-id="8c0f1-169">**DIXF サービス ホスト**: DIXF サービスのインストールのホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-169">**DIXF service host** – Enter the host name of the DIXF service installation.</span></span>
    - <span data-ttu-id="8c0f1-170">**テナント URL**: Finance and Operations の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-170">**Tenant URL** – Enter the Finance and Operations URL.</span></span> <span data-ttu-id="8c0f1-171">テナントが不明な場合は、Finance and Operations の web.config ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-171">If you aren't sure of the tenant, see the Finance and Operations web.config file.</span></span>

    > <span data-ttu-id="8c0f1-172">[!注意} Azure ポータルでは、Azure Active Directory (AAD) で新しいアプリケーションを作成するときは、2 つのオプションから選択できます。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-172">[!NOTE} In the Azure Portal, when you create a new app in the Azure Active Directory (AAD), you can select from two options.</span></span> <span data-ttu-id="8c0f1-173">**Web API** と **ネイティブ**。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-173">**Web API** and **Native**.</span></span> <span data-ttu-id="8c0f1-174">このインスタンスでは、**ネイティブ** を選択し、ネイティブ AAD アプリケーションへのアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-174">In this instance, select **Native** and grant permissions to native AAD app.</span></span>

## <a name="multi-box-setup"></a><span data-ttu-id="8c0f1-175">マルチボックスの設定</span><span class="sxs-lookup"><span data-stu-id="8c0f1-175">Multi-box setup</span></span>
<span data-ttu-id="8c0f1-176">マルチボックスの設定の場合、次のコンピューターが必要です。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-176">For a multi-box setup, you must have the following machines:</span></span>

- <span data-ttu-id="8c0f1-177">AX 2009 データベースおよび DIXF サービスがインストールされているコンピューター A</span><span class="sxs-lookup"><span data-stu-id="8c0f1-177">Machine A, where the AX 2009 database and DIXF service are installed</span></span>
- <span data-ttu-id="8c0f1-178">AX 2009 AOS インスタンスがインストールされているコンピューター B</span><span class="sxs-lookup"><span data-stu-id="8c0f1-178">Machine B, where the AX 2009 AOS instance is installed</span></span>
- <span data-ttu-id="8c0f1-179">AX 2009 クライアントがインストールされているコンピューター C</span><span class="sxs-lookup"><span data-stu-id="8c0f1-179">Machine C, where the AX 2009 client is installed</span></span>

<span data-ttu-id="8c0f1-180">この 3 コンピューター設定では、コンピューター C はコンピューター B の AOS インスタンスに接続するように構成されています。コンピューター B は、コンピューター A で構成されているデータベースに接続されます。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-180">In this three-machine setup, machine C is configured to connect to the AOS instance on machine B. Machine B is connected to the database that is configured on machine A.</span></span>

### <a name="dixf-service-machine-prerequisites-machine-a"></a><span data-ttu-id="8c0f1-181">DIXF サービス コンピューターの前提条件 (コンピューター A)</span><span class="sxs-lookup"><span data-stu-id="8c0f1-181">DIXF service machine prerequisites (machine A)</span></span>
<span data-ttu-id="8c0f1-182">コンピューター A の DIXF サービスには、次の前提条件があります。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-182">The DIXF service on machine A has the following prerequisites:</span></span>

- <span data-ttu-id="8c0f1-183">SQL Server 2008/2012/2014</span><span class="sxs-lookup"><span data-stu-id="8c0f1-183">SQL Server 2008/2012/2014</span></span>
- <span data-ttu-id="8c0f1-184">.NET Framework バージョン 4.5</span><span class="sxs-lookup"><span data-stu-id="8c0f1-184">The .NET Framework version 4.5</span></span>
- <span data-ttu-id="8c0f1-185">Access データベース エンジン</span><span class="sxs-lookup"><span data-stu-id="8c0f1-185">Access database engines</span></span>

    - <span data-ttu-id="8c0f1-186">**SQL Server 2008 の場合:** Access エンジン 32 ビットおよび 64 ビット (Microsoft Excel が 64 ビットの場合)</span><span class="sxs-lookup"><span data-stu-id="8c0f1-186">**For SQL Server 2008:** Access engine 32-bit and 64-bit (if Microsoft Excel is 64-bit)</span></span>
    - <span data-ttu-id="8c0f1-187">**SQL Server 2012 以降の場合:** Access エンジン 64 ビット</span><span class="sxs-lookup"><span data-stu-id="8c0f1-187">**For SQL Server 2012 or later:** Access engine 64-bit</span></span>

- <span data-ttu-id="8c0f1-188">AX 2009 データベース (SQL Server で構成)</span><span class="sxs-lookup"><span data-stu-id="8c0f1-188">AX 2009 database (configured on SQL Server)</span></span>

### <a name="aos-machine-prerequisites-machine-b"></a><span data-ttu-id="8c0f1-189">AOS コンピューターの前提条件 (コンピューター B)</span><span class="sxs-lookup"><span data-stu-id="8c0f1-189">AOS machine prerequisites (machine B)</span></span>
<span data-ttu-id="8c0f1-190">コンピューター B の AOS のインストールには、次の前提条件があります。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-190">The AOS installation on machine B has the following prerequisites:</span></span>

- <span data-ttu-id="8c0f1-191">AX 2009 AOS サーバー</span><span class="sxs-lookup"><span data-stu-id="8c0f1-191">AX 2009 AOS Server</span></span>
- <span data-ttu-id="8c0f1-192">アプリケーション ファイル</span><span class="sxs-lookup"><span data-stu-id="8c0f1-192">Application files</span></span>

### <a name="client-machine-prerequisites-machine-c"></a><span data-ttu-id="8c0f1-193">クライアント コンピューターの前提条件 (コンピューター C)</span><span class="sxs-lookup"><span data-stu-id="8c0f1-193">Client machine prerequisites (machine C)</span></span>
<span data-ttu-id="8c0f1-194">コンピューター C のクライアントのインストールには、次の前提条件があります。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-194">The client installation on machine C has the following prerequisites:</span></span>

- <span data-ttu-id="8c0f1-195">AX 2009 クライアント</span><span class="sxs-lookup"><span data-stu-id="8c0f1-195">AX 2009 client</span></span>

### <a name="shared-folder-permissions"></a><span data-ttu-id="8c0f1-196">共有フォルダーのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="8c0f1-196">Shared folder permissions</span></span>

<span data-ttu-id="8c0f1-197">既定のコンフィギュレーション ファイルとエクスポート パッケージ ファイルのパスは共有する必要があり、クライアント ユーザーおよび DIXF サービスにはこれらのファイルへの読み取り/書き込みアクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-197">The path of the default configuration file and the export package file should be shared, and client users and the DIXF service should have read/write access to these files.</span></span> <span data-ttu-id="8c0f1-198">アクセス権を付与するには、**データ移行** \> **設定** \> **マップの構成と生成** を選択し、**パスの検証** を選択して必要なアクセス権があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-198">To grant this access, select **Data migration** \> **Setup** \> **Configure and generate maps**, and then select **Validate path** to verify that the required access is available.</span></span>

### <a name="set-up-parameters"></a><span data-ttu-id="8c0f1-199">パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="8c0f1-199">Set up parameters</span></span>

1. <span data-ttu-id="8c0f1-200">**データ移行** \> **設定** \> **接続の構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-200">Select **Data migration** \> **Setup** \> **Configure connections**.</span></span>
2. <span data-ttu-id="8c0f1-201">**DIXF サービス ホスト** フィールドに、DIXF サービスがインストールされているリモート コンピューターの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-201">In the **DIXF service host** field, enter the name of the remote machine where the DIXF service is installed.</span></span> <span data-ttu-id="8c0f1-202">既定では、名前は **localhost** です。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-202">By default, the name is **localhost**.</span></span>
3. <span data-ttu-id="8c0f1-203">**検証** を選択し、クライアントが DIXF サービスにアクセスできることを検証します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-203">Select **Validate** to validate that the client can access the DIXF service.</span></span>

### <a name="workarounds"></a><span data-ttu-id="8c0f1-204">回避策</span><span class="sxs-lookup"><span data-stu-id="8c0f1-204">Workarounds</span></span>
<span data-ttu-id="8c0f1-205">"DIXF サービスを利用できません" というエラー メッセージが表示される場合、次の回避方法を実行してポート 7000 のサービスの接続を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-205">If you receive an error message that states, "DIXF service is unavailable," complete the following workaround to enable a service connection for port 7000.</span></span>

1. <span data-ttu-id="8c0f1-206">ポート 7000 を開いた後、DMT サービス コンピューターの受信ルールで **ファイアウォール設定** を選択して **実行** \> **wf.msc** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-206">Open port 7000, and then, for inbound rules on the DMT service machine, select **Firewall settings**, and then select **Run** \> **wf.msc**.</span></span>
2. <span data-ttu-id="8c0f1-207">**受信ルール** \> **新しいルール** を選択した後、**ルール タイプ** タブで、**ポート** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-207">Select **Inbound Rules** \> **New rule**, and then, on the **Rule Type** tab, select **Port**, and then select **Next**.</span></span>
3. <span data-ttu-id="8c0f1-208">**特定のローカル ポート** フィールドに、**7000** と入力し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-208">In the **Specific local ports** field, enter **7000**, and then select **Next**.</span></span>
4. <span data-ttu-id="8c0f1-209">**接続を許可する** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-209">Select **Allow the connection**, and then select **Next**.</span></span>
5. <span data-ttu-id="8c0f1-210">3 つのチェック ボックスをすべてオンにしてすべてのルールを適用し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-210">Select all three check boxes to apply all the rules, and then select **Next**.</span></span>
6. <span data-ttu-id="8c0f1-211">ルールの名前を入力し、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-211">Enter the name of the rule, and then select **Finish**.</span></span>
7. <span data-ttu-id="8c0f1-212">送信ルールでこれらの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="8c0f1-212">Repeat these steps for outbound rules.</span></span>


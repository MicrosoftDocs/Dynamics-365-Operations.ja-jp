---
title: "SQL Server 2014 用 AX 2012 R2 CU7 データのインポート/エクスポート フレームワークのインストール"
description: "Microsoft Dynamics AX 2012 R2 の累積更新プログラム 7 (CU7) のデータ インポート/エクスポート フレームワークを SQL Server 2014 Integration Services またはそれ以降で使用するには、AX 2012 R2 CU7 をインストールして、更新プログラム KB 3018235KB 3018235 を適用する必要があります。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 71103
ms.assetid: ee28572c-e38d-4c2a-a191-f2631f291e5f
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 83e5e517ed38be46b30708a8f7905a1eed6ddb77
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="install-the-ax-2012-r2-cu7-data-importexport-framework-for-sql-server-2014"></a><span data-ttu-id="53806-103">SQL Server 2014 用 AX 2012 R2 CU7 データのインポート/エクスポート フレームワークのインストール</span><span class="sxs-lookup"><span data-stu-id="53806-103">Install the AX 2012 R2 CU7 Data import/export framework for SQL Server 2014</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="53806-104">Microsoft Dynamics AX 2012 R2 の累積更新プログラム 7 (CU7) のデータ インポート/エクスポート フレームワークを SQL Server 2014 Integration Services またはそれ以降で使用するには、AX 2012 R2 CU7 をインストールして、更新プログラム <a href="https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235">KB 3018235</a> を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53806-104">To use the Data import/export framework for Microsoft Dynamics AX 2012 R2 cumulative update 7 (CU7) with SQL Server 2014 Integration Services or later, you must install AX 2012 R2 CU7, and then apply the update <a href="https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235">KB 3018235</a>.</span></span>

<span data-ttu-id="53806-105">次の手順は、SQL Server 2014 またはそれ以降のバージョンがインストールされている環境に適用されます。</span><span class="sxs-lookup"><span data-stu-id="53806-105">The following instructions apply for an environment in which SQL Server 2014 or a later version is installed.</span></span> <span data-ttu-id="53806-106">SQL Server 2008 または SQL Server 2012 統合サービスを実行している場合は、更新プログラムのインストーラーを使用して Dynamics AX 2012 R2 CU7 のデータのインポート/エクスポート フレームワークをインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="53806-106">If you are running SQL Server 2008 or SQL Server 2012 Integration Services, you can install the Data Import/Export Framework for Dynamics AX 2012 R2 CU7 by using the update installer.</span></span> <span data-ttu-id="53806-107">詳細については、[データのインポート/エクスポート フレームワーク バイナリ更新プログラム (CU7) のインストール](https://technet.microsoft.com/en-us/library/hh538446.aspx#DIXFInstall) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53806-107">For more information, see [Install the Data Import/Export Framework binary updates (CU7)](https://technet.microsoft.com/en-us/library/hh538446.aspx#DIXFInstall).</span></span> <span data-ttu-id="53806-108">データのインポート/エクスポート フレームワークでサポートされる統合サービスのバージョンを確認するには、[[Microsoft Dynamics AX 2012 のシステム要件](http://go.microsoft.com/fwlink/?LinkId=165377)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53806-108">To see which versions of Integration Services are supported with the Data Import/Export Framework, see the [Microsoft Dynamics AX 2012 System Requirements](http://go.microsoft.com/fwlink/?LinkId=165377).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="53806-109">準備</span><span class="sxs-lookup"><span data-stu-id="53806-109">Before you begin</span></span>
1.  <span data-ttu-id="53806-110">CU7 hotfix パッケージをダウンロードしてローカル フォルダーに展開します。</span><span class="sxs-lookup"><span data-stu-id="53806-110">Download the CU7 hotfix package, and extract it to a local folder.</span></span> <span data-ttu-id="53806-111">ダウンロードを抽出するには、[ダウンロードの手順に従い、CustomerSource、PartnerSource、または Lifecycle Services ](https://technet.microsoft.com/en-us/library/hh538446.aspx#Download) から更新プログラムを抽出します **。**</span><span class="sxs-lookup"><span data-stu-id="53806-111">To extract the download, follow the instructions in the [Download and extract an update from CustomerSource, PartnerSource, or Lifecycle Services](https://technet.microsoft.com/en-us/library/hh538446.aspx#Download)**.**</span></span>
2.  <span data-ttu-id="53806-112">[KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235) の修正プログラム パッケージをダウンロードしてローカル フォルダーに展開してください。</span><span class="sxs-lookup"><span data-stu-id="53806-112">Download the hotfix package for [KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235), and extract it to a local folder.</span></span>

## <a name="install-the-ax-2012-r2-cu7-data-importexport-framework-for-use-with-sql-server-2014-integration-services"></a><span data-ttu-id="53806-113">SQL Server 2014 Integration Services で使用する AX 2012 R2 CU7 データのインポート/エクスポート フレームワークのインストール</span><span class="sxs-lookup"><span data-stu-id="53806-113">Install the AX 2012 R2 CU7 Data import/export framework for use with SQL Server 2014 Integration Services</span></span>
<span data-ttu-id="53806-114">Integration Services を実行しているコンピューターで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="53806-114">On the computer that is running Integration Services, follow these steps.</span></span>

1.  <span data-ttu-id="53806-115">Windows PowerShell を実行します。</span><span class="sxs-lookup"><span data-stu-id="53806-115">Run Windows PowerShell.</span></span>
2.  <span data-ttu-id="53806-116">修正プログラムのパッケージの Support フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="53806-116">Navigate to the Support folder of the hotfix package.</span></span>
3.  <span data-ttu-id="53806-117">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="53806-117">Run the following script:</span></span>

        Install-DIXFService.ps1.

4.  <span data-ttu-id="53806-118">画面の指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="53806-118">Follow the on-screen instructions.</span></span>
5.  <span data-ttu-id="53806-119">Microsoft Dynamics AX 2012 R2 CU7 からデータ インポート/エクスポート フレームワーク サービス MSI を検索するように求められます。</span><span class="sxs-lookup"><span data-stu-id="53806-119">You will be asked to locate the Data Import/Export Framework service MSI from Microsoft Dynamics AX 2012 R2 CU7.</span></span> <span data-ttu-id="53806-120">このファイルは、**MSI\\ DIXF \_サービス\_x64** または **MSI\\DIXF\_サービス\_x86** フォルダーにあります。 </span><span class="sxs-lookup"><span data-stu-id="53806-120">This file can be found in the **MSI\\DIXF\_Service\_x64** or **MSI\\DIXF\_Service\_x86** folder.</span></span> <span data-ttu-id="53806-121">スクリプトが対応する MSP を見つけることがない場合、探すように求められます。</span><span class="sxs-lookup"><span data-stu-id="53806-121">If the script is unable to locate the corresponding MSP, you will be asked to locate it.</span></span> <span data-ttu-id="53806-122">MSP は、修正プログラム パッケージ フォルダー ([KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235))の **MSI\\DIXF\_Service\_x64** または **MSI\\DIXF\_Service\_x86** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="53806-122">The MSP can be found in the **MSI\\DIXF\_Service\_x64** or **MSI\\DIXF\_Service\_x86** folder in the hotfix package folder ([KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235)).</span></span> <span data-ttu-id="53806-123">データ インポート/エクスポート フレームワーク サービスを、**ネットワーク サービス** アカウントでインストールするかどうかを求められます。</span><span class="sxs-lookup"><span data-stu-id="53806-123">You will be asked if you want the Data Import/Export Framework Service to be installed under the **Network Service** account.</span></span> <span data-ttu-id="53806-124">回答が**いいえ**である場合、サービスを実行するにはユーザー名とパスワード (ドメイン\\ユーザー名の形式) を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="53806-124">If you answer **No**, you will be asked to enter the username (DOMAIN\\username format) and password to run the service.</span></span> <span data-ttu-id="53806-125">インストールを開始してください。</span><span class="sxs-lookup"><span data-stu-id="53806-125">Installation should start.</span></span>

## <a name="verify-installation"></a><span data-ttu-id="53806-126">インストールの確認</span><span class="sxs-lookup"><span data-stu-id="53806-126">Verify installation</span></span>
<span data-ttu-id="53806-127">既定では、スクリプトのログは **InstallDIXFService-&lt; 日付 &gt;\_&lt; 時間 &gt;.log** という名前のファイルに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="53806-127">By default the script’s log will be written to a file that is named **InstallDIXFService-&lt;date&gt;\_&lt;time &gt;.log**.</span></span> <span data-ttu-id="53806-128">ファイルから正常なインストールの報告があったことを確認します。</span><span class="sxs-lookup"><span data-stu-id="53806-128">Verify that the file reports a successful installation.</span></span> <span data-ttu-id="53806-129">インストールに失敗すると、**DIXFService\_インストール -&lt;日付&gt;\_&lt;時間 &gt;.log** という名前の MSI によりログが生成されます。</span><span class="sxs-lookup"><span data-stu-id="53806-129">If the installation fails, the log produced by the MSI is named **DIXFService\_install -&lt;date&gt;\_&lt;time &gt;.log**.</span></span> <span data-ttu-id="53806-130">検索を行い、一覧表示された問題を調査します。</span><span class="sxs-lookup"><span data-stu-id="53806-130">Search for it, and investigate the listed issues.</span></span>

## <a name="install-the-data-importexport-framework-client-and-server-components"></a><span data-ttu-id="53806-131">データのインポート/エクスポート フレームワークのクライアントおよびサーバー コンポーネントのインストール</span><span class="sxs-lookup"><span data-stu-id="53806-131">Install the Data import/export framework Client and Server Components</span></span>
<span data-ttu-id="53806-132">pw\_DMF サービス コンポーネントのインストールが完了した後、データのインポート/エクスポート フレームワーク クライアントと AOS コンポーネントを通常の方法でインストールします。</span><span class="sxs-lookup"><span data-stu-id="53806-132">After installation of pw\_DMF Service component has completed, install the Data Import/Export Framework Client and AOS components the ordinary way.</span></span>

1.  <span data-ttu-id="53806-133">適切なコンピューターにコンポーネントの CU7 バージョンをインストールします。</span><span class="sxs-lookup"><span data-stu-id="53806-133">Install the CU7 version of the components on the appropriate computers.</span></span> <span data-ttu-id="53806-134">[データのインポート/エクスポート フレームワーク バイナリ更新プログラム (CU7) のインストール](https://technet.microsoft.com/en-us/library/hh538446.aspx#DIXFInstall) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53806-134">See [Install the Data Import/Export Framework binary updates (CU7)](https://technet.microsoft.com/en-us/library/hh538446.aspx#DIXFInstall).</span></span>
2.  <span data-ttu-id="53806-135">修正プログラム [KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235) を適切なコンピューターに適用します。</span><span class="sxs-lookup"><span data-stu-id="53806-135">Apply hotfix [KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235) on the appropriate computers.</span></span>

## <a name="optional-create-a-silent-installation-windows-powershell-script"></a><span data-ttu-id="53806-136">オプション: サイレント インストール Windows PowerShell スクリプトを作成します。</span><span class="sxs-lookup"><span data-stu-id="53806-136">Optional: Create a silent installation Windows PowerShell script</span></span>
<span data-ttu-id="53806-137">適切なパラメーターで **Install-DIXFService.ps1** スクリプトを指定した場合、サイレント インストールを行うには、スクリプトを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="53806-137">If you supply the **Install-DIXFService.ps1** script with the appropriate parameters you can use the script to do a silent installation.</span></span> <span data-ttu-id="53806-138">次のテーブルに、利用可能なパラメーターとその使用方法の簡単な説明を示します。</span><span class="sxs-lookup"><span data-stu-id="53806-138">The following table provides a brief description of the parameters that are available and how to use them.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53806-139">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="53806-139">Parameter name</span></span></td>
<td><span data-ttu-id="53806-140">説明</span><span class="sxs-lookup"><span data-stu-id="53806-140">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53806-141">UseNetworkService</span><span class="sxs-lookup"><span data-stu-id="53806-141">UseNetworkService</span></span></td>
<td><span data-ttu-id="53806-142">これは切り替えです。</span><span class="sxs-lookup"><span data-stu-id="53806-142">This is a switch:</span></span>
<ul>
<li><span data-ttu-id="53806-143">ネットワーク サービス アカウントでサービスをインストールする場合は、コマンドに <strong>UseNetworkService</strong> を含めます。</span><span class="sxs-lookup"><span data-stu-id="53806-143">If you want to install the service under the Network Service account, include <strong>UseNetworkService</strong> in your command.</span></span></li>
<li><span data-ttu-id="53806-144"><strong>UseNetworkService</strong> が指定されている場合、<strong>ServiceAccount</strong> および <strong>ServicePassword</strong> に対して指定された値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="53806-144">If <strong>UseNetworkService</strong> is specified, any value specified for <strong>ServiceAccount</strong> and <strong>ServicePassword</strong> will be ignored.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53806-145">ServiceAccount</span><span class="sxs-lookup"><span data-stu-id="53806-145">ServiceAccount</span></span></td>
<td><span data-ttu-id="53806-146">サービスが実行されるアカウントを指定します。</span><span class="sxs-lookup"><span data-stu-id="53806-146">Specifies the account the service will be run under.</span></span> <span data-ttu-id="53806-147">UseNetworkService が使用されていない場合は、このパラメーターを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53806-147">This parameter must be supplied if UseNetworkService is not used.</span></span> <span data-ttu-id="53806-148">これは、ドメイン \ ユーザー名の形式にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="53806-148">This should be in DOMAIN\username format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53806-149">ServicePassword</span><span class="sxs-lookup"><span data-stu-id="53806-149">ServicePassword</span></span></td>
<td><span data-ttu-id="53806-150">サービスが実行されるアカウントのパスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="53806-150">Specifies the password for account that the service will run under.</span></span> <span data-ttu-id="53806-151"><strong>UseNetworkService</strong> が使用されていない場合は、このパラメーターを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53806-151">This parameter must be supplied if <strong>UseNetworkService</strong> is not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53806-152">MSIFileName 必須</span><span class="sxs-lookup"><span data-stu-id="53806-152">MSIFileName Required</span></span></td>
<td><span data-ttu-id="53806-153">Microsoft Dynamics AX 2012 R2 CU7 修正プログラムの <strong>dixf_service_</strong><em>&lt;アーキテクチャ&gt;</em><strong>.msi</strong> のパス。</span><span class="sxs-lookup"><span data-stu-id="53806-153">The path of the <strong>dixf_service_</strong><em>&lt;architecture&gt;</em><strong>.msi</strong> file from the Microsoft Dynamics AX 2012 R2 CU7 hotfix.</span></span> <span data-ttu-id="53806-154">これは、相対パスまたは絶対パスにできます。</span><span class="sxs-lookup"><span data-stu-id="53806-154">This can be a relative or absolute path.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53806-155">MSPFileName</span><span class="sxs-lookup"><span data-stu-id="53806-155">MSPFileName</span></span></td>
<td><span data-ttu-id="53806-156"><strong>dixf_service_</strong><em>&lt;アーキテクチャ&gt;</em><strong>.msp</strong> ファイルのパス。</span><span class="sxs-lookup"><span data-stu-id="53806-156">The path of the <strong>dixf_service_</strong><em>&lt;architecture&gt;</em><strong>.msp</strong> file.</span></span> <span data-ttu-id="53806-157">修正プログラムのパッケージでサポート フォルダーの Install-DIXFService.ps1 スクリプトを実行すると、スクリプトがファイルを自動的に見つけることができる必要があるため、このパラメータは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="53806-157">If the Install-DIXFService.ps1 script is run from the Support folder in a hotfix package, this parameter is not required, because the script should be able to find the file automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53806-158">LogFileName</span><span class="sxs-lookup"><span data-stu-id="53806-158">LogFileName</span></span></td>
<td><span data-ttu-id="53806-159">スクリプトのログ ファイルのパス。</span><span class="sxs-lookup"><span data-stu-id="53806-159">The path of the log file for the script.</span></span> <span data-ttu-id="53806-160">このパラメータが設定されていない場合は、現在のディレクトリが使用されています。</span><span class="sxs-lookup"><span data-stu-id="53806-160">If this parameter is not set, the current directory is used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53806-161">MSIExecLogFileName</span><span class="sxs-lookup"><span data-stu-id="53806-161">MSIExecLogFileName</span></span></td>
<td><span data-ttu-id="53806-162">実際のインストール ログが存在する場所である MSIExec のログ ファイルのパス。</span><span class="sxs-lookup"><span data-stu-id="53806-162">The path of the log file for MSIExec, which is where the actual installation log can be found.</span></span> <span data-ttu-id="53806-163">このパラメータが設定されていない場合は、現在のディレクトリが使用されています。</span><span class="sxs-lookup"><span data-stu-id="53806-163">If this parameter is not set, the current directory is used.</span></span></td>
</tr>
</tbody>
</table>



### <a name="example-1-install-under-network-service-and-use-default-log-file-paths"></a><span data-ttu-id="53806-164">例 1: ネットワーク サービスの下でインストールし、既定のログ ファイルのパスを使用</span><span class="sxs-lookup"><span data-stu-id="53806-164">Example 1: Install under Network Service and use default log file paths</span></span>

    Install-DIXFService.ps1 -UseNetworkService -MSIFileName "C:\CU7Package\MSI\dixf_service_x64\dixf_service_x64.msi"

### <a name="example-2-install-as-a-specific-user-and-specify-log-file-paths"></a><span data-ttu-id="53806-165">例 2: 特定のユーザーとしてインストールおよびログファイルパスを指定</span><span class="sxs-lookup"><span data-stu-id="53806-165">Example 2: Install as a specific user and specify log file paths</span></span>

    Install-DIXFService.ps1 -ServiceAccount "MYDOMAIN\myuser" -ServicePassword "VerySecure.1234" 
    -MSIFileName "C:\CU7Package\MSI\dixf_service_x64\dixf_service_x64.msi" 
    –LogFileName "C:\MyLogs\DIXFService-script-log.txt" -MSIExecLogFileName "C:\MyLogs\DIXFService-MSIExec-log.txt"

<a name="additional-resources"></a><span data-ttu-id="53806-166">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="53806-166">Additional resources</span></span>
--------

[<span data-ttu-id="53806-167">複数のバージョン (DIXF) がある環境でデータのインポート / エクスポート フレームワークで使用される SQL Server Integration Services のバージョンを構成する</span><span class="sxs-lookup"><span data-stu-id="53806-167">Configure the version of SQL Server Integration Services used by the Data import/export framework in an environment with multiple versions (DIXF)</span></span>](configure-sql-server-integration-services-multiple-versions-dixf.md)





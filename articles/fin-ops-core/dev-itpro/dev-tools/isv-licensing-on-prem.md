---
title: 独立系ソフトウェア ベンダー (ISV) ライセンス (オンプレミス)
description: このトピックでは、オンプレミス環境における独立系ソフトウェア ベンダー (ISV) のライセンス機能について説明します。
author: jorisdg
manager: AnnBe
ms.date: 03/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 70381
ms.assetid: 90ae4ae6-f19a-4ea5-8bd9-1d45729b0636
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2018-03-07
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 6b5ad11ad6f93681af752ba10ab36036b45846d2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408963"
---
# <a name="independent-software-vendor-isv-licensing-on-premises"></a><span data-ttu-id="b2cbe-103">独立系ソフトウェア ベンダー (ISV) ライセンス (オンプレミス)</span><span class="sxs-lookup"><span data-stu-id="b2cbe-103">Independent software vendor (ISV) licensing (on-premises)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2cbe-104">このトピックでは、独立系ソフトウェア ベンダー (ISV) ライセンスをオンプレミス配置にインポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-104">This topic explains how to import independent software vendor (ISV) licenses into an on-premises deployment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2cbe-105">このトピックで説明するプロセスは、プラットフォーム更新プログラム 12 以降で展開されているオンプレミス環境のユーザーのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-105">The process that is described in this topic is available only for customers who have on-premises environments that are deployed with Platform update 12 or later.</span></span>

<span data-ttu-id="b2cbe-106">ISV ライセンスの福利厚生についての一般情報、ソリューションのライセンスを有効にする方法についての情報、および自己署名証明書に関連するその他の情報については、[独立系ソフトウェア ベンダー (ISV) ライセンス](isv-licensing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-106">For general information about the benefits of ISV licensing, information about how to enable licensing for your solution, and other information that is related to self-signed certificates, see [Independent software vendor (ISV) licensing](isv-licensing.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b2cbe-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="b2cbe-107">Prerequisites</span></span>
<span data-ttu-id="b2cbe-108">オンプレミス環境に ISV ライセンス ファイルをインポートする前に、次の前提条件が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-108">Before you import the ISV license file into your on-premises environment, verify that the following prerequisites are met:</span></span>

- <span data-ttu-id="b2cbe-109">最新のバージョンのローカル エージェントは、環境が配置されたときに使用されました。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-109">The most recent version of the local agent was used when the environment was deployed.</span></span>
- <span data-ttu-id="b2cbe-110">環境はプラットフォーム更新プログラム 12 で配置され、プラットフォーム更新プログラム 12 のすべての修正プログラムが適用されます。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-110">The environment is deployed with Platform update 12, and all hotfixes for Platform update 12 are applied.</span></span> <span data-ttu-id="b2cbe-111">Microsoft が ISV ライセンス シナリオの修正プログラムをリリースしたため、このステップは必須です。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-111">This step is mandatory because Microsoft has released a fix for an ISV licensing scenario.</span></span> <span data-ttu-id="b2cbe-112">最新の修正プログラムを入手するには、Microsoft Dynamics Lifecycle Services (LCS) の **環境の詳細** ページでタイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-112">To get the latest set of hotfixes, use the tiles on the **Environment details** page in Microsoft Dynamics Lifecycle Services (LCS).</span></span>
- <span data-ttu-id="b2cbe-113">ISV ライセンスをインポートする前に、環境を展開し、Application Object Server (AOS) サービスを実行している必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-113">Before you import the ISV license, the environment must be deployed, and the Application Object Server (AOS) service must be running.</span></span>
- <span data-ttu-id="b2cbe-114">ISV ライセンスをインポートする前に、ISV ソリューションをオンプレミス環境に適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-114">Before you import the ISV license, the ISV solution must be applied to the on-premises environment.</span></span> <span data-ttu-id="b2cbe-115">ISV ソリューションは、配置フロー中に設置環境に適用できます。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-115">The ISV solution can be applied to an on-premises environment during the deployment flow.</span></span> <span data-ttu-id="b2cbe-116">または、LCS の **更新プログラムの適用** フローを使用して配置後のステップとして ISV ソリューションを適用することができます。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-116">Alternatively, you can use the **Apply updates** flow in LCS to apply the ISV solution as a post-deployment step.</span></span> <span data-ttu-id="b2cbe-117">ライセンスをインポートする前に、ISV ソリューションが適用されていない場合、カスタマイズを使用できません。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-117">If the ISV solution isn't applied before you import the license, the customizations won't be enabled.</span></span>

## <a name="import-licenses"></a><span data-ttu-id="b2cbe-118">ライセンスのインポート</span><span class="sxs-lookup"><span data-stu-id="b2cbe-118">Import licenses</span></span>
<span data-ttu-id="b2cbe-119">オンプレミス プロジェクトに配置されているサンドボックス環境または本番環境では、次の手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-119">The following procedure can be used for a sandbox environment or a production environment that is deployed in an on-premises project.</span></span>

> [!NOTE]
> <span data-ttu-id="b2cbe-120">ISV ライセンスのインポートにはダウンタイムが必要なため、インポート時に環境内で業務トランザクションを実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-120">Because import of an ISV license requires downtime, no business transactions can be performed in the environment during import.</span></span> <span data-ttu-id="b2cbe-121">インポートを完了したら、だれもシステムを使用していないことと、公式ダウンタイム通知システムがすべてのユーザーに通知済みであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-121">When you complete the import, make sure that no one is using the system, and that an official downtime notice has been communicated to all the users.</span></span>

1. <span data-ttu-id="b2cbe-122">ライセンスを発行する顧客のテナント名と ID を収集します:</span><span class="sxs-lookup"><span data-stu-id="b2cbe-122">Collect the tenant name and ID for the customer to issue the license to:</span></span>

    1. <span data-ttu-id="b2cbe-123">環境がホストされている Service Fabric Explorer のインスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-123">Connect to the instance of Service Fabric Explorer where the environment is hosted.</span></span>
    2. <span data-ttu-id="b2cbe-124">**クラスタ** &gt; **アプリケーション** &gt; **AXSFType** &gt; **ファブリック:\\AXSF** の順に移動し、次に右のページで、**詳細** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-124">Go to **Clusters** &gt; **Applications** &gt; **AXSFType** &gt; **fabric:\\AXSF**, and then, on the right page, select the **Details** tab.</span></span>
    3. <span data-ttu-id="b2cbe-125">**パラメーター** テーブルで **License\_TenantDomainGuid** および **Licence\_TenantId** キーの値を検索します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-125">In the **Parameters** table, find the values for the **License\_TenantDomainGuid** and **Licence\_TenantId** keys.</span></span>

2. <span data-ttu-id="b2cbe-126">顧客のライセンス (テナント ID と名前) を生成し、証明書のプライベート キーを使用してライセンスを登録します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-126">Generate a license for the customer (tenant ID and name), and sign the license by using the certificate's private key.</span></span> <span data-ttu-id="b2cbe-127">ライセンス ファイルを作成するには、次のパラメーターを  AXUtil **genlicense**  コマンドに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-127">The following parameters must be passed to the AXUtil **genlicense** command to create the license file.</span></span> <span data-ttu-id="b2cbe-128">コマンドは XML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-128">The command will generate an XML file.</span></span>

    | <span data-ttu-id="b2cbe-129">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="b2cbe-129">Parameter name</span></span>  | <span data-ttu-id="b2cbe-130">説明</span><span class="sxs-lookup"><span data-stu-id="b2cbe-130">Description</span></span> |
    |-----------------|-------------|
    | <span data-ttu-id="b2cbe-131">ファイル</span><span class="sxs-lookup"><span data-stu-id="b2cbe-131">file</span></span>            | <span data-ttu-id="b2cbe-132">ライセンス ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-132">The name of the license file.</span></span> |
    | <span data-ttu-id="b2cbe-133">licensecode</span><span class="sxs-lookup"><span data-stu-id="b2cbe-133">licensecode</span></span>     | <span data-ttu-id="b2cbe-134">Microsoft Visual Studio のライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-134">The name of the license code from Microsoft Visual Studio.</span></span> |
    | <span data-ttu-id="b2cbe-135">certificatepath</span><span class="sxs-lookup"><span data-stu-id="b2cbe-135">certificatepath</span></span> | <span data-ttu-id="b2cbe-136">証明書のプライベート キーのパス。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-136">The path of the certificate's private key.</span></span> |
    | <span data-ttu-id="b2cbe-137">パスワード</span><span class="sxs-lookup"><span data-stu-id="b2cbe-137">password</span></span>        | <span data-ttu-id="b2cbe-138">証明書のプライベート キーのパスワード。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-138">The password of the certificate's private key.</span></span> |
    | <span data-ttu-id="b2cbe-139">顧客</span><span class="sxs-lookup"><span data-stu-id="b2cbe-139">customer</span></span>        | <span data-ttu-id="b2cbe-140">顧客のテナント名。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-140">The customer's tenant name.</span></span> |
    | <span data-ttu-id="b2cbe-141">serialnumber</span><span class="sxs-lookup"><span data-stu-id="b2cbe-141">serialnumber</span></span>    | <span data-ttu-id="b2cbe-142">顧客のテナント ID。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-142">The customer's tenant ID.</span></span> |
    | <span data-ttu-id="b2cbe-143">expirationdate</span><span class="sxs-lookup"><span data-stu-id="b2cbe-143">expirationdate</span></span>  | <span data-ttu-id="b2cbe-144">オプション: ライセンスの有効期限。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-144">Optional: The expiration date of the license.</span></span> |
    | <span data-ttu-id="b2cbe-145">usercount</span><span class="sxs-lookup"><span data-stu-id="b2cbe-145">usercount</span></span>       | <span data-ttu-id="b2cbe-146">オプション: カスタム検証ロジックに必要となる可能性がある数値。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-146">Optional: The number that can be required for the custom validation logic.</span></span> <span data-ttu-id="b2cbe-147">この数はユーザー数が可能ですが、ユーザーに限定されるものではありません。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-147">This number can be the number of users, but it isn't limited to users.</span></span> |

    <span data-ttu-id="b2cbe-148">コマンドの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-148">Here is an example of the command.</span></span>

    ```Console
    C:\AOSService\PackagesLocalDirectory\Bin\axutil genlicense /file:c:\templicense.txt /certificatepath:c:\tempisvcert.pfx /licensecode:ISVLicenseCode /customer:TAEOfficial.ccsctp.net /serialnumber:4dbfcf74-c5a6-4727-b638-d56e51d1f381 /password:********
    ```

3. <span data-ttu-id="b2cbe-149">生成されたライセンスを fabric:/AXSF を実行しているマシンの 1 つのフォルダーにコピーし、fabric:/AXSF が正常であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-149">Copy the licenses that are generated to a folder on one of the machines that is running fabric:/AXSF, and verify that fabric:/AXSF is healthy.</span></span>
4. <span data-ttu-id="b2cbe-150">AOS コンピューターのいずれかから **Import-LicensePackage.ps1** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-150">Run the **Import-LicensePackage.ps1** script from one of the AOS machines.</span></span> <span data-ttu-id="b2cbe-151">このスクリプトは、LCS 内の共有アセット ライブラリにある  **モデル** タブの最新の **配置スクリプト** フォルダーで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-151">You can find this script in the latest **Deployment scripts** folder on the **Model** tab in the Shared asset library in LCS.</span></span> <span data-ttu-id="b2cbe-152">スクリプトに渡す必要があるパラメータの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-152">Here is a list of the parameters that you must pass to the script:</span></span>

   - <span data-ttu-id="b2cbe-153">**LicenseFilesPath** – インポートする必要があるライセンス ファイルを含むフォルダーのパス。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-153">**LicenseFilesPath** – The path of a folder that contains the license files that must be imported.</span></span> 
   - <span data-ttu-id="b2cbe-154">**SqlUser** – AOS を実行する credentials.json ファイルに指定されている同じユーザー。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-154">**SqlUser** – The same user who is specified in the credentials.json file to run the AOS.</span></span>
   - <span data-ttu-id="b2cbe-155">**SqlPassword** – SQL への接続に使用できるパスワード。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-155">**SqlPassword** – The password that can be used to connect to SQL.</span></span>
   - <span data-ttu-id="b2cbe-156">**EnvironmentConfigPath** - 環境のコンフィギュレーション ファイル。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-156">**EnvironmentConfigPath** – The configuration file for the environment.</span></span> <span data-ttu-id="b2cbe-157">このファイルの名前は、config.json で、wp \\&lt; 環境名 &gt;\\ StandaloneSetup という形式のフォルダー内のエージェント共有の下にあります。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-157">This file is named config.json and is located under the agent share in a folder that has the format wp\\&lt;environment-name&gt;\\StandaloneSetup.</span></span>

     <span data-ttu-id="b2cbe-158">コマンドを実行した後、ログ ファイルは、処理されるライセンス ファイルごとに生成されます。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-158">After the command is run, log files are generated for each license file that is processed.</span></span> <span data-ttu-id="b2cbe-159">ログ ファイルの名前は、{license\_file\_name}.output.log 形式と {license\_file\_name}.error.log 形式です。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-159">The names of the log files are in the format {license\_file\_name}.output.log and {license\_file\_name}.error.log.</span></span> <span data-ttu-id="b2cbe-160">データベース同期中に生成されるログは、dbsync.output.log および dbsync.error.log のような構造のファイルにあります。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-160">The logs that are generated during database synchronization are located in files that are structured like dbsync.output.log and dbsync.error.log.</span></span>

5. <span data-ttu-id="b2cbe-161">スクリプトが正常に実行されたとき、コンフィギュレーション キーがインポートされて有効になっていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-161">When the script has been run successfully, validate that the configuration key has been imported and enabled.</span></span> <span data-ttu-id="b2cbe-162">製品では、対応するコンフィギュレーション キーは、 **ライセンス コンフィギュレーション**  ページで使用可能になり、有効になります。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-162">In the product, the corresponding configuration key will be available and enabled on the **License configuration** page.</span></span> <span data-ttu-id="b2cbe-163">既定では、コンフィギュレーションが有効です。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-163">By default, the configuration is enabled.</span></span> <span data-ttu-id="b2cbe-164">たとえば、ISVConfigurationKey1 と呼ばれるコンフィギュレーション キーを追加した場合、コンフィギュレーション キーの一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-164">For example, if you added a configuration key that is named ISVConfigurationKey1, it will appear in the list of configuration keys.</span></span>

<span data-ttu-id="b2cbe-165">コンフィギュレーション キーが有効になると、ISV ソリューションの変更は製品に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2cbe-165">When the configuration key is enabled, the changes in the ISV solution will be visible in the product.</span></span>

---
title: オンプレミス環境での小売チャネルのコンポーネントのインストール手順
description: このトピックでは、オンプレミス環境での小売チャネルのコンポーネントのインストール手順について説明します。
author: jashanno
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 3d06e39c77b8f31afea857ccf033733d620304d7
ms.sourcegitcommit: d599bc1fc60a010c2753ca547219ae21456b1df9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2019
ms.locfileid: "1702712"
---
# <a name="installation-steps-for-retail-channel-components-in-an-on-premises-environment"></a><span data-ttu-id="6e0d3-103">オンプレミス環境での小売チャネルのコンポーネントのインストール手順</span><span class="sxs-lookup"><span data-stu-id="6e0d3-103">Installation steps for Retail channel components in an on-premises environment</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6e0d3-104">このトピックでは、オンプレミス環境での小売チャネルのコンポーネントのインストール手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-104">This topic covers the installation steps for Retail channel components in an on-premises environment.</span></span>

## <a name="overview"></a><span data-ttu-id="6e0d3-105">概要</span><span class="sxs-lookup"><span data-stu-id="6e0d3-105">Overview</span></span>

<span data-ttu-id="6e0d3-106">オンプレミス環境では、小売チャネル機能は Retail Store Scale Unit による使用のみ有効です。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-106">Retail channel functionality, in an on-premises environment, is enabled exclusively via use of Retail Store Scale Unit.</span></span> <span data-ttu-id="6e0d3-107">Retail Store Scale Unit の概要については、[Retail Store Scale Unit](../../retail/dev-itpro/retail-store-system-begin.md) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-107">For an overview of Retail Store Scale Unit, see [Retail Store Scale Unit](../../retail/dev-itpro/retail-store-system-begin.md).</span></span> 

<span data-ttu-id="6e0d3-108">クラウド展開とは異なり、オンプレミス環境では Lifecycle Services (LCS) 経由で小売チャネル コンポーネントのシームレスで可用性の高い展開は有効になりません。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-108">Unlike a cloud deployment, an on-premises environment does not enable seamless, high-availability deployment of Retail channel components via Lifecycle Services (LCS).</span></span> <span data-ttu-id="6e0d3-109">Retail Store Scale Unit をインストールすることによってのみ、小売チャネル コンポーネントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-109">The only way to use Retail channel components is by installing Retail Store Scale Unit.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6e0d3-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="6e0d3-110">Prerequisites</span></span> 

<span data-ttu-id="6e0d3-111">小売チャネル コンポーネントのインストールを開始する前に、まずオンプレミス環境のすべての事前インストール手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-111">Before you can start installation of Retail channel components, you must first complete all prior installation steps for an on-premises environment.</span></span> <span data-ttu-id="6e0d3-112">この手順は、[オンプレミス環境の設定と配置 (Platform update 12 以降)](setup-deploy-on-premises-pu12.md)で説明されています。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-112">These steps are listed in [Set up and deploy on-premises environments (Platform update 12 and later)](setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="6e0d3-113">さらに、Retail の全機能を使用するは、バージョン 8.1.1 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-113">In addition, version 8.1.1 must be installed in order for Retail have full functionality.</span></span> <span data-ttu-id="6e0d3-114">バージョン 8.1.2 に更新することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-114">We recommend that you update to version 8.1.2.</span></span>

> [!NOTE]
> <span data-ttu-id="6e0d3-115">誰もが自由にアクセスできない、セキュリティで保護されたネットワークを使用して、Retail Store Scale Unit (RSSU) を小売用バック オフィスに接続することが絶対に必要です。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-115">It is critical to ensure that a secure network, that is not publicly  accessible, is used to connect Retail Store Scale Unit (RSSU) to Retail headquarters.</span></span> <span data-ttu-id="6e0d3-116">さらに、小売用バックオフィスへのネットワーク アクセスを、ネットワーク フィルタリングやその他の方法を介した既知の RSSU デバイスのみに許可されるように制限してください。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-116">You must also restrict network access to Retail headquarters, so access is only allowed to known RSSU devices via network filtering or other means.</span></span> <span data-ttu-id="6e0d3-117">つまり、ファイアウォールが存在する必要があります。ホワイトリストへの追加を強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-117">This means that a firewall must exist and whitelisting is highly recommended.</span></span>

## <a name="installation-steps"></a><span data-ttu-id="6e0d3-118">インストール手順</span><span class="sxs-lookup"><span data-stu-id="6e0d3-118">Installation steps</span></span>

1.  <span data-ttu-id="6e0d3-119">以前に作成した [アプリケーションの共有](setup-deploy-on-premises-pu12.md#setupfile) ( **LocalAgent** 共有フォルダではありません) にて、共有を行う場所のルートディレクトリに **selfservicepackages** という名称のフォルダを作成します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-119">On the previously created [Application share](setup-deploy-on-premises-pu12.md#setupfile), (not the **LocalAgent** share folder), create a new folder called **selfservicepackages** in the root directory of the share location.</span></span>  
2.  <span data-ttu-id="6e0d3-120">各 AOS コンピューターで、簡単にアクセスできるディレクトリを作成します (**C:/selfservicepackages** など)。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-120">On each AOS computer, create an easily accessible directory, such as **C:/selfservicepackages**.</span></span>
3.  <span data-ttu-id="6e0d3-121">いづれかのAOSコンピュータ (どれでも構いません) 上で、次のPowerShellスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-121">On one AOS computer (which one does not matter), run the following PowerShell script.</span></span>

    ```powershell
    .\RetailUpdateDatabase.ps1 -envName '<Environment name>' -AosUrl 'https://<My Environment Name>.com/namespaces/AXSF/’ -       SendProductSupportTelemetryToMicrosoft
    ```
  > [!IMPORTANT]
  > <span data-ttu-id="6e0d3-122">上記の手順は、バージョン10.0以降にて有効です。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-122">The above steps apply to version 10.0 and later.</span></span>  <span data-ttu-id="6e0d3-123">Retail オンプレミス機能のオリジナル 8.1.3 版では、オリジナルバージョンのスクリプト区切り文字を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-123">For the original 8.1.3 release of Retail on-premises functionality, the original version of the script delimiters must be used.</span></span>
  
  > ```powershell
  > .\RetailUpdateDatabase.ps1 -DatabaseServer '<Database server name for AOS database>' -DatabaseName '<Database name for AOS database>' -envName '<Environment name>' -RetailSelfServicePackages '<Local path of Retail self-service packages, such as **C:/selfservicepackages**>’ -SendProductSupportTelemetryToMicrosoft
  > ```
  > - <span data-ttu-id="6e0d3-124">パラメーター **- envName** は、環境が生成されるときに作成時に既知である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-124">The parameter **-envName** should be known based on creation when the environment is generated.</span></span>
  > - <span data-ttu-id="6e0d3-125">従来のパラメータ **-DatabaseServer** および **-DatabaseName** が環境設定に基づいて認識される必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-125">The legacy parameters **-DatabaseServer** and **-DatabaseName** should be known based on the environment setup.</span></span>
  > - <span data-ttu-id="6e0d3-126">パラメーター **-SendProductSupportTelemetryToMicrosoft** は、Microsoft へのテレメトリを有効にするための必須の値です。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-126">The parameter **-SendProductSupportTelemetryToMicrosoft** is a required value to enable telemetry to Microsoft.</span></span>  <span data-ttu-id="6e0d3-127">これは、Microsoft によるサポートを最大限に受けるために不可欠です。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-127">This is critical to maximize support from Microsoft.</span></span>
  > - <span data-ttu-id="6e0d3-128">このスクリプトはと、Retail サービスのユーザーとロールの更新や、Retail レジストリ キーの更新を含むさまざまなアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-128">This script will perform a variety of actions, including updating the Retail Service user and role and updating Retail registry keys.</span></span>

4. <span data-ttu-id="6e0d3-129">それぞれのAOS コンピューターで、次の PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-129">On each AOS computer, run the following PowerShell script.</span></span>

  ```powershell
  .\RetailUpdateDatabase.ps1 -RetailSelfServicePackages 'C:\RetailSelfService\Packages'
  ```

  > [!NOTE]
  > <span data-ttu-id="6e0d3-130">パラメーター **-RetailSelfServicePackages** は、この手順の最初で作成したフル パスの場所です (**C:/selfservicepackages**)。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-130">The parameter **-RetailSelfServicePackages** is the full path location created in the beginning of this step (**C:/selfservicepackages**).</span></span>

5.  <span data-ttu-id="6e0d3-131">Retailインストーラーを使用するには、LCSから適切なバイナリ更新をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-131">Download the appropriate binary update from LCS to have the Retail installers.</span></span> <span data-ttu-id="6e0d3-132">手順については、[Lifecycle Services (LCS) から更新プログラムを入手](../migration-upgrade/download-hotfix-lcs.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-132">For instructions, see [Get updates from Lifecycle Services (LCS)](../migration-upgrade/download-hotfix-lcs.md).</span></span>
6.  <span data-ttu-id="6e0d3-133">ZIP ファイルを展開し、すべてのセルフ サービス インストーラーを、手順 2 において各 AOS コンピューターで定義および作成された **C:/selfservicepackages** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-133">Extract the zip file and copy all self-service installers into the folder **C:/selfservicepackages** defined and created in step 2 in each of the AOS machines.</span></span> <span data-ttu-id="6e0d3-134">6 つのセルフ サービス インストーラーは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-134">The six self-service installers include:</span></span> 
    - <span data-ttu-id="6e0d3-135">AsyncServerConnectorServiceSetup.exe</span><span class="sxs-lookup"><span data-stu-id="6e0d3-135">AsyncServerConnectorServiceSetup.exe</span></span>
    - <span data-ttu-id="6e0d3-136">RealtimeServiceAX63Setup.exe</span><span class="sxs-lookup"><span data-stu-id="6e0d3-136">RealtimeServiceAX63Setup.exe</span></span>
    - <span data-ttu-id="6e0d3-137">HardwareStationSetup.exe</span><span class="sxs-lookup"><span data-stu-id="6e0d3-137">HardwareStationSetup.exe</span></span>
    - <span data-ttu-id="6e0d3-138">ModernPosSetup.exe</span><span class="sxs-lookup"><span data-stu-id="6e0d3-138">ModernPosSetup.exe</span></span>
    - <span data-ttu-id="6e0d3-139">ModernPosSetupOffline.exe</span><span class="sxs-lookup"><span data-stu-id="6e0d3-139">ModernPosSetupOffline.exe</span></span>
    - <span data-ttu-id="6e0d3-140">StoreSystemSetup.exe</span><span class="sxs-lookup"><span data-stu-id="6e0d3-140">StoreSystemSetup.exe</span></span>
7.  <span data-ttu-id="6e0d3-141">ADFS コンピューターに移動し、InfrastructureScripts フォルダに移動してください。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-141">Navigate to the AD FS machine, then go to the InfrastructureScripts folder.</span></span> <span data-ttu-id="6e0d3-142">これは、以前に実行した Retail PowerShell スクリプトがあったのと同じファイル ディレクトリです (**RetailUpdateDatabase.ps1**)。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-142">This is the same file directory where the previously run Retail PowerShell script was located (**RetailUpdateDatabase.ps1**).</span></span> <span data-ttu-id="6e0d3-143">PowerShell スクリプト **Create-ADFSServerApplicationForRetail.ps1** を見つけます。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-143">Find the PowerShell script **Create-ADFSServerApplicationForRetail.ps1**.</span></span>
8.  <span data-ttu-id="6e0d3-144">ご利用の ADFS コンピューターで、新規 PowerShell ウィンドウから **.\Create-ADFSServerApplicationForRetail -HostUrl 'https://ax.d365ffo.onprem.contoso.com'** コマンドを使用してこのスクリプトを実行します。 **HostUrl** の値は Service Fabric にて確認することができます。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-144">On the AD FS machine that you're currently using, run this script in a new PowerShell window using the command **.\Create-ADFSServerApplicationForRetail -HostUrl 'https://ax.d365ffo.onprem.contoso.com'**, where the **HostUrl** value can be found in Service Fabric.</span></span>  <span data-ttu-id="6e0d3-145">**HostUrl** 値を見つけるには、 **Service Fabric** &gt; **アプリケーション ファブリック:/AXSF** &gt; **詳細** &gt; **Aad_AADValidAudience** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-145">To find the **HostUrl** value, go to **Service Fabric** &gt; **Application fabric:/AXSF** &gt; **Details** &gt; **Aad_AADValidAudience**.</span></span>
9.  <span data-ttu-id="6e0d3-146">AD FS 管理の **アプリケーション グループ** から新しく生成されたサーバー アプリケーションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-146">Access the newly generated Server application from the **Application Groups** in AD FS Management.</span></span>
10.  <span data-ttu-id="6e0d3-147">新しく生成されたサーバー アプリケーションを編集し、**シークレットをリセット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-147">Edit the newly generated Server application and select **Reset the Secret**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="6e0d3-148">これは、各 Retail Store Scale Unit でこのスクリプトを実行する重要なセキュリティ手法です。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-148">It is an important security measure to run this script for each Retail Store Scale Unit.</span></span>  <span data-ttu-id="6e0d3-149">これにより、セキュリティが最大化され、セキュリティ侵害が発生した場合のワークロードが最小化されます。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-149">This maximizes security and minimizes the workload in case of a security breach.</span></span> 
  >
  > <span data-ttu-id="6e0d3-150">このシークレットを安全に保つことが重要です。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-150">It is critical to keep this secret safe.</span></span> <span data-ttu-id="6e0d3-151">このシークレットは、1 回だけコピーしてください。システムに保存しないでください。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-151">This secret should only be copied once and never stored on the system.</span></span>  <span data-ttu-id="6e0d3-152">生成されたクライアント ID とシークレットは、Retail Store Scale Unit インストーラーの実行中に使用されるため、後で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-152">The Client ID and Secret generated will be used during the Retail Store Scale Unit installer, so it is required to be used at a later time.</span></span>  <span data-ttu-id="6e0d3-153">シークレットはいつでも再度リセットできますが、前のシークレットを使用した Retail Store Scale Unit で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-153">You can always reset the secret again, but it must then be updated on any Retail Store Scale Unit that used the previous secret.</span></span>

11.  <span data-ttu-id="6e0d3-154">**小売用**&gt;**バックオフィスの設定**&gt;**小売用スケジューラ**&gt;**Microsoft Dynamics AX のコネクタ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-154">Go to **Retail** &gt; **Headquarters setup** &gt; **Retail scheduler** &gt; **Connector for Microsoft Dynamics AX**.</span></span>
12.  <span data-ttu-id="6e0d3-155">アクション ウィンドウで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-155">Select **Edit** on the Action pane.</span></span>
13.  <span data-ttu-id="6e0d3-156">**プロファイル** フィールドに、**既定**値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-156">In the **Profile** field, enter the value **Default**.</span></span>  <span data-ttu-id="6e0d3-157">必要に応じて、**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-157">If needed, enter a description in the **Description** field.</span></span>

  > [!NOTE]
  > <span data-ttu-id="6e0d3-158">手順 12 ～ 14 の以下のフィールドには既に値が入っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-158">It is possible for the following fields in steps 12 through 14 to already have values.</span></span> <span data-ttu-id="6e0d3-159">これが発生した場合、この一連の手順を省略し、そこから続行します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-159">If this occurs, skip those steps and continue from there.</span></span> <span data-ttu-id="6e0d3-160">選択可能なプロファイル タイトル (この場合は既定値) があることが重要です。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-160">What is important is to have a selectable profile title (default in this case).</span></span>

14.  <span data-ttu-id="6e0d3-161"> **Web アプリケーション名** フィールドに、**RetailCDXRealTimeService** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-161">In the  **Web application name** field, enter **RetailCDXRealTimeService**.</span></span>
15.  <span data-ttu-id="6e0d3-162">**プロトコル** フィールドで、**https** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-162">In the **Protocol** field, select **https**.</span></span>
16.  <span data-ttu-id="6e0d3-163">**通称**フィールドに、**AXServiceUser@contoso.com** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-163">In the **Common name** field, enter **AXServiceUser@contoso.com**.</span></span>
17.  <span data-ttu-id="6e0d3-164">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-164">Select **Save** on the Action Pane.</span></span>
18.  <span data-ttu-id="6e0d3-165">小売用バックオフィスで、**Retail** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売共有パラメーター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-165">In Retail headquarters, go to **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail shared parameters**.</span></span>
19.  <span data-ttu-id="6e0d3-166">**セキュリティ** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-166">Select the **Security** tab.</span></span>
20.  <span data-ttu-id="6e0d3-167">**取引サービスの従来のプロパティ** の下位ヘッダーにて、 **Real-time サービス プロファイル** フィールドを選択し、新たに作成した **既定** 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-167">Under the sub-heading **Transaction service legacy properties**, select the **Real-time Service profile** field, and then select the newly created **Default** value.</span></span>
21.  <span data-ttu-id="6e0d3-168">**ID プロバイダー** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-168">Select the **Identity providers** tab.</span></span>
22.  <span data-ttu-id="6e0d3-169">**ID プロバイダー**クイック タブで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-169">On the **Identity providers** FastTab, select **Add**.</span></span>
23.  <span data-ttu-id="6e0d3-170">新しい **発行者** 行で、新しい ID プロバイダー値 **https://sts.windows.net/** をフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-170">In the new **Issuer** row, enter the new Identity provider value **https://sts.windows.net/** in the field.</span></span>
24.  <span data-ttu-id="6e0d3-171">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-171">Select **Save** on the Action Pane.</span></span>
25.  <span data-ttu-id="6e0d3-172">**小売** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売パラメーター**の順にを移動します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-172">Go to **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
26.  <span data-ttu-id="6e0d3-173">**全般** タブで、**初期化** リンクを選択し、Retail 機能のシード データを構成します。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-173">On the **General** tab, select the **Initialize** link to configure seed data for Retail functionality.</span></span>

  > [!NOTE]
  > <span data-ttu-id="6e0d3-174">初めてダウンロードが試みられるとき、インストーラーは関連するページからダウンロードされません。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-174">The installers will not download from their relevant pages the first time a download is attempted.</span></span>  <span data-ttu-id="6e0d3-175">これは、インストーラーはダウンロードの場所に配置されているだけであり、関連付けられているデータベースの値がまだ存在しないためです。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-175">This is because the installers have only just been placed into the download location and the associated database values do not yet exist.</span></span>  <span data-ttu-id="6e0d3-176">バックオフィスで、**ダウンロード**機能が試行されると (たとえば、Retail Store Scale Unit または Retail Modern POS)、エラーが表示され、2 回目にダウンロードが試みられたときにインストーラーをダウンロードできるようにする自動アップロード機能が開始されます。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-176">In headquarters, when the **Download** functionality is attempted (for example, Retail Store Scale Unit or Retail Modern POS), an error will display and then an automated upload functionality will be initiated to allow the installers to be downloaded the second time that the download is attempted.</span></span> <span data-ttu-id="6e0d3-177">(インストーラーのダウンロードがもう一度試みられるまで 1 分待ってください)。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-177">(Wait one minute before attempting to download the installer again).</span></span>

  > <span data-ttu-id="6e0d3-178">周辺機器シミュレータ (本社の ハードウェアプロファイル ページにてダウンロードできます) は、最低でも1つのハードウェア プロファイルが作成され、動作可能となるまで使用することができません。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-178">The Peripheral Simulator (downloaded on the Hardware profile page in headquarters) will not be available until at least one Hardware profile has been created and is functional.</span></span> <span data-ttu-id="6e0d3-179">それらが完了していれば、以下のスクリプトを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-179">After that point has been achieved, the following script can be run.</span></span>
  
  > ```powershell
  > .\RetailUpdateDatabase.ps1 -envName 'LBDenv1' -UpdateRetailHardwareProfileSelfServicePackage
  > ```

28. <span data-ttu-id="6e0d3-180">Retail Store Scale Unit のインストールのためのインストール手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-180">Follow the installation steps for installing the Retail Store Scale Unit.</span></span> <span data-ttu-id="6e0d3-181">手順については、[Retail Store Scale Unit のコンフィギュレーションとインストール](../../retail/dev-itpro/retail-store-scale-unit-configuration-installation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-181">For instructions, see [Configure and install Retail Store Scale Unit](../../retail/dev-itpro/retail-store-scale-unit-configuration-installation.md).</span></span>  <span data-ttu-id="6e0d3-182">このドキュメントの複数の場所に、オンプレミス配置の指示に対する変更を参照するメモがあります。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-182">At multiple locations in this document there will be notes referencing changes to the instructions for an on-premises deployment.</span></span> <span data-ttu-id="6e0d3-183">これらの変更を記録することが重要です。</span><span class="sxs-lookup"><span data-stu-id="6e0d3-183">It is important to note each of these changes.</span></span> 

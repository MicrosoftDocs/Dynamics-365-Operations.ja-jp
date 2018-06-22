---
title: "エンタープライズ ポータル サーバーの 1 つのサーバー ファームへの結合 (AX 2012)"
description: "この記事では、エンタープライズ ポータル サーバー (Microsoft Dynamics AX 2012 用) を単一のサーバー ファームに参加させる方法について説明します。"
author: aneesmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: IT Pro
ms.reviewer: robinr
ms.search.scope: AX 2012
ms.custom: 27431
ms.assetid: 05316e9d-818e-4f4b-901c-2e67fe8edfd1
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0173a36b47035d0025d44e3afce22c7e394c33b9
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="join-enterprise-portal-servers-into-a-single-server-farm-ax-2012"></a><span data-ttu-id="70614-103">エンタープライズ ポータル サーバーの 1 つのサーバー ファームへの結合 (AX 2012)</span><span class="sxs-lookup"><span data-stu-id="70614-103">Join Enterprise Portal servers into a single server farm (AX 2012)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="70614-104">この記事では、エンタープライズ ポータル サーバー (Microsoft Dynamics AX 2012 用) を単一のサーバー ファームに参加させる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="70614-104">This article explains how to join Enterprise Portal servers (for Microsoft Dynamics AX 2012) into a single server farm.</span></span> 

<span data-ttu-id="70614-105">Microsoft Dynamics Lifecycle Services (LCS) でエンタープライズ ポータル (EP) サーバーが配置されると、各サーバーは独自のサーバー ファームに配置されます。</span><span class="sxs-lookup"><span data-stu-id="70614-105">When Microsoft Dynamics Lifecycle Services (LCS) deploys Enterprise Portal (EP) servers, each EP server is deployed into its own server farm.</span></span> <span data-ttu-id="70614-106">この記事のステップでは、すべての EP サーバーを単一のサーバー ファームに参加させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="70614-106">The steps in this article show how to join all EP servers into a single server farm.</span></span> <span data-ttu-id="70614-107">基本概念は、1 台の EP サーバー上にサーバー ファームを保持し、その他のすべての EP サーバーをそのファームに結合することです。</span><span class="sxs-lookup"><span data-stu-id="70614-107">The basic idea is to keep the server farm on one EP server and join all the other EP servers to that farm.</span></span> <span data-ttu-id="70614-108">この記事の情報は、次の前提条件に基づいています。</span><span class="sxs-lookup"><span data-stu-id="70614-108">The information in this article is based on the following assumptions:</span></span>

-   <span data-ttu-id="70614-109">*N* EP サーバーは、LCS によってが配置され、これらのサーバーは、EP-01、EP 02、EP-03...EP 0*N*とラベル付けされています。</span><span class="sxs-lookup"><span data-stu-id="70614-109">*N* EP servers are deployed by LCS, and these servers are labeled EP-01, EP-02, EP-03...EP-0*N*.</span></span>
-   <span data-ttu-id="70614-110">ロード バランサを AzureILB01 と呼びます。</span><span class="sxs-lookup"><span data-stu-id="70614-110">The load balancer is named AzureILB01.</span></span>
-   <span data-ttu-id="70614-111">EP-01 を単一のサーバー ファームとして使用し、その他のすべての EP サーバーはそのファームに参加します。</span><span class="sxs-lookup"><span data-stu-id="70614-111">You're using EP-01 as the single server farm, and all the other EP servers will join that farm.</span></span>

## <a name="overview"></a><span data-ttu-id="70614-112">概要</span><span class="sxs-lookup"><span data-stu-id="70614-112">Overview</span></span>
<span data-ttu-id="70614-113">次の図は、EP サーバーを単一のサーバー ファームに参加させるプロセスを示しています。</span><span class="sxs-lookup"><span data-stu-id="70614-113">The following image shows the process for joining EP servers into a single server farm.</span></span> <span data-ttu-id="70614-114">[![ProcessFlow\_ConfigureEPServersInFarm](./media/processflow_configureepserversinfarm.png)](./media/processflow_configureepserversinfarm.png)</span><span class="sxs-lookup"><span data-stu-id="70614-114">[![ProcessFlow\_ConfigureEPServersInFarm](./media/processflow_configureepserversinfarm.png)](./media/processflow_configureepserversinfarm.png)</span></span>

## <a name="put-ep-servers-into-a-single-server-farm"></a><span data-ttu-id="70614-115">1 台のサーバー ファームに EP サーバーを配置</span><span class="sxs-lookup"><span data-stu-id="70614-115">Put EP servers into a single server farm</span></span>
1.  <span data-ttu-id="70614-116">Dynamics インストーラー ユーザー サービス アカウントを使用して EP-01 にログオンします。</span><span class="sxs-lookup"><span data-stu-id="70614-116">Log on to EP-01 by using the Dynamics Installer User service account.</span></span>
2.  <span data-ttu-id="70614-117">Microsoft SharePoint 2013 サーバーの管理を起動します。</span><span class="sxs-lookup"><span data-stu-id="70614-117">Start Microsoft SharePoint 2013 Central Administration.</span></span>
3.  <span data-ttu-id="70614-118">**システム設定** &gt; **代替アクセス マッピングのコンフィギュレーション**に移動します。</span><span class="sxs-lookup"><span data-stu-id="70614-118">Go to **System settings** &gt; **Configure alternate access mappings**.</span></span>
4.  <span data-ttu-id="70614-119">**内部 URL を追加する**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70614-119">Click **Add Internal URLs**.</span></span> <span data-ttu-id="70614-120">次のスクリーン ショットは、EP サイトが作成されたポートである、ポート 81 に EP-02 のマッピングを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="70614-120">The following screen shot shows how to add a mapping for EP-02 on port 81, which is the port that the EP site is created on.</span></span> <span data-ttu-id="70614-121">LCS によって展開されているすべての EP サーバーでこの手順を繰り返します。[![AddInternalURLs](./media/addinternalurls.png)](./media/addinternalurls.png)</span><span class="sxs-lookup"><span data-stu-id="70614-121">Repeat this step for every EP server that is deployed by LCS.[![AddInternalURLs](./media/addinternalurls.png)](./media/addinternalurls.png)</span></span>
5.  <span data-ttu-id="70614-122">**公開 URL の編集**をクリックし、適切な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70614-122">Click **Edit Public URLs**, and enter appropriate values:</span></span>
    -   <span data-ttu-id="70614-123">**既定:** ロード バランサ URL + ポート 81 を使用します。</span><span class="sxs-lookup"><span data-stu-id="70614-123">**Default:** Use the load balancer URL + port 81.</span></span>
    -   <span data-ttu-id="70614-124">**イントラネット:** EP-01 (SharePoint サーバー ファームの仮想マシン) とポート 81 を使用します。</span><span class="sxs-lookup"><span data-stu-id="70614-124">**Intranet:** Use EP-01 (the SharePoint server farm virtual machine) + port 81.</span></span>
    -   <span data-ttu-id="70614-125">**インターネット:** 公的に登録された URL と ポート 81 を使用します。</span><span class="sxs-lookup"><span data-stu-id="70614-125">**Internet:** Use the publicly registered URL + port 81.</span></span>

    <span data-ttu-id="70614-126">[![EditPublicZoneURLs](./media/editpubliczoneurls.png)](./media/editpubliczoneurls.png)</span><span class="sxs-lookup"><span data-stu-id="70614-126">[![EditPublicZoneURLs](./media/editpubliczoneurls.png)](./media/editpubliczoneurls.png)</span></span>
6.  <span data-ttu-id="70614-127">レジストリ エディター (regedit) を開き、次のレジストリ キーを作成します。</span><span class="sxs-lookup"><span data-stu-id="70614-127">Open Registry Editor (regedit), and create the following registry key:</span></span>
    -   <span data-ttu-id="70614-128">**パス:** HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Contro\\Lsa\\MSV1\_0</span><span class="sxs-lookup"><span data-stu-id="70614-128">**Path:** HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Contro\\Lsa\\MSV1\_0</span></span>
    -   <span data-ttu-id="70614-129">**キーの詳細、キー値:** ロード バランサー名と完全修飾名</span><span class="sxs-lookup"><span data-stu-id="70614-129">**Key details, key value:** The load balancer name and the fully qualified name</span></span>

    <span data-ttu-id="70614-130">[![EditMultiString](./media/editmultistring.png)](./media/editmultistring.png)</span><span class="sxs-lookup"><span data-stu-id="70614-130">[![EditMultiString](./media/editmultistring.png)](./media/editmultistring.png)</span></span>
7.  <span data-ttu-id="70614-131">**コマンド プロンプト** ウィンドウを開き、**ipconfig** コマンドを実行してローカル コンピューターの IP アドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="70614-131">Open a **Command Prompt** window, and get the IP address of the local machine by running the **ipconfig** command.</span></span>
8.  <span data-ttu-id="70614-132">メモ帳で C:\\Windows\\System32\\drivers\\etc\\hosts ファイルを開き、ロード バランサー名をローカル コンピューターの IP アドレスにマップします。</span><span class="sxs-lookup"><span data-stu-id="70614-132">In Notepad, open the C:\\Windows\\System32\\drivers\\etc\\hosts file, and map the load balancer name to the local machine IP address.</span></span> <span data-ttu-id="70614-133">このマッピングは、ローカル EP サーバーが動作していることをテストするために使用されます。[![NotePad](./media/notepad.png)](./media/notepad.png)。</span><span class="sxs-lookup"><span data-stu-id="70614-133">This mapping is used to test that the local EP server is working.[![NotePad](./media/notepad.png)](./media/notepad.png)</span></span>
9.  <span data-ttu-id="70614-134">LCS によって展開されているすべての EP サーバー上で手順 6 ～ 8 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="70614-134">Repeat steps 6 through 8 on every EP server that is deployed by LCS.</span></span>
10. <span data-ttu-id="70614-135">Dynamics インストーラー ユーザー サービス アカウントを使用して EP-02 サーバーにログオンします。</span><span class="sxs-lookup"><span data-stu-id="70614-135">Log on to the EP-02 server by using the Dynamics Installer User service account.</span></span>
11. <span data-ttu-id="70614-136">Dynamics インストーラが格納されているドライブに移動します (このドライブはたいていドライブ F です)。</span><span class="sxs-lookup"><span data-stu-id="70614-136">Go to the drive where the Dynamics installer is stored (this drive is most likely drive F).</span></span> <span data-ttu-id="70614-137">**セットアップ** を右クリックし、**管理者として実行** をクリックして以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="70614-137">Right-click **Setup**, click **Run as administrator**, and then follow these steps:</span></span>
    1.  <span data-ttu-id="70614-138">**Microsoft Dynamics AX コンポーネントのインストール**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70614-138">Click **Install Microsoft Dynamics AX components**.</span></span>
    2.  <span data-ttu-id="70614-139">**ようこそ**ページで、**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70614-139">On the **Welcome** page, click **Next**.</span></span>
    3.  <span data-ttu-id="70614-140">**コンポーネントの追加または変更**をクリックし、次に**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70614-140">Click **Add or modify components**, and then click **Next**.</span></span>
    4.  <span data-ttu-id="70614-141">**Webサーバー コンポーネント** で、**エンタープライズ ポータル** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="70614-141">Under **Web server components**, select the **Enterprise Portal** check box.</span></span> <span data-ttu-id="70614-142">**OK** をクリックして EP をインストールすることを同意し、**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70614-142">Click **OK** to acknowledge that you want to install EP, and then click **Next**.</span></span>
    5.  <span data-ttu-id="70614-143">検証エラーがないことを確認し、**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70614-143">Make sure that there are no validation errors, and then click **Next**.</span></span>
    6.  <span data-ttu-id="70614-144">BC プロキシ ユーザーのパスワードを入力し、**次**を入力します。</span><span class="sxs-lookup"><span data-stu-id="70614-144">Enter the BC proxy user password, and then click **Next**.</span></span>
    7.  <span data-ttu-id="70614-145">**エンタープライズ ポータル用の Web サイトの構成**ページで、Web アプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="70614-145">On the **Configure a Web site for Enterprise Portal **page, select the web application.</span></span>
    8.  <span data-ttu-id="70614-146">**Windows SharePoint Services を構成する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="70614-146">Select the **Configure for Windows SharePoint Services** check box.</span></span>
    9.  <span data-ttu-id="70614-147">**インストールの完了後に IIS を再起動** チェック ボックスをオンにし、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70614-147">Select the **Restart IIS after installation is completed** check box, and then click **Next**.</span></span>

    <span data-ttu-id="70614-148">[![EP 用の Web サイトの構成](./media/configure-a-web-site-for-ep.png)](./media/configure-a-web-site-for-ep.png)</span><span class="sxs-lookup"><span data-stu-id="70614-148">[![Configure a Web site for EP](./media/configure-a-web-site-for-ep.png)](./media/configure-a-web-site-for-ep.png)</span></span>
12. <span data-ttu-id="70614-149">インストールが完了するまで**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70614-149">Click **Next** until the installation is completed.</span></span>
13. <span data-ttu-id="70614-150">サーバー EP-03 から EP-0*N* で手順 10 ～ 12 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="70614-150">Repeat steps 10 through 12 on servers EP-03 through EP-0*N*.</span></span> <span data-ttu-id="70614-151">(ファームがコンフィギュレーションされている単一のサーバーを除くすべての EP サーバーに EP を再インストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="70614-151">(You must re-install EP on every EP server, except the single server where the farm is configured.</span></span> <span data-ttu-id="70614-152">ここでは、このサーバーは EP-01 です。)</span><span class="sxs-lookup"><span data-stu-id="70614-152">In our example, this server is EP-01.)</span></span>
14. <span data-ttu-id="70614-153">各 EP サーバー、EP-01 ～ EP-0*N* でこれらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="70614-153">Follow these steps on every EP server, EP-01 through EP-0*N*:</span></span>
    1.  <span data-ttu-id="70614-154">インターネット インフォメーション サービス (IIS) の管理コンソール (inetmgr) を開きます。</span><span class="sxs-lookup"><span data-stu-id="70614-154">Open the Internet Information Services (IIS) administration console (inetmgr).</span></span>
    2.  <span data-ttu-id="70614-155">**サイト** &gt; **SharePoint – 81** に移動します。</span><span class="sxs-lookup"><span data-stu-id="70614-155">Go to **Sites** &gt; **SharePoint – 81**.</span></span>
    3.  <span data-ttu-id="70614-156">右クリックして **バインドの編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70614-156">Right-click, and then click **Edit bindings**.</span></span>
    4.  <span data-ttu-id="70614-157">バインディングをダブルクリックして、**Edit Site Binding** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="70614-157">Double-click the binding to open the **Edit Site Binding** dialog box.</span></span>
    5.   <span data-ttu-id="70614-158">**ホスト名**フィールドに、ロード バランサー名を入力します。</span><span class="sxs-lookup"><span data-stu-id="70614-158">In the **Host name** field, enter the load balancer name.</span></span>

    <span data-ttu-id="70614-159">[![編集サイト バインディング](./media/edit-site-binding.png)](./media/edit-site-binding.png)</span><span class="sxs-lookup"><span data-stu-id="70614-159">[![Edit Site Binding](./media/edit-site-binding.png)](./media/edit-site-binding.png)</span></span>
15. <span data-ttu-id="70614-160">各 EP サーバーで、これらの検証手順に従います。</span><span class="sxs-lookup"><span data-stu-id="70614-160">Follow these validation steps on every EP server:</span></span>
    1.  <span data-ttu-id="70614-161">**コマンド プロンプト** ウィンドウで、**iisreset** コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="70614-161">In a **Command Prompt** window, run the **iisreset** command.</span></span>
    2.  <span data-ttu-id="70614-162">Internet Explorer を起動し、**http://AzureILB01:81/sites/DynamicsAx** に移動します。</span><span class="sxs-lookup"><span data-stu-id="70614-162">Start Internet Explorer, and go to **http://AzureILB01:81/sites/DynamicsAx**.</span></span>
    3.  <span data-ttu-id="70614-163">ロール センター ページがエラーなく表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="70614-163">Make sure that the Role Center page is rendered without error.</span></span>

## <a name="configure-appfabric-cache"></a><span data-ttu-id="70614-164">AppFabric キャッシュのコンフィギュレーション。</span><span class="sxs-lookup"><span data-stu-id="70614-164">Configure AppFabric cache</span></span>
1.  <span data-ttu-id="70614-165">Dynamics インストール ユーザー サービス アカウントを使用して EP-01 サーバーにログオンします。</span><span class="sxs-lookup"><span data-stu-id="70614-165">Log on to the EP-01 server by using the Dynamics Install User service account.</span></span>
2.  <span data-ttu-id="70614-166">Microsoft Windows PowerShell **コマンド プロンプト** ウィンドウを管理者として開きます。</span><span class="sxs-lookup"><span data-stu-id="70614-166">Open a Microsoft Windows PowerShell **Command Prompt** window as an administrator.</span></span>
3.  <span data-ttu-id="70614-167">**Use-CacheCluster** コマンドを実行し、Windows PowerShell セッションのコンテキストを特定のキャッシュ クラスターに設定します。</span><span class="sxs-lookup"><span data-stu-id="70614-167">Run the **Use-CacheCluster** command to set the context of your Windows PowerShell session to a specific cache cluster.</span></span>
4.  <span data-ttu-id="70614-168">**New-Cache** コマンドを実行して新しい名前のキャッシュを作成します。</span><span class="sxs-lookup"><span data-stu-id="70614-168">Run the **New-Cache** command to create a new named cache.</span></span> <span data-ttu-id="70614-169">指定する名前をメモします。</span><span class="sxs-lookup"><span data-stu-id="70614-169">Make a note of the name that you specify.</span></span> <span data-ttu-id="70614-170">(このキャッシュ名は、次の手順で入力します。)</span><span class="sxs-lookup"><span data-stu-id="70614-170">(You'll enter this cache name in the next procedure.)</span></span>
5.  <span data-ttu-id="70614-171">**Grant-CacheAllowedClientAccount** コマンドを実行し、.NET Business Connector プロキシを指定します。</span><span class="sxs-lookup"><span data-stu-id="70614-171">Run the **Grant-CacheAllowedClientAccount** command, and specify the .NET Business Connector proxy.</span></span> <span data-ttu-id="70614-172">(これは、EP アプリケーション プールで使用される口座です。)</span><span class="sxs-lookup"><span data-stu-id="70614-172">(This is the account that is used by the EP application pool).</span></span>
6.  <span data-ttu-id="70614-173">次のコマンドを実行します: **Set-CacheConfig -Secondaries 1**</span><span class="sxs-lookup"><span data-stu-id="70614-173">Run the following command: **Set-CacheConfig -Secondaries 1**</span></span>
    1.  <span data-ttu-id="70614-174">キャッシュ名の入力を要求するメッセージが表示されたら、ステップ 4 から名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="70614-174">When you're prompted for the cache name, enter the name from step 4.</span></span>
    2.  <span data-ttu-id="70614-175">続行するかどうかを問われたときは、**Y** を入力します。</span><span class="sxs-lookup"><span data-stu-id="70614-175">When you're asked whether you want to continue, enter **Y**.</span></span>

7.  <span data-ttu-id="70614-176">手順 6 では、エラーが発生する場合は、次の順序でコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="70614-176">If step 6 causes an error, try to run the commands in the following order:</span></span>
    1.  <span data-ttu-id="70614-177">stop-cachecluster</span><span class="sxs-lookup"><span data-stu-id="70614-177">stop-cachecluster</span></span>
    2.  <span data-ttu-id="70614-178">Set-CacheConfig -Secondaries 1</span><span class="sxs-lookup"><span data-stu-id="70614-178">Set-CacheConfig -Secondaries 1</span></span>

8.  <span data-ttu-id="70614-179">**Export-CacheClusterConfig** コマンドを実行してコンフィギュレーションをエキスポートします。</span><span class="sxs-lookup"><span data-stu-id="70614-179">Export the configuration by running the **Export-CacheClusterConfig** command.</span></span> <span data-ttu-id="70614-180">ファイルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="70614-180">Specify a name for the file.</span></span> <span data-ttu-id="70614-181">このファイルは、ローカル コンピューターの任意の場所に保存できます。</span><span class="sxs-lookup"><span data-stu-id="70614-181">This file can be saved anywhere on the local computer.</span></span>
9.  <span data-ttu-id="70614-182">先ほど作成したファイルを開き、**&lt;advancedProperties&gt;** セクションに次のコンフィギュレーションを追加します。</span><span class="sxs-lookup"><span data-stu-id="70614-182">Open the file that you just created, and add the following configuration to the **&lt;advancedProperties&gt;** section.</span></span>

        <transportProperties maxBufferSize="1000000000" />

10. <span data-ttu-id="70614-183">**Import-CacheClusterConfig c:\\newConfig.xml** のコマンドを実行して、コンフィギュレーションをインポートします。続行するか確認された場合、**Y** を入力します。</span><span class="sxs-lookup"><span data-stu-id="70614-183">Import the configuration by running the following command: **Import-CacheClusterConfig c:\\newConfig.xml** When you're asked whether you want to continue, enter **Y**.</span></span>
11. <span data-ttu-id="70614-184">**Start-CacheCluster** コマンドを実行してキャッシュを開始します。</span><span class="sxs-lookup"><span data-stu-id="70614-184">Run the **Start-CacheCluster** command to start the cache.</span></span>
12. <span data-ttu-id="70614-185">メモ帳で web.config ファイル (C:\\inetpub\\wwwroot\\wss\\VirtualDirectories\\81\\web.config) を管理者モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="70614-185">In Notepad, open the web.config file (C:\\inetpub\\wwwroot\\wss\\VirtualDirectories\\81\\web.config) in admin mode.</span></span>
13. <span data-ttu-id="70614-186">**&lt;configSections&gt;** セクションを検索します。</span><span class="sxs-lookup"><span data-stu-id="70614-186">Locate the **&lt;configSections&gt;** section.</span></span> <span data-ttu-id="70614-187">次の**セクション**要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="70614-187">Add the following **section** element.</span></span>

    ```
    <section name="dataCacheClient" type="Microsoft.ApplicationServer.Caching.DataCacheClientSection, Microsoft.ApplicationServer.Caching.Core, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35" allowLocation="true" allowDefinition="Everywhere" />
    ```

14. <span data-ttu-id="70614-188">**&lt;/configSections&gt;** タグの後の web.config ファイルに、次の **dataCacheClient** 要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="70614-188">Add the following **dataCacheClient** element to the web.config file after the **&lt;/configSections&gt;** tag.</span></span>

    1.  <span data-ttu-id="70614-189">“Host\_server\_name” のすべてのインスタンスを EP サーバーの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="70614-189">Replace every instance of “Host\_server\_name” with the name of an EP server.</span></span>
    2.  <span data-ttu-id="70614-190">"既定値" を **New-Cache** コマンドを実行したときに指定した名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="70614-190">Replace “default” with the name that you specified when you ran the **New-Cache** command.</span></span>

    <span data-ttu-id="70614-191"><!-- -->

        <!-- velocity -->
        <dataCacheClient dataCacheServiceAccountType="DomainAccount">
        <localCache isEnabled="false" />
        <hosts>
        <!--List of hosts -->
        <!-- Replace highlighted with your own EP server name -->
        <host name="EP-01" cachePort="22233" /> <host name="EP-02" cachePort="22233" /> <host name="EP-03" cachePort="22233" /> <host name="EP-0N" cachePort="22233" /> </hosts>
        </dataCacheClient>
        <Microsoft.Dynamics>
        <AppFabricCaching CacheName="default" />
        </Microsoft.Dynamics>
        <!-- velocity --></span><span class="sxs-lookup"><span data-stu-id="70614-191"><!-- -->

        <!-- velocity -->
        <dataCacheClient dataCacheServiceAccountType="DomainAccount">
        <localCache isEnabled="false" />
        <hosts>
        <!--List of hosts -->
        <!-- Replace highlighted with your own EP server name -->
        <host name="EP-01" cachePort="22233" /> <host name="EP-02" cachePort="22233" /> <host name="EP-03" cachePort="22233" /> <host name="EP-0N" cachePort="22233" /> </hosts>
        </dataCacheClient>
        <Microsoft.Dynamics>
        <AppFabricCaching CacheName="default" />
        </Microsoft.Dynamics>
        <!-- velocity --></span></span>

15. <span data-ttu-id="70614-192">LCS によって展開されているすべての EP サーバー上で手順 12 ～ 14 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="70614-192">Repeat steps 12 through 14 on every EP server that is deployed by LCS.</span></span>
16. <span data-ttu-id="70614-193">EP-01 サーバーの、Windows PowerShell ウィンドウで、**stop-cachecluster** コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="70614-193">On the EP-01 server, in a Windows PowerShell window, run the **stop-cachecluster** command.</span></span>
17. <span data-ttu-id="70614-194">**start-cachecluster** コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="70614-194">Run the **start-cachecluster** command.</span></span>

## <a name="validate-appfabric"></a><span data-ttu-id="70614-195">AppFabric の検証</span><span class="sxs-lookup"><span data-stu-id="70614-195">Validate AppFabric</span></span>
1.  <span data-ttu-id="70614-196">EP サーバーのいずれかの Windows サービス コンソールで、AppFabric キャッシュ サービスが実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="70614-196">On one of the EP servers, in the Windows Services console, verify that AppFabricCachingService is running.</span></span>
2.  <span data-ttu-id="70614-197">Windows PowerShell **コマンド プロンプト** ウィンドウを管理者として開きます。</span><span class="sxs-lookup"><span data-stu-id="70614-197">Open a Windows PowerShell **Command Prompt** window as an administrator.</span></span>
3.  <span data-ttu-id="70614-198">既定の **Get-CacheStatistics** コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="70614-198">Run the **Get-CacheStatistics** default command.</span></span> <span data-ttu-id="70614-199">結果にはすべてゼロが表示されます。</span><span class="sxs-lookup"><span data-stu-id="70614-199">The result should show all zeros.</span></span>
4.  <span data-ttu-id="70614-200">**iisereset** コマンドを実行することで、EP サーバーで Web サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="70614-200">Restart the web service on the EP server by running the **iisereset** command.</span></span>
5.  <span data-ttu-id="70614-201">EP を開き、**販売**に移動します。</span><span class="sxs-lookup"><span data-stu-id="70614-201">Open EP, and go to **Sales**.</span></span>
6.  <span data-ttu-id="70614-202">既定の **Get-CacheStatistics** コマンドをもう一度を実行し、キャッシュにより値が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="70614-202">Run the **Get-CacheStatistics** default command again, and verify that the cache shows values.</span></span> <span data-ttu-id="70614-203">この結果は、キャッシュの配分が機能していることを示しています。</span><span class="sxs-lookup"><span data-stu-id="70614-203">This result indicates that cache distribution is working.</span></span>

## <a name="clean-up"></a><span data-ttu-id="70614-204">クリーンアップ</span><span class="sxs-lookup"><span data-stu-id="70614-204">Clean up</span></span>
<span data-ttu-id="70614-205">すべての EP サーバーが独自のサーバー ファームに配置されているため、すべてのサーバーを単一のファームに結合させた後、他の EP サーバー ファーム用に作成されたデータベースを SQL から削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70614-205">Because every EP server was deployed into its own server farm, after you join all the servers into a single farm, the databases that were created for other EP server farms must be removed from SQL.</span></span>

-   <span data-ttu-id="70614-206">Spfarm\_admincontent\_ep-02</span><span class="sxs-lookup"><span data-stu-id="70614-206">Spfarm\_admincontent\_ep-02</span></span>
-   <span data-ttu-id="70614-207">Spfarm\_admincontent\_ep-03</span><span class="sxs-lookup"><span data-stu-id="70614-207">Spfarm\_admincontent\_ep-03</span></span>
-   <span data-ttu-id="70614-208">…</span><span class="sxs-lookup"><span data-stu-id="70614-208">…</span></span>
-   <span data-ttu-id="70614-209">Spfarm\_admincontent\_ep-0*N*</span><span class="sxs-lookup"><span data-stu-id="70614-209">Spfarm\_admincontent\_ep-0*N*</span></span>
-   <span data-ttu-id="70614-210">Spfarm\_config\_ep-02</span><span class="sxs-lookup"><span data-stu-id="70614-210">Spfarm\_config\_ep-02</span></span>
-   <span data-ttu-id="70614-211">Spfarm\_config\_ ep-03</span><span class="sxs-lookup"><span data-stu-id="70614-211">Spfarm\_config\_ ep-03</span></span>
-   <span data-ttu-id="70614-212">…</span><span class="sxs-lookup"><span data-stu-id="70614-212">…</span></span>
-   <span data-ttu-id="70614-213">Spfarm\_config\_ep-0*N*</span><span class="sxs-lookup"><span data-stu-id="70614-213">Spfarm\_config\_ep-0*N*</span></span>
-   <span data-ttu-id="70614-214">WSS\_コンテンツ\_\*</span><span class="sxs-lookup"><span data-stu-id="70614-214">WSS\_Content\_\*</span></span>

<span data-ttu-id="70614-215">特定のサイトの WSS \_コンテンツ\_\* データベースの名前を知るには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="70614-215">To learn the name of the WSS\_Content\_\* database for a particular site, follow these steps.</span></span>

1.  <span data-ttu-id="70614-216">SharePoint サーバーの管理を起動します。</span><span class="sxs-lookup"><span data-stu-id="70614-216">Start SharePoint Central Administration.</span></span>
2.  <span data-ttu-id="70614-217">**アプリケーション管理** &gt; **サイト コレクションの表示**に移動します。</span><span class="sxs-lookup"><span data-stu-id="70614-217">Go to **Application management** &gt; **View site collection**.</span></span>
3.  <span data-ttu-id="70614-218">右上隅で、ポート 81 でホストされているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="70614-218">In the upper-right corner, select the site that is hosted on port 81.</span></span> <span data-ttu-id="70614-219">結果画面には、選択したサイトに使用されているデータベースが示されます。</span><span class="sxs-lookup"><span data-stu-id="70614-219">The result screen should indicate which database is used for the selected site.</span></span>
4.  <span data-ttu-id="70614-220">サイト 81 が作成されたサーバーで使用されていない WSS \_コンテンツ\_\* データベースをすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="70614-220">Delete all WSS\_Content\_\* databases that aren't used by the server that site 81 is created on.</span></span> <span data-ttu-id="70614-221">この場合は、EP-01 によって使用される WSS\_Content\_\* データベースを保持し、WSS\_Content\_\* で始まる名前の他のデータベースをすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="70614-221">In this case, keep the WSS\_Content\_\* database that is used by EP-01, and delete every other database that has a name that starts with WSS\_Content\_\*.</span></span>






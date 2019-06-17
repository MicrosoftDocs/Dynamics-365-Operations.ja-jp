<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="join-enterprise-portal-servers-single-server-farm.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>join-enterprise-portal-servers-single-server-farm.203e12.488afaea08cf10ead1768ec888e0bd8219073a1b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>488afaea08cf10ead1768ec888e0bd8219073a1b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\ax-2012\join-enterprise-portal-servers-single-server-farm.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Join Enterprise Portal servers into a single server farm</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンタープライズ ポータル サーバーの 1 つのサーバー ファームへの結合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article explains how to join Enterprise Portal servers (for Microsoft Dynamics AX 2012) into a single server farm.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、エンタープライズ ポータル サーバー (Microsoft Dynamics AX 2012 用) を単一のサーバー ファームに参加させる方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Join Enterprise Portal servers into a single server farm</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンタープライズ ポータル サーバーの 1 つのサーバー ファームへの結合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article explains how to join Enterprise Portal servers (for Microsoft Dynamics AX 2012) into a single server farm.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、エンタープライズ ポータル サーバー (Microsoft Dynamics AX 2012 用) を単一のサーバー ファームに参加させる方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When Microsoft Dynamics Lifecycle Services (LCS) deploys Enterprise Portal (EP) servers, each EP server is deployed into its own server farm.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) でエンタープライズ ポータル (EP) サーバーが配置されると、各 EP サーバーは独自のサーバー ファームに配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The steps in this article show how to join all EP servers into a single server farm.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事のステップでは、すべての EP サーバーを単一のサーバー ファームに参加させる方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The basic idea is to keep the server farm on one EP server and join all the other EP servers to that farm.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本概念は、1 台の EP サーバー上にサーバー ファームを保持し、その他のすべての EP サーバーをそのファームに結合することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The information in this article is based on the following assumptions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事の情報は、次の前提条件に基づいています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">*</bpt>N<ept id="p1">*</ept> EP servers are deployed by LCS, and these servers are labeled EP-01, EP-02, EP-03...EP-0<bpt id="p2">*</bpt>N<ept id="p2">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>N<ept id="p1">*</ept> EP サーバーは、LCS によってが配置され、これらのサーバーは、EP-01、EP 02、EP-03...EP 0<bpt id="p2">*</bpt>N<ept id="p2">*</ept>とラベル付けされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The load balancer is named AzureILB01.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロード バランサを AzureILB01 と呼びます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You're using EP-01 as the single server farm, and all the other EP servers will join that farm.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EP-01 を単一のサーバー ファームとして使用し、その他のすべての EP サーバーはそのファームに参加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The following image shows the process for joining EP servers into a single server farm.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、EP サーバーを単一のサーバー ファームに参加させるプロセスを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>ProcessFlow<ph id="ph2">\_</ph>ConfigureEPServersInFarm<ept id="p1">](./media/processflow_configureepserversinfarm.png)](./media/processflow_configureepserversinfarm.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ProcessFlow<ph id="ph2">\_</ph>ConfigureEPServersInFarm<ept id="p1">](./media/processflow_configureepserversinfarm.png)](./media/processflow_configureepserversinfarm.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Put EP servers into a single server farm</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 台のサーバー ファームに EP サーバーを配置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Log on to EP-01 by using the Dynamics Installer User service account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics インストーラー ユーザー サービス アカウントを使用して EP-01 にログオンします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Start Microsoft SharePoint 2013 Central Administration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SharePoint 2013 Central Administration を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Go to <bpt id="p1">**</bpt>System settings<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Configure alternate access mappings<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム設定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>代替アクセス マッピングのコンフィギュレーション<ept id="p2">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Click <bpt id="p1">**</bpt>Add Internal URLs<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>内部 URL を追加する<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The following screen shot shows how to add a mapping for EP-02 on port 81, which is the port that the EP site is created on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットは、EP サイトが作成されたポートである、ポート 81 に EP-02 のマッピングを追加する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Repeat this step for every EP server that is deployed by LCS.<bpt id="p1">[</bpt><ph id="ph1">![</ph>AddInternalURLs<ept id="p1">](./media/addinternalurls.png)](./media/addinternalurls.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS によって展開されているすべての EP サーバーでこの手順を繰り返します。<bpt id="p1">[</bpt><ph id="ph1">![</ph>AddInternalURLs<ept id="p1">](./media/addinternalurls.png)](./media/addinternalurls.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Click <bpt id="p1">**</bpt>Edit Public URLs<ept id="p1">**</ept>, and enter appropriate values:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>公開 URL の編集<ept id="p1">**</ept>をクリックし、適切な値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Default:<ept id="p1">**</ept> Use the load balancer URL + port 81.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既定:<ept id="p1">**</ept>ロード バランサ URL + ポート 81 を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Intranet:<ept id="p1">**</ept> Use EP-01 (the SharePoint server farm virtual machine) + port 81.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>イントラネット:<ept id="p1">**</ept> EP-01 (SharePoint サーバー ファームの仮想マシン) とポート 81 を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Internet:<ept id="p1">**</ept> Use the publicly registered URL + port 81.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インターネット:<ept id="p1">**</ept> 公的に登録された URL と ポート 81 を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>EditPublicZoneURLs<ept id="p1">](./media/editpubliczoneurls.png)](./media/editpubliczoneurls.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>EditPublicZoneURLs<ept id="p1">](./media/editpubliczoneurls.png)](./media/editpubliczoneurls.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Open Registry Editor (regedit), and create the following registry key:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジストリ エディター (regedit) を開き、次のレジストリ キーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Path:<ept id="p1">**</ept> HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE<ph id="ph3">\\</ph>SYSTEM<ph id="ph4">\\</ph>CurrentControlSet<ph id="ph5">\\</ph>Contro<ph id="ph6">\\</ph>Lsa<ph id="ph7">\\</ph>MSV1<ph id="ph8">\_</ph>0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パス:<ept id="p1">**</ept> HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE<ph id="ph3">\\</ph>SYSTEM<ph id="ph4">\\</ph>CurrentControlSet<ph id="ph5">\\</ph>Contro<ph id="ph6">\\</ph>Lsa<ph id="ph7">\\</ph>MSV1<ph id="ph8">\_</ph>0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Key details, key value:<ept id="p1">**</ept> The load balancer name and the fully qualified name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>キーの詳細、キー値:<ept id="p1">**</ept> ロード バランサー名と完全修飾名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>EditMultiString<ept id="p1">](./media/editmultistring.png)](./media/editmultistring.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>EditMultiString<ept id="p1">](./media/editmultistring.png)](./media/editmultistring.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window, and get the IP address of the local machine by running the <bpt id="p2">**</bpt>ipconfig<ept id="p2">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、<bpt id="p2">**</bpt>ipconfig<ept id="p2">**</ept> コマンドを実行してローカル コンピューターの IP アドレスを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In Notepad, open the C:<ph id="ph1">\\</ph>Windows<ph id="ph2">\\</ph>System32<ph id="ph3">\\</ph>drivers<ph id="ph4">\\</ph>etc<ph id="ph5">\\</ph>hosts file, and map the load balancer name to the local machine IP address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メモ帳で C:<ph id="ph1">\\</ph>Windows<ph id="ph2">\\</ph>System32<ph id="ph3">\\</ph>drivers<ph id="ph4">\\</ph>etc<ph id="ph5">\\</ph>hosts ファイルを開き、ロード バランサー名をローカル コンピューターの IP アドレスにマップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>This mapping is used to test that the local EP server is working.<bpt id="p1">[</bpt><ph id="ph1">![</ph>NotePad<ept id="p1">](./media/notepad.png)](./media/notepad.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このマッピングは、ローカル EP サーバーが動作していることをテストするために使用されます。<bpt id="p1">[</bpt><ph id="ph1">![</ph>NotePad<ept id="p1">](./media/notepad.png)](./media/notepad.png)</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Repeat steps 6 through 8 on every EP server that is deployed by LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS によって展開されているすべての EP サーバー上で手順 6 ～ 8 を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Log on to the EP-02 server by using the Dynamics Installer User service account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics インストーラー ユーザー サービス アカウントを使用して EP-02 サーバーにログオンします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Go to the drive where the Dynamics installer is stored (this drive is most likely drive F).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics インストーラが格納されているドライブに移動します (このドライブはたいていドライブ F です)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Right-click <bpt id="p1">**</bpt>Setup<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Run as administrator<ept id="p2">**</ept>, and then follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セットアップ<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>管理者として実行<ept id="p2">**</ept> をクリックして以下の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Click <bpt id="p1">**</bpt>Install Microsoft Dynamics AX components<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Install Microsoft Dynamics AX コンポーネントのインストール<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>On the <bpt id="p1">**</bpt>Welcome<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ようこそ<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>次へ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Click <bpt id="p1">**</bpt>Add or modify components<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コンポーネントの追加または変更<ept id="p1">**</ept>をクリックし、次に<bpt id="p2">**</bpt>次へ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Under <bpt id="p1">**</bpt>Web server components<ept id="p1">**</ept>, select the <bpt id="p2">**</bpt>Enterprise Portal<ept id="p2">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Webサーバー コンポーネント<ept id="p1">**</ept> で、<bpt id="p2">**</bpt>エンタープライズ ポータル<ept id="p2">**</ept> チェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to acknowledge that you want to install EP, and then click <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックして EP をインストールすることを同意し、<bpt id="p2">**</bpt>次へ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Make sure that there are no validation errors, and then click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証エラーがないことを確認し、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Enter the BC proxy user password, and then click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BC プロキシ ユーザーのパスワードを入力し、<bpt id="p1">**</bpt>次<ept id="p1">**</ept>を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>On the **Configure a Web site for Enterprise Portal **page, select the web application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">**エンタープライズ ポータル用の Web サイトの構成**ページで、Web アプリケーションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Select the <bpt id="p1">**</bpt>Configure for Windows SharePoint Services<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Windows SharePoint Services を構成する<ept id="p1">**</ept>チェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Select the <bpt id="p1">**</bpt>Restart IIS after installation is completed<ept id="p1">**</ept> check box, and then click <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インストールの完了後に IIS を再起動<ept id="p1">**</ept> チェック ボックスをオンにし、<bpt id="p2">**</bpt>次へ<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Configure a Web site for EP<ept id="p1">](./media/configure-a-web-site-for-ep.png)](./media/configure-a-web-site-for-ep.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>EP 用の Web サイトの構成<ept id="p1">](./media/configure-a-web-site-for-ep.png)](./media/configure-a-web-site-for-ep.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> until the installation is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールが完了するまで<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Repeat steps 10 through 12 on servers EP-03 through EP-0<bpt id="p1">*</bpt>N<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー EP-03 から EP-0<bpt id="p1">*</bpt>N<ept id="p1">*</ept> で手順 10 ～ 12 を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>(You must re-install EP on every EP server, except the single server where the farm is configured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ファームがコンフィギュレーションされている単一のサーバーを除くすべての EP サーバーに EP を再インストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>In our example, this server is EP-01.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここでは、このサーバーは EP-01 です。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Follow these steps on every EP server, EP-01 through EP-0<bpt id="p1">*</bpt>N<ept id="p1">*</ept>:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 EP サーバー、EP-01 ～ EP-0<bpt id="p1">*</bpt>N<ept id="p1">*</ept> でこれらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Open the Internet Information Services (IIS) administration console (inetmgr).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット インフォメーション サービス (IIS) の管理コンソール (inetmgr) を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Go to <bpt id="p1">**</bpt>Sites<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>SharePoint – 81<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サイト<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>SharePoint – 81<ept id="p2">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Right-click, and then click <bpt id="p1">**</bpt>Edit bindings<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックして <bpt id="p1">**</bpt>バインドの編集<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Double-click the binding to open the <bpt id="p1">**</bpt>Edit Site Binding<ept id="p1">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バインディングをダブルクリックして、<bpt id="p1">**</bpt>Edit Site Binding<ept id="p1">**</ept> ダイアログ ボックスを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the <bpt id="p1">**</bpt>Host name<ept id="p1">**</ept> field, enter the load balancer name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ホスト名<ept id="p1">**</ept>フィールドに、ロード バランサー名を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Edit Site Binding<ept id="p1">](./media/edit-site-binding.png)](./media/edit-site-binding.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>編集サイト バインディング<ept id="p1">](./media/edit-site-binding.png)](./media/edit-site-binding.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Follow these validation steps on every EP server:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 EP サーバーで、これらの検証手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window, run the <bpt id="p2">**</bpt>iisreset<ept id="p2">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>iisreset<ept id="p2">**</ept> コマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Start Internet Explorer, and go to <bpt id="p1">**</bpt><ph id="ph1">http://AzureILB01:81/sites/DynamicsAx</ph><ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer を起動し、<bpt id="p1">**</bpt><ph id="ph1">http://AzureILB01:81/sites/DynamicsAx</ph><ept id="p1">**</ept> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Make sure that the Role Center page is rendered without error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロール センター ページがエラーなく表示されることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Configure AppFabric cache</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AppFabric キャッシュのコンフィギュレーション。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Log on to the EP-01 server by using the Dynamics Install User service account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics インストール ユーザー サービス アカウントを使用して EP-01 サーバーにログオンします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Open a Microsoft Windows PowerShell <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows PowerShell <bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを管理者として開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Run the <bpt id="p1">**</bpt>Use-CacheCluster<ept id="p1">**</ept> command to set the context of your Windows PowerShell session to a specific cache cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Use-CacheCluster<ept id="p1">**</ept> コマンドを実行し、Windows PowerShell セッションのコンテキストを特定のキャッシュ クラスターに設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Run the <bpt id="p1">**</bpt>New-Cache<ept id="p1">**</ept> command to create a new named cache.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>New-Cache<ept id="p1">**</ept> コマンドを実行して新しい名前のキャッシュを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Make a note of the name that you specify.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定する名前をメモします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>(You'll enter this cache name in the next procedure.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(このキャッシュ名は、次の手順で入力します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Run the <bpt id="p1">**</bpt>Grant-CacheAllowedClientAccount<ept id="p1">**</ept> command, and specify the .NET Business Connector proxy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Grant-CacheAllowedClientAccount<ept id="p1">**</ept> コマンドを実行し、.NET Business Connector プロキシを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>(This is the account that is used by the EP application pool).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(これは、EP アプリケーション プールで使用される口座です。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Run the following command: <bpt id="p1">**</bpt>Set-CacheConfig -Secondaries 1<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを実行します: <bpt id="p1">**</bpt>Set-CacheConfig -Secondaries 1<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>When you're prompted for the cache name, enter the name from step 4.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュ名の入力を要求するメッセージが表示されたら、ステップ 4 から名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>When you're asked whether you want to continue, enter <bpt id="p1">**</bpt>Y<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">続行するかどうかを問われたときは、<bpt id="p1">**</bpt>Y<ept id="p1">**</ept> を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>If step 6 causes an error, try to run the commands in the following order:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 6 では、エラーが発生する場合は、次の順序でコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>stop-cachecluster</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">stop-cachecluster</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Set-CacheConfig -Secondaries 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Set-CacheConfig -Secondaries 1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Export the configuration by running the <bpt id="p1">**</bpt>Export-CacheClusterConfig<ept id="p1">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Export-CacheClusterConfig<ept id="p1">**</ept> コマンドを実行してコンフィギュレーションをエキスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Specify a name for the file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルの名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>This file can be saved anywhere on the local computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルは、ローカル コンピューターの任意の場所に保存できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Open the file that you just created, and add the following configuration to the <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>advancedProperties<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先ほど作成したファイルを開き、<bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>advancedProperties<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> セクションに次のコンフィギュレーションを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Import the configuration by running the following command: <bpt id="p1">**</bpt>Import-CacheClusterConfig c:<ph id="ph1">\\</ph>newConfig.xml<ept id="p1">**</ept> When you're asked whether you want to continue, enter <bpt id="p2">**</bpt>Y<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Import-CacheClusterConfig c:<ph id="ph1">\\</ph>newConfig.xml<ept id="p1">**</ept> のコマンドを実行して、コンフィギュレーションをインポートします。続行するか確認された場合、<bpt id="p2">**</bpt>Y<ept id="p2">**</ept> を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Run the <bpt id="p1">**</bpt>Start-CacheCluster<ept id="p1">**</ept> command to start the cache.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Start-CacheCluster<ept id="p1">**</ept> コマンドを実行してキャッシュを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In Notepad, open the web.config file (C:<ph id="ph1">\\</ph>inetpub<ph id="ph2">\\</ph>wwwroot<ph id="ph3">\\</ph>wss<ph id="ph4">\\</ph>VirtualDirectories<ph id="ph5">\\</ph>81<ph id="ph6">\\</ph>web.config) in admin mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メモ帳で web.config ファイル (C:<ph id="ph1">\\</ph>inetpub<ph id="ph2">\\</ph>wwwroot<ph id="ph3">\\</ph>wss<ph id="ph4">\\</ph>VirtualDirectories<ph id="ph5">\\</ph>81<ph id="ph6">\\</ph>web.config) を管理者モードで開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Locate the <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>configSections<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>configSections<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> セクションを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Add the following <bpt id="p1">**</bpt>section<ept id="p1">**</ept> element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の<bpt id="p1">**</bpt>セクション<ept id="p1">**</ept>要素を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Add the following <bpt id="p1">**</bpt>dataCacheClient<ept id="p1">**</ept> element to the web.config file after the <bpt id="p2">**</bpt><ph id="ph1">&amp;lt;</ph>/configSections<ph id="ph2">&amp;gt;</ph><ept id="p2">**</ept> tag.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt><ph id="ph1">&amp;lt;</ph>/configSections<ph id="ph2">&amp;gt;</ph><ept id="p2">**</ept> タグの後の web.config ファイルに、次の <bpt id="p1">**</bpt>dataCacheClient<ept id="p1">**</ept> 要素を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Replace every instance of “Host<ph id="ph1">\_</ph>server<ph id="ph2">\_</ph>name” with the name of an EP server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">“Host<ph id="ph1">\_</ph>server<ph id="ph2">\_</ph>name” のすべてのインスタンスを EP サーバーの名前に置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Replace “default” with the name that you specified when you ran the <bpt id="p1">**</bpt>New-Cache<ept id="p1">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"既定値" を <bpt id="p1">**</bpt>New-Cache<ept id="p1">**</ept> コマンドを実行したときに指定した名前に置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Repeat steps 12 through 14 on every EP server that is deployed by LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS によって展開されているすべての EP サーバー上で手順 12 ～ 14 を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>On the EP-01 server, in a Windows PowerShell window, run the <bpt id="p1">**</bpt>stop-cachecluster<ept id="p1">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EP-01 サーバーの、Windows PowerShell ウィンドウで、<bpt id="p1">**</bpt>stop-cachecluster<ept id="p1">**</ept> コマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Run the <bpt id="p1">**</bpt>start-cachecluster<ept id="p1">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>start-cachecluster<ept id="p1">**</ept> コマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Validate AppFabric</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AppFabric の検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>On one of the EP servers, in the Windows Services console, verify that AppFabricCachingService is running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EP サーバーのいずれかの Windows サービス コンソールで、AppFabric キャッシュ サービスが実行されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Open a Windows PowerShell <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows PowerShell <bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを管理者として開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Run the <bpt id="p1">**</bpt>Get-CacheStatistics<ept id="p1">**</ept> default command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の <bpt id="p1">**</bpt>Get-CacheStatistics<ept id="p1">**</ept> コマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The result should show all zeros.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果にはすべてゼロが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Restart the web service on the EP server by running the <bpt id="p1">**</bpt>iisereset<ept id="p1">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>iisereset<ept id="p1">**</ept> コマンドを実行することで、EP サーバーで Web サービスを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Open EP, and go to <bpt id="p1">**</bpt>Sales<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EP を開き、<bpt id="p1">**</bpt>販売<ept id="p1">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Run the <bpt id="p1">**</bpt>Get-CacheStatistics<ept id="p1">**</ept> default command again, and verify that the cache shows values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の <bpt id="p1">**</bpt>Get-CacheStatistics<ept id="p1">**</ept> コマンドをもう一度を実行し、キャッシュにより値が表示されることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>This result indicates that cache distribution is working.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この結果は、キャッシュの配分が機能していることを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Clean up</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クリーンアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Because every EP server was deployed into its own server farm, after you join all the servers into a single farm, the databases that were created for other EP server farms must be removed from SQL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての EP サーバーが独自のサーバー ファームに配置されているため、すべてのサーバーを単一のファームに結合させた後、他の EP サーバー ファーム用に作成されたデータベースを SQL から削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Spfarm<ph id="ph1">\_</ph>admincontent<ph id="ph2">\_</ph>ep-02</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Spfarm<ph id="ph1">\_</ph>admincontent<ph id="ph2">\_</ph>ep-02</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Spfarm<ph id="ph1">\_</ph>admincontent<ph id="ph2">\_</ph>ep-03</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Spfarm<ph id="ph1">\_</ph>admincontent<ph id="ph2">\_</ph>ep-03</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>…</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">…</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Spfarm<ph id="ph1">\_</ph>admincontent<ph id="ph2">\_</ph>ep-0<bpt id="p1">*</bpt>N<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Spfarm<ph id="ph1">\_</ph>admincontent<ph id="ph2">\_</ph>ep-0<bpt id="p1">*</bpt>N<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Spfarm<ph id="ph1">\_</ph>config<ph id="ph2">\_</ph>ep-02</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Spfarm<ph id="ph1">\_</ph>config<ph id="ph2">\_</ph>ep-02</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Spfarm<ph id="ph1">\_</ph>config<ph id="ph2">\_</ph> ep-03</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Spfarm<ph id="ph1">\_</ph>config<ph id="ph2">\_</ph> ep-03</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>…</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">…</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Spfarm<ph id="ph1">\_</ph>config<ph id="ph2">\_</ph>ep-0<bpt id="p1">*</bpt>N<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Spfarm<ph id="ph1">\_</ph>config<ph id="ph2">\_</ph>ep-0<bpt id="p1">*</bpt>N<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>WSS<ph id="ph1">\_</ph>Content<ph id="ph2">\_</ph><ph id="ph3">\*</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WSS<ph id="ph1">\_</ph>コンテンツ<ph id="ph2">\_</ph><ph id="ph3">\*</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>To learn the name of the WSS<ph id="ph1">\_</ph>Content<ph id="ph2">\_</ph><ph id="ph3">\*</ph> database for a particular site, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のサイトの WSS <ph id="ph1">\_</ph>コンテンツ<ph id="ph2">\_</ph><ph id="ph3">\*</ph> データベースの名前を知るには、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Start SharePoint Central Administration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SharePoint サーバーの管理を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Go to <bpt id="p1">**</bpt>Application management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>View site collection<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>サイト コレクションの表示<ept id="p2">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>In the upper-right corner, select the site that is hosted on port 81.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右上隅で、ポート 81 でホストされているサイトを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The result screen should indicate which database is used for the selected site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果画面には、選択したサイトに使用されているデータベースが示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Delete all WSS<ph id="ph1">\_</ph>Content<ph id="ph2">\_</ph><ph id="ph3">\*</ph> databases that aren't used by the server that site 81 is created on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイト 81 が作成されたサーバーで使用されていない WSS <ph id="ph1">\_</ph>コンテンツ<ph id="ph2">\_</ph><ph id="ph3">\*</ph> データベースをすべて削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>In this case, keep the WSS<ph id="ph1">\_</ph>Content<ph id="ph2">\_</ph><ph id="ph3">\*</ph> database that is used by EP-01, and delete every other database that has a name that starts with WSS<ph id="ph4">\_</ph>Content<ph id="ph5">\_</ph><ph id="ph6">\*</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合は、EP-01 によって使用される WSS<ph id="ph1">\_</ph>Content<ph id="ph2">\_</ph><ph id="ph3">\*</ph> データベースを保持し、WSS<ph id="ph4">\_</ph>Content<ph id="ph5">\_</ph><ph id="ph6">\*</ph> で始まる名前の他のデータベースをすべて削除します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
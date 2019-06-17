<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="install-dmt.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>install-dmt.410525.a301bafc023af117a38e6901e1e0d01232f6e79b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>a301bafc023af117a38e6901e1e0d01232f6e79b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\install-dmt.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>AX 2009 migration - Install the Data migration tool</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 の移行 － データ移行ツールのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to set up the Data migration tool (DMT) so that you can migrate your data from Microsoft Dynamics AX 2009 to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations にデータを移行できるように、データ移行ツール (DMT) を設定する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>AX 2009 migration – Install the Data migration tool</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 の移行 – データ移行ツールのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to set up the Data migration tool (DMT) so that you can migrate data from Microsoft Dynamics AX 2009 to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations にデータを移行できるように、データ移行ツール (DMT) を設定する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>At this time, the DMT is in private preview.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現時点で、DMT はプライベート プレビューです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>If you are interested you can sign up for the <bpt id="p1">[</bpt>Preview Program<ept id="p1">](https://microsoft.qualtrics.com/jfe/form/SV_brOLCioQ7mmeykB)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関心をお持ちの場合、<bpt id="p1">[</bpt>プレビュー プログラム<ept id="p1">](https://microsoft.qualtrics.com/jfe/form/SV_brOLCioQ7mmeykB)</ept>にサインアップすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The public release date for the DMT has not been set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DMT の公開リリース日は設定されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Microsoft SQL Server 2008/2012/2014/2016.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2008/2012/2014/2016。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The Microsoft .NET Framework version 4.5 or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft .NET Framework バージョン 4.5 またはそれ以降。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Microsoft SQL Server machine that has Microsoft SQL 2012 Native Client installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL 2012 Native Client がインストールされている Microsoft SQL Server コンピューター。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The Microsoft SQL Server Integration Services (SSIS) service is installed and running on the machine where the DMT service will be installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server Integration Services (SSIS) サービスがインストールされ、DMT サービスがインストールされるコンピューターで実行されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>SQL Server authentication must support both SQL authentication and Microsoft Windows authentication.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server 認証は、SQL 認証と Microsoft Windows 認証の両方をサポートする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Microsoft Access database engines that follows the version guidance in the following table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表のバージョン ガイダンスに従っている Microsoft Access データベース エンジン。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>SQL Server 2008</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server 2008</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>SQL Server 2012 and later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server 2012 以降</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>No Microsoft Office on the VM<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>VM に Microsoft Office がない<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Access engine 32-bit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Access エンジン 32 ビット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Access engine 64-bit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Access エンジン 64 ビット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Microsoft Office 32-bit<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Office 32 ビット<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Access engine 32-bit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Access エンジン 32 ビット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Access engine 64-bit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Access エンジン 64 ビット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Microsoft Office 64-bit<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Office 64 ビット<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Access engine 32-bit and 64-bit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Access エンジン 32 ビットおよび 64 ビット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Access engine 64-bit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Access エンジン 64 ビット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Microsoft Dynamics AX 2009 SP1 5.0.1000.52 or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2009 SP1 5.0.1000.52 以降。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The prerequisite patch (axpatch.exe) installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件となる修正プログラム (axpatch.exe) がインストールされている。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>To find the patch, from the location where you downloaded and extracted the zip file, go to &lt;pre-requisiteforpatch<ph id="ph1">\&gt;</ph><ph id="ph2">\&lt;</ph>application<ph id="ph3">\&gt;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正プログラムを見つけるには、ZIP ファイルをダウンロードして展開した場所から、&lt;pre-requisiteforpatch<ph id="ph1">\&gt;</ph><ph id="ph2">\&lt;</ph>application<ph id="ph3">\&gt;</ph> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Install DIXF service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DIXF サービスのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Go to the location where you extracted the zip file, and then, in the <bpt id="p1">**</bpt>DIXF msi<ept id="p1">**</ept> folder, right-click <bpt id="p2">**</bpt>DIXF<ph id="ph1">\_</ph>Service<ph id="ph2">\_</ph>x64.msi<ept id="p2">**</ept>, and select <bpt id="p3">**</bpt>Run<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ZIP ファイルを展開した場所に移動し、<bpt id="p1">**</bpt>DIXF msi<ept id="p1">**</ept> フォルダーで <bpt id="p2">**</bpt>DIXF<ph id="ph1">\_</ph>Service<ph id="ph2">\_</ph>x64.msi<ept id="p2">**</ept> を右クリックし、<bpt id="p3">**</bpt>実行<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>When the wizard starts, select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィザードが開始したら、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Accept the license terms, and then select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンス条項を受け入れ、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Select an account for the service, and then select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービスのアカウントを選択し、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The account should have admin rights.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アカウントは、管理者権限を持っている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you select the <bpt id="p1">**</bpt>Network Service<ept id="p1">**</ept> check box, verify that the network service account has admin rights.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ネットワーク サービス<ept id="p1">**</ept> チェック ボックスをオンにした場合、ネットワーク サービス アカウントに管理者権限があることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Otherwise, clear the check box, and enter an admin account user name and password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、チェック ボックスをオフにし、管理者アカウントのユーザー名とパスワードを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Then select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Select the SQL Server version, and then select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server のバージョンを選択し、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Select <bpt id="p1">**</bpt>Install<ept id="p1">**</ept>, and then, when the wizard is completed, select <bpt id="p2">**</bpt>Finish<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インストール<ept id="p1">**</ept> を選択し、ウィザードが完了したら <bpt id="p2">**</bpt>完了<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Copy binaries</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バイナリのコピー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Go to the location where you extracted the zip file, and copy the following files to the <bpt id="p1">**</bpt>Program Files (x86)<ph id="ph1">\\</ph>Microsoft Dynamics AX<ph id="ph2">\\</ph>50<ph id="ph3">\\</ph>Client<ph id="ph4">\\</ph>Bin<ept id="p1">**</ept> folder:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ZIP ファイルを展開した場所に移動し、以下のファイルを <bpt id="p1">**</bpt>Program Files (x86)<ph id="ph1">\\</ph>Microsoft Dynamics AX<ph id="ph2">\\</ph>50<ph id="ph3">\\</ph>Client<ph id="ph4">\\</ph>Bin<ept id="p1">**</ept> フォルダーにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Microsoft.Dynamics.AX.Framework.Tools.DMT.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.AX.Framework.Tools.DMT.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Interop.Shell32.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Interop.Shell32.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Install DMT components for AX 2009</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 の DMT コンポーネントのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>There are two ways to install the DMT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DMT をインストールする方法は 2 つあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>You can use the combined XPO file or an application hotfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結合された XPO ファイルまたはアプリケーション修正プログラムを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If you're using a Microsoft Dynamics Lifecycle Services (LCS) Implementation project, use the application hotfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) 実装プロジェクトを使用している場合、アプリケーション修正プログラムを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Installation takes approximately seven hours.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールには、約 7 時間かかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Combined XPO file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結合された XPO ファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Extract the combined XPO file from <bpt id="p1">**</bpt>DMT_V1.0\CombinedXPO<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結合された XPO ファイルを <bpt id="p1">**</bpt>DMT_V1.0\CombinedXPO<ept id="p1">**</ept> から展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Import the combined XPO file into AX 2009.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 に結合された XPO ファイルをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Copy the label file from <bpt id="p1">**</bpt>DMT_V1.0\Label file<ept id="p1">**</ept> to the <bpt id="p2">**</bpt>Program Files<ph id="ph1">\\</ph>Microsoft Dynamics AX<ph id="ph2">\\</ph>50<ph id="ph3">\\</ph>Application<ph id="ph4">\\</ph>Appl<ph id="ph5">\\</ph>&lt;NameOfYourDeployment<ph id="ph6">\&gt;</ph><ept id="p2">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DMT_V1.0\Label file<ept id="p1">**</ept> ファイルから  <bpt id="p2">**</bpt>Program Files<ph id="ph1">\\</ph>Microsoft Dynamics AX<ph id="ph2">\\</ph>50<ph id="ph3">\\</ph>Application<ph id="ph4">\\</ph>Appl<ph id="ph5">\\</ph>&lt;NameOfYourDeployment<ph id="ph6">\&gt;</ph><ept id="p2">**</ept> フォルダーにラベル ファイルをコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Restart the Application Object Server (AOS) instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS) インスタンスを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In AX 2009, select <bpt id="p1">**</bpt>Data migration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Compile and synchronize DMT application<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 で、<bpt id="p1">**</bpt>データ移行<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>DMT アプリケーションのコンパイルと同期<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Note that the combined XPO file is imported into the layer that the user is signed in to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがログインしているレイヤーに結合された XPO ファイルがインポートされることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Application hotfix</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの修正プログラム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Go to <bpt id="p1">**</bpt>DMT_V1.0<ph id="ph1">\\</ph>ApplicationHotfix<ph id="ph2">\\</ph>DynamicsAX2009-KB4010403-SP1<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>setup.exe<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>Run<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DMT_V1.0<ph id="ph1">\\</ph>ApplicationHotfix<ph id="ph2">\\</ph>DynamicsAX2009-KB4010403-SP1<ept id="p1">**</ept> に移動し、<bpt id="p2">**</bpt>setup.exe<ept id="p2">**</ept> を右クリックして <bpt id="p3">**</bpt>実行<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In AX 2009, in the Application Object Tree (AOT), notice that the <bpt id="p1">**</bpt>LegalEntityId<ept id="p1">**</ept> field has been added to the <bpt id="p2">**</bpt>DMTCustomerAddressView<ept id="p2">**</ept> and <bpt id="p3">**</bpt>DMTVendorAddressView<ept id="p3">**</ept> views.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 のアプリケーション オブジェクト ツリー (AOT) で、<bpt id="p1">**</bpt>LegalEntityId<ept id="p1">**</ept> フィールドが <bpt id="p2">**</bpt>DMTCustomerAddressView<ept id="p2">**</ept> ビューと <bpt id="p3">**</bpt>DMTVendorAddressView<ept id="p3">**</ept> ビューに追加されていることに注目してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Select <bpt id="p1">**</bpt>Data migration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Compile and synchronize DMT application<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ移行<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>DMT アプリケーションのコンパイルと同期<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Parameter setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメータの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Go to the location to where you extracted the zip file, and find <bpt id="p1">**</bpt>defaultvalue.xlsx<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ZIP ファイルを展開した場所に移動し、<bpt id="p1">**</bpt>defaultvalue.xlsx<ept id="p1">**</ept> を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The file is saved in .xlsx format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルは .xlsx 形式に保存されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Don't change the extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を変更しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>When you provide this file as input for the <bpt id="p1">**</bpt>Default configuration<ept id="p1">**</ept> parameter, select <bpt id="p2">**</bpt>All Files<ept id="p2">**</ept> so that you can select the .xlsx format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルを <bpt id="p1">**</bpt>既定のコンフィギュレーション<ept id="p1">**</ept> パラメーターの入力として入力したら、<bpt id="p2">**</bpt>すべてのファイル<ept id="p2">**</ept> を選択して .xlsx 形式を選択できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>If you don't select this format, errors will occur when you start to generate mappings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この形式を選択しない場合、マッピングの生成を開始するとエラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>In AX 2009, select <bpt id="p1">**</bpt>Data migration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Configure default maps<ept id="p3">**</ept>, and enter the appropriate information in the following fields:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 で、<bpt id="p1">**</bpt>データ移行<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>既定のマップを構成する<ept id="p3">**</ept> を選択し、次のフィールドに適切な情報を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Default configuration<ept id="p1">**</ept> – Enter the path of the Microsoft Excel file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既定のコンフィギュレーション<ept id="p1">**</ept>: Microsoft Excel ファイルのパスを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">**</bpt>Export file path<ept id="p1">**</ept> – Enter the server path that can be accessed by the service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エクスポート ファイルのパス<ept id="p1">**</ept>: サービスがアクセスできるサーバーのパスを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>SQL Server user and password<ept id="p1">**</ept> – Enter the SQL authentication credentials for the AX 2009 database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SQL Server のユーザー名とパスワード<ept id="p1">**</ept>: AX 2009 データベースの SQL 認証資格情報を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Close the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Under <bpt id="p1">**</bpt>Setup<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Configure connections<ept id="p2">**</ept>, and enter the appropriate information on the following fields:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定<ept id="p1">**</ept> で、<bpt id="p2">**</bpt>接続の構成<ept id="p2">**</ept> を選択し、次のフィールドに適切な情報を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source><bpt id="p1">**</bpt>DIXF service host<ept id="p1">**</ept> – Enter the host name of the DIXF service installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DIXF サービス ホスト<ept id="p1">**</ept>: DIXF サービスのインストールのホスト名を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">**</bpt>Tenant URL<ept id="p1">**</ept> – Enter the Finance and Operations URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テナント URL<ept id="p1">**</ept>: Finance and Operations の URL を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>If you aren't sure of the tenant, see the Finance and Operations web.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テナントが不明な場合は、Finance and Operations の web.config ファイルを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>[!NOTE} In the Azure Portal, when you create a new app in the Azure Active Directory (AAD), you can select from two options.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[!注意} Azure ポータルでは、Azure Active Directory (AAD) で新しいアプリケーションを作成するときは、2 つのオプションから選択できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><bpt id="p1">**</bpt>Web API<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Native<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Web API<ept id="p1">**</ept> と <bpt id="p2">**</bpt>ネイティブ<ept id="p2">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>In this instance, select <bpt id="p1">**</bpt>Native<ept id="p1">**</ept> and grant permissions to native AAD app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このインスタンスでは、<bpt id="p1">**</bpt>ネイティブ<ept id="p1">**</ept> を選択し、ネイティブ AAD アプリケーションへのアクセス許可を付与します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Multi-box setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マルチボックスの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>For a multi-box setup, you must have the following machines:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マルチボックスの設定の場合、次のコンピューターが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Machine A, where the AX 2009 database and DIXF service are installed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 データベースおよび DIXF サービスがインストールされているコンピューター A</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Machine B, where the AX 2009 AOS instance is installed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 AOS インスタンスがインストールされているコンピューター B</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Machine C, where the AX 2009 client is installed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 クライアントがインストールされているコンピューター C</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In this three-machine setup, machine C is configured to connect to the AOS instance on machine B. Machine B is connected to the database that is configured on machine A.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この 3 コンピューター設定では、コンピューター C はコンピューター B の AOS インスタンスに接続するように構成されています。コンピューター B は、コンピューター A で構成されているデータベースに接続されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>DIXF service machine prerequisites (machine A)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DIXF サービス コンピューターの前提条件 (コンピューター A)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>The DIXF service on machine A has the following prerequisites:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューター A の DIXF サービスには、次の前提条件があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>SQL Server 2008/2012/2014</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server 2008/2012/2014</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The .NET Framework version 4.5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NET Framework バージョン 4.5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Access database engines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Access データベース エンジン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>For SQL Server 2008:<ept id="p1">**</ept> Access engine 32-bit and 64-bit (if Microsoft Excel is 64-bit)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SQL Server 2008 の場合:<ept id="p1">**</ept> Access エンジン 32 ビットおよび 64 ビット (Microsoft Excel が 64 ビットの場合)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>For SQL Server 2012 or later:<ept id="p1">**</ept> Access engine 64-bit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SQL Server 2012 以降の場合:<ept id="p1">**</ept> Access エンジン 64 ビット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>AX 2009 database (configured on SQL Server)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 データベース (SQL Server で構成)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>AOS machine prerequisites (machine B)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS コンピューターの前提条件 (コンピューター B)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The AOS installation on machine B has the following prerequisites:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューター B の AOS のインストールには、次の前提条件があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>AX 2009 AOS Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 AOS サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Application files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション ファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Client machine prerequisites (machine C)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンピューターの前提条件 (コンピューター C)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>The client installation on machine C has the following prerequisites:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューター C のクライアントのインストールには、次の前提条件があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>AX 2009 client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Shared folder permissions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有フォルダーのアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>The path of the default configuration file and the export package file should be shared, and client users and the DIXF service should have read/write access to these files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のコンフィギュレーション ファイルとエクスポート パッケージ ファイルのパスは共有する必要があり、クライアント ユーザーおよび DIXF サービスにはこれらのファイルへの読み取り/書き込みアクセスが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>To grant this access, select <bpt id="p1">**</bpt>Data migration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Configure and generate maps<ept id="p3">**</ept>, and then select <bpt id="p4">**</bpt>Validate path<ept id="p4">**</ept> to verify that the required access is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクセス権を付与するには、<bpt id="p1">**</bpt>データ移行<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>マップの構成と生成<ept id="p3">**</ept> を選択し、<bpt id="p4">**</bpt>パスの検証<ept id="p4">**</ept> を選択して必要なアクセス権があることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Set up parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメータの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Select <bpt id="p1">**</bpt>Data migration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Configure connections<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ移行<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>接続の構成<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>In the <bpt id="p1">**</bpt>DIXF service host<ept id="p1">**</ept> field, enter the name of the remote machine where the DIXF service is installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DIXF サービス ホスト<ept id="p1">**</ept> フィールドに、DIXF サービスがインストールされているリモート コンピューターの名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>By default, the name is <bpt id="p1">**</bpt>localhost<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、名前は <bpt id="p1">**</bpt>localhost<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Select <bpt id="p1">**</bpt>Validate<ept id="p1">**</ept> to validate that the client can access the DIXF service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>検証<ept id="p1">**</ept> を選択し、クライアントが DIXF サービスにアクセスできることを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Workarounds</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">回避策</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>If you receive an error message that states, "DIXF service is unavailable," complete the following workaround to enable a service connection for port 7000.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"DIXF サービスを利用できません" というエラー メッセージが表示される場合、次の回避方法を実行してポート 7000 のサービスの接続を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Open port 7000, and then, for inbound rules on the DMT service machine, select <bpt id="p1">**</bpt>Firewall settings<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Run<ept id="p2">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p3">**</bpt>wf.msc<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポート 7000 を開いた後、DMT サービス コンピューターの受信ルールで <bpt id="p1">**</bpt>ファイアウォール設定<ept id="p1">**</ept> を選択して <bpt id="p2">**</bpt>実行<ept id="p2">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p3">**</bpt>wf.msc<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Select <bpt id="p1">**</bpt>Inbound Rules<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>New rule<ept id="p2">**</ept>, and then, on the <bpt id="p3">**</bpt>Rule Type<ept id="p3">**</ept> tab, select <bpt id="p4">**</bpt>Port<ept id="p4">**</ept>, and then select <bpt id="p5">**</bpt>Next<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>受信ルール<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>新しいルール<ept id="p2">**</ept> を選択した後、<bpt id="p3">**</bpt>ルール タイプ<ept id="p3">**</ept> タブで、<bpt id="p4">**</bpt>ポート<ept id="p4">**</ept> を選択し、<bpt id="p5">**</bpt>次へ<ept id="p5">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>In the <bpt id="p1">**</bpt>Specific local ports<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>7000<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>Next<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>特定のローカル ポート<ept id="p1">**</ept> フィールドに、<bpt id="p2">**</bpt>7000<ept id="p2">**</ept> と入力し、<bpt id="p3">**</bpt>次へ<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Select <bpt id="p1">**</bpt>Allow the connection<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>接続を許可する<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>次へ<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Select all three check boxes to apply all the rules, and then select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 つのチェック ボックスをすべてオンにしてすべてのルールを適用し、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Enter the name of the rule, and then select <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールの名前を入力し、<bpt id="p1">**</bpt>完了<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Repeat these steps for outbound rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">送信ルールでこれらの手順を繰り返します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
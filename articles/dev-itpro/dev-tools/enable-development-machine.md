<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="enable-development-machine.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>enable-development-machine.3b62e5.9c12c765c6bc1a55b2d89e3b01b00df8c4a6b132.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>9c12c765c6bc1a55b2d89e3b01b00df8c4a6b132</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\enable-development-machine.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Create new users on development machines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発マシンでの新しいユーザーの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>When an environment is first deployed, only one user account is enabled as a developer on the virtual machine (VM).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境が最初に配置されるとき、1 つのユーザー アカウントのみが仮想マシン (VM)上で開発者として有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>This article explains how to enable another user account as a developer on a development VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、開発者が開発 VM に別のユーザー アカウントを有効にする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Create new users on development machines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発マシンでの新しいユーザーの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This article explains how to enable another user account as a developer on a development VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、開発者が開発 VM に別のユーザー アカウントを有効にする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic only applies to downloaded local virtual machines (VMs) or VMs that are hosted in a customer’s subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、ダウンロードされたローカル仮想マシン (VM) か、顧客のサブスクリプションでホストされている VM にのみ適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You can't create new users on Microsoft-managed developer and build machines where developers have no administrator acces to the VM (Platform update 12 or newer).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者が VM への管理者アクセスを持たない Microsoft が管理する開発およびビルド マシン (プラットフォーム更新 12 以降) において、新しいユーザーを作成することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>When an environment is first deployed, only one user account is enabled as a developer on the virtual machine (VM).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境が最初に配置されるとき、1 つのユーザー アカウントのみが仮想マシン (VM)上で開発者として有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This user is preconfigured by Microsoft Dynamics Lifecycle Services (LCS) or is the local administrator account on downloaded virtual hard disks (VHDs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このユーザーは、Microsoft Dynamics Lifecycle Services (LCS) によって事前設定するか、ダウンロードした仮想ハードディスク (VHD) のローカル管理者のアカウントです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, you can enable a new user account to develop on the VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、新しいユーザー アカウントを VM で開発できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Even after you enable a new account, only one developer can develop at a time on the same VM/application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいアカウントを有効にした後でも、同じ VM/アプリケーションで一度に開発できる開発者は 1 人だけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To enable a new user account to develop on the VM, the user account must be an administrator on the VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいユーザー アカウントが VM で開発できるようにするには、ユーザー アカウントが VM の管理者である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Additionally, you must log on to the VM by using the credentials of the default developer account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、既定の開発者アカウントの資格情報を使用して VM にログオンする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If the VM is a Microsoft Azure VM, the account information is available on the environment page in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM が Microsoft Azure VM である場合は、この勘定の情報は LCS の環境のページで使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>If the VM is a local VM that runs on the downloaded VHD, use the local administrator account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM がダウンロードした VHD 上で実行されるローカル VM である場合は、ローカル管理者アカウントを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>For more information, see <bpt id="p1">[</bpt>Access Instances<ept id="p1">](../dev-tools/access-instances.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>アクセス インスタンス<ept id="p1">](../dev-tools/access-instances.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Download the following script: ProvisionAxDeveloper.ps1, the script is available at <ph id="ph1">&lt;https://github.com/Microsoft/Dynamics-AX-Scripts&gt;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプト ProvisionAxDeveloper.ps1 をダウンロードしてください。スクリプトは、<ph id="ph1">&lt;https://github.com/Microsoft/Dynamics-AX-Scripts&gt;</ph> で利用可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Open a Microsoft Windows <bpt id="p1">**</bpt>PowerShell Command Prompt<ept id="p1">**</ept> window as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows PowerShell <bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを管理者として開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Run the ProvisionAxDeveloper.ps1 script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProvisionAxDeveloper.ps1 スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Specify the following parameters:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のパラメーターを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>DatabaseServerName<ept id="p1">**</ept> – Typically, this is the machine name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DatabaseServerName<ept id="p1">**</ept> - 通常、これは、コンピューター名です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Users<ept id="p1">**</ept> – Use the following format: <ph id="ph1">&amp;lt;</ph>domain or machine name<ph id="ph2">&amp;gt;</ph><ph id="ph3">\\</ph>user1, …</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ユーザー<ept id="p1">**</ept> – 次の形式を使用します: <ph id="ph1">&amp;lt;</ph>ドメインまたはコンピューター名<ph id="ph2">&amp;gt;</ph><ph id="ph3">\\</ph>ユーザー 1、…</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><ph id="ph1">&amp;lt;</ph>domain or machine name<ph id="ph2">&amp;gt;</ph><ph id="ph3">\\</ph>user n</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>ドメインまたはコンピューター名<ph id="ph2">&amp;gt;</ph><ph id="ph3">\\</ph>ユーザー n</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Examples<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If more than one user account will be developing on the same version control workspace, you need to make the workspace public.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つ以上のユーザー アカウントが同じバージョン管理ワークスペース上で開発されている場合、ワークスペースをパブリックにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In Visual Studio, open <bpt id="p1">**</bpt>Source Control Explorer<ept id="p1">**</ept>, select the workspace dropdown and select <bpt id="p2">**</bpt>Manage workspaces<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、<bpt id="p1">**</bpt>ソース管理エクスプローラー<ept id="p1">**</ept>を開き、ワークスペース ドロップダウンを選択し、<bpt id="p2">**</bpt>ワークスペースの管理<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Select the application workspace, click <bpt id="p1">**</bpt>Edit,<ept id="p1">**</ept> then click <bpt id="p2">**</bpt>Advanced<ept id="p2">**</ept> and set the workspace to <bpt id="p3">**</bpt>Public workspace<ept id="p3">**</ept>.<bpt id="p4">[</bpt><ph id="ph1">![</ph>publicworkspace<ept id="p4">](./media/publicworkspace.png)](./media/publicworkspace.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション ワークスペースを選択して、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept> をクリックし、<bpt id="p2">**</bpt>詳細<ept id="p2">**</ept> をクリックしてワークスペースを <bpt id="p3">**</bpt>パブリック ワークスペース<ept id="p3">**</ept>.<bpt id="p4">[</bpt><ph id="ph1">![</ph>publicworkspace<ept id="p4">](./media/publicworkspace.png)](./media/publicworkspace.png)</ept> にせっていします</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
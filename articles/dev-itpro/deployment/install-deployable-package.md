<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="install-deployable-package.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>install-deployable-package.9e2665.773db05f4b98d30396f420525170d16cf90080aa.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>773db05f4b98d30396f420525170d16cf90080aa</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\deployment\install-deployable-package.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Install deployable packages from the command line</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド ラインからの配置可能パッケージのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic walks you through the steps for using the command line to apply either a binary update or an application (AOT) deployable package that was created in your development/build environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、開発環境またはビルド環境で作成されたバイナリ更新プログラムまたはアプリケーション (AOT) の展開可能パッケージのいずれかをコマンドラインを使用して適用する手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Install deployable packages from the command line</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド ラインからの配置可能パッケージのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic walks you through the steps for using the command line to apply either a binary update or an application (AOT) deployable package that was created in your development or build environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、開発環境またはビルド環境で作成されたバイナリ更新プログラムまたはアプリケーション (AOT) の展開可能パッケージのいずれかをコマンドラインを使用して適用する手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For most types of environments, you can apply a deployable package to an environment directly from Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどのタイプの環境については、配置可能パッケージを Microsoft Dynamics  Lifecycle Services (LCS) から直接環境に適用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For more information, see <bpt id="p1">[</bpt>Apply a deployable package on a system<ept id="p1">](apply-deployable-package-system.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>システムで配置可能パッケージの適用<ept id="p1">](apply-deployable-package-system.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Therefore, this topic applies primarily to environment types that don't support the application of updates via LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、このトピックは主に、LCS による更新の適用をサポートしていない環境タイプに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Examples include local development environments (downloadable virtual hard disks [VHDs]), multi-box development/test environments in Microsoft Azure (LCS Partner and trial projects), and build environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例としては、Microsoft Azure のローカル開発環境 (ダウンロード可能な仮想ハード ディスク [VHD])、マルチボックス開発/テスト環境 (LCS パートナーおよび試用プロジェクト) およびビルド環境があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>However, you can also use this topic any time that you want to install deployable packages by using the command line instead of LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、LCS ではなくコマンド ラインを使用して展開可能パッケージをインストールする場合は、いつでもこのトピックを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Key concepts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な概念</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source><bpt id="p1">**</bpt>Deployable package<ept id="p1">**</ept> – A deployable package is a unit of deployment that can be applied to any environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>配置可能パッケージ<ept id="p1">**</ept> - 配置可能パッケージとは、任意の環境に適用できる配置の単位です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It can consist of a binary hotfix to the runtime components of Application Object Server (AOS), an updated application package, or a new application package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS)、更新されたアプリケーション パッケージ、または新しいアプリケーション パッケージのランタイム コンポーネントに対するバイナリの修正プログラムで構成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>AXUpdateInstaller<ept id="p1">**</ept> – AXUpdateInstaller is an executable program that is bundled in the deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AXUpdateInstaller<ept id="p1">**</ept> - AXUpdateInstaller は実行可能プログラムで、配置可能パッケージにバンドルされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>When the package is downloaded to a computer, the installer is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージがコンピューターにダウンロードされると、インストーラーを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Runbook<ept id="p1">**</ept> – The deployment runbook is a series of steps that is generated and used to apply the deployable package to the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Runbook<ept id="p1">**</ept> – 展開ランブックは展開可能なパッケージを対象となる環境に適用させるために生成され、使われる一連の手順です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Some of the steps are automated, and some are manual.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップの一部が自動化され、一部は手動です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>AXUpdateInstaller enables these steps to be run one at a time and in the correct order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXUpdateInstaller は、これらの手順を一度に 1 つずつ正しい順序で実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Install an application (AOT) deployable package on a development environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境でのアプリケーション (AOT) 配置可能パッケージのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>An AOT deployable package is a package that contains customizations and extensions to your application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT 配置可能パッケージはアプリケーションのカスタマイズおよび拡張機能を含むパッケージです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>If you want to use the command line just to install an AOT deployable package on a development or demo environment, follow the instructions in this section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発またはデモ環境で AOT 配置可能パッケージをインストールするためだけにコマンド ラインを使用する場合、このセクションの指示に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You can then skip the rest of this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックの残りをスキップすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>On the virtual machine (VM), download the zip file for the deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想マシン (VM) で、配置可能パッケージの zip ファイルをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Make sure that the zip file is stored in a non-user folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非ユーザー フォルダーに zip ファイルが保存されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>After you download the zip file, right-click it, and then select <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ZIP ファイルをダウンロードした後、右クリックし<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Then, in the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> dialog box, on the <bpt id="p2">**</bpt>General<ept id="p2">**</ept> tab, select <bpt id="p3">**</bpt>Unblock<ept id="p3">**</ept> to unlock the files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ダイアログ ボックスの <bpt id="p2">**</bpt>全般<ept id="p2">**</ept> タブで、<bpt id="p3">**</bpt>ブロック解除<ept id="p3">**</ept> を選択してファイルのロックを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Extract the files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルを抽出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Open a Command Prompt window, and go to the folder where you extracted the deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド プロンプト ウィンドウを開き、配置可能パッケージを展開したフォルダーに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The <bpt id="p1">**</bpt>devinstall<ept id="p1">**</ept> option installs the AOT deployable package on the VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>devinstall<ept id="p1">**</ept> オプションは、AOT の可能なパッケージを VM にインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>As of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with platform update 12, the <bpt id="p1">**</bpt>devinstall<ept id="p1">**</ept> option doesn't require that you be an administrator on the VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition のプラットフォーム更新プログラム 12 では、<bpt id="p1">**</bpt>devinstall<ept id="p1">**</ept> オプションを使用するには VM の管理者である必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>This command doesn't run database synchronization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドは、データベース同期を実行しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>You must run database synchronization from Microsoft Visual Studio after you install the deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能なパッケージをインストールした後、Microsoft Visual Studio からデータベースの同期を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Collect topology configuration data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トポロジ コンフィギュレーション データを収集する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In LCS, on the <bpt id="p1">**</bpt>Environment<ept id="p1">**</ept> page, select the name of a VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS で、<bpt id="p1">**</bpt>環境<ept id="p1">**</ept>ページの VM の名前を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Establish a Remote Desktop connection to the VM by using the user name and password that are provided on the <bpt id="p1">**</bpt>Environment<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境<ept id="p1">**</ept>ページで提供されているユーザー名とパスワードを使用して、VM へのリモート デスクトップの接続を確立します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>On the VM, download the zip file for the deployable package from LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM で、LCS から配置可能パッケージの zip ファイルをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Make sure that the zip file is stored in a non-user folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非ユーザー フォルダーに zip ファイルが保存されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>After you download the zip file, right-click it, and then select <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ZIP ファイルをダウンロードした後、右クリックし<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Then, in the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> dialog box, on the <bpt id="p2">**</bpt>General<ept id="p2">**</ept> tab, select <bpt id="p3">**</bpt>Unblock<ept id="p3">**</ept> to unlock the files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ダイアログ ボックスの <bpt id="p2">**</bpt>全般<ept id="p2">**</ept> タブで、<bpt id="p3">**</bpt>ブロック解除<ept id="p3">**</ept> を選択してファイルのロックを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Extract the files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルを抽出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In the folder where you extracted the deployable package, find and open the file that is named <bpt id="p1">**</bpt>DefaultTopologyData.xml<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージを展開したフォルダーで、<bpt id="p1">**</bpt>DefaultTopologyData.xml<ept id="p1">**</ept> というファイルを検索して開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>You must specify the VM name and the installed components in this file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルには、VM 名とインストール済みコンポーネントを指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>To specify the VM name, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM 名を指定するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>In File Explorer, right-click <bpt id="p1">**</bpt>This PC<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル エクスプローラーで、<bpt id="p1">**</bpt>この PC<ept id="p1">**</ept> を右クリックしてから、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In the system properties, find and make a note of the computer name (for example, <bpt id="p1">**</bpt>AOS-950ed2c3e7b<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム プロパティで、コンピューター名を検索して記録します (たとえば、<bpt id="p1">**</bpt>AOS 950ed2c3e7b<ept id="p1">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In the DefaultTopologyData.xml file, replace the machine name with the computer name that you found in the previous step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DefaultTopologyData.xml ファイルで、前の手順で示されているコンピューター名にマシン名を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To specify the installed components, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールされたコンポーネントを指定するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Open a Command Prompt window as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者としてコマンド プロンプト ウィンドウを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Go to the extracted folder, and run the following command to see a list of all the components that are installed on the computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開したフォルダーに移動し、コンピューターにインストールされているすべてのコンポーネントの一覧を表示するため、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Update the DefaultTopologyData.xml file with the list of components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネントの一覧で DefaultTopologyData.xml ファイルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>When you've finished specifying the VM name and the installed components, the DefaultTopologyData.xml file should resemble the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM 名とインストールされているコンポーネントの指定が完了したら、DefaultTopologyData.xml ファイルは次の図のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Topology configuration data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トポロジ構成データ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Repeat steps 1 through 4 for every other VM that is listed on the <bpt id="p1">**</bpt>Environment<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境<ept id="p1">**</ept> ページに記載されているその他のすべて VM に対して 手順 1 ～ 4 を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Generate a runbook from the topology</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トポロジから Runbook を生成します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Based on the topology information in the DefaultTopologyData.xml file, you must generate the runbook file that will provide step-by-step instructions for updating each VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DefaultTopologyData.xml ファイルのトポロジの情報に基づいて、各 VM の更新手順を示す Runbook ファイルを生成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>On any VM, run the following command to generate the runbook.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての VM で、次のコマンドを実行して Runbook を生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Here is an explanation of the parameters that are used in this command:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドで使用されるパラメータの説明を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt><ph id="ph1">\[</ph>runbookID<ph id="ph2">\]</ph><ept id="p1">**</ept>– A parameter that is specified by the developer who applies the deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\[</ph>runbookID<ph id="ph2">\]</ph><ept id="p1">**</ept>- 配置可能パッケージを適用する開発者が指定するパラメータ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">**</bpt><ph id="ph1">\[</ph>topologyFile<ph id="ph2">\]</ph><ept id="p1">**</ept>– The path of the DefaultTopologyData.xml file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\[</ph>topologyFile<ph id="ph2">\]</ph><ept id="p1">**</ept>- DefaultTopologyData.xml ファイルのパス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt><ph id="ph1">\[</ph>serviceModelFile<ph id="ph2">\]</ph><ept id="p1">**</ept>– The path of the DefaultServiceModelData.xml file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\[</ph>serviceModelFile<ph id="ph2">\]</ph><ept id="p1">**</ept>- DefaultServiceModelData.xml ファイルのパス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt><ph id="ph1">\[</ph>runbookFile<ph id="ph2">\]</ph><ept id="p1">**</ept>– The name of the runbook file to generate (for example, <bpt id="p2">**</bpt>AOSRunbook.xml<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\[</ph>runbookFile<ph id="ph2">\]</ph><ept id="p1">**</ept> - 生成する Runbook クファイルの名前 (たとえば、<bpt id="p2">**</bpt>AOSRunbook.xml<ept id="p2">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>The runbook provides the sequence of steps that must be run to update the environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Runbook には、環境を更新するために実行する必要がある一連のステップが備わっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The following illustration shows an example of a runbook file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、Runbook ファイルの例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Each step in a runbook is associated with an ID, a machine name, and step execution details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Runbook の各ステップは、ID、マシン名、およびステップ実行の詳細に関連付けられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Example of a runbook file<ept id="p1">](./media/runbook-steps-1024x624.jpg)](./media/runbook-steps.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Runbook ファイルの例<ept id="p1">](./media/runbook-steps-1024x624.jpg)](./media/runbook-steps.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Install a deployable package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>On the first machine (VM) that is listed in the runbook file, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Runbook ファイルに記載されている最初のマシン (VM) で、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Import the runbook by running the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを実行して、Runbook をインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Verify the runbook.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Runbook を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Run the runbook.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">runbook を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>AXUpdateInstaller updates the runbook file after each step is run on a VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXUpdateInstaller は、各ステップが VM で実行された後に Runbook ファイルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>The runbook also logs information about each step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Runbook には、各ステップに関する情報も記録されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>For manual steps, follow the instructions, and then run the following command to mark the step as completed in the runbook.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動ステップについては、指示に従い、Runbook でステップを完了済とマークする以下のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If errors occur during any step, debug the script or the instructions in the step, and update accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どの段階中でもエラーが発生した場合は、そのステップのスクリプトまたは指示をデバッグし、それに応じて更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Export the runbook.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Runbook をエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Repeat step 1 on every other VM that is listed in the runbook file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Runbook ファイルに記載されているその他のすべての VM で手順 1 を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>For one-box environments, such as development, build, and demo environments, there is only one VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 ボックス環境では、開発、構築、およびデモ環境など、1 つの VM のみがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Verify installation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールの確認</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Run the following command to verify that the new updates are installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい更新プログラムがインストールされていることを確認するには、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>View the runbook to see the completed steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Runbook を表示して、完了したステップを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Here is an example of a runbook file where the steps have been completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順が完了した runbook ファイルの例を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Example of completed steps in a runbook<ept id="p1">](./media/image013-1024x978.png)](./media/image013.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>runbook の完了したステップの例<ept id="p1">](./media/image013-1024x978.png)](./media/image013.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Backup the runbook file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Runbook ファイルをバックアップします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>After all the steps in the runbook are completed and you've exported the runbook, save the file outside the computer for future reference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Runbook のすべての手順を完了した後、Runbook をエクスポートし、後で参照できるようにファイルをコンピューターの外部に保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>For example, you might have to use the runbook file in these situations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、このような状況で Runbook ファイルを使用する必要が生じる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>You must analyze the downtime requirements for production, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産などのダウンタイム要件を分析する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>You must send the file to Microsoft because a deployable package can't be installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージをインストールすることはできないため、マイクロソフトにファイルを送信する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Troubleshooting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>If any step in the runbook fails, you can rerun it by running the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">runbook の段階で失敗した場合は、次のコマンドを実行して再実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>To prevent version mismatch or downgrade, or installation of the same deployable package, run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョンの不一致やダウングレード、または同じ展開可能パッケージのインストールを防止するには、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>To verify database synchronization, in the <bpt id="p1">**</bpt>aosservce<ph id="ph1">\\</ph>scripts<ph id="ph2">\\</ph><ept id="p1">**</ept> folder, find and open the <bpt id="p2">**</bpt>dbsync.error.txt<ept id="p2">**</ept> file, and look for any errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの同期を確認するには、&lt;<bpt id="p1">**</bpt>aosservce<ph id="ph1">\\</ph>scripts<ph id="ph2">\\</ph><ept id="p1">**</ept> フォルダー内の <bpt id="p2">**</bpt>dbsync.error.txt<ept id="p2">**</ept> ファイルを見つけて開き、エラーを探します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
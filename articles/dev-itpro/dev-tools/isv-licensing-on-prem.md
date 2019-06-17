<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="isv-licensing-on-prem.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>isv-licensing-on-prem.e09ad9.a78dbef13408bc4256138198add914cf7d3932e2.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>a78dbef13408bc4256138198add914cf7d3932e2</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\isv-licensing-on-prem.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Independent software vendor (ISV) licensing (on-premises)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">独立系ソフトウェア ベンダー (ISV) ライセンス (オンプレミス)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the independent software vendor (ISV) licensing feature for on-premises environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、オンプレミス環境における独立系ソフトウェア ベンダー (ISV) のライセンス機能について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Independent software vendor (ISV) licensing (on-premises)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">独立系ソフトウェア ベンダー (ISV) ライセンス (オンプレミス)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to import independent software vendor (ISV) licenses into an on-premises deployment of Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、独立系ソフトウェア ベンダー (ISV) ライセンスを Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置にインポートする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The process that is described in this topic is available only for customers who have on-premises environments that are deployed with Platform update 12 or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックで説明するプロセスは、プラットフォーム更新プログラム 12 以降で展開されているオンプレミス環境のユーザーのみ利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For general information about the benefits of ISV licensing, information about how to enable licensing for your solution, and other information that is related to self-signed certificates, see <bpt id="p1">[</bpt>ISV licensing<ept id="p1">](isv-licensing.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV ライセンスの福利厚生についての一般情報、ソリューションのライセンスを有効にする方法についての情報、および自己署名証明書に関連するその他の情報については、<bpt id="p1">[</bpt>ISV ライセンス<ept id="p1">](isv-licensing.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Before you import the ISV license file into your on-premises environment, verify that the following prerequisites are met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス環境に ISV ライセンス ファイルをインポートする前に、次の前提条件が満たされていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The most recent version of the local agent was used when the environment was deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新のバージョンのローカル エージェントは、環境が配置されたときに使用されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The environment is deployed with Platform update 12, and all hotfixes for Platform update 12 are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境はプラットフォーム更新プログラム 12 で配置され、プラットフォーム更新プログラム 12 のすべての修正プログラムが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This step is mandatory because Microsoft has released a fix for an ISV licensing scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft が ISV ライセンス シナリオの修正プログラムをリリースしたため、このステップは必須です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To get the latest set of hotfixes, use the tiles on the <bpt id="p1">**</bpt>Environment details<ept id="p1">**</ept> page in Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新の修正プログラムを入手するには、Microsoft Dynamics Lifecycle Services (LCS) の <bpt id="p1">**</bpt>環境の詳細<ept id="p1">**</ept>ページでタイルを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Before you import the ISV license, the environment must be deployed, and the Application Object Server (AOS) service must be running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV ライセンスをインポートする前に、環境を展開し、Application Object Server (AOS) サービスを実行している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Before you import the ISV license, the ISV solution must be applied to the on-premises environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV ライセンスをインポートする前に、ISV ソリューションをオンプレミス環境に適用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The ISV solution can be applied to an on-premises environment during the deployment flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV ソリューションは、配置フロー中に設置環境に適用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Alternatively, you can use the <bpt id="p1">**</bpt>Apply updates<ept id="p1">**</ept> flow in LCS to apply the ISV solution as a post-deployment step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、LCS の<bpt id="p1">**</bpt>更新プログラムの適用<ept id="p1">**</ept>フローを使用して配置後のステップとして ISV ソリューションを適用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>If the ISV solution isn't applied before you import the license, the customizations won't be enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンスをインポートする前に、ISV ソリューションが適用されていない場合、カスタマイズを使用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Import licenses</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンスのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following procedure can be used for a sandbox environment or a production environment that is deployed in an on-premises project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス プロジェクトに配置されているサンドボックス環境または本番環境では、次の手順を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Because import of an ISV license requires downtime, no business transactions can be performed in the environment during import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV ライセンスのインポートにはダウンタイムが必要なため、インポート時に環境内で業務トランザクションを実行することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>When you complete the import, make sure that no one is using the system, and that an official downtime notice has been communicated to all the users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートを完了したら、だれもシステムを使用していないことと、公式ダウンタイム通知システムがすべてのユーザーに通知済みであることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Collect the tenant name and ID for the customer to issue the license to:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンスを発行する顧客のテナント名と ID を収集します:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Connect to the instance of Service Fabric Explorer where the environment is hosted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境がホストされている Service Fabric Explorer のインスタンスに接続します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Go to <bpt id="p1">**</bpt>Clusters<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Applications<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>AXSFType<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>fabric:<ph id="ph4">\\</ph>AXSF<ept id="p4">**</ept>, and then, on the right page, select the <bpt id="p5">**</bpt>Details<ept id="p5">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クラスタ<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アプリケーション<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>AXSFType<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>ファブリック:<ph id="ph4">\\</ph>AXSF<ept id="p4">**</ept> の順に移動し、次に右のページで、<bpt id="p5">**</bpt>詳細<ept id="p5">**</ept>タブを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>In the <bpt id="p1">**</bpt>Parameters<ept id="p1">**</ept> table, find the values for the <bpt id="p2">**</bpt>License<ph id="ph1">\_</ph>TenantDomainGuid<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Licence<ph id="ph2">\_</ph>TenantId<ept id="p3">**</ept> keys.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パラメーター<ept id="p1">**</ept> テーブルで <bpt id="p2">**</bpt>License<ph id="ph1">\_</ph>TenantDomainGuid<ept id="p2">**</ept> および <bpt id="p3">**</bpt>Licence<ph id="ph2">\_</ph>TenantId<ept id="p3">**</ept> キーの値を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Generate a license for the customer (tenant ID and name), and sign the license by using the certificate's private key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客のライセンス (テナント ID と名前) を生成し、証明書のプライベート キーを使用してライセンスを登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The following parameters must be passed to the AXUtil <bpt id="p1">**</bpt>genlicense<ept id="p1">**</ept><ph id="ph1"> </ph>command to create the license file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンス ファイルを作成するには、次のパラメーターを  AXUtil <bpt id="p1">**</bpt>genlicense<ept id="p1">**</ept><ph id="ph1"> </ph> コマンドに渡す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The command will generate an XML file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンドは XML ファイルを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Parameter name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The name of the license file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンス ファイルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>licensecode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">licensecode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The name of the license code from Microsoft Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio のライセンス コードの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>certificatepath</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">certificatepath</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The path of the certificate's private key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書のプライベート キーのパス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>password</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パスワード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The password of the certificate's private key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書のプライベート キーのパスワード。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>customer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The customer's tenant name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客のテナント名。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>serialnumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">serialnumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The customer's tenant ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客のテナント ID。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>expirationdate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">expirationdate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Optional: The expiration date of the license.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: ライセンスの有効期限。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>usercount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">usercount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Optional: The number that can be required for the custom validation logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: カスタム検証ロジックに必要となる可能性がある数値。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>This number can be the number of users, but it isn't limited to users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この数はユーザー数が可能ですが、ユーザーに限定されるものではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Here is an example of the command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンドの例を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Copy the licenses that are generated to a folder on one of the machines that is running fabric:/AXSF, and verify that fabric:/AXSF is healthy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたライセンスを fabric:/AXSF を実行しているマシンの 1 つのフォルダーにコピーし、fabric:/AXSF が正常であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Run the <bpt id="p1">**</bpt>Import-LicensePackage.ps1<ept id="p1">**</ept> script from one of the AOS machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS コンピューターのいずれかから <bpt id="p1">**</bpt>Import-LicensePackage.ps1<ept id="p1">**</ept> スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>You can find this script in the latest <bpt id="p1">**</bpt>Deployment scripts<ept id="p1">**</ept> folder on the <bpt id="p2">**</bpt>Model<ept id="p2">**</ept> tab in the Shared asset library in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このスクリプトは、LCS 内の共有アセット ライブラリにある  <bpt id="p2">**</bpt>モデル<ept id="p2">**</ept> タブの最新の <bpt id="p1">**</bpt>配置スクリプト<ept id="p1">**</ept> フォルダーで見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Here is a list of the parameters that you must pass to the script:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトに渡す必要があるパラメータの一覧を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>LicenseFilesPath<ept id="p1">**</ept> – The path of a folder that contains the license files that must be imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>LicenseFilesPath<ept id="p1">**</ept> – インポートする必要があるライセンス ファイルを含むフォルダーのパス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>SqlUser<ept id="p1">**</ept> – The same user who is specified in the credentials.json file to run the AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SqlUser<ept id="p1">**</ept> – AOS を実行する credentials.json ファイルに指定されている同じユーザー。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source><bpt id="p1">**</bpt>SqlPassword<ept id="p1">**</ept> – The password that can be used to connect to SQL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SqlPassword<ept id="p1">**</ept> – SQL への接続に使用できるパスワード。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>EnvironmentConfigPath<ept id="p1">**</ept> – The configuration file for the environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EnvironmentConfigPath<ept id="p1">**</ept> - 環境のコンフィギュレーション ファイル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This file is named config.json and is located under the agent share in a folder that has the format wp<ph id="ph1">\\</ph><ph id="ph2">&amp;lt;</ph>environment-name<ph id="ph3">&amp;gt;</ph><ph id="ph4">\\</ph>StandaloneSetup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルの名前は、config.json で、wp <ph id="ph1">\\</ph><ph id="ph2">&amp;lt;</ph> 環境名 <ph id="ph3">&amp;gt;</ph><ph id="ph4">\\</ph> StandaloneSetup という形式のフォルダー内のエージェント共有の下にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>After the command is run, log files are generated for each license file that is processed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンドを実行した後、ログ ファイルは、処理されるライセンス ファイルごとに生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The names of the log files are in the format {license<ph id="ph1">\_</ph>file<ph id="ph2">\_</ph>name}.output.log and {license<ph id="ph3">\_</ph>file<ph id="ph4">\_</ph>name}.error.log.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ログ ファイルの名前は、{license<ph id="ph1">\_</ph>file<ph id="ph2">\_</ph>name}.output.log 形式と {license<ph id="ph3">\_</ph>file<ph id="ph4">\_</ph>name}.error.log 形式です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>The logs that are generated during database synchronization are located in files that are structured like dbsync.output.log and dbsync.error.log.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース同期中に生成されるログは、dbsync.output.log および dbsync.error.log のような構造のファイルにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>When the script has been run successfully, validate that the configuration key has been imported and enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトが正常に実行されたとき、コンフィギュレーション キーがインポートされて有効になっていることを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>In the product, the corresponding configuration key will be available and enabled on the<bpt id="p1"> **</bpt>License configuration<ept id="p1">**</ept><ph id="ph1"> </ph>page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品では、対応するコンフィギュレーション キーは、<bpt id="p1"> **</bpt>ライセンス コンフィギュレーション<ept id="p1">**</ept><ph id="ph1"> </ph> ページで使用可能になり、有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>By default, the configuration is enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、コンフィギュレーションが有効です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>For example, if you added a configuration key that is named ISVConfigurationKey1, it will appear in the list of configuration keys.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ISVConfigurationKey1 と呼ばれるコンフィギュレーション キーを追加した場合、コンフィギュレーション キーの一覧に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>When the configuration key is enabled, the changes in the ISV solution will be visible in the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーが有効になると、ISV ソリューションの変更は製品に表示されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
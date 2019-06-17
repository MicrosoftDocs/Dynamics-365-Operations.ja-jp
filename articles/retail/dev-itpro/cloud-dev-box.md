<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cloud-dev-box.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cloud-dev-box.5986aa.982dd5d02bca9faedbf952575726e62330452322.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>982dd5d02bca9faedbf952575726e62330452322</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>0b9856cfc175f791898af47aa0d6fc6ac63873b0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/31/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\cloud-dev-box.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Development in cloud-hosted development environments without admin access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者アクセスのないクラウド ホスト開発環境での開発</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic demonstrates the configuration steps for Retail developers working on cloud-hosted development machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、クラウドでホストされている開発マシンで作業している Retail 開発者向けのコンフィギュレーション手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Development in cloud-hosted development environments without admin access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者アクセスのないクラウド ホスト開発環境での開発</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>As of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, Platform update 12, customers will no longer have access to virtual machine (VM) administrator accounts on development or build environments that are running in Microsoft subscriptions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 12 の時点で、顧客は Microsoft サブスクリプションで実行中の開発またはビルド環境で仮想マシン (VM) 管理者アカウントにアクセスできなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This restriction only applies to new deployments of Platform update 12 (or newer) environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この制限は、プラットフォーム更新 12 (またはそれ以降) 環境の新しい展開にのみ適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Environments that were deployed before this update, and  have been updated to Platform update 12, will still have administrator access.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この更新プログラムの前に展開され、プラットフォーム更新プログラム 12 に更新された環境では、引き続き管理者アクセス権が与えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You can use a remote desktop (RDP) to access these restricted environments using the non-admin user provided on the Lifecycle Services (LCS) environment page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップ (RDP) を使用して、Lifecycle Services (LCS) 環境ページに用意されている非管理ユーザーを使用するこれらの制限された環境にアクセスすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For more information about environments that don't allow administrator access, see <bpt id="p1">[</bpt>Development and build VMs that don't allow administrator access FAQ<ept id="p1">](../../dev-itpro/sysadmin/VMs-no-admin-access.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者アクセスを許可しない環境の詳細については、<bpt id="p1">[</bpt>管理者アクセスを許可しない開発用 およびビルド用 VM に関するよく寄せられる質問<ept id="p1">](../../dev-itpro/sysadmin/VMs-no-admin-access.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>If you deploy an environment using Microsoft Azure subscription in Lifecycle Services (LCS), then you will not have admin access in this environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) で Microsoft Azure サブスクリプションを使用する環境を配置した場合、この環境では管理者アクセス権がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If you need admin access in your environment, use your Azure subscription and deploy the environment using LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ご使用の環境で管理者アクセス権が必要な場合は、Azure サブスクリプションを使用し、LCS を使用して環境を配置してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can also use the downloadable VHD and deploy it in your Azure virtual machine (VM) or host it locally to get full admin access.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンロード可能な VHD を使用して Azure 仮想マシン (VM) に配置したり、ローカルでホストしたりして完全な管理者権限を取得することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>If you don’t have admin access in the environment, you will not be able to test and debug using Modern POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境に管理者アクセス権がない場合、Modern POS を使用してテストおよびデバッグすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>You can still do all retail customization for POS if you are testing the customization, you must use Cloud POS in that environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズをテストしている場合は、POS のすべての小売カスタマイズを行うことができます。その環境でクラウド POS を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>From a customization perspective, there is no difference between Cloud POS and Modern POS - any customization will work both in Cloud POS and Modern POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズの観点からは、Cloud POS および Modern POS に違いはありません - どのカスタマイズも Cloud POS および Modern POS の両方で機能します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>There is no additional logic or code for customization completed in Cloud POS in order to work in Modern POS or vice versa, unless you added logic that is browser-specific or UWP app- specific for Hardware and other scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェアおよびその他のシナリオの、ブラウザー固有もしくは UWP アプリ固有のロジックを追加しない限り、Modern POS か、その逆で作業するために Cloud POS で完了したカスタマイズの追加のロジックやコードはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Another option is to do all development work in the environment using Modern POS and test it in some other environment where you have admin access to install MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別のオプションは、Modern POS を使用した環境ですべての開発を実行し、MPOS をインストールするための管理者アクセス権限を持つ他の環境でテストすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In most cases, you should be able to test using Cloud POS, expect if you want to test for offline scenarios.</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">ほとんどの場合はクラウド POS を使用してテストすることが可能で、オフラインのシナリオをテストするか予想します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>If you want to test offline scenarios, you can create a Modern POS installer using the build script, and then test it in your test environment or some other POS registers.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">オフライン シナリオをテストする場合は、ビルド スクリプトを使用して Modern POS インストーラーを作成し、テスト環境またはその他のいくつかの POS レジスターでテストできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>If you are using Cloud POS for development, set up the following configuration before opening the Cloud POS project<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クラウド POS を開発に使用している場合は、クラウド POS プロジェクトを開く前に以下の設定を行います<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Open Visual Studio and click <bpt id="p1">**</bpt>View<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を開き、<bpt id="p1">**</bpt>表示<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>アプリケーション エクスプ ローラー<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Wait for Internet Information Services (IIS) Express to start with all the Retail websites deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット インフォメーション サービス (IIS) Express が配置されているすべての Retail Web サイトで開始するまで待ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>You should see the IIS tray icon in the task bar with all the Retail websites running, such as Cloud POS and Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク バーに IIS トレー アイコンが表示され、Cloud POS や Retail Server など、Retail のウェブサイトがすべて表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>To debug CRT/RS extensions, attach the CRT/RS project to the IIS Express process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT/RS 拡張をデバッグするには、CRT/RS プロジェクトを IIS Express プロセスに添付します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>When you open the Cloud POS project from the Retail SDK, IIS Express may fail with the following error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK からクラウド POS プロジェクトを開くと、次のエラーで IIS Express が失敗することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>To resolve this issue<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>この問題を解決するには<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Close Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Copy the <bpt id="p1">**</bpt>aspnet.config<ept id="p1">**</ept> and <bpt id="p2">**</bpt>redirection.config<ept id="p2">**</ept> files to <bpt id="p3">**</bpt>%userprofile%\Documents\IISExpress\config<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>aspnet.config<ept id="p1">**</ept> および <bpt id="p2">**</bpt>redirection.config<ept id="p2">**</ept> ファイルを <bpt id="p3">**</bpt>%userprofile%\Documents\IISExpress\config<ept id="p3">**</ept> にコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Open the <bpt id="p1">**</bpt>applicationhost.config<ept id="p1">**</ept> file in the <bpt id="p2">**</bpt>%userprofile%\Documents\IISExpress\config<ept id="p2">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>%userprofile%\Documents\IISExpress\config<ept id="p2">**</ept> フォルダー内の <bpt id="p1">**</bpt>applicationhost.config<ept id="p1">**</ept> ファイルを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>In <bpt id="p1">**</bpt>applicationhost.config<ept id="p1">**</ept>, change the physcialPath of RetailCloudPos to point to your SDK location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>applicationhost.config<ept id="p1">**</ept> で、RetailCloudPos の physcialPath を変更し、SDK の場所をポイントするようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For example, physicalPath="K:\RetailSDK\POS\Web".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、physicalPath="K:\RetailSDK\POS\Web" です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The overall section will look like the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全体的なセクションは、次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Save the changes to <bpt id="p1">**</bpt>applicationhost.config<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を <bpt id="p1">**</bpt>applicationhost.config<ept id="p1">**</ept> に保存します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Rename the <bpt id="p1">**</bpt>%userprofile%\Documents\IISExpress\config<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>%userprofile%\Documents\IISExpress\config<ept id="p1">**</ept> フォルダーの名前を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Do not delete the files because you will copy the                      <bpt id="p1">**</bpt>applicationhost.config<ept id="p1">**</ept> file to a new location in <bpt id="p2">**</bpt>step 8<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>ステップ 8<ept id="p2">**</ept> の新しい場所に <bpt id="p1">**</bpt>applicationhost.config<ept id="p1">**</ept> ファイルをコピーするため、ファイルを削除しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Start Visual Studio again with the Cloud POS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Cloud POS プロジェクトに対して、Visual Studio を再度起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The <bpt id="p1">**</bpt>%userprofile%\Documents\IISExpress\config<ept id="p1">**</ept> folder will be recreated         with the default config files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>%userprofile%\Documents\IISExpress\config<ept id="p1">**</ept> フォルダーが、既定の構成ファイルを使用して再作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Copy the <bpt id="p1">**</bpt>applicationhost.config<ept id="p1">**</ept> file from the folder that you renamed in <bpt id="p2">**</bpt>step 6<ept id="p2">**</ept>, to the folder created in <bpt id="p3">**</bpt>step 7<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>applicationhost.config<ept id="p1">**</ept> ファイルを、<bpt id="p2">**</bpt>ステップ 6<ept id="p2">**</ept> で名前を変更したフォルダーから、<bpt id="p3">**</bpt>ステップ 7<ept id="p3">**</ept> で作成したフォルダーにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Right-click the Pos.Web project and click <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pos.Web プロジェクトを右クリックし、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, click the <bpt id="p2">**</bpt>Web<ept id="p2">**</ept> tab. Select the <bpt id="p3">**</bpt>Start URL radio<ept id="p3">**</ept> option and set the start URL as your Cloud POS URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>Web<ept id="p2">**</ept> タブをクリックします。<bpt id="p3">**</bpt>開始 URL<ept id="p3">**</ept> ラジオ オプションをオンにし、クラウド POS URL として開始 URL を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>For example, <ph id="ph1">`https://usnconeboxax1pos.cloud.onebox.dynamics.com`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<ph id="ph1">`https://usnconeboxax1pos.cloud.onebox.dynamics.com`</ph>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Save the changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Install the Developer topology prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者トポロジの前提条件のインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Cloud-hosted development environments do not include Typescript version 2.2.2 by default, and the default Windows host file does not contain the Cloud POS URL to use for local debugging.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド ホスト開発環境には Typescript バージョン 2.2.2 が既定で含まれておらず、既定の Windows ホスト ファイルにはローカル デバッグに使用するクラウド POS URLが含まれていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The <bpt id="p1">**</bpt>Developer topology prerequisites<ept id="p1">**</ept> package installs Typescript 2.2.2 and updates the Windows host file with your Cloud POS URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開発者トポロジの前提条件<ept id="p1">**</ept> パッケージは、Typescript 2.2.2 をインストールし、Cloud POS URL を使用して Windows ホスト ファイルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Deploying the package will take a few minutes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージの展開には数分かかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To install the Developer topology prerequisites:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者トポロジの前提条件をインストールするには、次のようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Go to Lifecycle Services (<ph id="ph1">https://lcs.dynamics.com)</ph> and sign in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (<ph id="ph1">https://lcs.dynamics.com)</ph> に移動しサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Under <bpt id="p1">**</bpt>Projects<ept id="p1">**</ept>, select the project where your dev environment is deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクト<ept id="p1">**</ept> で、開発環境が展開されているプロジェクトを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In the <bpt id="p1">**</bpt>More tools<ept id="p1">**</ept> section, click the <bpt id="p2">**</bpt>Asset library<ept id="p2">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加ツール<ept id="p1">**</ept> セクションで、<bpt id="p2">**</bpt>アセット ライブラリ<ept id="p2">**</ept> タイルをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Select <bpt id="p1">**</bpt>Software deployable package<ept id="p1">**</ept> for the Asset library type and click <bpt id="p2">**</bpt>Import<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アセット ライブラリ タイプとして <bpt id="p1">**</bpt>ソフトウェア配置可能パッケージ<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>インポート<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>In the <bpt id="p1">**</bpt>Shared asset library list<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Developer topology prerequisites<ept id="p2">**</ept> and click <bpt id="p3">**</bpt>Pick<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>共有アセット ライブラリ リスト<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>開発者トポロジの前提条件<ept id="p2">**</ept>を選択して<bpt id="p3">**</bpt>選択<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Go to the <bpt id="p1">**</bpt>Environments<ept id="p1">**</ept> section, and click your development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境<ept id="p1">**</ept>セクションに移動し、開発環境をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Click the <bpt id="p1">**</bpt>Maintain<ept id="p1">**</ept> tab and select <bpt id="p2">**</bpt>Apply updates<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>管理<ept id="p1">**</ept>タブをクリックし、<bpt id="p2">**</bpt>更新プログラムの適用<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Select <bpt id="p1">**</bpt>Developer topology prerequisites<ept id="p1">**</ept> and click <bpt id="p2">**</bpt>Apply<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開発者トポロジの前提条件<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>適用<ept id="p2">**</ept> をクリックします。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
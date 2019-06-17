<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="install-run-system-diagnostics-lcs.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>install-run-system-diagnostics-lcs.b562d2.d51f75f9ebbf42d6ce0125124463dae35d3084bd.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d51f75f9ebbf42d6ce0125124463dae35d3084bd</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\ax-2012\install-run-system-diagnostics-lcs.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Install and run System diagnostics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム診断のインストールと実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>In Microsoft Dynamics Lifecycle Services, System diagnostics includes an on-premises component that must be installed before you can use the service to discover Microsoft Dynamics AX environments and collect data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services では、Microsoft Dynamics AX 環境を検出してデータを収集するサービスが使用できるようになる前にインストールする必要があるオンプレミス コンポーネントがシステム診断に含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Install and run System diagnostics (AX 2012)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム診断のインストールと実行 (AX 2012)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Microsoft Dynamics Lifecycle Services, System diagnostics includes an on-premises component that must be installed before you can use the service to discover Microsoft Dynamics AX environments and collect data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services では、Microsoft Dynamics AX 環境を検出してデータを収集するサービスが使用できるようになる前にインストールする必要があるオンプレミス コンポーネントがシステム診断に含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Install the System diagnostics on-premises component</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム診断オンプレミス コンポーネントのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>To install the System diagnostics on-premises component, the following is required:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム診断オンプレミス コンポーネントをインストールするには、以下が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>A service account with specific permissions on the local computer and the Microsoft Dynamics AX business database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル コンピューターと Microsoft Dynamics AX ビジネス データベースに特定のアクセス許可を持つサービス アカウント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>An X509 certificate .</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X509 証明書です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>You can either use an existing certificate, or have the installer create one for you.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の証明書を使用するか、インストーラーにより作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Each X509 certificate is associated with a single project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 X509 証明書は、単一プロジェクトに関連付けられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Diagnostics from an environment can be uploaded to only one project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境からの診断は、1 つのプロジェクトにのみアップロードできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Microsoft .NET 4.5 or 4.5.1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft .NET 4.5 または 4.5.1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Configure the service account for System diagnostics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム診断用のサービス アカウントをコンフィギュレーションする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This section describes the permissions that are required for the service account that the Lifecycle Services Diagnostic Service (LCSDiagFXService.exe) runs as.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、Lifecycle Services 診断サービス (LCSDiagFXService.exe) が実行されるサービス アカウントに必要なアクセス許可について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The service account must be a domain account that is a user in Microsoft Dynamics AX and a member of the <bpt id="p1">**</bpt>BusinessConnector<ept id="p1">**</ept> role.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス アカウントは、Microsoft Dynamics AX のユーザーで、<bpt id="p1">**</bpt>BusinessConnector<ept id="p1">**</ept> ロールのメンバーであるドメイン アカウントである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>We strongly recommend that, if possible, the account be the same account used for the .NET Business Connector proxy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可能な場合、アカウントは、.NET Business Connector プロキシに使用する同じアカウントを使用することを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>For more information, see <bpt id="p1">[</bpt>Specify the .NET Business Connector proxy account<ept id="p1">](http://technet.microsoft.com/library/3e46dc0a-2ff4-4a06-ae61-041e52dcc774(AX.60).aspx)</ept> and <bpt id="p2">[</bpt>Assign users to security roles<ept id="p2">](http://technet.microsoft.com/library/214ee45b-5b99-4ea8-9454-f4297f68e38c(AX.60).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>.NET Business Connector プロキシ アカウントを指定<ept id="p1">](http://technet.microsoft.com/library/3e46dc0a-2ff4-4a06-ae61-041e52dcc774(AX.60).aspx)</ept> および <bpt id="p2">[</bpt>セキュリティ ロールにユーザーを割り当てる<ept id="p2">](http://technet.microsoft.com/library/214ee45b-5b99-4ea8-9454-f4297f68e38c(AX.60).aspx)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メモ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>If you reuse the .NET Business connector proxy account, you must still add it as a member of the <bpt id="p1">**</bpt>BusinessConnector<ept id="p1">**</ept> role.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NET Business Connector プロキシ アカウントを再利用する場合は、引き続きそれを <bpt id="p1">**</bpt>BusinessConnector<ept id="p1">**</ept> ロールのメンバーとして追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The service account must have read access to specific registry keys in the HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE hive on all of the computers that run AOS instances and host Microsoft Dynamics AX business databases, so that the Lifecycle Services Diagnostic Service can discover environments and collect data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services 診断サービスがデータを収集できるよう、サービス アカウントには、AOS インスタンスを実行し、Microsoft Dynamics AX ビジネス データベースをホストするすべてのコンピューター上の HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE ハイブ内の特定のレジストリ キーへの読み取りアクセスが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The service account must be a member of the <bpt id="p1">**</bpt>Event Log Readers<ept id="p1">**</ept> local group on each server in the environment, so that the Lifecycle Services Diagnostic Service can read the Windows event logs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス アカウントは、Lifecycle Services 診断サービスが Windows イベントログを読み取れるように、環境内の各サーバー上の<bpt id="p1">**</bpt>イベント ログ リーダー<ept id="p1">**</ept>のローカル グループのメンバーである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The service account must have read access to the Microsoft Dynamics AX business database (<bpt id="p1">**</bpt>db<ph id="ph1">\_</ph>datareader<ept id="p1">**</ept>), and must have VIEW SERVER STATE permission for the SQL Server instance, so that Lifecycle Services Diagnostic Service can run default dynamic management views in SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services 診断サービスが SQL Server で既定の動的管理ビューを実行できるよう、サービス アカウントには、Microsoft Dynamics AX ビジネス データベース (<bpt id="p1">**</bpt>db<ph id="ph1">\_</ph>datareader<ept id="p1">**</ept>) への読み取りアクセスと、SQL Server インスタンスに対して VIEW SERVER STATE 権限が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Configure read permissions to the registry</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジストリへの読み取りアクセス許可をコンフィギュレーションする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>On each server in your environment that hosts an AOS instance or Microsoft Dynamics AX SQL Server business database, you must grant read access to a registry key in the HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE hive to the service account for the System diagnostics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS インスタンスまたは Microsoft Dynamics AX SQL Server ビジネス データベースをホストする環境内の各サーバーで、HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE ハイブ内のレジストリ キーに対する読み取りアクセス権を、システム診断のサービス アカウントに付与する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Caution<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注意<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The following procedure includes editing the Windows Registry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順には、Windows レジストリの編集が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Editing the registry incorrectly can cause serious problems that may require you to reinstall Windows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジストリを誤って編集すると深刻な問題が発生し、Windows の再インストールが必要になることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Microsoft cannot guarantee that problems resulting from incorrectly editing the registry can be solved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、レジストリの編集によって発生した問題の解決については保証できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>solved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解決済み。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>You should make a backup copy of the registry files (System.dat and User.dat) before you edit the registry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジストリを編集する前に、レジストリ ファイル (System.dat と User.dat) のバックアップを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>To grant access to collect data from the Windows registry on the server that hosts the SQL Server business database:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server ビジネス データベースをホストするサーバー上の Windows レジストリからデータを収集するためのアクセスを許可するには、次のようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Click <bpt id="p1">**</bpt>Start<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Run<ept id="p2">**</ept>, type <bpt id="p3">**</bpt>regedit<ept id="p3">**</ept>, and then press <bpt id="p4">**</bpt>Enter<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開始<ept id="p1">**</ept>、<bpt id="p2">**</bpt>実行<ept id="p2">**</ept>をクリックし、<bpt id="p3">**</bpt>regedit<ept id="p3">**</ept> と入力し、次に <bpt id="p4">**</bpt>Enter<ept id="p4">**</ept> を押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Expand <bpt id="p1">**</bpt>HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE<ept id="p1">**</ept>, navigate to the subkey <bpt id="p2">**</bpt>System\CurrentControlSet\Control\PriorityControl<ept id="p2">**</ept>, right-click it and select <bpt id="p3">**</bpt>Permissions<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE<ept id="p1">**</ept> を展開し、サブキー <bpt id="p2">**</bpt>System\CurrentControlSet\Control\PriorityControl<ept id="p2">**</ept> で移動し、右クリックおよび<bpt id="p3">**</bpt>アクセス許可<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Add the user that you want to associate with the Lifecycle Services Diagnostic Service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services 診断サービスに関連付ける必要のあるユーザーを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Select the user that you added, and then allow read permissions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加したユーザーを選択し、読み取りアクセス許可を許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Click <bpt id="p1">**</bpt>Advanced Security Settings<ept id="p1">**</ept>, and then ensure that the permissions are inherited by the child objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セキュリティの詳細設定<ept id="p1">**</ept>をクリックし、アクセス許可が子オブジェクトによって継承されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>To grant access to collect data from the Windows registry on a server that hosts one or more AOS instances:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つ以上の AOS インスタンスをホストするサーバー上の Windows レジストリからデータを収集するためのアクセスを許可するには、次のようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Click <bpt id="p1">**</bpt>Start<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Run<ept id="p2">**</ept>, type <bpt id="p3">**</bpt>regedit<ept id="p3">**</ept>, and press <bpt id="p4">**</bpt>Enter<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開始<ept id="p1">**</ept>、<bpt id="p2">**</bpt>実行<ept id="p2">**</ept>をクリックし、<bpt id="p3">**</bpt>regedit<ept id="p3">**</ept> と入力し <bpt id="p4">**</bpt>Enter<ept id="p4">**</ept> を押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Expand <bpt id="p1">**</bpt>HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE<ept id="p1">**</ept>, navigate to the subkey <bpt id="p2">**</bpt>System\CurrentControlSet\Services\Dynamics Server\6.0<ept id="p2">**</ept>, right-click it and select <bpt id="p3">**</bpt>Permissions<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE<ept id="p1">**</ept> を展開し、サブキー <bpt id="p2">**</bpt>System\CurrentControlSet\Services\Dynamics Server\6.0<ept id="p2">**</ept> で移動し、右クリックおよび<bpt id="p3">**</bpt>アクセス許可<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Add the user that you want to associate with the Lifecycle Services Diagnostic Service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services 診断サービスに関連付ける必要のあるユーザーを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Select the user that you added, and then allow read permissions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加したユーザーを選択し、読み取りアクセス許可を許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Click <bpt id="p1">**</bpt>Advanced Security Settings<ept id="p1">**</ept>, and then ensure that the permissions are inherited by the child objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セキュリティの詳細設定<ept id="p1">**</ept>をクリックし、アクセス許可が子オブジェクトによって継承されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Repeat for all AOS instances in each environment that you want to collect data from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データの収集元にする各環境でのすべての AOS インスタンスを繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Important<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>重要<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>As you are configuring rights in the registry, do not reduce account privileges that already exist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジストリで権限を設定するには、既に存在しているアクセス特権を削減することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>For more information about Advanced security settings, see:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティの詳細設定については、以下を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">&lt;a href="http://technet.microsoft.com/en-us/library/jj134043.aspx"&gt;</bpt>Windows Server 2012 Access Control and Authorization Overview<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://technet.microsoft.com/en-us/library/jj134043.aspx"&gt;</bpt>Windows Server 2012 アクセス制御と承認の概要<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">&lt;a href="http://technet.microsoft.com/en-us/library/cc730772.aspx"&gt;</bpt>Windows Server 2008 R2 Advanced Security Settings Properties Page - Permissions Tab<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://technet.microsoft.com/en-us/library/cc730772.aspx"&gt;</bpt>Windows Server 2008 R2 セキュリティの詳細設定のプロパティ ページ - アクセス許可タブ<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Edit the Group Policy on the AOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS のグループ ポリシーを編集</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You must make the services of the AOS remotely accessible in Group Policy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Group Policy では、AOS のサービスをリモートで利用できるようにしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>On the computer running the AOS instance, click <bpt id="p1">**</bpt>Start<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Run<ept id="p2">**</ept>, type <bpt id="p3">**</bpt>gpedit.msc<ept id="p3">**</ept>, and then press <bpt id="p4">**</bpt>Enter<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS インスタンスを実行するコンピューターで、<bpt id="p1">**</bpt>開始<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>実行<ept id="p2">**</ept>をクリックして、<bpt id="p3">**</bpt>gpedit.msc<ept id="p3">**</ept> を入力し、<bpt id="p4">**</bpt>Enter<ept id="p4">**</ept> キーを押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>In the left pane, expand <bpt id="p1">**</bpt>Computer Configuration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Windows settings<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Security settings<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Local policies<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Security options<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左ウィンドウで、<bpt id="p1">**</bpt>コンピューターの構成<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Windows の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>セキュリティ設定<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>ローカル ポリシー<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>セキュリティ オプション<ept id="p5">**</ept>を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>In the right pane, double-click <bpt id="p1">**</bpt>Network access: Remotely accessible registry paths and sub-paths<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右ウィンドウで、<bpt id="p1">**</bpt>ネットワーク アクセス: リモートからアクセスできるレジストリ パスおよびサブ パス<ept id="p1">**</ept>をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>If the following paths are not in the list, add them to the end of the list and then click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のパスがリストにない場合は、リストの最後にそれを追加し、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>System\CurrentControlSet\Control\PriorityControl</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System\CurrentControlSet\Control\PriorityControl</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>System\CurrentControlSet\services\Dynamics Server\6.0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System\CurrentControlSet\services\Dynamics Server\6.0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Configure Windows event log and WMI permissions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows イベント ログおよび WMI のアクセス許可をコンフィギュレーションする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>The service account must be able to read the Windows event logs on each server in the environment, and must be able to monitor remote Windows Management Instrumentation connections.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス アカウントは、環境内の各サーバー上の Windows イベント ログを読み取ることができ、リモートで Windows Management Instrumentation 接続を監視できる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>For more information, see <bpt id="p1">[</bpt>Add a member to a local group<ept id="p1">](http://technet.microsoft.com/en-us/library/cc772524(v=WS.10).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>ローカル グループへのメンバーの追加<ept id="p1">](http://technet.microsoft.com/en-us/library/cc772524(v=WS.10).aspx)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>On each server in the environment, add the service account to the <bpt id="p1">**</bpt>Event Log Readers<ept id="p1">**</ept> local group, the <bpt id="p2">**</bpt>Distributed COM Users<ept id="p2">**</ept> local group and the <bpt id="p3">**</bpt>Performance Monitor Users<ept id="p3">**</ept> local group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境内の各サーバーでは、サービス アカウントを<bpt id="p1">**</bpt>イベント ログ リーダー<ept id="p1">**</ept>ローカル グループ、<bpt id="p2">**</bpt>配分 COM ユーザー<ept id="p2">**</ept>ローカル グループ、および<bpt id="p3">**</bpt>パフォーマンス ユーザーの監視<ept id="p3">**</ept> ローカル グループに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Secure the remote Windows Management Instrumentation connections</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Management Instrumentation リモート接続をセキュリティで保護</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>On each server in your environment that hosts an AOS instance or Microsoft Dynamics AX SQL Server business database, ensure that you secure the remote Windows Management Instrumentation (WMI) connection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS インスタンスまたは Microsoft Dynamics AX SQL Server ビジネス データベースをホストする環境内の各サーバーで、リモート Windows Management Instrumentation(WMI) 接続をセキュリティで保護されたことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Click <bpt id="p1">**</bpt>Start<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Run<ept id="p2">**</ept>, type <bpt id="p3">**</bpt>DCOMCNFG<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>OK<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開始<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>実行<ept id="p2">**</ept>の順にクリックし、<bpt id="p3">**</bpt>DCOMCNFG<ept id="p3">**</ept> と入力し <bpt id="p4">**</bpt>OK<ept id="p4">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>In the <bpt id="p1">**</bpt>Component Services<ept id="p1">**</ept> dialog box, expand <bpt id="p2">**</bpt>Component Services<ept id="p2">**</ept>, expand <bpt id="p3">**</bpt>Computers<ept id="p3">**</ept>, and then right-click <bpt id="p4">**</bpt>My Computer<ept id="p4">**</ept> and click <bpt id="p5">**</bpt>Properties<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コンポーネント サービス<ept id="p1">**</ept> ダイアログ ボックスで、<bpt id="p2">**</bpt>コンポーネント サービス<ept id="p2">**</ept>を展開し、<bpt id="p3">**</bpt>コンピューター<ept id="p3">**</ept>を展開してから、<bpt id="p4">**</bpt>マイ コンピューター<ept id="p4">**</ept>を右クリックして<bpt id="p5">**</bpt>プロパティ<ept id="p5">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>In the <bpt id="p1">**</bpt>My Computer Properties<ept id="p1">**</ept> dialog box, click the <bpt id="p2">**</bpt>COM Security<ept id="p2">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>マイ コンピューターのプロパティ<ept id="p1">**</ept> ダイアログ ボックスで、<bpt id="p2">**</bpt>COM セキュリティ<ept id="p2">**</ept> タブをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Under <bpt id="p1">**</bpt>Launch and Activation Permissions<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Edit Limits<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>起動とアクティベーションのアクセス許可<ept id="p1">**</ept> で、<bpt id="p2">**</bpt>制限の編集<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>In the <bpt id="p1">**</bpt>Launch Permission<ept id="p1">**</ept> dialog box, follow these steps if your name or your group does not appear in the <bpt id="p2">**</bpt>Groups or user names<ept id="p2">**</ept> list:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>起動アクセス許可<ept id="p1">**</ept>ダイアログ ボックスで、名前またはグループが<bpt id="p2">**</bpt>グループまたはユーザー名<ept id="p2">**</ept>一覧に表示されない場合は次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>In the <bpt id="p1">**</bpt>Launch Permission<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>起動アクセス許可<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>In the <bpt id="p1">**</bpt>Select Users, Computers, or Groups<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Enter the object names to select<ept id="p2">**</ept> box, type <bpt id="p3">**</bpt>Distributed COM Users<ept id="p3">**</ept>, click <bpt id="p4">**</bpt>Check Names<ept id="p4">**</ept>, and then click <bpt id="p5">**</bpt>OK<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ユーザー、コンピュータ、またはグループの選択<ept id="p1">**</ept>ダイアログ ボックスの<bpt id="p2">**</bpt>選択するオブジェクト名を入力してください<ept id="p2">**</ept>ボックスに<bpt id="p3">**</bpt>配分 COM ユーザー<ept id="p3">**</ept>と入力して、<bpt id="p4">**</bpt>名前の確認<ept id="p4">**</ept>をクリックしてから <bpt id="p5">**</bpt>OK<ept id="p5">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>In the <bpt id="p1">**</bpt>Enter the object names to select<ept id="p1">**</ept> box, type <bpt id="p2">**</bpt>Performance Monitor Users<ept id="p2">**</ept>, click <bpt id="p3">**</bpt>Check Names<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>OK<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>選択するオブジェクト名を入力してください<ept id="p1">**</ept>ボックスに、<bpt id="p2">**</bpt>パフォーマンス モニター ユーザー<ept id="p2">**</ept>と入力し、<bpt id="p3">**</bpt>名前の確認<ept id="p3">**</ept>をクリックしてから、<bpt id="p4">**</bpt>OK<ept id="p4">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Select <bpt id="p1">**</bpt>Allow<ept id="p1">**</ept> for each of the permissions (Local Launch, Remote Launch, Local Activation, Remote Activation) for each of these groups, and then click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各グループの各アクセス許可 (ローカル起動、リモート起動、ローカルの有効化、リモートの有効化) について <bpt id="p1">**</bpt>許可<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Apply the WMI control security settings to all namespaces:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての名前空間に WMI コントロールのセキュリティ設定を適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Click <bpt id="p1">**</bpt>Start<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Run<ept id="p2">**</ept>, type <bpt id="p3">**</bpt>wmimgmt.msc<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>OK<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開始<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>実行<ept id="p2">**</ept>の順にクリックし、<bpt id="p3">**</bpt>wmimgmt.msc<ept id="p3">**</ept> と入力し <bpt id="p4">**</bpt>OK<ept id="p4">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Right-click <bpt id="p1">**</bpt>WMI Control (Local)<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>WMI コントロール (ローカル)<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>On the <bpt id="p1">**</bpt>Security<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>Root<ept id="p2">**</ept>, click <bpt id="p3">**</bpt>Security<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>Add<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セキュリティ<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>ルート<ept id="p2">**</ept>をクリックし、<bpt id="p3">**</bpt>セキュリティ<ept id="p3">**</ept>をクリックして、<bpt id="p4">**</bpt>追加<ept id="p4">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Under <bpt id="p1">**</bpt>Enter the object names to select<ept id="p1">**</ept>, type Distributed COM users, click <bpt id="p2">**</bpt>Check Names<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>OK<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>選択するオブジェクト名の入力<ept id="p1">**</ept> で Distributed COM ユーザーを入力し、<bpt id="p2">**</bpt>名前の確認<ept id="p2">**</ept> をクリックしてから <bpt id="p3">**</bpt>OK<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Click <bpt id="p1">**</bpt>Advanced<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>詳細<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Select <bpt id="p1">**</bpt>Distributed COM Users<ept id="p1">**</ept> and then click <bpt id="p2">**</bpt>Edit<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>配布される COM ユーザー<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>編集<ept id="p2">**</ept> をクリックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Select <bpt id="p1">**</bpt>This namespace and subnamespaces<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>この名前空間とサブ名前空間<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Select <bpt id="p1">**</bpt>Allow<ept id="p1">**</ept> for the following permissions: Execute Methods, Enable Account, and Remote Enable, and then click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドの実行、アカウントの有効化、リモートの有効化のアクセス許可について <bpt id="p1">**</bpt>許可<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Repeat step 6 for the Performance Monitor Users group, and then close all windows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス モニター ユーザー グループで手順 6 を繰り返し、すべてのウィンドウを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>For more information, see <bpt id="p1">[</bpt>Securing a Remote WMI Connection<ept id="p1">](http://msdn.microsoft.com/en-us/library/windows/desktop/aa393266(v=vs.85).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>リモート WMI 接続の保護<ept id="p1">](http://msdn.microsoft.com/en-us/library/windows/desktop/aa393266(v=vs.85).aspx)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Configure SQL Server permissions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server のアクセス許可をコンフィギュレーションします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>The service account must be able to read the data in the Microsoft Dynamics AX business database and must have access to the default dynamic management views in SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス アカウントは、Microsoft Dynamics AX ビジネス データベースのデータを読み取ることができ、SQL Server の既定の動的管理ビューにアクセスできる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Add the service account as a login to the SQL Server instance where the Microsoft Dynamics AX business database is installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX ビジネス データベースがインストールされている SQL Server インスタンスに、ログインとしてサービス アカウントを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>For information about how to perform this step, see <bpt id="p1">[</bpt>Create a Login<ept id="p1">](http://msdn.microsoft.com/en-us/library/aa337562.aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップを実行する方法の詳細については、「<bpt id="p1">[</bpt>ログインの作成<ept id="p1">](http://msdn.microsoft.com/en-us/library/aa337562.aspx)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Add the account as a user of the business database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス データベースのユーザーとしてアカウントを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>For information about how to perform this step, see <bpt id="p1">[</bpt>How to: Create a Database User<ept id="p1">](http://msdn.microsoft.com/en-us/library/aa337545.aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップを実行する方法の詳細については、「<bpt id="p1">[</bpt>方法: データベース ユーザーの作成<ept id="p1">](http://msdn.microsoft.com/en-us/library/aa337545.aspx)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Add the service account to the db<ph id="ph1">\_</ph>datareader role in the business database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス データベースの db<ph id="ph1">\_</ph>datareader ロールにサービス アカウントを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For information about how to perform this step, see <bpt id="p1">[</bpt>Join a Role<ept id="p1">](http://msdn.microsoft.com/en-us/library/ff877886.aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップを実行する方法の詳細については、「<bpt id="p1">[</bpt>ロールに参加<ept id="p1">](http://msdn.microsoft.com/en-us/library/ff877886.aspx)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Grant the service account the VIEW SERVER STATE permission in the SQL Server instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス アカウントに SQL Server インスタンスの VIEW SERVER STATE 権限を付与します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>In SQL Server Management Studio, expand <bpt id="p1">**</bpt>Databases<ept id="p1">**</ept>, right-click the <bpt id="p2">**</bpt>Microsoft Dynamics AX<ept id="p2">**</ept> database, and then click <bpt id="p3">**</bpt>Properties<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Management Studio で、<bpt id="p1">**</bpt>データベース<ept id="p1">**</ept>を展開し、<bpt id="p2">**</bpt>Microsoft Dynamics AX<ept id="p2">**</ept> データベースを右クリックし、<bpt id="p3">**</bpt>プロパティ<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Click <bpt id="p1">**</bpt>Permissions<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>View server permissions<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アクセス許可<ept id="p1">**</ept>をクリックし、次に<bpt id="p2">**</bpt>サーバーのアクセス許可を表示<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>In the <bpt id="p1">**</bpt>Logins or Roles<ept id="p1">**</ept> list, click the user to whom you want to grant the permission.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ログインまたはロール<ept id="p1">**</ept>一覧で、アクセス許可を付与するユーザーをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>In the <bpt id="p1">**</bpt>Explicit permissions for user<ept id="p1">**</ept> list, select the <bpt id="p2">**</bpt>Grant<ept id="p2">**</ept> check box next to <bpt id="p3">**</bpt>View server state permission<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ユーザーの明示的なアクセス許可<ept id="p1">**</ept>リストで、<bpt id="p3">**</bpt>サーバー状態のアクセス許可を表示<ept id="p3">**</ept>の隣にある<bpt id="p2">**</bpt>付与<ept id="p2">**</ept>チェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Verify that the .NET Business connector service is running in the environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境で .NET Business connector サービスが実行されていることを確認する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The Business Connector service must be running on the host where the Lifecycle Services Diagnostic Service is installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Business Connector サービスは、Lifecycle Services 診断サービスがインストールされているホストで実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>If more than one environment is to be discovered, the .Net Business Connector proxy account must be the same for each server that is running a Microsoft Dynamics AX Application Object Server (AOS) instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つ以上の環境が見つかると、.Ne ビジネス コネクタ プロキシ アカウントは、Microsoft Dynamics AX Application Object Server (AOS) インスタンスを実行している各サーバーと同じものである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>For more information, see <bpt id="p1">[</bpt>Install the .NET Business Connector<ept id="p1">](http://technet.microsoft.com/library/c67944e8-73c5-4434-94d6-84484c810333(AX.60).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>.NET Business Connector のインストール<ept id="p1">](http://technet.microsoft.com/library/c67944e8-73c5-4434-94d6-84484c810333(AX.60).aspx)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Install the Microsoft Dynamics Lifecycle Services System diagnostics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services システム診断のインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>To install the on-premises component of System diagnostics, you must be a member of the Administrator group on the local computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム診断プログラムのオンプレミス コンポーネントをインストールするには、ローカル コンピューターの Administrator グループのメンバーである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">[</bpt>Go to Lifecycle Services<ept id="p1">](https://lcs.dynamics.com)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Lifecycle Services に移動<ept id="p1">](https://lcs.dynamics.com)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Open a project and click the <bpt id="p1">**</bpt>System diagnostics<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを開いて、<bpt id="p1">**</bpt>システム診断<ept id="p1">**</ept>タイルをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>On the <bpt id="p1">**</bpt>Admin<ept id="p1">**</ept> page, download the compressed installer (<bpt id="p2">**</bpt>LCSDiagFX<ph id="ph1">\_</ph>x64.zip.<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>管理者<ept id="p1">**</ept>ページで、圧縮インストーラーをダウンロードします (<bpt id="p2">**</bpt>LCSDiagFX<ph id="ph1">\_</ph>x64.zip.<ept id="p2">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Extract the installer to a computer that is running a Microsoft Dynamics AX client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX クライアントを実行しているコンピュータにインストーラーを抽出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>The computer must have network access to all other servers in the environment, and must be running the .NET Business Connector if you are using the NET Business Connector proxy account as a service account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューターが環境内の他のすべてのサーバーにネットワーク アクセスできる必要があります。.Net Business Connector プロキシ アカウントをサービス アカウントとして使用している場合は、.NET Business Connector を実行している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Important<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>重要<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In a production environment, we recommend that you install the on-premises component on a computer that is running only a client, not on computers that are also running an AOS instance or a SQL Server instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境では、AOS インスタンスまたは SQL Server インスタンスも実行しているコンピューターではなく、クライアントのみ実行しているコンピューターにオンプレミス コンポーネントをインストールすることをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Run <bpt id="p1">**</bpt>Setup.exe<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Setup.exe<ept id="p1">**</ept> を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メモ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Do not run the .msi file directly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">直接 MSI ファイルを実行しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Accept the license terms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンス条項に同意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>If you have an existing local X509 certificate, on the <bpt id="p1">**</bpt>Select the certificate type<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Use existing<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のローカル X509 証明書をお持ちの場合は、<bpt id="p1">**</bpt>証明書タイプを選択<ept id="p1">**</ept> ページで、<bpt id="p2">**</bpt>既存のものを使用<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>If you do not have an X509 certificate, perform the following steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X509 証明書がない場合は、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>On the <bpt id="p1">**</bpt>Select the certificate type<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Create new<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>証明書タイプの選択<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>新規作成<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Enter a prefix to be used in the certificate name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書の名前で使用される接頭語を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to create the certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックして証明書を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Verify that the new certificate has been created in the specified location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した場所に新しい証明書が作成されたことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Return to the <bpt id="p1">**</bpt>System diagnostics<ept id="p1">**</ept> page, browse to the location of the certificate, and click <bpt id="p2">**</bpt>Upload<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム診断<ept id="p1">**</ept> ページに戻り、証明書の場所を参照して <bpt id="p2">**</bpt>アップロード<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Return to the <bpt id="p1">**</bpt>Upload the new certificate<ept id="p1">**</ept> page of the <bpt id="p2">**</bpt>Microsoft Dynamics Lifecycle Services Diagnostic Service Setup Wizard<ept id="p2">**</ept>, select <bpt id="p3">**</bpt>Certificate file has been uploaded<ept id="p3">**</ept>, and click <bpt id="p4">**</bpt>Next<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Microsoft Dynamics Lifecycle Services 診断サービス セットアップ ウィザード<ept id="p2">**</ept>の <bpt id="p1">**</bpt>新しい証明書のアップロード<ept id="p1">**</ept> ページに戻り、<bpt id="p3">**</bpt>証明書ファイルがアップロードされました<ept id="p3">**</ept>を選択して<bpt id="p4">**</bpt>次へ<ept id="p4">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>On the <bpt id="p1">**</bpt>Select private certificate<ept id="p1">**</ept> page, the name of the certificate is displayed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プライベート証明書の選択<ept id="p1">**</ept>ページで、証明書の名前が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>On the <bpt id="p1">**</bpt>Specify service account<ept id="p1">**</ept> page, enter the service account and password, and then click <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サービス アカウントの指定<ept id="p1">**</ept>ページで、サービス アカウントとパスワードを入力し、<bpt id="p2">**</bpt>次へ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>On the <bpt id="p1">**</bpt>Change destination folder<ept id="p1">**</ept> page, enter the location where you want to store the logs that were collected by the System diagnostics, and then click <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>変更先フォルダ<ept id="p1">**</ept>ページで、システム診断によって収集されたログを保管する場所を入力し、<bpt id="p2">**</bpt>次<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to install and start the System diagnostics, and then click <bpt id="p2">**</bpt>Finish<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> クリックして、システム診断をインストールおよび開始し、次に<bpt id="p2">**</bpt>完了<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Two executable programs are installed: LCSDiagFXDiscovery.exe and LCSDiagFXCollector.exe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの実行可能プログラム、LCSDiagFXDiscovery.exe と LCSDiagFXCollector.exe がインストールされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Discover environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境を検出</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Click <bpt id="p1">**</bpt>Start<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Microsoft Dynamics AX Lifecycle Services Diagnostic Service Discovery.<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開始<ept id="p1">**</ept>、<bpt id="p2">**</bpt>Microsoft Dynamics AX Lifecycle Services 診断サービス検索<ept id="p2">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In the <bpt id="p1">**</bpt>Environment Discovery<ept id="p1">**</ept> window, enter a name for the environment, the fully-qualified name of the SQL Server instance and database, and then click <bpt id="p2">**</bpt>Discover<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境の検出<ept id="p1">**</ept>ウィンドウに、環境の名前と SQL Server のインスタンスとデータベースの完全修飾名を入力してから、<bpt id="p2">**</bpt>検出<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>At the bottom of the Window, click the <bpt id="p1">**</bpt>Test permissions<ept id="p1">**</ept> button <ph id="ph1">![</ph>Test permissions button for System diagnostics<ph id="ph2">](./media/testpermissions.jpg)</ph> at the bottom of the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウの一番下にある<bpt id="p1">**</bpt>テストアクセス許可<ept id="p1">**</ept>ボタンをクリックします。<ph id="ph1">![</ph>システム診断用のテストアクセス許可ボタン<ph id="ph2">](./media/testpermissions.jpg)</ph> ページの下部にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>On the <bpt id="p1">**</bpt>Change destination folder<ept id="p1">**</ept> page, enter the location where you want to store the logs that were collected by the System diagnostics, and then click <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>変更先フォルダ<ept id="p1">**</ept>ページで、システム診断によって収集されたログを保管する場所を入力し、<bpt id="p2">**</bpt>次<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Collect data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データを収集</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>You can collect data on demand from the <bpt id="p1">**</bpt>Environment Discovery<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて <bpt id="p1">**</bpt>環境の検出<ept id="p1">**</ept> ウィンドウからデータを収集することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>We recommend that you schedule a job to collect data regularly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定期的にデータを収集するジョブをスケジュールすることをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Data collection typically takes between 5 and 15 minutes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ収集は、通常、5 ~ 15 分かかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Errors that are encountered during data collection are logged in the Windows Application event log, as well as in a log file in the location that you specified during installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ収集中に発生したエラーは、Windows アプリケーション イベント ログと、インストール中に指定した場所のログ ファイルに記録されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>To run an initial data collection in the <bpt id="p1">**</bpt>Environment Discovery<ept id="p1">**</ept> window, click <bpt id="p2">**</bpt>Collect now<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境の検出<ept id="p1">**</ept> ウィンドウで初期データ収集を実行するには、<bpt id="p2">**</bpt>今すぐ収集<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>We recommend that you run an initial collection immediately after discovering an environment for the first time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">初めて環境を検出した直後に最初のコレクションを実行することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>To generate a collection command that you can use to schedule collection jobs, click <bpt id="p1">**</bpt>Generate collection command<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コレクション ジョブのスケジューリングに使用できるコレクション コマンドを生成するするには、<bpt id="p1">**</bpt>コレクション コマンドを生成<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Copy the generated command to the clipboard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたコマンドをクリップボードにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Schedule the command to run by using a scheduling engine, such as <bpt id="p1">**</bpt>Windows Task Scheduler<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Windows タスク スケジューラ<ept id="p1">**</ept>などのスケジュール エンジンを使用して実行するコマンドをスケジュール設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>For more information about using <bpt id="p1">**</bpt>Task Scheduler<ept id="p1">**</ept>, see <bpt id="p2">[</bpt>Schedule a task<ept id="p2">](http://technet.microsoft.com/en-us/library/cc766428.aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タスク スケジューラ<ept id="p1">**</ept>の使用の詳細については、<bpt id="p2">[</bpt>タスクのスケジュール<ept id="p2">](http://technet.microsoft.com/en-us/library/cc766428.aspx)</ept> を参照してください</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Use same X509 certificate for all environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての環境で同じ X509 証明書を使用する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>First time let setup generate certificate as usual</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">当初期間は、証明書を生成する設定を従来どおりにします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Run MMC (Microsoft management console) as admin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MMC (Microsoft管理コンソール) を管理者として実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>File -<ph id="ph1">&amp;gt;</ph> "<bpt id="p1">**</bpt>Add or Remove Snap-ins<ept id="p1">**</ept>"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル -<ph id="ph1">&amp;gt;</ph> <bpt id="p1">**</bpt>スナップインの追加または削除<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Double click <bpt id="p1">**</bpt>Certificates<ept id="p1">**</ept> item and choose computer account then next-<ph id="ph1">&amp;gt;</ph>finish-<ph id="ph2">&amp;gt;</ph>ok</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>証明書<ept id="p1">**</ept>項目をダブルクリックし、コンピューター アカウントと next-<ph id="ph1">&amp;gt;</ph>finish-<ph id="ph2">&amp;gt;</ph>ok を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Expand Certificates (Local Computer)-<ph id="ph1">&amp;gt;</ph><bpt id="p1">**</bpt>Personal<ept id="p1">**</ept><ph id="ph2">-</ph><ph id="ph3">&amp;gt;</ph>Certificates:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書 (ローカル コンピューター)-<ph id="ph1">&amp;gt;</ph><bpt id="p1">**</bpt>個人<ept id="p1">**</ept><ph id="ph2">-</ph><ph id="ph3">&amp;gt;</ph> 証明書を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Right click on certificate generated on first step -<ph id="ph1">&amp;gt;</ph> All tasks -<ph id="ph2">&amp;gt;</ph> Export -<ph id="ph3">&amp;gt;</ph> Next -<ph id="ph4">&amp;gt;</ph> Choose "<bpt id="p1">**</bpt>Yes, export the private key<ept id="p1">**</ept>"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の手順 - <ph id="ph1">&amp;gt;</ph> すべてのタスク -<ph id="ph2">&amp;gt;</ph> エクスポート -<ph id="ph3">&amp;gt;</ph> 次へ -<ph id="ph4">&amp;gt;</ph> "<bpt id="p1">**</bpt>はい、プライベート キーをエクスポートします<ept id="p1">**</ept>" で生成された証明書を右クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Leave default values in <ph id="ph1">\*</ph>.pfx export setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph>.pfx エクスポート設定で既定値のままにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>In security step Use domain account or password for securing your exported file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ ステップでは、エクスポートしたファイルを保護するためにドメイン アカウントまたはパスワードを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Export files in next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順でファイルをエキスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Copy exported file to new environment click it and choose <bpt id="p1">**</bpt>Install PFX<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートしたファイルを新しい環境にコピーし、クリックして、<bpt id="p1">**</bpt>PFX のインストール<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Choose <bpt id="p1">**</bpt>Local Machine<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ローカル コンピューター<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Click next -<ph id="ph1">&amp;gt;</ph> And in following screen make sure that <bpt id="p1">**</bpt>Mark this key as exportable<ept id="p1">**</ept> is set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次へ -<ph id="ph1">&amp;gt;</ph> をクリックし、次の画面で、<bpt id="p1">**</bpt>このキーをエクスポート可能としてマーク<ept id="p1">**</ept>が設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Click next and finish</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次へをクリックして終了</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Now when running Lifecycle services system diagnostics setup choose on new environment use an existing certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで、Lifecycle Services システム診断セットアップを実行している場合、新しい環境を選択して既存の証明書を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Certificate generated in first step should be present in client certificates lookup choose it and continue as usual:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の手順で生成された証明書は、クライアント証明書のルックアップに含まれており、それを選択して通常どおりに続行する必要があります:</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
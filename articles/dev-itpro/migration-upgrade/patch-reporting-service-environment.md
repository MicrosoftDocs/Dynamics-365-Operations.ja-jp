<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="patch-reporting-service-environment.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>patch-reporting-service-environment.156c48.da0e173602d637a7bb0584dab15f79a941ff7a34.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>da0e173602d637a7bb0584dab15f79a941ff7a34</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\patch-reporting-service-environment.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Patch SQL Server Reporting Services (SSRS) in one-box environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 ボックス環境で SQL Server Reporting Services (SSRS) への修正プログラムの適用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>Apply SSRS hotfixes to a one-box development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSRS 修正プログラムをワンボックス開発環境に適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Patch SQL Server Reporting Services (SSRS) in one-box environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 ボックス環境で SQL Server Reporting Services (SSRS) への修正プログラムの適用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>The following procedure is for one-box development environments only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順は、1 ボックス開発環境のみを対象としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Patch the Reporting Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reporting Service のパッチ適用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The following procedure is for one-box development environments only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順は、1 ボックス開発環境のみを対象としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Download the patch .zip file from Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッチ .zip file を Lifecycle Services (LCS) からダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If there are any font files in the Reporting Service patch’s data folder, install these to the machine where SQL Server Reporting Services (SSRS) is running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート サービスの修正プログラムのデータのフォルダーにフォント ファイルがある場合は、SQL Server Reporting Services (SSRS) が実行されているコンピューターにこれらをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For more information about installing fonts on windows, see <bpt id="p1">[</bpt>TrueType overview<ept id="p1">](https://www.microsoft.com/Typography/TrueTypeInstall.aspx)</ept>.</source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match">Windows にフォントをインストールする詳細については <bpt id="p1">[</bpt>TrueType 概要<ept id="p1">](https://www.microsoft.com/Typography/TrueTypeInstall.aspx)</ept> を参照してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Any fonts that have already been installed do not need to be installed again.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">既にインストールされているフォントは再度インストールする必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Copy the files in the Reporting Services patch scripts folder to the Report plug-in folder located under C:<ph id="ph1">\\</ph>Packages<ph id="ph2">\\</ph>Plugins<ph id="ph3">\\</ph>AxReportVmRoleStartupTask.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reporting Services のパッチ スクリプト フォルダーのファイルを C:<ph id="ph1">\\</ph>Packages<ph id="ph2">\\</ph>Plugins<ph id="ph3">\\</ph>AxReportVmRoleStartupTask の下にあるレポート プラグイン フォルダーにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Change the directory to the Report plug-in folder where you stored the script files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ディレクトリを、スクリプト ファイルを格納したレポート プラグイン フォルダに変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Using one of the methods listed below, replace the old instance of reporting extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下に示すメソッドのいずれかを使用して、レポート拡張機能の古いインスタンスを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Remove/reinstall the reporting extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート拡張機能を削除/再インストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The remove/reinstall option requires that redeploy all reports after you have finished the reinstallation..</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除/再インストール オプションでは、インストールが完了した後にすべてのレポートを再配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Manually copy binaries to the sql server binary folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server バイナリ フォルダーに手動でバイナリをコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>If you choose to manually copy the files, then you do not need to redeploy reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動でファイルをコピーする場合は、レポートを再展開する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Remove/reinstall the reporting extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート拡張機能を削除/再インストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Complete the following procedure as a user in the administrator group for the machine where SSRS is running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSRS が実行されているマシンの管理者グループのユーザーとして、以下の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Using Windows PowerShell, remove the Dynamics SSRS extension by running the following script:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows PowerShell を使用して、次のスクリプトを実行することで、Dynamics SSRS 拡張機能を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>PowerShell .<ph id="ph1">\\</ph>DeploySsrsExtension.ps1 –UninstallOnly</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PowerShell .<ph id="ph1">\\</ph>DeploySsrsExtension.ps1 –UninstallOnly</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>In PowerShell, reinstall the Dynamics SSRS extension by running the following script:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PowerShell では、次のスクリプトを実行することで Dynamics SSRS 拡張機能を再インストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>PowerShell .<ph id="ph1">\\</ph>DeploySsrsExtension.ps1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PowerShell .<ph id="ph1">\\</ph>DeploySsrsExtension.ps1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Removing the reporting extension removes all the reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートの拡張機能を削除すると、すべてのレポートが削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>If you have removed and then reinstalled the reporting extension, it is necessary to re-deploy the reports by running the following script:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート拡張機能を削除してから再インストールした場合は、次のスクリプトを実行してレポートを再展開する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Powershell .<ph id="ph1">\\</ph>DeployAllReportsToSsrs.ps1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Powershell .<ph id="ph1">\\</ph>DeployAllReportsToSsrs.ps1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This task will take 20 to 30 minutes to complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスクは、完了までに 20 ~ 30 分かかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Manually copy binaries to the SQL Server binary folder</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server バイナリ フォルダーへの手動でのバイナリのコピー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Stop SQL Server Reporting Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Reporting Services を停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This can be done either from the <bpt id="p1">**</bpt>Services management<ept id="p1">**</ept> console or from the <bpt id="p2">**</bpt>Reporting Services Configuration Manager<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、<bpt id="p1">**</bpt>サービス管理コンソール<ept id="p1">**</ept>または <bpt id="p2">**</bpt>Reporting Services 構成マネージャー<ept id="p2">**</ept>から実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Configuration<ph id="ph2">\_</ph>RSHotfix<ept id="p1">](./media/configuration_rshotfix.png)](./media/configuration_rshotfix.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Configuration<ph id="ph2">\_</ph>RSHotfix<ept id="p1">](./media/configuration_rshotfix.png)](./media/configuration_rshotfix.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Find the SQL Server Reporting Services binary folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Reporting Services バイナリ フォルダーを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>This folder is usually located at C:<ph id="ph1">\\</ph>Program Files<ph id="ph2">\\</ph>Microsoft SQL Server<ph id="ph3">\\</ph>MSRS11.MSSQLSERVER<ph id="ph4">\\</ph>Reporting Services<ph id="ph5">\\</ph>ReportServer<ph id="ph6">\\</ph>bin.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフォルダーは、通常、C:<ph id="ph1">\\</ph>Program Files<ph id="ph2">\\</ph>Microsoft SQL Server<ph id="ph3">\\</ph>MSRS11.MSSQLSERVER<ph id="ph4">\\</ph>Reporting Services<ph id="ph5">\\</ph>ReportServer<ph id="ph6">\\</ph>bin にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If any of the following files are in the patch, copy them to the SQL Server Reporting Services bin folder.* *</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">次のファイルのいずれかがパッチにある場合は、それらのファイルを SQL Server Reporting Services Bin フォルダーにコピーします。* *</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Patches can either be full patches, which would contain all of the files used by the service, or incremental patches, which contain only the files that have changed.</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">パッチは、サービスによって使用されるすべてのファイルを含む完全なパッチ、または変更されたファイルのみを含む増分パッチのいずれかです。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>If you have an incremental patch, then some files may not be included.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">差分の修正プログラムを使用する場合は、一部のファイルが含まれない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Files not included in the patch do not need to be replaced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッチに含まれていないファイルは、置き換える必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Microsoft.Dynamics.AX.Framework.Services.Platform.Client.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.AX.Framework.Services.Platform.Client.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Microsoft.Dynamics.Framework.ReportsExtensions.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.Framework.ReportsExtensions.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Microsoft.Dynamics.Framework.Reports.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.Framework.Reports.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Microsoft.Dynamics.ApplicationPlatform.SSRSReportRuntime.Instrumentation.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.ApplicationPlatform.SSRSReportRuntime.Instrumentation.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Microsoft.Dynamics.ApplicationPlatform.SSRSReportRuntime.man</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.ApplicationPlatform.SSRSReportRuntime.man</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Microsoft.Dynamics.Platform.Integration.ClientSdk.Abstraction.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.Platform.Integration.ClientSdk.Abstraction.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Microsoft.Dynamics.AX.Framework.Reports.Shared.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.AX.Framework.Reports.Shared.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Microsoft.Dynamics.AX.Framework.EncryptionEngine.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.AX.Framework.EncryptionEngine.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Microsoft.Dynamics.AX.Framework.Utilities.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.AX.Framework.Utilities.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Microsoft.Dynamics.ApplicationSuite.Reporting.BusinessLogic.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.ApplicationSuite.Reporting.BusinessLogic.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Microsoft.Dynamics.ApplicationPlatform.Environment.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.ApplicationPlatform.Environment.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Microsoft.Dynamics.AX.ReportConfiguration.axc</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.AX.ReportConfiguration.axc</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Microsoft.WindowsAzure.ServiceRuntime.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.WindowsAzure.ServiceRuntime.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Microsoft.IdentityModel.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.IdentityModel.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>msshrtmi.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">msshrtmi.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Restart SQL Server Reporting Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Reporting Services を再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Reporting service installation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reporting Services インストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The following changes are made with the reporting service installation: The following files will be copied into Reporting service bin folder (C:<ph id="ph1">\\</ph>Program Files<ph id="ph2">\\</ph>Microsoft SQL Server<ph id="ph3">\\</ph>MSRS11.MSSQLSERVER<ph id="ph4">\\</ph>Reporting Services<ph id="ph5">\\</ph>ReportServer<ph id="ph6">\\</ph>bin), and the corresponding SSRS config files will be updated so that SSRS is aware of the extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート サービスのインストールでは、以下の変更が行われます。以下のファイルは、レポート サービスの bin フォルダー (C:<ph id="ph1">\\</ph>Program Files<ph id="ph2">\\</ph>Microsoft SQL Server<ph id="ph3">\\</ph>MSRS11.MSSQLSERVER<ph id="ph4">\\</ph>Reporting Services<ph id="ph5">\\</ph>ReportServer<ph id="ph6">\\</ph>bin) にコピーされ、対応する SSRS 設定ファイルが更新され、SSRS は拡張機能を認識します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Dynamics.AX.Framework.Services.Platform.Client.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.AX.Framework.Services.Platform.Client.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Dynamics.Framework.ReportsExtensions.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.Framework.ReportsExtensions.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Dynamics.Framework.Reports.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.Framework.Reports.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Dynamics.ApplicationPlatform.SSRSReportRuntime.Instrumentation.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.ApplicationPlatform.SSRSReportRuntime.Instrumentation.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Dynamics.ApplicationPlatform.SSRSReportRuntime.man</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.ApplicationPlatform.SSRSReportRuntime.man</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Dynamics.Platform.Integration.ClientSdk.Abstraction.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.Platform.Integration.ClientSdk.Abstraction.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Dynamics.AX.Framework.Reports.Shared.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.AX.Framework.Reports.Shared.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Dynamics.AX.Framework.EncryptionEngine.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.AX.Framework.EncryptionEngine.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Dynamics.AX.Framework.Utilities.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.AX.Framework.Utilities.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Dynamics.ApplicationSuite.Reporting.BusinessLogic.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.ApplicationSuite.Reporting.BusinessLogic.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Dynamics.ApplicationPlatform.Environment.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.ApplicationPlatform.Environment.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Dynamics.AX.ReportConfiguration.axc</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics.AX.ReportConfiguration.axc</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>WindowsAzure.ServiceRuntime.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WindowsAzure.ServiceRuntime.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>IdentityModel.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IdentityModel.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>msshrtmi.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">msshrtmi.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>An SSRS service account will be updated to use the local system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSRS サービス アカウントはローカル システムを使用して更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>A new SSRS catalog database DynamicsAxReportServer and temp database DynamicsAxReportServerTempDB database will be created, and SSRS will be configured to use these two databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい SSRS カタログ データベースの DynamicsAxReportServer と、一時データベースの DynamicsAxReportServerTempDB データベースが作成され、SSRS は、これら 2 つのデータベースを使用するように構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>The default catalog database ReportServer and ReportServerTempDBstill exist, but are set to not be used by reporting services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のカタログ データベース ReportServer と ReportServerTempDBstill は存在しますが、レポート サービスでは使用されないように設定されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The SSRS service will be updated to use Windows Authentication.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSRS サービスは、Windows 認証を使用するために更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>An xml configuration file ReportPVMConfiguration.xml will be created in the SSRS bin folder for the report runtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">xml 構成ファイル ReportPVMConfiguration.xml はレポート実行時間の SSRS bin フォルダー内に作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>A report root folder named <bpt id="p1">**</bpt>Dynamics<ept id="p1">**</ept> and a new security role named <bpt id="p2">**</bpt>DynamicsBrowser<ept id="p2">**</ept> will be created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics<ept id="p1">**</ept> という名前のレポート ルート フォルダーと <bpt id="p2">**</bpt>DynamicsBrowser<ept id="p2">**</ept> という名前のセキュリティ ロールが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Both AOS Web application AppPool identity and batch service account will be added to this custom role.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このカスタム ロールには AOS Web アプリケーションの AppPool ID とバッチ サービス アカウントの両方が追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Note that during deployment, the report folder will be deleted and then recreated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置中、レポート フォルダーは削除されてから再作成されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Therefore all the previously deployed reports will be deleted from the SSRS server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、以前に展開されたレポートはすべて SSRS サーバーから削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>After you reinstall the reporting extension, you must redeploy the reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート拡張機能を再インストールした後は、レポートを再配置する必要があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
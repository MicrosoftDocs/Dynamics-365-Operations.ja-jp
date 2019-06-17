<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="copy-database-from-sql-server-to-azure-sql.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>copy-database-from-sql-server-to-azure-sql.2ac07c.e081cdd84dc37f9211047a5dba74e5b993ebdc2d.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e081cdd84dc37f9211047a5dba74e5b993ebdc2d</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\database\copy-database-from-sql-server-to-azure-sql.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Copy Finance and Operations databases from SQL Server to production Azure SQL Database environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations データベースを SQL Server から Azure SQL データベース運用環境にコピーする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to move a Microsoft Dynamics 365 for Finance and Operations database from a SQL Server–based development, build, or demo environment (Tier 1 or one-box) to an Azure SQL database–based sandbox UAT environment (Tier 2 or higher).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースを SQL Server をベースとした開発、ビルド、またはデモ環境 (第 1 層または ワンボックス) から Azure SQL データベースをベースしたサンドボックス UAT 環境 (第 2 層以上) に移動する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Copy Finance and Operations databases from SQL Server to production Azure SQL Database environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations データベースを SQL Server から Azure SQL データベース運用環境にコピーする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to move a Microsoft Dynamics 365 for Finance and Operations database from an environment that is based on Microsoft SQL Server (a development, build or demo environment, which is also known as a Tier 1 or one-box environment) to an environment that is based on a Microsoft Azure SQL database (a sandbox user acceptance testing <ph id="ph1">\[</ph>UAT<ph id="ph2">\]</ph> environment, Tier 2 or higher).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースを、Microsoft SQL Server をベースとした環境 (開発、ビルド、またはデモ環境。第 1 層またはワンボックス環境とも呼ばれます) から Microsoft Azure SQL データベースをベースとした環境 (サンドボックス ユーザー受け入れテストの <ph id="ph1">\[</ph>UAT<ph id="ph2">\]</ph> 環境。第 2 層以上) に移動する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Typically, this process is completed before go-live, to bring a golden (or seed) database that contains only system configuration data into a production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、このプロセスは稼動前に完了し、システム構成データのみを含むゴールデン (またはシード) データベースを実稼働環境に移行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This process isn't suitable for all situations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスは、すべての状況に適しているわけではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>For example, you should not use this process to import data for a new legal entity for an existing live deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、既存の実際の展開に対して新しい法人のデータをインポートするためには、このプロセスを使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>In situations of this type, we recommend that you use <bpt id="p1">[</bpt>process data packages<ept id="p1">](../lcs-solutions/process-data-packages-lcs-solutions.md)</ept> or <bpt id="p2">[</bpt>data entity data packages<ept id="p2">](../data-entities/data-entities-data-packages.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタイプの場合、<bpt id="p1">[</bpt>プロセス データ パッケージ<ept id="p1">](../lcs-solutions/process-data-packages-lcs-solutions.md)</ept>または<bpt id="p2">[</bpt>データ エンティティ データ パッケージ<ept id="p2">](../data-entities/data-entities-data-packages.md)</ept>を使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Here is the supported procedure for bringing a golden database into a production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ゴールデン データベースを実稼働環境に移行するためにサポートされている手順を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>A customer or partner exports the database from SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客やパートナーは、SQL Server のデータベースをエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The customer or partner imports the database into a sandbox environment that runs on an Azure SQL database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客またはパートナーは、データベースを Azure SQL データベース上で実行されるサンドボックス環境にインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In Microsoft Dynamics Lifecycle Services (LCS), the customer or partner submits a service request of the <bpt id="p1">**</bpt>Sandbox to Production<ept id="p1">**</ept> type to ask that the Microsoft Dynamics Support Engineering (DSE) team move the sandbox database to the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) では、顧客またはパートナーが<bpt id="p1">**</bpt>サンドボックスから実稼働環境<ept id="p1">**</ept>タイプのサービス要求を送信して、Microsoft Dynamics のサポート エンジニアリング (DSE) チームにサンドボックス データベースを実稼動環境に移動してもらうよう依頼します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The DSE team copies the database from the sandbox environment to the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DSE チームでは、データベースをサンドボックス環境から実稼働環境にコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Microsoft accepts requests to copy a database into a production environment only before go-live.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、運用する前にのみデータベースを実稼働環境にコピーする要求を受け入れます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>During the process for moving a database, the sqlpackage.exe command-line tool is used to export the database from SQL Server and import it into an Azure SQL database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの移動中に、sqlpackage.exe コマンド ライン ツールを使用して、SQL Server からデータベースをエクスポートし、Azure SQL データベースにインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Because the file name extension for the exported data file is .bacpac, the process is often referred to as the <bpt id="p1">*</bpt>bacpac process<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートされたデータ ファイルのファイル名拡張子は .bacpac なので、プロセスは多くの場合 <bpt id="p1">*</bpt>bacpac プロセス<ept id="p1">*</ept>と呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Here is the high-level process for a database move.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース移動のための高レベルのプロセスを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Create a copy of the source database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース データベースのコピーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Run a script to prepare the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの準備のためスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Export the database from SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server からデータベースをエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Import the database into an Azure SQL database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure SQL データベースにデータベースをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Run a script to update the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの更新のためスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If you encounter issues, see the "Known issues and limitations" section at the end of this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題が発生する場合は、このトピックの最後にある「既知の問題と制限事項」を参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>It explains how to troubleshoot, gives performance tips, and explains limitations of the copy process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トラブルシューティング方法について説明し、パフォーマンスのヒントを紹介して、コピー処理の制限について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The source environment (the environment where the source database was created) must run a version of the Finance and Operations platform that is earlier than or the same as the version of the platform that the destination environment runs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース環境 (ソース データベースが作成された環境) は、ターゲット環境が実行されているプラットフォームのバージョンよりも前または同じバージョンの Finance and Operations プラットフォームを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>To import a database from a sandbox environment, you must be running the same version of SQL Server Management Studio that is in the environment you will be importing the database to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス環境からデータベースをインポートするには、データベースをインポートする環境で同じバージョンの SQL Server Management Studio を実行している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>This may require you to install the <bpt id="p1">[</bpt>latest version of SQL Server Management Studio<ept id="p1">](https://msdn.microsoft.com/en-us/library/mt238290.aspx)</ept> on the computer that runs Application Object Server (AOS) in the sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、サンドボックス環境で Application Object Server (AOS) を実行するコンピューターに <bpt id="p1">[</bpt>SQL Server Management Studio の最新バージョン<ept id="p1">](https://msdn.microsoft.com/en-us/library/mt238290.aspx)</ept>をインストールする必要が生じる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>You can then do the bacpac export on that AOS computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS コンピューターで、bacpac エクスポートを実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>There are two reasons for this requirement:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要件は 2 つの理由があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Because of an Internet Protocol (IP) access restriction on the sandbox instance of SQL Server, only computers in that environment can connect to the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server のサンドボックス インスタンスに対するインターネット プロトコル (IP) アクセス制限のため、その環境内のコンピュータのみがインスタンスに接続できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The exported <ph id="ph1">\*</ph>.bacpac file may be dependent on version specific features of Management Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートされた <ph id="ph1">\*</ph>.bacpac ファイルは、Management Studio のバージョン固有の機能に依存する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>If your environment includes Microsoft Dynamics 365 for Retail components, you must manually store some environment-specific values before you begin.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境に、Microsoft Dynamics 365 for Retail コンポーネントが含まれている場合、開始する前に、一部の環境固有の値を手動で保存する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>For more information, see the "Additional steps for Retail environments" section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「小売環境の追加手順」セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Before you begin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Supported SQL Server collation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポートされる SQL Server の照合順序</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The only supported collation for Finance and Operations databases in the cloud is <bpt id="p1">**</bpt>SQL_Latin1_General_CP1_CI_AS<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウドの Finance and Operations データベースでサポートされている唯一の照合順序は、<bpt id="p1">**</bpt>SQL_Latin1_General_CP1_CI_AS<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Please ensure that your SQL Server and database collations in development environments are set to this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境の SQL Server とデータベース照合順序がこれに設定されていることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Also ensure that any configuration environments that are published to Sandbox have this same collation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこれと同じ照合順序があることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Document the values of encrypted fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗号化されたフィールドの値を文書化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Encrypted and environment-specific values can't be imported into a new environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗号化された環境固有の値を新しい環境にインポートすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>After you've completed the import, you must re-enter some data from your source environment in your target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート処理を完了した後は、ターゲット環境内のソース環境から一部のデータを再入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Because of a technical limitation that is related to the certificate that is used for data encryption, values that are stored in encrypted fields in a database will be unreadable after that database is imported into a new environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ暗号化に使用される証明書に関連する技術的な制限のため、データベースの暗号化されたフィールドに格納されている値はそのデータベースが新しい環境にインポートされた後は読み取れません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Therefore, after an import, you must manually delete and re-enter values that are stored in encrypted fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、インポート後、暗号化されたフィールドに格納されている値を手動で削除して再入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>New values that are entered in encrypted fields after an import will be readable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート後に暗号化されたフィールドに入力される新しい値は読み取り可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The following fields are affected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のフィールドが影響されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The field names are given in Table.Field format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名は Table.Field 形式で指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Field name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Where to set the value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値を設定する場所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>CreditCardAccountSetup.SecureMerchantProperties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreditCardAccountSetup.SecureMerchantProperties</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Select <bpt id="p1">**</bpt>Accounts receivable<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Payments setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Payment services<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>売掛金勘定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>支払設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>支払サービス<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>ExchangeRateProviderConfigurationDetails.Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ExchangeRateProviderConfigurationDetails.Value</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Select <bpt id="p1">**</bpt>General ledger<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Currencies<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Configure exchange rate providers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>総勘定元帳<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>通貨<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>為替レート プロバイダーを構成する<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>FiscalEstablishment<ph id="ph1">\_</ph>BR.ConsumerEFDocCsc</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FiscalEstablishment<ph id="ph1">\_</ph>BR.ConsumerEFDocCsc</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Select <bpt id="p1">**</bpt>Organization administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Fiscal establishments<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Fiscal establishments<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>組織管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>会計機関<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>会計機関<ept id="p3">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>FiscalEstablishmentStaging.CSC</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FiscalEstablishmentStaging.CSC</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This field is used by the Data Import/Export Framework (DIXF).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>HcmPersonIdentificationNumber.PersonIdentificationNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HcmPersonIdentificationNumber.PersonIdentificationNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Select <bpt id="p1">**</bpt>Human resources<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Workers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Workers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>人事管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>作業者<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>作業者<ept id="p3">**</ept> の順に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>On the <bpt id="p1">**</bpt>Worker<ept id="p1">**</ept> tab, in the <bpt id="p2">**</bpt>Personal information<ept id="p2">**</ept> group, select <bpt id="p3">**</bpt>Identification numbers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ワーカー<ept id="p1">**</ept>タブの、<bpt id="p2">**</bpt>個人情報<ept id="p2">**</ept>グループで、<bpt id="p3">**</bpt>ID 番号<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>HcmWorkerActionHire.PersonIdentificationNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HcmWorkerActionHire.PersonIdentificationNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>This field has been obsolete since Microsoft Dynamics AX 7.0 (February 2016).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) は廃止されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>It previously appeared in the <bpt id="p1">**</bpt>All worker actions<ept id="p1">**</ept> form (<bpt id="p2">**</bpt>Human resources<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Workers<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Actions<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>All worker actions<ept id="p5">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは以前、<bpt id="p1">**</bpt>すべての作業者アクション<ept id="p1">**</ept> フォーム (<bpt id="p2">**</bpt>人事管理<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>作業者<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>アクション<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>すべての作業者アクション<ept id="p5">**</ept>) に表示されていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>SysEmailSMPTPassword.Password</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysEmailSMPTPassword.Password</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Select <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Email<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Email parameters<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>電子メール<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>電子メール パラメーター<ept id="p3">**</ept> の順に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>SysOAuthUserTokens.EncryptedAccessToken</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysOAuthUserTokens.EncryptedAccessToken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This field is used internally by AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、AOS で内部的に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>It can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは無視できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>SysOAuthUserTokens.EncryptedRefreshToken</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysOAuthUserTokens.EncryptedRefreshToken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>This field is used internally by AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、AOS で内部的に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>It can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは無視できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>If you're running Retail components, document encrypted and environment-specific values</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネントを実行している場合は、暗号化された、環境固有の値を文書化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>The values on the following pages are either environment-specific or encrypted in the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のページの値は、環境固有またはデータベースで暗号化されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Therefore, all the imported values will be incorrect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、インポートされた値はすべて正しくありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Payments services (<bpt id="p1">**</bpt>Accounts receivable<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Payments setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Payments services<ept id="p3">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払サービス (<bpt id="p1">**</bpt>売掛金勘定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>支払設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>支払サービス<ept id="p3">**</ept>) に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Hardware profiles (<bpt id="p1">**</bpt>Retail and commerce<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS setup<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS profiles<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Hardware profiles<ept id="p5">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア プロファイル (<bpt id="p1">**</bpt>小売りとコマース<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>チャネル設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS 設定<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS プロファイル<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>ハードウェア プロファイル<ept id="p5">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Create a copy of the source database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース データベースのコピーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Because you must delete database users before you can export the source SQL Server database, you should create a copy of that database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース SQL Server データベースをエクスポートする前に、データベース ユーザーを削除する必要があるため、そのデータベースのコピーを作成してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>You can then work with the copy instead of modifying the original database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元のデータベースを修正する代わりに、コピーで作業することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>The following script backs up the default AxDB database and then restores it to the same instance under a new name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリプトは、既定の AxDB データベースをバックアップし、それを新しいインスタンス名に変更して同じインスタンスに復元します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>To use this script, first verify that the path D:<ph id="ph1">\\</ph>backups exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このスクリプトを使用するには、最初に D:<ph id="ph1">\\</ph>backups のパスが存在することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Prepare the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Run the following script against the AxDB<ph id="ph1">\_</ph>CopyForExport database that you created in the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリプトを、前のセクションで作成した AxDB<ph id="ph1">\_</ph>CopyForExport データベースに対して実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>This script makes the following changes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このスクリプトは、次の変更を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Set the <bpt id="p1">**</bpt>SysGlobalConfiguration<ept id="p1">**</ept> flag to inform Finance and Operations that the database is Azure-based.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysGlobalConfiguration<ept id="p1">**</ept> フラグを設定し、データベースが Azure ベースであることを Finance and Operations に知らせます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Remove a reference to tempDB in the XU<ph id="ph1">\_</ph>DisableEnableNonClusteredIndexes procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">XU<ph id="ph1">\_</ph>DisableEnableNonClusteredIndexes 手順で tempDB への参照を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>References to tempDB aren't allowed in an Azure SQL database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure SQL データベースでは、tempDB の参照が許可されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The database synchronization process will re-create the reference later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース同期プロセスは後で照会を再作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Drop users, because Microsoft Windows users are forbidden in Azure SQL databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows のユーザーは Azure SQL データベースで許可されていないため、ユーザーをドロップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Other users must be re-created later, so that they're correctly linked to the appropriate sign-in on the target server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のユーザーは、対象のサーバーの適切なサインインに正しくリンクされるように、後で再作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Clear encrypted hardware profile merchand properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗号化されたハードウェア プロファイルの merchand プロパティの消去</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>A successful export and import of the database requires all these changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのエクスポートとインポートに成功するには、これらすべての変更が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Export the database from SQL Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server からデータベースをエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window and run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The <bpt id="p1">**</bpt>140<ept id="p1">**</ept> folder reflects the current version, you are required to use the version that is available in your sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>140<ept id="p1">**</ept> フォルダーは、現在のバージョンを反映しており、サンドボックス環境で使用可能なバージョンを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>This may require you to install the <bpt id="p1">[</bpt>latest version of Management Studio<ept id="p1">](https://msdn.microsoft.com/en-us/library/mt238290.aspx)</ept> in your development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、開発環境に <bpt id="p1">[</bpt>Management Studio の最新バージョン<ept id="p1">](https://msdn.microsoft.com/en-us/library/mt238290.aspx)</ept> をインストールする必要が生じる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Here is an explanation of the parameters:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメータの説明を以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source><bpt id="p1">**</bpt>ssn (source server name)<ept id="p1">**</ept> – The name of the SQL Server to export from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ssn(ソース サーバー名)<ept id="p1">**</ept> – エクスポートする SQL Server の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For the purposes of this topic, the name should always be <bpt id="p1">**</bpt>localhost<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、名前は常に <bpt id="p1">**</bpt>localhost<ept id="p1">**</ept> である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>sdn (source database name)<ept id="p1">**</ept> – The name of the database to export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>sdn(ソース データベース名)<ept id="p1">**</ept> – エクスポートするデータベースの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>tf (target file)<ept id="p1">**</ept> – The path and name of the file to export to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tf(ターゲット ファイル)<ept id="p1">**</ept> – エクスポートするファイルのパスと名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>The folder should already exist, but the export process will create the file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォルダーはすでに存在しているはずですが、エクスポート プロセスによってファイルが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Import the database into an Azure SQL database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure SQL データベースへのデータベースのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Copy the .bacpac file that was generated in the previous section to the AOS computer in the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のセクションで生成された .bacpac ファイルをターゲット環境の AOS コンピュータにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>A typical .bacpac file for a golden database will be smaller than 100 MB.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ゴールデン データベースの標準的な .bacpac ファイルは、100 MB より小さくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Therefore, you can copy and paste the file through a Remote Desktop Protocol (RDP) window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、リモート デスクトップ プロトコル (RDP) ウィンドウを使用してファイルをコピーして貼り付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>If the .bacpac file is much larger than 100 MB, <bpt id="p1">[</bpt>upload it to an Azure storage account<ept id="p1">](https://azure.microsoft.com/en-gb/documentation/articles/storage-use-azcopy/)</ept>, and then download it to the target AOS computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.Bacpac ファイルが 100 MB よりも大きい場合、<bpt id="p1">[</bpt>Azure ストレージ アカウントにアップロード<ept id="p1">](https://azure.microsoft.com/en-gb/documentation/articles/storage-use-azcopy/)</ept>し、対象となる AOS コンピューターにダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、Finance and Operations の契約の一部としてストレージ アカウントを提供しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>You must either purchase a storage account or use a storage account from a separate Azure subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>For performance reasons, we recommend that you put the .bacpac file on drive D on the AOS computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス上の理由から、.bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>(For more information, see the "Known issues and limitations" section.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(詳細については、「既知の問題と制限事項」セクションを参照してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window and run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>The version of SqlPackage.exe must match the version used to export the .bacpac file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SqlPackage.exe のバージョンは、.bacpac ファイルのエクスポートに使用するバージョンと一致する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>You may be required to install the <bpt id="p1">[</bpt>latest version of Management Studio<ept id="p1">](https://msdn.microsoft.com/en-us/library/mt238290.aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Management Studio の最新バージョン<ept id="p1">](https://msdn.microsoft.com/en-us/library/mt238290.aspx)</ept> のインストールが必要な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Here is an explanation of the parameters:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメータの説明を以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source><bpt id="p1">**</bpt>tsn (target server name)<ept id="p1">**</ept> – The name of the Azure SQL Database server to import to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tsn(ターゲット サーバー名)<ept id="p1">**</ept> – インポートする Azure SQL データベース サーバーの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>You can find the name in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を LCS で見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Add the suffix <bpt id="p1">**</bpt>database.windows.net<ept id="p1">**</ept> to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接尾語 <bpt id="p1">**</bpt>database.windows.net<ept id="p1">**</ept> を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source><bpt id="p1">**</bpt>tdn (target database name)<ept id="p1">**</ept> – The name of the database to import into.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tdn(ターゲット データベース名)<ept id="p1">**</ept> – インポートするデータベースの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The database should <bpt id="p1">**</bpt>not<ept id="p1">**</ept> already exist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースが既に存在していては<bpt id="p1">**</bpt>いけません<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>The import process will create it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート処理が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source><bpt id="p1">**</bpt>sf (source file)<ept id="p1">**</ept> – The path and name of the file to import from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>sf(ソース ファイル)<ept id="p1">**</ept> – インポートするファイルのパスと名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source><bpt id="p1">**</bpt>tu (target user)<ept id="p1">**</ept> – The SQL user name for the target Azure SQL database instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tu(ターゲット ユーザー)<ept id="p1">**</ept> – ターゲットの Azure SQL データベース インスタンスの SQL ユーザー名。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>We recommend that you use the standard <bpt id="p1">**</bpt>sqladmin<ept id="p1">**</ept> user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準の <bpt id="p1">**</bpt>sqladmin<ept id="p1">**</ept> ユーザーを使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>You can retrieve the password for this user from your LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトからは、このユーザーのパスワードを取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source><bpt id="p1">**</bpt>tp (target password)<ept id="p1">**</ept> – The password for the target Azure SQL database user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tp(ターゲット パスワード)<ept id="p1">**</ept> – ターゲットの Azure SQL データベース ユーザーのパスワード。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source><bpt id="p1">**</bpt>DatabaseServiceObjective<ept id="p1">**</ept> – Specifies the performance level of the database such as S1, P2, or P4.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DatabaseServiceObjective<ept id="p1">**</ept> – S1、P2、P4 などのデータベースのパフォーマンス レベルを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>To meet performance requirements and comply with your service agreement, use the same service objective level as the current Finance and Operations database (AXDB) on this environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス要件を満たし、サービス契約を遵守するには、現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルをこの環境で使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>To query the service level objective of the current database, run the following query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のデータベースのサービス レベル目標を照会するには、次のクエリを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>You will receive the following warning message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の警告メッセージを受け取ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>You can safely ignore it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは無視してかまいません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>A project which specifies SQL Server 2016 as the target platform may experience compatibility issues with Microsoft Azure SQL Database v12.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット プラットフォームとして SQL Server 2016 を指定するプロジェクトでは、Microsoft Azure SQL データベース v12 で互換性の問題が発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Retaining copies of the database for an extended period is not allowed in any Finance and Operations environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どの Finance and Operations 環境でも、長期間にわたってデータベースのコピーを保持することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Microsoft reserves the right to delete any copies of the database older than 7 days without any prior notice.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、事前に通知することなく、7 日を超える古いデータベースのコピーを削除する権限を保有します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Update the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Run the following script against the imported database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートされたデータベースに対して、次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The script performs the following actions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトでは次のアクションを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Re-create database users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース ユーザーを再作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Set the correct performance parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切な実績パラメーターを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Enable the SQL Query Store feature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Query Store 機能を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>You must add the tenant ID to the last three queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テナント ID を最後の 3 つのクエリに追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>You can find this value by querying the SysServiceConfigurationSetting table in an existing database in the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この値はターゲット環境内の既存のデータベースで SysServiceConfigurationSetting テーブルをクエリすることにより見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Synchronize the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの同期</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Use Remote Desktop to connect to all the computers in the target environment, and stop the following Windows services by using services.msc.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップを使用して、ターゲット環境内のすべてのコンピュータに接続し、services.msc を使用して次の Microsoft Windows サービスを停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>These services will have open connections to the Finance and Operations database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>After you stop the services, you can replace the existing Finance and Operations database with the newly imported database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービスを停止した後に、既存の Finance and Operations データベースを新しくインポートされたデータベースに置き換えることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>World wide web publishing service (on all AOS computers)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Management Reporter 2012 Process Service (on business intelligence <ph id="ph1">\[</ph>BI<ph id="ph2">\]</ph> computers only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter 2012 のプロセス サービス (ビジネス インテリジェンス <ph id="ph1">\[</ph>BI<ph id="ph2">\]</ph> コンピューターのみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>On the AOS computer where the bacpac import was done, run the following script in Management Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">bacpac インポートが行われた AOS コンピューターで、Management Studio の次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>This script renames the original database and then renames the newly imported database so that it uses the original database name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このスクリプトは、元のデータベースの名前を変更し、新しくインポートされたデータベースの名前を変更して元のデータベース名を使用するようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>In this example, the original database was named axdb<ph id="ph1">\_</ph>123456789, and the newly imported database was named importeddb.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、元のデータベースは axdb<ph id="ph1">\_</ph>123456789 という名前が付けられ、新しくインポートされたデータベースは importeddb という名前が付けられました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Make sure that the you're using the SQL Server 2016 version of Management Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio の SQL Server 2016 バージョンを使用していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Synchronize the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを同期させます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window as an administrator, and run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として <bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Use services.msc to restart the services that you stopped earlier:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">services.msc を使用して、以前に停止したサービスを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>World wide web publishing service (on all AOS computers)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Management Reporter 2012 Process Service (on BI computers only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>At this point, you can open the Finance and Operations application URL and sign in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この時点で、Finance and Operations アプリケーション URL を開いてサイン インすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Verify that the application works as you expect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションが予期したとおりに動作することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Then drop the original database by running the following script in Management Studio on the AOS computer where you did the bacpac import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、bacpac のインポートを行った AOS コンピューターの Management Studio で以下のスクリプトを実行して、元のデータベースを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Enable change tracking</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更追跡の有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>If change tracking was enabled in the source database, ensure to enable change tracking again in the newly provisioned database in the target environment using the ALTER DATABASE command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース データベースで変更追跡が有効になっている場合は、ALTER DATABASE コマンドを使用して、ターゲット環境の新たなプロビジョニング データベースで変更追跡を再度有効にしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>To ensure current version of the store procedure (related to change tracking) is used in the new database, you must enable/disable change tracking for a data entity in data management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータベースで店舗の業務手順の現在のバージョン (変更追跡に関連する) が使用されていることを確認するには、データ管理のデータ エンティティの変更追跡を有効または無効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>This can be done on any entity as this is needed to trigger the refresh of store procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、店舗の業務手順の更新をトリガーするために必要なので、どのエンティティでも実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Re-provision the target environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対象の環境を再プロビジョニング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Reset the Financial Reporting database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務報告データベースのリセット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If you're using Financial Reporting, which was previously named Management Reporter, you must reset the Financial Reporting database by following the steps in <bpt id="p1">[</bpt>Resetting the financial reporting data mart after restoring a database<ept id="p1">](../analytics/reset-financial-reporting-datamart-after-restore.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter という以前の名前を持った財務報告を使用する場合は、<bpt id="p1">[</bpt>データベースを復元した後の財務報告のデータ マートのリセット<ept id="p1">](../analytics/reset-financial-reporting-datamart-after-restore.md)</ept>の手順に従って、財務報告データベースをリセットする必要があります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Submit a service request to copy the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースをコピーするサービス要求を送信</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>To copy the golden database to a production environment, you must submit a service request of the <bpt id="p1">**</bpt>Sandbox to Production<ept id="p1">**</ept> type in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ゴールデン データベースを実稼働環境にコピーするには、LCS に <bpt id="p1">**</bpt>サンドボックスから実稼働環境<ept id="p1">**</ept> タイプのサービス要求を送信する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>In this request, you ask that Microsoft run the copy action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求では、Microsoft がコピー操作を実行することを求めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>You can't use a request of the <bpt id="p1">**</bpt>Database refresh request<ept id="p1">**</ept> type, because the request involves copying to a production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求には実稼働環境へのコピーが含まれるので、<bpt id="p1">**</bpt>データベースを最新の情報に更新要求<ept id="p1">**</ept> タイプの要求を使用することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>In LCS, on the Project home page, select <bpt id="p1">**</bpt>Service requests<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS のプロジェクト ホーム ページで、<bpt id="p1">**</bpt>サービス要求<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>On the <bpt id="p1">**</bpt>Service requests<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>Sandbox to Production<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サービス要求<ept id="p1">**</ept> ページで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept> を選択し、<bpt id="p3">**</bpt>サンドボックスから実稼働環境<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>In the <bpt id="p1">**</bpt>Sandbox to Production<ept id="p1">**</ept> dialog box, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サンドボックスから実稼働環境<ept id="p1">**</ept> ダイアログ ボックスで、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>In the <bpt id="p1">**</bpt>Environment name<ept id="p1">**</ept> field, select the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境名<ept id="p1">**</ept>フィールドで、実稼動環境を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Set the <bpt id="p1">**</bpt>Preferred downtime start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Preferred downtime end date<ept id="p2">**</ept> fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ダウンタイム開始日を優先<ept id="p1">**</ept> および <bpt id="p2">**</bpt>ダウンタイム終了日を優先<ept id="p2">**</ept> フィールドを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>The end date must be at least one hour after the start date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイクル終了日は、サイクル開始日の少なくとも 1 時間後でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>To help guarantee that resources are available to run the request, submit your request at least 24 hours before your preferred downtime window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求を実行するためのリソースが確保されるようにするには、推奨ダウンタイム ウィンドウの少なくとも 24 時間前にリクエストを送信してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Select the check boxes at the bottom to agree to the terms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">下部にあるチェック ボックスをオンにして、条項に同意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Additional steps for Retail environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売環境の追加手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>If your environment includes Retail components, you must perform additional steps to help guarantee that the environment will work after the database import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境に、Retail のコンポーネントが含まれている場合、追加の手順を実行して、データベースのインポート後に環境が機能することを保証する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Re-enter encrypted and environment-specific values in the target database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット データベースの暗号化された環境固有の値を再入力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The values on the following pages are encrypted in the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のページの値は、データベースで暗号化されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Therefore, all the imported values will be incorrect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、インポートされた値はすべて正しくありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Payments services (<bpt id="p1">**</bpt>Accounts receivable<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Payments setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Payments services<ept id="p3">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払サービス (<bpt id="p1">**</bpt>売掛金勘定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>支払設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>支払サービス<ept id="p3">**</ept>) に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Hardware profiles (<bpt id="p1">**</bpt>Retail and commerce<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS setup<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS profiles<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Hardware profiles<ept id="p5">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア プロファイル (<bpt id="p1">**</bpt>小売りとコマース<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>チャネル設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS 設定<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS プロファイル<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>ハードウェア プロファイル<ept id="p5">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>In the target system, open these pages, and enter the values that you documented earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット システムで、これらのページを開き、前に記録した値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Re-enter data from encrypted and environment-specific fields in the target database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット データベースの暗号化された環境固有のフィールドからデータを再入力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>In the Finance and Operations client, enter the values that you documented for the encrypted and environment-specific fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations クライアントでは、暗号化された環境固有のフィールドに記録した値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>The following fields are affected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のフィールドが影響されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>The field names are given in Table.Field format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名は Table.Field 形式で指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Field name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Where to set the value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値を設定する場所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>CreditCardAccountSetup.SecureMerchantProperties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreditCardAccountSetup.SecureMerchantProperties</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Select <bpt id="p1">**</bpt>Accounts receivable<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Payments setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Payment services<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>売掛金勘定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>支払設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>支払サービス<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>ExchangeRateProviderConfigurationDetails.Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ExchangeRateProviderConfigurationDetails.Value</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Select <bpt id="p1">**</bpt>General ledger<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Currencies<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Configure exchange rate providers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>総勘定元帳<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>通貨<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>為替レート プロバイダーを構成する<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>FiscalEstablishment<ph id="ph1">\_</ph>BR.ConsumerEFDocCsc</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FiscalEstablishment<ph id="ph1">\_</ph>BR.ConsumerEFDocCsc</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Select <bpt id="p1">**</bpt>Organization administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Fiscal establishments<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Fiscal establishments<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>組織管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>会計機関<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>会計機関<ept id="p3">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>FiscalEstablishmentStaging.CSC</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FiscalEstablishmentStaging.CSC</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>This field is used by DIXF.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは DIXF で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>HcmPersonIdentificationNumber.PersonIdentificationNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HcmPersonIdentificationNumber.PersonIdentificationNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Select <bpt id="p1">**</bpt>Human resources<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Workers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Workers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>人事管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>作業者<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>作業者<ept id="p3">**</ept> の順に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>On the <bpt id="p1">**</bpt>Worker<ept id="p1">**</ept> tab, in the <bpt id="p2">**</bpt>Personal information<ept id="p2">**</ept> group, select <bpt id="p3">**</bpt>Identification numbers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ワーカー<ept id="p1">**</ept>タブの、<bpt id="p2">**</bpt>個人情報<ept id="p2">**</ept>グループで、<bpt id="p3">**</bpt>ID 番号<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>HcmWorkerActionHire.PersonIdentificationNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HcmWorkerActionHire.PersonIdentificationNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>This field has been obsolete since AX 7.0 (February 2016).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、AX 7.0 以降 (2016 年 2 月) は廃止されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>It previously appeared in the <bpt id="p1">**</bpt>All worker actions<ept id="p1">**</ept> form (<bpt id="p2">**</bpt>Human resources<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Workers<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Actions<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>All worker actions<ept id="p5">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは以前、<bpt id="p1">**</bpt>すべての作業者アクション<ept id="p1">**</ept> フォーム (<bpt id="p2">**</bpt>人事管理<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>作業者<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>アクション<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>すべての作業者アクション<ept id="p5">**</ept>) に表示されていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>SysEmailSMPTPassword.Password</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysEmailSMPTPassword.Password</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Select <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Email<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Email parameters<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>電子メール<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>電子メール パラメーター<ept id="p3">**</ept> の順に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>SysOAuthUserTokens.EncryptedAccessToken</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysOAuthUserTokens.EncryptedAccessToken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>This field is used internally by AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、AOS で内部的に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>It can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは無視できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>SysOAuthUserTokens.EncryptedRefreshToken</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysOAuthUserTokens.EncryptedRefreshToken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>This field is used internally by AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、AOS で内部的に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>It can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは無視できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Known issues and limitations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既知の問題と制限事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>I can't download the Management Studio installer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio インストーラーをダウンロードできません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>When you try to download the Management Studio installer, you might receive the following message:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio インストーラーをダウンロードしようとすると、次のメッセージが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Your current security settings do not allow this file to be downloaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のセキュリティ設定では、このファイルをダウンロードすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>To work around this issue, follow these steps to enable file downloads.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を回避するには、次の手順を実行してファイルのダウンロードを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In your web browser, open <bpt id="p1">**</bpt>Internet options<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web ブラウザーで<bpt id="p1">**</bpt>インターネット オプション<ept id="p1">**</ept>を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>On the <bpt id="p1">**</bpt>Security<ept id="p1">**</ept> tab, select the <bpt id="p2">**</bpt>Internet<ept id="p2">**</ept> zone, and then select <bpt id="p3">**</bpt>Custom level<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セキュリティ<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>インターネット<ept id="p2">**</ept>ゾーンを選択し、<bpt id="p3">**</bpt>レベルのカスタマイズ<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Scroll to <bpt id="p1">**</bpt>Downloads<ept id="p1">**</ept>, and then, under <bpt id="p2">**</bpt>File download<ept id="p2">**</ept>, select the <bpt id="p3">**</bpt>Enable<ept id="p3">**</ept> option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ダウンロード<ept id="p1">**</ept> までスクロールし、<bpt id="p2">**</bpt>ファイルのダウンロード<ept id="p2">**</ept> で <bpt id="p3">**</bpt>有効にする<ept id="p3">**</ept> オプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Performance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>The following guidelines can help you achieve optimal performance:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のガイドラインは、最適なパフォーマンスを達成するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Always export from a computer that is in the same Azure datacenter as the Azure SQL database instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">常に Azure SQL データベース インスタンスと同じ Azure データ センター内にあるコンピューターからエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>In practice, this guideline means that when you export a copy of your sandbox database, you should export it from the sandbox AOS computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実際、このガイドラインはサンドボックス データベースのコピーをエクスポートするときに、サンドボックス AOS コンピューターからエクスポートする必要があることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Always import the .bacpac file locally on the computer that runs the SQL Server instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">常に .bacpac ファイルを SQL Server インスタンスを実行するコンピューターにローカルでインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Don't import it from Management Studio on a remote computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート コンピューターで Management Studio からインポートしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>In a one-box environment that is hosted in Azure, put the .bacpac file on drive D when you export it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure でホストされている 1 ボックス環境では、エクスポートするときに D ドライブに .bacpac ファイルを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>(A one-box environment is also known as a Tier 1 environment.) For more information about the temporary drive on Azure computers, see the <bpt id="p1">[</bpt>Understanding the temporary drive on Windows Azure Virtual Machines<ept id="p1">](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)</ept> post on the Azure Support Team blog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ワンボックス環境はレベル 1 環境とも呼ばれます。) Azure コンピューター 上でのテンポラリー ドライブに関する詳細については、<bpt id="p1">[</bpt>Windows Azure 仮想マシンのテンポラリー ドライブを理解する<ept id="p1">](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)</ept> Azure サポート チームのブログ投稿を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Grant the account that runs the SQL Server Windows service <bpt id="p1">[</bpt>Instance File Initialization<ept id="p1">](https://msdn.microsoft.com/en-us/library/ms175935.aspx)</ept> rights.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Windows サービス <bpt id="p1">[</bpt>インスタンス ファイルの初期化<ept id="p1">](https://msdn.microsoft.com/en-us/library/ms175935.aspx)</ept> を実行するアカウントに権限を付与します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>In this way, you can help improve the speed of the import process and the speed of a restore from a <ph id="ph1">\*</ph>.bak file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、インポート処理の速度および <ph id="ph1">\*</ph>.bak ファイルからの復元の速度を向上させることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>For a developer environment, you can easily make sure that the account that runs the SQL Server service has these rights by setting SQL Server to run as the axlocaladmin account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者環境では、axlocaladmin アカウントとして実行する SQL Server を設定することにより、SQL Server サービスを実行するアカウントがこれらの権限を持っていることを簡単に確認することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>We recommend that you not use the option to export and import from Azure SQL Database in Management Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio の Azure SQL データベースからエクスポートおよびインポートするオプションを使用しないことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>(This option is also known as <bpt id="p1">**</bpt>Export data tier application<ept id="p1">**</ept>.) You should not use this option because there can be memory limitations for larger databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(このオプションは、<bpt id="p1">**</bpt>データ層アプリケーションのエクスポート<ept id="p1">**</ept>とも呼ばれます。) 大規模なデータベースにはメモリーの制限があるため、このオプションは使用しないでください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
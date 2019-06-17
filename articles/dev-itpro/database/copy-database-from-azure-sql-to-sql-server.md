<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="copy-database-from-azure-sql-to-sql-server.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>copy-database-from-azure-sql-to-sql-server.567a2d.3ea81f46ca3e48578deca7e58cd794671f7e98e0.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>3ea81f46ca3e48578deca7e58cd794671f7e98e0</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\database\copy-database-from-azure-sql-to-sql-server.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Copy Finance and Operations databases from Azure SQL Database to SQL Server environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations データベースを Azure SQL データベースから SQL Server 環境にコピーする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to move a Microsoft Dynamics 365 for Finance and Operations database from an Azure-based environment to a SQL Server–based environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースを Azure ベースの環境から SQL Server ベースの環境に移動する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Copy Finance and Operations databases from Azure SQL Database to SQL Server environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations データベースを Azure SQL データベースから SQL Server 環境にコピーする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to export a Microsoft Dynamics 365 for Finance and Operations database from an environment that is based on Microsoft Azure and import it into an environment that is based on Microsoft SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースを、Microsoft Azure に基づいた環境からエクスポートし、Microsoft SQL Server に基づいた環境にインポートする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>To move a database, use the self-service action to export the database from Azure SQL Database and then import it into Microsoft SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを移動するには、セルフ サービス アクションを使用して Azure SQL データベースからデータベースをエクスポートし、Microsoft SQL Server にインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Because the file name extension for the exported data is .bacpac, this process is often referred to as the <bpt id="p1">*</bpt>bacpac process<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートされたデータのファイル名拡張子は .bacpac なので、このプロセスは多くの場合 <bpt id="p1">*</bpt>bacpac プロセス<ept id="p1">*</ept>と呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The high-level process for a database move includes the following phases:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース移動の高レベルのプロセスには、次のフェーズが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Export your source environment to the LCS Asset Library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS 資産ライブラリにソース環境をエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Import the database into SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server にデータベースをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Run a SQL script to update the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの更新のため SQL スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The following prerequisites must be met before you can move a database:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを移動するには、次の前提条件を満たす必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The source environment (that is, the environment that is connected to the source database) must run a version of the Finance and Operations platform that is earlier than or the same as the version of the platform that the destination environment runs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース環境 (つまりソース データベースに接続されている環境) は、ターゲット環境が実行されているプラットフォームのバージョンよりも前または同じバージョンの Finance and Operations プラットフォームを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Only a sandbox environment database can be exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス環境データベースのみをエクスポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>If you must copy the production environment, you must first refresh that environment to the sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境をコピーする必要がある場合は、最初に、その環境をサンド ボックス環境に更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In this topic, the term <bpt id="p1">*</bpt>sandbox<ept id="p1">*</ept> is used to refer to a Standard or Premier Acceptance Testing (Tier 2+) or higher environment connected to a SQL Azure database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、<bpt id="p1">*</bpt>サンドボックス<ept id="p1">*</ept> という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 以上)、またはより高度な環境を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The destination SQL Server environment must run SQL Server 2016 Release to Manufacturing (RTM) (13.00.1601.5) or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出力先の SQL Server 環境では、SQL Server 2016 Release to Manufacturing (RTM) (13.00.1601.5) 以降を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The Community Technology Preview (CTP) versions of SQL Server 2016 might cause errors during the import process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server 2016 の Community Technology Preview (CTP) バージョンでは、インポート処理中にエラーが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Before you begin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Encrypted and environment-specific values can't be imported into a new environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗号化された環境固有の値を新しい環境にインポートすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>After you've completed the import, you must re-enter some data from your source environment in your target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート処理を完了した後は、ターゲット環境内のソース環境から一部のデータを再入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Document the values of encrypted fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗号化されたフィールドの値を文書化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Because of a technical limitation that is related to the certificate that is used for data encryption, values that are stored in encrypted fields in a database will be unreadable after that database is imported into a new environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ暗号化に使用される証明書に関連する技術的な制限のため、データベースの暗号化されたフィールドに格納されている値はそのデータベースが新しい環境にインポートされた後は読み取れません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Therefore, after an import, you must manually delete and re-enter values that are stored in encrypted fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、インポート後、暗号化されたフィールドに格納されている値を手動で削除して再入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>New values that are entered in encrypted fields after an import will be readable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート後に暗号化されたフィールドに入力される新しい値は読み取り可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The following fields are affected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のフィールドが影響されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The field names are given in Table.Field format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名は Table.Field 形式で指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Field name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Where to set the value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値を設定する場所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>CreditCardAccountSetup.SecureMerchantProperties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreditCardAccountSetup.SecureMerchantProperties</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Select <bpt id="p1">**</bpt>Accounts receivable<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Payments setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Payment services<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>売掛金勘定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>支払設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>支払サービス<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>ExchangeRateProviderConfigurationDetails.Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ExchangeRateProviderConfigurationDetails.Value</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Select <bpt id="p1">**</bpt>General ledger<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Currencies<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Configure exchange rate providers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>総勘定元帳<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>通貨<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>為替レート プロバイダーを構成する<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>FiscalEstablishment<ph id="ph1">\_</ph>BR.ConsumerEFDocCsc</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FiscalEstablishment<ph id="ph1">\_</ph>BR.ConsumerEFDocCsc</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Select <bpt id="p1">**</bpt>Organization administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Fiscal establishments<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Fiscal establishments<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>組織管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>会計機関<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>会計機関<ept id="p3">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>FiscalEstablishmentStaging.CSC</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FiscalEstablishmentStaging.CSC</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>This field is used by the Data Import/Export Framework (DIXF).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>HcmPersonIdentificationNumber.PersonIdentificationNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HcmPersonIdentificationNumber.PersonIdentificationNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Select <bpt id="p1">**</bpt>Human resources<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Workers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Workers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>人事管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>作業者<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>作業者<ept id="p3">**</ept> の順に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>On the <bpt id="p1">**</bpt>Worker<ept id="p1">**</ept> tab, in the <bpt id="p2">**</bpt>Personal information<ept id="p2">**</ept> group, select <bpt id="p3">**</bpt>Identification numbers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ワーカー<ept id="p1">**</ept>タブの、<bpt id="p2">**</bpt>個人情報<ept id="p2">**</ept>グループで、<bpt id="p3">**</bpt>ID 番号<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>HcmWorkerActionHire.PersonIdentificationNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HcmWorkerActionHire.PersonIdentificationNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>This field has been obsolete since Microsoft Dynamics AX 7.0 (February 2016).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) は廃止されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>It was previously in the <bpt id="p1">**</bpt>All worker actions<ept id="p1">**</ept> form (<bpt id="p2">**</bpt>Human resources<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Workers<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Actions<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>All worker actions<ept id="p5">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは以前、<bpt id="p1">**</bpt>すべての作業者アクション<ept id="p1">**</ept> フォーム (<bpt id="p2">**</bpt>人事管理<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>作業者<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>アクション<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>すべての作業者アクション<ept id="p5">**</ept>) でした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>SysEmailSMTPPassword.Password</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysEmailSMTPPassword.Password</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Select <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Email<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Email parameters<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>電子メール<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>電子メール パラメーター<ept id="p3">**</ept> の順に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>SysOAuthUserTokens.EncryptedAccessToken</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysOAuthUserTokens.EncryptedAccessToken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>This field is used internally by AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、AOS で内部的に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>It can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは無視できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>SysOAuthUserTokens.EncryptedRefreshToken</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysOAuthUserTokens.EncryptedRefreshToken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>This field is used internally by AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、AOS で内部的に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>It can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは無視できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If you're running Retail components, document encrypted and environment-specific values</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネントを実行している場合は、暗号化された、環境固有の値を文書化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The values on the following pages are either environment-specific or encrypted in the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のページの値は、環境固有またはデータベースで暗号化されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Therefore, all the imported values will be incorrect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、インポートされた値はすべて正しくありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Payments services (<bpt id="p1">**</bpt>Accounts receivable<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Payments setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Payments services<ept id="p3">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払サービス (<bpt id="p1">**</bpt>売掛金勘定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>支払設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>支払サービス<ept id="p3">**</ept>) に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Hardware profiles (<bpt id="p1">**</bpt>Retail and commerce<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS setup<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS profiles<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Hardware profiles<ept id="p5">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア プロファイル (<bpt id="p1">**</bpt>小売りとコマース<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>チャネル設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS 設定<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS プロファイル<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>ハードウェア プロファイル<ept id="p5">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Self-service database export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのセルフ サービスエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Import the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>After you have downloaded a .bacpac file, you can begin the manual import operation on your Tier 1 environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.bacpac ファイルをダウンロードした後、レベル 1 環境の手動インポート操作を開始することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>When you import the database, we recommend that you follow these guidelines:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースをインポートするときは、これらのガイドラインに従うことお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Retain a copy of the existing AxDB database so that you can revert to it later, if needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な場合は、後で戻すことができるように、既存の AxDB データベースのコピーを保持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Import the new database under a new name, such as <bpt id="p1">**</bpt>AxDB<ph id="ph1">\_</ph>fromProd<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AxDB<ph id="ph1">\_</ph>fromProd<ept id="p1">**</ept> などの新しい名前の下に新しいデータベースをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>To help ensure the best performance, copy the <ph id="ph1">\*</ph>.bacpac file to the local computer that you're importing from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最高のパフォーマンスを確保するには、<ph id="ph1">\*</ph>.bacpac ファイルをインポート元のローカル コンピューターにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window and run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Here is an explanation of the parameters:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメータの説明を以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>tsn (target server name)<ept id="p1">**</ept> – The name of the SQL Server to import into.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tsn(ターゲット サーバー名)<ept id="p1">**</ept> – インポートする SQL Server の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">**</bpt>tdn (target database name)<ept id="p1">**</ept> – The name of the database to import into.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tdn(ターゲット データベース名)<ept id="p1">**</ept> – インポートするデータベースの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The database should <bpt id="p1">**</bpt>not<ept id="p1">**</ept> already exist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースが既に存在していては<bpt id="p1">**</bpt>いけません<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>sf (source file)<ept id="p1">**</ept> – The path and name of the file to import from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>sf(ソース ファイル)<ept id="p1">**</ept> – インポートするファイルのパスと名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>During import, the user name and password aren't required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート中に、ユーザー名およびパスワードは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>By default, SQL Server uses Microsoft Windows authentication for the user who is currently signed in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、SQL Server は、現在サインインしているユーザーに対して Microsoft Windows 認証を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Update the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Run the following SQL script against the imported database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートされたデータベースに対して、次の SQL スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>This script adds back the users that you deleted from the source database and correctly links them to the SQL logins for this SQL instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このスクリプトは、ソース データベースから削除したユーザーを追加し、この SQL インスタンスの SQL のログインに正しくリンクします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The script also turns change tracking back on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトはまた、変更の追跡を元に戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Remember to edit the final <bpt id="p1">**</bpt>ALTER DATABASE<ept id="p1">**</ept> statement so that it uses the name of your database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必ず、データベースの名前を使用できるように、最後の <bpt id="p1">**</bpt>ALTER DATABASE<ept id="p1">**</ept> ステートメントを編集してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Enable change tracking</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更追跡の有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>If change tracking was enabled in the source database, ensure to enable change tracking again in the newly provisioned database in the target environment using the ALTER DATABASE command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース データベースで変更追跡が有効になっている場合は、ALTER DATABASE コマンドを使用して、ターゲット環境の新たなプロビジョニング データベースで変更追跡を再度有効にしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>To ensure that the current version of the store procedure (related to change tracking) is used in the new database, you must enable/disable change tracking for a data entity in data management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータベースで店舗の業務手順の現在のバージョン (変更追跡に関連する) が使用されていることを確認するには、データ管理のデータ エンティティの変更追跡を有効または無効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>This can be done on any entity, as this is needed to trigger the refresh of store procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、店舗の業務手順の更新をトリガーするために必要なので、どのエンティティでも実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Start to use the new database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータベースの使用を開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>To switch the environment and use the new database, first stop the following services:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境を切り替えて新しいデータベースを使用するには、最初に次のサービスを停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>World Wide Web Publishing Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">World Wide Web 公開サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Microsoft Dynamics 365 Unified Operations: Batch Management Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 Unified Operations: バッチ管理サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Management Reporter 2012 Process Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter 2012 処理サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>After the services have been stopped, rename the AxDB database <bpt id="p1">**</bpt>AxDB<ph id="ph1">\_</ph>orig<ept id="p1">**</ept>, rename your newly imported database <bpt id="p2">**</bpt>AxDB<ept id="p2">**</ept>, and then restart the three services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービスが停止した後、AxDB データベース <bpt id="p1">**</bpt>AxDB<ph id="ph1">\_</ph>orig<ept id="p1">**</ept> の名前を変更し、新しくインポートしたデータベース <bpt id="p2">**</bpt>AxDB<ept id="p2">**</ept> の名前を変更し、そして 3 つのサービスを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>To rename the database, use the following ALTER DATABASE command:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの名前を変更するには、次の ALTER DATABASE コマンドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>To switch back to the original database, reverse this process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元のデータベースに戻すには、このプロセスを逆にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>In other words, stop the services, rename the databases, and then restart the services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、サービスを停止し、データベースの名前を変更してから、サービスを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Re-provision the target environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対象の環境を再プロビジョニング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Reset the Financial Reporting database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務報告データベースのリセット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>If you're using Financial Reporting, which was previously named Management Reporter, you must reset the Financial Reporting database by following the steps in <bpt id="p1">[</bpt>Resetting the financial reporting data mart after restoring a database<ept id="p1">](../analytics/reset-financial-reporting-datamart-after-restore.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter という以前の名前を持った財務報告を使用する場合は、<bpt id="p1">[</bpt>データベースを復元した後の財務報告のデータ マートのリセット<ept id="p1">](../analytics/reset-financial-reporting-datamart-after-restore.md)</ept>の手順に従って、財務報告データベースをリセットする必要があります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Re-enter data from encrypted and environment-specific fields in the target database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット データベースの暗号化された環境固有のフィールドからデータを再入力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>In the Finance and Operations client, enter the values that you documented for the encrypted and environment-specific fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations クライアントでは、暗号化された環境固有のフィールドに記録した値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>The following fields are affected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のフィールドが影響されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>The field names are given in Table.Field format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名は Table.Field 形式で指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Field name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Where to set the value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値を設定する場所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>CreditCardAccountSetup.SecureMerchantProperties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreditCardAccountSetup.SecureMerchantProperties</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Select <bpt id="p1">**</bpt>Accounts receivable<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Payments setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Payment services<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>売掛金勘定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>支払設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>支払サービス<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>ExchangeRateProviderConfigurationDetails.Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ExchangeRateProviderConfigurationDetails.Value</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Select <bpt id="p1">**</bpt>General ledger<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Currencies<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Configure exchange rate providers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>総勘定元帳<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>通貨<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>為替レート プロバイダーを構成する<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>FiscalEstablishment<ph id="ph1">\_</ph>BR.ConsumerEFDocCsc</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FiscalEstablishment<ph id="ph1">\_</ph>BR.ConsumerEFDocCsc</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Select <bpt id="p1">**</bpt>Organization administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Fiscal establishments<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Fiscal establishments<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>組織管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>会計機関<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>会計機関<ept id="p3">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>FiscalEstablishmentStaging.CSC</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FiscalEstablishmentStaging.CSC</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>This field is used by DIXF.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは DIXF で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>HcmPersonIdentificationNumber.PersonIdentificationNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HcmPersonIdentificationNumber.PersonIdentificationNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Select <bpt id="p1">**</bpt>Human resources<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Workers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Workers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>人事管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>作業者<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>作業者<ept id="p3">**</ept> の順に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Worker<ept id="p1">**</ept> tab, in the <bpt id="p2">**</bpt>Personal information<ept id="p2">**</ept> group, select <bpt id="p3">**</bpt>Identification numbers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ワーカー<ept id="p1">**</ept>タブの、<bpt id="p2">**</bpt>個人情報<ept id="p2">**</ept>グループで、<bpt id="p3">**</bpt>ID 番号<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>HcmWorkerActionHire.PersonIdentificationNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HcmWorkerActionHire.PersonIdentificationNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>This field has been obsolete since AX 7.0 (February 2016).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、AX 7.0 以降 (2016 年 2 月) は廃止されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>It was previously in the <bpt id="p1">**</bpt>All worker actions<ept id="p1">**</ept> form (<bpt id="p2">**</bpt>Human resources<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Workers<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Actions<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>All worker actions<ept id="p5">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは以前、<bpt id="p1">**</bpt>すべての作業者アクション<ept id="p1">**</ept> フォーム (<bpt id="p2">**</bpt>人事管理<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>作業者<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>アクション<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>すべての作業者アクション<ept id="p5">**</ept>) でした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>SysEmailSMTPPassword.Password</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysEmailSMTPPassword.Password</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Select <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Email<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Email parameters<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>電子メール<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>電子メール パラメーター<ept id="p3">**</ept> の順に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>SysOAuthUserTokens.EncryptedAccessToken</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysOAuthUserTokens.EncryptedAccessToken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This field is used internally by AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、AOS で内部的に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>It can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは無視できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>SysOAuthUserTokens.EncryptedRefreshToken</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysOAuthUserTokens.EncryptedRefreshToken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>This field is used internally by AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、AOS で内部的に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>It can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは無視できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Known issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既知の問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>I can't download Management Studio installation files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio インストール ファイルをダウンロードできません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>When you try to download the Management Studio installer, you might receive the following error message:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio インストーラーをダウンロードしようとすると、次のエラー メッセージが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Your current security settings do not allow this file to be downloaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のセキュリティ設定では、このファイルをダウンロードすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>To work around this issue, follow these steps to enable file downloads.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を回避するには、次の手順を実行してファイルのダウンロードを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>In your web browser, open <bpt id="p1">**</bpt>Internet options<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web ブラウザーで<bpt id="p1">**</bpt>インターネット オプション<ept id="p1">**</ept>を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>On the <bpt id="p1">**</bpt>Security<ept id="p1">**</ept> tab, select the <bpt id="p2">**</bpt>Internet<ept id="p2">**</ept> zone, and then select <bpt id="p3">**</bpt>Custom level<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セキュリティ<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>インターネット<ept id="p2">**</ept>ゾーンを選択し、<bpt id="p3">**</bpt>レベルのカスタマイズ<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Scroll to <bpt id="p1">**</bpt>Downloads<ept id="p1">**</ept>, and then, under <bpt id="p2">**</bpt>File download<ept id="p2">**</ept>, select the <bpt id="p3">**</bpt>Enable<ept id="p3">**</ept> option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ダウンロード<ept id="p1">**</ept> までスクロールし、<bpt id="p2">**</bpt>ファイルのダウンロード<ept id="p2">**</ept> で <bpt id="p3">**</bpt>有効にする<ept id="p3">**</ept> オプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Database synchronization fails</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース同期の失敗</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>When you synchronize the database against the newly imported database from Microsoft Visual Studio, the synchronization might fail, and you might receive the following error message:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを Microsoft Visual Studio から新しくインポートされたデータベースと同期させると、その同期は失敗することがあり、次のエラー メッセージが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Failed to open SQL connection syncengine.exe exited with code -1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード 1 で終了した SQL connection syncengine.exe のオープンに失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>In this case, the following message is also logged under event ID 140 in the Windows application log:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、次のメッセージも Windows アプリケーション ログのイベント ID 140 で記録されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Object Server Database Synchronizer: The internal system table version number stored in the database is higher than the version supported by the kernel (141/138).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクト サーバー データベース シンクロナイザー: データベースに格納されている内部システム テーブル バージョン番号が、カーネル (141/138) でサポートされているバージョンよりも大きくなっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Use a newer Microsoft Dynamics kernel, or start Microsoft Dynamics using the -REPAIR command line parameter to enforce synchronization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい Microsoft Dynamics カーネルを使用するか、-REPAIR コマンドライン パラメーターを使用して Microsoft Dynamics を起動し、同期を強制します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>This issue can occur when the platform build number of the current environment is lower than the platform build number of the source environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、現在の環境のプラットフォーム ビルド番号がソース環境のプラットフォーム ビルド番号よりも低い場合に発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Depending on your circumstances, either use the <bpt id="p1">**</bpt>Updates<ept id="p1">**</ept> tiles on the LCS <bpt id="p2">**</bpt>Environment<ept id="p2">**</ept> page to upgrade the platform in the current environment so that it matches the platform in the source environment, or run the following query to adjust the expected version in the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">状況に応じて、LCS <bpt id="p2">**</bpt>環境<ept id="p2">**</ept>ページの<bpt id="p1">**</bpt>更新<ept id="p1">**</ept>タイルを使用して、現在の環境のプラットフォームをソース環境のプラットフォームと一致するようにアップグレードするか、次のクエリを実行してデータベースの必要なバージョンを調整します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>The value <bpt id="p1">**</bpt>138<ept id="p1">**</ept> in the preceding query is taken from the event log message, where version 138 was expected in this particular environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のクエリの値 <bpt id="p1">**</bpt>138<ept id="p1">**</ept> は、この特定の環境でバージョン 138 が予想されるイベント ログ メッセージから取得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Performance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The following guidelines can help you achieve optimal performance:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のガイドラインは、最適なパフォーマンスを達成するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Always export a database from a virtual machine (VM) that is in the same Azure datacenter as the Azure SQL database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">常に Azure SQL データベースと同じ Azure データ センター内にある仮想マシン (VM) からデータベースをエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>If you're exporting a copy of your sandbox database, export it from the sandbox AOS computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス データベースのコピーをエクスポートする場合は、サンド ボックス AOS コンピューターからエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Always import the .bacpac file locally on the computer that runs the SQL Server instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">常に .bacpac ファイルを SQL Server インスタンスを実行するコンピューターにローカルでインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Don't import it from Management Studio on a remote machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート マシンで Management Studio からインポートしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>In a Finance and Operations one-box environment that is hosted in Azure, put the .bacpac file on drive D when you import it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure でホストされている Finance and Operations 1 ボックス環境では、インポートするときに D ドライブに .bacpac ファイルを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>(A one-box environment is also known as a Tier 1 environment.) For more information about the temporary drive on Azure VMs, see the <bpt id="p1">[</bpt>Understanding the temporary drive on Windows Azure Virtual Machines<ept id="p1">](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)</ept> blog post.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ワンボックス環境はレベル 1 環境とも呼ばれます。) Azure Vm 上でのテンポラリー ドライブに関する詳細については、<bpt id="p1">[</bpt>Windows Azure 仮想マシンのテンポラリー ドライブを理解する<ept id="p1">](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)</ept> ブログ投稿を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Grant the account that runs the SQL Server Windows service <bpt id="p1">[</bpt>Instance File Initialization<ept id="p1">](https://msdn.microsoft.com/en-us/library/ms175935.aspx)</ept> rights.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Windows サービス <bpt id="p1">[</bpt>インスタンス ファイルの初期化<ept id="p1">](https://msdn.microsoft.com/en-us/library/ms175935.aspx)</ept> を実行するアカウントに権限を付与します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>In this way, you can help improve the speed of the import process and the speed of a restore from a <ph id="ph1">\*</ph>.bak file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、インポート処理の速度および <ph id="ph1">\*</ph>.bak ファイルからの復元の速度を向上させることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>For a developer environment, you can easily make sure that the account that runs the SQL Server service has these rights by setting SQL Server to run as the axlocaladmin account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者環境では、axlocaladmin アカウントとして実行する SQL Server を設定することにより、SQL Server サービスを実行するアカウントがこれらの権限を持っていることを簡単に確認することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>From Azure SQL Database, don't select <bpt id="p1">**</bpt>Export data tier application in Management Studio<ept id="p1">**</ept>, because there can be a memory limitation for larger databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">大きなデータベースのメモリ制限が存在する場合があるので、Azure SQLデータベースから、<bpt id="p1">**</bpt>Management Studio でデータ層アプリケーションのエクスポート<ept id="p1">**</ept>を選択しないでください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
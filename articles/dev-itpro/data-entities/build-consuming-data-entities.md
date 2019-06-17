<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="build-consuming-data-entities.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>build-consuming-data-entities.a9188c.8567553bf3008866799c315a9c7ab90d23c86ad4.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>8567553bf3008866799c315a9c7ab90d23c86ad4</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\data-entities\build-consuming-data-entities.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Build and consume data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのビルドおよび使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This tutorial shows how to build an entity and how to consume some out-of-band (OOB) entities in an integration scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、エンティティを構築する方法と、統合シナリオで一部のアウト・オブ・バンド (OOB) エンティティを使用する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Build and consume data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのビルドおよび使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This tutorial shows how to build an entity and how to consume some out-of-band (OOB) entities in an integration scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、エンティティを構築する方法と、統合シナリオで一部のアウト・オブ・バンド (OOB) エンティティを使用する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>You will also preview how these data entities will be consumed in various integrations scenarios, such as data import and export, integration, and OData services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポートとエクスポート、統合、および OData サービスなどのさまざまな統合シナリオで、これらのデータ エンティティが使用される方法もプレビューされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This tutorial requires that you access an environment by using Remote Desktop, and that you be provisioned as an administrator on the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Throughout this tutorial, baseUrl refers to the base URL of the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、baseUrl はインスタンスのベース URL を指します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In the cloud environment, the base URL is obtained from Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド環境では、ベース URL は Microsoft Dynamics Lifecycle Services (LCS) から取得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>On a local virtual machine (VM), the base URL is <ph id="ph1">https://usnconeboxax1aos.cloud.onebox.dynamics.com</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル仮想マシン (VM) の、基準 URL は <ph id="ph1">https://usnconeboxax1aos.cloud.onebox.dynamics.com</ph> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Key concepts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な概念</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Developing a data entity in Microsoft Visual Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio のデータ エンティティの開発</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Enabling a data entity for data management and OData services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ管理および OData サービスのデータ エンティティを有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Consuming a data entity in integration scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合シナリオでデータ エンティティを消費する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Business problem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネスの問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Fleet Management stores customer data in the FMCustomer table and address data in the FMAddressTable table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理は、FMCustomer table テーブルに顧客データを、FMAddressTable テーブルにアドレス データを格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>To access or update customer information, users must access multiple tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客情報にアクセスまたは更新するには、複数のテーブルにアクセスする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Instead, you can create a business object that functionally represents customer information, and that you can use to build integration solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、機能的に顧客情報を表し、統合ソリューションを構築するために使用できるビジネス オブジェクトを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Building the FMLabCustomer entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMLabCustomer エンティティの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In this section, you must create a data entity for FMLabCustomer in the Fleet Management model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、フリート管理モデルで FMLabCustomer のデータ エンティティを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>This entity will be used to manage master data through import/export and integration services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティは、インポート/エクスポートおよび統合サービスを通じてマスター データを管理するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The primary data source is FMCustomer, and the secondary data source is FMAddressTable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライマリ データ ソースが FMCustomer で、セカンダリ データ ソースが FMAddressTable です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Data entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>FMLabCustomerEntity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMLabCustomerEntity</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Data entity fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Mapping</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マッピング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>CellPhone</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CellPhone</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>FMCustomer.CellPhone</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMCustomer.CellPhone</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>DriverLicense</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DriverLicense</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>FMCustomer.DriverLicense</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMCustomer.DriverLicense</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Email</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>FMCustomer.Email</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMCustomer.Email</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>FirstName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>FMCustomer.FirstName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMCustomer.FirstName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>LastName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">姓</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>FMCustomer.LastName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMCustomer.LastName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>CustomerGroup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerGroup</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>FMCustomer.CustGroup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMCustomer.CustGroup</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>AddressLine1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddressLine1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>FMAddressTable.AddressLine1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMAddressTable.AddressLine1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>AddressLine2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddressLine2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>FMAddressTable.AddressLine2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMAddressTable.AddressLine2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>City</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">市町村</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>FMAddressTable.City</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMAddressTable.City</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>State</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">行政単位 (区画)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>FMAddressTable.State</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMAddressTable.State</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>ZipCode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ZipCode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>FMAddressTable.ZipCode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMAddressTable.ZipCode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Country</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">国</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>FMAddressTable.Country</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMAddressTable.Country</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Corresponding staging table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対応するステージング テーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Staging tables are used in import/export scenarios to provide intermediary storage during file parsing and transformation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステージング テーブルは、ファイルの解析と変換時に中間ストレージを提供するため、インポート/エクスポートのシナリオで使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>These tables are also used in connector integration scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのテーブルは、コネクター統合シナリオでも使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In many cases, staging table are mapped 1:1 to an entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、ステージング テーブルはエンティティに対して 1 対 1 でマップされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The staging table that corresponds to the <bpt id="p1">**</bpt>FMLabCustomerEntity<ept id="p1">**</ept> entity is named FMLabCustomerStaging.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMLabCustomerEntity<ept id="p1">**</ept> エンティティに対応するステージング テーブルの名前は FMLabCustomerStaging です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Create a new project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいプロジェクトの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In Visual Studio click <bpt id="p1">**</bpt>File<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>New<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Project<ept id="p3">**</ept>, and then select <bpt id="p4">**</bpt>Finance and Operations Project<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、<bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>新規<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>プロジェクト<ept id="p3">**</ept> の順にクリックしてから、<bpt id="p4">**</bpt>Finance and Operations のプロジェクト<ept id="p4">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Right-click the project, click <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>, and verify that the project is in the Fleet Management model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを右クリックして <bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> をクリックし、プロジェクトがフリート管理モデルであることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>If it isn't, set the <bpt id="p1">**</bpt>Model<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>Fleet Management<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定されていない場合、<bpt id="p1">**</bpt>モデル<ept id="p1">**</ept> プロパティを<bpt id="p2">**</bpt>フリート管理<ept id="p2">**</ept>に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Add a new data entity to your project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトへの新しいデータ エンティティの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Create a new entity that is named <bpt id="p1">**</bpt>FMLabCustomerEntity<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMLabCustomerEntity<ept id="p1">**</ept> という名前の新しいエンティティを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Right-click you project, and then click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>New item<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを右クリックし、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>新しい項目<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The <bpt id="p1">**</bpt>Add New Item<ept id="p1">**</ept> dialog box opens.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しい項目の追加<ept id="p1">**</ept> ダイアログ ボックスが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Select <bpt id="p1">**</bpt>Data Entity<ept id="p1">**</ept>, and then set the <bpt id="p2">**</bpt>Name<ept id="p2">**</ept> property to <bpt id="p3">**</bpt>FMLabCustomerEntity<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ エンティティ<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>名前<ept id="p2">**</ept> プロパティを <bpt id="p3">**</bpt>FMLabCustomerEntity<ept id="p3">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>In the <bpt id="p1">**</bpt>Data entity<ept id="p1">**</ept> wizard, specify the properties for the data entity that you're creating.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ エンティティ<ept id="p1">**</ept> ウィザードで、作成しているデータ エンティティのプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Use the values that are shown in the following screen shot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットに表示される値を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The name of an entity must not have '_' or any numeric digits (0…9).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの名前に「_」や数字 (0...9) を使用することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Using these characters may result in mapping errors later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの文字を使用すると、後でマッピング エラーが発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Data Entity Wizard<ept id="p1">](./media/data-entity-wizard.png)](./media/data-entity-wizard.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>データ エンティティ ウィザード<ept id="p1">](./media/data-entity-wizard.png)](./media/data-entity-wizard.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>For more information about the function of each property, see "Categories of entities" and "Building an entity" in <bpt id="p1">[</bpt>Data entities<ept id="p1">](data-entities.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各プロパティ機能の詳細については、<bpt id="p1">[</bpt>データ エンティティ<ept id="p1">](data-entities.md)</ept>の「エンティティのカテゴリ」および「エンティティの作成」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Add fields to the new entity from your data source, as shown in the following screen shot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットに示すように、データ ソースから新しいエンティティにフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>You can add fields from the primary data source, <bpt id="p1">**</bpt>FMCustomer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主要なデータ ソース、<bpt id="p1">**</bpt>FMCustomer<ept id="p1">**</ept> からフィールドを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>For this entity, clear the check box for the <bpt id="p1">**</bpt>Image<ept id="p1">**</ept> and <bpt id="p2">**</bpt>LicenseImage<ept id="p2">**</ept> container types to simplify testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティについては、テストを効率化するため<bpt id="p1">**</bpt>画像<ept id="p1">**</ept>および <bpt id="p2">**</bpt>LicenseImage<ept id="p2">**</ept> コンテナー タイプのチェック ボックスをオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Rename the data entity fields to reflect public data contract standards, or click <bpt id="p1">**</bpt>Convert labels to field names<ept id="p1">**</ept> to generate names from the existing labels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのフィールドの名前を、パブリック データ コントラクト標準を反映するように変更するか、<bpt id="p1">**</bpt>ラベルをフィールド名に変換<ept id="p1">**</ept> をクリックして既存のラベルから名前を生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>On the line for the <bpt id="p1">**</bpt>DriverLicense<ept id="p1">**</ept> field, select the <bpt id="p2">**</bpt>Is mandatory<ept id="p2">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DriverLicense<ept id="p1">**</ept> フィールドの行で、<bpt id="p2">**</bpt>必須<ept id="p2">**</ept>チェック ボックスを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>This field will be used as the natural key for the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドはエンティティのナチュラル キーとして使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Data Entity Wizard 2<ept id="p1">](./media/data-entity-wizard-2.png)](./media/data-entity-wizard-2.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>データ エンティティ ウィザード 2<ept id="p1">](./media/data-entity-wizard-2.png)](./media/data-entity-wizard-2.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In the <bpt id="p1">**</bpt>Data source<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>PrimaryAddress<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ ソース<ept id="p1">**</ept> フィールドで、<bpt id="p2">**</bpt>PrimaryAddress<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Notice that the <bpt id="p1">**</bpt>PrimaryAddress<ept id="p1">**</ept> data source is automatically added because of automatic expansion or the surrogate foreign key replacement of <bpt id="p2">**</bpt>AddressID<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>AddressID<ept id="p2">**</ept> の自動拡張または代理外部キー交換のため、<bpt id="p1">**</bpt>PrimaryAddress<ept id="p1">**</ept> データ ソースが自動的に追加されることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Steps and add fields<ept id="p1">](./media/steps-and-add-fields.png)](./media/steps-and-add-fields.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>手順およびフィールドの追加<ept id="p1">](./media/steps-and-add-fields.png)](./media/steps-and-add-fields.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Select the fields from the <bpt id="p1">**</bpt>PrimaryAddress<ept id="p1">**</ept> data source that you want to be part of your entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの一部にする <bpt id="p1">**</bpt>PrimaryAddress<ept id="p1">**</ept> データ ソースからフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Additionally, rename the following fields to reflect proper public data contract naming:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、次のフィールドの名前を変更して、適切な公開データ契約の名前付けを反映します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>PrimaryAddress <ph id="ph1">\_</ph>AddressLine1 <ph id="ph2">&amp;gt;</ph> AddressLine1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PrimaryAddress <ph id="ph1">\_</ph>AddressLine1 <ph id="ph2">&amp;gt;</ph> AddressLine1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>PrimaryAddress <ph id="ph1">\_</ph>AddressLine2 <ph id="ph2">&amp;gt;</ph> AddressLine2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PrimaryAddress <ph id="ph1">\_</ph>AddressLine2 <ph id="ph2">&amp;gt;</ph> AddressLine2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>PrimaryAddress <ph id="ph1">\_</ph>City <ph id="ph2">&amp;gt;</ph> City</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PrimaryAddress <ph id="ph1">\_</ph>City <ph id="ph2">&amp;gt;</ph> City</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>PrimaryAddress <ph id="ph1">\_</ph>State <ph id="ph2">&amp;gt;</ph> State</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PrimaryAddress <ph id="ph1">\_</ph>State <ph id="ph2">&amp;gt;</ph> State</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>PrimaryAddress <ph id="ph1">\_</ph>ZipCode <ph id="ph2">&amp;gt;</ph> ZipCode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PrimaryAddress <ph id="ph1">\_</ph>ZipCode <ph id="ph2">&amp;gt;</ph> ZipCode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>PrimaryAddress <ph id="ph1">\_</ph>Country <ph id="ph2">&amp;gt;</ph> Country</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PrimaryAddress <ph id="ph1">\_</ph>Country <ph id="ph2">&amp;gt;</ph> Country</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Data entity wizard</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ ウィザード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Click <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>完了<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>A data entity item and staging table are added to the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティの品目およびステージング テーブルは、プロジェクトに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Solution explorer<ept id="p1">](./media/solution-explorer.png)](./media/solution-explorer.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ソリューション エクスプローラー<ept id="p1">](./media/solution-explorer.png)](./media/solution-explorer.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Build your project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>In Solution Explorer, right-click your project, and then click <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、プロジェクトを右クリックしてから<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Change the value of the <bpt id="p1">**</bpt>Synchronize database on build<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>True<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>OK<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビルドでのデータベースの同期<ept id="p1">**</ept>プロパティの値を <bpt id="p2">**</bpt>True<ept id="p2">**</ept> に変更し、<bpt id="p3">**</bpt>OK<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>This property must be set only one time per project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティは、プロジェクトごとに 1 回のみ設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Entities are created as views in Microsoft SQL Server, and staging tables are also added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティが Microsoft SQL Server のビューとして作成され、ステージング テーブルが追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Therefore, you must sync a database when you build entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、エンティティを作成するときにデータベースを同期する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Property pages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ ページ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>On the Visual Studio toolbar, click <bpt id="p1">**</bpt>Build<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Build Solution<ept id="p2">**</ept> to build the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio ツールバーで、<bpt id="p1">**</bpt>構築<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ソリューションの構築<ept id="p2">**</ept> の順にクリックしてプロジェクトを構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Verify that the build doesn't contain any errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドにエラーが含まれていないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>At this point in the tutorial, warnings are allowed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この時点でチュートリアルは警告が許可されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Visually validate and customize an entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目視による検証とエンティティのカスタマイズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>In Solution Explorer, right-click the <bpt id="p1">**</bpt>FMLabCustomerEntity<ept id="p1">**</ept> node, and then click <bpt id="p2">**</bpt>Open<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>FMLabCustomerEntity<ept id="p1">**</ept> ノードを右クリックしてから<bpt id="p2">**</bpt>開く<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The designer for the entity opens in the middle pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのデザイナーが中央のウィンドウに開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Validate the properties of the <bpt id="p1">**</bpt>FMLabCustomerEntity<ept id="p1">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMLabCustomerEntity<ept id="p1">**</ept> エンティティのプロパティを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Select the entity in Solution Explorer, and compare the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane values to the following screen shot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプ ローラーでエンティティを選択し、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウの値と次のスクリーンショットを比較します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Set the <bpt id="p1">**</bpt>Label<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>Fleet Lab Customers<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル<ept id="p1">**</ept> プロパティを <bpt id="p2">**</bpt>フリート ラボ顧客<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMLabCustomerEntity - Properties<ept id="p1">](./media/fmlabcustomerentity-properties.png)](./media/fmlabcustomerentity-properties.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMLabCustomerEntity - プロパティ<ept id="p1">](./media/fmlabcustomerentity-properties.png)](./media/fmlabcustomerentity-properties.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In the left pane, click <bpt id="p1">**</bpt>Data Sources<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>FMCustomer<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Data Sources<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>FMAddressTable<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左ウィンドウで、<bpt id="p1">**</bpt>データ ソース<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>FMCustomer<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>データ ソース<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>FMAddressTable<ept id="p4">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Change the <bpt id="p1">**</bpt>Is Read Only<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>読み取り専用<ept id="p1">**</ept>プロパティを<bpt id="p2">**</bpt>いいえ<ept id="p2">**</ept>に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>This is a known issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、既知の問題です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Eventually, the value will be set to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> or <bpt id="p2">**</bpt>No<ept id="p2">**</ept> automatically, based on the type of join.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最終的に、この値は結合のタイプに基づき、自動的に<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>または<bpt id="p2">**</bpt>いいえ<ept id="p2">**</ept>に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>The value should be <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> for composition scenarios, and <bpt id="p2">**</bpt>No<ept id="p2">**</ept> for associations (surrogate foreign key expansions).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">合成シナリオの場合、値は <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>、アソシエーションの場合、値は <bpt id="p2">**</bpt>No<ept id="p2">**</ept> にしてください (代理外部キー拡張)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>This property enables the data source to be read/write.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティを使用すると、データ ソースを読み取り/書き込みをすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMLabCustomerEntity - Properties2<ept id="p1">](./media/fmlabcustomerentity-properties2.png)](./media/fmlabcustomerentity-properties2.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMLabCustomerEntity - プロパティ 2<ept id="p1">](./media/fmlabcustomerentity-properties2.png)](./media/fmlabcustomerentity-properties2.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>In the <bpt id="p1">**</bpt>FMLabCustomerEntity<ept id="p1">**</ept> designer, click <bpt id="p2">**</bpt>Keys<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>EntityKey<ept id="p3">**</ept>, and then expand the <bpt id="p4">**</bpt>Fields<ept id="p4">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMLabCustomerEntity<ept id="p1">**</ept> デザイナーで、<bpt id="p2">**</bpt>キー<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>EntityKey<ept id="p3">**</ept> とクリックしてから<bpt id="p4">**</bpt>フィールド<ept id="p4">**</ept> ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Verify that the list of fields matches the following screen shot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドの一覧が次のスクリーン ショットと一致していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMLabCustomerEntity<ept id="p1">](./media/fmlabcustomerentity.png)](./media/fmlabcustomerentity.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMLabCustomerEntity<ept id="p1">](./media/fmlabcustomerentity.png)](./media/fmlabcustomerentity.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>To visually validate the staging table that will be used for import/export, open the <bpt id="p1">**</bpt>FMLabCustomerStaging<ept id="p1">**</ept> table in the designer, and then select the <bpt id="p2">**</bpt>FMLabCustomerStaging<ept id="p2">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート/エクスポートに使用するステージング テーブルを視覚的に検証するには、デザイナーの <bpt id="p1">**</bpt>FMLabCustomerStaging<ept id="p1">**</ept> テーブルを開き、<bpt id="p2">**</bpt>FMLabCustomerStaging<ept id="p2">**</ept> ノードを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>fMLabCustomerStaging - Properties<ept id="p1">](./media/fmlabcustomerstaging-properties.png)](./media/fmlabcustomerstaging-properties.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>fMLabCustomerStaging - プロパティ<ept id="p1">](./media/fmlabcustomerstaging-properties.png)](./media/fmlabcustomerstaging-properties.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Click <bpt id="p1">**</bpt>FMLabCustomerStaging<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Fields<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMLabCustomerStaging<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>フィールド<ept id="p2">**</ept>とクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>In the following screen shot, the standard fields of the staging tables are selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットでは、ステージング テーブルの標準フィールドが選択されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>All entity staging tables have these standard fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのエンティティ ステージング テーブルにはこれらの標準的なフィールドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>The screen shot also shows the data fields that belong on this data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリーンショットには、このデー タエンティティに属するデータ フィールドも表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMLabCustomerStaging<ept id="p1">](./media/fmlabcustomerstaging.png)](./media/fmlabcustomerstaging.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMLabCustomerStaging<ept id="p1">](./media/fmlabcustomerstaging.png)](./media/fmlabcustomerstaging.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In Solution Explorer, right-click your project, and then select <bpt id="p1">**</bpt>Rebuild<ept id="p1">**</ept> to rebuild and synchronize the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、プロジェクトを右クリックしてから、<bpt id="p1">**</bpt>再構築<ept id="p1">**</ept>を選択して、プロジェクトを再構築して同期します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Testing data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのテスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Entities can be tested by using various methods in X++, through data import/export, or through integrations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティは、データのインポート/エキスポートまたは統合を通じ、X++ のさまざまなメソッドを使用してテストできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>In this section, we'll explore scenarios for validating entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、エンティティを検証するためのシナリオについて調べます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Test the entity by using X++ code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コードを使用してエンティティをテスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>One of the most common ways of interacting with data entities is through X++, by using a unit test or a runnable job to validate that the entities have been built.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティとの対話の最も一般的な方法の 1 つは、単体テストまたは実行可能なジョブを使用してエンティティが構築されたことを検証することによって、x++ を使用する方法です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>In this example, we will use a runnable job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、実行可能なジョブを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>In Solution Explorer, click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>New item<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Runnable class<ept id="p3">**</ept> to add a runnable class to your project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>新しい項目<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>実行可能なクラス<ept id="p3">**</ept>をクリックして、実行可能なクラスをプロジェクトに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Copy and paste the following code into the class to test your data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードをコピーしてクラスに貼り付け、データ エンティティをテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Run the code in debugger to set it as a startup object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタートアップ オブジェクトとして設定するためデバッガーでコードを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>To validate the entity, view the Infolog in the debugger window or in notifications on the website.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティを検証するには、デバッガー ウィンドウまたは Web サイトの通知で Infolog を調べます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>You will see that three successful messages are logged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 つの成功メッセージが記録されていることが確認されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>You will also see the actions that were taken.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行されたアクションも表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Importing data by using entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティを使用したデータのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Data entities that have the <bpt id="p1">**</bpt>Data Management Enabled<ept id="p1">**</ept> property can be used to import and export data in various file formats.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ管理を有効<ept id="p1">**</ept>プロパティを持つデータ エンティティは、さまざまなファイル形式のデータをインポートおよびエクスポートするために使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>In this section, you will import data in a CSV file format for the <bpt id="p1">**</bpt>FMLabCustomer<ept id="p1">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、<bpt id="p1">**</bpt>FMLabCustomer<ept id="p1">**</ept> エンティティについて CSV ファイル形式でデータをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>File import</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル インポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>After you create your data entity, you can validate import/export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティを作成した後は、インポート/エクスポートを検証することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Create a sample CSV file that you can import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートすることができる CSV ファイルのサンプルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Copy the following text, and save it as <bpt id="p1">**</bpt>FM Lab Customer Import.csv<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテキストをコピーし、<bpt id="p1">**</bpt>FM Lab Customer Import.csv<ept id="p1">**</ept> として保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Click <bpt id="p1">**</bpt>User Dashboard<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Data management<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ユーザー ダッシュ ボード<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>データ管理<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In the <bpt id="p1">**</bpt>Data Management<ept id="p1">**</ept> workspace, click the <bpt id="p2">**</bpt>Import<ept id="p2">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ管理<ept id="p1">**</ept>ワークスペースで、<bpt id="p2">**</bpt>インポート<ept id="p2">**</ept> タイルをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>On the <bpt id="p1">**</bpt>Import<ept id="p1">**</ept> page, enter the import details, as shown in the following screen shot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インポート<ept id="p1">**</ept> ページで、次のスクリーン ショットに表示されるインポートの詳細を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Import new record</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいレコードのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Click the <bpt id="p1">**</bpt>Upload data<ept id="p1">**</ept> button next to the <bpt id="p2">**</bpt>Upload file for entity<ept id="p2">**</ept> field, and select the CSV file that you created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>エンティティ ファイルのアップロード<ept id="p2">**</ept> フィールドの隣にある <bpt id="p1">**</bpt>データのアップロード<ept id="p1">**</ept> ボタンをクリックし、作成した CSV ファイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>After the file is uploaded, you will notice that the entity is added to the middle section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルがアップロードされると、エンティティが中間セクションに追加された事が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>You will also receive an error that states that the mapping isn't valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、マッピングが無効であることを示すエラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>A few fields aren't mapped correctly between the source file and the target entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかのフィールドは、ソース ファイルとターゲット エンティティの間で正しくマップされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>In the entities list, click <bpt id="p1">**</bpt>View map<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ リストで<bpt id="p1">**</bpt>マップの表示<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source><bpt id="p1">**</bpt>AddressLine1<ept id="p1">**</ept> and <bpt id="p2">**</bpt>AddressLine2<ept id="p2">**</ept> are two fields in the source that aren't mapped to target fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AddressLine1<ept id="p1">**</ept> および <bpt id="p2">**</bpt>AddressLine2<ept id="p2">**</ept> は、ターゲット フィールドにマップされていないソース内の 2 つのフィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>In the visual mapper, or details view, map these fields as follows, and then click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジュアル マッパー、または詳細表示で、これらのフィールドを次のようにマップして<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>AddressLine1 – Address1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddressLine1 – Address1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>AddressLine2 – Address2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddressLine2 – Address2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Map source to staging<ept id="p1">](./media/map-source-to-staging.png)](./media/map-source-to-staging.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ソースをステージングにマップ<ept id="p1">](./media/map-source-to-staging.png)](./media/map-source-to-staging.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Click the <bpt id="p1">**</bpt>Back<ept id="p1">**</ept> button in your browser to go back to the <bpt id="p2">**</bpt>Import job<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザーの <bpt id="p1">**</bpt>戻る<ept id="p1">**</ept> ボタンをクリックして、<bpt id="p2">**</bpt>インポート ジョブ<ept id="p2">**</ept> ページに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The check mark in the entities list indicates that the entity is now ready for import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ リストのチェック マークは、エンティティがインポートの準備ができていることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Import new record 2<ept id="p1">](./media/import-new-record-2.png)](./media/import-new-record-2.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>新規レコード 2 のインポート<ept id="p1">](./media/import-new-record-2.png)](./media/import-new-record-2.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Click <bpt id="p1">**</bpt>Import Now<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>今すぐインポート<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>After the import is completed, the job status page opens.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートが完了したら、ジョブ ステータス ページが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Consuming entities by using OData</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData を使用してエンティティを消費する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>In this section, you will learn how to expose and consume an entity for OData.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、OData のエンティティを公開して使用する方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Before you begin, verify that the Fleet demo data is loaded from the client: <ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/?f=FMSetup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始する前に、クライアントからフリート デモ データが読み込まれたことを確認します。<ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/?f=FMSetup</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Review the FleetRental entity and add a navigation property for OData</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FleetRental エンティティを確認し、OData のナビゲーション プロパティを追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>You will review the existing <bpt id="p1">**</bpt>FleetRental<ept id="p1">**</ept> entity and then create a relationship from one data entity to another.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の <bpt id="p1">**</bpt>FleetRental<ept id="p1">**</ept> エンティティをレビューしてから、1 つのデータ エンティティと別のデータ エンティティ間のリレーションシップを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>This relationship will be used as a navigation property for OData entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この関係は、OData エンティティのナビゲーション プロパティとして使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>In Solution Explorer, verify that you're in the <bpt id="p1">**</bpt>FMEntityLab<ept id="p1">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>FMEntityLab<ept id="p1">**</ept> プロジェクトの中であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>In Application Explorer, search for <bpt id="p1">**</bpt>FMRentalEntity<ept id="p1">**</ept>, right-click it, and then select <bpt id="p2">**</bpt>Add to Project<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーで、<bpt id="p1">**</bpt>FMRentalEntity<ept id="p1">**</ept> を検索して右クリックしてから、<bpt id="p2">**</bpt>プロジェクトに追加<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>In Application Explorer, search for <bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept>, right-click it, and then select <bpt id="p2">**</bpt>Add to project<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーで、<bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept> を検索して右クリックしてから、<bpt id="p2">**</bpt>プロジェクトに追加<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>In Solution Explorer, right-click <bpt id="p1">**</bpt>FMRentalEntity<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Open<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>FMRentalEntity<ept id="p1">**</ept> を右クリックしてから、<bpt id="p2">**</bpt>開く<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>In the view designer, select the root node, <bpt id="p1">**</bpt>FMRentalEntity<ept id="p1">**</ept>, and review the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビュー デザイナーで、ルート ノード <bpt id="p1">**</bpt>FMRentalEntity<ept id="p1">**</ept> を選択し、次のプロパティを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>IsPublic</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IsPublic</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>When this property is set to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>, the entity is visible by using the OData application programming interface (API).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティを <bpt id="p1">**</bpt>はい<ept id="p1">**</ept> に設定すると、OData アプリケーション プログラミング インターフェイス (API) を使用して、エンティティを表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Public Entity Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パブリック エンティティ名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>FleetRental</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FleetRental</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>The name that will be used in the OData APIs for <bpt id="p1">**</bpt>EntityType<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EntityType<ept id="p1">**</ept> の OData API で使用される名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Public Collection Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パブリック コレクション名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>FleetRentals</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FleetRentals</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>The name that will be used for the OData collection entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData コレクション エンティティに使用される名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>In the view designer, expand the <bpt id="p1">**</bpt>Relations<ept id="p1">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビュー デザイナーで、<bpt id="p1">**</bpt>関係<ept id="p1">**</ept>ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Select <bpt id="p1">**</bpt>Customer Relation<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Delete<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>顧客関係<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>削除<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Right-click <bpt id="p1">**</bpt>Relations<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>New<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Relation<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>関係<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Select <bpt id="p1">**</bpt>Relation1<ept id="p1">**</ept>, and set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係 1<ept id="p1">**</ept> を選択し、次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Cardinality</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>ZeroMore</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ZeroMore</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>CustomerRelation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerRelation</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Related Data Entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連するデータ エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>FMCustomerEntity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMCustomerEntity</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Related Data Entity Cardinality</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連データ エンティティ カーディナリティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>ExactlyOne</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ExactlyOne</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Related Data Entity Role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連するデータ エンティティ ロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>CustomerRole</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerRole</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Relationship Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係のタイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Association</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">役割</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Rental</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レンタル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>In the view designer, right-click the <bpt id="p1">**</bpt>CustomerRelation<ept id="p1">**</ept> node, and then select <bpt id="p2">**</bpt>New<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Normal<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビュー デザイナーで、<bpt id="p1">**</bpt>CustomerRelation<ept id="p1">**</ept> ノードを右クリックしてから、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>標準<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Right-click the new node under <bpt id="p1">**</bpt>CustomerRelation<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomerRelation<ept id="p1">**</ept> で新しいノードを右クリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>Set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source><bpt id="p1">**</bpt>CustomerDriverLicense<ept id="p1">**</ept>This is the foreign key field on <bpt id="p2">**</bpt>FMRentalEntity<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomerDriverLicense<ept id="p1">**</ept> これは、<bpt id="p2">**</bpt>FMRentalEntity<ept id="p2">**</ept> の外部キーフィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Related Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source><bpt id="p1">**</bpt>DriverLicense<ept id="p1">**</ept>This is the unique key on <bpt id="p2">**</bpt>FMCustomerEntity<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DriverLicense<ept id="p1">**</ept> これは、<bpt id="p2">**</bpt>FMCustomerEntity<ept id="p2">**</ept> の固有のキーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>The following screen shot shows the relation in Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーンショットは、Visual Studio での関係を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMRentalEntity - Solution explorer<ept id="p1">](./media/fmrentalentity-solution-explorer.png)](./media/fmrentalentity-solution-explorer.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMRentalEntity - ソリューション エクスプローラー<ept id="p1">](./media/fmrentalentity-solution-explorer.png)](./media/fmrentalentity-solution-explorer.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>On the <bpt id="p1">**</bpt>BUILD<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Build Solution<ept id="p2">**</ept> to save your changes and build the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビルド<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>ソリューションのビルド<ept id="p2">**</ept>をクリックして変更を保存し、プロジェクトをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>You can view the build progress in the <bpt id="p1">**</bpt>Output<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>出力<ept id="p1">**</ept> ウィンドウでビルドの進行状況を表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>To update the OData endpoint with the changes, you must run an <bpt id="p1">**</bpt>iisreset<ept id="p1">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData エンドポイントをこの変更と併せて更新するには、<bpt id="p1">**</bpt>iisreset<ept id="p1">**</ept> コマンドを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window as an administrator, and enter <bpt id="p2">**</bpt>iisreset<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として<bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、<bpt id="p2">**</bpt>iisreset<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>You've now created a navigation property between <bpt id="p1">**</bpt>FMRentalEntity<ept id="p1">**</ept> and <bpt id="p2">**</bpt>FMCustomerEntity<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これで、<bpt id="p1">**</bpt>FMRentalEntity<ept id="p1">**</ept> と <bpt id="p2">**</bpt>FMCustomerEntity<ept id="p2">**</ept> 間に、ナビゲーション プロパティの作成を完了しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Use standard OData syntax to retrieve data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準の OData 構文を使用してデータを取得する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>In this section, you will use some of the standard OData syntax to navigate and query the OData entities that are exposed in the Fleet Management model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、標準の OData 構文の一部を使用し、フリート管理モデルで公開されている OData エンティティを操作して照会します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>First, follow these steps to enable Internet Explorer to view JSON formatted data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、以下の手順に従って、JSON 形式のデータを表示する Internet Explorer を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Close all Internet Explorer windows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての Internet Explorer ウィンドウを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Go to C:<ph id="ph1">\\</ph>FMLab, and select and double-click the json.ie.reg file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C:<ph id="ph1">\\</ph>FMLab に移動し、json.ie.reg ファイルを選択してダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In the <bpt id="p1">**</bpt>Registry Editor<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レジストリ エディター<ept id="p1">**</ept> ダイアログ ボックスで、<bpt id="p2">**</bpt>はい<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>You can now use Internet Explorer to explore some OData URIs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer  を使用して一部の OData URI を表示できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Start Internet Explorere, and enter the following URL in the address bar: <ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/data/$metadata You will see all the metadata that is associated with OData entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer を起動し、アドレス バーに URL <ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/data/$metadata を入力します。OData エンティティに関連付けられたすべてのメタデータが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>The metadata might take a few minutes to appear the first time that you access it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初にアクセスする場合、メタデータの表示に数分かかることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>In the XML, you can see all of the properties and navigation properties associated with the OData entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">XML で、OData エンティティに関連付けられているすべてのプロパティおよびナビゲーション プロパティを表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>In the browser, find <bpt id="p1">**</bpt>FleetRental<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザーで <bpt id="p1">**</bpt>FleetRental<ept id="p1">**</ept> を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>The following screen shot shows the metadata of the <bpt id="p1">**</bpt>FleetRental<ept id="p1">**</ept> entity, together with the new relationship, <bpt id="p2">**</bpt>NavigationProperty<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットは、<bpt id="p1">**</bpt>FleetRental<ept id="p1">**</ept> エンティティのメタデータと、新しいリレーションシップ <bpt id="p2">**</bpt>NavigationProperty<ept id="p2">**</ept> を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FleetRental metadata<ept id="p1">](./media/fleetrental-metadata.png)](./media/fleetrental-metadata.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FleetRental メタデータ<ept id="p1">](./media/fleetrental-metadata.png)](./media/fleetrental-metadata.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>To view all the customers in the Fleet Management application in JSON format, enter the following URL into the address bar of your browser: <ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/data/FleetCustomer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理アプリケーションのすべての顧客を JSON 形式で表示するには、ブラウザーのアドレス バーに <ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/data/FleetCustomer の URL を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Entity names are case-sensitive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ名は大文字と小文字が区別されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>If you don't want to retrieve all properties for the customers, you can retrieve just selected properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客のすべてのプロパティを取得しない場合は、選択したプロパティのみを取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>For example, to retrieve only <bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept> and <bpt id="p2">**</bpt>LastName<ept id="p2">**</ept>, enter the following URL: <ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/data/FleetCustomers?$filter=FirstName.LastName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept> および <bpt id="p2">**</bpt>LastName<ept id="p2">**</ept> のみを取得するには、次の URL を入力します: <ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/data/FleetCustomers?$filter=FirstName.LastName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>You can also apply filters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、フィルターを適用することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>For example, to filter on all customers where <bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept><ph id="ph1">=</ph><bpt id="p2">**</bpt>Phil<ept id="p2">**</ept>, enter the following URL: <ph id="ph2">\[</ph>baseUrl<ph id="ph3">\]</ph>/data/FleetCustomers?$filter=FirstName%20eq%20'Phil'</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept><ph id="ph1">=</ph><bpt id="p2">**</bpt>Phil<ept id="p2">**</ept> であるすべての顧客をフィルター処理するには、次の URL を入力します: <ph id="ph2">\[</ph>baseUrl<ph id="ph3">\]</ph>/data/FleetCustomers?$filter=FirstName%20eq%20'Phil'</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>These URLs won't work if you copy and paste them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの URL はコピーおよび貼り付けする場合、機能しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>You must manually enter them in the address bar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アドレス バーに手動で入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>To retrieve all the <bpt id="p1">**</bpt>Rental<ept id="p1">**</ept> records, together with all details of the customers, enter the following URL: <ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/data/FleetRentals?$expand=CustomerRole The following example shows a <bpt id="p2">**</bpt>Rental<ept id="p2">**</ept> record, together with details of the linked customer, in JSON format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客のすべての詳細とともにすべての<bpt id="p1">**</bpt>レンタル<ept id="p1">**</ept>レコードを取得するには、URL "<ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/data/FleetRentals?$expand=CustomerRole" を入力します。次の例は、<bpt id="p2">**</bpt>レンタル<ept id="p2">**</ept>レコードと、リンクされた顧客の詳細を JSON 形式で示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Add an action to OData entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData エンティティへのアクションの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Actions provide a way to inject behaviors into the data model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションは、動作をデータ モデルに挿入する方法を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>In Dynamics 'AX 7,' you add actions by adding a method to the data entity and then decorating the method with specific attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 'AX 7' では、データ エンティティにメソッドを追加して特定の属性を持つメソッドを修飾することで、アクションを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>In this section, we'll walk through the steps for adding an action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、アクションを追加するための手順を見てみましょう。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>In Solution Explorer, right-click <bpt id="p1">**</bpt>FMRentalEntity<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>View code<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>FMRentalEntity<ept id="p1">**</ept> を右クリックしてから、<bpt id="p2">**</bpt>コードの表示<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Copy the following code lines, and paste them into the <bpt id="p1">**</bpt>Code<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード明細行をコピーし、<bpt id="p1">**</bpt>コード<ept id="p1">**</ept>ウィンドウに貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>On the <bpt id="p1">**</bpt>BUILD<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Rebuild Solution<ept id="p2">**</ept> to save your changes and build the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビルド<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>ソリューションの再構築<ept id="p2">**</ept>をクリックして変更を保存し、プロジェクトをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>You can view the build progress in the <bpt id="p1">**</bpt>Output<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>出力<ept id="p1">**</ept> ウィンドウでビルドの進行状況を表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>To update the OData endpoint with the changes, you must run an <bpt id="p1">**</bpt>iisreset<ept id="p1">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData エンドポイントをこの変更と併せて更新するには、<bpt id="p1">**</bpt>iisreset<ept id="p1">**</ept> コマンドを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window as an administrator, and enter <bpt id="p2">**</bpt>iisreset<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として<bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、<bpt id="p2">**</bpt>iisreset<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>The action that you just added can be invoked through code, as you will see in the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加したアクションは、次のセクションに示すように、コードで呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Consume the OData API from an external console application</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部コンソール アプリケーションから OData API を消費する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>In this section, you will use a console application to consume the OData endpoints that are exposed in the Fleet Management application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、コンソール アプリケーションを使用して、フリート管理アプリケーションで公開されている OData エンドポイントを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>The console application first creates a new customer and then creates a new reservation for that customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンソール アプリケーションは、最初に、新規顧客を作成し、その顧客の新しい予約を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>This tutorial shows how easy it is to use OData together with standard .NET Windows Communication Foundation (WCF) data service libraries to integrate with Dynamics AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、標準の .NET Windows Communication Foundation (WCF) データ サービス ライブラリと共に OData を使用して、Dynamics AX と統合することがいかに簡単であるかを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Start a new instance of Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio の新しいインスタンスを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>On the <bpt id="p1">**</bpt>File<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Open<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Project/Solution<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>開く<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>プロジェクト/ソリューション<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>In the <bpt id="p1">**</bpt>Open Project<ept id="p1">**</ept> dialog box, browse to <bpt id="p2">**</bpt>C:<ph id="ph1">\\</ph>FMLab<ph id="ph2">\\</ph>Odata4ConsoleApplication<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>Odata4ConsoleApplication.csproj<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクトを開く<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>C:<ph id="ph1">\\</ph>FMLab<ph id="ph2">\\</ph>Odata4ConsoleApplication<ept id="p2">**</ept> を参照してから <bpt id="p3">**</bpt>Odata4ConsoleApplication.csproj<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Click <bpt id="p1">**</bpt>Open<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開く<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>The <bpt id="p1">**</bpt>Odata4ConsoleApplication<ept id="p1">**</ept> project appears in Solution Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Odata4ConsoleApplication<ept id="p1">**</ept> プロジェクトがソリューション エクスプローラーに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>In Solution Explorer, double-click <bpt id="p1">**</bpt>OdataProxyGenerator.tt<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>OdataProxyGenerator.tt<ept id="p1">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>In the code editor, replace the following string with your organization's URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード エディターで、次の文字列を組織の URL に置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Save the OdataProxyGenerator.tt file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OdataProxyGenerator.tt ファイルを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>In the <bpt id="p1">**</bpt>Save of Read-only file<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>Overwrite<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>読み取り専用ファイルの保存<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>上書き<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>The proxy class for the OData metadata endpoint is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData メタデータ エンドポイントのプロキシ クラスが生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>This operation might take a few minutes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この操作には数分かかる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>In Solution Explorer, double-click <bpt id="p1">**</bpt>Program.cs<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>Program.cs<ept id="p1">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Replace the value of the <bpt id="p1">**</bpt>dynamicsBaseUri<ept id="p1">**</ept> variable with your organization's URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>dynamicsBaseUri<ept id="p1">**</ept> 変数の値を組織の URL に置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Verify that there is a final closing slash (/) in the URL, and then click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">URL に最後の終了スラッシュ (/) があることを確認してから、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>In the <bpt id="p1">**</bpt>Save of Read-only file<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>Overwrite<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>読み取り専用ファイルの保存<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>上書き<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>Press F5 to run the application, and then follow the instructions in the output console window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">F5 キーを押してアプリケーションを実行し、出力コンソール ウィンドウで指示に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>The application might prompt you for your Dynamics AX credentials.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションによって、Dynamics AX の資格情報を入力するよう求められる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>After the application has run, the new customer and the corresponding reservation are created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションが実行された後、新しい顧客と対応する引当が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Follow these steps to verify that the new reservation appears on the <bpt id="p1">**</bpt>Rental<ept id="p1">**</ept> page:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レンタル<ept id="p1">**</ept>ページで新しい予約が表示されることを確認するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Start Internet Explorer, and enter the following URL in the address bar: <ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/?mi=FMRental The <bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept> page shows the list of rentals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer を起動して、アドレス バーに URL <ph id="ph1">\[</ph>baseURL<ph id="ph2">\]</ph>/?mi=FMRental を入力します。<bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept>  ページにレンタルの一覧が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Rental list<ept id="p1">](./media/rental-list.png)](./media/rental-list.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>レンタル リスト<ept id="p1">](./media/rental-list.png)](./media/rental-list.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>At the bottom of the list, click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to view the next page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストの下部にある<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックして、次のページを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>On this page, you can see that the reservation was created for the new customer that you added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このページで、追加された新しい顧客の予約が作成されたことを確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>customer reservation<ept id="p1">](./media/customer-reservation.png)](./media/customer-reservation.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>顧客引当<ept id="p1">](./media/customer-reservation.png)](./media/customer-reservation.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>This completes the walkthrough, where you've seen an external client interacting with the Fleet Management model by using OData endpoint.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これで、OData エンドポイントを使用して フリート管理モデルと対話する外部クライアントを見たウォークスルーは完了です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Casing rules in data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティでのケーシング規則</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>XML format</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">XML 形式</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>During an export, the entity name and the field names are exported in uppercase.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート中、エンティティ名とフィールド名は大文字でエクスポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>If there is a need to apply a transformation, the transformation must use uppercase in all references.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変換を適用する必要がある場合、変換ではすべての参照で大文字を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>During an import, data management accepts input file in any casing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート中、データ管理は大文字、小文字どちらの入力ファイルも受け入れます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>However, care must be taken to have the same format for a given attribute/element in the file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ファイル内の特定の属性/要素に同じ形式を使用するように注意する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>When applying a transformation, ensure that the transformation is using the same casing rules in all references as in the incoming file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変換を適用するときは、変換が着信ファイル内のすべての参照で同じケーシング規則を使用していることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>Excel format</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel 形式</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>During an export, column names will be exported in uppercase.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート中、列名は大文字でエクスポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>Imports are not case sensitive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートでは大文字と小文字が区別されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>CSV format</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CSV 形式</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>During an export, column names will be exported in uppercase.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート中、列名は大文字でエクスポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>Imports are not case sensitive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートでは大文字と小文字が区別されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Tips and tricks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヒントや秘訣</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>Max join limits</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最大結合の制限</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>During entity development, take care to ensure that the overall structure of the entity does not exceed the max join limit of 26.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの開発中に、エンティティの全体的な構造が最大統合制限である 26 を超えないように注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>This is the default limit in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、Finance and Operations で既定の限度です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>Increasing the join limit is not recomended becaues it can have unintended consequences.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合制限を増やすことは意図しない結果をもたらす可能性があるためお勧めできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>If this limit is exceeded, the entity will most likely fail to process records and will result in the following SQL error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この制限を超えると、エンティティはレコードの処理に失敗する可能性が高く、次の SQL エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>It is also recomended to manage the total number of columns in the entity to avoid this error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、エラーを回避するエンティティで列の合計数を管理することもお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source><bpt id="p1">[</bpt>Developing an entity and using it for data migration<ept id="p1">](develop-entity-for-data-migration.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>エンティティを開発してデータ移行に使用する<ept id="p1">](develop-entity-for-data-migration.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
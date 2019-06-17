<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="develop-entity-for-data-migration.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>develop-entity-for-data-migration.73beca.23670175ec93dcfd3062875cc45c27ca834571b1.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>23670175ec93dcfd3062875cc45c27ca834571b1</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\data-entities\develop-entity-for-data-migration.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Develop entities for data migration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ移行のエンティティの開発</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This tutorial shows how to develop data entities in Microsoft Visual Studio and then use them for data migration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、Microsoft Visual Studio でデータ エンティティを開発し、データ移行に使用する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Develop entities for data migration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ移行のエンティティの開発</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This tutorial shows how to develop data entities in Microsoft Visual Studio and then use them for data migration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、Microsoft Visual Studio でデータ エンティティを開発し、データ移行に使用する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This tutorial is broken out into two sections and four exercises.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルは、2 つのセクションと 4 つの演習に分かれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In the first section, you will build a <bpt id="p1">**</bpt>Project Category<ept id="p1">**</ept> entity in Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のセクションでは、Visual Studio で<bpt id="p1">**</bpt>プロジェクト カテゴリ<ept id="p1">**</ept> エンティティを構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You will then use this entity to export data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、このエンティティを使用して、データをエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>In the second section, you will use <bpt id="p1">**</bpt>Customer Groups<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> entities to import multiple sets of files by using the new Data Import/Export Framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 番目のセクションで、新しいデータのインポート/エクスポート フレームワークを使用することで、<bpt id="p1">**</bpt>顧客グループ<ept id="p1">**</ept>および<bpt id="p2">**</bpt>顧客<ept id="p2">**</ept>エンティティを使用して複数のセットのファイルをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This tutorial is designed to be slightly more challenging than <bpt id="p1">[</bpt>Building and consuming data entities<ept id="p1">](build-consuming-data-entities.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルは、<bpt id="p1">[</bpt>データ エンティティの構築と消費<ept id="p1">](build-consuming-data-entities.md)</ept>よりもさらに少し難しく設計されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Instead of providing a step-by-step guide, it has scenario exercises and describes the expected outcomes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ バイ ステップのガイドを提供するのではなく、シナリオ練習を設けて、期待される結果を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The assumption is that you've already familiarized yourself with entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティをすでに理解していることを前提としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This tutorial requires that you access the environment by using Remote Desktop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>You must be provisioned as an administrator on the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンスに管理者としてプロビジョニングする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Base URL</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準 URL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Throughout this tutorial, "base URL" refers to the base URL of the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、「ベース URL」はインスタンスのベース URL を指します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the cloud environment, you obtain the base URL from Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド環境では、ベース URL は Microsoft Dynamics Lifecycle Services (LCS) から取得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>On a local virtual machine (VM), the base URL is <ph id="ph1">https://usnconeboxax1aos.cloud.onebox.dynamics.com</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル仮想マシン (VM) の、基準 URL は <ph id="ph1">https://usnconeboxax1aos.cloud.onebox.dynamics.com</ph> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Developing an entity in Visual Studio and enabling it for data export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio でエンティティを開発し、データをエクスポートできるようにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Business problem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネスの問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You're developing a new solution for a Project module.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト モジュールの新しいソリューションを開発しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>As part of your implementation, you must represent the data from project categories, so that this data can be imported into the system or exported from it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装の一環として、このデータをシステムにインポートするか、システムからエクスポートできるようにプロジェクト カテゴリのデータを表す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>To accomplish this goal, you will first build an entity for the project category and then use the export functionality to test data extraction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この目標を達成するには、まずプロジェクト カテゴリのエンティティを作成し、エクスポート機能を使用してデータ抽出をテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Exercise 1: Build a Project Category entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 1: プロジェクト カテゴリのエンティティを構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>In this exercise, you will build an entity, <bpt id="p1">**</bpt>Project Category<ept id="p1">**</ept>, that uses the ProjCategory table as its primary data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この練習では、<bpt id="p1">**</bpt>プロジェクト カテゴリ<ept id="p1">**</ept>というエンティティを構築し、ProjCategory テーブルをプライマリ データ ソースとして使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>This entity has the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティには、次のプロパティがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Entity AOT name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ AOT の名前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>ProjectCategoryEntity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProjectCategoryEntity</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Label</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Project Categories</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト カテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Entity category</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ カテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Reference</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">参照</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Public name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パブリック名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>ProjectCategory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProjectCategory</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Collection name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グループ名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>ProjectCategories</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProjectCategories</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Enable public API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パブリック API の有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Enable data management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ管理の有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The entity also has the following fields:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティには、次のフィールドもあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>ActiveInJournals</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ActiveInJournals</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>CategoryGroup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CategoryGroup</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Category</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>TransactionType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TransactionType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>CategoryName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CategoryName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Worker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワーカー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>CustomerPaymentRetention</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerPaymentRetention</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>IndirectCostComponent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IndirectCostComponent</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>ItemSalesTaxGroup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ItemSalesTaxGroup</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>ServiceCode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ServiceCode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Absence</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">休暇</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>In Visual Studio, create a new Microsoft Dynamics 365 for Finance and Operations project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、新しい Microsoft Dynamics 365 for Finance and Operations プロジェクトを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>In Solution Explorer, select the project, and then right-click <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、プロジェクトを選択してから<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept>を右クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Specify the following project properties, and then click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のプロジェクト プロパティを指定し、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Application Suite</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Suite</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Company</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>USSI</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">USSI</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Synchronize Database on build</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド上にデータベースを同期</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>True</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">はい</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>From the project, right-click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>New item<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトから、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>新しい品目<ept id="p2">**</ept>を右クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Select <bpt id="p1">**</bpt>Data Model<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Data Entity<ept id="p2">**</ept> as your new item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ モデル<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>データ エンティティ<ept id="p2">**</ept> を新しい項目として選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Enter a name, and then click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> to start the <bpt id="p2">**</bpt>Data<ept id="p2">**</ept> <bpt id="p3">**</bpt>Entity<ept id="p3">**</ept> wizard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を入力し、次に<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックすると<bpt id="p2">**</bpt>データ<ept id="p2">**</ept> <bpt id="p3">**</bpt>エンティティ<ept id="p3">**</ept>ウィザードが開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>On the first page of the wizard, specify the set of properties for the entity by using the table earlier in this exercise.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィザードの最初のページで、この練習の前の表を使用して、エンティティのプロパティのセットを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Then click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Specify properties page<ept id="p1">](./media/specifyproperties_devoentity.png)](./media/specifyproperties_devoentity.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>プロパティ ページの指定<ept id="p1">](./media/specifyproperties_devoentity.png)](./media/specifyproperties_devoentity.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>On the next page, add fields from the primary data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のページで、プライマリ データ ソースからフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Make sure that each field name reflects the public contract (see the table earlier in this exercise).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名ごとに、パブリック契約が反映されていることを確認します (この練習では前の表を参照してください)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>To use the field's label as the field name, select the <bpt id="p1">**</bpt>Convert label to field names<ept id="p1">**</ept> option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドのラベルをフィールド名として使用するには、<bpt id="p1">**</bpt>ラベルをフィールド名に変換<ept id="p1">**</ept> オプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Clear the option for any fields that are not required for the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティに必須ではないフィールドのオプションをクリアします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Click <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept> to complete the wizard, and to add the entity and its artifacts to the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィザードを完了し、エンティティとそのコンポーネントをプロジェクトに追加するには、<bpt id="p1">**</bpt>完了<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Build your project, so that you can start to use the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの使用を開始できるように、プロジェクトをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Expected outcome</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予想される結果</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>In Visual Studio, the following artifacts will appear in the project after you've completed the <bpt id="p1">**</bpt>Data Entity<ept id="p1">**</ept> wizard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、<bpt id="p1">**</bpt>データ エンティティ<ept id="p1">**</ept> ウィザードを完了すると、次のコンポーネントがプロジェクトに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>New project artifacts<ept id="p1">](./media/testappsuite_devoentity.png)](./media/testappsuite_devoentity.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>新規プロジェクト コンポーネント<ept id="p1">](./media/testappsuite_devoentity.png)](./media/testappsuite_devoentity.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Right-click the data entity, and then select <bpt id="p1">**</bpt>Open table browser<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティを右クリックし、<bpt id="p1">**</bpt>テーブル ブラウザーを開く<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Make sure that your company is set to <bpt id="p1">**</bpt>USSI<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社が <bpt id="p1">**</bpt>USSI<ept id="p1">**</ept> に設定されていることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Exercise 2: Export a limited set of data by using a sample file mapping and filters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 2: サンプル ファイル マッピングおよびフィルターを使用して限られたデータ セットをエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In this exercise, you will use the <bpt id="p1">**</bpt>Project Category<ept id="p1">**</ept> entity that you just built to export data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この練習では、データをエクスポートするために構築した<bpt id="p1">**</bpt>プロジェクト カテゴリ<ept id="p1">**</ept> エンティティを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>To export only a subset of the data, you will use a sample file mapping and filters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのサブセットのみをエクスポートするには、サンプル ファイルのマッピングとフィルターを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The exported data will be in XML format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートされたデータは XML 形式です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>After you've finished building the <bpt id="p1">**</bpt>Project Category<ept id="p1">**</ept> entity, start the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクト カテゴリ<ept id="p1">**</ept> エンティティを作成した後、クライアントを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Change the company to <bpt id="p1">**</bpt>USSI<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社を <bpt id="p1">**</bpt>USSI<ept id="p1">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>In the <bpt id="p1">**</bpt>Data management<ept id="p1">**</ept> workspace, click <bpt id="p2">**</bpt>Export<ept id="p2">**</ept> to begin data extraction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ管理<ept id="p1">**</ept>ワークスペースで、<bpt id="p2">**</bpt>エクスポート<ept id="p2">**</ept>をクリックしてデータの抽出を開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Enter the export details, such as entity name and target data format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ名およびターゲット データ形式などのエクスポートの詳細を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Entering export details<ept id="p1">](./media/exportprojectcategory_devoentity.png)](./media/exportprojectcategory_devoentity.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>エクスポートの詳細の入力<ept id="p1">](./media/exportprojectcategory_devoentity.png)](./media/exportprojectcategory_devoentity.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Use the following file as the sample file format for XML: <bpt id="p1">[</bpt>ProjectCategoryExport<ph id="ph1">\_</ph>Sample<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845209)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">XML のサンプル ファイル形式として、<bpt id="p1">[</bpt>ProjectCategoryExport<ph id="ph1">\_</ph>Sample<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845209)</ept> ファイルを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Open this file in a text editor, and save it as an XML file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト エディタでこのファイルを開き、XML ファイルとして保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>If the sample file mapping isn't valid, there is an incorrect field name in the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプル ファイル マッピングが無効の場合、エンティティに不適切なフィールド名があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Fix either the entity or the sample file to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">続行するため、エンティティまたはサンプル ファイルのいずれかを修正します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Click <bpt id="p1">**</bpt>Filter<ept id="p1">**</ept>, and then specify <bpt id="p2">**</bpt>Project<ept id="p2">**</ept> as the filter criterion, so that only limited data is exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィルター<ept id="p1">**</ept>をクリックし、フィルター条件として<bpt id="p2">**</bpt>プロジェクト<ept id="p2">**</ept>を指定すると、限定されたデータのみがエクスポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Filtering by project<ept id="p1">](./media/inquiry_devoentity.png)](./media/inquiry_devoentity.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>プロジェクトによるフィルター処理<ept id="p1">](./media/inquiry_devoentity.png)](./media/inquiry_devoentity.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>In the <bpt id="p1">**</bpt>Export<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エクスポート<ept id="p1">**</ept> ダイアログ ボックスで、<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Expected outcome</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予想される結果</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Fifteen records are successfully exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">15 のレコードは正常にエクスポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The output is similar to the following file: <bpt id="p1">[</bpt>ProjectCategoryExport<ph id="ph1">\_</ph>Output<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845210)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出力は次のファイルに似ています。<bpt id="p1">[</bpt>ProjectCategoryExport<ph id="ph1">\_</ph>Output<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845210)</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>(Open the file in a text editor to verify this outcome.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(この結果を確認するにはテキスト エディタでファイルを開きます。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Migrating data in multiple files by using the Data Import/Export Framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポート/エクスポート フレームワークを使用した複数のファイルのデータの移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Business problem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネスの問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You're implementing a new environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい環境を実装しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>As part of this implementation, you want to migrate some legacy customer data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この実装の一環として、レガシ顧客データを移行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The data is contained in two sets of files, each of which has data for the <bpt id="p1">**</bpt>Customers<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Customer Groups<ept id="p2">**</ept> entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データは 2 つのファイル セットに含まれ、各ファイルには<bpt id="p1">**</bpt>顧客<ept id="p1">**</ept>および<bpt id="p2">**</bpt>顧客顧客グループ<ept id="p2">**</ept>のエンティティのデータが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>This migration is slightly complex, because some columns in the data files don't map directly to the entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ファイルの一部の列がエンティティに直接マップされないため、この移行はやや複雑です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Additionally, the files have validation errors that must be corrected during the import process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、ファイルには、インポート処理中に修正する必要がある検証エラーがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Exercise 3: Create a data project and import multiple files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 3: データ プロジェクトを作成し、複数のファイルをインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In this exercise, you will import two files into the <bpt id="p1">**</bpt>USRT<ept id="p1">**</ept> company by using the new Data Import/Export Framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この練習では、新しいデータのインポート/エクスポート フレームワークを使用して、2 つのファイルを <bpt id="p1">**</bpt>USRT<ept id="p1">**</ept> という会社にインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>These files need to be imported in sequence by using a single data project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのファイルは、単一のデータ プロジェクトを使用して順番にインポートする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The <bpt id="p1">**</bpt>Customers<ept id="p1">**</ept> entity has a reference to the <bpt id="p2">**</bpt>Customer Groups<ept id="p2">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>顧客<ept id="p1">**</ept> エンティティには、<bpt id="p2">**</bpt>顧客グループ<ept id="p2">**</ept> エンティティへの参照があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Because the Customers1 file doesn't map correctly to the <bpt id="p1">**</bpt>Customers<ept id="p1">**</ept> entity, you will receive an error when you upload the file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Customers1 ファイルが<bpt id="p1">**</bpt>顧客<ept id="p1">**</ept>エンティティに正しくマップされないため、ファイルをアップロードするときにエラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Therefore, to complete the import process, you will have to provide the correct column mappings for the <bpt id="p1">**</bpt>Customers<ept id="p1">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、インポート プロセスを完了するには、<bpt id="p1">**</bpt>Customers<ept id="p1">**</ept> エンティティに正しい列マッピングを提供する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Open the following files in Microsoft Excel, and save them as CSV files in your local directory:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Excel で以下のファイルを開いて、ローカル ディレクトリ内に CSV ファイルとして保存する:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">[</bpt>Customers1<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845211)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Customers1<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845211)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">[</bpt>CustomerGroups1<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845212)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>CustomerGroups1<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845212)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>In the client, change the company to <bpt id="p1">**</bpt>USRT<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントで、会社を <bpt id="p1">**</bpt>USRT<ept id="p1">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>From the <bpt id="p1">**</bpt>User<ept id="p1">**</ept> dashboard, open the <bpt id="p2">**</bpt>Data Management<ept id="p2">**</ept> workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ユーザー<ept id="p1">**</ept>ダッシュ ボードから、<bpt id="p2">**</bpt>データ管理<ept id="p2">**</ept>ワークスペースを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Click <bpt id="p1">**</bpt>Import<ept id="p1">**</ept> to configure a new data project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータ プロジェクトを設定するには、<bpt id="p1">**</bpt>インポート<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Enter the project details, such as the name and file format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前およびファイルの形式などのプロジェクト詳細を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>For each file, select an entity, and then upload the data file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各ファイルについては、エンティティを選択し、次にデータ ファイルをアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Because the Customer1.csv file doesn't map correctly to the <bpt id="p1">**</bpt>Customers<ept id="p1">**</ept> entity, you will receive an error when you upload the file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Customer1.csv ファイルが<bpt id="p1">**</bpt>顧客<ept id="p1">**</ept>エンティティに正しくマップされないため、ファイルをアップロードするときにエラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>After the file is uploaded, click <bpt id="p1">**</bpt>View mappings<ept id="p1">**</ept> to fix the column mappings for the <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルがアップロードされた後、<bpt id="p1">**</bpt>マッピングの表示<ept id="p1">**</ept>をクリックし、<bpt id="p2">**</bpt>顧客<ept id="p2">**</ept>エンティティ列のマッピングを修正します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source><bpt id="p1">**</bpt>CustomerAccount<ept id="p1">**</ept> is required in the entity during import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomerAccount<ept id="p1">**</ept> はインポート中にエンティティで必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>It is mapped from <bpt id="p1">**</bpt>AccountNum<ept id="p1">**</ept> in the source file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース ファイルで <bpt id="p1">**</bpt>AccountNum<ept id="p1">**</ept> からマップされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Address fields are optional for the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">住所フィールドは、インポートのオプションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>When you've finished, click the <bpt id="p1">**</bpt>Back<ept id="p1">**</ept> button in your browser to return to the data project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了したら、ブラウザの <bpt id="p1">**</bpt>戻る<ept id="p1">**</ept> ボタンをクリックして、データ プロジェクトに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>On the <bpt id="p1">**</bpt>Data Project<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Import now<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ プロジェクト<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>今すぐインポート<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Expected outcome</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予想される結果</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Four updates and 23 inserts are successfully imported and the <bpt id="p1">**</bpt>Execution summary<ept id="p1">**</ept> page shows the results.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4 つの更新および 23 の挿入が正常にインポートされ、<bpt id="p1">**</bpt>実行の要約<ept id="p1">**</ept>ページが結果を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Exercise 4: Re-import by using an existing data project and manage data in staging</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 4: 既存のデータ プロジェクトを使い再インポートし、ステージングでデータを管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>In this exercise, you will use a new set of files to import data through the existing data project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この練習では、新しいファイルのセットを使用して、既存のデータ プロジェクトからデータをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Customers2 contains new and updated data for the <bpt id="p1">**</bpt>Customers<ept id="p1">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Customers2 は<bpt id="p1">**</bpt>顧客<ept id="p1">**</ept>エンティティの新規および更新されたデータを含みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>CustomerGroups2 contains updated data for the <bpt id="p1">**</bpt>Customer Groups<ept id="p1">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerGroups2 は<bpt id="p1">**</bpt>顧客グループ<ept id="p1">**</ept> エンティティの更新されたデータを含みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Customers2 contains some error records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Customers2 には、いくつかのエラー レコードが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>You will fix these errors in staging, validate the data, and then push it to the target to complete the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステージングでのこれらのエラーを修正し、データを検証し、それをターゲットに送って、インポートを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>In the <bpt id="p1">**</bpt>Data management<ept id="p1">**</ept> workspace, select the existing data project, and the click <bpt id="p2">**</bpt>Re-import<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ管理<ept id="p1">**</ept>ワークスペースで、既存のデータ プロジェクトを選択し、<bpt id="p2">**</bpt>再インポート<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>By using the re-import functionality, you can preserve your previous settings for the data project and use new files for the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再インポート機能を使用することにより、データ プロジェクトの以前の設定を保持し、インポートに新しいファイルを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>However, if you click <bpt id="p1">**</bpt>Reload data project<ept id="p1">**</ept> and upload new files instead, the previous mappings will be overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>データ プロジェクトの再読み込み<ept id="p1">**</ept>をクリックし、代わりに新しいファイルをアップロードする場合、以前のマッピングが上書きされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Open the following files in Excel, and save them as CSV files in your local directory:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で以下のファイルを開いて、ローカル ディレクトリ内の CSV ファイルとして保存する:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source><bpt id="p1">[</bpt>Customers2<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845213)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Customers2<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845213)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source><bpt id="p1">[</bpt>CustomerGroups2<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845214)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>CustomerGroups2<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=845214)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Upload the new files for each entity, and then click <bpt id="p1">**</bpt>Import now<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各エンティティの新しいファイルをアップロードし、<bpt id="p1">**</bpt>今すぐインポート<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>On the <bpt id="p1">**</bpt>Status<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>View execution log<ept id="p2">**</ept> to investigate the errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステータス<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>実行ログの表示<ept id="p2">**</ept>をクリックしてエラーを調査します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>On the <bpt id="p1">**</bpt>Status<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>View staging<ept id="p2">**</ept> to view the data in a staging table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステータス<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>ステージングの表示<ept id="p2">**</ept>をクリックして、ステージング テーブルのデータを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>This view will also show records that have errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このビューには、エラーのあるレコードも表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> to fix records that have errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーが発生したレコードを修正するには、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>(The <bpt id="p1">**</bpt>Customer Group<ept id="p1">**</ept> value for records DM10221 and DM1022 isn't valid.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(DM10221 および DM1022 レコードの<bpt id="p1">**</bpt>顧客グループ<ept id="p1">**</ept>値は無効です。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Select the records that you fixed, and then click <bpt id="p1">**</bpt>Validate<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正したレコードを選択し、<bpt id="p1">**</bpt>検証<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Refresh the page to verify that the status of the records is <bpt id="p1">**</bpt>Validated<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページを更新し、レコードのステータスが <bpt id="p1">**</bpt>検証済み<ept id="p1">**</ept> であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Click <bpt id="p1">**</bpt>Copy data to target<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データをターゲットにコピー<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>In the <bpt id="p1">**</bpt>Select a job ID to run<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Run for<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>Criteria<ept id="p3">**</ept>, and set <bpt id="p4">**</bpt>Row selected by user<ept id="p4">**</ept> to <bpt id="p5">**</bpt>Yes<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実行するジョブ ID の選択<ept id="p1">**</ept>ダイアログ ボックスの<bpt id="p2">**</bpt>実行<ept id="p2">**</ept>フィールドで<bpt id="p3">**</bpt>基準<ept id="p3">**</ept>を選択して、<bpt id="p4">**</bpt>ユーザーによって選択された行<ept id="p4">**</ept>を<bpt id="p5">**</bpt>はい<ept id="p5">**</ept>に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Then click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Selecting a job to run<ept id="p1">](./media/selectjob_devoentity.png)](./media/selectjob_devoentity.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>実行するジョブの選択<ept id="p1">](./media/selectjob_devoentity.png)](./media/selectjob_devoentity.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>On the <bpt id="p1">**</bpt>Target data execution<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Run<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ターゲット データ実行<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>実行<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>When the run is completed, refresh the page to see the latest staging status.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行が完了したら、ページを更新して、最新のステージングの状態を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Expected outcome</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予想される結果</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>On the first try, the import succeeds for the <bpt id="p1">**</bpt>Customer Groups<ept id="p1">**</ept> entity and partially succeeds for the <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の試行で、<bpt id="p1">**</bpt>顧客グループ<ept id="p1">**</ept>エンティティのインポートが成功し、<bpt id="p2">**</bpt>顧客<ept id="p2">**</ept>エンティティでは部分的に成功します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The <bpt id="p1">**</bpt>Execution summary<ept id="p1">**</ept> page shows that five records were created, three records were updated, and two records have errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実行の概要<ept id="p1">**</ept> ページには、5 つのレコードが作成され、3 つのレコードが更新され、2 つのレコードにエラーがあることが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>In the staging view, two records have errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステージング ビューでは、2 つのレコードにエラーがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>After you fix the records and run the import again, the staging view shows that all records are completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レコードを修正し再度インポートを実行すると、ステージング ビューにすべてのレコードが完了したことが表示されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
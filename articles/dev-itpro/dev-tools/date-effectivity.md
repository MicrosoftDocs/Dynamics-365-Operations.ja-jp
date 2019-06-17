<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="date-effectivity.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>date-effectivity.84d81c.357ee5f87d821a97ec0cc138e0de553b1f2843f3.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>357ee5f87d821a97ec0cc138e0de553b1f2843f3</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\date-effectivity.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Date effectivity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付の有効期間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about date-effective data entities and data sources, and shows how to create a date-effective entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、データ エンティティとデータ ソースの開始日時に関する情報を提供し、エンティティの開始日時を作成する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It also explains how date effectivity applies to read and write activities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、日付の有効性が読み取りおよび書き込みアクティビティに適用される方法についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Date effectivity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付の有効期間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic provides information about date-effective data entities and data sources, and shows how to create a date-effective entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、データ エンティティとデータ ソースの開始日時に関する情報を提供し、エンティティの開始日時を作成する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It also explains how date effectivity applies to read and write activities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、日付の有効性が読み取りおよび書き込みアクティビティに適用される方法についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>There are different design patterns for date-effective features that involve data entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティを含む日付有効機能のデザイン パターンはさまざまです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The patterns are classified into two main categories:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パターンは、次の 2 つの主要なカテゴリに分類されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">**</bpt>Date-effective entities<ept id="p1">**</ept> – The entity has at least one date-effective data source, and the entity itself is also date effective.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効日エンティティ<ept id="p1">**</ept> - エンティティには少なくとも 1 つの有効日データ ソースがあり、エンティティ自体も日付が有効です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source><bpt id="p1">**</bpt>Non-date-effective entities<ept id="p1">**</ept> – The entity itself is not date effective, but it does contain date-effective data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効日の対象外のエンティティ<ept id="p1">**</ept> – エンティティ自体は、有効日ではありませんが、有効日データ ソースが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The next sections describe the small list of properties and methods that control the date-effective behavior of entities and their date-effective data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、プロパティの小さなリストとエンティティの日付を有効にする操作と有効日データ ソースを制御するメソッドについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Date-effective entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効日のエンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The following table describes the properties that control the date-effective behavior of a data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、データ エンティティの日付を有効にする操作を制御するプロパティを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Property name of the entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのプロパティ名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Node of the property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティのノード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>ValidTimeStateEnabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidTimeStateEnabled</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Data entity node in the designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーのデータ エンティティ ノード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Yes (or No)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">はい (またはいいえ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The value <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> makes the entity date effective.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値 <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> は、エンティティの日付を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The entity must have <bpt id="p1">**</bpt>ValidFrom<ept id="p1">**</ept> and <bpt id="p2">**</bpt>ValidTo<ept id="p2">**</ept> fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティには、<bpt id="p1">**</bpt>ValidFrom<ept id="p1">**</ept> および <bpt id="p2">**</bpt>ValidTo<ept id="p2">**</ept> フィールドが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>These fields are mapped to the <bpt id="p1">**</bpt>ValidFrom<ept id="p1">**</ept> and <bpt id="p2">**</bpt>ValidTo<ept id="p2">**</ept> fields of a date-effective data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのフィールドは、有効日データ ソースの <bpt id="p1">**</bpt>ValidFrom<ept id="p1">**</ept> フィールドおよび <bpt id="p2">**</bpt>ValidTo<ept id="p2">**</ept> フィールドにマップされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The value <bpt id="p1">**</bpt>No<ept id="p1">**</ept> does <bpt id="p2">*</bpt>not<ept id="p2">*</ept> disable the enforcement of date effectivity on any date-effective tables that are data sources of the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値 <bpt id="p1">**</bpt>No<ept id="p1">**</ept> は、エンティティのデータ ソースである日付有効テーブルの日付有効性の強制を無効に<bpt id="p2">*</bpt>しません<ept id="p2">*</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>ValidTimeStateKey</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidTimeStateKey</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Under the data entity node, <bpt id="p1">**</bpt>Keys<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>EntityKey<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ ノードの下では、<bpt id="p1">**</bpt>キー<ept id="p1">**</ept><ph id="ph1">&amp;gt;</ph><bpt id="p2">**</bpt>EntityKey<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Yes (or No)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">はい (またはいいえ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The value <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> identifies the key that is required to enforce the date-effective values on this particular entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値 <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> は、この特定のエンティティの日付有効値を実施するために必要なキーを識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Read activities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">読み取りアクティビティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When date effectivity is set at the data entity level, reads from the entity behave the same way as reads from a table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付の有効期限がデータ エンティティ レベルで設定されると、エンティティからの読み取りはテーブルからの読み取りと動作が同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The entity has <bpt id="p1">**</bpt>ValidFrom<ept id="p1">**</ept> and <bpt id="p2">**</bpt>ValidTo<ept id="p2">**</ept> fields that the system applies date filters to during reads.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティには、システムが読み込み中に日付フィルターを適用する <bpt id="p1">**</bpt>ValidFrom<ept id="p1">**</ept> および <bpt id="p2">**</bpt>ValidTo<ept id="p2">**</ept> フィールドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Query modes and the validtimestate keyword of X++ SQL select</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ モードと X++ SQL 選択の validtimestate キーワード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>A date-effective entity supports the following three <bpt id="p1">*</bpt>query modes<ept id="p1">*</ept>, which vary in their use of the X++ <bpt id="p2">**</bpt>validtimestate<ept id="p2">**</ept> keyword:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付有効なエンティティは、X++ <bpt id="p2">**</bpt>validtimestate<ept id="p2">**</ept> キーワードの使用方法が異なる次の 3 つの<bpt id="p1">*</bpt>クエリモード<ept id="p1">*</ept>をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Default mode<ept id="p1">**</ept> – Current records are returned using <ph id="ph1">`select * from FMVehicleRateEntity; // X++ SQL.`</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既定のモード<ept id="p1">**</ept> - 現在のレコードは、<ph id="ph1">`select * from FMVehicleRateEntity; // X++ SQL.`</ph> を使用して返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>AsOfDate mode<ept id="p1">**</ept> – Records valid for the specified date are returned using <ph id="ph1">`select validtimestate(d1) * from FMVehicleRateEntity;`</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AsOfDate モード<ept id="p1">**</ept> - 指定された日付に有効なレコードは <ph id="ph1">`select validtimestate(d1) * from FMVehicleRateEntity;`</ph> を使用して返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>AsOfDateRange mode<ept id="p1">**</ept> – Records valid for the specified date range are returned using <ph id="ph1">`select validtimestate(d1,d2) * from FMVehicleRateEntity;`</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AsOfDateRange モード<ept id="p1">**</ept> - 指定された日付範囲に有効なレコードは <ph id="ph1">`select validtimestate(d1,d2) * from FMVehicleRateEntity;`</ph> を使用して返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Important:<ept id="p1">**</ept> For data entities that aren't themselves date effective, but that have a data-effective data source, only the default query mode is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>重要:<ept id="p1">**</ept> それら自体は有効日ではないデータ エンティティでも、有効日のデータ ソースがある場合には、既定のクエリ モードのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>This concept is discussed later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この概念については、この記事の後半で説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Applying a date filter at the data source level</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース レベルで日付フィルターを適用する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>There are scenarios where date-effective filtering is required outside the data entity, at the data source level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付実効フィルタリングが、データ エンティティの外部、データ ソース レベルで必要とされるシナリオがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>For example, the customer entity (CustTableTestEntity) contains CustTable and LogisticsPostalAddress as data sources, where LogisticsPostalAddress is a date-effective table and CustTable is a regular table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、顧客エンティティ (CustTableTestEntity) にはデータ ソースとして CustTable および LogisticsPostalAddress が含まれています。LogisticsPostalAddress は日付の有効なテーブルであり、CustTable は通常のテーブルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The purpose of a customer entity is to have a list of customers and their active primary addresses, if they have primary addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客エンティティの目的は、顧客とそのアクティブなプライマリ アドレスのリスト (プライマリ アドレスがある場合) を含めることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Therefore, the customer entity itself isn't date effective, but it requires date filters on one of the data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、顧客エンティティ自体は日付有効ではありませんが、データ ソースの 1 つに日付フィルターが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>In this case, the entity isn't marked <bpt id="p1">**</bpt>ValidTimeStateEnabled<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、エンティティは <bpt id="p1">**</bpt>ValidTimeStateEnabled<ept id="p1">**</ept> にマークされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Instead, an <bpt id="p1">**</bpt>Apply Date Filter<ept id="p1">**</ept> property is added on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、<bpt id="p1">**</bpt>日付フィルターの適用<ept id="p1">**</ept>プロパティがデータ ソースに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>If the value of <bpt id="p1">**</bpt>Apply Date Filter<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, date filters are automatically applied to that data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>日付フィルターの適用<ept id="p1">**</ept>の値が<bpt id="p2">**</bpt>はい<ept id="p2">**</ept>に設定されている場合、日付フィルターがそのデータ ソースに自動的に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The following table describes the properties that control the date-effective behavior of a date-effective data source of a data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルでは、データ エンティティの有効日データ ソースの有効日動作を制御するプロパティについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Property name of the data source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースのプロパティ名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Node of the property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティのノード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Apply Date Filter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付フィルターの適用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Node of any particular data source of the entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの特定のデータ ソースのノード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Yes (or No)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">はい (またはいいえ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>For <bpt id="p1">*</bpt>reads<ept id="p1">*</ept>, this property controls whether date filters are applied on the entity data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>読み取り<ept id="p1">*</ept>で、このプロパティは、エンティティ データ ソースで日付フィルターが適用されるかどうかを制御します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>In this case, the data source should be marked <bpt id="p1">**</bpt>ValidTimeStateEnabled<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、データ ソースを <bpt id="p1">**</bpt>ValidTimeStateEnabled<ept id="p1">**</ept> にマークする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This property value has effect regardless of whether the entity itself is date effective.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティ値は、エンティティ自体が日付有効であるかどうかにかかわらず有効です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>For <bpt id="p1">*</bpt>writes<ept id="p1">*</ept>, this property has no effect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>書き込み<ept id="p1">*</ept>で、このプロパティは影響を与えません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>This article describes the use of these date-effective properties and the interactions between them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、これらの日付が有効なプロパティの使用方法とそれらの相互作用について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>State matrixes for reads</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">読み取り用の状態マトリックス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>This section concerns only reads from the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションは、データ エンティティからの読み取りのみに関係します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The following pair of reference matrixes describe the combinations of date-effective states that can exist between a data entity and its data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の一対の参照マトリックスは、データ エンティティとそのデータ ソースとの間に存在できる日付有効状態の組み合わせについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Each table contains four cases, and each case discusses two distinct targets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各テーブルには、4 つのクラスが含まれ、各ケースでは、2 つの異なるターゲットについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Here are the primary points that you should understand:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">理解しておく必要がある主要なポイントを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>On any given read from the entity, the query mode is the same for both the entity and date-effective data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティから指定された読み取りで、クエリ モードはエンティティと有効日データ ソースの両方で同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>If the entity is not date effective, the query mode is limited to the default mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの日付が有効ではない場合、クエリ モードは既定のモードに限定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Therefore, the date-effective data source is accessed only for the current date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、日付が有効なデータ ソースは現在の日付のみにアクセスされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>On the date-effective data source, the <bpt id="p1">**</bpt>Apply Date Filter<ept id="p1">**</ept> property can be set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept> to make the data source return all data – past, current, and future.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効日データ ソースで、<bpt id="p1">**</bpt>日付フィルターの適用<ept id="p1">**</ept>プロパティを<bpt id="p2">**</bpt>いいえ<ept id="p2">**</ept>に設定すると、過去、現在、未来のすべてのデータをデータソースに戻すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>For OData, date-effective filters are not applied to the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData で、日付の有効なフィルターはデータ エンティティには適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>However, filters on the data source are applied at all code paths.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、データ ソースのフィルターはすべてのコード パスに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>A.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">A.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Entity <bpt id="p1">*</bpt>is<ept id="p1">*</ept> date effective, because ValidTimeStateEnabled = Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティは有効日で<bpt id="p1">*</bpt>ある<ept id="p1">*</ept>、なぜならば ValidTimeStateEnabled = はい</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">**</bpt>Data source <bpt id="p2">*</bpt>is<ept id="p2">*</ept> date effective<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ ソース<bpt id="p2">*</bpt>は<ept id="p2">*</ept>日付が有効<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">**</bpt>Data source is <bpt id="p2">*</bpt>not<ept id="p2">*</ept> date effective<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ ソース<bpt id="p2">*</bpt>は<ept id="p2">*</ept>日付が有効ではない<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">**</bpt>Apply Date Filter = Yes<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>日付フィルターの適用 = はい<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><bpt id="p1">**</bpt>Entity:<ept id="p1">**</ept> Date filters are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティ<ept id="p1">**</ept> 日付フィルターが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Any query mode is supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのクエリ モードがサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source><bpt id="p1">**</bpt>Data source:<ept id="p1">**</ept> Filters are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ ソース:<ept id="p1">**</ept> フィルターが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Any query mode is supported, but the mode is the same as is coded for the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ モードはサポートされていますが、モードはエンティティのコードと同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Non-date-effective data sources aren't affected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効日の対象外のデータ ソースは影響しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Apply Date Filter = No<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>日付フィルターの適用 = いいえ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source><bpt id="p1">**</bpt>Entity:<ept id="p1">**</ept> Date filters are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティ<ept id="p1">**</ept> 日付フィルターが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Any query mode is supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのクエリ モードがサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source><bpt id="p1">**</bpt>Data source:<ept id="p1">**</ept> No date filters are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ ソース:<ept id="p1">**</ept> 日付フィルターは適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Non-date-effective data sources aren't affected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効日の対象外のデータ ソースは影響しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>B.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">B.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Entity is <bpt id="p1">*</bpt>not<ept id="p1">*</ept> date effective, because ValidTimeStateEnabled = No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティは有効日では<bpt id="p1">*</bpt>ない<ept id="p1">*</ept>、なぜならば ValidTimeStateEnabled = いいえ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source><bpt id="p1">**</bpt>Data source <bpt id="p2">*</bpt>is<ept id="p2">*</ept> date effective<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ ソース<bpt id="p2">*</bpt>は<ept id="p2">*</ept>日付が有効<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Data source is <bpt id="p2">*</bpt>not<ept id="p2">*</ept> date effective<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ ソース<bpt id="p2">*</bpt>は<ept id="p2">*</ept>日付が有効ではない<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Apply Date Filter = Yes<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>日付フィルターの適用 = はい<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Entity:<ept id="p1">**</ept> No date filters are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティ<ept id="p1">**</ept> 日付フィルターが適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source><bpt id="p1">**</bpt>Data source:<ept id="p1">**</ept> Date filters are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ ソース:<ept id="p1">**</ept> 日付フィルターが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Only the default query mode is supported, where the X++ <bpt id="p1">**</bpt>validtimestate<ept id="p1">**</ept> keyword is omitted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のクエリ モードのみサポートされ、X++ <bpt id="p1">**</bpt>validtimestate<ept id="p1">**</ept> キーワードは省略されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Non-date-effective data sources aren't affected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効日の対象外のデータ ソースは影響しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Apply Date Filter = No<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>日付フィルターの適用 = いいえ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">**</bpt>Entity:<ept id="p1">**</ept> No date filters are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティ<ept id="p1">**</ept> 日付フィルターが適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Data source:<ept id="p1">**</ept> No date filters are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ ソース:<ept id="p1">**</ept> 日付フィルターは適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Non-date-effective data sources aren't affected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効日の対象外のデータ ソースは影響しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>The following screen shot shows the <bpt id="p1">**</bpt>Apply Date Filter<ept id="p1">**</ept> property set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットは、<bpt id="p1">**</bpt>日付フィルターの適用<ept id="p1">**</ept> プロパティを <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> に設定したものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Therefore, date filters will be applied to reads of the <bpt id="p1">**</bpt>Address<ept id="p1">**</ept> data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p1">**</bpt>Address<ept id="p1">**</ept> データ ソースの読み取りに日付フィルターが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Apply Date Filter = Yes<ept id="p1">](./media/date1.png)](./media/date1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>日付フィルターの適用 = はい<ept id="p1">](./media/date1.png)](./media/date1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Write activities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">活動の記述</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>This section describes your options for configuring the behavior of date-effective entities and their date-effective data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、有効日エンティティとその有効日データ ソースの動作を設定するオプションについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>We will start by reviewing the concept of date-effective tables and contrasting them with date-effective entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効日テーブルの概念を確認し、それを有効日エンティティと対比させることから開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Date-effective table:<ept id="p1">**</ept> When data is inserted or updated in a date-effective table, the process has the option of calling the <bpt id="p2">**</bpt>xRecord.validTimeStateUpdateMode<ept id="p2">**</ept> method on the table buffer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効日テーブル:<ept id="p1">**</ept> データが有効日テーブルに挿入または更新されると、プロセスは、<bpt id="p2">**</bpt>xRecord.validTimeStateUpdateMode<ept id="p2">**</ept> メソッドをテーブルバッファーで呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>The method accepts an element of the <bpt id="p1">**</bpt>ValidTimeStateUpdate<ept id="p1">**</ept> enumeration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、<bpt id="p1">**</bpt>ValidTimeStateUpdate<ept id="p1">**</ept> 列挙型の要素を受け入れます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Here are the available element values:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用可能な要素値を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>CreateNewTimePeriod</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateNewTimePeriod</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Correction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">訂正</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>EffectiveBased</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EffectiveBased</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source><bpt id="p1">**</bpt>Date-effective entity:<ept id="p1">**</ept> By contrast, when data is inserted or updated in a date-effective data entity, the <bpt id="p2">**</bpt>validTimeStateUpdateMode<ept id="p2">**</ept> method isn't used at the entity level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効日エンティティ:<ept id="p1">**</ept> 対照的に、データが有効日データ エンティティに挿入または更新されると、<bpt id="p2">**</bpt>validTimeStateUpdateMode<ept id="p2">**</ept> メソッドはエンティティ レベルで使用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>For writes, the data entity leaves the date-effective processing to the table level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">書き込みについては、データ エンティティは、テーブル レベルに有効日プロセスを残します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>You can use the <bpt id="p1">**</bpt>Valid Time State Update<ept id="p1">**</ept> property on the entity data source to specify the <bpt id="p2">**</bpt>validTimeStateUpdateMode<ept id="p2">**</ept> method to use for each data source of the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ データ ソース上で <bpt id="p1">**</bpt>有効時間状態の更新<ept id="p1">**</ept> プロパティを使用すると、データ エンティティの各データ ソースのために <bpt id="p2">**</bpt>validTimeStateUpdateMode<ept id="p2">**</ept> メソッドを使用することを指定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Creating a date-effective entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付有効なエンティティを作成しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>This section shows how to create a date-effective entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、有効日のあるエンティティを作成する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Create a new project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいプロジェクトの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Click <bpt id="p1">**</bpt>File<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>New<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Project<ept id="p3">**</ept> to create a new project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>新規<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>プロジェクト<ept id="p3">**</ept>とクリックし、新しいプロジェクトを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>In Solution Explorer, right-click your project, and then click <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、プロジェクトを右クリックしてから<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The <bpt id="p1">**</bpt>Property Pages<ept id="p1">**</ept> dialog box for your project opens.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトの <bpt id="p1">**</bpt>プロパティ ページ<ept id="p1">**</ept> ダイアログ ボックスが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Change the value of the <bpt id="p1">**</bpt>Synchronize database on build<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>True<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>OK<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビルドでのデータベースの同期<ept id="p1">**</ept>プロパティの値を <bpt id="p2">**</bpt>True<ept id="p2">**</ept> に変更し、<bpt id="p3">**</bpt>OK<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>You must set this property only one time per project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティはプロジェクトごとに 1 回のみ設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Synchronize database on build = True<ept id="p1">](./media/date3.png)](./media/date3.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ビルド上にデータベースを同期 =True<ept id="p1">](./media/date3.png)](./media/date3.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Add a new data entity to your project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトへの新しいデータ エンティティの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Create a new entity that is named <bpt id="p1">**</bpt>FMVehicleRateEntity<ept id="p1">**</ept>, and add it to the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMVehicleRateEntity<ept id="p1">**</ept> という名前の新しいエンティティを作成し、プロジェクトに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In the left pane, select <bpt id="p1">**</bpt>Microsoft Dynamics 365 Artifacts<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Data Entity<ept id="p2">**</ept> in the left column of the main pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左ウィンドウで <bpt id="p1">**</bpt>Microsoft Dynamics 365 アーティファクト<ept id="p1">**</ept>を選択してから、メイン ウィンドウの左側にある<bpt id="p2">**</bpt>データ エンティティ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The <bpt id="p1">**</bpt>Data Entity View<ept id="p1">**</ept> wizard starts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ エンティティ ビュー<ept id="p1">**</ept> ウィザードが起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Specify the property values for the data entity that you are creating, as shown in the following screen shot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットに表示される作成するデータ エンティティのプロパティ値を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The most important field is <bpt id="p1">**</bpt>Primary data source<ept id="p1">**</ept>, where you select <bpt id="p2">**</bpt>FMVehicleRate<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最も重要なフィールドは、<bpt id="p1">**</bpt>FMVehicleRate<ept id="p1">**</ept> を選択する <bpt id="p2">**</bpt>プライマリ データ ソース<ept id="p2">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Primary data source = FMVehicleRate<ept id="p1">](./media/date5.png)](./media/date5.png)</ept> Click <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>プライマリ データ ソース =FMVehicleRate<ept id="p1">](./media/date5.png)](./media/date5.png)</ept> <bpt id="p2">**</bpt>次へ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Add fields to the entity from the primary data source, <bpt id="p1">**</bpt>FMVehicleRate<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライマリ データ ソース、<bpt id="p1">**</bpt>FMVehicleRate<ept id="p1">**</ept> からエンティティにフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Select all fields, and then click <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのフィールドを選択し、<bpt id="p1">**</bpt>完了<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Selecting all the newly added fields<ept id="p1">](./media/date6.png)](./media/date6.png)</ept> The items are added to the project in Solution Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>新たに追加されたフィールドをすべて選択する<ept id="p1">](./media/date6.png)](./media/date6.png)</ept>品目は、ソリューション エクスプ ローラーのプロジェクトに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>The project in Solution Explorer<ept id="p1">](./media/date7.png)](./media/date7.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ソリューション エクスプローラー内のプロジェクト<ept id="p1">](./media/date7.png)](./media/date7.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Build your project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Click <bpt id="p1">**</bpt>Build<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Build Solution<ept id="p2">**</ept> to build your project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビルド<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ソリューションのビルド<ept id="p2">**</ept>とクリックし、プロジェクトを構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Verify that the build has no errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドにエラーが含まれていないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Warnings should be tolerated at this stage in the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスのこの段階では、警告を容認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Validate the property values</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ値の検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>In Solution Explorer, select the <bpt id="p1">**</bpt>FMVehicleRateEntity<ept id="p1">**</ept> node, and validate the properties of the <bpt id="p2">**</bpt>FMVehicleRateEntity<ept id="p2">**</ept> entity by comparing them to the values in the <bpt id="p3">**</bpt>Properties<ept id="p3">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>FMVehicleRateEntity<ept id="p1">**</ept> ノードを選択し、<bpt id="p2">**</bpt>FMVehicleRateEntity<ept id="p2">**</ept> エンティティのプロパティを<bpt id="p3">**</bpt>プロパティ<ept id="p3">**</ept> ウィンドウの値と比較して確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Values in the Properties pane<ept id="p1">](./media/date8.png)](./media/date8.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>プロパティ ウィンドウの値<ept id="p1">](./media/date8.png)](./media/date8.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Make your entity date effective</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの日付を有効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>In Solution Explorer, right-click the <bpt id="p1">**</bpt>FMVehicleRateEntity<ept id="p1">**</ept> node, and then click <bpt id="p2">**</bpt>Open<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>FMVehicleRateEntity<ept id="p1">**</ept> ノードを右クリックしてから<bpt id="p2">**</bpt>開く<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The designer for the entity opens in the middle pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのデザイナーが中央のウィンドウに開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Designer for the FMVehicleRateEntity entity<ept id="p1">](./media/date9.png)](./media/date9.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMVehicleRateEntity エンティティのデザイナー<ept id="p1">](./media/date9.png)](./media/date9.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Change the value of the <bpt id="p1">**</bpt>Validate Time State Enabled<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>時間状態が有効であるかどうかを検証する<ept id="p1">**</ept>プロパティの値を<bpt id="p2">**</bpt>はい<ept id="p2">**</ept>に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Validate Time State Enabled = Yes<ept id="p1">](./media/date10.png)](./media/date10.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>時間状態が有効であるかどうかを検証する = はい<ept id="p1">](./media/date10.png)](./media/date10.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Configure the Valid Time State Update property for the date-effective data source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効日データソースの有効時間状態の更新プロパティのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Select the <bpt id="p1">**</bpt>FMVehicleRate<ept id="p1">**</ept> data source, and then set the <bpt id="p2">**</bpt>Valid Time State Update<ept id="p2">**</ept> property to <bpt id="p3">**</bpt>CreateNewTimePeriod<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMVehicleRate<ept id="p1">**</ept> データ ソースを選択し、<bpt id="p2">**</bpt>有効時間状態の更新<ept id="p2">**</ept> プロパティを <bpt id="p3">**</bpt>CreateNewTimePeriod<ept id="p3">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Valid Time State Update = CreateNewTimePeriod<ept id="p1">](./media/date11.png)](./media/date11.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>有効時間状態の更新 = CreateNewTimePeriod<ept id="p1">](./media/date11.png)](./media/date11.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Test your project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをテスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Build your project again, and run the following X++ job to test your project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを再度ビルドし、次の X++ ジョブを実行してプロジェクトをテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Testing the project<ept id="p1">](./media/capa-504x1024.png)](./media/capa.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>プロジェクトのテスト<ept id="p1">](./media/capa-504x1024.png)](./media/capa.png)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
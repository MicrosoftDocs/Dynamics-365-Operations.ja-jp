<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="validations-defaults-unmapped-fields.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>validations-defaults-unmapped-fields.884741.af8d38ccc48db39ab7bf071c54a86e2786be18c1.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>af8d38ccc48db39ab7bf071c54a86e2786be18c1</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\data-entities\validations-defaults-unmapped-fields.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Validations, default values, and unmapped fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証、既定値、およびマップされていないフィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how data entity values are validated, how default values can be provided, and how to use fields that are not mapped to data source values, but instead contain virtual or computed data (unmapped fields).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、データ エンティティの値を検証する方法、既定値を設定する方法、およびデータ ソース値にマップされないが、代わりに仮想または計算のデータが含まれるフィールド (マップされていないフィールド) を使用する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Validations, default values, and unmapped fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証、既定値、およびマップされていないフィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes how data entity values are validated, how default values can be provided, and how to use fields that are not mapped to data source values, but instead contain virtual or computed data (unmapped fields).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、データ エンティティの値を検証する方法、既定値を設定する方法、およびデータ ソース値にマップされないが、代わりに仮想または計算のデータが含まれるフィールド (マップされていないフィールド) を使用する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Validations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Validations can be defined on the tables that back up entities, at both the field level and the record level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証は、フィールド レベルとレコード レベルの両方でエンティティをバックアップするテーブルで定義できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Validations can also be defined at the data entity level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証は、データ エンティティ レベルで定義することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Table (data source) vs. entity validation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル (データ ソース) とエンティティ検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Entities are backed by tables (data sources), and validations are defined for these tables at both the field level (<bpt id="p1">**</bpt>Table.validateField()<ept id="p1">**</ept>) and the record level (<bpt id="p2">**</bpt>Table.validateWrite()<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティはテーブル (データ ソース) によって戻され、検証はフィールド レベル (<bpt id="p1">**</bpt>Table.validateField()<ept id="p1">**</ept>) とレコード レベル (<bpt id="p2">**</bpt>Table.validateWrite()<ept id="p2">**</ept>) の両方でテーブルに対して定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The validations are respected by data entities that are built by using those tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証は、これらのテーブルを使用して構築されたデータ エンティティによって考慮されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Although these validations are intrinsic to the tables that back a data entity, validations can also be defined at the data entity level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの検証はデータ エンティティを戻すテーブルに組み込まれますが、検証はデータ エンティティ レベルで定義することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Like table-based validations, entity-based validations can be written at the field level (<bpt id="p1">**</bpt>DataEntity.validateField()<ept id="p1">**</ept>) or the record level (<bpt id="p2">**</bpt>DataEntity.validateWrite()<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルに基づく検証と同様に、エンティティに基づく検証はフィールド レベル (<bpt id="p1">**</bpt>DataEntity.validateField()<ept id="p1">**</ept>) またはレコード レベル (<bpt id="p2">**</bpt>DataEntity.validateWrite()<ept id="p2">**</ept>) で書き込むことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Table-based validation behavior</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル ベースの検証動作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Table validations are fired automatically as a part of the CUD operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの検証は CUD 操作の一部として自動的に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Table.ValidateField, AllowEdit, AllowEditOnCreate<ept id="p1">**</ept> Field-level validations are fired automatically when you perform inserts or updates on the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Table.ValidateField、AllowEdit、AllowEditOnCreate<ept id="p1">**</ept> フィールド レベルの検証は、データ エンティティで挿入または更新を実行する時に、自動的に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>This is true for all paths (X++, OData, and so on).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、すべてのパス (X++、OData など) に当てはまります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>These validations occur during the mapping process, when fields are mapped from an entity to individual data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの検証は、エンティティから個々のデータ ソースにフィールドがマップされるマッピング処理中に行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>redo1<ept id="p1">](./media/redo1-1024x582.png)](./media/redo1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>redo1<ept id="p1">](./media/redo1-1024x582.png)](./media/redo1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>After the field values from the data entity are copied to mapped data source fields, field validations are run on the set fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティからフィールド値がマップされたデータ ソース フィールドにコピーされた後、フィールドの検証は設定されたフィールドで実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Validations include table-level <bpt id="p1">**</bpt>validateField<ept id="p1">**</ept>, which validates <bpt id="p2">**</bpt>AllowEdit<ept id="p2">**</ept> and <bpt id="p3">**</bpt>AllowEditOnCreate<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証にはテーブル レベルの <bpt id="p1">**</bpt>validateField<ept id="p1">**</ept> が含まれ、<bpt id="p2">**</bpt>AllowEdit<ept id="p2">**</ept> および <bpt id="p3">**</bpt>AllowEditOnCreate<ept id="p3">**</ept> を検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>If a validation fails because of an error, validation for the remaining fields continues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーにより検証が失敗した場合、残りのフィールドの検証が続行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Finally, validation checks whether any error occurred during the validation process for any of the data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、データ ソースのいずれかの検証プロセス中に発生したエラーが発生したかどうかを、検証によって確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If there was an error, the process errors out at this point, and table-level <bpt id="p1">**</bpt>validateWrite()<ept id="p1">**</ept> isn't called.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーがあった場合、この時点でプロセス エラーが発生するようになり、テーブル レベルの <bpt id="p1">**</bpt>validateWrite()<ept id="p1">**</ept> は呼び出されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To skip <bpt id="p1">**</bpt>validateField<ept id="p1">**</ept> for a back-end table, a consumer can call <bpt id="p2">**</bpt>DataEntity.skipDataSourceValidateField(Int <ph id="ph1">\_</ph>DataEntityFieldId, Boolean <ph id="ph2">\_</ph>skip)<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックエンド テーブルに対して <bpt id="p1">**</bpt>validateField<ept id="p1">**</ept> をスキップするには、コンシューマーは<bpt id="p2">**</bpt>DataEntity.skipDataSourceValidateField(Int <ph id="ph1">\_</ph>DataEntityFieldId, ブール値 <ph id="ph2">\_</ph>skip)<ept id="p2">**</ept> を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Note that the field ID for this method is the field ID of the data-entity mapped field, not the back-end table field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドのフィールド ID は、データ エンティティにマップされたフィールドのフィールド ID であり、フィールドに、バックエンド テーブルのフィールドではないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>By using the following API, you can skip validation for a particular field, regardless of the consumer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の API を使用することによって、コンシューマーに関係なく、特定のフィールドの検証をスキップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Over9<ept id="p1">](./media/over9.png)](./media/over9.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Over9<ept id="p1">](./media/over9.png)](./media/over9.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Table.ValidateWrite<ept id="p1">**</ept> Record-level <bpt id="p2">**</bpt>ValidateWrite<ept id="p2">**</ept> validations that are defined in back-end tables are fired automatically when you perform data-entity inserts and updates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Table.ValidateWrite<ept id="p1">**</ept> レコード レベル <bpt id="p2">**</bpt>Table.ValidateWrite<ept id="p2">**</ept> バックエンドテーブルに定義されている検証は、データ エンティティの挿入および更新を実行すると自動的に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>This is true for all paths (X++, OData, and so on).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、すべてのパス (X++、OData など) に当てはまります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>These validations occur just before the actual insert or update is applied to the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの検証は、実際の挿入または更新がデータ ソースに適用される直前に行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>If the validation fails, an error is thrown, and the process stops for other data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証が失敗すると、エラーが発生し、その他のデータ ソースのプロセスが停止されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>redo2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">redo2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>To skip <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> for all back-end tables for a data entity, a consumer can call <bpt id="p2">**</bpt>DataEntity.skipDataSourceValidateWrite(Boolean <ph id="ph1">\_</ph>skip)<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのすべてのバックエンド テーブルに対して <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> をスキップするには、コンシューマーは <bpt id="p2">**</bpt>DataEntity.skipDataSourceValidateWrite(ブール値 <ph id="ph1">\_</ph>skip)<ept id="p2">**</ept> を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>This method turns <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> on or off for all data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、すべてのデータソースに対して <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> をオンまたはオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>By using the following API, you can skip validation for a particular field, regardless of the consumer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の API を使用することによって、コンシューマーに関係なく、特定のフィールドの検証をスキップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Over10<ept id="p1">](./media/over10.png)](./media/over10.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Over10<ept id="p1">](./media/over10.png)](./media/over10.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Table.ValidateDelete<ept id="p1">**</ept> Record-level <bpt id="p2">**</bpt>ValidateDelete<ept id="p2">**</ept> validations that are defined in back-end tables are fired automatically when you perform data entity deletes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バック エンド テーブルに定義されている<bpt id="p1">**</bpt>Table.ValidateDelete<ept id="p1">**</ept> レコード レベル <bpt id="p2">**</bpt>ValidateDelete<ept id="p2">**</ept> 検証は、データ エンティティの削除を実行すると自動的に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>This is true for all paths (X++, OData, and so on).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、すべてのパス (X++、OData など) に当てはまります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>These validations occur just before the delete is applied to the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの検証は、削除がデータ ソースに適用される直前に行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>If the validation fails, an error is thrown, and the process stops for other data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証が失敗すると、エラーが発生し、その他のデータ ソースのプロセスが停止されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Over11<ept id="p1">](./media/over11.png)](./media/over11.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Over11<ept id="p1">](./media/over11.png)](./media/over11.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>To skip <bpt id="p1">**</bpt>validateDelete<ept id="p1">**</ept> for all back-end tables for a data entity, a consumer can call <bpt id="p2">**</bpt>DataEntity.skipDataSourceValidateDelete(Boolean <ph id="ph1">\_</ph>skip)<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのすべてのバックエンド テーブルに対して <bpt id="p1">**</bpt>validateDelete<ept id="p1">**</ept> をスキップするには、コンシューマーは <bpt id="p2">**</bpt>DataEntity.skipDataSourceValidateDelete(ブール値 <ph id="ph1">\_</ph>skip)<ept id="p2">**</ept> を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>This method turns <bpt id="p1">**</bpt>validateDelete<ept id="p1">**</ept> on or off for all data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、すべてのデータソースに対して <bpt id="p1">**</bpt>validateDelete<ept id="p1">**</ept> をオンまたはオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>By using the following API, you can skip validation for a particular data source, regardless of the consumer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の API を使用すると、コンシューマーに関係なく、特定のデータ ソースの検証をスキップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Over12<ept id="p1">](./media/over12.png)](./media/over12.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Over12<ept id="p1">](./media/over12.png)](./media/over12.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Entity-based validation behavior</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ ベースの検証動作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Validation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Target</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Caller</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">呼び出し側</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>DataEntity.ValidateField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntity.ValidateField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Mandatory relationships (both tables and extended data types [EDTs])</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必須の関係 (テーブルおよび拡張データ型 [EDT] の両方)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Any custom validation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Doesn't call <bpt id="p1">&lt;strong&gt;</bpt>validateField<ept id="p1">&lt;/strong&gt;</ept> for underlying mapped table fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本マップのテーブル フィールドの <bpt id="p1">&lt;strong&gt;</bpt>validateField<ept id="p1">&lt;/strong&gt;</ept> を呼び出さないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Is called automatically from OData</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData から自動的に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Is called by the form engine when a field is modified</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドが変更されたときに、フォーム エンジンで呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Isn't called automatically if an insert/update is fired from X++ code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">挿入/更新が X++ コードから発生した場合は、自動的に呼び出されません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>DataEntity.ValidateWrite</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntity.ValidateWrite</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Mandatory columns</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必須の列</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Relationships (both tables and EDTs)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係 (テーブルおよび EDT の両方)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Any custom validation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Doesn't call table-level <bpt id="p1">&lt;strong&gt;</bpt>validateWrite<ept id="p1">&lt;/strong&gt;</ept> for underlying tables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本テーブルのテーブル レベル <bpt id="p1">&lt;strong&gt;</bpt>validateWrite<ept id="p1">&lt;/strong&gt;</ept> を呼び出さないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Is called automatically from OData</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData から自動的に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Is called by the form engine when a record is saved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レコードが保存されたときに、フォーム エンジンで呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Isn't called automatically if an insert/update is fired from X++ code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">挿入/更新が X++ コードから発生した場合は、自動的に呼び出されません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>DataEntity.ValidateDelete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntity.ValidateDelete</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>DeleteActions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DeleteActions</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Any custom validation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Doesn't call table-level <bpt id="p1">&lt;strong&gt;</bpt>validateDelete<ept id="p1">&lt;/strong&gt;</ept> for underlying tables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本テーブルの テーブル レベル <bpt id="p1">&lt;strong&gt;</bpt>validateDelete<ept id="p1">&lt;/strong&gt;</ept> を呼び出さないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Is called automatically from OData.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData から自動的に呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Is called by the form engine when a record is deleted</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レコードが削除されたときに、フォーム エンジンで呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Isn't called automatically if a delete is fired from X++ code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除が X++ コードから発生した場合は、自動的に呼び出されません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Defaults</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Default values can be provided for initializations and rows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">初期化と行には既定値を指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Initializations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">初期化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><bpt id="p1">**</bpt>DataEntity.initValue:<ept id="p1">**</ept> A data entity is initialized with default values and by using any custom logic that is present in entity-level <bpt id="p2">**</bpt>initValue<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DataEntity.initValue:<ept id="p1">**</ept> データ エンティティは、既定値で、エンティティ レベル <bpt id="p2">**</bpt>initValue<ept id="p2">**</ept> に存在するカスタム ロジックを使用して初期化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This method isn't called automatically when an insert or update is performed on a data entity from X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、X++ からのデータ エンティティに対して挿入または更新が実行されたときに自動的に呼び出されることはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>It must be called explicitly if it's required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な場合に明示的に呼び出す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The method is called automatically by the form engine when a new record is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、新しいレコードが作成されるときにフォーム エンジンによって自動的に呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>DataEntity.initValue<ept id="p1">**</ept> doesn't call the <bpt id="p2">**</bpt>initValue<ept id="p2">**</ept> method for back-end tables that are used in the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DataEntity.initValue<ept id="p1">**</ept> は、データ エンティティで使用されるバック エンド テーブルの <bpt id="p2">**</bpt>initValue<ept id="p2">**</ept> メソッドを呼び出しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Table.initValue:<ept id="p1">**</ept> Table-level <bpt id="p2">**</bpt>initValue<ept id="p2">**</ept>, as defined for back-end tables, is fired when you perform a data entity insert.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Table.initValue:<ept id="p1">**</ept> テーブル レベル <bpt id="p2">**</bpt>initValue<ept id="p2">**</ept> は、バック エンド テーブル定義に従って、データ エンティティの挿入を実行するときに発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This is true for all paths (X++, OData, and so on).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、すべてのパス (X++、OData など) に当てはまります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Table.initValue<ept id="p1">**</ept> is run just before the entity is mapped to data source fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Table.initValue<ept id="p1">**</ept> はエンティティがデータ ソース フィールドにマップされる直前に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Over13<ept id="p1">](./media/over13.png)](./media/over13.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Over13<ept id="p1">](./media/over13.png)](./media/over13.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>To skip entity-level <bpt id="p1">**</bpt>initValue<ept id="p1">**</ept> for all back-end tables for a data entity, a consumer can call <bpt id="p2">**</bpt>DataEntity.skipDataSourceInitValue(Boolean <ph id="ph1">\_</ph>skip)<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのすべてのバックエンド テーブルに対してエンティティ レベルの <bpt id="p1">**</bpt>initValue<ept id="p1">**</ept> をスキップするには、コンシューマーは <bpt id="p2">**</bpt>DataEntity.skipDataSourceInitValue(ブール値 <ph id="ph1">\_</ph>skip)<ept id="p2">**</ept> を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>This method turns <bpt id="p1">**</bpt>initValue<ept id="p1">**</ept> on or off for all data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、すべてのデータソースに対して <bpt id="p1">**</bpt>initValue<ept id="p1">**</ept> をオンまたはオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>By using the following API, you can skip <bpt id="p1">**</bpt>initValue<ept id="p1">**</ept> for a particular field, regardless of the consumer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の API を使用することによって、コンシューマーに関係なく、特定のフィールドの <bpt id="p1">**</bpt>initValue<ept id="p1">**</ept> をスキップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Capturea<ept id="p1">](./media/capturea.png)](./media/capturea.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Capturea<ept id="p1">](./media/capturea.png)](./media/capturea.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>DefaultRow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DefaultRow</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>DataEntity.DefaultRow: DataEntity.DefaultRow<ept id="p1">**</ept> is used in conjunction with <bpt id="p2">**</bpt>defaultField<ept id="p2">**</ept> and <bpt id="p3">**</bpt>getDefaultDependencies<ept id="p3">**</ept> to provide defaults.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DataEntity.DefaultRow: DataEntity.DefaultRow<ept id="p1">**</ept> は、<bpt id="p2">**</bpt>defaultField<ept id="p2">**</ept> および <bpt id="p3">**</bpt>getDefaultDependencies<ept id="p3">**</ept> と組み合わせて使用され、既定値を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>It isn't called automatically by X++ or the form engine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ またはフォーム エンジンによって自動的に呼び出されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source><bpt id="p1">**</bpt>Table.DefaultRow: Table.DefaultRow<ept id="p1">**</ept> is called automatically for each data source after mapping is completed, and before the insert and validation on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Table.DefaultRow: Table.DefaultRow<ept id="p1">**</ept> は、データソースの挿入と検証の前に、マッピングが完了した後データソースに対して自動的に呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Captureb<ept id="p1">](./media/captureb.png)](./media/captureb.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Captureb<ept id="p1">](./media/captureb.png)](./media/captureb.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Unmapped fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マップされていないフィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>A data entity can have <bpt id="p1">*</bpt>unmapped<ept id="p1">*</ept> fields in addition those fields that are directly mapped to fields of the data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティは、データ ソースのフィールドに直接マップされているフィールドに<bpt id="p1">*</bpt>マップされていない<ept id="p1">*</ept>フィールドを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>There are two mechanisms for generating values for unmapped fields:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マップされていないフィールドの値を生成するメカニズムは 2 つあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Custom X++ code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム X++ コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>SQL that is run by Microsoft SQL Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server によって実行される SQL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>The two types of unmapped fields are <bpt id="p1">*</bpt>virtual<ept id="p1">*</ept> and <bpt id="p2">*</bpt>computed<ept id="p2">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マップされていない2種類のフィールドは、<bpt id="p1">*</bpt>仮想<ept id="p1">*</ept> と <bpt id="p2">*</bpt>計算<ept id="p2">*</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Unmapped fields always support read actions, but the feature specification might not require any development effort to support write actions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マップされていないフィールドは常に読み取り操作をサポートしますが、機能仕様では、書き込み操作をサポートするための開発作業は必要とされない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Virtual field<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>仮想フィールド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>A non-persisted field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保持されないフィールド。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Controlled by custom X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム X++ コードによって制御されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Read and writes occur through custom X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">読み取り/書き込みは、カスタム X++ コードを通じて発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Typically used for intake values that are calculated by using X++ code and can't be replaced by computed columns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常は X++ コードを用いて計算される入力値に使用され、計算された列によって置き換わることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Computed field<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>計算フィールド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>The value is generated by an SQL view computed column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値は、SQL ビューの計算列によって生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>During reads, data is computed by SQL and fetched directly from the view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">読み取り中に、データは SQL によって計算され、ビューから直接フェッチされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For writes, custom X++ code must parse the input value and then write the parsed values to the regular fields of the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">書き込みについては、カスタム X++ コードは入力値を解析し、データ エンティティの通常のフィールドに解析された値を書き込む必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The values are stored in the regular fields of the data sources of the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値はエンティティのデータ ソースの通常のフィールドに格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Used mostly for reads.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの場合の読み取りに使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>It's a good idea to use computed columns instead of virtual fields whenever you can, because computed columns are computed at the SQL Server level, whereas virtual fields are computed row by row in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計算された列は SQL Server レベルで計算されている一方、仮想フィールドは、X++ の行ごとに計算された行であるため、可能な限り仮想フィールドではなく計算された列を使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Properties of unmapped fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マップされていないフィールドのプロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Category</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">種類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Default value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Behavior</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">動作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>IsComputedField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IsComputedField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>NoYes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NoYes</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Yes:<ept id="p1">&lt;/strong&gt;</ept> The field is synchronized as a SQL view computed column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>はい:<ept id="p1">&lt;/strong&gt;</ept> フィールドは、SQL ビューの計算済み列として同期されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>An X++ method is required to compute the SQL definition string for the column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ メソッドは列の SQL 定義文字列を計算する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>The virtual column definition is static and is used when the entity is synchronized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想列の定義は静的であり、エンティティが同期されているときに使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>After that, the X++ method isn't called at run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後は、X++ メソッドは、実行時に呼び出されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source><bpt id="p1">&lt;strong&gt;</bpt>No:<ept id="p1">&lt;/strong&gt;</ept> The field is a true virtual field, where inbound and outbound values are fully controlled through custom code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>いいえ:<ept id="p1">&lt;/strong&gt;</ept> フィールドは、入庫および出荷の値がカスタム コードによって完全に制御される真の仮想フィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>ComputedFieldMethod</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ComputedFieldMethod</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>String</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>A static <bpt id="p1">&lt;strong&gt;</bpt>DataEntity<ept id="p1">&lt;/strong&gt;</ept> method in X++ is used to build the SQL expression that generates the field definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の静的 <bpt id="p1">&lt;strong&gt;</bpt>DataEntity<ept id="p1">&lt;/strong&gt;</ept> メソッドは、フィールド定義を生成する SQL 式の構築に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>This property is disabled and irrelevant if the <bpt id="p1">&lt;strong&gt;</bpt>IsComputedField<ept id="p1">&lt;/strong&gt;</ept> property is set to <bpt id="p2">&lt;strong&gt;</bpt>No<ept id="p2">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>IsComputedField<ept id="p1">&lt;/strong&gt;</ept> プロパティが <bpt id="p2">&lt;strong&gt;</bpt>いいえ<ept id="p2">&lt;/strong&gt;</ept> に設定されている場合、このプロパティは無効で無関係です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The method is required if the <bpt id="p1">&lt;strong&gt;</bpt>IsComputedField<ept id="p1">&lt;/strong&gt;</ept> property is set to <bpt id="p2">&lt;strong&gt;</bpt>Yes<ept id="p2">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、<bpt id="p1">&lt;strong&gt;</bpt>IsComputedField<ept id="p1">&lt;/strong&gt;</ept> プロパティが <bpt id="p2">&lt;strong&gt;</bpt>はい<ept id="p2">&lt;/strong&gt;</ept> に設定されている場合に必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>ExtendedDataType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ExtendedDataType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>String</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Unmapped field comparison</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マップされていないフィールドの比較</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Virtual field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Computed field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計算フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Metadata properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータのプロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Is computed = No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">No と算出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Is Computed = Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計算済み = はいとなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Computed Field Method = static method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計算フィールド メソッド = 静的メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Read</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既読</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>X++ (override <bpt id="p1">&lt;strong&gt;</bpt>postLoad<ept id="p1">&lt;/strong&gt;</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ (override <bpt id="p1">&lt;strong&gt;</bpt>postLoad<ept id="p1">&lt;/strong&gt;</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Row by row</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 行ずつ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>SQL computed column</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL 計算列</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Set-based read possible</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セット ベースの読み取り可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Write</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>X++ (override <bpt id="p1">&lt;strong&gt;</bpt>mapEntityToDataSource<ept id="p1">&lt;/strong&gt;</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ (override <bpt id="p1">&lt;strong&gt;</bpt>mapEntityToDataSource<ept id="p1">&lt;/strong&gt;</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>X++ (override <bpt id="p1">&lt;strong&gt;</bpt>mapEntityToDataSource<ept id="p1">&lt;/strong&gt;</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ (override <bpt id="p1">&lt;strong&gt;</bpt>mapEntityToDataSource<ept id="p1">&lt;/strong&gt;</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Advantages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メリット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Unbound to the schema, keeps the public contract the same, but the implementation can change</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スキーマにバインドされていないため公開契約は同じですが、実装が変更される可能性があります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Call X++ methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ メソッドの呼び出し</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Faster reads, large export can occur directly from the view</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高速読み込みで、大きなエクスポートはビューから直接発生が可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>The following table provides a computed example if a <bpt id="p1">**</bpt>UnitOfMeasure<ept id="p1">**</ept> relationship exists, and displays that in an unmapped field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、<bpt id="p1">**</bpt>UnitOfMeasure<ept id="p1">**</ept> のリレーションシップが存在する場合の計算例を示し、マップされていないフィールドにその値を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Virtual field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Computed field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計算フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>On postLoad()<bpt id="p1">*</bpt>//Check to see if record exists in UnitOfMeasureInternalCode.UnitOfMeasure//Set hasFixedInternalCode value based on the field<ept id="p1">*</ept>if(this.UnitOfMeasure)this.HasFixedInternalCodeVirtual = NoYes::Yes; else this.HasFixedInternalCodeVirtual = NoYes::No;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">postLoad() で、<bpt id="p1">*</bpt>// UnitOfMeasureInternalCode.UnitOfMeasure//Set hasFixedInternalCode 値に、フィールドに基づいてレコードが存在するかどうかを確認します<ept id="p1">*</ept> (this.UnitOfMeasure)this.HasFixedInternalCodeVirtual = NoYes::Yes; else this.HasFixedInternalCodeVirtual = NoYes::No; の場合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>On computedFieldMethod()<bpt id="p1">*</bpt>//Desired SQL computed column statement(CASE WHEN T2.RECID IS NULL THEN 0 ELSE 1 END) AS INT)<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ComputedFieldMethod() で <bpt id="p1">*</bpt>// 任意の SQL 計算された列の明細書 (T2.RECID が NULL の場合は 0 ELSE 1)INTとして)<ept id="p1">*</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
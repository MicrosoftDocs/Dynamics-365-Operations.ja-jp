<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="create-tables.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>create-tables.e7f262.36ff012c58152eb3b29a346269f7f5daa1d00b8f.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>36ff012c58152eb3b29a346269f7f5daa1d00b8f</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\ax-2012\create-tables.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Create tables by using the Application Object Tree (AOT)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション オブジェクト ツリー (AOT) を使用してテーブルを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to use the Application Object Tree (AOT) to create tables in which to store data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、アプリケーション オブジェクト ツリー (AOT) を使用してデータを格納するテーブルを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Create tables by using the Application Object Tree (AOT)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション オブジェクト ツリー (AOT) を使用してテーブルを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Create tables to store data in by using the Application Object Tree (AOT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション オブジェクト ツリー (AOT) を使用してデータを格納するテーブルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メモ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Before creating new tables, review the tables that ship with Microsoft Dynamics AX to determine whether you can use existing tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいテーブルを作成する前に、Microsoft Dynamics AX に付属のテーブルを確認して既存のテーブルを使用できるかどうかを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>For more information, see <bpt id="p1">[</bpt>Application Tables<ept id="p1">](http://msdn.microsoft.com/library/a905f039-ef71-4c61-8f3f-71dadf27b09e(AX.60).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>アプリケーション テーブル<ept id="p1">](http://msdn.microsoft.com/library/a905f039-ef71-4c61-8f3f-71dadf27b09e(AX.60).aspx)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Table fields are based on a primitive data type or an extended data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル フィールドは、プリミティブ データ型または拡張データ型に基づいています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For more information, see <bpt id="p1">[</bpt>Primitive Data Types<ept id="p1">](http://msdn.microsoft.com/library/29e7d464-b72d-4a86-a982-12f9e90e704e(AX.60).aspx)</ept> and <bpt id="p2">[</bpt>How to: Create an Extended Data Type<ept id="p2">](http://msdn.microsoft.com/library/6292481f-1d73-46e9-8b46-18ab7de9a71d(AX.60).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>プリミティブ データ型<ept id="p1">](http://msdn.microsoft.com/library/29e7d464-b72d-4a86-a982-12f9e90e704e(AX.60).aspx)</ept> および <bpt id="p2">[</bpt>方法: 拡張データ型の作成<ept id="p2">](http://msdn.microsoft.com/library/6292481f-1d73-46e9-8b46-18ab7de9a71d(AX.60).aspx)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The AutoReport and AutoLookup groups are automatically created when you create a table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AutoReport および AutoLookup グループは、テーブルを作成するときに自動的に作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For more information, see <bpt id="p1">[</bpt>Implementing Automatic Reports for Forms<ept id="p1">](http://msdn.microsoft.com/library/86ee1f62-8325-4bcb-a884-a5ae521355c8(AX.60).aspx)</ept> and <bpt id="p2">[</bpt>How to: Add a Control with a Lookup Form<ept id="p2">](http://msdn.microsoft.com/library/2e365e4b-842a-44eb-b0fa-6fa4c8c1e0fe(AX.60).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>フォームの自動レポートの実装<ept id="p1">](http://msdn.microsoft.com/library/86ee1f62-8325-4bcb-a884-a5ae521355c8(AX.60).aspx)</ept> および <bpt id="p2">[</bpt>方法: ルックアップ フォームでコントロールの追加<ept id="p2">](http://msdn.microsoft.com/library/2e365e4b-842a-44eb-b0fa-6fa4c8c1e0fe(AX.60).aspx)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To manage changes to AOT objects, a version control system is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT オブジェクトの変更を管理するために、バージョン管理システムが利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For more information, see <bpt id="p1">[</bpt>Version Control System<ept id="p1">](http://msdn.microsoft.com/library/522708f8-80a0-4bfd-9634-b7cb868d1874(AX.60).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>バージョン管理システム<ept id="p1">](http://msdn.microsoft.com/library/522708f8-80a0-4bfd-9634-b7cb868d1874(AX.60).aspx)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Create a Table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In the AOT, expand the <bpt id="p1">**</bpt>Data Dictionary<ept id="p1">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT で、<bpt id="p1">**</bpt>データ ディクショナリ<ept id="p1">**</ept> ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Right-click the <bpt id="p1">**</bpt>Tables<ept id="p1">**</ept> node, and then select <bpt id="p2">**</bpt>New Table<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル<ept id="p1">**</ept> ノードを右クリックし、<bpt id="p2">**</bpt>新しいテーブル<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Right-click the table, and then click <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルを右クリックし、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Rename the table by modifying the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Name<ept id="p1">**</ept> プロパティを変更することにより、テーブルの名前を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>To specify the table as temporary, set the <bpt id="p1">**</bpt>Temporary<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルを一時的に指定するには、<bpt id="p1">**</bpt>一時的な<ept id="p1">**</ept> プロパティを <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For more information, see <bpt id="p1">[</bpt>Table Properties<ept id="p1">](table-properties.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>テーブル プロパティ<ept id="p1">](table-properties.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Modify additional table properties, as needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、追加のテーブル プロパティを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>For more information, see <bpt id="p1">[</bpt>Table Properties<ept id="p1">](table-properties.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>テーブル プロパティ<ept id="p1">](table-properties.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>To delete the table, right-click it, and then click <bpt id="p1">**</bpt>Delete<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルを削除するには、それを右クリックし、<bpt id="p1">**</bpt>削除<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Add Fields to a Table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルにフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メモ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>You can delete only fields that do not contain data in any of the table records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル レコードのどこにもデータを含まないフィールドのみを削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>You cannot modify the data type of an existing field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のフィールドのデータ型を変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Right-click the <bpt id="p1">**</bpt>Fields<ept id="p1">**</ept> node of your table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの <bpt id="p1">**</bpt>フィールド<ept id="p1">**</ept> ノードを右クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Click <bpt id="p1">**</bpt>New<ept id="p1">**</ept>, and then choose a primitive data type to base your field on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept>をクリックし、フィールドの基になるプリミティブ データ型を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If you plan to base the field on a specific extended data type, you must choose a primitive data type that the extended data type is based on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の拡張データ型のフィールドを基準に計画する場合は、拡張データ型の基準となるプリミティブ データ タイプを選択する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>To base the field on an extended data type, set the <bpt id="p1">**</bpt>ExtendedDataType<ept id="p1">**</ept> property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型に基づいてフィールドを設定するには、<bpt id="p1">**</bpt>ExtendedDataType<ept id="p1">**</ept> プロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Modify additional field properties, as needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、追加のフィールド プロパティを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>For more information, see <bpt id="p1">[</bpt>Table Field Properties<ept id="p1">](table-properties.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>テーブル フィールド プロパティ<ept id="p1">](table-properties.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To delete the field, right-click it, and then click <bpt id="p1">**</bpt>Delete<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドを削除するには、フィールドを右クリックし、<bpt id="p1">**</bpt>削除<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Restart the AOS after Adding Fields to Tables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドをテーブルに追加した後、AOS を再起動</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>When you insert data in a table during development, the SQL statement you use to insert the data is cached in the AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発時にテーブルにデータを挿入するとき、データの挿入に使用する SQL ステートメントは AOS でキャッシュされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Next you might add a new field to the table and persist the change to the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、テーブルに新しいフィールドを追加して、データベースへの変更を保持する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>This causes the SQL statement in the cache to become stale, because the statement is not updated to include the new field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、新しいフィールドを含むようにステートメントが更新されないため、キャッシュ内の SQL ステートメントが無効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>If you reuse the stale statement, the new field is ignored, or an error might occur.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">古いステートメントを再利用すると、新しいフィールドは無視されるか、エラーが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>To avoid this problem, restart the AOS after you persist table schema changes to the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を回避するには、スキーマ変更をデータベースに保持した後で AOS を再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The cache is empty when the AOS restarts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS が再起動すると、キャッシュは空になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">[</bpt>Use the Table Browser to View, Add, Modify, or Delete Records<ept id="p1">](http://msdn.microsoft.com/library/89402b55-02ea-40bc-ad0e-0774b1655426(AX.60).aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>テーブル ブラウザを使用して、表示、追加、変更、またはレコードを削除する<ept id="p1">](http://msdn.microsoft.com/library/89402b55-02ea-40bc-ad0e-0774b1655426(AX.60).aspx)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">[</bpt>How to: Add a Relation to a Table<ept id="p1">](http://msdn.microsoft.com/library/1b164b99-de08-4557-8da5-1931d9469ca1(AX.60).aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>方法: テーブルへのリレーションの追加<ept id="p1">](http://msdn.microsoft.com/library/1b164b99-de08-4557-8da5-1931d9469ca1(AX.60).aspx)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">[</bpt>How to: Create an Index<ept id="p1">](http://msdn.microsoft.com/library/5c412c46-724b-4498-ab42-51725f15c71a(AX.60).aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>方法: インデックスを作成する<ept id="p1">](http://msdn.microsoft.com/library/5c412c46-724b-4498-ab42-51725f15c71a(AX.60).aspx)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">[</bpt>Tables, Views, and Maps<ept id="p1">](http://msdn.microsoft.com/library/9c62bde0-46a1-4b48-87b2-778a68627cd1(AX.60).aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>テーブル、ビュー、およびマップ<ept id="p1">](http://msdn.microsoft.com/library/9c62bde0-46a1-4b48-87b2-778a68627cd1(AX.60).aspx)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="channel-db-extensions.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>channel-db-extensions.23b99a.ac3b987438503e57425eba26933c2d39ed3ea608.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>ac3b987438503e57425eba26933c2d39ed3ea608</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\channel-db-extensions.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Channel database extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベース 拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to extend the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、チャネル データベースを拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Channel database extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベース 拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>The channel database (channel DB) holds transactional and master data from one or more retail channels, such as an online store or a brick-and-mortar store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベース (チャネル DB) は、オンライン ストアまたはブリックアンドモルタル ストアなどの 1 つまたは複数の小売チャネルからのトランザクションおよびマスターデータを保持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The master data is pushed down from the Retail Headquarters (Retail HQ) to the channel database using the commerce data exchange (CDX).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange (CDX) を使用して、マスター データは <ph id="2">Retail Headquarters</ph> (Retail HQ) からチャネル データベースにプッシュされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The transactional data stored in the channel database is pulled back to the headquarters using the CDX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベースに格納されたトランザクション データは、CDX を使用して本社に引き戻されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In this topic we explain how to extend the channel database for different scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、さまざまなシナリオのチャネル データベースを拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The steps here apply only to Dynamics 365 for Retail, Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の手順は、Dynamics 365 for Retail、Dynamics 365 for Finance and Operations にのみ適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Before discussing the different scenarios for extension, it's important to understand the recent enhancements to channel DB extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能のさまざまなシナリオを説明する前に、チャネル DB 拡張機能の最新の機能拡張を理解することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>We have made some improvements to how extensions are handled during an upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード時の拡張機能の処理の方法にいくつかの改善を加えました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>We recommend using one of the following environment configurations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の環境構成のいずれかを使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with application update 5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) およびアプリケーション更新プログラム 5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Microsoft Dynamics 365 for Retail 7.2 with application update 5, which will be available soon.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Retail 7.2 およびアプリケーション更新プログラム 5 (まもなく利用できます)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Microsoft Dynamics 365 for Retail 7.3, which includes application update 5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Retail 7.3 (アプリケーション更新プログラム 5 を含みます)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Microsoft Dynamics 365 for Finance and Operations 7.3, which includes application update 5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations 7.3 (アプリケーション更新プログラム 5 を含みます)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Ext Schema</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ext スキーマ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In Dynamics 365 for Retail and Dynamics 365 Finance and Operations we introduced a new schema called the <bpt id="p1">**</bpt>ext schema<ept id="p1">**</ept> to support extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retail および Dynamics 365 Finance and Operations では、<bpt id="p1">**</bpt>ext スキーマ<ept id="p1">**</ept>と呼ばれる新しいスキーマを導入して拡張機能をサポートしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>In previous versions, if you wanted to add an extension to channel DB, you would add it to the CRT or AX schema.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前のバージョンでは、チャネル DB に拡張機能を追加する場合、CRT または AX スキーマに追加していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In Dynamics 365 for Retail and Dynamics 365 for Finance and Operations version you cannot change the CRT, AX, or DBO schemas.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retail および Dynamics 365 for Finance and Operations バージョンでは、CRT、AX、または DBO スキーマを変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>All changes must be made in the <bpt id="p1">**</bpt>ext schema<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての変更は <bpt id="p1">**</bpt>ext スキーマ<ept id="p1">**</ept>で行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>If you modify anything in the CRT or AX schemas, then deployment in Lifecycle Services will fail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT または AX スキーマのなにかを変更した場合、Lifecycle Services での展開に失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The error reports that don’t have permission to modify the CRT, AX, and DBO schemas.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT、AX、および DBO スキーマを変更する権限がありませんというエラーが報告されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Best practices for channel DB extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル DB 拡張機能のためのベスト プラクティス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Don’t modify anything in the CRT, AX, or DBO schemas.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT、AX、または DBO スキーマのいずれも変更しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Use the <bpt id="p1">**</bpt>ext schema<ept id="p1">**</ept> for all extension scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての拡張シナリオで <bpt id="p1">**</bpt>ext スキーマ<ept id="p1">**</ept>を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Don’t access any CRT, AX, or DBO objects in the <bpt id="p1">**</bpt>ext schema<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ext schema<ept id="p1">**</ept> 内で、CRT、AX、または DBO オブジェクトにアクセスしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>You must use the commerce runtime data service to access any channel DB artifacts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意のチャネル データベース コンポーネントにアクセスするには、商取引ランタイム データ サービスを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Don't do this</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようにしない</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The following is an example of what you should not do.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下はユーザーがしてはいけないことの例です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Instead, you should use the CRT data service to get the primary key value and then use the primary key to insert into your extension table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、主キーの値を取得するために CRT データ サービスを使用してから、拡張テーブルに挿入するために主キーの値を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Don't do this</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようにしない</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If you are creating extension table or new table all should be done in ext schema.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張テーブルまたは新しいテーブルを作成する場合、すべてを ext スキーマで行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Don’t modify any views, procedures, functions or any of the database artifacts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビュー、手順、関数、またはデータベースのコンポーネントを変更しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Don’t access or call any of any database artifacts including views, defined types, functions and procedures from your extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子からのビュー、定義されたタイプ、関数および手順を含むデータベースのコンポーネントにアクセスしたり、呼び出したりしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To access the database artifacts, use the CRT data service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのアーティファクトにアクセスするには、CRT データ サービスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>For example, suppose you want to extend the product search view to search some custom fields or to show custom columns in journal views.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、一部のカスタム フィールドを検索する、または仕訳帳のビューにカスタム列を表示する製品検索ビューを拡張するとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Don’t modify the views or procedures or functions in SQL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL 内では、ビューまたは手順、機能を変更しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Instead, use the CRT data service and do the extension either by overriding or using post triggers and then call your extended procedures.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、CRT データ サービスを使用して、投稿トリガーをオーバーライドまたは使用することによって拡張機能を実行し、拡張プロシージャを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Adding extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>All the extension tables should have grant permission on <bpt id="p1">**</bpt>UserRole<ept id="p1">**</ept> and <bpt id="p2">**</bpt>DeployExtensibilityRole<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての拡張機能テーブルは <bpt id="p1">**</bpt>UserRole<ept id="p1">**</ept> および <bpt id="p2">**</bpt>DeployExtensibilityRole<ept id="p2">**</ept> にアクセス許可を付与する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Grant <bpt id="p1">**</bpt>DataSyncUsersRole<ept id="p1">**</ept> permission if your table is going to send receive data from HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルが HQ から受信するデータを送信する場合、<bpt id="p1">**</bpt>DataSyncUsersRole<ept id="p1">**</ept> アクセス許可を付与します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>If you are creating extended table and want to sync the data back to HQ, then have the primary column of the parent table in the extended table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張テーブルを作成し、HQ にデータを同期させる場合は、拡張テーブルに親テーブルの主な列を含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Always prefix your table, for example, <bpt id="p1">**</bpt>ContosoRetailTransactionTable<ept id="p1">**</ept>, so that you can avoid conflicts with other partner/ISV customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>ContosoRetailTransactionTable<ept id="p1">**</ept> など、常にテーブルに接頭語を付けると、他のパートナー/ISV カスタマイズとの競合を回避できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Attributes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>We extended the attribute framework in HQ to support attributes for Customers, Customer orders, cash and carry transactions and call center orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客、顧客の注文、現金売りトランザクション、およびコール センター注文の属性をサポートするために、HQ の属性フレームワークを拡張しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Customer attributes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客属性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>With the new customer attribute framework, you can use configurations to add new fields to the customer add/edit or customer details screens in POS or HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい顧客属性フレームワークでは、構成を使用して、POS または HQ 内の顧客追加/編集画面または顧客詳細画面に新しいフィールドを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>After configuring the customer attribute group in retail parameters, POS and HQ will automatically show up the new attribute without any code change or customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売パラメーターで顧客属性グループを構成した後、POS や HQ はコードの変更やカスタマイズを行わずに新しい属性を自動的に表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The screen layout designer will also be configured to show the customer attributes in the transaction screen - <bpt id="p1">**</bpt>Customer<ept id="p1">**</ept> panel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画面レイアウト設計者は、取引画面 (<bpt id="p1">**</bpt>顧客<ept id="p1">**</ept> パネル) に顧客属性を表示するようにも設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Order attributes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注文属性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The attribute framework was extended to support attributes in cash and carry transactions, customer orders, and call center orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性フレームワークは、現金売りトランザクション、顧客の注文、およびコール センター注文の属性をサポートするように拡張されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>You can edit and set values directly in HQ or in CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HQ または CRT で値を直接編集して設定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>All this can be done through configurations, without any database changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらすべてはデータベースを変更せずにコンフィギュレーションを介して実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>(You can customization the attribute values for core business logic, not required for basic CRUD operations.) Previously, you had to create new tables in HQ and channel DB, and then modify CRT to do this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(基本的な CRUD 操作は必要ではなく、主要なビジネス ロジックの属性値をカスタマイズすることができます。) 以前は、これを行うには、HQ とチャンネル DB に新しいテーブルを作成し、CRT を変更する必要がありました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Now all the attribute creation can be done through configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在は、すべての属性の作成をコンフィギュレーションを通じて実行できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Adding a new table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいテーブルの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>In this scenario we will explain how to create a new table and add it to the channel DB.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオでは、新しいテーブルを作成し、チャネル DB に追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>All extension code has access to the <bpt id="p1">**</bpt>ext schema<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての拡張コードは <bpt id="p1">**</bpt>ext スキーマ<ept id="p1">**</ept>へアクセスすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Create a new table in the channel database in the <bpt id="p1">**</bpt>ext schema<ept id="p1">**</ept> either using SQL Server Management Studio Designer or using SQL scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Management Studio デザイナーを使用するか、SQL スクリプトを使用して、<bpt id="p1">**</bpt>ext スキーマ<ept id="p1">**</ept>のチャネル データベースに新しいテーブルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>The following is an example SQL script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下は、SQL スクリプトの例です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Adding new views, stored procedure, functions, and defined types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいビュー、ストアド プロシージャ、関数、定義済タイプの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>All new stored procedures, views or functions must be created in the <bpt id="p1">**</bpt>ext schema<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての新しいストアド プロシージャ、ビューまたは機能は <bpt id="p1">**</bpt>ext スキーマ<ept id="p1">**</ept>に作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Don't access or call our database artifacts from your procedures, views, or functions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順、ビューまたは機能から、データベース コンポーネントをアクセスするまたは呼びだすことはやめてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Deployment checks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置のチェック</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The deployment process determines if there are any modification to the database artifacts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置プロセスは、データベースのコンポーネントに変更があるかどうかを判断します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>If you have attempted to modify the CRT, AX, or DBO schema objects, or access them for any scenario directly in SQL, then deployment will fail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT、AX、または DBO スキーマ オブジェクトを変更しようとした場合、またはどのシナリオの場合でも SQL でそれらに直接アクセスすると、展開は失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Extension scripts and deployment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張スクリプトおよび展開</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Channel Database extensions are provided by authoring one or more T-SQL script files and including them in a <bpt id="p1">[</bpt>deployable package<ept id="p1">](./retail-sdk/retail-sdk-packaging.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャンネル データベース拡張は、1 つまたは複数の T-SQL スクリプト ファイルを作成し、<bpt id="p1">[</bpt>展開可能なパッケージ<ept id="p1">](./retail-sdk/retail-sdk-packaging.md)</ept>に含めることで用意されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>This process is described in the <bpt id="p1">[</bpt>Retail SDK<ept id="p1">](./retail-sdk/retail-sdk-overview.md)</ept> documentation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスについては、<bpt id="p1">[</bpt>Retail SDK<ept id="p1">](./retail-sdk/retail-sdk-overview.md)</ept> ドキュメントで説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Extension script files must be written using <bpt id="p1">[</bpt>T-SQL<ept id="p1">](https://docs.microsoft.com/en-us/sql/t-sql/language-reference)</ept> and compatible with <bpt id="p2">[</bpt>Azure SQL Database<ept id="p2">](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-features)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張スクリプト ファイルは、<bpt id="p1">[</bpt>T-SQL<ept id="p1">](https://docs.microsoft.com/en-us/sql/t-sql/language-reference)</ept> を使用して記述され、<bpt id="p2">[</bpt>Azure SQL データベース<ept id="p2">](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-features)</ept>と互換性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>The script files must end with the <bpt id="p1">*</bpt>.sql<ept id="p1">*</ept> file extension, any other files will be ignored or may induce a packaging or deployment failure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプト ファイルの末尾は <bpt id="p1">*</bpt>.sql<ept id="p1">*</ept> ファイル拡張子にする必要があります。その他のファイルは無視されます。または、パッケージングまたは配置障害を引き起こす可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>If you intend to deploy your Channel Database extensions as part of Retail Store Scale Unit or Modern POS offline, the scripts must also be compatible with the version of SQL Express and/or SQL Server that will be used for those components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit または Modern POS の一部としてオフラインでチャネル データベース拡張機能を展開する場合、スクリプトは、それらのコンポーネントに対して使用される SQL Express または SQL Server のバージョンの両方またはいずれかと互換性があることも必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>During deployment and installation, the extension scripts are executed in alphabetical order based on the script file name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置とインストール中、拡張子スクリプトは、スクリプト ファイル名に基づいたアルファベット順で実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Each script is run to completion and then a metadata record is added to the Channel Database's CRT.RETAILUPGRADEHISTORY table to track the completion of that extension script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各スクリプトは、完了するまで実行され、拡張スクリプトの完了を追跡するため、メタデータ レコードはチャンネル データベースの CRT.RETAILUPGRADEHISTORY テーブルに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>The script will not be executed again for the same Channel Database in subsequent deployments if that metadata record is present.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのメタデータ レコードが存在する場合、その後の展開で同じチャネル データベースに対してスクリプトが再度実行されることはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>If a script fails during execution and does not complete successfully, its metadata will not be stored and the script will be rerun on subsequent deployments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトが実行中に失敗し、正常に完了しない場合、そのメタデータは保存されず、以降の配置でスクリプトが再実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If the deployment or installation is combined with an update of the product, the extension scripts are run after the product update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開やインストールが製品の更新と組み合わされている場合、拡張スクリプトは製品の更新後に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>To author a successful Channel Database extension, you must adhere to the following guidelines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正常に行われるチャネル データベース拡張を作成するには、次のガイドラインに従う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Use a naming convention that ensures stable order when sorted alphabetically</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アルファベット順に並べ替えられたときに、安定した順序が確保される名前付け規則を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Because extension scripts are executed in alphabetical order based on the file name, you should establish a naming convention that ensures that the correct execution order is used when sorted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張スクリプトは、ファイル名に基づくアルファベット順に実行されるので、並べ替えたときに正しい実行順序が使用される名前付け規則を確立する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>One example would be naming files with the following pattern: "&lt;ISO 8601 date&gt;_<ph id="ph1">&lt;descriptio&gt;</ph>.sql", where <bpt id="p1">**</bpt>&lt;ISO 8601 date&gt;<ept id="p1">**</ept> is a ISO 8601 formatted date and <bpt id="p2">**</bpt><ph id="ph2">&lt;description&gt;</ph><ept id="p2">**</ept> is descriptive text to identify the purpose of the script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つの例は、次のパターンを持つファイルの名前付けです: "&lt;ISO 8601 date&gt;_<ph id="ph1">&lt;descriptio&gt;</ph>.sql"。ここで <bpt id="p1">**</bpt>&lt;ISO 8601 date&gt;<ept id="p1">**</ept> は ISO 8601 形式の日付で、<bpt id="p2">**</bpt><ph id="ph2">&lt;description&gt;</ph><ept id="p2">**</ept> はスクリプトの目的を識別するための説明のテキストです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>For instance, <bpt id="p1">*</bpt>"20180501_CustomerDetails.sql"<ept id="p1">*</ept> and <bpt id="p2">*</bpt>"20181102_CustomerDetailsIndex.sql"<ept id="p2">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">*</bpt>"20180501_CustomerDetails.sql"<ept id="p1">*</ept> と <bpt id="p2">*</bpt>"20181102_CustomerDetailsIndex.sql"<ept id="p2">*</ept> などです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>The former would represent an extension script authored on May 1, 2018 that is related to "Customer Details" feature and the latter an extension script associated to indexes related to the previous feature authored on November 2, 2018.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前者は、「顧客の詳細」機能に関連する 2018 年 5 月 1 日に作成された拡張スクリプトを表しており、後者は、2018 年 11 月 2 日に作成された以前の機能に関連するインデックスに関連付けられている拡張スクリプトです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Another simpler alternative is to use an incremental numeric prefix, such as "0001_CustomerDetails.sql" and "0002_CustomerDetailsIndex.sql".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別の単純な方法は、"0001_CustomerDetails.sql" や "0002_CustomerDetailsIndex.sql" などの差分数値接頭語を使用する方法です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>If one script depends on another having executed successfully, you must name then in a way that ensures that the file name in alphabetical order matches the required execution order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのスクリプトが正常に実行される別のスクリプトに依存している場合、アルファベット順のファイル名が必要な実行順序と一致していることを確認する方法で命名する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Do not alter extension scripts that have been published</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発行された拡張スクリプトを変更しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>If you have released a deployable package or installer extension that contains Channel Database extension scripts, do not alter those scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開可能なパッケージまたはチャンル データベース拡張スクリプトを含むインストーラー拡張をリリースした場合、それらのスクリプトを変更しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Extension scripts are run only once per Channel Database instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張スクリプトは、チャネル データベース インスタンスあたり 1 回だけ実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>If you alter published scripts and those scripts may have already been run against a Channel Database, the modifications to an already executed script will not be applied to the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既にスクリプトを発行しており、それらのスクリプトがチャネル データベースに対して実行済の場合、既に実行されたスクリプトへの変更はデータベースには適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Instead, provide the modifications in a new script file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、新しいスクリプト ファイル内の変更を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Consider the naming convention noted above to ensure that it runs after its dependencies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">依存関係の後に実行されるように、上記の名前付け規則を検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Do not remove old extension scripts that have been published</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発行された以前の拡張スクリプトを削除しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Your deployable package or installer extension must represent a cumulative update for your database extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開可能なパッケージまたはインストーラー拡張機能は、データベースの拡張機能の累積的な更新を表す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>There should be no dependencies on previous versions of an extension package or installer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能パッケージまたはインストーラーの以前のバージョンには依存関係はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>A customer should be able to apply your extension package or installer without depending on a previous version of your package or extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは、パッケージまたは拡張機能の以前のバージョンに依存しなくても拡張機能パッケージやインストーラーを適用できる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>If your extension scripts have been published as part of a deployable package or installer extension, do not remove them from subsequent updates in your package or installer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張スクリプトが展開可能なパッケージまたはインストーラー拡張の一部として公開されている場合、パッケージまたはインストーラーの以降の更新から削除しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>To account for disaster recovery, upgrade and scale out scenarios, extension packages may be used to bring a new instance of the Channel Database to the same version of the last deployed extension package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">災害復旧、アップグレード、スケール アウト シナリオに対応するため、チャンル データベースの新しいインスタンスを同じバージョンの最後に配置された拡張機能パッケージに持ち込むために拡張パッケージを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Extension scripts must be idempotent and reentrant</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張スクリプトは、非べき等および再入力である必要がある</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Although extension scripts are run only once per Channel Database, scripts may fail due to authoring errors or transient SQL errors, like time outs or transaction deadlocks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張スクリプトはチャネル データベースあたり 1 回だけ実行されますが、スクリプトはオーサリング エラーまたはタイムアウトやトランザクション デッドロックなどの一時的な SQL エラーが原因で実行されない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>The extension scripts must be idempotent and reentrant to account for those failure scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張スクリプトは、それらの障害シナリオに対応するため、非べき等および再入力である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>If the extension script fails due to any error, it may be rerun.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張スクリプトがエラーが原因で失敗した場合、再実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Rerunning the script should not adversely affect the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトを再実行しても、データベースに悪影響を及ぼしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Do not assume that the Channel Database data is perennial</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベース データが永続すると仮定しない</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The Channel Database is a transactional database that provides storage support for operations performed by Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベースは、Retail サーバーで実行される操作の記憶域サポートを提供するトランザクション データベースです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>All data that is stored in the Channel Database that must be kept for long periods of time must be uploaded to the headquarters through the <bpt id="p1">[</bpt>Commerce Data Exchange<ept id="p1">](./cdx-extensibility.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">長期間保存する必要があるチャネル データベースに格納されるすべてのデータは、<bpt id="p1">[</bpt>Commerce Data Exchange<ept id="p1">](./cdx-extensibility.md)</ept> を通じて本社にアップロードする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Data uploaded to the headquarters can be accessed by the <bpt id="p1">[</bpt>Commerce Data Exchange Real-time Service<ept id="p1">](./extend-commerce-data-exchange.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">本社にアップロードされたデータには、<bpt id="p1">[</bpt>Commerce Data Exchange リアルタイム サービス<ept id="p1">](./extend-commerce-data-exchange.md)</ept>によりアクセスすることができます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
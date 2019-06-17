<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="dimension-entry-control-uptake.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>dimension-entry-control-uptake.5dbd0d.37c412a65a774b239cc23f91f3516712ddaa1b50.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>37c412a65a774b239cc23f91f3516712ddaa1b50</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\financial\dimension-entry-control-uptake.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Uptake of Dimension Entry controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールの取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>Describes the Dimension Entry control and associated Controller classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールおよび関連するコントローラー クラスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Uptake of Dimension Entry controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールの取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Describes the Dimension Entry control and associated Controller classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールおよび関連するコントローラー クラスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>General approach</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的なアプローチ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The design goal is to encapsulate the control implementation and not require the form to interact with the classes backing the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設計の目標は、コントロールの実装をカプセル化し、コントロールをサポートするクラスとやり取りするフォームを必要としないことです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In alignment with this design, <bpt id="p1">**</bpt>all forms should interact only with the Dimension Entry control instance API and not directly with the controller classes<ept id="p1">**</ept>, like LedgerDimensionEntryController, LedgerDefaultDimensionEntryController, etc. Any property that was manipulated or any method that was called on the controller would now need to be called on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この設計に合わせて、LedgerDimensionEntryController、LedgerDefaultDimensionEntryController などのように、<bpt id="p1">**</bpt>すべてのフォームは直接コントローラー クラスではなく、分析コードのエントリ コントロール インスタンス API のみと対話する必要があります<ept id="p1">**</ept>。操作されたプロパティおよびコントローラーで呼び出されたメソッドは、コントロールで呼び出される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The upgrade script only handles Dimension Entry controls constructed with the constructInGroupWithValues() and constructInTabWithValues() methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード スクリプトは、constructInGroupWithValues() メソッドおよび constructInTabWithValues() メソッドを使用して作成された分析コード エントリ コントロールのみを処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Other controls will need to be upgraded manually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のコントロールは、手動でアップグレードする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The upgrade script will not handle any Dimension Entry controls sent as parameters to helper methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード スクリプトは、ヘルパー メソッドのパラメーターとして送信された分析コード エントリ コントロールを処理しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>This code will need to be manually upgraded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードは、手動でアップグレードする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>In Dynamics AX 2012, the container for the default dimension control may have been defined as a securable control by setting ‘Needed Permission’ = Manual.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 では、既定の分析コード コントロールのコンテナーは、「必要なアクセス許可」 = 手動に設定することでセキュリティ保護可能なコントロールとして定義できました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Access to the control was granted in the security model so view and maintain access worked correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールへのアクセスは、セキュリティ モデルで付与されているため、アクセスを正しく表示および管理することができました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The default dimension control is now a design-time experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の分析コードのコントロールは、デザイン時のエクスペリエンスになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Therefore forms no longer need to define the container of the control as a securable control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、フォームでは、コントロールのコンテナーを保護可能なコントロールとして定義する必要がなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In most cases, forms that control metadata should be updated to remove the Manual setting and the references to the control in the security model need to be removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの場合、手動の設定を削除するためにメタデータを制御するフォームを更新して、セキュリティ モデルのコントロールへの参照を削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The setting can be left as Manual if it is used to maintain fine-grained security control over the Dimension Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dimension Entry コントロールに対して細かいセキュリティ制御を維持するために使用される場合、この設定は [手動] のままにすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In Dynamics AX 2012, parmAttributeSetDataSource and parmAttributeValueSetDataSource were used to set the datasource and datasource field associated with the Default Dimensions control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 では、parmAttributeSetDataSource および parmAttributeValueSetDataSource がデータ ソースと既定の分析コード コントロールに関連付けられたデータ ソースのフィールドを設定するために使用されていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Typically these were set in the init method of the form, immediately after constructing the DimensionDefaultingController instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは通常、DimensionDefaultingController インスタンスを作成した直後にフォームの init メソッドで設定されていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>All calls to parmAttributeSetDataSource and parmAttributeValueSetDataSource will be removed after upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての呼び出し parmAttributeSetDataSource および parmAttributeValueSetDataSource はアップグレード後に削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The values from these calls are used to populate metadata on the upgraded control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの呼び出しの値を使用して、アップグレードされたコントロールのメタデータを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>After upgrade the form should be checked to verify that it is working as expected after the removal of all these calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード後、これらの呼び出しをすべて削除した後、フォームが正常に機能していることを確認するために、フォームをチェックする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Dimension Entry controls are now modelled on form design.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ディメンション入力コントロールはフォーム デザインでモデル化されるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>To find a Dimension Entry control, expand the design elements or search for “DimensionEntry” on the form design.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コードの入力管理を検索するには、デザイン要素を展開するか、フォーム デザインで "DimensionEntry" を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Here is what the new control will look like at design time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイン時に新しいコントロールがどのようなものかを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>1<ept id="p1">](./media/1.png)](./media/1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>1<ept id="p1">](./media/1.png)](./media/1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The custom properties for the Dimension Entry control are found under the <bpt id="p1">**</bpt>Controller<ept id="p1">**</ept> group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールのカスタム プロパティは、<bpt id="p1">**</bpt>コントローラー<ept id="p1">**</ept> グループの下にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Capture1<ept id="p1">](./media/capture1.png)](./media/capture1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Capture1<ept id="p1">](./media/capture1.png)](./media/capture1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Details on the properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティの詳細</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Valid Values<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効な値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Usage<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>用途<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Caption Text</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャプション テキスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Any label</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのラベル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Caption for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールのキャプション。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Controller Class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>One of the 8 Controller classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">8 つのコントローラー クラスのうちの 1 つです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>For example, LedgerDefaultDimensionEntryController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、LedgerDefaultDimensionEntryController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Determines the behavior of the Dimension Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールの動作を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>More information about this property is provided below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティの詳細については以下で説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Any data source in the form data source list</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム データ ソース一覧のデータ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The data source specified here should be pointed to the table that holds the field specified in the Value Data Field property and/or the Enum Data Field property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで指定するデータソースは、値データフィールドプロパティおよび/または列挙データフィールドプロパティで指定したフィールドを保持するテーブルをポイントする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Enum Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>A field in the table referenced by the data source provided in the Data Source property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース プロパティに指定されたデータ ソースによって参照されるテーブルのフィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>This is the field that the enumeration values will be stored in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、列挙型に格納されているフィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>This property shouldn’t be specified if the control is not using an enumeration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールが列挙を使用していない場合は、このプロパティを指定しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Enumeration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Any enumeration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意の列挙。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>For example, NoYes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、NoYes</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The enumeration used by the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールで使用する列挙型です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The enumeration will be used by the control instead of Dimension values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型は、分析コード値の代わりにコントロールによって使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Value Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値 データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>A field in the table referenced by the data source provided in the Data Source property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース プロパティに指定されたデータ ソースによって参照されるテーブルのフィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This is the field that the Dimension Entry control is bound to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、分析コード エントリ コントロールがバインドされているフィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Controller class property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー クラス プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The table provided below gives details about each controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各コントローラーの詳細は、以下のテーブルを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Controller<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントローラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Details<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>詳細<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>BudgetDefaultDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BudgetDefaultDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>This controller provides budget based support for default value data entry in the Dimension Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、予算ベースでサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Budget Default Dimensions require a Main Account Dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算の既定分析コードでは、主勘定分析コードが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>PurchReqDefaultDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchReqDefaultDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>This controller provides PurchReq based support for default value data entry in the Dimension Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、PurchReq ベースでサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>PurchReq Default Dimensions require a Main Account Dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchReq の既定分析コードでは、主勘定分析コードが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>LedgerDefaultDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerDefaultDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>This controller provides ledger based support for default value data entry in the Dimension Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、元帳ベースでサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Default Dimensions require the phrase “No default” to appear in the name column of any row that doesn’t have a value specified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の分析コードでは、値が指定されていない行の名前列に「既定値なし」という語句が表示されている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>This controller is typically used with setup, master data, and header records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、通常、設定、マスター データ、およびヘッダー レコードで使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>LedgerDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>This controller provides ledger based support for data entry in the Dimension Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、分析コード エントリ コントロールのデータ入力の元帳に基づくサポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This controller is typically used with line item or transactional data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは通常、明細行品目またはトランザクション データに使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>InventSiteLockedDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteLockedDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This controller provides support for data entry in the Dimension Entry control specifically for the InventSite form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、InventSite フォーム専用の分析コード エントリ コントロールのデータ入力をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>InventSiteLinkedDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteLinkedDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>This controller provides support for data entry in the Dimension Entry control for the behavior mandated by the Inventory Dimension Link setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>This controller updates the control in a special way when the company is changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーでは、会社が変更されたときに、特別な方法で、コントロールを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>InventSiteSMAItemDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteSMAItemDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>This controller provides support for data entry in the Dimension Entry control for the behavior mandated by the Inventory Dimension Link setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>InventSiteTmpLedgerBaseLinkedDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteTmpLedgerBaseLinkedDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This controller provides support for data entry in the Dimension Entry control for the behavior mandated by the Inventory Dimension Link setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>This controller specifically works with the DefaultDimension field on the TmpLedgerBase table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、特に TmpLedgerBase テーブルの DefaultDimension フィールドで動作します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Some Dimension Entry controls might not have the controller property set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの分析コード入力コントロールには、コントローラー プロパティが設定されていない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The controller is inferred from the EDT of the control’s Value Data Field in these cases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、コントローラーはコントロールの値データ フィールドの EDT から推測されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A set of Dimension Entry control specific properties is provided below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一連の分析コード エントリ コントロールの特定のプロパティを以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>These properties are for the Dimension Entry control selected in the General Approach section above (DimensionEntryControlHeader) on the PurchTable form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのプロパティは、上記の一般的なアプローチのセクション (DimensionEntryControlHeader) で選択した、分析コード入力コントロールの PurchTable フォームのプロパティです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>This Dimension Entry control is using the DefaultDimension field on the PurchTable table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この分析コード エントリ コントロールは、PurchTableのTable テーブルの DefaultDimension フィールドを使用しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>The Extended Data Type property of the DefaultDimension field on PurchTable is set to LedgerDefaultDimensionValueSet (shown below).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchTable の DefaultDimension フィールドの拡張データ型プロパティは、LedgerDefaultDimensionValueSet (以下を参照) に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>At runtime, this EDT will be mapped to the LedgerDefaultDimensionEntryController.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時に、この EDT は LedgerDefaultDimensionEntryController にマップされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>So the DimensionEntryControlHeader control uses the LedgerDefaultDimensionEntryController in this case.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、この場合 DimensionEntryControlHeader コントロールは LedgerDefaultDimensionEntryController を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The following example shows the EDTs and the controllers they are mapped to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、EDT とそれがマップされているコントローラーを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>3<ept id="p1">](./media/3.png)](./media/3.png)</ept> <bpt id="p2">[</bpt><ph id="ph2">![</ph>4<ept id="p2">](./media/4.png)](./media/4.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>3<ept id="p1">](./media/3.png)](./media/3.png)</ept> <bpt id="p2">[</bpt><ph id="ph2">![</ph>4<ept id="p2">](./media/4.png)](./media/4.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Extended data types and the controllers they are mapped to</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型およびマップされるコントローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">**</bpt>Extended data type<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>拡張データ型<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Controller<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントローラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>BudgetDefaultDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BudgetDefaultDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>BudgetDefaultDimensionEntryController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BudgetDefaultDimensionEntryController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>PurchReqDefaultDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchReqDefaultDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>PurchReqDefaultDimensionEntryController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchReqDefaultDimensionEntryController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>LedgerDefaultDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerDefaultDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>LedgerDefaultDimensionEntryController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerDefaultDimensionEntryController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>LedgerDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>LedgerDimensionEntryController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerDimensionEntryController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>InventSiteLockedDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteLockedDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>InventSiteLockedDimensionEntryController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteLockedDimensionEntryController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>InventSiteLinkedDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteLinkedDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>InventSiteLinkedDimensionEntryController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteLinkedDimensionEntryController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>InventSiteSMAItemDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteSMAItemDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>InventSiteSMAItemDimensionEntryController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteSMAItemDimensionEntryController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>InventSiteTmpLedgerBaseLinkedDimensionValueSet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteTmpLedgerBaseLinkedDimensionValueSet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>InventSiteTmpLedgerBaseLinked-</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventSiteTmpLedgerBaseLinked-</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>DimensionEntryController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DimensionEntryController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Upgrade Script TODOs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプト TODO のアップグレード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Microsoft Dynamics 365 for Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The reactivate method refreshes the Dimension Entry control with current settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">reactivate メソッドは、分析コード エントリ コントロールを現在の設定でリフレッシュします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The method only refreshes the control if the company or displayed dimension list changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、会社または表示された分析コード リストが変更された場合にのみ、コントロールを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>This call can be removed if neither of these are changed before it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この呼び出しは、これらのどちらも以前に変更されていない場合に削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Otherwise leave the call as is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合は、呼び出しはそのままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>If parmCompany() is called immediately before reactivate(), and it is the only DEC API called before reactivate(), and the method it resides in is called during the active() of the datasource; an optimization can be manually made to improve performance and reduce code uptake:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">reactivate() の直前で parmCompany() が呼び出され、それが reactivate() より前に呼び出された唯一の DEC API であり、そのメソッドがデータソースの active() 中に呼び出された場合、最適化を手動で行うことでパフォーマンスを向上させ、コードの取り込みを減らすことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source><ph id="ph1">1)</ph> Remove the parmCompany() and reactivate() calls during the datasource active process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">1)</ph> データ ソースのアクティブ プロセス中に、parmCompany() および reactivate() 呼び出しを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source><ph id="ph1">2)</ph> In the form init(), run(), datasource init(), or similar methods called before initial user interaction with the form, add the following line of code:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">2)</ph> 最初のユーザーとフォームとのやりとりの前に呼び出されるフォーム init()、run()、datasource init()、または同様のメソッドでは、次のコード行を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This change will allow the DEC to automatically find the company field reference that is updated when the active record changes and refresh the list of dimensions accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この変更により、DEC はアクティブなレコードが変更されたときに更新される会社フィールド参照を自動的に見つけ出し、それに応じてディメンションのリストを更新できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Note:<ept id="p1">&lt;/strong&gt;</ept> This should not be combined with the use of parmDisplayedDimensionSet() otherwise the list of dimensions may not be the ones expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>注記:<ept id="p1">&lt;/strong&gt;</ept> これは、parmDisplayedDimensionSet() の使用と組み合わせないでください。そうすると、分析コードの一覧が予想外のものになることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>In all other locations, such as the modified method of a company selection field, parmCompany() must be called to immediately reflect the change in company as the datasource is not in the process of being read at that time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社の選択フィールドの変更されたメソッドなど、他のすべての場所で、データ ソースがその時点で読み取られるプロセスではないため、会社内の変更をすぐに反映するように parmCompany() を呼び出す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>If a specific editable dimension set is needed, replace this call with:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の編集可能なディメンション セットが必要な場合は、この呼び出しを次のように置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source><bpt id="p1">
&lt;strong&gt;</bpt>Note<ept id="p1">&lt;/strong&gt;</ept>: The editableDimensionSet parameter is of type DimensionEnumeration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">
&lt;strong&gt;</bpt>注記<ept id="p1">&lt;/strong&gt;</ept>: editableDimensionSet パラメーターは、タイプ DimensionEnumeration です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>If this call is made within the pageActivated method of the Dimension Entry control’s parent control or the form init method, it can be removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコールを、分析コード エントリ コントロールの親コントロールの pageActivated メソッドまたは Form Init メソッド内で実行する場合、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The intent of this method call outside the above mentioned locations isn’t clear.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の場所以外のメソッド呼び出しの意図は明確ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Remove the call and test the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">呼び出しを削除して、コントロールをテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>A TODO will be left for a call to deleted() that is not inside a data source delete method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースの削除メソッド内にはない deleted() の呼び出しのために、TODO が残されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>These calls are only expected to be in data source delete methods, and there is no replacement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの呼び出しは、データソースの削除メソッド内にのみ存在すると予想され、置換はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Try to remove the call and test the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">呼び出しを削除して、コントロールをテストしてみてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The Dimension Entry control framework will save values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロール フレームワークは、値を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Remove the call and test the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">呼び出しを削除して、コントロールをテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>To find the entity, the getEntityInstance method needs to be called from the DimensionAttributeValue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティを検索するには、getEntityInstance メソッドを DimensionAttributeValue から呼び出す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Replace this call with something similar to the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この呼び出しを次のようなものに置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Since the updateValues() method is only called with one parameter here, the call can be replaced with a call to allowEdit().</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここに 1 つのパラメーターがある場合のみ updateValues() メソッドが呼び出されるため、呼び出しは allowEdit() の呼び出しに置き換えることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Since the call to updateValues() has two parameters in this case, it needs to be replaced with a call to allowEdit() to change the editability of the control and a call to loadAttributeValueSet() to clear the control’s values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、updateValues() の呼び出しには 2 つのパラメーターがあるので、コントロールの編集機能を変更するには allowEdit() の呼び出しと置き換え、コントロールの値をクリアするには loadAttributeValueSet() の呼び出しと置き換える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">
&lt;strong&gt;</bpt>Note:<ept id="p1">&lt;/strong&gt;</ept>If the first parameter in the updateValues method call was NoYesUnchanged::Unchanged, then the new call to allowEdit is not needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">
&lt;strong&gt;</bpt>注記:<ept id="p1">&lt;/strong&gt;</ept> updateValues メソッド呼び出しの最初のパラメーターが NoYesUnchanged::Unchanged の場合、allowEdit の新しい呼び出しは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Similarly, if the second parameter in the updateValues method call was false, then the call to loadAttributeValueSet is not needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、updateValues メソッドの 2 番目のパラメーターの呼び出しが false の場合、loadAttributeValueSet への呼び出しは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">**</bpt>Methods to potentially remove<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除する可能性のあるメソッド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Any leftover methods on the datasource or tabpage/group that holds the Dimension Entry control can be removed if there is no custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールを保持するデータソースまたは tabpage/グループの残りのメソッドは、カスタム ロジックがない場合、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The following table shows examples of methods without customizations which should be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、削除する必要があるカスタマイズのないメソッドの例を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>This method will be on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはデータソースにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>It can be removed if there is no custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ロジックがない場合に削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Finance and Operations This method will be on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations この方法はデータ ソースになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>It can be removed if there is no custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ロジックがない場合に削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>This method will be on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはデータソースにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>It can be removed if there is no custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ロジックがない場合に削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>This method will be on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはデータソースにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>It can be removed if there is no custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ロジックがない場合に削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>This method will be on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはデータソースにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>It can be removed if there is no custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ロジックがない場合に削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>This method will be on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはデータソースにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>It can be removed if there is no custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ロジックがない場合に削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Finance and Operations This method will be on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations この方法はデータ ソースになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>It can be removed if there is no custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ロジックがない場合に削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Finance and Operations This method will be on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations この方法はデータ ソースになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>It can be removed if there is no custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ロジックがない場合に削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Finance and Operations This method will be on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations この方法はデータ ソースになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>It can be removed if there is no custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ロジックがない場合に削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Finance and Operations This method will be on the tabpage or group that holds the Dimension Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations この方法は、分析コード エントリ コントロールを保持する TabPage またはグループになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>If there is no custom logic, the method can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ロジックがない場合は、メソッドを削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source><bpt id="p1">**</bpt>Compile Errors<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コンパイル エラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>This section will go through how to address common compile errors that may be left behind.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、取り残される可能性のある一般的なコンパイル エラーに対処する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source><bpt id="p1">&lt;strong&gt;</bpt>On the form (PurchTable):<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>フォームで (PurchTable)。<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source><bpt id="p1">
&lt;strong&gt;</bpt>In the class (PurchTableForm):<ept id="p1">&lt;/strong&gt;</ept><ph id="ph1">
</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">
&lt;strong&gt;</bpt>クラス内 (PurchTableForm):<ept id="p1">&lt;/strong&gt;</ept><ph id="ph1">
</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source><bpt id="p1">&lt;strong&gt;</bpt>On the form (PurchTable):<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>フォームで (PurchTable)。<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source><bpt id="p1">
&lt;strong&gt;</bpt>In the class (PurchTableForm):<ept id="p1">&lt;/strong&gt;</ept><ph id="ph1">
</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">
&lt;strong&gt;</bpt>クラス内 (PurchTableForm):<ept id="p1">&lt;/strong&gt;</ept><ph id="ph1">
</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source><bpt id="p1">[</bpt>Dimension Entry control migration walkthrough<ept id="p1">](dimension-entry-control-migration.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>分析コード エントリ コントロールのチュートリアル<ept id="p1">](dimension-entry-control-migration.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source><bpt id="p1">[</bpt>Dimension Entry control dialog support<ept id="p1">](dimension-entry-control-dialog-support.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>分析コード エントリ コントロール ダイアログのサポート<ept id="p1">](dimension-entry-control-dialog-support.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
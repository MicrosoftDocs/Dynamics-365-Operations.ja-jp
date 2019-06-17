<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="tax-engine-applicability.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>tax-engine-applicability.d76b64.d3d3f09bc0dfb0299f9f4ef374eb920f16001cd3.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d3d3f09bc0dfb0299f9f4ef374eb920f16001cd3</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\general-ledger\tax-engine-applicability.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Tax engine applicability</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジンの適用性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about Tax engine applicability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、税エンジンの適用性について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Tax engine applicability</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジンの適用性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>The <bpt id="p1">[</bpt>Tax engine<ept id="p1">](tax-engine.md)</ept> (also referred to as GTE) lets you configure tax rules that determine tax applicability, calculation, posting, and settlement, based on legal and business requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>税エンジン<ept id="p1">](tax-engine.md)</ept> (GTE とも呼ばれます) では、法的要件および業務要件に基づいて、税の適用、計算、転記、および決済を決定する税ルールを設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic walks you through a tax engine configuration to help you understand how GTE handles tax applicability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは GTE が税金の適用性を処理する方法を理解するのに役立つ税エンジン構成について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The Tax engine functionality is only available for legal entities with a primary address in India.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジン機能は、インドに基本住所がある法人に対してのみ使用可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This document uses India Goods and Services Tax configuration to explain the tax applicability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このドキュメントでは、インドの商品及びサービス税のコンフィギュレーションを使用して、税の適用について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For more information, see <bpt id="p1">[</bpt>India Goods and Services Tax<ept id="p1">](../localizations/apac-ind-gst.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>インドの商品及びサービス税<ept id="p1">](../localizations/apac-ind-gst.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Tax applicability is the condition under which tax type, tax component, or tax rate are applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税の適用性とは、税タイプ、税コンポーネント、または税率が適用される条件です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>For example, for India GST, if you sell goods from one state to another state, you need to charge IGST, and the goods you are selling will determine the tax rate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、インドの GST では、ある州から別の州に商品を販売する場合、IGST を請求する必要があります。販売している商品によって税率が決まります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The tax engine provides two ways to handle the tax applicability, lookup and condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジンは 2 種類の方法で、税の適用、ルックアップおよび条件を処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>A lookup is mainly used to handle the dynamic applicability rules, and a condition is used to handle the static applicability rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップは主に動的適用ルールを処理するために使用され、条件は静的適用ルールを処理するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The following GTE components are relevant to tax applicability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の GTE コンポーネントは、税の適用性に関連しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>GTE component</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GTE コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Lookup/Condition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ/条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Comments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Tax type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Lookup &amp; Condition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ &amp; 条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Tax component</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Lookup &amp; Condition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ &amp; 条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Both tax component and tax type can have applicability logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税コンポーネントと税タイプの両方に適用性ロジックを含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Because the tax component is under tax type, applicability logic is used to determine whether a specific tax component is applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税コンポーネントは税タイプに属しているため、特定の税コンポーネントが適用可能かどうかを判断するために適用性ロジックが使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Tax measure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税措置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The measure type should be <bpt id="p1">**</bpt>Tax rate<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Percentage<ept id="p2">**</ept>, or <bpt id="p3">**</bpt>Percentage group<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">測定タイプは、<bpt id="p1">**</bpt>税率<ept id="p1">**</ept>、<bpt id="p2">**</bpt>割合<ept id="p2">**</ept>、または<bpt id="p3">**</bpt>割合グループ<ept id="p3">**</ept>である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Formula</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">式</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Condition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For a specific transaction type, not all tax formulas are relevant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のトランザクション タイプに対して、すべての税計算式が関連するわけではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>For example, the formula that is used to calculate the non-deductible tax is only relevant for document purchases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、非控除税額の計算に使用される式は、ドキュメントの購入にのみ関連しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Posting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">転記</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Condition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Different transaction types have different posting logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">異なるトランザクション タイプには、異なる転記ロジックがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>In this case, a condition is used to ensure that the correct posting profile is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、条件を使用して正しい転記プロファイルが使用されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Accounting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Accounting is the same as tax accounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会計は税勘定と同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>With a lookup, you can maintain different sets of tax accounts for different scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップを使用すると、さまざまなシナリオに応じてさまざまな税勘定セットを管理できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>For example, different tax registration numbers have different tax accounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、税務登録番号が異なれば、税勘定も異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Credit pool</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クレジット プール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Use a lookup to determine how to settle tax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップを使用して税の決済方法を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>For example, you can settle tax based on different tax registration numbers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、さまざまな税務登録番号に基づいて税を決済できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Tax period</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税期間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Use a lookup to determine which tax period should be used for different scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップを使用して、さまざまなシナリオに使用する税の期間を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Condition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>If the applicability rule is always static, you need to use a condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適用ルールが常に静的な場合は、条件を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>For example, GST is not applicable for intra-state inventory transfer in India.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、GST はインドの州内在庫移動には適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Open Tax (India GST) by clicking the <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイナー<ept id="p1">**</ept>ボタンをクリックして税 (インドの GST) を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>CGST condition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CGST 条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Select the tax component CGST, and click the pencil icon, to check the detailed condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CGST、税コンポーネント CGST を選択し、鉛筆アイコンをクリックして、詳細な条件をチェックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>CGST condition details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CGST 条件の詳細</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The condition is actually an <bpt id="p1">[</bpt>Electronic Reporting<ept id="p1">](../../dev-itpro/analytics/general-electronic-reporting.md)</ept> expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件は、実際には、<bpt id="p1">[</bpt>電子申告<ept id="p1">](../../dev-itpro/analytics/general-electronic-reporting.md)</ept> 式です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>It is comprised of the fields on the left in <bpt id="p1">**</bpt>Data source<ept id="p1">**</ept>, and <bpt id="p2">**</bpt>Functions<ept id="p2">**</ept> on the right.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは<bpt id="p1">**</bpt>データ ソース<ept id="p1">**</ept>の左側のフィールドと右側の<bpt id="p2">**</bpt>関数<ept id="p2">**</ept>で構成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For a list of supported functions, see <bpt id="p1">[</bpt>Functions<ept id="p1">](../../dev-itpro/analytics/general-electronic-reporting-formula-designer.md#supported-functions)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポートされている関数の一覧については、<bpt id="p1">[</bpt>関数<ept id="p1">](../../dev-itpro/analytics/general-electronic-reporting-formula-designer.md#supported-functions)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>The following condition means that <bpt id="p1">*</bpt>Taxable Document Type<ept id="p1">*</ept> cannot be "Invent transfer order receive", "Invent transfer order shipment", or "Invent transfer order".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の条件は、<bpt id="p1">*</bpt>課税対象文書のタイプ<ept id="p1">*</ept>を「在庫転送オーダー受信」、「在庫転送オーダー出荷」、または「在庫転送オーダー」にすることはできないことを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>This also means that either HSN Code or SAC should be specified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり HSN コードまたは SAC のいずれかを指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Enable GST for intra-state inventory transfer order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">州内在庫移動オーダーに対して GST を有効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In this scenario, suppose that the Indian government requires you to calculate GST for intra-state inventory transfer orders if the GST registration numbers are different between the ship from and ship to warehouse.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオでは、GST 登録番号が出荷元と出荷先の倉庫間で異なる場合、インド政府が州内在庫移動オーダーの GST の計算を要求するとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Structure of the Data source in the formula designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーミュラ デザイナーのデータソースの構造</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>On the leftmost side of the formula designer, you can find all the fields that are defined in the taxable document and tax document, and the reference model that is defined in the taxable document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーミュラ デザイナーの左端には、課税対象文書と税務書類に定義されているすべてのフィールドと、課税対象文書に定義されている参照モデルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Change the applicability condition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適用条件を変更する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>To change the applicability condition, go to <bpt id="p1">**</bpt>Header &gt; Lines &gt; GST Registration number<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Header &gt; Lines &gt; Party GST Registration number<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適用条件を変更するには<bpt id="p1">**</bpt>ヘッダー &gt; 明細行 &gt; GST 登録番号<ept id="p1">**</ept>および<bpt id="p2">**</bpt>ヘッダー &gt; 明細行 &gt; パーティ GST 登録番号<ept id="p2">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>These represent the GST registration numbers for the ship from and ship to warehouse.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは、倉庫からの出荷および倉庫への出荷の GST 登録番号を表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The condition can be changed to the following.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件は以下のように変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Select the field from the data source, and use <bpt id="p1">**</bpt>Add data source<ept id="p1">**</ept> to add the field into the formula.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースからフィールドを選択し、<bpt id="p1">**</bpt>データ ソースの追加<ept id="p1">**</ept>を使用して、式にフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Make sure to use single quotes for the data source field if there is an empty space in the name, like 'Taxable Document Type'.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「課税対象文書のタイプ」のように、名前に空白がある場合は、データ ソース フィールドの単一引用符を使用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Use a double quote for the value if there is an empty space, like "Inventory transfer order".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「在庫移動オーダー」のように空白がある場合は、値に対して二重引用符を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Click <bpt id="p1">**</bpt>Test<ept id="p1">**</ept> to test your formula after you are done with editing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">編集が完了した後に、<bpt id="p1">**</bpt>テスト<ept id="p1">**</ept>をクリックして式をテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>If the static applicability rules are complex, or it is a dynamic applicability rule, you need to use a lookup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的適用ルールが複雑な場合、または動的適用ルールである場合は、ルックアップを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Lookup for static applicability rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的適用ルールのルックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Select <bpt id="p1">**</bpt>GST<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Lookups<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GST<ept id="p1">**</ept> を選択して、<bpt id="p2">**</bpt>ルックアップ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>CGST condition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CGST 条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Because a lookup can handle both static applicability rules and dynamic applicability rules, the <bpt id="p1">**</bpt>Source type<ept id="p1">**</ept> drop-down list is for this purpose.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップは静的適用ルールと動的適用ルールの両方を処理できるので、<bpt id="p1">**</bpt>ソース タイプ<ept id="p1">**</ept>ドロップダウンリストはこの目的のためにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Use <bpt id="p1">**</bpt>Configuration<ept id="p1">**</ept> for the static applicability rule, which means that the data used in the lookup comes from the configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的適用ルールには<bpt id="p1">**</bpt>コンフィギュレーション<ept id="p1">**</ept>を使用します。これは、ルックアップで使用されるデータがコンフィギュレーションから取得されることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Use <bpt id="p1">**</bpt>User data<ept id="p1">**</ept> for the dynamic applicability rule, which means that the data used in the lookup comes from the runtime environment, such as Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">動的適用ルールには<bpt id="p1">**</bpt>ユーザー データ<ept id="p1">**</ept>を使用します。これは、ルックアップに使用されるデータが Finance and Operations などのランタイム環境から取得されることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>A lookup is a matrix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップはマトリックスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>The relation of each line is <bpt id="p1">*</bpt>OR<ept id="p1">*</ept>, and the relation of each column within the line is <bpt id="p2">*</bpt>AND<ept id="p2">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各行の関係は <bpt id="p1">*</bpt>OR<ept id="p1">*</ept> で、行内の各列の関係は <bpt id="p2">*</bpt>AND<ept id="p2">*</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If the value of the cell is empty, it means that all of the values satisfy the condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セルの値が空の場合は、すべての値が条件を満たすことを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In the screenshot above, all the data for the lookup of tax type GST comes from the configuration, so the <bpt id="p1">**</bpt>Source type<ept id="p1">**</ept> is <bpt id="p2">**</bpt>Configuration<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上のスクリーンショットでは、税タイプ GST のルックアップのためのすべてのデータはコンフィギュレーションから来ているので、<bpt id="p1">**</bpt>ソース タイプ<ept id="p1">**</ept>は<bpt id="p2">**</bpt>コンフィギュレーション<ept id="p2">**</ept>です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>If you convert the lookup of GST into a condition, it will look like following.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GST のルックアップを条件に変換する場合は次のように表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Lookup for dynamic applicability rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">動的適用ルールのルックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Many applicability rules depend on the runtime data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの適用ルールは、ランタイム データに依存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>For example, some tax components are only applicable for a certain good or service, so a different type of tax transaction results in a different tax rate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、一部の税コンポーネントは特定の商品またはサービスにのみ適用されるため、税務取引の種類が異なると税率も異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Select <bpt id="p1">**</bpt>CESS<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Lookups<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CESS<ept id="p1">**</ept> を選択して、<bpt id="p2">**</bpt>ルックアップ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>In India, CESS is applicable for certain goods and services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インドでは、CESS は、特定の商品やサービスに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>In Finance and Operations, HSN represents goods, SAC represents services, so HSN Code and SAC are used in the lookup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations では、HSN は商品を表し、SAC はサービスを表すため、ルックアップでは HSN コードと SAC が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>The <bpt id="p1">**</bpt>Source type<ept id="p1">**</ept> is <bpt id="p2">**</bpt>User data<ept id="p2">**</ept>, because the real value of HSN Code and SAC come from Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HSN Code と SAC の実際の価は Finance and Operations から取得されるため、<bpt id="p1">**</bpt>ソース タイプ<ept id="p1">**</ept>は<bpt id="p2">**</bpt>ユーザー データ<ept id="p2">**</ept>です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Now, let's check how the CGST rate is determined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここでは、CGST レートを決定する方法を確認しましょう。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Select <bpt id="p1">**</bpt>CGST &gt; Rate<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Lookups<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CGST &gt; レート<ept id="p1">**</ept>の順に選択し、<bpt id="p2">**</bpt>ルックアップ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>CGST&gt;Rate Lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CGST &gt; レート ルックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Runtime data is required to determine the tax rate, so the system hides the <bpt id="p1">**</bpt>Source type<ept id="p1">**</ept>, and the <bpt id="p2">**</bpt>User data<ept id="p2">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ランタイム データは税率を決定するために必要なので、システムは<bpt id="p1">**</bpt>ソース タイプ<ept id="p1">**</ept>と<bpt id="p2">**</bpt>ユーザー データ<ept id="p2">**</ept>の値を隠します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Different goods and services result in different tax rates, so there are <bpt id="p1">**</bpt>HSN Code<ept id="p1">**</ept> and <bpt id="p2">**</bpt>SAC<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">商品やサービスが異なれば税率が異なるため、<bpt id="p1">**</bpt>HSN コード<ept id="p1">**</ept>および <bpt id="p2">**</bpt>SAC<ept id="p2">**</ept> があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Party GST Registration Number<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Tax Direction<ept id="p2">**</ept> are used to handle the scenario of purchasing from an unregistered GST supplier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パーティ GST 登録番号<ept id="p1">**</ept>および<bpt id="p2">**</bpt>税提示方法<ept id="p2">**</ept>は、GST 未登録の仕入先から購入するシナリオを処理するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source><bpt id="p1">**</bpt>Transaction Date from<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Transaction Date to<ept id="p2">**</ept> are used to handle different tax rate per periods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トランザクション開始日<ept id="p1">**</ept>および<bpt id="p2">**</bpt>トランザクション終了日<ept id="p2">**</ept>は、期間ごとに異なる税率を処理するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Enable different tax rate for different goods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">商品ごとに異なる税率を有効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Different goods can share one HSN code, so the lookup cannot satisfy this scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">異なる商品が 1 つの HSN コードを共有できるため、ルックアップでこのシナリオを満たすことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>A different lookup column is needed to handle this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これに対応するには、別のルックアップ列が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Click <bpt id="p1">**</bpt>Columns<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>列<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>On the left side, you can find all of the <bpt id="p1">**</bpt>Available columns<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左側に<bpt id="p1">**</bpt>使用可能な列<ept id="p1">**</ept>がすべてあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The structure is the same as the <bpt id="p1">**</bpt>Data source<ept id="p1">**</ept> in the formula designer, except that there are no reference models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構造は、参照モデルがないことを除けば、フォーミュラ デザイナーの<bpt id="p1">**</bpt>データ ソース<ept id="p1">**</ept>と同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>CGST&gt;Rate Change Lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CGST &gt; レート 変更 ルックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Select <bpt id="p1">**</bpt>Item ID<ept id="p1">**</ept> in <bpt id="p2">**</bpt>Available columns<ept id="p2">**</ept> to uniquely determine the goods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>使用可能な列<ept id="p2">**</ept>で<bpt id="p1">**</bpt>品目 ID<ept id="p1">**</ept>を選択し、商品を一意に決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Click the right-arrow icon to add it to the <bpt id="p1">**</bpt>Selected columns<ept id="p1">**</ept> side.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右矢印アイコンをクリックして、<bpt id="p1">**</bpt>選択された列<ept id="p1">**</ept>側に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>If HSN is not needed, you can select <bpt id="p1">**</bpt>HSN Code<ept id="p1">**</ept> in <bpt id="p2">**</bpt>Selected columns<ept id="p2">**</ept>, and click the left-arrow icon to remove it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HSN が不要な場合は、<bpt id="p2">**</bpt>選択された列<ept id="p2">**</ept>で <bpt id="p1">**</bpt>HSN コード<ept id="p1">**</ept>を選択し、左矢印アイコンをクリックして削除できます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
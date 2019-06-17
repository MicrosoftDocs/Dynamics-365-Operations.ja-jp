<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="order-attributes.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>order-attributes.ad5f89.d0aa6b55700a53becf5adcee3212615a5b85c875.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d0aa6b55700a53becf5adcee3212615a5b85c875</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>82447ca02786f41b799ab079e14d4361838044a9</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/28/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\order-attributes.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Define and set order attributes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注文属性の定義と設定をする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to edit and set attributes values for orders directly in Retail headquarters, the POS, and CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、小売用バックオフィス、POS、および CRT でオーダーの属性値を直接編集および設定する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Define and set order attributes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注文属性の定義と設定をする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Previously, the attribute framework supported attributes only in online orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前は、属性フレームワークは、オンライン注文でのみ属性をサポートしていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, the framework has been extended so that it now supports attributes in cash-and-carry transactions, customer orders, and call center orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、フレームワークが拡張されたため、現金売りトランザクション、顧客の注文、およびコール センター注文の属性がサポートされるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This enhancement lets you edit and set attribute values for orders directly in Retail headquarters, the point of sale (POS), and the Commerce runtime (CRT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能拡張により、小売用バックオフィス、販売時点管理 (POS)、および <ph id="1">Commerce Runtime</ph> (<ph id="2">CRT</ph>) でオーダーの属性値を直接編集および設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Retail headquarters now includes pages for editing and updating attribute values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バック オフィスには、属性の値を編集したり更新するためのページが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Therefore, you can set the values for call center orders in Retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たがって、コール センター注文の値は、小売用バックオフィスで設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Although no out-of-box user interface (UI) for setting attribute values is available in the POS, you can extend the POS to add a new UI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で使用できる属性値を設定するためのユーザー インターフェイス (UI) がありませんが、新しい UI を追加する POS を拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If you don't require a UI and just want to add business logic, you can add the business logic directly in CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UI を必要とせず、ビジネス ロジックを追加するだけの場合、ビジネス ロジックを CRT に直接追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can create new attributes by using the Retail headquarters configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売り用バックオフィス構成を使用することにより、新しい属性を作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>No database changes are required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの変更は必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Previously, you had to create new tables in Retail headquarters and the channel database, and then modify those tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前は、小売用バックオフィスとチャンネル データベースで新しいテーブルを作成するには、それらのテーブルを変更する必要がありました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Why and when you should order attributes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注文属性が必要な理由および場合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If you want to add new fields to cash-and-carry transactions, customer orders, or call center orders, and if you want to capture the information in the POS or Retail headquarters, use order attributes.</source><target logoport:matchpercent="96" state="translated" state-qualifier="fuzzy-match">現金売りトランザクション、顧客注文、またはコールセンターの注文に新しいフィールドを追加し、POS または Retail Headquarters で情報をキャプチャする場合は、注文属性を使用します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Previously, to add a new field to a cash-and-carry transaction (transaction header or lines) or a customer order in the POS, you had to create a new extension table in Retail headquarters and the channel database, and then make inline changes to CRT and POS code to handle the various screens and operations.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">以前は、現金売りトランザクション (トランザクション ヘッダーまたは行) または POS の顧客注文に新しいフィールドを追加するには、小売用バックオフィスとチャネル データベースで新しい拡張テーブルを作成し、CRT および POS コードにインライン変更を加えて各種画面および操作を処理する必要がありました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You also had to configure Commerce Data Exchange to synchronize the data between the channel database and Retail headquarters.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">また、チャネル データベースと小売用バックオフィス間でデータを同期するように Commerce Data Exchange を構成する必要がありました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, order attributes now let you complete all these actions through configuration.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">ただし、注文属性はコンフィギュレーションを通してこれらすべてのアクションを完了できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>You don't have to write any code or create custom extension tables, but you still need to create the core business logic and the POS UI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードを記述またはカスタム拡張機能テーブルを作成する必要はありませんが、主要なビジネス ロジックおよび POS UI を作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This first version supports only the <bpt id="p1">**</bpt>String<ept id="p1">**</ept> attribute type, but future versions will support other attribute types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この最初のバージョンは <bpt id="p1">**</bpt>String<ept id="p1">**</ept> 属性タイプのみをサポートしますが、将来のバージョンは他の属性タイプをサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>If you want the data to come from the master table, and that data involves complex search logic and core business logic in X++, you should use extension properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データをマスター テーブルから取得し、そのデータに X++ の複雑な検索ロジックとコア ビジネス ロジックが必要な場合は、拡張プロパティを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>We only support attributes on customer orders and cash-and-carry transactions, no other transaction types are supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客注文および現金店頭払いのトランザクションでのみ属性がサポートされます。他のトランザクション タイプはサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Define attribute types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性タイプを定義</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>First, you must define the attribute types and assign valid ranges to them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、属性タイプを定義し、それに有効な範囲を割り当てる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Go to <bpt id="p1">**</bpt>Product information management<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Setup<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Categories and attributes<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>Attribute types<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>製品情報管理<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>カテゴリと属性<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>属性タイプ<ept id="p4">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>On the <bpt id="p1">**</bpt>Attribute types<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>New<ept id="p2">**</ept> to add a new attribute type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>属性タイプ<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept>を選択し、新しい属性タイプを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Enter a name for the attribute type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層タイプ名を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>On the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> FastTab, in the <bpt id="p2">**</bpt>Type<ept id="p2">**</ept> field, select the type of data that can be entered for attributes that are assigned to this data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>一般<ept id="p1">**</ept>クイック タブの、<bpt id="p2">**</bpt>タイプ<ept id="p2">**</ept>フィールドで、このデータ型に割り当てられている属性に入力できるデータのタイプを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>If the attribute type is <bpt id="p1">**</bpt>Decimal<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Integer<ept id="p2">**</ept>, select a unit of measure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性タイプが<bpt id="p1">**</bpt>少数点<ept id="p1">**</ept>または<bpt id="p2">**</bpt>整数<ept id="p2">**</ept>の場合、測定単位を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If the attribute type is <bpt id="p1">**</bpt>Text<ept id="p1">**</ept>, you can define a fixed list of values for it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性の型が<bpt id="p1">**</bpt>テキスト<ept id="p1">**</ept>である場合は、それを固定値の一覧を定義できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Select the <bpt id="p1">**</bpt>Fixed list<ept id="p1">**</ept> check box, and then, on the <bpt id="p2">**</bpt>Values<ept id="p2">**</ept> FastTab, enter the list of values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>固定リスト<ept id="p1">**</ept> チェック ボックスをオンにし、<bpt id="p2">**</bpt>値<ept id="p2">**</ept> クイック タブで、値の一覧を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>To define a range of valid values for the attribute type, select the <bpt id="p1">**</bpt>Value range<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性タイプに有効な値の範囲を定義するには、<bpt id="p1">**</bpt>値の範囲<ept id="p1">**</ept> チェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Then, on the <bpt id="p1">**</bpt>Range<ept id="p1">**</ept> FastTab, enter the valid range of values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、<bpt id="p1">**</bpt>範囲<ept id="p1">**</ept> クイックタブで、値の有効範囲を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Define the attributes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性の定義</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Next, you must define the attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、属性を定義する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Follow these steps for each attribute that you want to define.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定義する各属性に対して、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Go to <bpt id="p1">**</bpt>Product information management<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Setup<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Categories and attributes<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>Attributes<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>製品情報管理<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>カテゴリと属性<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>属性<ept id="p4">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>On the <bpt id="p1">**</bpt>Attributes<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>New<ept id="p2">**</ept> to add a new attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>属性<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept>を選択し、新しい属性を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Enter a name, friendly name, and description for the attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性の名前、フレンドリ名、および説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Additionally, enter any Help text that should be shown to the user for the attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、属性にユーザーを表示する必要があるヘルプ テキストを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In the <bpt id="p1">**</bpt>Attribute type<ept id="p1">**</ept> field, select the attribute type to assign to the attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>属性タイプ<ept id="p1">**</ept> フィールドで、属性に割り当てる属性タイプを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Depending on the attribute type, in the <bpt id="p1">**</bpt>Default value<ept id="p1">**</ept> field, enter the value or range of values that is shown by default when the attribute is assigned to a channel.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">属性タイプに応じて、<bpt id="p1">**</bpt>既定値<ept id="p1">**</ept> フィールドに、属性がチャネルに割り当てられたときに既定で表示される値または値の範囲を入力します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Select <bpt id="p1">**</bpt>Translate<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>翻訳<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Then, on the <bpt id="p1">**</bpt>Text translation<ept id="p1">**</ept> page, enter the name, description, friendly name, and Help text for the attribute in additional languages.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>テキストの翻訳<ept id="p1">**</ept> ページで、追加の言語で属性の名前、説明、フレンドリ名、およびヘルプ テキストを入力できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Define attribute groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性グループの定義</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Go to <bpt id="p1">**</bpt>Product information management<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Setup<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Categories and attributes<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>Attribute groups<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>製品情報管理<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>カテゴリと属性<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>属性グループ<ept id="p4">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>On the <bpt id="p1">**</bpt>Attribute groups<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>New<ept id="p2">**</ept> to add a new attribute group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>属性グループ<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept>を選択し、新しい属性グループを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Enter a name for the attribute group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性グループ名を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Then, on the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> FastTab, enter a friendly name, a description, and any Help text for the attribute group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>全般<ept id="p1">**</ept> クイックタブで、属性グループのフレンドリ名、説明、およびヘルプ テキストを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>On the <bpt id="p1">**</bpt>Attributes<ept id="p1">**</ept> FastTab, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept> to add attributes to the attribute group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>属性<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>を選択して、属性グループに属性を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>In the <bpt id="p1">**</bpt>Default value<ept id="p1">**</ept> field, you can enter a default value for the selected attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既定値<ept id="p1">**</ept>フィールドでは、選択した属性の既定値を入力できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Select <bpt id="p1">**</bpt>Translate<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>翻訳<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Then, on the <bpt id="p1">**</bpt>Text translation<ept id="p1">**</ept> page, enter the description, friendly name, and Help text for the attribute group in additional languages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>テキストの翻訳<ept id="p1">**</ept> ページで、追加の言語で属性グループの説明、フレンドリ名、およびヘルプ テキストを入力できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Link the attribute group to the channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性グループのチャネルへのリンク</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Channels<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Retail stores<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>All retail stores<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>チャンネル<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>小売店舗<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>すべての小売店舗<ept id="p4">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Select the channel that the attributes on the <bpt id="p1">**</bpt>Channel<ept id="p1">**</ept> page should be linked to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チャネル<ept id="p1">**</ept> ページの属性をリンクする必要があるチャネルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>On the <bpt id="p1">**</bpt>Set up<ept id="p1">**</ept> tab, select <bpt id="p2">**</bpt>Sales order attributes<ept id="p2">**</ept> under <bpt id="p3">**</bpt>Attribute group<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定<ept id="p1">**</ept>タブで、<bpt id="p3">**</bpt>属性グループ<ept id="p3">**</ept>の<bpt id="p2">**</bpt>販売注文属性<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>On the <bpt id="p1">**</bpt>Sales order attribute groups<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>New<ept id="p2">**</ept> to link the attribute group to the channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>販売注文属性グループ<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept>を選択し、属性グループをチャネルにリンクします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, select the attribute group to link to the channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>フィールドで属性グループを選択してチャネルにリンクします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>In the <bpt id="p1">**</bpt>Apply attributes to<ept id="p1">**</ept> field, select one of the following options:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>属性の適用先<ept id="p1">**</ept>フィールドで、次のいずれかのオプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Header<ept id="p1">**</ept> – The attributes will apply only to the transaction header.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ヘッダー<ept id="p1">**</ept> – 属性は、トランザクション ヘッダーにのみ適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Lines<ept id="p1">**</ept> – The attribute will apply only to the transaction lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>明細行<ept id="p1">**</ept> – 属性は、トランザクション明細行にのみ適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Default<ept id="p1">**</ept> – The attribute will apply to both the transaction header and the transaction lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既定<ept id="p1">**</ept> - 属性は、トランザクション ヘッダーとトランザクション明細行の両方に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Run the distribution jobs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配送ジョブを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>小売 IT<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>配送スケジュール<ept id="p3">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Select <bpt id="p1">**</bpt>Products (1040)<ept id="p1">**</ept>, and then, on the Action Pane, select <bpt id="p2">**</bpt>Run now<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>製品 (1040)<ept id="p1">**</ept> を選択し、アクション ペインで <bpt id="p2">**</bpt>今すぐ実行<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>When you're prompted, select <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージが表示されたら、<bpt id="p1">**</bpt>はい<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>This step is required only if you added any new attributes, attribute types, or attribute groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップは、新しい属性、属性タイプ、または属性グループを追加した場合にのみ必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Select <bpt id="p1">**</bpt>Channel configuration job (1070)<ept id="p1">**</ept>, and then, on the Action Pane, select <bpt id="p2">**</bpt>Run now<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チャネル コンフィギュレーション ジョブ (1070)<ept id="p1">**</ept> を選択し、アクション ペインで <bpt id="p2">**</bpt>今すぐ実行<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you're prompted, select <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージが表示されたら、<bpt id="p1">**</bpt>はい<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Show order attributes in the POS transaction screen using the Attribute control (this feature is available in version 8.1.3 and later)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性コントロールを使用して POS トランザクション画面に注文属性を表示します (この機能はバージョン 8.1.3 以降で使用できます)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Retail headquarters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="1">Retail Headquarters</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Select <bpt id="p1">**</bpt>Retail &gt; Channel setup &gt; POS Setup &gt; POS &gt; Screen layouts<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Retail &gt; チャネル設定 &gt; POS 設定 &gt; POS &gt; 画面レイアウト<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>On the screen layout page, click <bpt id="p1">**</bpt>New<ept id="p1">**</ept> to create a new screen layout, or select an existing screen layout.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画面レイアウトページで、<bpt id="p1">**</bpt>新規<ept id="p1">**</ept> をクリックして新しい画面レイアウトを作成するか、既存の画面レイアウトを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Enter the ID and name for the screen layout.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリーン レイアウトの名前と ID を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>On the <bpt id="p1">**</bpt>Layout sizes<ept id="p1">**</ept> FastTab, select the <bpt id="p2">**</bpt>Add<ept id="p2">**</ept> button to add new layout sizes for the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レイアウト サイズ<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>ボタン選択して、POS の新しいレイアウト サイズを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, select the POS screen resolution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>フィールドで POS 画面の解像度を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>On the <bpt id="p1">**</bpt>Layout sizes<ept id="p1">**</ept> FastTab, click the <bpt id="p2">**</bpt>Layout designer<ept id="p2">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レイアウト サイズ<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>レイアウト デザイナー<ept id="p2">**</ept>ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>If you're prompted, select <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to download and install the Retail Designer Host by using the <bpt id="p2">**</bpt>Install/Run<ept id="p2">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロンプトが表示されたら、<bpt id="p2">**</bpt>インストール/実行<ept id="p2">**</ept>ボタンを使用して Retail Designer Host をダウンロードしてインストールするには、<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>When you're prompted, enter the Microsoft Dynamics 365 user name and password to start the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入力を求めるメッセージが表示されたら、Microsoft Dynamics 365 のユーザー名とパスワードを入力して、デザイナーを起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>After the designer is started, drag the Attributes panel anywhere in the screen layout designer and adjust the size according to your screen width.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーが開始されたら、属性パネルを画面レイアウト デザイナー内の任意の場所にドラッグし、画面の幅に従ってサイズを調整します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>When you've finished, select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to save your changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了したら、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> を選択して、変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Close the screen layout designer by clicking the <bpt id="p1">**</bpt>Close<ept id="p1">**</ept> button (X) in the upper-right corner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右上隅の <bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept> ボタン (X) をクリックし、画面レイアウト デザイナーを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>When you're prompted, select <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to save your changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージが表示されたら、<bpt id="p1">**</bpt>はい<ept id="p1">**</ept> を選択して、変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Go to <bpt id="p1">**</bpt>Retail &gt; Retail IT &gt; Distribution schedule<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売 &gt; 小売 IT &gt; 配送スケジュール<ept id="p1">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Select the Registers job (1090), and then, on the Action Pane, select <bpt id="p1">**</bpt>Run now<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジスター ジョブ (1090) を選択し、アクション ペインで <bpt id="p1">**</bpt>今すぐ実行<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>When you're prompted, select Yes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージが表示されたら、はい を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Start POS, and add any item to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS を起動し、任意の品目をトランザクションに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>You should see the Attribute panel in the transaction screen with the configured attributes both for header and lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘッダーと明細行の両方のコンフィギュレーション済の属性と共に、トランザクション画面に属性パネルが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Click the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> icon in the attribute panel to update the attribute value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性パネルで <bpt id="p1">**</bpt>編集<ept id="p1">**</ept> アイコンをクリックして、属性の値を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Click the header or lines tab in the attribute panel to view the header or lines attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性パネルでヘッダーまたは明細行タブをクリックして、ヘッダーまたは明細行の属性パネルを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The lines attribute will refresh automatically based on the lines selected in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明細行の属性は、トランザクションで選択した明細行に基づいて自動的に更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Set attribute values for call center orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コール センターの注文の属性値を設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>After you configure the order attributes for the channel, go to <bpt id="p1">**</bpt>Customer service<ept id="p1">**</ept> or <bpt id="p2">**</bpt>All Sales orders<ept id="p2">**</ept>, and create a new call center order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャンネルの注文属性を構成した後、<bpt id="p1">**</bpt>顧客サービス<ept id="p1">**</ept>または<bpt id="p2">**</bpt>すべての販売注文<ept id="p2">**</ept>、およびコール センターの新しい注文を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>After or during the creation of a customer order, if you want to set an attribute value for the transaction header, on the Action Pane, on the <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> tab, select <bpt id="p2">**</bpt>Retail Attributes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客注文の作成後または作成中に、トランザクション ヘッダーの属性値を設定する場合は、アクション ウィンドウの<bpt id="p1">**</bpt>小売<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>小売属性<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>On the <bpt id="p1">**</bpt>Sales order attributes values<ept id="p1">**</ept> page, you can set the values for the attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>販売注文属性値<ept id="p1">**</ept>ページで、属性値を設定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>The list of attributes on this page is based on the attribute group that you configured for the channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このページの属性のリストは、チャネル用にコンフィギュレーションした属性グループに基づいています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>To set attribute values at the line level, on the <bpt id="p1">**</bpt>Sales order<ept id="p1">**</ept> page, select the <bpt id="p2">**</bpt>Lines<ept id="p2">**</ept> view, and then select the line to set the attribute value for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">行レベルで属性値を設定するには、<bpt id="p1">**</bpt>販売注文<ept id="p1">**</ept> ページで <bpt id="p2">**</bpt>行<ept id="p2">**</ept> ビューを選択し、属性値を設定する行を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Under <bpt id="p1">**</bpt>Sales order lines group<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Retail<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Retail attributes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>販売注文明細行グループ<ept id="p1">**</ept> で <bpt id="p2">**</bpt>小売<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>小売属性<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Repeat step 3 for all the sales lines that you want to set the values for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値を設定するすべての販売明細行に対して手順 3 を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>View the attributes values for cash-and-carry transactions in Retail headquarters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バック オフィスでの現金売りトランザクションの属性値の表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>After you've run the distribution job and pulled a cash-and-carry transaction into Retail headquarters, you can view the attribute values for that transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配送ジョブを実行し小売用バックオフィスに現金売りトランザクションを収集した後、トランザクションの属性値を表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>The POS doesn't provide a UI for viewing order attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS は、注文の属性を表示するための UI を提供しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Therefore, to view the order attribute values, you must extend the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、注文の属性値を表示するには、POS を拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Inquires and reports<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Retail store transactions<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>照会およびレポート<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>小売店舗のトランザクション<ept id="p3">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>To view the transaction header attributes, on the Action Pane, select <bpt id="p1">**</bpt>Retail attributes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション ヘッダー属性を表示するには、アクション ウィンドウで <bpt id="p1">**</bpt>小売属性<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>To view the transaction lines attributes, on the Action Pane, select <bpt id="p1">**</bpt>Transaction<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Sales transaction<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション ヘッダー行の属性を表示するには、アクション ウィンドウで <bpt id="p1">**</bpt>トランザクション<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>販売トランザクション<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Sales transactions<ept id="p1">**</ept> page, select any line, and then, on the Action Pane, select <bpt id="p2">**</bpt>Retail attributes<ept id="p2">**</ept> to view the line attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>販売トランザクション<ept id="p1">**</ept>ページで、すべての明細行を選択し、アクション ウィンドウで、<bpt id="p2">**</bpt>小売属性<ept id="p2">**</ept>を選択して、明細行の属性を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Only the attributes that are configured as part of your attribute group and linked to the channel will appear in the Retail headquarters UI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">あなたの属性グループの一部として構成され、チャンネルにリンクされている属性のみ、Retail headquarters UI に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Extend attributes to add business logic in CRT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT でビジネス ロジックを追加するには、属性を拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>A new sample that has been added to the Retail SDK adds business logic for order attributes in CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK に追加された新しいサンプルでは、CRT の注文属性のビジネス ロジックを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>This sample includes code only for the business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例には、ビジネス ロジックのコードのみが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>It doesn't show how to save or read the attributes, because read and write operations for attributes are automated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性に対する読み取りおよび書き込み処理は自動化されているため、属性を保存したり読み取ったりする方法は示しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The sample implements the following scenario: Whenever you suspend a cart, you set set an attribute value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサンプルでは、次のシナリオを実装しています。カートを中断するときはいつでも、属性値を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>When you resume the cart, you want to clear that value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カートを再開するとき、その値を消去します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>A pre-trigger was added for <bpt id="p1">**</bpt>SuspendCartRequest<ept id="p1">**</ept>, and the business logic was written.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">事前トリガーが <bpt id="p1">**</bpt>SuspendCartRequest<ept id="p1">**</ept> に追加され、ビジネス ロジックが記述されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>You can extend any trigger or override any request in CRT to set the logic, based on your scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT で任意のトリガーを拡張または任意の要求をオーバーライドして、シナリオに基づきロジックをセットすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>You can find the full sample code in the Retail SDK at Retail SDK<ph id="ph1">\\</ph>SampleExtensions<ph id="ph2">\\</ph>CommerceRuntime<ph id="ph3">\\</ph>Extensions.TransactionAttributesSample.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全なサンプル コードは Retail SDK<ph id="ph1">\\</ph>SampleExtensions<ph id="ph2">\\</ph>CommerceRuntime<ph id="ph3">\\</ph>Extensions.TransactionAttributesSample の Retail SDK で見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Create a new C# portable class library project, and paste in the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい C# ポータブル クラス ライブラリ プロジェクトを作成し、次のコードを貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Extend attributes to do some business logic in the POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS でビジネス ロジックを行うには、属性を拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>The following changes are required only if you are running the application with version 8.1.2 or earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン 8.1.2 以降でアプリケーションを実行している場合にのみ、次の変更が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Starting in 8.1.3, you can use the new Attributes panel to set or update the attribute value in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">8.1.3 以降は、新しい属性パネルを使用して、POS で属性の値を設定または更新できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>With this control you no longer  need to write any additional code or create UI to set the attribute value in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントロールでは、POS で属性値を設定するために追加のコードを記述したり、UI を作成したりする必要がなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>In the attribute control UI has been added to set or update the attribute value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性値を設定または更新するための属性コントロール UI が追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Refer to the <bpt id="p1">**</bpt>Show Order attributes in the POS transaction screen using the Attribute control<ept id="p1">**</ept> section in this document for more details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、このドキュメントの<bpt id="p1">**</bpt>属性コントロールを使用して POS トランザクション画面で注文属性を表示する<ept id="p1">**</ept>セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>A new sample that has been added to the Retail SDK sets the business logic for order attributes in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK に追加された新しいサンプルでは、POS の注文属性のビジネス ロジックを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>This sample includes code only for the business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例には、ビジネス ロジックのコードのみが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>It doesn't show how to save or read attribute values, because read and write operations for attributes are automated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性に対する読み取りおよび書き込み処理は自動化されているため、属性の値を保存したり読み取ったりする方法は示しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>You can set the values for attributes in either CRT or the POS, based on your scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性の値は、シナリオに基づき、CRT または POS のいずれかで設定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>If your values are based on customer input, set them in the POS client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値が顧客の入力に基づいている場合、POS クライアントで設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>If some business logic is involved, set the values in CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部のビジネス ロジックが含まれている場合は、CRT で値を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>The sample implements the following scenario: You create a business-to-business (B2B) order and want to set the B2B attribute value (<bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> or <bpt id="p2">**</bpt>No<ept id="p2">**</ept>), based on customer input.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサンプルでは、次のシナリオを実装しています。企業間 (B2B) 注文を作成し、 顧客からのフィードバックに基づいて B2B 属性の値を設定する場合 (<bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> または <bpt id="p2">**</bpt>No<ept id="p2">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source><bpt id="p1">**</bpt>PreEndTransactionTrigger<ept id="p1">**</ept> was extended in the POS to set the values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreEndTransactionTrigger<ept id="p1">**</ept> は値を設定するために POS で拡張されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>You can extend any POS trigger or override the request as appropriate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて任意の POS トリガーを拡張、または要求をオーバーライドすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>You can find the full sample code in the Retail SDK at Retail SDK<ph id="ph1">\\</ph>POS<ph id="ph2">\\</ph>Extensions<ph id="ph3">\\</ph>B2BSample.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全なサンプル コードは Retail SDK<ph id="ph1">\\</ph>POS<ph id="ph2">\\</ph>Extensions<ph id="ph3">\\</ph>B2BSample の Retail SDK で見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Only the configured attributes will appear in the Retail headquarters UI, even if you set or add attributes and attribute values in the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのコードに属性と属性値を設定または追加した場合でも、構成された属性のみ Retail headquarters UI に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>If an attribute isn't part of the attribute group that you linked to the channel, it won't appear in the Retail headquarters UI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性が、チャンネルにリンクされている属性グループに属さない場合は、小売用バックオフィス UI に反映されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>From the Retail SDK, open <bpt id="p1">**</bpt>ModernPOS.sln<ph id="ph1">\\</ph>CloudPos.sln<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK から <bpt id="p1">**</bpt>ModernPOS.sln<ph id="ph1">\\</ph>CloudPos.sln<ept id="p1">**</ept> を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>In the Retail SDK, create a new extension folder under the <bpt id="p1">**</bpt>POS.Extension<ept id="p1">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK で、<bpt id="p1">**</bpt>POS.Extension<ept id="p1">**</ept> プロジェクトに新しい拡張フォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>In the new extension folder, add a new <bpt id="p1">**</bpt>manifest.json<ept id="p1">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい拡張フォルダーに、新しい <bpt id="p1">**</bpt>manifest.json<ept id="p1">**</ept> ファイルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Paste in the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードに貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Create a new TypeScript file to implement <bpt id="p1">**</bpt>PreEndTransactionTrigger<ept id="p1">**</ept>, and add the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい TypeScript ファイルを作成して <bpt id="p1">**</bpt>PreEndTransactionTrigger<ept id="p1">**</ept> を実装し、次のコードを追加します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
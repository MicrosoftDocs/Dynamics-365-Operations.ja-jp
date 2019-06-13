<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cost.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cost.4e88df.80e7a033467c3d94d55f06daa05f99bd27e19a29.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>80e7a033467c3d94d55f06daa05f99bd27e19a29</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\cost.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Cost configuration for distributed order management (DOM)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">配分済み注文の管理 (DOM) の原価コンフィギュレーション</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes cost configuration for the distributed order management (DOM) functionality in Microsoft Dynamics 365 for Retail.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">このトピックでは、Microsoft Dynamics 365 for Retail の配分済み注文の管理 (DOM) 機能の原価コンフィギュレーションについて説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Cost configuration for distributed order management (DOM)</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">配分済み注文の管理 (DOM) の原価コンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">組織は、注文のフルフィルメントに最適な場所を決定するために、複数の原価コンポーネントを考慮します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some of these cost components are shipping cost, handling cost, and packaging cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これらの原価コンポーネントには、出荷コスト、取扱コスト、梱包コストなどがあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A combination of these costs is calculated to determine the fulfillment location.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これらの原価の組み合わせを計算して、フルフィルメント場所を決定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Microsoft Dynamics 365 for Retail の配分済み注文の管理 (DOM) の最初のイテレーションで、注文をフルフィルメント場所に割り当てることが最適化されている場合、このイテレーションでは距離のみが考慮されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Although distance can be correlated with cost, it isn't the same as cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">距離は原価に関連付けることができますが、原価と同じではありません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">たとえば、翌日配送方式では、同じ距離に対して、3 日間配送または 7 日間配送の場合より費用が多くかかります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">原価コンフィギュレーション機能を使用すると、小売業者は、注文明細行のフルフィルメントに最適な場所を決定するために計算および考慮する追加の原価コンポーネントを定義および構成することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">原価コンポーネントが構成されると、DOM ソルバーはこれらの原価定義のみを使用して、注文のフルフィルメントに最適な場所を決定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It doesn't consider the distance component as a cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">DOM ソルバーは距離コンポーネントをコストと見なしません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">ただし、原価コンポーネントが構成されていない場合、DOM ソルバーは距離コンポーネントをコストとして使用し、注文のフルフィルメントに最適な場所を決定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up cost components</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">原価コンポーネントの設定</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Two major cost component types can be defined in the system: <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Other<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">システムでは、<bpt id="p1">**</bpt>出荷<ept id="p1">**</ept> と <bpt id="p2">**</bpt>その他<ept id="p2">**</ept> の 2 つの主要な原価コンポーネント タイプを定義できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Both cost component types support multiple calculation bases, as shown in the following table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">両方の原価コンポーネント タイプは、次の表に示すように、複数の計算基準をサポートします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Cost component type</source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match">原価コンポーネント タイプ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Calculation basis</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">計算基準</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Shipping</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">出荷</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Simple</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">簡易</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Tiered</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">階層化</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Other</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">その他</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Sales order</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">販売注文</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Sales line</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">販売明細行</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Location</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">保管場所</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Shipping cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">出荷原価コンポーネント タイプ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and a calculation basis for shipping costs.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このセクションでは、<bpt id="p1">**</bpt>出荷<ept id="p1">**</ept> 原価コンポーネント タイプと出荷コストの計算基準の各組み合わせを設定する方法について説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It also explains how the DOM solver uses each combination.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">また、DOM ソルバーで各組み合わせがどのように使用されるかについても説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Cost component type = Shipping and Calculation basis = Simple</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">原価コンポーネント タイプ = 出荷と計算基準 = 簡易</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Simple<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>出荷<ept id="p1">**</ept> 原価コンポーネント タイプと計算基準 <bpt id="p2">**</bpt>簡易<ept id="p2">**</ept> の組み合わせを使用する場合、荷渡方法の出荷コストは均一料金または距離に基づいて決定されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must set up the following fields for this combination:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この組み合わせに対して、次のフィールドを設定する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>原価係数<ept id="p1">**</ept> – 原価係数の固有識別子を入力します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source><target logoport:matchpercent="78" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>説明<ept id="p1">**</ept> – 原価係数の名前と説明を入力します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>開始日<ept id="p1">**</ept> および <bpt id="p2">**</bpt>終了日<ept id="p2">**</ept> – これらのフィールドを使用して、特定の日付範囲の原価係数を制限することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これらのフィールドを空白のままにすると、原価係数は無期限に有効になります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>有効<ept id="p1">**</ept> – 原価係数が有効かどうかを示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">DOM は、フルフィルメント プロファイルに関連付けられている有効な原価係数のみを考慮します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>会社<ept id="p1">**</ept> – 原価係数をコンフィギュレーションする対象の法人を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>All lines of the calculation criteria must be for the same legal entity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">計算基準のすべての明細行は、同じ法人に対して設定する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>荷渡方法<ept id="p1">**</ept> – 原価をコンフィギュレーションする対象の荷渡方法を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>計算タイプ<ept id="p1">**</ept> – 特定の荷渡方法に対して原価を計算する方法を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Two calculation types are supported:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の 2 つの計算タイプがサポートされます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>固定<ept id="p1">**</ept> – 荷渡方法に均一料金が使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この計算タイプを選択した場合は、<bpt id="p1">**</bpt>原価<ept id="p1">**</ept> フィールドによって均一料金が定義されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Per-distance unit<ept id="p1">**</ept> – The cost for the mode of delivery is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>距離単位ごと<ept id="p1">**</ept> – 荷渡方法に対するコストは、<bpt id="p2">**</bpt>原価<ept id="p2">**</ept> フィールドで指定された原価価値に配送先住所と保管場所の間の距離を乗じて計算されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>原価<ept id="p1">**</ept> – 荷渡方法の原価を計算するために、<bpt id="p2">**</bpt>計算タイプ<ept id="p2">**</ept> フィールドと組み合わせて使用される原価価値を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Cost component type = Shipping and Calculation basis = Tiered</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">原価コンポーネント タイプ = 出荷と計算基準 = 階層化</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Tiered<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>出荷<ept id="p1">**</ept> 原価コンポーネント タイプと計算基準 <bpt id="p2">**</bpt>階層化<ept id="p2">**</ept> の組み合わせを使用する場合、荷渡方法の出荷費用は均一料金または距離に基づいて決定されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>However, in this combination, the distance is based on a tiered range of distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ただし、この組み合わせでは、距離は階層化された距離の範囲に基づきます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">この組み合わせに対して、次のフィールドを設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>原価係数<ept id="p1">**</ept> – 原価係数の固有識別子を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>説明<ept id="p1">**</ept> – 原価係数の名前と説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Default cost<ept id="p1">**</ept> – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>既定の原価<ept id="p1">**</ept> – 配送先住所と保管場所の間の距離が荷渡方法の階層化された距離の範囲に含まれない場合、荷渡方法に使用される原価を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>開始日<ept id="p1">**</ept> および <bpt id="p2">**</bpt>終了日<ept id="p2">**</ept> – これらのフィールドを使用して、特定の日付範囲の原価係数を制限することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">これらのフィールドを空白のままにすると、原価係数は無期限に有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>有効<ept id="p1">**</ept> – 原価係数が有効かどうかを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM は、フルフィルメント プロファイルに関連付けられている有効な原価係数のみを考慮します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>会社<ept id="p1">**</ept> – 原価係数をコンフィギュレーションする対象の法人を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>All lines of the calculation criteria must be for the same legal entity.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">計算基準のすべての明細行は、同じ法人に対して設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>荷渡方法<ept id="p1">**</ept> – 原価をコンフィギュレーションする対象の荷渡方法を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Distance type<ept id="p1">**</ept> – Specify whether the tiered distance definition is an aerial distance or a road distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>距離タイプ<ept id="p1">**</ept> – 階層化された距離定義が空路の距離であるか、陸路の距離であるかを指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Distance units<ept id="p1">**</ept> – Specify the unit that the tiered distance is measured in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>距離単位<ept id="p1">**</ept> – 階層化された距離を測定する単位を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Distance from<ept id="p1">**</ept> – Specify the start range for the tiered distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>開始距離<ept id="p1">**</ept> – 階層化された距離の開始範囲を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>Distance to<ept id="p1">**</ept> – Specify the end range for the tiered distance.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>終了距離<ept id="p1">**</ept> – 階層化された距離の終了範囲を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>計算タイプ<ept id="p1">**</ept> – 特定の荷渡方法と階層化された距離に対してコストを計算する方法を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Two calculation types are supported:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">次の 2 つの計算タイプがサポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>固定<ept id="p1">**</ept> – 荷渡方法に均一料金が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">この計算タイプを選択した場合は、<bpt id="p1">**</bpt>原価<ept id="p1">**</ept> フィールドによって均一料金が定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Per distance unit<ept id="p1">**</ept> – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>距離単位ごと<ept id="p1">**</ept> – 荷渡方法と階層化された距離に対するコストは、<bpt id="p2">**</bpt>原価<ept id="p2">**</ept> フィールドで指定された原価価値に配送先住所と保管場所の間の距離を乗じて計算されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>原価<ept id="p1">**</ept> – 荷渡方法の原価を計算するために、<bpt id="p2">**</bpt>計算タイプ<ept id="p2">**</ept> フィールドと組み合わせて使用される原価価値を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you define tiered distances, the system validates that there are no missing or overlapping distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">階層化された距離を定義すると、欠落または重複する距離がないことが検証されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The distance type that is used for a mode of delivery must be the same across all the tiered distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">荷渡方法に使用される距離タイプは、階層化されたすべての距離にわたって同一である必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Other cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">その他原価コンポーネント タイプ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and an other cost type for non-shipping costs.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">このセクションでは、<bpt id="p1">**</bpt>その他<ept id="p1">**</ept> 原価コンポーネント タイプと出荷以外のコストのその他の原価タイプの各組み合わせを設定する方法について説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>It also explains how the DOM solver uses each combination.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">また、DOM ソルバーで各組み合わせがどのように使用されるかについても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Cost component type = Other and Other cost type = Sales order</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">原価コンポーネント タイプ = その他とその他の原価タイプ = 販売注文</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales order<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>その他<ept id="p1">**</ept> 原価コンポーネント タイプとその他の原価タイプ <bpt id="p2">**</bpt>販売注文<ept id="p2">**</ept> の組み合わせは、販売注文レベルでの出荷以外のコストを定義するために使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">この組み合わせに対して、次のフィールドを設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>原価係数<ept id="p1">**</ept> – 原価係数の固有識別子を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>説明<ept id="p1">**</ept> – 原価係数の名前と説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>開始日<ept id="p1">**</ept> および <bpt id="p2">**</bpt>終了日<ept id="p2">**</ept> – これらのフィールドを使用して、特定の日付範囲の原価係数を制限することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">これらのフィールドを空白のままにすると、原価係数は無期限に有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>有効<ept id="p1">**</ept> – 原価係数が有効かどうかを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM は、フルフィルメント プロファイルに関連付けられている有効な原価係数のみを考慮します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>原価<ept id="p1">**</ept> – 販売注文レベルでの出荷以外のコストの原価価値を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Cost component type = Other and Other cost type = Sales line</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">原価コンポーネント タイプ = その他とその他の原価タイプ = 販売明細行</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales line<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order line level.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>その他<ept id="p1">**</ept> 原価コンポーネント タイプとその他の原価タイプ <bpt id="p2">**</bpt>販売明細行<ept id="p2">**</ept> の組み合わせは、販売注文明細行レベルでの出荷以外のコストを定義するために使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">この組み合わせに対して、次のフィールドを設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>原価係数<ept id="p1">**</ept> – 原価係数の固有識別子を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>説明<ept id="p1">**</ept> – 原価係数の名前と説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>開始日<ept id="p1">**</ept> および <bpt id="p2">**</bpt>終了日<ept id="p2">**</ept> – これらのフィールドを使用して、特定の日付範囲の原価係数を制限することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">これらのフィールドを空白のままにすると、原価係数は無期限に有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>有効<ept id="p1">**</ept> – 原価係数が有効かどうかを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM は、フルフィルメント プロファイルに関連付けられている有効な原価係数のみを考慮します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order line level.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>原価<ept id="p1">**</ept> – 販売注文明細行レベルでの出荷以外のコストの原価価値を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Cost component type = Other and Other cost type = Location</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">原価コンポーネント タイプ = その他とその他の原価タイプ = 保管場所</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Location<ept id="p2">**</ept> other cost type is used to define non-shipping costs for a group of locations or an individual location.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>その他<ept id="p1">**</ept> 原価コンポーネント タイプとその他の原価タイプ <bpt id="p2">**</bpt>保管場所<ept id="p2">**</ept> の組み合わせは、保管場所のグループまたは個々の場所に対する出荷以外のコストを定義するために使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">この組み合わせに対して、次のフィールドを設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>原価係数<ept id="p1">**</ept> – 原価係数の固有識別子を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>説明<ept id="p1">**</ept> – 原価係数の名前と説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>開始日<ept id="p1">**</ept> および <bpt id="p2">**</bpt>終了日<ept id="p2">**</ept> – これらのフィールドを使用して、特定の日付範囲の原価係数を制限することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">これらのフィールドを空白のままにすると、原価係数は無期限に有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>有効<ept id="p1">**</ept> – 原価係数が有効かどうかを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM は、フルフィルメント プロファイルに関連付けられている有効な原価係数のみを考慮します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Fulfillment group<ept id="p1">**</ept> – Specify the group of locations that the non-shipping cost is defined for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>フルフィルメント グループ<ept id="p1">**</ept> – 出荷以外のコストを定義する対象の保管場所のグループを指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Fulfillment location<ept id="p1">**</ept> – Specify the location that the non-shipping cost is defined for.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>フルフィルメント場所<ept id="p1">**</ept> – 出荷以外のコストを定義する対象の保管場所を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">場所に基づく計算基準では、同じ明細行で、フルフィルメント グループとフルフィルメント場所を指定することはできません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>原価<ept id="p1">**</ept> – フルフィルメント グループ レベルまたはフルフィルメント場所レベルで、出荷以外のコストの原価価値を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">DOM でこれらの原価を実行時に考慮するには、関連するフルフィルメント プロファイルに原価係数を追加する必要があります。</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>
<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="client-api-design-overview.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>client-api-design-overview.410dff.97a1279bab499d72897ef3d71898cbcd6d23dcb5.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>97a1279bab499d72897ef3d71898cbcd6d23dcb5</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\mobile-apps\platform\scenarios\client-api-design-overview.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Client-side design APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント側の設計 API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides an overview of the client-side design APIs and includes recommendations for using them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、クライアント側での設計のための API の概要と、それらの使用に関する推奨事項について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Client-side design APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント側の設計 API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides an overview of the application programming interfaces (APIs) for client-side design and includes recommendations for using them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、クライアント側での設計のためのプリケーション プログラミング インターフェイス (API) の概要と、それらの使用に関する推奨事項について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Terminology</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">用語</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The following list includes some frequently used terms that apply to the client-side design APIs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のリストには、クライアント側の設計 API に適用される用語がいくつか含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source><bpt id="p1">**</bpt>Design<ept id="p1">**</ept> – A property that can optionally be specified on a Page, Action, or other component object to override its default design.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept> - 既定デザインを上書きするためにページ、アクション、またはその他のコンポーネント オブジェクトで必要に応じて指定できるプロパティ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source><bpt id="p1">**</bpt>Component<ept id="p1">**</ept> – A component can be one of four types:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コンポーネント<ept id="p1">**</ept> - コンポーネントには、次の 4 つのタイプがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">**</bpt>Block container<ept id="p1">**</ept> (default) – A container that has CSS block behaviors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブロック コンテナー<ept id="p1">**</ept> (既定) - CSS ブロック動作を持つコンテナーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>(In other words, the container is equivalent to an element that has a CSS <bpt id="p1">**</bpt>display: block<ept id="p1">**</ept> style declaration.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(つまり、コンテナーは、CSS <bpt id="p1">**</bpt>display: block<ept id="p1">**</ept> スタイル申告を持つ要素に相当します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source><bpt id="p1">**</bpt>Flex container<ept id="p1">**</ept> – A container that has CSS flex behaviors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フレックス コンテナー<ept id="p1">**</ept> – CSS フレックス動作のあるコンテナー。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>(In other words, the container is equivalent to an element that has a CSS <bpt id="p1">**</bpt>display: flex<ept id="p1">**</ept> style declaration.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(つまり、コンテナーは、CSS <bpt id="p1">**</bpt>display: flex<ept id="p1">**</ept> スタイル申告を持つ要素に相当します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>Control reference<ept id="p1">**</ept> – A component that refers to a control that exists in the static metadata (XML) of the Page or Action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントロール参照<ept id="p1">**</ept> - ページまたはアクションの静的メタデータ (XML) に存在するコントロールを参照するコンポーネント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>New control<ept id="p1">**</ept> – A component that instantiates a new control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しいコントロール<ept id="p1">**</ept> – 新しいコントロールをインスタンス化するコンポーネント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>(In other words, the control doesn't already exist in the static metadata [XML] of the Page or Action.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(つまり、コントロールは、ページまたはアクションの静的メタデータ [XML] にはまだ存在しません。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>A component is represented in the design by a JavaScript Object Notation (JSON) object, and the properties of this JSON object represent the properties of the component.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネントは JavaScript Object Notation (JSON) オブジェクトによってデザイン内に表され、この JSON オブジェクトのプロパティは、コンポーネントのプロパティを表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Almost every JSON object in the design property hierarchy is a component.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイン プロパティ階層のほとんどすべての JSON オブジェクトはコンポーネントです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Item<ept id="p1">**</ept> – A component that is nested in a container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>項目<ept id="p1">**</ept> – コンテナーに入れ子にされたコンポーネント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept> – Several types of properties can be set on a component:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> – コンポーネントで複数のタイプのプロパティを設定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Container-specific</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナー固有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Item-specific</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">品目固有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Control-specific</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール固有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>List-specific</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リスト固有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Generic (non-specific)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般 (不特定)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Properties are specified as key-value pairs on the component's JSON object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティは、コンポーネントの JSON オブジェクトのキーと値のペアとして指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The properties that are applicable depend on the type of component that the property is applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適用可能なプロパティは、プロパティが適用されるコンポーネントのタイプによって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For properties that have a predefined list of possible values, the first value that is shown in the documentation is the property's default value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用可能な値の定義済リストを持つプロパティについては、ドキュメントで示されている最初の値がプロパティの既定値です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In most cases, if you don't specify a property at all (that is, if you omit the property from the JSON object), the property behaves as if you had set its default value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの場合、プロパティをまったく指定していない (つまり、JSON オブジェクトからのプロパティを省略する) 場合、プロパティは既定値を設定していた場合と同じように動作します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Generic properties can be applied to all component types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的なプロパティは、すべてのコンポーネントのタイプに適用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When you specify properties, follow these guidelines:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティを指定するときは、次のガイドラインに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You should not enclose property names in quotation marks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ名は引用符で囲まないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>You must enclose all property values in double quotation marks, unless the documentation specifies otherwise.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメントでそれ以外が指定されない限り、すべてのプロパティ値を二重引用符で囲む必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Inheritance<ept id="p1">**</ept> – If a color, font size, or font weight is applied to a control, all descendant controls inherit the same property, unless they are reassigned.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>継承<ept id="p1">**</ept> – コントロールに色、フォントサイズ、またはフォントの太さが適用されている場合、すべての子孫コントロールは再割り当てされない限り、同じプロパティを継承します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If padding is applied to a control, it's inherited by the item (non-container) descendants of the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールにスペースを適用する場合は、コントロールの品目 (非コンテナー) 子孫によって継承されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>No other properties are inherited.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のプロパティは継承されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Using design APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設計 API の使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The following code is a modified segment of business logic code from a Reservation Management example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードは、予約管理の例のビジネス ロジック コードの変更されたセグメントです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Specifically, this code is from a variable that specifies the design for a reservation details page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">具体的には、このコードは、引当の詳細ページのデザインを指定する変数から取得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Comments are included in the code to highlight a few possibilities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コメントはコードに含まれており、いくつかの可能性を強調します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Any color, font size, or font weight that is applied to a control is also applied to all children of that control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールに適用される色、フォント サイズ、またはフォントの太さはコントロールのすべての子にも適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Padding is inherited by non-container children.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">埋め込みは、コンテナー以外の子によって継承されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>No other properties are inherited.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のプロパティは継承されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Containers include lists, pages, groups, and parts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーにはリスト、ページ、グループ、およびパーツが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>After a control is created that doesn't have any children or items, the control name just has to be written in quotation marks (see <bpt id="p1">**</bpt>FMCustomer<ph id="ph1">\_</ph>FullName<ept id="p1">**</ept> in the following code).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">子または品目を持たないコントロールを作成した後、コントロール名は引用符で囲む必要があります (次のコードの <bpt id="p1">**</bpt>FMCustomer<ph id="ph1">\_</ph>FullName<ept id="p1">**</ept> を参照してください)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>However, if any customization will be applied to that control, the code must be blocked, and the <bpt id="p1">**</bpt>name<ept id="p1">**</ept> label must be used (see <bpt id="p2">**</bpt>FMCustomer<ph id="ph1">\_</ph>Image<ept id="p2">**</ept> in the following code).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、任意のカスタマイズがコントロールに適用される場合、コードはブロックされる必要があり、<bpt id="p1">**</bpt>名前<ept id="p1">**</ept>ラベルを使用する必要があります (次のコードで <bpt id="p2">**</bpt>FMCustomer<ph id="ph1">\_</ph>画像<ept id="p2">**</ept>を参照してください)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The following illustration shows the customer image, customer name, font, background color, and so on, that preceding code produces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、前のコードで生成された顧客画像、顧客名、フォント、背景色などを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Sample image</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプル画像</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
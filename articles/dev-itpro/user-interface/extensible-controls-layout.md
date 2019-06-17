<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extensible-controls-layout.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extensible-controls-layout.e92fa8.7d04dd393685d4e4a69cee6a3b4983b1dc7bdeca.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>7d04dd393685d4e4a69cee6a3b4983b1dc7bdeca</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\extensible-controls-layout.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extensible control layout guidelines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なコントロール レイアウトのガイドライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article provides guidelines that you should follow when you specify the layout and sizing of extensible controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、拡張可能なコントロールのレイアウトとサイズを指定するときに従うガイドラインについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Extensible control layout guidelines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なコントロール レイアウトのガイドライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article provides guidelines that you should follow when you specify the layout and sizing of extensible controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、拡張可能なコントロールのレイアウトとサイズを指定するときに従うガイドラインについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Dos and don'ts for achieving the desired layout</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的のレイアウトを実現するための注意事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Don't use the layout classes on your control directly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールのレイアウト クラスを直接使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>(For example, <bpt id="p1">**</bpt>layout-container<ept id="p1">**</ept> and <bpt id="p2">**</bpt>layout-horizontal<ept id="p2">**</ept> are classes that you might see on controls in the DOM.) Instead, use the layout binding handlers to apply these classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(たとえば、<bpt id="p1">**</bpt>layout-container<ept id="p1">**</ept> および <bpt id="p2">**</bpt>layout-horizontal<ept id="p2">**</ept> は、DOM のコントロールに表示されるクラスです。) 代わりに、レイアウト バインディング ハンドラーを使用して、これらのクラスを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Internet Explorer uses a different layout framework, and to add some inline styles to elements, this framework requires the extra binding information that the handlers provide.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer は異なるレイアウト フレームワークを使用しており、要素にいくつかのインライン スタイルを追加するには、このフレームワークにハンドラーが提供する予備のバインディング情報が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Therefore, make sure that the classes are <bpt id="p1">**</bpt>not<ept id="p1">**</ept> hard-coded into the controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、クラスがコントロールにハードコードされて<bpt id="p1">**</bpt>いない<ept id="p1">**</ept>ことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Don't use absolute positioning (<bpt id="p1">**</bpt>position: absolute<ept id="p1">**</ept> and <bpt id="p2">**</bpt>top<ept id="p2">**</ept><ph id="ph1">/</ph><bpt id="p3">**</bpt>bottom<ept id="p3">**</ept><ph id="ph2">/</ph><bpt id="p4">**</bpt>left<ept id="p4">**</ept><ph id="ph3">/</ph><bpt id="p5">**</bpt>right<ept id="p5">**</ept> positions) for elements that are children of a container that uses the layout binding handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レイアウト バインディング ハンドラーを使うコンテナーの子である要素に、絶対配置 (<bpt id="p1">**</bpt>position: absolute<ept id="p1">**</ept> and <bpt id="p2">**</bpt>top<ept id="p2">**</ept><ph id="ph1">/</ph><bpt id="p3">**</bpt>bottom<ept id="p3">**</ept><ph id="ph2">/</ph><bpt id="p4">**</bpt>left<ept id="p4">**</ept><ph id="ph3">/</ph><bpt id="p5">**</bpt>right<ept id="p5">**</ept> positions) を使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Absolute positioning of these elements prevents the CSS classes that are applied from laying things out correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの要素の絶対配置は、正しく物事をレイアウトすることに適用される CSS クラスを妨げます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Be careful about using <bpt id="p1">**</bpt>width: 100%<ept id="p1">**</ept> and <bpt id="p2">**</bpt>height: 100%<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>幅: 100%<ept id="p1">**</ept> と<bpt id="p2">**</bpt>高さ: 100%<ept id="p2">**</ept> の使用には注意が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>These settings might not always work when they are combined with our layout CSS classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの設定は、レイアウト CSS クラスと組み合わせて使用すると、必ずしも機能しない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>If you want filling behavior, it's a good idea to use the <bpt id="p1">**</bpt>$dyn.layout.Size.available<ept id="p1">**</ept> option of the sizing binding handler instead.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">塗りつぶし動作を使用する場合、代わりにサイズ変更バインディング ハンドラーの <bpt id="p1">**</bpt>$dyn.layout.Size.available<ept id="p1">**</ept> オプションを使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Layout binding handlers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レイアウト バインディング ハンドラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Layout</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レイアウト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Used to apply <bpt id="p1">**</bpt>ArrangeMethod<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Columns<ept id="p2">**</ept> attributes to containers Options: <bpt id="p3">**</bpt>arrangeMethod<ept id="p3">**</ept>, <bpt id="p4">**</bpt>Columns<ept id="p4">**</ept>, <bpt id="p5">**</bpt>Children<ept id="p5">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ArrangeMethod<ept id="p1">**</ept> 属性と <bpt id="p2">**</bpt>Columns<ept id="p2">**</ept> 属性をコンテナーの <bpt id="p3">**</bpt>arrangeMethod<ept id="p3">**</ept>、<bpt id="p4">**</bpt>Columns<ept id="p4">**</ept>、<bpt id="p5">**</bpt>Children<ept id="p5">**</ept> オプションに適用するのに使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>ArrangeMethod</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ArrangeMethod</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>$dyn.layout.ArrangeMethod.vertical</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$dyn.layout.ArrangeMethod.vertical</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>$dyn.layout.ArrangeMethod.horizontalLeft</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$dyn.layout.ArrangeMethod.horizontalLeft</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>$dyn.layout.ArrangeMethod.horizontalWrap</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$dyn.layout.ArrangeMethod.horizontalWrap</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>$dyn.layout.ArrangeMethod.horizontalRight</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$dyn.layout.ArrangeMethod.horizontalRight</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>$dyn.layout.ArrangeMethod.none (No layout CSS classes should be applied to the element.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$dyn.layout.ArrangeMethod.none (レイアウト CSS クラスは要素に適用されません。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Columns</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>$dyn.layout.Columns.fill<ept id="p1">**</ept> – Use this constant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>$dyn.layout.Columns.fill<ept id="p1">**</ept> - この定数を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Depending on the control, either "fill" and "balanced" columns are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールに応じて、「塗りつぶし」と「バランス」のいずれかの列が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">**</bpt>$dyn.layout.Columns.fixed<ept id="p1">**</ept> – Use a fixed value, such as <bpt id="p2">**</bpt>1<ept id="p2">**</ept>, <bpt id="p3">**</bpt>2<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>3<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>$dyn.layout.Columns.fixed<ept id="p1">**</ept> - <bpt id="p2">**</bpt>1<ept id="p2">**</ept>、<bpt id="p3">**</bpt>2<ept id="p3">**</ept>、<bpt id="p4">**</bpt>3<ept id="p4">**</ept> のような固定値を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Children</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Use **$data.Children **if the content handlers (append, replace) will be used to append children through this container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコンテナを介して子を追加するためにコンテンツ ハンドラー (追加、置換) を使用する場合は、**$ data.Children** を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>It should be used only if this control is a container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントロールがコンテナーである場合にのみ使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Example usage:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>使用例:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Sizing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイズ変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Height/width</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高さ/幅</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>$dyn.layout.Size.available (SizeToAvailable)<ept id="p1">**</ept> – Fill the available space in that direction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>$dyn.layout.Size.available (SizeToAvailable)<ept id="p1">**</ept> - その方向に使用可能領域を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>$dyn.layout.Size.content (SizeToContent)<ept id="p1">**</ept> – Size to the contents in that direction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>$dyn.layout.Size.content (SizeToContent)<ept id="p1">**</ept> - その方向のコンテンツへのサイズ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>$dyn.layout.Size.fixed (Manual)<ept id="p1">**</ept> – A fixed pixel value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>$dyn.layout.Size.fixed (手動)<ept id="p1">**</ept> - 固定ピクセル値。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Example usage:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>使用例:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Things to note about the sizing binding handler:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サイズ変更バインディング ハンドラーに関する注意事項:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>When you use the sizing binding handler in combination with the <bpt id="p1">**</bpt>SizeToAvailable<ept id="p1">**</ept> option (<bpt id="p2">**</bpt>$dyn.layout.Size.available<ept id="p2">**</ept>), the layout binding handler must be used on the parent <bpt id="p3">**</bpt><ph id="ph1">&amp;lt;</ph>div<ph id="ph2">&amp;gt;</ph><ept id="p3">**</ept>/DOM element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイジング バインディング ハンドラーを <bpt id="p1">**</bpt>SizeToAvailable<ept id="p1">**</ept> オプション (<bpt id="p2">**</bpt>$dyn.layout.Size.available<ept id="p2">**</ept>) と組み合わせて使用するとき、レイアウト バインディング ハンドラーを親の <bpt id="p3">**</bpt><ph id="ph1">&amp;lt;</ph>div<ph id="ph2">&amp;gt;</ph><ept id="p3">**</ept>/DOM 要素使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>This is how we know which axis to fill along (horizontal or vertical).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、どの軸 (水平または垂直方向) に沿って満たされるかがわかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Should you use layout/sizing handlers or set the properties directly?<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レイアウト/サイズ ハンドラーを使用すべきですか、または直接プロパティを設定する必要がありますか。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>If your extensible control inherits from a client control (such as Group or PivotItem), you won't use the binding handlers directly on the <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>div<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> that is associated with that control, because the binding is already there.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能コントロールがクライアント コントロール (グループまたは PivotItem など) から継承している場合、バインディングが既に存在するため、直接そのコントロールに関連付けられている <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>div<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> でバインディング ハンドラーを使用しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>However, you might have to set the properties as you want them directly in the <bpt id="p1">**</bpt>data-dyn-bind<ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>data-dyn-bind<ept id="p1">**</ept> 属性にプロパティが直接入れるように、プロパティを設定する必要がある場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>Example:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例 :<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>FAQ</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">よく寄せられる質問</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Is my control being laid out as expected?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自分のコントロールが期待どおりにレイアウトされているか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>A good way to tell is to inspect the element and look for the desired classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指示に適した方法は、要素を検査し、目的のクラスを探すことです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Layout classes to look for, depending on the options applied:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適用されるオプションに応じて検索するレイアウト クラス:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>layout-container</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">layout-container</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>layout-vertical</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">layout-vertical</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>layout-horizontal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">layout-horizontal</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Sizing classes to look for:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索するクラスのサイズ設定:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>For <bpt id="p1">**</bpt>$dyn.layout.Size.available<ept id="p1">**</ept>,  you should see either <bpt id="p2">**</bpt>fill-width<ept id="p2">**</ept> or <bpt id="p3">**</bpt>fill-height<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>$dyn.layout.Size.available<ept id="p1">**</ept> で、<bpt id="p2">**</bpt>入力幅<ept id="p2">**</ept>または<bpt id="p3">**</bpt>入力高さ<ept id="p3">**</ept>のいずれかを表示する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>For manual size, you should see either <bpt id="p1">**</bpt>fixed-height<ept id="p1">**</ept> or <bpt id="p2">**</bpt>fixed-width<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動サイズについては、<bpt id="p1">**</bpt>固定高さ<ept id="p1">**</ept>または<bpt id="p2">**</bpt>固定幅<ept id="p2">**</ept>のいずれかを表示する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>For <bpt id="p1">**</bpt>$dyn.layout.Size.content<ept id="p1">**</ept>, there should be no extra classes, and the manual height/width should be specified inline on the element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>$dyn.layout.Size.content<ept id="p1">**</ept> では、追加のクラスは存在すべきでなく、手動の高さと幅は要素で特定されたインラインである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>If these classes don't appear as you expected, examine the usage of your binding handlers, and make sure that you've read through the list of dos and don'ts on this page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのクラスが予期したとおりに表示されない場合、拘束力のあるハンドラーの使用状況を確認し、このページの注意事項の一覧を読んだことを確認します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
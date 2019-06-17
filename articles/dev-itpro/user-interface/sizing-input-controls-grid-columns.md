<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="sizing-input-controls-grid-columns.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>sizing-input-controls-grid-columns.c4e6fd.2becb4ad5e048619a1a7328778540ae8506cbfc8.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>2becb4ad5e048619a1a7328778540ae8506cbfc8</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\sizing-input-controls-grid-columns.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Input controls and grid column sizes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入力コントロールとグリッド列のサイズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes how to create a consistent look and feel for forms by controlling the size of controls and grids.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、コントロールとグリッドのサイズを制御することによってフォームの一貫した概観を作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Input controls and grid column sizes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入力コントロールとグリッド列のサイズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article describes how to create a consistent look and feel for forms by controlling the size of controls and grids.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、コントロールとグリッドのサイズを制御することによってフォームの一貫した概観を作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Many frameworks offer complete freedom over the width of input controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くのフレームワークでは、入力コントロールの幅が完全に自由にできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>However, that level of freedom can lead to inconsistent presentation of data and a non-uniform layout for similar forms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、その自由度は、データの一貫しない表示および同様のフォームの一様でないレイアウトにつながる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For example, the customer name in one form might show 10 characters of information, whereas the customer name in another form might show 20 characters of information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、1 つのフォームでの顧客名は情報の 10 文字を表示する可能性があり、別のフォームでの顧客名は情報の 20 文字を表示する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To provide streamlined, easy-to-read interfaces, discrete sizing helps guarantee consistent presentation of data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">合理化された読みやすいインターフェイスを提供するために、個別のサイズ変更により、データを一貫した形で表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The introduction of discrete sizing is a significant change to the basic input controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">個別のサイズ変更の導入は、基本的な入力コントロールにとって重要な変更です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The control framework attempts to provide a fresh, clean user experience that provides simplicity and consistency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール フレームワークは、シンプルさと一貫性を提供する新鮮でクリーンなユーザー エクスペリエンスを提供しようとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>As part of an attempt to provide consistent and uniform layout of forms, each input control is sized to one of four sizes: extra-small (XS), small (S), medium (M), or large (L).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームの均一なレイアウトと一貫性を提供する試行の一環として、各入力コントロールは超小型 (XS)、小型 (S)、中型 (M)、または大型 (L) の 4 種類のサイズのいずれか 1 つに調整されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>These sizes are determined by inspecting the explicitly specified width in the <bpt id="p1">**</bpt>DisplayLength<ept id="p1">**</ept> property of the control or the corresponding extended data type (EDT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのサイズは、コントロールの <bpt id="p1">**</bpt>DisplayLength<ept id="p1">**</ept> プロパティまたは対応する拡張データ型 (EDT) で明示的に指定された幅を調べることによって決定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Sizing grid columns</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッド列のサイズを変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The approach that Dynamic 365 for Finance and Operations takes to column sizing in a grid control differs slightly from the legacy algorithm, which tried to provide an initial appealing presentation for each grid, based partly on the contents of the first page of data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="1">Dynamics 365 for Finance and Operations</ph> が、グリッド コントロールの列幅を調整する場合のアプローチは、従来のアルゴリズムとは少し異なっています。従来のアルゴリズムでは、データの最初のページの内容に部分的に基づいて、最初に各グリッドを魅力的に表示しようとしていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The new approach disregards the contents of the first page of data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいアプローチでは、データの最初のページの内容は無視されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Instead, the end user decides which columns are most important to view and the ideal viewing width for each of those columns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、エンド ユーザーは最も重要な表示すべき列および各列の理想的な表示幅を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>By using personalization, each user can change the width of grid columns, and the client keeps track of that user's preference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">個人用設定を使用することにより、各ユーザーはグリッドの列の幅を変更でき、クライアントはそのユーザーの基本設定を追跡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In the new, simplified approach, the default column sizing is based on 75 percent of the base input control sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい簡略化されたアプローチでは、既定の列のサイズ変更は基準の入力コントロールのサイズ変更の 75% に基づきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In most cases, we recommended that developers not override the default sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの場合、開発者は既定のサイズ変更をオーバーライドしないことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>However, if you must resize the column width programmatically or in the model, see the next two sections of this article for guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、プログラムでまたはモデルで列幅のサイズを変更する必要がある場合、ガイダンスのこの記事の次の 2 つのセクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Discrete sizing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">個別のサイズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Size</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Character range</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字の範囲</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Size in pixels (px)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ピクセル (px) 単位のサイズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>XS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">XS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>0–5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">0-5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>60</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">60</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>S</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">S</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>6–15</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">6-15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>120</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">120</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>M</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">M</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>16–30</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">16-30</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>180</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">180</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>L</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">L</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><ph id="ph1">&amp;gt;</ph>30</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[<ph id="ph1">&amp;gt;</ph>] 30</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>240</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">240</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The explicit number of pixels will likely vary over time as the user interface evolves.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> 明示的なピクセル数は、ユーザー インターフェイスの発展に伴って、時間の経過と共に変化する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Developers should not rely on explicit pixel sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は明示的なピクセル サイズに頼るべきではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Forcing a desired discrete size</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な個別のサイズの強制</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>As the previous table shows, if you change the width of a grid-hosted control from 6 characters to 15 characters, you don't affect the width of the column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前の表で示すように、グリッド ホスト コントロールの幅を 6 文字から 15 文字に変更すると、列の幅には影響しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The layout engine gives the same width to all control widths that are in the 6-to-15-character range, because controls in this range are considered small (S).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レイアウト エンジンは、6〜15 文字の範囲内のすべてのコントロール幅に同じ幅を与えます。これは、この範囲のコントロールが小さい (S) とみなされるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source> If you want to extend the control to medium (M) size, the width value must be set to a value that is more than 16 characters and less than 31 characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">中規模な (M) サイズにコントロールを拡張する場合は、幅の値は 16 文字以上 31 文字未満の値に設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>For guidance about how to size input controls, see the following table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入力コントロールの区分する方法の指針については、次の表を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source> In some cases, the use of a form pattern will override or hide developer-defined sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、フォーム パターンの使用は開発者によって定義されたサイズ変更をオーバーライドまたは非表示にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>DisplayLengthMode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DisplayLengthMode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Auto</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Use the kernel’s default value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カーネルの既定値を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>DisplayLengthMode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DisplayLengthMode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Fixed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始日固定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Use the developer-defined <bpt id="p1">**</bpt>DisplayLength<ept id="p1">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者定義の <bpt id="p1">**</bpt>DisplayLength<ept id="p1">**</ept> 値を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>WidthMode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WidthMode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Auto</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Use the kernel’s default sizing behavior.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カーネルの既定のサイズ変更ビヘイビアーを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>WidthMode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WidthMode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Fixed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始日固定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Use the developer-defined <bpt id="p1">**</bpt>Width<ept id="p1">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者定義の <bpt id="p1">**</bpt>Width<ept id="p1">**</ept> 値を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>WidthMode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WidthMode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Column Width</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列の幅</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Use size-to-parent behavior.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイズ-親のビヘイビアーを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>DisplayLength</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DisplayLength</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>N</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The developer-defined control width, which is specified in characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字で指定されている、開発者が定義したコントロールの幅。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>(Values are mapped to the sizing groups that are listed in the previous table.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(値は、前の表にリストされているサイズ グループにマップされます。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Width</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">幅</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>N</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The developer-defined control width, which is specified in pixels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ピクセル単位で指定されている、開発者が定義したコントロールの幅。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
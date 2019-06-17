<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extensible-enums.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extensible-enums.26ccb5.04c1a7dd5430fbb0476ad0889dbf8d2a2e7a07e2.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>04c1a7dd5430fbb0476ad0889dbf8d2a2e7a07e2</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\extensible-enums.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Write extensible enums</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能列挙の書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to write extensible enums.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張可能列挙を書き込む方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Write extensible enums</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能列挙の書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>An enumeration (enum) is made extensible by setting the following enum properties:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙を拡張可能にするには、以下の列挙プロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Is Extensible = True</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Is Extensible = True</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>UseEnumValue = No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UseEnumValue = No</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>If you set these properties, downstream implementors can extend the enum with more elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのプロパティを設定する場合、下位の実装者がより多くの要素で列挙を拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The values of the elements are determined at deployment time and won't be identical across systems.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要素の値は、展開時に決定され、システム間で同じになりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>However, the following behavior is ensured:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、次の動作が確認されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Data upgrade scripts aren't required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ アップグレード スクリプトは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Enum values are persisted in the database, regardless of the enum that is extended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙値は、拡張される列挙に関係なく、データベースに保存されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Therefore, when an enum is made extensible, the enum values that are used on any system will prevail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、列挙が拡張可能になると、すべてのシステムで使用されている列挙が優先されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The first element in the enum gets a value of 0 (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙の最初の要素は、0 (ゼロ) の値を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Therefore, an extensible enum can still be used with the <bpt id="p1">**</bpt>not<ept id="p1">**</ept> operator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、拡張可能列挙は <bpt id="p1">**</bpt>not<ept id="p1">**</ept> 演算子にも使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The only exception is when the first element of the enum had a non-zero value before the enum was made extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">唯一の例外は、列挙が拡張可能になる前に、列挙の最初の要素がゼロ以外の値を持っていた場合です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Using extensible enums in code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードでの拡張可能列挙の使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Because enum values are no longer controlled by the developer, there is no certainty about the enum values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙値は開発者により制御されなくなったため、列挙値に関する確実性はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>When you use extensible enums in code, remember that extensible enums can't be used in comparisons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードで拡張可能列挙を使用する場合は、比較で拡張可能列挙を使用することはできない点に注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For example, <bpt id="p1">**</bpt>MyEnum::Value1 <ph id="ph1">\&gt;</ph> MyEnum::Value2<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>MyEnum::Value1 <ph id="ph1">\&gt;</ph> MyEnum::Value2<ept id="p1">**</ept> などです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Also, look for any conversions between integers and enums.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、整数と列挙の間のすべての変換を探します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>For example, modeled ranges in views and queries, and queries that are created from code by using comparisons, such as <bpt id="p1">**</bpt><ph id="ph1">\&lt;</ph><ept id="p1">**</ept> and <bpt id="p2">**</bpt><ph id="ph2">\&gt;</ph><ept id="p2">**</ept> or by using hardcoded integer values in comparisons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ビューとクエリのモデル化された範囲、比較を使用するか比較でハードコード化された整数値を使用してコードから作成したクエリ (<bpt id="p1">**</bpt><ph id="ph1">\&lt;</ph><ept id="p1">**</ept> や <bpt id="p2">**</bpt><ph id="ph2">\&gt;</ph><ept id="p2">**</ept> など) などです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>When the model and all dependent models are compiled, the comparisons and conversions to integers will be detected by the compiler as errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルと依存しているすべてのモデルをコンパイルすると、比較および整数への変換がコンパイラによってエラーとして検出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Make sure that logic where the enum values are used is extracted in <bpt id="p1">**</bpt>smaller methods<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙値が使用されているロジックがで<bpt id="p1">**</bpt>小さなメソッド<ept id="p1">**</ept>で抽出されることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>In that way, an extension that uses Chain of Command (CoC) can handle the enum values that are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法により、コマンド チェーン (CoC) を使用する拡張が、追加された列挙値を処理できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For <bpt id="p1">**</bpt>construct<ept id="p1">**</ept> methods where the instantiation is based on enum values, replace switch blocks with <bpt id="p2">**</bpt>SysExtension<ept id="p2">**</ept> wherever such a replacement is possible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンス化が列挙値に基づいている<bpt id="p1">**</bpt>構築<ept id="p1">**</ept>メソッドの場合、可能な場合は必ず切り替えブロックを <bpt id="p2">**</bpt>SysExtension<ept id="p2">**</ept> に置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In other cases, make sure that the default block is extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、既定のブロックが拡張可能であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For an example, see the <bpt id="p1">**</bpt>PurchRFQCaseCopying<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>PurchRFQCaseCopying<ept id="p1">**</ept> クラスを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>If the enum is used in <bpt id="p1">**</bpt>switch blocks<ept id="p1">**</ept>, avoid having default blocks that either have or don't have throws that aren't extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙が<bpt id="p1">**</bpt>切り替えブロック<ept id="p1">**</ept>で使用される場合、拡張可能ではないスローを持つか持たない既定のブロックを回避します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When there are <bpt id="p1">**</bpt>long switch case blocks<ept id="p1">**</ept> or <bpt id="p2">**</bpt>if...else blocks<ept id="p2">**</ept> for the enum values, consider creating a class hierarchy to handle specific logic that is related to the enum.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙値に<bpt id="p1">**</bpt>長い切り替えケース ブロック<ept id="p1">**</ept>または <bpt id="p2">**</bpt>if...else ブロック<ept id="p2">**</ept>がある場合、列挙に関連する特定のロジックを処理するクラス階層を作成することを検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For an example, see the <bpt id="p1">**</bpt>PriceGroupTypeTradeAgreementMapping<ept id="p1">**</ept> class hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>PriceGroupTypeTradeAgreementMapping<ept id="p1">**</ept> クラス階層を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Use the <bpt id="p1">**</bpt>in<ept id="p1">**</ept> keyword for query ranges that use the enum values, and make the container that the <bpt id="p2">**</bpt>in<ept id="p2">**</ept> keyword uses extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙値を使用するクエリ範囲に <bpt id="p1">**</bpt>in<ept id="p1">**</ept> キーワードを使用し、<bpt id="p2">**</bpt>in<ept id="p2">**</ept> キーワードが使用するコンテナーを拡張可能にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Potential issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">潜在的な問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Some enums require the elements to have a certain order or value, and cannot be made extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの列挙では、要素が特定の順序または特定の値を持つ必要があり、拡張可能にすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>This could be status enums, where the values represent a logical progressive sequence, like: Draft, Approved, Completed, or Archived.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、ドラフト、承認済み、完了、またはアーカイブなど、値が論理的な連続する順序を表すステータス列挙の可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>It could also be enums where the values must have a fixed integral value to match another artifact, like another enum or a tabpage control's number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別の列挙またはタブページ コントロールの番号など、別のコンポーネントと一致する固定整数値が値に必要な列挙の可能性もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Some enums have many elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの列挙には、多くの要素があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Enums support up to 250 elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙は、最大 250 の要素をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>If your enum has many elements, such as more than 100, consider redesigning the solution instead of making the enum extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙に多くの要素がある場合 (100 を超えるなど)、列挙を拡張可能にするのではなく、ソリューションを再設計することを検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>If the enum is extensible, then adding more elements in the future might break customers's combined solution as the addition might exceed the limit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙が拡張可能である場合、後で要素を追加すると、追加が制限を超える可能性があるため、顧客の結合ソリューションが壊れる可能性があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
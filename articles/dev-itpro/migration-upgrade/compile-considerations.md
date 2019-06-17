<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="compile-considerations.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>compile-considerations.00f75c.90b2ff7b63619c0b043bf14711982b8403d641e7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>90b2ff7b63619c0b043bf14711982b8403d641e7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\compile-considerations.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Plan and prepare for compiling code against the latest update</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新の更新プログラムに対してコードをコンパイルするための計画と準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic highlights potential issues that a developer might see when compiling partner code with the latest update from Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から最新の更新プログラムを使用してパートナー コードをコンパイルするときに、開発者が遭遇する可能性のある潜在的な問題を取り上げます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Plan and prepare for compiling code against the latest update</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新の更新プログラムに対してコードをコンパイルするための計画と準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>With the rollout of the One Version servicing plan, Microsoft is committed to backward compatibility from a binary and functional perspective.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのバージョンのサービス プランの展開では、Microsoft はバイナリおよび機能の観点から下位互換性の確保に努めています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For detailed information about One Version, see <bpt id="p1">[</bpt>One Version service updates FAQ<ept id="p1">](../../fin-and-ops/get-started/one-version.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのバージョンの詳細については、<bpt id="p1">[</bpt>1 つのバージョンのサービス更新に関するよく寄せられる質問<ept id="p1">](../../fin-and-ops/get-started/one-version.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Even with backward compatibility as a priority, there are situations where development activities may result in required code changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">下位互換性が優先事項であっても、開発活動の結果コードの変更が必要になる状況があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Some of those situations are described below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのような状況の一部を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>When Microsoft makes an enumeration extensible, it is considered a binary compatible change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft が列挙を拡張可能にするとき、バイナリと互換性のある変更と見なされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The compiler checks for unsafe extensible enumeration operations that depend on the integer value of a non-extensible enumeration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラは、非拡張可能列挙の整数値に依存する安全ではない拡張可能列挙操作をチェックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Any partner code that contains unsafe extensible enumeration operations will have compiler errors when re-compiled and will need to be modified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">安全ではない拡張可能列挙操作を含むすべてのパートナー コードは、再コンパイル時にコンパイラ エラーとなるため、変更を加える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For more information, see <bpt id="p1">[</bpt>Add values to enums through extension<ept id="p1">](../extensibility/add-enum-value.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>拡張機能による列挙への値の追加<ept id="p1">](../extensibility/add-enum-value.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To avoid possible unresolved references when compiling, a partner model should reference the top-level modules and sub-modules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイル時に生じる可能性のある未解決の参照を避けるため、パートナー モデルは最上位レベルのモジュールと下位のモジュールを参照する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If this is not done, a Microsoft change that adds new resources in an unreferenced sub-module may cause an unresolved reference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行わないと、参照されていない下位モジュールに新しいリソースを追加する Microsoft の変更により、未解決の参照が発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>To resolve the compilation error, add the sub-module as a reference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイル エラーを解決するには、参照として下位モジュールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Some methods will be attributed as obsolete to signal that they will be fully deprecated in the future.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかのメソッドは、将来完全に非推奨となることを示すため、非推奨属性が設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Any compiler warning that is generated due to the calling or wrapping of an obsolete method should be investigated to ensure that the expected code path still exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">古いメソッドの呼び出しまたはラップのために生成されたコンパイラ警告は、予想されるコード パスがまだ存在することを確認するために調べる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In some cases, Microsoft code will directly call the new method in place of the obsolete method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、Microsoft コードが古いメソッドの代わりに新しいメソッドを直接呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>When this happens, the code built around the obsolete method will not execute when expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、古いメソッドに基づいて構築されたコードは実行されません (予期される場合)。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extensible-forms.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extensible-forms.95e5a1.6b439202a4afbca3f4517c3935590bf1509cc362.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>6b439202a4afbca3f4517c3935590bf1509cc362</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\extensible-forms.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Write extensible forms</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能フォームの書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to write extensible forms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張可能フォームを書き込む方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Write extensible forms</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能フォームの書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Methods on forms</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム上のメソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In general, the guidelines for writing extensible methods also apply to form methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、拡張可能なメソッドを記述するためのガイドラインは、フォーム メソッドにも適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Chain of Command (CoC) gives access to the form's non-private members, which are the same as the non-private members for classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド チェーン (CoC) は、フォームの非プライベート メンバー (クラスの非プライベート メンバーと同じ) にアクセスを許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>CoC is enabled for nested classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CoC は入れ子になったクラスで有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Therefore, methods that are defined in various levels on the form are extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、フォーム上のさまざまなレベルで定義されているメソッドは拡張可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>One limitation of methods on forms, that for form data source methods only methods that are defined in the kernel are enabled for extensions, i.e. methods defined on the form data source are not extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのメソッドの 1 つの制限として、データ ソース メソッドの場合、カーネルで定義されているメソッドのみで拡張が有効になります。つまり、フォーム データ ソースで定義されたメソッドは拡張可能ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This will be available in an upcoming Platform Update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは今後のプラットフォーム更新で使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Field groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド グループ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Consider using field groups whenever possible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可能であれば必ずフィールド グループの使用を検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>In this way, independent software vendors (ISVs) can add their fields for free when they extend a field group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、独立系ソフトウェア ベンダー (ISV) はフィールド グループを拡張するときにそのフィールドを無料で追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Form controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム コントロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Moving around form controls could potentially cause a break if the controls are made non-extensible by moving.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールが移動により拡張不可になった場合、フォーム コントロールでの移動により中断が発生する可能性があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
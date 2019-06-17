<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="pos-override-handler.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>pos-override-handler.6b2199.54144a2a0e6539c2cf89a7f8e551a335dc3b3cdb.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>54144a2a0e6539c2cf89a7f8e551a335dc3b3cdb</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\pos-override-handler.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail software development kit (SDK)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail ソフトウェア開発キット (SDK)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides general information about the Retail SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Retail SDK に関する一般情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>The Retail SDK includes code, code samples, templates, and tools that you can use to customize retail functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK は、小売クライアントをカスタマイズするために使用できる、コード、コード サンプル、テンプレート、およびツールが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>POS Override request handler (SDK)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS オーバーライド要求ハンドラー (SDK)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic explains how to override POS request handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、POS 要求ハンドラーをオーバーライドする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>We introduced new extension pattern for overriding the POS business logic, if you have any scenario where you want to modify/add some business logic to the core POS business flow then you can follow this pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS ビジネス ロジックをオーバーライドするための新しい拡張パターンを導入しました。ビジネス ロジックをコア POS 業務フローに変更/追加するシナリオがある場合、このパターンに従うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Ex: When you sell serial item, POS will show a dialog to enter the serial number for that item after the scan, but if you want to automate the serial number process by entering the serial number through code then you can override this serial number handler and customize.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例: シリアル品目を販売するとき、POS にはスキャン後にその品目のシリアル番号を入力するためのダイアログが表示されますが、コードを使用してシリアル番号を入力することでシリアル番号のプロセスを自動化する場合、このシリアル番号ハンドラーをオーバーライドしてカスタマイズできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Any business logic in POS is based upon request and response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS のビジネス ロジックは、要求と応答に基づいています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>So, you can override the relevant request and return the response according to your business scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、関連する要求をオーバーライドし、ビジネス シナリオに従って応答を返すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Note: Not all business request is exposed for customization only few requests are overridable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注意: すべての業務要求がカスタマイズできるように公開されるわけではありませんいくつかの要求のみオーバーライド可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>If you want to customize any business logic and if that request is not overrdiable then create a support ticket or log a request in the LCS extensibility tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス ロジックをカスタマイズする場合で、その要求がオーバーライド可能でない場合、サポート チケットを作成するか、LCS 機能拡張ツールでリクエストを登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Later in this article we have listed the list of requests available for overriding.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事の後方では、オーバーライドできる要求の一覧を示します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="er-apis-app73.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>er-apis-app73.de2f8d.c7da36a60b695882f2585ca408410303ee85f777.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c7da36a60b695882f2585ca408410303ee85f777</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\er-apis-app73.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>ER framework API changes for Application update 7.3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application update 7.3 での ER フレームワーク API の変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how the API of the Electronic reporting (ER) framework has been changed in the Dynamics 365 for Finance and Operations, Enterprise edition Application update 7.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Dynamics 365 for Finance and Operations、Enterprise Edition のアプリケーション更新プログラム 7.3 での電子申告 (ER) フレームワークの API における変更について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>ER framework API changes for Application update 7.3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application update 7.3 での ER フレームワーク API の変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes how the API of the Electronic reporting (ER) framework has been changed in the Dynamics 365 for Finance and Operations, Enterprise edition Application update 7.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Dynamics 365 for Finance and Operations、Enterprise Edition のアプリケーション更新プログラム 7.3 での電子申告 (ER) フレームワークの API における変更について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>There are two types of changes to the ER APIs:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ER API には 2 つのタイプの変更があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Several X++ classes were moved from X++ to an external assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの X++ クラスが外部アセンブリに X++ から移行されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The rest of X++ classes were marked as internal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ クラスの残りの部分は、内部としてマークされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>How to access classes that were moved from X++ to an external assembly</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部アセンブリに X++ から移行されたクラスへのアクセス方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To access external classes, you need to add the <bpt id="p1">**</bpt>using<ept id="p1">**</ept> directive to the beginning of your file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部クラスにアクセスするには、ファイルの先頭に <bpt id="p1">**</bpt>using<ept id="p1">**</ept> ディレクティブを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can then access an external class without any additional changes, for example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、追加の変更をせずに外部クラスにアクセスすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can also create an alias for your namespace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前空間のエイリアスを作成することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>You can then refer to an external class by using the namespace alias that you created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成した名前空間のエイリアスを使用して、外部のクラスを参照することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>How to access internal X++ objects by using ERObjectsFactory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ERObjectsFactory を使用して内部 X++ オブジェクトにアクセスする方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>In Application update 7.3 and later updates, the calling code must access the ER objects by using the methods of the <bpt id="p1">**</bpt>ERObjectsFactory<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの更新プログラム 7.3 以降では、呼び出し元のコードは <bpt id="p1">**</bpt>ERObjectsFactory<ept id="p1">**</ept> クラスのメソッドを使用して ER オブジェクトにアクセスする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Several examples of these changes are shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの変更の例をいくつか示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Code to display a format mapping lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーマット マッピング ルックアップを表示するコード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Before Application update 7.3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション 更新 7.3 より前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Application update 7.3 and later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション更新プログラム 7.3 以降</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Code to run a format mapping for data export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エクスポート用のフォーマット マッピングを実行するためのコード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Before Application update 7.3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション 更新 7.3 より前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Application update 7.3 and later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション更新プログラム 7.3 以降</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Code to run a format mapping for data import</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ インポート用の形式マッピングを実行するためのコード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Before Application update 7.3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション 更新 7.3 より前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Application update 7.3 and later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション更新プログラム 7.3 以降</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Code to create a browser file destination</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザー ファイルの宛先を作成するためのコード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Before Application update 7.3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション 更新 7.3 より前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Application update 7.3 and later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション更新プログラム 7.3 以降</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Code to create an attachment file destination</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">添付ファイルの宛先を作成するためのコード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Before Application update 7.3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション 更新 7.3 より前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Application update 7.3 and later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション更新プログラム 7.3 以降</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
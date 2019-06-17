<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="RetailSDK-update.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>RetailSDK-update.677160.767ffaf742dc794dc60fe74942d2b295ac918d07.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>767ffaf742dc794dc60fe74942d2b295ac918d07</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\RetailSDK-update.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Upgrade the Retail channel extension to the latest Retail SDK</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail チャネル拡張機能を最新の Retail SDK にアップグレード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to upgrade the retail channel extension from earlier releases to the latest update of the Retail SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、以前のリリースから Retail チャネル拡張機能を Retail SDK の最新の更新プログラムにアップグレードする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Upgrade the Retail channel extension to the latest Retail SDK</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail チャネル拡張機能を最新の Retail SDK にアップグレード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information about how to upgrade to the latest update of the Retail SDK from earlier releases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、以前のリリースから Retail SDK の最新の更新プログラムにアップグレードする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The overall process and the supported scenario information are included, but this topic doesn’t provide detailed instructions of every step in the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセス全体とサポートされるシナリオの情報が含まれていますが、このトピックではプロセスの各ステップに関する詳細な指示は提示しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic is applicable for Dynamics 365 for Retail and Dynamics 365 for Finance and Operations 7.3 version and higher.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、Dynamics 365 for Retail および Dynamics 365 for Finance and Operations 7.3 バージョンおよびそれ以上に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The following sections will walk through how to manually move your extension to the new Retail SDK, however you can do this using any source control system like Azure DevOps or Git.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のセクションは新しい Retail SDK に拡張機能を手動で移動する方法を説明しますが、Azure DevOps または Git などのソース管理システムを使用してこれを行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Update the Retail SDK</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>When you update the Retail SDK by applying a new binary hotfix, a new <bpt id="p1">**</bpt>Update<ept id="p1">**</ept> folder is created inside the existing RetailSDK folder and a copy of the updated SDK is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいバイナリの修正プログラムを適用することで Retail SDK を更新するときに、既存の Retail SDK フォルダー内に新しい <bpt id="p1">**</bpt>更新<ept id="p1">**</ept> フォルダーと、更新済の SDK のコピーが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If you deploy a new environment, the new Retail SDK is located in the services volume of the virtual machine (VM) or in the C drive of the downloadable VHD.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい環境を配置する場合、新しい Retail SDK は仮想マシン (VM) のサービス ボリュームまたはダウンロード可能な VHD の C ドライブにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Retail SDK components</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK のコンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The Retail SDK updates consist mainly of the following components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK の更新は、主に次のコンポーネントで構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Assets: Configuration file changes related to extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">資産: 拡張機能に関連するコンフィギュレーション ファイル変更。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Build tools: Customization package and versioning settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド ツール: カスタマイズ パッケージおよびバージョン管理設定。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Database: Extension DB scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース: 拡張 DB スクリプト。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Documents: Instructions to run the samples.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメント: サンプルを実行する方法。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Package: Deployment package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージ: 配置パッケージ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Payment externals: Payment packaging folders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払の外部参照: 支払パッケージング フォルダー。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Payment: Payment sample code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払: 支払のサンプル コード。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>POS: Modern and Cloud POS App code and samples.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS: Modern POS および Cloud POS のアプリケーション コードとサンプル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>References: All binary reference and commerce analyzer proxy tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">参照: すべてのバイナリ参照およびコマース アナライザー プロキシ ツール。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Sample extensions: Extension sample projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプル拡張機能: 拡張機能のサンプル プロジェクト。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Upgrade scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード シナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Upgrade can be completed for one of the following scenarios:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のシナリオのいずれかでアップグレードを完了することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Update to a specific binary hotfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のバイナリ修正プログラムを更新する。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Upgrade your custom code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム コードをアップグレードする。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Upgrade to the latest application release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新のアプリケーション リリースにアップグレードする。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The process for SDK upgrade varies between versions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SDK アップグレード プロセスは、バージョンによって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>With version 7.3 and higher, we sealed all of the Retail components and customizations must be completed only by using the extension points.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン 7.3 以降では、すべての Retail コンポーネントがシールされており、拡張点を使用してのみカスタマイズを完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This should result in an easier code upgrade experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、コード アップグレード作業が容易になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>However, if you are upgrading from 7.0, 7.1, or 7.2 and if you have made inline changes, you must move the inline changes to extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、7.0、7.1、または 7.2 からアップグレードした場合と、インライン変更を行った場合、インラインを拡張機能に移動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>This will require additional work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには追加の作業が必要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The following tables provide some high-level information about which version the code is sealed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表では、コードがシールされているバージョンに関する一部の概要情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If you are upgrading from an unsealed version to a sealed version, you should identify all of your customizations and move any inline customizations to extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アンシールド バージョンからシールド バージョンにアップグレードする場合は、すべてのカスタマイズを識別し、拡張機能にインライン カスタマイズを移動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To move the inline customizations, verify that you have all of the necessary extension points to do this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インライン カスタマイズを移動するには、これを行うために必要な拡張ポイントがすべてあることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>If you don't, submit an extensibility request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ない場合は、拡張機能の要求を送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>You might have to rewrite some of the POS inline changes that were completed in 7.1 when you upgrade to version 7.3 or higher.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン 7.3 以上にアップグレードする際、7.1 で行った POS インラインの変更の一部を書き換える必要がある場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Application version<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーションのバージョン<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>CRT sealed<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CRT シールド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>HWS sealed<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>HWS シールド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>POS sealed<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POS シールド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">**</bpt>DB sealed<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DB シールド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Retail proxy sealed<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Retail プロキシ シールド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Application release 8.1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション リリース 8.1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Application release 8.0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション リリース 8.0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Application 7.3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション 7.3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>July 2017 release (Application 7.2)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2017 年 7 月のリリース (アプリケーション 7.2)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Release 1611 (Application 7.1)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リリース 1611 (アプリケーション 7.1)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>February 2016 release (Application 7.0)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2016 年 2 月リリース (アプリケーション 7.0)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Upgrade the Retail channel extension from 7.3 to a higher version</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">7.3 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>If you are completing a code upgrade, the following Retail SDK components must be upgraded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード アップグレードを実行している場合、Retail SDK の次のコンポーネントをアップグレードする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Each of these components are folders inside the Retail SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの各コンポーネントは、Retail SDK 内のフォルダーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Code upgrade can be completed using a source control/merge tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース管理/マージ ツールを使用してコード アップグレードを完了できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>We recommend using a source control tool for this process so that you can track the changes and revert if required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を追跡して必要に応じて戻すことができるように、このプロセスでソース コード管理ツールを使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>If you are not using any source control, before you upgrade the code, be sure to make a back up of the old and new retail SDK folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース管理を使用していない場合、コードをアップグレードする前に、古いおよび新しい Retail SDK フォルダーのバックアップを作成することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source><bpt id="p1">**</bpt>Assets:<ept id="p1">**</ept> If you have modified any of the following extension config files to include your custom assemblies, you must move those changes to the same config files in the new <bpt id="p2">**</bpt>Asset folder<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>資産:<ept id="p1">**</ept> カスタム アセンブリを含めるために次の拡張構成ファイルのいずれかを変更した場合、これらの変更を新しい<bpt id="p2">**</bpt>資産フォルダー<ept id="p2">**</ept>にある同じ構成ファイルに移動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>CommerceRuntime.Ext.config - CRT extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CommerceRuntime.Ext.config - CRT 拡張。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>CommerceRuntime.MPOSOffline.Ext.config - CRT offline extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CommerceRuntime.MPOSOffline.Ext.config - CRT オフライン拡張。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>HardwareStation.Extension.config - Hardware station and payment extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HardwareStation.Extension.config - ハードウェア ステーションと支払拡張機能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>RetailProxy.MPOSOffline.ext.config - Retail proxy extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RetailProxy.MPOSOffline.ext.config - Retail プロキシ拡張機能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Build tools:<ept id="p1">**</ept> The <bpt id="p2">**</bpt>Build tools<ept id="p2">**</ept> folder contains the files related to packaging, build settings and pfx, and snk files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビルド ツール:<ept id="p1">**</ept> <bpt id="p2">**</bpt>ビルド ツール<ept id="p2">**</ept> フォルダーには、パッケージング、ビルド設定と pfx、および snk ファイルに関連するファイルが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Merge or update the following files if you have made any changes in the older versions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前のバージョンで変更を加えた場合は、以下のファイルをマージおよび更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Customization.settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Customization.settings</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Microsoft.Dynamics.RetailSdk.Build.props</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.RetailSdk.Build.props</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Any custom pfx or snk files that you have created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成したカスタム pfx または snk ファイル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">**</bpt>Database:<ept id="p1">**</ept> Copy and drop all your custom SQL scripts: ...<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>Database<ph id="ph3">\\</ph>Upgrade<ph id="ph4">\\</ph>Custom</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データベース:<ept id="p1">**</ept> カスタム SQL スクリプトをすべてコピーしてドロップします: ...<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>Database<ph id="ph3">\\</ph>Upgrade<ph id="ph4">\\</ph>Custom</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Online Store:<ept id="p1">**</ept> If you have an online store web project or online extension code, include it in this folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>オンライン ストア:<ept id="p1">**</ept> オンライン ストア Web プロジェクトまたはオンライン拡張コードがある場合、このフォルダーに含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Retail deployable package will not include online store code for packaging.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 配置可能パッケージには、パッケージ用のオンライン ストア コードは含まれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Payment externals<ept id="p1">**</ept>: Copy and paste all of your payment extension assemblies to the following <bpt id="p2">**</bpt>Payment assemblies<ept id="p2">**</ept> folders:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>支払の外部参照<ept id="p1">**</ept>: 支払拡張アセンブリすべてをコピーして以下の<bpt id="p2">**</bpt>支払アセンブリ<ept id="p2">**</ept> フォルダーに貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>IPaymentDeviceAssemblies</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IPaymentDeviceAssemblies</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>IPaymentProcessorAssemblies</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IPaymentProcessorAssemblies</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>PaymentWebFiles</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentWebFiles</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Payments:<ept id="p1">**</ept> Merge all of your payment extension projects into this folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>支払:<ept id="p1">**</ept> このフォルダーにすべての支払拡張プロジェクトをマージします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>If you created a new payment extension project and did not modify anything in this folder, you can include it as part of the build and packaging process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい支払拡張機能プロジェクトを作成したが、このフォルダーは何も変更しなかった場合、ビルドとパッケージング プロセスの一部として含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Update <bpt id="p1">**</bpt>dirs.proj<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>RetailSDK<ept id="p2">**</ept> folder to build your custom project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>RetailSDK<ept id="p2">**</ept> フォルダーで <bpt id="p1">**</bpt>dirs.proj<ept id="p1">**</ept> を更新し、カスタム プロジェクトをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Next, update the <bpt id="p1">**</bpt>Customization.settings<ept id="p1">**</ept> file with the payment extension drop location so that during package creation your custom project is built.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、支払拡張機能の格納場所で <bpt id="p1">**</bpt>Customization.settings<ept id="p1">**</ept> ファイルを更新し、パッケージの作成時にカスタム プロジェクトがビルドされるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Make sure to include the extension as part of the packaging.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必ず、パッケージの一部として拡張機能を含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>POS:<ept id="p1">**</ept> If you have any POS extensions, including the generated proxy, copy your POS extensions from <bpt id="p2">*</bpt>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS<ph id="ph3">\\</ph>Extensions<ept id="p2">*</ept> to the new Retail SDK POS extension folder, <bpt id="p3">*</bpt>RetailSDK<ph id="ph4">\\</ph>POS<ph id="ph5">\\</ph>Extensions<ept id="p3">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POS:<ept id="p1">**</ept> 生成されたプロキシを含む任意の POS 拡張機能がある場合、POS 拡張機能を <bpt id="p2">*</bpt>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS<ph id="ph3">\\</ph>Extensions<ept id="p2">*</ept> から新しい Retail SDK POS 拡張子フォルダー <bpt id="p3">*</bpt>RetailSDK<ph id="ph4">\\</ph>POS<ph id="ph5">\\</ph>Extensions<ept id="p3">*</ept> にコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>After you copy the extensions,  update and merge the extension.json file inside the <bpt id="p1">*</bpt>POS<ph id="ph1">\\</ph>Extensions<ept id="p1">*</ept> folder with the new POS extensions folder you copied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能をコピーしたら、<bpt id="p1">*</bpt>POS<ph id="ph1">\\</ph>Extensions<ept id="p1">*</ept> フォルダー内の extension.json ファイルを更新して、コピーした新しい POS 拡張機能とマージします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>For example, if you copied the <bpt id="p1">**</bpt>CustomExtension<ept id="p1">**</ept> folder, then you would update extension.json as shown below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>CustomExtension<ept id="p1">**</ept> フォルダーをコピーした場合、以下に示すように extension.json を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>You should also update tsconfig.json with the custom extension package so that the POS can compile the changes during build.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド中に変更を POS がコンパイルできるように、カスタム拡張機能パッケージで tsconfig.json を更新する必要もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source><bpt id="p1">**</bpt>Reference:<ept id="p1">**</ept> Copy all of your extension output assemblies, such as <bpt id="p2">**</bpt>Commerce runtime<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Hardware station<ept id="p3">**</ept>, <bpt id="p4">**</bpt>proxy<ept id="p4">**</ept>, and any external assemblies, to the reference folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>参照:<ept id="p1">**</ept> <bpt id="p2">**</bpt>Commerce ランタイム<ept id="p2">**</ept>、<bpt id="p3">**</bpt>ハードウェア ステーション<ept id="p3">**</ept>、<bpt id="p4">**</bpt>プロキシ<ept id="p4">**</ept> などのすべての拡張機能出力アセンブリと、へのすべての外部アセンブリを参照フォルダーにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Include any assemblies that you want included as part of your deployment and packaging.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置およびパッケージの一部として含めようとしているすべてのアセンブリを含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source><bpt id="p1">**</bpt>Commerce runtime (CRT) and retail server (RS) extensions:<ept id="p1">**</ept> Copy all of your CRT and RS extension projects under the <bpt id="p2">**</bpt>Retail SDK<ept id="p2">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Commerce ランタイム (CRT) と小売サーバー (RS) 拡張:<ept id="p1">**</ept> CRT および RS 拡張機能プロジェクトすべてを <bpt id="p2">**</bpt>Retail SDK<ept id="p2">**</ept> フォルダーの下にコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Make sure to include the CRT and RS extension solution file details in the dirs.proj file under the <bpt id="p1">**</bpt>RetailSDK folder<ept id="p1">**</ept> so that during msbuild, all of the extension project is built and the output path for the project assemblies is set to the <bpt id="p2">*</bpt>RetailSDK<ph id="ph1">\\</ph>Reference<ept id="p2">*</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">msbuild 中にすべての拡張プロジェクトがビルドされ、プロジェクト アセンブリの出力パスが <bpt id="p2">*</bpt>RetailSDK<ph id="ph1">\\</ph>Reference<ept id="p2">*</ept> フォルダーに設定されるように、必ず、CRT および RS 拡張ソリューション ファイルの詳細を <bpt id="p1">**</bpt>RetailSDK フォルダー<ept id="p1">**</ept>にある dirs.proj ファイルに含めてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source><bpt id="p1">**</bpt>Hardware station (HWS) and payment extensions:<ept id="p1">**</ept> Copy all of your hardware station (HWS) and payment extension projects under the <bpt id="p2">**</bpt>Retail SDK<ept id="p2">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ハードウェア ステーション (HWS) および支払拡張機能:<ept id="p1">**</ept> すべてのハードウェア ステーション (HWS) と支払拡張プロジェクトを <bpt id="p2">**</bpt>Retail SDK<ept id="p2">**</ept> フォルダーの下にコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Make sure to include the HWS and payment extension solution file details in the dirs.proj file under the <bpt id="p1">**</bpt>RetailSDK<ept id="p1">**</ept> folder so that during msbuild, all of the extension projects are built and the output path for the project assemblies is set to the <bpt id="p2">*</bpt>RetailSDK<ph id="ph1">\\</ph>Reference<ept id="p2">*</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">msbuild 中にすべての拡張プロジェクトがビルドされ、プロジェクト アセンブリの出力パスが <bpt id="p2">*</bpt>RetailSDK<ph id="ph1">\\</ph>Reference<ept id="p2">*</ept> フォルダーに設定されるように、必ず、HWS および支払拡張ソリューション ファイルの詳細を <bpt id="p1">**</bpt>RetailSDK<ept id="p1">**</ept> フォルダーにある dirs.proj ファイルに含めてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source><bpt id="p1">**</bpt>Retail proxy extensions:<ept id="p1">**</ept> Copy all of your retail proxy extension projects under the <bpt id="p2">**</bpt>Retail SDK<ept id="p2">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Retail プロキシ拡張:<ept id="p1">**</ept> すべての Retail プロキシ拡張プロジェクトを <bpt id="p2">**</bpt>Retail SDK<ept id="p2">**</ept> フォルダーにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Make sure to include the proxy solution file details in the dirs.proj file under the <bpt id="p1">**</bpt>RetailSDK<ept id="p1">**</ept> folder so that during msbuild, all of the extension projects are built and the output path for the project assemblies is set to the <bpt id="p2">*</bpt>RetailSDK<ph id="ph1">\\</ph>Reference<ept id="p2">*</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">msbuild 中にすべての拡張プロジェクトがビルドされ、プロジェクト アセンブリの出力パスが <bpt id="p2">*</bpt>RetailSDK<ph id="ph1">\\</ph>Reference<ept id="p2">*</ept> フォルダーに設定されるように、必ず、プロキシ ソリューション ファイルの詳細を <bpt id="p1">**</bpt>RetailSDK<ept id="p1">**</ept> フォルダーにある dirs.proj ファイルに含めてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Run <bpt id="p1">**</bpt>msbuild<ept id="p1">**</ept> on the root of the Retail SDK folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK フォルダーのルートで <bpt id="p1">**</bpt>msbuild<ept id="p1">**</ept> を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Use the Microsoft Visual Studio developer command-line tool to generate the retail deployable packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能小売パッケージを生成するために、Microsoft Visual Studio 開発者コマンド ライン ツールを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>After you have upgraded all of the components, deploy the Retail deployable packages, validate the deployment, and add the Retail SDK files to the repository.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのコンポーネントをアップグレードしたら、Retail 配置可能パッケージを配置し、配置を検証して、Retail SDK ファイルをリポジトリに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Upgrade the Retail channel extension from 7.2 to a higher version</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">7.2 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The steps mentioned  in the previous section, <bpt id="p1">**</bpt>Upgrade the retail channel extension from 7.3 to higher versions<ept id="p1">**</ept>, will remain same for all the retail components except the Retail proxy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のセクション <bpt id="p1">**</bpt>7.3 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする<ept id="p1">**</ept>で説明した手順は、Retail プロキシを除くすべての小売コンポーネントでも同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In 7.2, you must have completed inline changes in the retail proxy project if you have CRT with RS extension and the typescript proxy was auto-generated based on the <bpt id="p1">**</bpt>customization.settings<ept id="p1">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RS 拡張機能を持つ CRT があり、<bpt id="p1">**</bpt>customization.settings<ept id="p1">**</ept> ファイルに基づいて TypeScript セッションが自動生成された場合、7.2 では、Retail プロキシ プロジェクトでインライン変更を完了している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>To upgrade your proxy to 7.3, complete the steps in the topic, <bpt id="p1">[</bpt>Typescript and C# proxies for Retail point of sale (POS)<ept id="p1">](typescript-proxy-retail-pos.md)</ept> and then move the proxy to the Retail SDK folder and then update the config file, <bpt id="p2">**</bpt>RetailProxy.MPOSOffline.ext.config<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロキシを 7.3 にアップグレードするには、<bpt id="p1">[</bpt>Typescript および小売販売時点管理 (POS) の C# プロキシ<ept id="p1">](typescript-proxy-retail-pos.md)</ept>のトピックの手順を完了した後、Retail SDK フォルダーにプロキシを移動し、構成ファイル <bpt id="p2">**</bpt>RetailProxy.MPOSOffline.ext.config<ept id="p2">**</ept> を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Upgrade the Retail channel extension from 7.1 to a higher version</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">7.1 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>In 7.1, you should have completed most of the POS and Proxy customizations inline.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">7.1 では、POS およびプロキシ カスタマイズ インラインのほとんどを完了している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>To upgrade to higher a application release, you should move all of your inline changes to extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以上のアプリケーション リリースにアップグレードするは、すべてのインライン変更を拡張機能に移動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>If it is a binary hotfix upgrade, then you must perform a code merge with the new Retail SDK and then regenerate the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バイナリ修正プログラムのアップグレードの場合、新しい Retail SDK とのコード マージを実行し、パッケージを再生成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Upgrade the Retail channel extension from 7.0 to a higher version</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">7.0 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>In 7.0, you should have completed most of the customizations inline.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">7.0 では、カスタマイズ インラインのほとんどを完了している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>To upgrade to higher a application release, you should move all of your inline changes to extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以上のアプリケーション リリースにアップグレードするは、すべてのインライン変更を拡張機能に移動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>If it is binary hotfix upgrade, you must perform a code merge with the new Retail SDK and regenerate the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バイナリ修正プログラムのアップグレードの場合、新しい Retail SDK とのコード マージを実行し、パッケージを再生成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Generate a deployable package for validation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証用の配置可能パッケージを生成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Complete the steps in the topic, <bpt id="p1">[</bpt>Create retail deployable packages<ept id="p1">](retail-sdk/retail-sdk-packaging.md)</ept>, to generate the deployable package for validation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トピック<bpt id="p1">[</bpt>配置可能な小売パッケージの作成<ept id="p1">](retail-sdk/retail-sdk-packaging.md)</ept>の手順を完了し、検証用の配置可能パッケージを生成します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
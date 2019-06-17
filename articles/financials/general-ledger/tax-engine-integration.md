<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="tax-engine-integration.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>tax-engine-integration.c2d083.31b0ffe27eafeee21dfdd388738243129bb215b8.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>31b0ffe27eafeee21dfdd388738243129bb215b8</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\general-ledger\tax-engine-integration.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Tax engine integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジンの統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about Tax engine integration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、税エンジンの統合について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Tax engine integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジンの統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>To integrate the <bpt id="p1">[</bpt>Tax engine<ept id="p1">](tax-engine.md)</ept> (also referred to as GTE) with Microsoft Dynamics 365 for Finance and Operations, you must implement X++ code that interacts with the Tax engine for tax calculation, and that consumes the results to show, account, and post tax for voucher and tax transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>税エンジン<ept id="p1">](tax-engine.md)</ept> (GTE とも呼ばれます) を Microsoft Dynamics 365 for Finance and Operations と統合するには、税計算のために税エンジンとやり取りする X++ コードを実装する必要があります。それは結果を消費して、伝票および税トランザクションの税金の表示、計算、および転記を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>(The tax calculation can either include or exclude tax adjustment.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(税計算では、税調整を含める、または除外することができます。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The Tax engine functionality is only available for legal entities with a primary address in India.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジン機能は、インドに基本住所がある法人に対してのみ使用可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Tax engine integration models</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジンの統合モデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>There are three models for Tax engine integration in the Finance and Operations application:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations アプリケーションに税エンジンを統合するための 3 つのモデルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Tax engine interfaces with the Tax engine service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジン サービスを使用した税エンジン インターフェース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Tax business service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税 ビジネス サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Finance and Operations application integration:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations アプリケーションの統合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Application integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Accounting integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会計の統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>GTE integration models</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GTE 統合モデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Tax engine interfaces with the Tax engine service model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジン サービス モデルを使用した税エンジン インターフェース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>This model is part of the Finance and Operations integration framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このモデルは、Finance and Operations の統合フレームワークの一部です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Therefore, almost no uptake is required for partners or customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、パートナーや顧客にはほとんど取得の必要がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The ITaxEngine interface and its implementation contain the basic operations of the Tax engine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ITaxEngine インターフェースとその実装には、税エンジンの基本操作が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>These operations include calculating tax through the tax engine, persisting the calculated result to Finance and Operations tables, retrieving the tax document for the transaction, and deleting the tax document from both the Tax engine cache and Finance and Operations tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの操作には、税エンジンを介した税の計算、Finance and Operations テーブルへの計算結果の保持、トランザクションの税務書類の取得、税エンジンキャッシュと Finance and Operations テーブルの両方からの税務書類の削除が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The set of ITaxDocument interfaces and implementations enables information to be read from a tax document that the Tax engine calculates and returns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ITaxDocument インターフェイスと実装のセットにより、税エンジンが計算して返す税務書類から情報を読み取ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>This set includes ITaxDocument, ITaxDocumentLine, ITaxDocumentField, ITaxDocumentComponentLine, and ITaxDocumentMeasure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセットには、ITaxDocument、ITaxDocumentLine、ITaxDocumentField、ITaxDocumentComponentLine、およびITaxDocumentMeasure が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>GTE interfaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GTE インターフェイス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>These interfaces also provide methods for retrieving a specified field value (<bpt id="p1">**</bpt>ITaxDocumentField<ept id="p1">**</ept>) from ITaxDocumentLine and an expected measure value (<bpt id="p2">**</bpt>ITaxDocumentMeasure<ept id="p2">**</ept>) from ITaxDocumentComponentLine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのインタフェースは、ITaxDocumentLine から指定されたフィールド値 (<bpt id="p1">**</bpt>ITaxDocumentField<ept id="p1">**</ept>) および ITaxDocumentComponentLine から予測される数値 (<bpt id="p2">**</bpt>ITaxDocumentMeasure<ept id="p2">**</ept>) を取得するためのメソッドも提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The set of ITaxDocumentMetaData interfaces enables model information to be read from a tax document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ITaxDocumentMetaData インターフェイスのセットにより、税務文書からモデル情報を読み取ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>This set includes ITaxDocumentMetaData, ITaxDocumentLineMetaData, ITaxDocumentComponentLineMetaData, and ITaxDocumentMeasureMetaData.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセットには、ITaxDocumentMetaData、ITaxDocumentLineMetaData、ITaxDocumentComponentLineMetaData、および ITaxDocumentMeasureMetaData が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The set of ITaxDocumentEnumerator and ITaxDocumentMeataDataEnumerator interfaces provides an enumerator to read a list of tax document–related objects, such as ITaxDocumentLine, ITaxDocumentField, ITaxDocumentComponentLine, and ITaxDocumentMeasure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ITaxDocumentEnumerator および ITaxDocumentMeataDataEnumerator インターフェイスのセットは、ITaxDocumentLine、ITaxDocumentField、ITaxDocumentComponentLine、および ITaxDocumentMeasure などの税務書類関連オブジェクトのリストを読み取るための列挙子を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Tax business service model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税ビジネス サービス モデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The Tax business service model is part of the Finance and Operations integration framework and almost no uptake is required for partners or customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税ビジネス サービス モデルは、Finance and Operations の統合フレームワークの一部であり、パートナーや顧客にはほとんど取得の必要がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>This model supports the interactions that the Finance and Operations application has with the Tax engine for basic operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このモデルは、Finance and Operations アプリケーションが基本的な操作のために税エンジンと相互作用することをサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>It uses both the interface model and the application model to calculate, account, and post tax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インタフェース モデルとアプリケーション モデルの両方を使用して、税の計算、会計、および転記を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The Tax business service model provides the following methods:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税ビジネス サービス モデルでは、次の方法を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Method<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>メソッド<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Description<ept id="p1">&lt;/strong&gt;</ept><ph id="ph1">
</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>説明<ept id="p1">&lt;/strong&gt;</ept><ph id="ph1">
</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>CalculateTax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税の計算</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Delete a tax document if it&amp;#39;s marked as <bpt id="p1">&lt;strong&gt;</bpt>Dirty<ept id="p1">&lt;/strong&gt;</ept>, and then calculate tax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>ダーティー<ept id="p1">&lt;/strong&gt;</ept>とマークされている場合は、税務書類を削除してから税金を計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Input<ept id="p1">&lt;/strong&gt;</ept>: Taxable document identifier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>入力<ept id="p1">&lt;/strong&gt;</ept>: 課税対象文書の識別子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Output<ept id="p1">&lt;/strong&gt;</ept>: Tax document object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>出力<ept id="p1">&lt;/strong&gt;</ept>: 税務署類オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>RecalculateTax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税の再計算</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Explicitly recalculate a tax document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明示的に税務書類を再計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Input<ept id="p1">&lt;/strong&gt;</ept>: Taxable document identifier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>入力<ept id="p1">&lt;/strong&gt;</ept>: 課税対象文書の識別子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Output<ept id="p1">&lt;/strong&gt;</ept>: Tax document object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>出力<ept id="p1">&lt;/strong&gt;</ept>: 税務署類オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>SaveTaxDocument</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveTaxDocument</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Persist a tax document to the Finance and Operations database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類を Finance and Operations データベースに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Input<ept id="p1">&lt;/strong&gt;</ept>: Taxable document identifier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>入力<ept id="p1">&lt;/strong&gt;</ept>: 課税対象文書の識別子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Output<ept id="p1">&lt;/strong&gt;</ept>: Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>出力<ept id="p1">&lt;/strong&gt;</ept>: 該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>GetTaxDocumentBySource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetTaxDocumentBySource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Read a tax document, based on the source transaction identifier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース トランザクション ID に基づいて税務書類を読み取ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Input<ept id="p1">&lt;/strong&gt;</ept>: Taxable document identifier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>入力<ept id="p1">&lt;/strong&gt;</ept>: 課税対象文書の識別子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Output<ept id="p1">&lt;/strong&gt;</ept>: Tax document object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>出力<ept id="p1">&lt;/strong&gt;</ept>: 税務署類オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>GetTaxDocumentLineBySource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetTaxDocumentLineBySource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Read a tax document line, based on the source transaction line identifier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース トランザクション明細行 ID に基づいて税務書類明細行を読み取ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Input<ept id="p1">&lt;/strong&gt;</ept>: Transaction line identifier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>入力<ept id="p1">&lt;/strong&gt;</ept>: トランザクション明細行識別子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Output<ept id="p1">&lt;/strong&gt;</ept>: Tax document line object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>出力<ept id="p1">&lt;/strong&gt;</ept>: 税務署類明細行オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>GetTaxDocumentTaxStatus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetTaxDocumentTaxStatus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Read the status of a tax document for the associated transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連するトランザクションの税務書類のステータスを読み取ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Input<ept id="p1">&lt;/strong&gt;</ept>: Taxable document identifier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>入力<ept id="p1">&lt;/strong&gt;</ept>: 課税対象文書の識別子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Output<ept id="p1">&lt;/strong&gt;</ept>: Tax document object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>出力<ept id="p1">&lt;/strong&gt;</ept>: 税務署類オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>MarkTaxDocumentTaxStatus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MarkTaxDocumentTaxStatus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Mark a tax document as <bpt id="p1">&lt;strong&gt;</bpt>Dirty<ept id="p1">&lt;/strong&gt;</ept> when the underlining transaction has been updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">下線を引いたトランザクションが更新されたら、税務文書を<bpt id="p1">&lt;strong&gt;</bpt>ダーティー<ept id="p1">&lt;/strong&gt;</ept>としてマークします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Input<ept id="p1">&lt;/strong&gt;</ept>: Taxable document identifier, Tax document status</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>入力<ept id="p1">&lt;/strong&gt;</ept>: 課税対象文書の識別子、税務書類のステータス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Output<ept id="p1">&lt;/strong&gt;</ept>: Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>出力<ept id="p1">&lt;/strong&gt;</ept>: 該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>DeleteTaxDocument</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DeleteTaxDocument</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Delete a tax document when the transaction is deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションが削除された場合に、税務書類を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Input<ept id="p1">&lt;/strong&gt;</ept>: Taxable document identifier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>入力<ept id="p1">&lt;/strong&gt;</ept>: 課税対象文書の識別子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Output<ept id="p1">&lt;/strong&gt;</ept>: Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>出力<ept id="p1">&lt;/strong&gt;</ept>: 該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>PostTax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PostTax</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Post tax for the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの税金を転記します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Input<ept id="p1">&lt;/strong&gt;</ept>: Ledger voucher for the tax that must be posted, Taxable document identifier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>入力<ept id="p1">&lt;/strong&gt;</ept>: 転記する必要がある税の元帳伝票、課税対象文書の識別子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Output<ept id="p1">&lt;/strong&gt;</ept>: Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>出力<ept id="p1">&lt;/strong&gt;</ept>: 該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>TransferTaxDocument</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TransferTaxDocument</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Transfer a tax document from one transaction that the source supports to another transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソースがサポートしているトランザクションから別のトランザクションに税務書類を転送します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Input<ept id="p1">&lt;/strong&gt;</ept>: Source transaction, Target transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>入力<ept id="p1">&lt;/strong&gt;</ept>: ソース トランザクション、ターゲット トランザクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Output<ept id="p1">&lt;/strong&gt;</ept>: Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>出力<ept id="p1">&lt;/strong&gt;</ept>: 該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>PostTaxDocument</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PostTaxDocument</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Just change the status of the tax document to <bpt id="p1">&lt;strong&gt;</bpt>Posted<ept id="p1">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務文書のステータスを <bpt id="p1">&lt;strong&gt;</bpt>転記済<ept id="p1">&lt;/strong&gt;</ept>に変更するだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Input<ept id="p1">&lt;/strong&gt;</ept>: Taxable document identifier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>入力<ept id="p1">&lt;/strong&gt;</ept>: 課税対象文書の識別子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Output<ept id="p1">&lt;/strong&gt;</ept>: Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>出力<ept id="p1">&lt;/strong&gt;</ept>: 該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Finance and Operations application integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations アプリケーションの統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Transaction information from Finance and Operations should be sent to the Tax engine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations からのトランザクション情報は、税エンジンに送信する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>At the same time, the accounting and posting of tax should be aligned with the Finance and Operations implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同時に、税の会計と転記は、Finance and Operations の実装と整合する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Therefore, three parts are created in the Finance and Operations application:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、Finance and Operations application では 3 つの部分が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Taxable document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">課税対象文書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Tax accounting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税会計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Tax posting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税転記</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Meanwhile, the integration uses the transit document framework to maintain the relationship between the Finance and Operations transaction and the tax document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一方、統合では、輸送文書フレームワークを使用して、Finance and Operations トランザクションと税務書類の間の関係を維持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Application integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Taxable document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">課税対象文書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>A taxable document encapsulates transaction information by using a set of data providers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">課税対象文書は、一連のデータ プロバイダーを使用して、トランザクションの情報をカプセル化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Transaction information is wrapped by a TaxableDocument object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの情報は、TaxableDocument オブジェクトによってラップされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>A TaxableDocumentDescriptor object in this object should describe what the transaction is, and it should list a set of data providers that bind tax model attributes with transaction data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオブジェクトの TaxableDocumentDescriptor オブジェクトは、トランザクションとは何かを説明し、税モデル属性をトランザクション データにバインドする一連のデータ プロバイダーをリストする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Taxable document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">課税対象文書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source><bpt id="p1">**</bpt>TaxableDocumentDescriptor<ept id="p1">**</ept> is the class that implements a set of TaxableDocumentTypeDefinition interfaces and describes what the transaction is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TaxableDocumentDescriptor<ept id="p1">**</ept> は、一連の TaxableDocumentTypeDefinition インターフェイスを実装し、トランザクションとは何かを説明するクラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Technically, TaxableDocumentDescriptors are the Finance and Operations table bases, whereas TaxableDocumentTypeDefinitions are more business-driven and are used mainly for tax configuration conditions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">技術的には、TaxableDocumentDescriptors は Finance and Operations のテーブル ベースですが、TaxableDocumentTypeDefinitions はよりビジネス主導型であり、主に税の設定条件に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>In the following example, TaxableDocumentDescriptorPurchaseOrderParm implements three interfaces that share the same Finance and Operations PurchParmTable table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、TaxableDocumentDescriptorPurchaseOrderParm は、同じ Finance and Operations PurchParmTable テーブルを共有する 3 つのインターフェースを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Shared table example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有テーブルの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>If additional attributes are added to a tax configuration, and they are used for lookup, condition, formula, or other configurations, you should bind the attributes with transaction data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の属性が税コンフィギュレーションに追加され、それらがルックアップ、条件、式、またはその他のコンフィギュレーションに使用される場合は、属性をトランザクション データとバインドする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Therefore, you should modify the corresponding data provider classes for a transaction so that they do this type of data binding.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、トランザクションに対応するデータ プロバイダー クラスを変更して、このようなデータ バインディングが行われるようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>If additional transactions should support GTE, you should create related TaxableDocumentTypeDefinitions, TaxableDocumentDescriptors, and TaxableDocumentDataProviders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加のトランザクションが GTE をサポートする必要がある場合は、関連する TaxableDocumentTypeDefinitions、TaxableDocumentDescriptors、および TaxableDocumentDataProviders を作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Transit document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">輸送文書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>A transit document is an existing framework in Finance and Operations that is used for the following two purposes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">輸送文書は、次の 2 つの目的に使用される Finance and Operations の既存のフレームワークです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Maintain the relationship between a transaction and a transit document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションおよび輸送文書間の関係を維持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Transfer the document from one transaction to another transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">あるトランザクションから別のトランザクションにドキュメントを転送します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>This framework lets you easily find a transaction's document and track the transit history.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフレームワークを使用すると、トランザクションのドキュメントを簡単に見つけて輸送履歴を追跡できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>For example, a tax document is created from VendInvoiceInfoTable, and then the transit document maintains the relationship between VendInvoiceInfoTable and TaxDocument.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、VendInvoiceInfoTable から税務書類が作成され、輸送ドキュメントでは VendInvoiceInfoTable と TaxDocument の関係が維持されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>When a purchase order is invoiced, the tax document from VendInvoiceInfoTable is transferred to VendInvoiceJour.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発注書が請求されると、VendInvoiceInfoTable からの税務書類が VendInvoiceJour に転送されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>If additional transactions should support the Tax engine, you should define a rule for the transit document framework to describe which transaction should have a tax document from both the header level and the line level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加のトランザクションが税エンジンをサポートする必要がある場合は、ヘッダー レベルと明細行レベルの両方から、どのトランザクションに税務書類があるかを説明するための輸送ドキュメント フレームワークのルールを定義する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>The rule should also define the transit action from the source transaction to the target transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールには、ソース トランザクションからターゲット トランザクションへの輸送アクションも定義する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Transaction integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Transaction integration occurs only on a case-by-case basis.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの統合は個別でのみ発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>For each transaction and scenario, the Tax business service should be called in the appropriate manner for tax calculation, tax assumption, and tax posting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各トランザクションおよびシナリオに対して、税 ビジネス サービスは税計算、税の仮定、および税転記に対して適切な方法で呼び出す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>For an example, see the <bpt id="p1">[</bpt>Finance and Operations integration example – Purchase order invoice<ept id="p1">](#example-finance-and-operations-integration--purchase-order-invoice)</ept> section later in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、このトピックで後述する <bpt id="p1">[</bpt>Finance and Operations 統合の例 – 発注請求書<ept id="p1">](#example-finance-and-operations-integration--purchase-order-invoice)</ept> セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Accounting integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会計の統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Tax accounting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税会計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The accounting of Finance and Operations transactions has two parts: source document accounting and non-source document accounting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations トランザクションの会計には、元伝票会計と非元伝票会計の 2 つの部分があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The same behavior applies to Tax engine tax accounting, which is integrated with the Finance and Operations implementation on both sides:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ動作が税エンジンの税務会計にも当てはまります。税務会計は、以下の両面で Finance and Operations の実装と統合されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>For source document transactions, such as a purchase order or free text invoice, the account information for tax is fetched when the tax document is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発注書やフ自由書式の請求書などの元伝票のトランザクションでは、税務書類が作成されたときに税のアカウント情報が取得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>For non-source document transactions, such as a sales order or general journal, the account information is determined when tax is posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売注文や一般仕訳帳などの非元伝票トランザクションの場合、アカウント情報は税が転記されるときに決定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>If any additional source document transaction requires Tax engine support, you should create source document–related classes to extend AccountingJournalizationRule and AccountingDistributionRule for the specified business event and monetary amount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の元伝票トランザクションに税エンジンのサポートが必要な場合は、指定されたビジネス イベントと金額に対して AccountingJournalizationRule と AccountingDistributionRule を拡張するための元伝票関連クラスを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Tax engine tax posting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジン税転記</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Currently, Tax engine tax posting generates TaxTrans, TaxTrans<ph id="ph1">\_</ph>IN (if you're running under the India country/region code), and a related voucher for TaxTrans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、税エンジンの税転記により、TaxTrans、TaxTrans<ph id="ph1">\_</ph>IN (インドの国/地域コードで実行している場合)、および TaxTrans の関連伝票が生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In order for the <bpt id="p1">**</bpt>taxTrans<ept id="p1">**</ept> field to be filled with attributes or measures from the tax document, the mapping should be provided via <bpt id="p2">**</bpt>TaxAcctTaxTransTaxDocAttrMapping<ept id="p2">**</ept> and <bpt id="p3">**</bpt>TaxAcctTxTransTaxDocMeasureMapping<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>taxTrans<ept id="p1">**</ept> フィールドに税務書類の属性または基準を入力するには、<bpt id="p2">**</bpt>TaxAcctTaxTransTaxDocAttrMapping<ept id="p2">**</ept> および <bpt id="p3">**</bpt>TaxAcctTxTransTaxDocMeasureMapping<ept id="p3">**</ept> を使用してマッピングを提供する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The following illustration shows how TaxTrans and the voucher are created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、TaxTrans および伝票の作成方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Create TaxTrans and the voucher</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxTrans および伝票の作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>If <bpt id="p1">**</bpt>taxTrans<ept id="p1">**</ept> fields should be filled with additional fields from the tax document, you should update the <bpt id="p2">**</bpt>TaxAcctTaxTransTaxDocAttrMapping<ept id="p2">**</ept> class, the <bpt id="p3">**</bpt>TaxAcctTxTransTaxDocMeasureMapping<ept id="p3">**</ept> class, or the extended classes of one of these classes in the appropriate manner for data binding.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>taxTrans<ept id="p1">**</ept> フィールドに税務書類の追加フィールドを入力する必要がある場合は、 <bpt id="p2">**</bpt>TaxAcctTaxTransTaxDocAttrMapping<ept id="p2">**</ept> クラス、<bpt id="p3">**</bpt>TaxAcctTxTransTaxDocMeasureMapping<ept id="p3">**</ept> クラス、またはこれらのクラスのいずれかの拡張クラスをデータ バインディングに適切な方法で更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Example: Finance and Operations integration – Purchase order invoice</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例: Finance and Operations の統合: 発注請求書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>This section provides an example of how the Tax engine is integrated with purchase order invoices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、税エンジンが発注請求書とどのように統合されるかの例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Related transaction tables include VendInvoiceInfoTable, VendInvoiceInfoLine, VendInvoiceJour, and VendInvoiceTrans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連するトランザクション テーブルには、VendInvoiceInfoTable、VendInvoiceInfoLine、VendInvoiceJour、およびVendInvoiceTrans が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Integration checklist</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合 チェックリスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The following table summarizes all relevant changes that are related to the integration with purchase order invoices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の表は、発注請求書との統合に関連するすべての該当する変更をまとめたものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Transaction uptake checklist</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの取得のチェックリスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>AOT object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Definition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定義</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Define a taxable document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">課税対象文書を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Create the taxable document type and description to describe what the transaction is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">課税対象文書タイプとトランザクションの説明を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>TaxableDocumentTypeDefinitionPurchaseInvoice</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentTypeDefinitionPurchaseInvoice</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>TaxableDocumentDescriptorPurchaseInvoice</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentDescriptorPurchaseInvoice</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Define data providers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ プロバイダーを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Create data providers to provide transaction data to GTE.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション データを GTE に提供するデータ プロバイダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>TaxableDocumentTypeDefinitionPurchaseInvoice</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentTypeDefinitionPurchaseInvoice</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>TaxableDocumentDescriptorPurchaseInvoice</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentDescriptorPurchaseInvoice</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Creation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Add the <bpt id="p1">&lt;strong&gt;</bpt>Tax document<ept id="p1">&lt;/strong&gt;</ept> button on a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションに<bpt id="p1">&lt;strong&gt;</bpt>税務書類<ept id="p1">&lt;/strong&gt;</ept>ボタンを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Add the <bpt id="p1">&lt;strong&gt;</bpt>Tax document<ept id="p1">&lt;/strong&gt;</ept> button to the transaction pages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション ページに<bpt id="p1">&lt;strong&gt;</bpt>税務書類<ept id="p1">&lt;/strong&gt;</ept>ボタンを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>VendEditInvoice</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendEditInvoice</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>VendInvoiceInfoListPage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendInvoiceInfoListPage</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Integrate with transaction totals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの合計と統合します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Create the tax document when the <bpt id="p1">&lt;strong&gt;</bpt>Totals<ept id="p1">&lt;/strong&gt;</ept> button is clicked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>合計<ept id="p1">&lt;/strong&gt;</ept>ボタンをクリックすると、税務書類を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>PurchTotals_ParmTrans.calcTax()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchTotals_ParmTrans.calcTax()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>PurchTotals_ParmTransEdit.calcTax()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchTotals_ParmTransEdit.calcTax()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>PurchTotals_ParmTransEditInvoice.calcTax()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchTotals_ParmTransEditInvoice.calcTax()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Integrate with a source document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元伝票と統合します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Because a purchase invoice is a source document transaction, create a source document when tax is calculated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入請求書は元伝票トランザクションなので、税が計算されるときに元伝票を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>AccDistRuleProductTaxMeasure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AccDistRuleProductTaxMeasure</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>AccJourRuleVendPaymReqTaxMeasure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AccJourRuleVendPaymReqTaxMeasure</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Deletion</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除 </target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Delete a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Delete the tax document when a transaction is deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションが削除される場合、税務書類を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>VendInvoiceInfoTable.delete()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendInvoiceInfoTable.delete()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Delete a transaction line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション明細行を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Recalculate tax when a transaction line is deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション明細行が削除される場合に、税を再計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>VendInvoiceInfoLine.delete()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendInvoiceInfoLine.delete()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Update</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Update transaction header information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション ヘッダー情報を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Recalculate tax when fields that affect tax are updated at the transaction header level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション ヘッダー レベルで税に影響するフィールドが更新されると、税を再計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>VendInvoiceInfoTable.update()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendInvoiceInfoTable.update()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Update transaction line information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション明細行情報を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Recalculate tax when fields that affect tax are updated on a transaction line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション明細行で税に影響するフィールドが更新されると、税を再計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>VendInvoiceInfoLine.update()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendInvoiceInfoLine.update()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Update tax information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税情報を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Recalculate tax when tax information fields are updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税情報のフィールドが更新されると、税を再計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>TransTaxinformation.Write() (page data source)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TransTaxinformation.Write() (ページのデータ ソース)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Posting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">転記</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Define a tax document transition rule.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類の移行ルールを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Define a rule for the transfer of a tax document from one transaction to another transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">あるトランザクションから別のトランザクションへの税務書類の転送に関するルールを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>TaxDocumentTransitRuleEventHandler.initTransitDocumentTransactionRuleList()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxDocumentTransitRuleEventHandler.initTransitDocumentTransactionRuleList()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Transfer a tax document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類を転送します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Transfer the tax document from one transaction to another transaction during posting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">転記中にあるトランザクションから別のトランザクションに税務書類を転送します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>PurchaseInvoiceJournalCreate.endCreate()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchaseInvoiceJournalCreate.endCreate()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Post tax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税金を転記します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Post tax during transaction posting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの転記時に、税を転記します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>PurchaseInvoiceJournalPost.PostTax()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchaseInvoiceJournalPost.PostTax()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Add inventory tax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫税を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Add tax to inventory if a tax load on inventory is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫に対する課税が可能な場合は、在庫に税を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>PurchaseInvoiceJournalPost.PostInventory()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchaseInvoiceJournalPost.PostInventory()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Post a tax document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類を転記します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Post the tax document after the transaction voucher is posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの伝票が転記された後に、税務書類を転記します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>As a result, the tax document status is updated to <bpt id="p1">&lt;strong&gt;</bpt>Posted<ept id="p1">&lt;/strong&gt;</ept>, and records are generated in relation tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果として、税務書類のステータスが、<bpt id="p1">&lt;strong&gt;</bpt>転記済<ept id="p1">&lt;/strong&gt;</ept>に更新され、レコードが関連テーブルに生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>PurchaseInvoiceJournalPost.endUpdate()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchaseInvoiceJournalPost.endUpdate()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Inquiry</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">照会</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Add the <bpt id="p1">&lt;strong&gt;</bpt>Tax document<ept id="p1">&lt;/strong&gt;</ept> button on a journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕訳帳に<bpt id="p1">&lt;strong&gt;</bpt>税務書類<ept id="p1">&lt;/strong&gt;</ept>ボタンを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Add the <bpt id="p1">&lt;strong&gt;</bpt>Tax document<ept id="p1">&lt;/strong&gt;</ept> button to the journal page for inquiry purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">照会用に、ジャーナル ページに<bpt id="p1">&lt;strong&gt;</bpt>税務書類<ept id="p1">&lt;/strong&gt;</ept>ボタンを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>VendInvoiceJournal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendInvoiceJournal</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Define a taxable document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">課税対象文書の定義</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source><bpt id="p1">**</bpt>TaxableDocumentTypeDefintionPurchaseInvoice<ept id="p1">**</ept> and <bpt id="p2">**</bpt>TaxableDocumentDescriptorPurchaseInvoice<ept id="p2">**</ept> are the classes that define a purchase invoice as a taxable document for the Tax engine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TaxableDocumentTypeDefintionPurchaseInvoice<ept id="p1">**</ept> および <bpt id="p2">**</bpt>TaxableDocumentDescriptorPurchaseInvoice<ept id="p2">**</ept> は、税エンジンの課税対象文書として仕入請求書を定義するクラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Taxable document classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">課税対象文書クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>TaxableDocumentTypeDefinitionPurchaseInvoice is the interface that defines a purchase invoice as a taxable document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentTypeDefinitionPurchaseInvoice は、課税対象文書として仕入請求書を定義するインターフェイスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Purchase invoice taxable document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入請求書の課税対象文書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source><bpt id="p1">**</bpt>TaxableDocumentDescriptorPurchaseInvoice.getDataProvider()<ept id="p1">**</ept> specifies the data provider class that is used for a purchase invoice.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TaxableDocumentDescriptorPurchaseInvoice.getDataProvider()<ept id="p1">**</ept> は、仕入請求書に使用されるデータ プロバイダー クラスを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Data provider for a purchase invoice</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入請求書のデータ プロバイダー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Define data providers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ プロバイダーの定義</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>The following illustration shows the data providers that are used to send transaction data to the Tax engine for any tax-related operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、税関連の操作でトランザクション データを税エンジンに送信するために使用されるデータ プロバイダーを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Data providers for GTE</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GTE のデータ プロバイダー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source><bpt id="p1">**</bpt>TaxableDocPurchaseInvoiceDataProvider.buildQuery()<ept id="p1">**</ept> provides a query for all related transactions, such as VendInvoiceInfoTable and VendInvoiceInfoLine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TaxableDocPurchaseInvoiceDataProvider.buildQuery()<ept id="p1">**</ept> は、VendInvoiceInfoTable や VendInvoiceInfoLine など、すべての関連トランザクションに対するクエリを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>It also registers each data source with a row data provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、行のデータ プロバイダーで各データ ソースを登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>For example, the VendInvoiceInfoTable data source is registered with TableDocVendInvoiceInfoTableRowDP.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、VendInvoiceInfoTable データ ソースは、TableDocVendInvoiceInfoTableRowDP で登録されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>VendInvoiceInfoTable data source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendInvoiceInfoTable データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>TaxableDocVendInvoiceInfoTableRowDP extends the <bpt id="p1">**</bpt>TaxableDocPurchTableRowDataProvider<ept id="p1">**</ept> class to set up transaction header–related information, whereas TaxableDocVendInvoiceInfoLineRowDP extends <bpt id="p2">**</bpt>TaxableDocPurchLineRowDataProvider<ept id="p2">**</ept> to set up invoice line–related information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocVendInvoiceInfoTableRowDP は <bpt id="p1">**</bpt>TaxableDocPurchTableRowDataProvider<ept id="p1">**</ept> クラスを拡張してトランザクション ヘッダー関連情報を設定し、TaxableDocVendInvoiceInfoLineRowDP は <bpt id="p2">**</bpt>TaxableDocPurchLineRowDataProvider<ept id="p2">**</ept> を拡張して請求明細行関連の情報を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>The following table lists the taxable document fields that are mapped in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表に、Finance and Operations にマップされている課税対象文書フィールドの一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Taxable document field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">課税対象文書フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Logic in the AOT object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT オブジェクトのロジック</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Required</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必須</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Default value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>SubLines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SubLines</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>TaxableDocumentLineObject.getSubLines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentLineObject.getSubLines</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>TaxableDocumentLineObject.getFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentLineObject.getFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>ModelFieldName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModelFieldName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>TaxableDocumentLineObject.parmModelFieldName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentLineObject.parmModelFieldName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>TaxAdjustment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxAdjustment</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>TaxEngineIntegrationAXContractEventHandler.getLineAdjustment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxEngineIntegrationAXContractEventHandler.getLineAdjustment</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>TableId</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TableId</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>TaxableDocumentLineObject.getTransactionLineTableId</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentLineObject.getTransactionLineTableId</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>RecId</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"> Recid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>TaxableDocumentLineObject.getTransactionLineRecordId</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentLineObject.getTransactionLineRecordId</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Taxable Document Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">課税対象文書タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>TaxableDocumentDescriptor.createRow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentDescriptor.createRow</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Skipped (Document level)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スキップ済 (ドキュメント レベル)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>TaxableDocumentDescriptor.createRow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentDescriptor.createRow</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>DistributionSide</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DistributionSide</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>TaxableDocumentObject.getDistributionSide</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentObject.getDistributionSide</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Auto</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>ExchangeRates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ExchangeRates</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>TaxEngineIntegrationAXContractEventHandler.getExchangeRate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxEngineIntegrationAXContractEventHandler.getExchangeRate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>ReportingCurrencyExchangeRates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ReportingCurrencyExchangeRates</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>TaxEngineIntegrationAXContractEventHandler.getReportingCurrencyExchangeRate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxEngineIntegrationAXContractEventHandler.getReportingCurrencyExchangeRate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Tax Document Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類の目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>TaxableDocumentRowDataProviderLine.fillInFrameworkFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">取引</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Transaction Currency</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション通貨</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>TaxableDocumentRowDataProviderLine.fillInFrameworkFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Transaction Date</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション日付</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>TaxableDocumentRowDataProviderLine.fillInFrameworkFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Skipped (Line level)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スキップ済 (明細行レベル)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>TaxableDocumentRowDataProviderLine.fillInFrameworkFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Tax Direction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税提示方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>TaxableDocumentRowDataProviderLine.fillInFrameworkFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Sales tax receivable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">消費税収入</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Post To Ledger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳への転記</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>TaxableDocumentRowDataProviderLine.fillInFrameworkFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>Enable Accounting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会計の有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>TaxableDocumentRowDataProviderLine.fillInFrameworkFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Line Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">行タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>TaxableDocumentRowDataProviderLine.fillInFrameworkFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Line</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Import Order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート注文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Export Order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート注文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>GST Composition Scheme</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GST 構成スキーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Composition Scheme</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成スキーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Customer Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>None</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>Provisional Assessment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮評価</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>Foreign party</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部関係者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>Nature of Assesse</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">評価の種類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Company</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Preferrential Party</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">優先的関係者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>GTA-Commercial vendor</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GTA 商業仕入先</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Ledger Currency</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳通貨</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>Total Discount Percentage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">合計割引率</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>TaxableDocumentRowDataProviderHeader.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderHeader.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>Exempt</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">免税</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>Transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">取引</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>Prices include sales tax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税込価格</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>Delivery Date</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配送日</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>DiscountAmount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DiscountAmount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>Net Amount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正味金額</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>Quantity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">件数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>Consumption State</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">消費状態</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>Return</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返金</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>Disposition Action</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">処分アクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>No (Yes for a return)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いいえ (返品あり)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>Credit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クレジット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>Assessable Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">課税金額</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>Inter-State</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">州間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>Import Custom Tariff Code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム税率コードのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>No (Yes for an import order)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いいえ (インポート注文はあり)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>Export Custom Tariff Code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム税率コードのエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>No (Yes for an export order)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いいえ (エクスポート注文はあり)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>IEC Number</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IEC 番号</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>Maximum Retail Price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最大小売価格</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>Party GST Registration Number</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パーティ GST 登録番号</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>GST Registration Number</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GST 登録番号</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>HSN Code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HSN コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source>SAC</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SAC</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source>Service Category</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス カテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source>Inward</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">内向き</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source>ITC Category</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ITC カテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source>Input</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source>Is Scrap</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕損</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source>TaxableDocumentRowDataProviderLine.fillInFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxableDocumentRowDataProviderLine.fillInFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source>No (Yes for a sales order)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いいえ (販売注文はあり)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source>Add the Tax document button on a transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションに税務書類ボタンを追加する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="504">
          <source>One way to trigger tax calculation in the Tax engine is through a <bpt id="p1">**</bpt>Tax document<ept id="p1">**</ept> button that you add on the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジンで税計算をトリガーする 1 つの方法は、トランザクションに追加する<bpt id="p1">**</bpt>税務書類<ept id="p1">**</ept>ボタンを使用することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="505">
          <source>When this button is clicked, transactional data is sent to the Tax engine as a predefined taxable document object, and tax calculation is triggered in the Tax engine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このボタンをクリックすると、トランザクション データが事前定義された課税対象文書オブジェクトとして税エンジンに送信され、税計算が税エンジンでトリガーされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="506">
          <source>The button is usually added to a transaction page, such as <bpt id="p1">**</bpt>VendEditInvoice<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタンは通常、<bpt id="p1">**</bpt>VendEditInvoice<ept id="p1">**</ept> などのトランザクション ページに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="507">
          <source>Immediately after tax is calculated, the result appears in the tax document user interface (UI).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税が計算された直後に、結果が税務書類のユーザー インターフェイス (UI) に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="508">
          <source>Tax document button on the Action Pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ペインの税務書類ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="509">
          <source>taxdocumentlauncher properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">taxdocumentlauncher プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="510">
          <source>Integrate with transaction totals</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの合計との統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="511">
          <source>The <bpt id="p1">**</bpt>Totals<ept id="p1">**</ept> button is used to show a transaction's financial information, such as the tax amount, discount amount, and total amounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>合計<ept id="p1">**</ept>ボタンは税金額、割引額、合計額などのトランザクションの財務情報を表示するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="512">
          <source>The tax amount that appears on the total page will also be added to the invoiced amount of the journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">合計ページに表示される税額も、仕訳帳の請求金額に追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="513">
          <source>For an existing implementation of Finance and Operations, a set of <bpt id="p1">**</bpt>PurchTotals<ept id="p1">**</ept> classes is created to handle this functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations の既存の実装では、この機能を処理するために <bpt id="p1">**</bpt>PurchTotals<ept id="p1">**</ept> クラスのセットが作成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="514">
          <source>Therefore, Tax engine-related code is inserted into the class's <bpt id="p1">**</bpt>calcTax<ept id="p1">**</ept> method to help guarantee that the expected tax total amount is initiated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、税エンジン関連のコードがクラスの <bpt id="p1">**</bpt>calcTax<ept id="p1">**</ept> メソッドに挿入され、予想される税金の合計金額が確実に開始されるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="515">
          <source>calcTax method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">calcTax メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="516">
          <source>For alignment with the existing logic, the existing <bpt id="p1">**</bpt>taxTotal<ept id="p1">**</ept> parameter is used to show the tax amount for the whole transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のロジックとの調整のため、既存の <bpt id="p1">**</bpt>taxTotal<ept id="p1">**</ept> パラメーターを使用して、トランザクション全体の税額を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="517">
          <source>A new parameter that is named <bpt id="p1">**</bpt>taxTotalGTE<ept id="p1">**</ept> is used to show the tax that is posted to the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>taxTotalGTE<ept id="p1">**</ept> という名前の新しいパラメーターは、仕入先に転記される税を表示するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="518">
          <source>In some cases, such as a reverse charge, the <bpt id="p1">**</bpt>taxTotal<ept id="p1">**</ept> value doesn't equal the <bpt id="p2">**</bpt>taxTotalGTE<ept id="p2">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">逆請求など、場合によっては、<bpt id="p1">**</bpt>taxTotal<ept id="p1">**</ept> の値が <bpt id="p2">**</bpt>taxTotalGTE<ept id="p2">**</ept> の値と一致しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="519">
          <source>Therefore, <bpt id="p1">**</bpt>taxTotal<ept id="p1">**</ept> will be used for journal posting, whereas <bpt id="p2">**</bpt>taxTotalGTE<ept id="p2">**</ept> will be used on <bpt id="p3">**</bpt>Totals<ept id="p3">**</ept> pages to show the total tax amount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p1">**</bpt>taxTotal<ept id="p1">**</ept> が仕訳の転記に使用され、<bpt id="p2">**</bpt>taxTotalGTE<ept id="p2">**</ept> は<bpt id="p3">**</bpt>合計<ept id="p3">**</ept>ページで合計税額を表示するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="520">
          <source>Integrate with a source document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元伝票との統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="521">
          <source>A purchase invoice is a source document transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入請求書は、元伝票のトランザクションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="522">
          <source>Therefore, the calculated tax result from the Tax engine should be integrated with the existing source document framework in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、税エンジンから計算された税の結果は、Finance and Operations の既存の元伝票フレームワークと統合する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="523">
          <source>The main logic is already completed and handled by the Tax engine integration framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主要なロジックはすでに完成しており、税エンジン統合フレームワークによって処理されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="524">
          <source>However, for each source document transaction, the distribution and journalization rules should still be defined for accounting purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、各元伝票トランザクションについては、配分ルールおよび仕訳ルールを会計目的で定義する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="525">
          <source>Distribution and journalization rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配分ルールと仕訳ルール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="526">
          <source>Two classes are created for a purchase invoice: <bpt id="p1">**</bpt>AcctDistRuleProductTaxMeasure<ept id="p1">**</ept> and <bpt id="p2">**</bpt>AccJourRuleVendPaymReqTaxMeasure<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入請求書用に <bpt id="p1">**</bpt>AcctDistRuleProductTaxMeasure<ept id="p1">**</ept> および <bpt id="p2">**</bpt>AccJourRuleVendPaymReqTaxMeasure<ept id="p2">**</ept> の 2 つのクラスが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="527">
          <source>AcctDistRuleProductTaxMeasure class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AcctDistRuleProductTaxMeasure クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="528">
          <source>AccJourRuleVendPaymReqTaxMeasure class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AccJourRuleVendPaymReqTaxMeasure クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="529">
          <source>When the source document classes are created correctly, the distribution page should show calculated tax together with the component label, tax amount, and ledger account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元伝票クラスが正しく作成されると、配分ページには、計算された税金とコンポーネント ラベル、税額、および勘定科目が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="530">
          <source>Accounting distributions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">勘定配布</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="531">
          <source>Delete a transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="532">
          <source>When a purchase invoice is deleted, the associated tax document should also be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入請求書が削除されると、関連する税務書類も削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="533">
          <source>To delete an associated tax document, call TaxBusinessService in the <bpt id="p1">**</bpt>delete<ept id="p1">**</ept> method of VendInvoiceInfoTable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連する税務書類を削除するには、VendInvoiceInfoTable の<bpt id="p1">**</bpt>削除<ept id="p1">**</ept>メソッドで TaxBusinessService を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="534">
          <source>Transaction deletion method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの削除方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="535">
          <source>Delete a transaction line</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション明細行を削除する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="536">
          <source>When a transaction line is deleted, the tax document should be recalculated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション明細行が削除されると、税務書類を再計算する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="537">
          <source>For performance reasons, GTE doesn't recalculate tax immediately after a transaction line is deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス上の理由から、トランザクション明細行が削除された直後に GTE が税を再計算することはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="538">
          <source>Instead, it updates the tax document's status to <bpt id="p1">**</bpt>Dirty<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、税務書類のステータスを<bpt id="p1">**</bpt>ダーティー<ept id="p1">**</ept>に更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="539">
          <source>When a tax document is retrieved so that it can be viewed or posted, GTE checks whether the status is <bpt id="p1">**</bpt>Dirty<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示または転記できるように税務書類が取得されると、GTE は状態が <bpt id="p1">**</bpt>ダーティー<ept id="p1">**</ept> かどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="540">
          <source>Depending on the status, recalculation occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステータスによっては、再計算が行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="541">
          <source>Tax document status</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類のステータス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="542">
          <source>Tax document status change</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類のステータスの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="543">
          <source>Update transaction header information</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション ヘッダー情報を更新する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="544">
          <source>Some transaction header information can affect tax calculation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部のトランザクション ヘッダー情報は税の計算に影響を与えることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="545">
          <source>Examples include the transaction date and currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例には、トランザクションの日付と通貨が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="546">
          <source>Therefore, when this type of information is updated to a different value, the tax document should be marked as <bpt id="p1">**</bpt>Dirty<ept id="p1">**</ept> so that it can be recalculated later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、この種の情報が別の値に更新された場合は、後で再計算できるよう税務書類を<bpt id="p1">**</bpt>ダーティー<ept id="p1">**</ept>としてマークする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="547">
          <source>Tax document Dirty status</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類のダーティー ステータス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="548">
          <source>The following method lists fields that might affect tax calculation for a purchase invoice.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の方法は、仕入請求書の税計算に影響を与える可能性のあるフィールドを一覧表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="549">
          <source>Method for listing fields that affect tax calculation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税計算に影響を与えるフィールドを一覧表示する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="550">
          <source>Update transaction line information</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション明細行情報を更新する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="551">
          <source>Similarly, the update of some transaction line fields also affects tax calculation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、いくつかのトランザクション明細行フィールドの更新も、税計算に影響します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="552">
          <source>Transaction lines that affect tax calculation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税計算に影響を与えるトランザクション明細行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="553">
          <source>Update tax information</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税情報を更新する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="554">
          <source>The tax information of a transaction line has a major effect on tax calculation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション明細行の税情報は、税計算に大きな影響を与えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="555">
          <source>The logic is maintained on the Application Object Tree (AOT) <bpt id="p1">**</bpt>TransTaxInformation<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロジックはアプリケーション オブジェクト ツリー (AOT) <bpt id="p1">**</bpt>TransTaxInformation<ept id="p1">**</ept> ページで管理されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="556">
          <source>This page might not require further uptake.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このページはそれ以上の取得を必要としない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="557">
          <source>Define a tax document transit rule</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類の輸送ルールを定義する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="558">
          <source>A rule should be defined to associate a purchase invoice and journal with the tax document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入請求書および仕訳帳に税務書類を関連付けるには、ルールを定義する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="559">
          <source>In <bpt id="p1">**</bpt>TaxDocumentTransitRuleEventHandler::initTransitDocumentRuleList()<ept id="p1">**</ept>, rules are defined for VendInvoiceInfoTable, VendInvoiceInfoLine, VendInvoiceJour, and VendInvoiceTrans to specify that the tax document or tax document row should be associated with the transaction table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TaxDocumentTransitRuleEventHandler::initTransitDocumentRuleList()<ept id="p1">**</ept> では、VendInvoiceInfoTable、VendInvoiceInfoLine、VendInvoiceJour、VendInvoiceTrans の各ルールを定義して、税務書類または税務書類行をトランザクション テーブルに関連付ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="560">
          <source>Tax document transit rule</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類の輸送ルール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="561">
          <source><bpt id="p1">**</bpt>TaxDocumentTransitRuleEventHandler::initTransitDocumentRuleExtList()<ept id="p1">**</ept> includes extended rule definitions of a transit action from the transaction to the journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TaxDocumentTransitRuleEventHandler::initTransitDocumentRuleExtList()<ept id="p1">**</ept> には、トランザクションから仕訳帳への輸送アクションの拡張ルールの定義が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="562">
          <source>Tax document transit rule extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類の輸送ルールの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="563">
          <source>Transfer a tax document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類を転送する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="564">
          <source>When a journal is created from a transaction, the tax document should be transferred to the journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションから仕訳帳が作成される場合、税務書類を仕訳帳に転送する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="565">
          <source>The following code transfers a tax document from a purchase invoice to a purchase invoice journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードは、税務書類を仕入請求書から仕入請求書の仕訳帳に転送します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="566">
          <source>Transfer a tax document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類を転送する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="567">
          <source>Post tax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税を転記する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="568">
          <source>Tax posting occurs when the purchase invoice journal is posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税の転記は、仕入請求書の仕訳帳が転記されるときに発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="569">
          <source>Therefore, <bpt id="p1">**</bpt>TaxBusinessService::PostTax()<ept id="p1">**</ept> is called in the <bpt id="p2">**</bpt>FormLetterJournalPost.postTax()<ept id="p2">**</ept> base class to post the purchase invoice journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p2">**</bpt>FormLetterJournalPost.postTax()<ept id="p2">**</ept> 基本クラスで <bpt id="p1">**</bpt>TaxBusinessService::PostTax()<ept id="p1">**</ept> が仕入請求書の仕訳帳を転記するために呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="570">
          <source>Posting tax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税の転記</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="571">
          <source>Add inventory tax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫税を追加する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="572">
          <source>Tax that must be posted to inventory should be added to an inventory transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫に転記する必要がある税は、在庫トランザクションに追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="573">
          <source>The following example shows logic in the <bpt id="p1">**</bpt>Inventory<ept id="p1">**</ept> module that posts tax for inventory by using the <bpt id="p2">**</bpt>taxEngineInventMovement().updateTaxFinancial()<ept id="p2">**</ept> class method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、<bpt id="p2">**</bpt>taxEngineInventMovement().updateTaxFinancial()<ept id="p2">**</ept> クラス メソッドを使用して、在庫に対する税を転記する<bpt id="p1">**</bpt>在庫<ept id="p1">**</ept>モジュールのロジックを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="574">
          <source>Adding inventory tax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫税を追加する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="575">
          <source>Post a tax document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類を転記する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="576">
          <source>After tax is posted, the tax document should be updated to a status that indicates that the tax document has been posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税が転記されたら、税務書類を転記したことを示すステータスに税務書類を更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="577">
          <source>Post a tax document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類を転記する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="578">
          <source>When the preceding method is called, an additional record is created in the TaxDocumentGeneralJournalEntryLink table to maintain the relationship between GeneralJournalEntry and the journal transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記のメソッドが呼び出されると、GeneralDournalEntry と仕訳帳トランザクションの関係を維持するために、TaxDocumentGeneralJournalEntryLink テーブルに追加のレコードが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="579">
          <source>This record will help GTE easily fetch the tax document at the GeneralJournalEntry level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このレコードは GTE が GeneralJournalEntry レベルで税務書類を簡単に取得するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="580">
          <source>Tax document journal entry</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類の仕訳帳入力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="581">
          <source>Debugging</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="582">
          <source>Debugging of the Tax engine is done mainly on the validation of transaction data and the calculated tax document result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジンのデバッグは、主にトランザクション データの検証と計算された税務書類の結果に基づいて行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="583">
          <source>Both the transaction data and the calculated result are in JavaScript Object Notation (JSON) string format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションデータと計算結果はどちらも JavaScript Object Notation (JSON) 文字列形式です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="584">
          <source>Debugging transaction data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション データのデバッグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="585">
          <source>Put a breakpoint in <bpt id="p1">**</bpt>TaxEngineServiceProxy.calculate()<ept id="p1">**</ept>, as shown in the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図に示すように、<bpt id="p1">**</bpt>TaxEngineServiceProxy.calculate()<ept id="p1">**</ept> にブレークポイントを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="586">
          <source>Debugging transaction data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション データのデバッグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="587">
          <source><bpt id="p1">**</bpt>JsonStr<ept id="p1">**</ept> contains all the transaction data information that is prepared by data providers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>JsonStr<ept id="p1">**</ept> には、データ プロバイダーによって作成されたすべてのトランザクション データ情報が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="588">
          <source>You can use any online JSON viewer to easily identify whether data is correctly set for tax model attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンラインの JSON ビューアーを使用して、税モデルの属性にデータが正しく設定されているかどうかを簡単に識別できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="589">
          <source>Debugging the tax document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税務書類のデバッグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="590">
          <source>If the Tax engine returns errors for a calculation, all the results will be set to the <bpt id="p1">**</bpt>RET<ept id="p1">**</ept> attribute in the preceding method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジンが計算に対してエラーを返した場合、すべての結果は上記のメソッドの <bpt id="p1">**</bpt>RET<ept id="p1">**</ept> 属性に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="591">
          <source>By using a Quick Watch command on the attribute, you can easily understand the full error from the Tax engine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性にクイック ウォッチ コマンドを使用すると、税エンジンからの完全なエラーを簡単に理解できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="592">
          <source>If the Tax engine returns no issues, the tax document result will be persisted into the following tables:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税エンジンが問題を返さない場合、税務書類の結果は以下の表に保持されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="593">
          <source>TaxDocument</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxDocument</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="594">
          <source>TaxDocumentRow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxDocumentRow</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="595">
          <source>TaxDocumentJson</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxDocumentJson</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="596">
          <source>By querying these tables to obtain the JSON string, you can easily check the result details via any online JSON viewer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのテーブルを照会して JSON 文字列を取得することで、オンラインの JSON ビューアーを介して結果の詳細を簡単に確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="597">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加リソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="598">
          <source><bpt id="p1">[</bpt>Tax engine overview<ept id="p1">](tax-engine.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>税エンジンの概要<ept id="p1">](tax-engine.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="599">
          <source><bpt id="p1">[</bpt>Extending the Tax engine<ept id="p1">](extend-tax-engine-configurations.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>税エンジンの拡張<ept id="p1">](extend-tax-engine-configurations.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
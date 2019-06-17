<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="segmented-entry-control-migration-guidance.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>segmented-entry-control-migration-guidance.2abfce.9182d9feb4653ef23c733ff3d43b009b04e06e36.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>9182d9feb4653ef23c733ff3d43b009b04e06e36</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\financial\segmented-entry-control-migration-guidance.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Migration guidance for Segmented Entry controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セグメント化されたエントリ コントロールの移行のガイダンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic guides you through the process of migrating a Segmented Entry control from the Microsoft Dynamics AX 2012 pattern to the new pattern in Microsoft Dynamics AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、セグメント化エントリ コントロールを Microsoft Dynamics AX 2012 のパターンから Microsoft Dynamics AX の新しいパターンに移行するプロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Migration guidance for Segmented Entry controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セグメント化されたエントリ コントロールに関する移行ガイダンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic guides you through the process of migrating a Segmented Entry control from the Microsoft Dynamics AX 2012 pattern to the new pattern in Microsoft Dynamics AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、セグメント化エントリ コントロールを Microsoft Dynamics AX 2012 のパターンから Microsoft Dynamics AX の新しいパターンに移行するプロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The goal of the new design is to encapsulate the control implementation and not require that forms interact with the classes that back the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい設計の目標は、コントロールの実装をカプセル化し、コントロールをサポートするクラスとやり取りするフォームを必要としないことです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Therefore, in Microsoft Dynamics AX, <bpt id="p1">&lt;em&gt;</bpt>all forms should interact only with the application programming interface (API) of the *<bpt id="p2">*</bpt>Segmented Entry<ept id="p2">&lt;/em&gt;</ept><ept id="p1">*</ept> control instance<bpt id="p3">&lt;em&gt;</bpt>. They should not interact directly with the controller classes (such as *<bpt id="p4">*</bpt>LedgerDimensionAccountController<ept id="p4">&lt;/em&gt;</ept><ept id="p3">*</ept> and <bpt id="p5">&lt;strong&gt;</bpt>DimensionDynamicAccountController<ept id="p5">&lt;/strong&gt;</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、Microsoft Dynamics AX で、<bpt id="p1">&lt;em&gt;</bpt>すべてのフォームは、*<bpt id="p2">*</bpt>セグメント化されたエントリ<ept id="p2">&lt;/em&gt;</ept><ept id="p1">*</ept>コントロール インスタンス<bpt id="p3">&lt;em&gt;</bpt>のアプリケーション プログラミング インターフェイス (API) とのみ対話する必要があります。それらは、コントローラー クラス (*<bpt id="p4">*</bpt>LedgerDimensionAccountController<ept id="p4">&lt;/em&gt;</ept><ept id="p3">*</ept> や <bpt id="p5">&lt;strong&gt;</bpt>DimensionDynamicAccountController<ept id="p5">&lt;/strong&gt;</ept> など) と直接対話してはなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Any property that was previously manipulated or called on the controller must now be called on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー上で以前に操作または呼び出された任意のプロパティは、コントロール上で呼び出される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Notes:<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>メモ :<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Some APIs have naming differences between the controller and the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部の API は、コントローラーとコントロールで命名方法が違います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The following table lists these APIs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルにこれらの API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source><bpt id="p1">**</bpt>Controller Method (old)<ept id="p1">**</ept><ph id="ph1">
</ph><bpt id="p2">**</bpt>Control Method (new)<ept id="p2">**</ept> parmDate parmControlDate parmFilterLedgerPostingType parmPostingType parmDimensionAccountStorageUsage parmDimensionAccountStorageUsageType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントローラー メソッド (旧)<ept id="p1">**</ept><ph id="ph1">
</ph><bpt id="p2">**</bpt>コントロール メソッド (新)<ept id="p2">**</ept> parmDate parmControlDate parmFilterLedgerPostingType parmPostingType parmDimensionAccountStorageUsage parmDimensionAccountStorageUsageType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>Before:<ept id="p1">**</ept> controller.parmDate(systemDateGet())</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以前:<ept id="p1">**</ept> controller.parmDate(systemDateGet())</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>After:<ept id="p1">**</ept> LedgerAccount.parmControlDate(systemDateGet());</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以後:<ept id="p1">**</ept> LedgerAccount.parmControlDate(systemDateGet());</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In this example, <bpt id="p1">**</bpt>controller<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>LedgerDimensionAccountController<ept id="p2">**</ept> instance and <bpt id="p3">**</bpt>LedgerAccount<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> new <bpt id="p4">**</bpt>Segmented Entry<ept id="p4">**</ept> control instance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>コントローラー<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>LedgerDimensionAccountController<ept id="p2">**</ept> インスタンスと <bpt id="p3">**</bpt>LedgerAccount<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> 新しい<bpt id="p4">**</bpt>セグメント化エントリ<ept id="p4">**</ept> コントロールのインスタンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In methods that have been overridden on controls and data fields, the code upgrade rule replaces method calls on the controllers with method calls on each control instance that was using a particular controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールやデータ フィールドでオーバーライドされたメソッドでは、コード アップグレード ルールが、コントローラーのメソッドの呼び出しを、特定のコントローラーを使用していた各コントロール インスタンスのメソッドの呼び出しに置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Before:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以前:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>After:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以後:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>These changes are made so that it's easier to copy and paste code that must be moved elsewhere (for example, in some instances of <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> and other such methods).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの変更は、他の場所に移動する必要があるコードをコピーして貼り付ける方が簡単になるように行われています (例: <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> およびその他の類似メソッドの一部のインスタンス)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You can ignore this change when you decide whether the method can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドを削除するかどうか決定するときは、この変更を無視することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Your decision should depend on whether the method has any custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">決定内容は、メソッドにカスタム ロジックにあるかどうかによって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The code upgrade script does not handle cases where a controller is instantiated within a method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードのアップグレード スクリプトは、コントローラーがメソッド内でインスタンス化されるケースを処理しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>These cases must be migrated manually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このような場合は、手動で移行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The MRU functionality from Microsoft Dynamics AX 2012 has been removed in Dynamics AX and won't be replaced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 の MRU 機能は、Dynamics AX で削除されました。置き換えの予定はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>parmTaxCode<ept id="p1">**</ept> has been removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parmTaxCode<ept id="p1">**</ept> が削除されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>There is no replacement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">交換はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The custom properties for the <bpt id="p1">**</bpt>Segmented Entry<ept id="p1">**</ept> control are found under <bpt id="p2">**</bpt>Controller<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セグメント化エントリ<ept id="p1">**</ept>コントロールのカスタム プロパティは、<bpt id="p2">**</bpt>コントローラー<ept id="p2">**</ept>の下にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The following screen shot shows an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットは、例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>111<ept id="p1">](./media/111.png)](./media/111.png)</ept> Not all properties apply to all <bpt id="p2">**</bpt>Controller<ept id="p2">**</ept> class types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>111<ept id="p1">](./media/111.png)](./media/111.png)</ept> すべてのプロパティがすべての<bpt id="p2">**</bpt>コント ローラー<ept id="p2">**</ept>クラス タイプに適用されるわけではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Properties that don't apply to a selected controller class will be disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したコントローラー クラスに適用されないプロパティは無効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The following table provides details about the properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、それぞれのプロパティに関する詳細を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>Valid Values<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効な値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Usage<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>用途<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Account Type Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">勘定タイプ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>A field from the datasource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースからのフィールド。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Determines the type of account used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用されるアカウントの種類を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Typically utilized for journal entry from a multi-segment ledger account to single segment values from other backing tables such as Cust, Vend, Bank, Project and similar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、複数セグメントの勘定科目から、Cust、Vend、Bank、Project などの他のックアップ テーブルの単一セグメント値への仕訳入力に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Controller Class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>One of 6 Controller classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">6 つのコントローラー クラスのうちの 1 つです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>For example LedgerDimensionDefaultAccountController.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば LedgerDimensionDefaultAccountController。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Determines the pattern and behavior of the Segmented Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セグメント化されたエントリ コントロールの動作およびパターンを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>More information about this property is provided below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティの詳細については以下で説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Include Financial Accounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務勘定を含む</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>NoYes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NoYes</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Determines if Main accounts that are Financial accounts are valid for use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務勘定である主勘定が有効であるかどうかを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Include Total Accounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">勘定合計を含む</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>NoYes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NoYes</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Determines if Main accounts of type Total are valid for use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイプが "合計" の主勘定が有効であるかどうかを判断します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Is Default Account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の勘定です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>TrueFalse</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TrueFalse</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>For a Dynamic account, determines if the account should be a default or full account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">動的アカウントで、アカウントが既定または完全アカウントであるべきかどうかを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Lock Main Account Segment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主勘定セグメントのロック</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>NoYes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NoYes</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Controls whether the Main account segment is locked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主勘定セグメントがロックされているかどうかをコントロールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Typically used in journals and distributions based upon configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常は仕訳帳や構成に基づく配分に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Posting Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">転記タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>A value from the LedgerPostingType enumeration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerPostingType 列挙の値。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The Main account is validated to see if the posting type is allowed to be used with that account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主勘定が検証され、そのアカウントで使用される転記タイプが許可されているかどうかを確認されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Validate Blocked For Manual Entry</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動入力のブロック状態の検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>NoYes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NoYes</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Determines if the 'Blocked for Manual Entry' status on the dimension should be respected or not.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コードの「手動入力のブロック」ステータスを優先するかどうかを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Controller class property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー クラス プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The following table provides details about each controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、それぞれのコントローラーに関する詳細を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Controller<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントローラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">**</bpt>Details<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>詳細<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>BudgetLedgerDimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BudgetLedgerDimension</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>This Controller provides budget based support for data entry in the Segmented Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、セグメント化された入力コントロールのデータ入力の予算に基づくサポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When using this controller, an Account Structure must be provided to the Segmented Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコント ローラーを使用するときは、勘定構造をセグメント化エントリ コントロールに提供する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>BudgetPlanningLedgerDimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BudgetPlanningLedgerDimension</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>This Controller provides budget planning based support for data entry in the Segmented Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、セグメント化された入力コントロールのデータ入力の予算計画に基づくサポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>When using this controller, an Account Structure must be provided to the Segmented Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコント ローラーを使用するときは、勘定構造をセグメント化エントリ コントロールに提供する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>DimensionDynamicAccount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DimensionDynamicAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This Controller provides support for multiple account types in the Segmented Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、セグメント化された入力コントロールの複数のアカウント タイプのサポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>LedgerDimensionAccountAlias</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerDimensionAccountAlias</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>This Controller provides support for account aliases in the Segmented Entry control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、セグメント化された入力コントロールのアカウント エイリアスのサポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>LedgerDimensionAccount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerDimensionAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This Controller provides support for multi-segment data entry in the Segmented Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、セグメント化された入力コントロールの複数のセグメントのデータ入力のサポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>LedgerDimensionDefaultAccount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerDimensionDefaultAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This Controller provides support for default accounts in the Segmented Entry control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントローラーは、セグメント化された入力コントロールの既定のアカウントのサポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Migration steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">移行ステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Step 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ１</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>If <bpt id="p1">**</bpt>SegmentedEntry<ept id="p1">**</ept> appears as the type next to any control, change it to <bpt id="p2">**</bpt>SegmentedEntryControl<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SegmentedEntry<ept id="p1">**</ept> は任意のコントロールの横にあるタイプとして表示され、<bpt id="p2">**</bpt>SegmentedEntryControl<ept id="p2">**</ept> と変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate01<ept id="p1">](./media/segmentmigrate01.png)](./media/segmentmigrate01.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate01<ept id="p1">](./media/segmentmigrate01.png)](./media/segmentmigrate01.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>An easy method is to append "<ph id="ph1">\_</ph>old" to the name of the old control, add the new control (which should have the original name of the control), migrate all the settings over, and then delete the old control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">簡単な方法は古いコントロールの名前に「<ph id="ph1">\_</ph>旧」を追加し、新しいコントロール (コントロールの元の名前がある必要があります) を付け加え、すべての設定を移行した後、古いコントロールを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> To prevent tests and other code that references the control from breaking, make sure that the new control has the same name as the old control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> コントロールを参照するテストおよび他のコードが破損しないようにするには、新しいコントロールが古いコントロールと同じ名前であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>To add the new control, right-click the parent control that will contain the <bpt id="p1">**</bpt>Segmented Entry<ept id="p1">**</ept> control, and then select <bpt id="p2">**</bpt>New<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>SegmentedEntryControl<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいコントロールを追加するには、<bpt id="p1">**</bpt>Segmented Entry<ept id="p1">**</ept> コントロールを含む親コントロールを右クリックし、<bpt id="p2">**</bpt>New<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>SegmentedEntryControl<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate02<ept id="p1">](./media/segmentmigrate02-623x1024.png)](./media/segmentmigrate02.png)</ept> The following screen shot shows how new control will look.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate02<ept id="p1">](./media/segmentmigrate02-623x1024.png)](./media/segmentmigrate02.png)</ept> 次のスクリーンショットは、新しいコントロールの外観を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate03<ept id="p1">](./media/segmentmigrate03.png)](./media/segmentmigrate03.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate03<ept id="p1">](./media/segmentmigrate03.png)](./media/segmentmigrate03.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Step 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ２</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Override the  <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> control/field method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"> <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> コントロール/メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Remove the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method completely if it contains no other functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の機能が含まれなくなった場合は <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドを完全に削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>If there is other custom <bpt id="p1">**</bpt>jumpRef<ept id="p1">**</ept> functionality, leave that.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のカスタム <bpt id="p1">**</bpt>jumpRef<ept id="p1">**</ept> 機能がある場合は、それをそのままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>However, <bpt id="p1">**</bpt>jumpRef<ept id="p1">**</ept> is otherwise automatically handled by the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>jumpRef<ept id="p1">**</ept> がコントロールによって自動的に処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Step 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Override the <bpt id="p1">**</bpt>loadAutoCompleteData()<ept id="p1">**</ept> control method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadAutoCompleteData()<ept id="p1">**</ept> コントロール メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Remove the <bpt id="p1">**</bpt>loadAutoCompleteData()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadAutoCompleteData()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Step 4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Override the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> control method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> コントロール メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>If the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> method does nothing except call the controller's <bpt id="p2">**</bpt>loadSegments()<ept id="p2">**</ept> and <bpt id="p3">**</bpt>parmControl()<ept id="p3">**</ept> methods, remove it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> メソッドが、コントローラーの <bpt id="p2">**</bpt>loadSegments()<ept id="p2">**</ept> および <bpt id="p3">**</bpt>parmControl()<ept id="p3">**</ept> メソッドを呼ぶ以外に何もしない場合は、それを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>However, make a note of the SEC control instance that is passed to the <bpt id="p1">**</bpt>parmControl()<ept id="p1">**</ept> call.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>parmControl()<ept id="p1">**</ept> 呼び出しに渡される SEC コントロール インスタンスをメモしておきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>The methods that were being called will now have to be called on that instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">呼び出されていたメソッドは、そのインスタンスで呼び出される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Step 5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Override the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> control method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> コントロール メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>If the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> method was used to set parameters on the controller, the calls to <bpt id="p2">**</bpt>parm<ept id="p2">**</ept> method must be moved to every location where the source of the <bpt id="p3">**</bpt>parm<ept id="p3">**</ept> method can change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> メソッドがコントローラーでのパラメーターを設定するために使用された場合、<bpt id="p2">**</bpt>パラメーター<ept id="p2">**</ept> メソッドへの呼び出しは、<bpt id="p3">**</bpt>パラメーター<ept id="p3">**</ept> メソッドのソースを変更することができるすべての場所に移動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>In most cases, these locations are the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method on the corresponding data field and/or the <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> method on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの場合、これらの場所は対応するデータ フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドおよび/またはデータ ソースの <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> メソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>For example, some of the migrated code for the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> override on the left would look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> の移行したコードの一部は、左側で上書きをし、次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Make a note of the SEC control instance that is passed on to the <bpt id="p1">**</bpt>parmControl()<ept id="p1">**</ept> call.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parmControl()<ept id="p1">**</ept> 呼び出しに渡される SEC コントロール インスタンスをメモしておきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>The methods that were being called on the controller will now have to be called on that instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー上で呼び出されていたメソッドは、そのインスタンスで呼び出される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source><bpt id="p1">**</bpt>LedgerJournalTable data source<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>LedgerJournalTable データ ソース<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> After you've moved all the code out of the <bpt id="p2">**</bpt>loadSegments()<ept id="p2">**</ept> method, you can delete the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p2">**</bpt>loadSegments()<ept id="p2">**</ept> メソッドからすべてのコードを削除したら、そのメソッドを削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Step 6</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 6</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Override the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> control method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> コントロール メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>In some cases, the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> method might use a table buffer to set parameters on the controller, but that table buffer isn't a data source on the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、<bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> メソッドは、テーブル バッファを使用してコントローラーでパラメーターを設定することがありますが、そのテーブル バッファはフォーム上のデータ ソースではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>For example, on the <bpt id="p1">**</bpt>LedgerJournalTransDaily<ept id="p1">**</ept> form, the original implementation of <bpt id="p2">**</bpt>loadSegments()<ept id="p2">**</ept> looked like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>LedgerJournalTransDaily<ept id="p1">**</ept> フォームでは、<bpt id="p2">**</bpt>loadSegments()<ept id="p2">**</ept> の元の実装は次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Note that the <bpt id="p1">**</bpt>JournalName<ept id="p1">**</ept> property is set from the ledgerJournalTable buffer, but the LedgerJournalTable table isn't a data source on the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>JournalName<ept id="p1">**</ept> プロパティは、ledgerJournalTable バッファから設定されますが、LedgerJournalTable テーブルはフォームのデータ ソースではないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>In such cases, you can't move that code to either the <bpt id="p1">**</bpt>active()<ept id="p1">**</ept> method of a data source or the <bpt id="p2">**</bpt>modified()<ept id="p2">**</ept> method on the data field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このような場合、そのコードをデータ ソースの <bpt id="p1">**</bpt>active()<ept id="p1">**</ept> メソッド、またはデータ フィールドの <bpt id="p2">**</bpt>modified()<ept id="p2">**</ept> メソッドに移動できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Instead, you should identify where the table buffer is being set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、テーブル バッファが設定されている場所を特定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>For example, in the original implementation of the <bpt id="p1">**</bpt>LedgerJournalTransDaily<ept id="p1">**</ept> form, the ledgerJournalTable buffer was set in the <bpt id="p2">**</bpt>initLedger()<ept id="p2">**</ept> method on the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>LedgerJournalTransDaily<ept id="p1">**</ept> フォームの元の実装では、ledgerJournalTable バッファはフォームの <bpt id="p2">**</bpt>initLedger()<ept id="p2">**</ept> メソッドで設定されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>It should be evident that the value that is passed to <bpt id="p1">**</bpt>parmJournalName()<ept id="p1">**</ept> can change only when the buffer is reassigned in the <bpt id="p2">**</bpt>initLedger()<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parmJournalName()<ept id="p1">**</ept> に渡される値は、バッファが <bpt id="p2">**</bpt>initLedger()<ept id="p2">**</ept> メソッドで再割り当てされる場合のみ変更できることを明らかにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Therefore, code would have to be moved to the <bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> method after the assignment of the buffer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、バッファを割り当てた後、コードを <bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> メソッドに移動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Also, in accordance with the general guidelines, the <bpt id="p1">**</bpt>parmJournalName()<ept id="p1">**</ept> method would be called on the control instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、一般的なガイドラインに従って、コントロールインスタンスに対して <bpt id="p1">**</bpt>parmJournalName()<ept id="p1">**</ept> メソッドが呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Step 7</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 7</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Override the <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> control method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> コントロール メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If the implementation of <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> does nothing except call <bpt id="p2">**</bpt>super()<ept id="p2">**</ept> and the <bpt id="p3">**</bpt>segmentValueChanged()<ept id="p3">**</ept> method on the controller, you can remove the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> を実装した場合に、コントローラー上で <bpt id="p2">**</bpt>super()<ept id="p2">**</ept> と <bpt id="p3">**</bpt>segmentValueChanged()<ept id="p3">**</ept> メソッドを呼び出す以外何も起こらない場合は、メソッドを削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Step 8</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 8</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Override the <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> control method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> コントロール メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>If the implementation of <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> has additional logic, you must replace the method with the <bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> method, as shown here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> の実装に追加のロジックがある場合、次に示すように、メソッドを <bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> メソッドに置き換える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source><bpt id="p1">**</bpt>Notes:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メモ :<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>To add the <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> method, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> メソッドを追加するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Expand the <bpt id="p1">**</bpt>Segmented Entry<ept id="p1">**</ept> control to add the method to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドを追加するには、<bpt id="p1">**</bpt>セグメント化されたエントリ<ept id="p1">**</ept>コントロールを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Right-click the <bpt id="p1">**</bpt>Methods<ept id="p1">**</ept> node, and then select <bpt id="p2">**</bpt>Override<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>onSegmentChanged<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メソッド<ept id="p1">**</ept> ノードをクリックし、<bpt id="p2">**</bpt>オーバーライド<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>onSegmentChanged<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The new method doesn't have to call <bpt id="p1">**</bpt>super()<ept id="p1">**</ept> or any other method on either the control or the controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいメソッドは、<bpt id="p1">**</bpt>super()<ept id="p1">**</ept> またはコントロールまたはコントローラーのいずれかの他のメソッドを呼び出す必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Step 9</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 9</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Override the <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> control method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> コントロール メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Remove the <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> method, unless you have additional validation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の検証がある場合以外は、<bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>The <bpt id="p1">**</bpt>super()<ept id="p1">**</ept> call does everything that this code used to do.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>super()<ept id="p1">**</ept> 呼び出しは、このコードが行っていたすべてのことを行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Therefore, keep only any new code that you have.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、保持している新しいコードのみを残しておいてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Step 10</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 10</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Override the <bpt id="p1">**</bpt>lookup()<ept id="p1">**</ept> control method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>lookup()<ept id="p1">**</ept> コントロール メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Leave the <bpt id="p1">**</bpt>lookup()<ept id="p1">**</ept> method as it is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>lookup()<ept id="p1">**</ept> メソッドをそのままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Step 11</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 11</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Override the <bpt id="p1">**</bpt>lookupReference()<ept id="p1">**</ept> control method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"> <bpt id="p1">**</bpt>lookupReference()<ept id="p1">**</ept> コントロール メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>If the <bpt id="p1">**</bpt>lookupReference()<ept id="p1">**</ept> method uses the default implementation, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>lookupReference()<ept id="p1">**</ept> メソッドが既定の実装を使用している場合、それを削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Step 12</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 12</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Override the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> control method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> コントロール メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Leave the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method as it is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドをそのままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Step 13</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 13</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Override the <bpt id="p1">**</bpt>gotFocus()<ept id="p1">**</ept> control method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>gotFocus()<ept id="p1">**</ept> コントロール メソッドをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>The approach is similar to the approach for the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアプローチは、<bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> メソッドのアプローチに似ています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>The code must be moved to every location where the source of the <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> method can change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parm<ept id="p1">**</ept> メソッドのソースが変更できるすべての場所にコードを移動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>In most cases, these locations are the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method on the corresponding data field and/or the <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> method on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの場合、これらの場所は対応するデータ フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドおよび/またはデータ ソースの <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> メソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>For example, for the preceding code, the migrated code would look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、上記のコードでは、移行したコードはこのようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> After all the code has been moved out of the <bpt id="p2">**</bpt>gotFocus()<ept id="p2">**</ept> method, you can delete the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p2">**</bpt>gotFocus()<ept id="p2">**</ept> メソッドからすべてのコードを削除したら、そのメソッドを削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Step 14</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 14</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>In the form <bpt id="p1">**</bpt>init()<ept id="p1">**</ept> method:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム <bpt id="p1">**</bpt>init()<ept id="p1">**</ept> メソッド:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Set the following properties on the control:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールで以下のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source><bpt id="p1">**</bpt>Data Source<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ ソース<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source><bpt id="p1">**</bpt>Reference Field<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>参照フィールド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source><bpt id="p1">**</bpt>Controller Class<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントローラー クラス<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate04<ept id="p1">](./media/segmentmigrate04.png)](./media/segmentmigrate04.png)</ept> <bpt id="p2">[</bpt><ph id="ph2">![</ph>SegmentMigrate05<ept id="p2">](./media/segmentmigrate05.png)](./media/segmentmigrate05.png)</ept> <bpt id="p3">**</bpt>Note:<ept id="p3">**</ept> A controller class is required for the control to work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate04<ept id="p1">](./media/segmentmigrate04.png)](./media/segmentmigrate04.png)</ept> <bpt id="p2">[</bpt><ph id="ph2">![</ph>SegmentMigrate05<ept id="p2">](./media/segmentmigrate05.png)](./media/segmentmigrate05.png)</ept> <bpt id="p3">**</bpt>注記:<ept id="p3">**</ept> コントロールが動作するためにはコントローラー クラスが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Therefore, a run-time error will be thrown if the <bpt id="p1">**</bpt>Controller Class<ept id="p1">**</ept> property isn't set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p1">**</bpt>Controller Class<ept id="p1">**</ept> プロパティが設定されていないと、ランタイム エラーがスローされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Step 15</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>A map of the dimension specifiers must be created that can then be sent into the <bpt id="p1">**</bpt>Segmented Entry<ept id="p1">**</ept> control's <bpt id="p2">**</bpt>setDimensionSpecifiers<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コードの指定子のマップを作成してから、<bpt id="p1">**</bpt>セグメント化されたエントリ<ept id="p1">**</ept>コントロールの <bpt id="p2">**</bpt>setDimensionSpecifiers<ept id="p2">**</ept> メソッドに送信する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> You can add anything to the dimension specifiers map before it's sent to the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> 分析コードの指定子のマップに何かを追加してからコントロールに送ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>You can also create a new map here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいマップをここで作成することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>(See the <bpt id="p1">**</bpt>onSegmentChangedForPrimaryAccount<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>LedgerJournalEngine<ept id="p2">**</ept> class for similar logic.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(同様のロジックに関しては、<bpt id="p2">**</bpt>LedgerJournalEngine<ept id="p2">**</ept> クラス内の <bpt id="p1">**</bpt>onSegmentChangedForPrimaryAccount<ept id="p1">**</ept> メソッドを参照してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Step 16</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 16</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source><bpt id="p1">**</bpt>parmControl()<ept id="p1">**</ept> method calls: (These are typically present in the form's <bpt id="p2">**</bpt>init()<ept id="p2">**</ept> method or one of the methods that are overridden on the control.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parmControl()<ept id="p1">**</ept> メソッド呼び出し:(これらは通常、フォームの <bpt id="p2">**</bpt>init()<ept id="p2">**</ept> メソッドまたはコントロールで上書きされたメソッドのうちの 1 つに存在します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Remove this line of code, because it's no longer required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要がなくなったため、このコード行を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>However, first make a note of which controller is used with which control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、最初にどのコントローラーがどのコントロールで使用されるかを記録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>For example, in this case, ledgerDimensionDefaultAccountController is being used with the ClearingAccount SEC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、この場合、ledgerDimensionDefaultAccountController が ClearingAccount SEC で使用されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>A mapping is required when you replace method calls on controller objects with corresponding method calls on the control, and when you set the properties at design time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マッピングは、コントロールでコントローラー オブジェクトのメソッド呼び出しを対応するメソッド呼び出しに置き換える場合、およびデザイン時にプロパティを設定する場合に必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Step 17</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 17</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>In the form <bpt id="p1">**</bpt>init()<ept id="p1">**</ept> method:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム <bpt id="p1">**</bpt>init()<ept id="p1">**</ept> メソッド:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>This is the <bpt id="p1">**</bpt>Posting Type<ept id="p1">**</ept> property on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コントロールの<bpt id="p1">**</bpt>転記タイプ<ept id="p1">**</ept>プロパティです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>The control that the <bpt id="p1">**</bpt>PostingType<ept id="p1">**</ept> property must be set on can be determined from the mapping details that are derived by looking at the <bpt id="p2">**</bpt>parmControl()<ept id="p2">**</ept> call.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostingType<ept id="p1">**</ept> プロパティを設定する必要があるコントロールは、<bpt id="p2">**</bpt>parmControl()<ept id="p2">**</ept> 呼び出しを見て派生したマッピングの詳細から判別できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate06<ept id="p1">](./media/segmentmigrate06.png)](./media/segmentmigrate06.png)</ept> These properties can also be set in code, through corresponding <bpt id="p2">**</bpt>parm<ept id="p2">**</ept> methods on the control instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate06<ept id="p1">](./media/segmentmigrate06.png)](./media/segmentmigrate06.png)</ept> これらのプロパティは、コントロール インスタンスで <bpt id="p2">**</bpt>parm<ept id="p2">**</ept> メソッドを介してコードで設定することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Here's an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Step 18</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 18</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Override <bpt id="p1">**</bpt>resolveReference()<ept id="p1">**</ept> in the data source field for the ledger dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳分析コードのデータ ソース フィールドで <bpt id="p1">**</bpt>resolveReference()<ept id="p1">**</ept> をオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate07<ept id="p1">](./media/segmentmigrate07.png)](./media/segmentmigrate07.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>SegmentMigrate07<ept id="p1">](./media/segmentmigrate07.png)](./media/segmentmigrate07.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Delete this code, because it's no longer required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">不要になったので、このコードを削除してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>The control handles this automatically.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールこれを自動的に処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>Step 19</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 19</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>The form sets properties on the controller through <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームは、<bpt id="p1">**</bpt>parm<ept id="p1">**</ept> メソッドを通じてコントローラーのプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>In general, any property that was previously set on the controller class should now be set directly on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、コントローラー クラスに以前設定されていたプロパティをコントロールに直接設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>The control that the property must be set on can be determined from the mapping details that are derived by looking at the <bpt id="p1">**</bpt>parmControl()<ept id="p1">**</ept> call.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティを設定する必要があるコントロールは、<bpt id="p1">**</bpt>parmControl()<ept id="p1">**</ept> 呼び出しを見て派生したマッピングの詳細から判断できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Additionally, for the <bpt id="p1">**</bpt>Segmented Entry<ept id="p1">**</ept> control, any property that is available in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> dialog box in Microsoft Visual Studio can also be set in code, through the corresponding <bpt id="p3">**</bpt>parm<ept id="p3">**</ept> method on the control instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p1">**</bpt>セグメント化エントリ<ept id="p1">**</ept> コントロールの場合、Microsoft Visual Studio の<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ダイアログ ボックスで使用できるプロパティは、コントロール インスタンスで対応する <bpt id="p3">**</bpt>parm<ept id="p3">**</ept> メソッドを使用して、コードで設定することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Step 20</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 20</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>The form uses the control's <bpt id="p1">**</bpt>currentSegmentIndex()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームは、コントロールの <bpt id="p1">**</bpt>currentSegmentIndex()<ept id="p1">**</ept> メソッドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>In general, any property that was previously set on the controller class should now be set directly on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、コントローラー クラスに以前設定されていたプロパティをコントロールに直接設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>The control that the property must be set on can be determined from the mapping details that are derived by looking at the <bpt id="p1">**</bpt>parmControl()<ept id="p1">**</ept> call.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティを設定する必要があるコントロールは、<bpt id="p1">**</bpt>parmControl()<ept id="p1">**</ept> 呼び出しを見て派生したマッピングの詳細から判断できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Additionally, for the <bpt id="p1">**</bpt>Segmented Entry<ept id="p1">**</ept> control, any property that is available in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> dialog box in Visual Studio can also be set in code, through the corresponding <bpt id="p3">**</bpt>parm<ept id="p3">**</ept> method on the control instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p1">**</bpt>セグメント化エントリ<ept id="p1">**</ept> コントロールの場合、Visual Studio の<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ダイアログ ボックスで使用できるプロパティは、コントロール インスタンスで対応する <bpt id="p3">**</bpt>parm<ept id="p3">**</ept> メソッドを使用して、コードで設定することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Step 21</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 21</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>The form calls methods on the controller object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフォームは、コントローラー オブジェクトのメソッドを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Here's an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>All method calls on the controller must be replaced with method calls on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー上のすべてのメソッド呼び出しはコントロール上のメソッド呼び出しに置き換える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>For this example, use the <bpt id="p1">**</bpt>getDimensionAttributeByControlIndex()<ept id="p1">**</ept> method on the control instead.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、代わりにコントロールで <bpt id="p1">**</bpt>getDimensionAttributeByControlIndex()<ept id="p1">**</ept> メソッドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Step 22</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 22</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>For <bpt id="p1">**</bpt>DimensionDynamicAccountController<ept id="p1">**</ept>, the account type is specified through the constructor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DimensionDynamicAccountController<ept id="p1">**</ept> で、勘定タイプはコンストラクターを通して指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>There are two methods for implementing this functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を実装するには、2 つのメソッドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>These methods are mutually exclusive, so use only one of them, depending on the situation:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドは相互に排他的なため、状況に応じてそれらのメソッドのうち 1 つのみを使用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>For the <bpt id="p1">**</bpt>Segmented Entry<ept id="p1">**</ept> control, in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> dialog box, set the <bpt id="p3">**</bpt>Account Type Field<ept id="p3">**</ept> property to the data source field that will provide the account type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セグメント化されたエントリー<ept id="p1">**</ept>コントロールについては、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept>ダイアログ ボックスで、<bpt id="p3">**</bpt>勘定タイプ フィールド<ept id="p3">**</ept>プロパティを勘定タイプを提供するデータ ソース フィールドに設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>This is the preferred method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これが推奨されるメソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> If the <bpt id="p2">**</bpt>super()<ept id="p2">**</ept> call has been removed from the <bpt id="p3">**</bpt>modified()<ept id="p3">**</ept> method for the field that is bound to the <bpt id="p4">**</bpt>Account Type Field<ept id="p4">**</ept> property, this method won't work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p2">**</bpt>super()<ept id="p2">**</ept> 呼び出しが、<bpt id="p4">**</bpt>勘定タイプ フィールド<ept id="p4">**</ept> プロパティにバインドされているフィールドの <bpt id="p3">**</bpt>modified()<ept id="p3">**</ept> メソッドから削除されている場合、このメソッドは機能しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>We have seen this issue in some journal forms, such as <bpt id="p1">**</bpt>LedgerJournalTransDaily<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>LedgerJournalTransDaily<ept id="p1">**</ept> などのいくつかの仕訳帳フォームで、この問題が確認されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>In such cases, either add the <bpt id="p1">**</bpt>super()<ept id="p1">**</ept> call back to the <bpt id="p2">**</bpt>modified()<ept id="p2">**</ept> method, or use the second method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このような場合、<bpt id="p1">**</bpt>super()<ept id="p1">**</ept> コールバックを <bpt id="p2">**</bpt>modified()<ept id="p2">**</ept> メソッドに追加するか、2 つ目のメソッドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Set the account type manually by calling the <bpt id="p1">**</bpt>parmAccountTypeEnumValue()<ept id="p1">**</ept> method on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールで <bpt id="p1">**</bpt>parmAccountTypeEnumValue()<ept id="p1">**</ept> メソッドを呼び出すことにより、勘定タイプを手動で設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Here's an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The call to <bpt id="p2">**</bpt>parmAccountTypeEnumValue()<ept id="p2">**</ept> must be put in both the data source's <bpt id="p3">**</bpt>active()<ept id="p3">**</ept> method and the <bpt id="p4">**</bpt>modified()<ept id="p4">**</ept> method of the field that will provide the account type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p2">**</bpt>parmAccountTypeEnumValue()<ept id="p2">**</ept> への呼び出しは、勘定タイプを提供するフィールドの、データソースの <bpt id="p3">**</bpt>active()<ept id="p3">**</ept> メソッド、および <bpt id="p4">**</bpt>modified()<ept id="p4">**</ept> メソッドの両方に入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Step 23</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 23</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>The form has a variable that is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームには定義されている変数があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Remove this, because the controller is no longer required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラーが必要なくなったため、これを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Step 24</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 24</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source><bpt id="p1">**</bpt>parmCurrentLedgerCOA()<ept id="p1">**</ept> method calls: (These are typically present in the form's <bpt id="p2">**</bpt>init()<ept id="p2">**</ept> method or one of the methods that are overridden on the control.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parmCurrentLedgerCOA()<ept id="p1">**</ept> メソッド呼び出し:(これらは通常、フォームの <bpt id="p2">**</bpt>init()<ept id="p2">**</ept> メソッドまたはコントロールで上書きされたメソッドのうちの 1 つに存在します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Remove this line of code, because it's no longer required in most cases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの場合に必要がなくなったため、このコード行を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Before you delete this line, make sure that the data area ID is correctly passed in to the controller as a parameter, because the <bpt id="p1">**</bpt>LedgerCOA<ept id="p1">**</ept> value will be derived from that information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この線を削除する前に、<bpt id="p1">**</bpt>LedgerCOA<ept id="p1">**</ept> 値がその情報から派生するため、データ領域 ID がパラメーターとしてコントローラーに正しく渡されていることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>If the data area ID is not passed in, replace <bpt id="p1">**</bpt>parmCurrentLedgerCOA(â€¦)<ept id="p1">**</ept> with <bpt id="p2">**</bpt>parmDataAreaId(â€¦)<ept id="p2">**</ept>, and pass the appropriate <bpt id="p3">**</bpt>SelectableDataArea<ept id="p3">**</ept> value, which is usually <bpt id="p4">**</bpt>curext()<ept id="p4">**</ept> or another table field that controls the scope of the company for the account control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ領域 ID が渡されない場合は、<bpt id="p1">**</bpt>parmCurrentLedgerCOA(â€¦)<ept id="p1">**</ept> を <bpt id="p2">**</bpt>parmDataAreaId(â€¦)<ept id="p2">**</ept> で交換し、通常は <bpt id="p4">**</bpt>curext()<ept id="p4">**</ept> または会社のアカウント管理のために範囲を制御する別のテーブル フィールドである適切な <bpt id="p3">**</bpt>SelectableDataArea<ept id="p3">**</ept> 値を渡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>If the form has no data area context but only a current <bpt id="p1">**</bpt>LedgerCOA<ept id="p1">**</ept> value, it should be working only with the default account controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームにデータ領域のコンテキストはありませんが、現在の <bpt id="p1">**</bpt>LedgerCOA<ept id="p1">**</ept> 値のみがある場合、既定のアカウント コント ローラーだけで動作する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>There are only a few forms that are agnostic of a company, but that are scoped to a specific chart of accounts (COA) (for example, <bpt id="p1">**</bpt>MainAccount<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Allocations<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">企業には無関係ですが、特定の勘定科目表 (COA) (<bpt id="p1">**</bpt>MainAccount<ept id="p1">**</ept> および <bpt id="p2">**</bpt>Allocations<ept id="p2">**</ept> など) にスコープされているフォームがいくつかあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>In these cases, <bpt id="p1">**</bpt>parmCurrentLedgerCOA<ept id="p1">**</ept> should be called on the <bpt id="p2">**</bpt>Segmented Entry<ept id="p2">**</ept> control instance that has a default account controller type set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのような場合、<bpt id="p1">**</bpt>parmCurrentLedgerCOA<ept id="p1">**</ept> が、既定のアカウント コントローラー タイプ セットを持つ<bpt id="p2">**</bpt>セグメント化エントリ<ept id="p2">**</ept> コントロール インスタンスで呼び出される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Step 25</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 25</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source><bpt id="p1">**</bpt>parmIncludeFinancialAccounts(NoYes)<ept id="p1">**</ept> method calls:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parmIncludeFinancialAccounts(NoYes)<ept id="p1">**</ept> メソッド呼び出し:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>This line of code is no longer required and should be set directly via a property on the <bpt id="p1">**</bpt>Segmented Entry<ept id="p1">**</ept> control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコード行は不要になり、<bpt id="p1">**</bpt>セグメント化されたエントリ<ept id="p1">**</ept>コントロールのプロパティを使用して直接設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> Because of a framework bug, if you don't set this explicitly, <bpt id="p2">**</bpt>No<ept id="p2">**</ept> will be assigned on a ledger dimension default account controller, whereas the previous behavior was to implicitly assign <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept> during construction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> フレームワークのバグのため、これを明示的に設定しないと、以前の動作では、構築中に暗黙的に<bpt id="p3">**</bpt>はい<ept id="p3">**</ept>が割り当てられていましたが、勘定分析コードの既定のアカウント コントローラーに<bpt id="p2">**</bpt>いいえ<ept id="p2">**</ept>が割り当てられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>You must set this manually as a property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この操作は、プロパティとして手動で設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Alternatively, for a <bpt id="p1">**</bpt>dialog<ept id="p1">**</ept> class, the <bpt id="p2">**</bpt>parm<ept id="p2">**</ept> method should still be explicitly called.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、<bpt id="p1">**</bpt>ダイアログ<ept id="p1">**</ept>クラスへの、<bpt id="p2">**</bpt>parm<ept id="p2">**</ept> メソッドがまだ明示的に呼び出されるはずです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>Step 26</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 26</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>The code for the <bpt id="p1">**</bpt>modified<ept id="p1">**</ept> method of the data field that provides the account type for the <bpt id="p2">**</bpt>Segmented Entry<ept id="p2">**</ept> control might look like this when the control is used as a dynamic account control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>セグメント化エントリ<ept id="p2">**</ept> コントロールのアカウントタイプを提供するデータフィールドの <bpt id="p1">**</bpt>変更済み<ept id="p1">**</ept> メソッドのコードは、コントロールが動的アカウントコントロールとして使用されている場合、このようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>The <bpt id="p1">**</bpt>modified<ept id="p1">**</ept> method of this data field must now clear the ledger dimension field that is bound to the <bpt id="p2">**</bpt>Segmented Entry<ept id="p2">**</ept> control as a <bpt id="p3">**</bpt>Reference<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータ フィールドの <bpt id="p1">**</bpt>modified<ept id="p1">**</ept> メソッドは、<bpt id="p3">**</bpt>参照<ept id="p3">**</ept> フィールドとして <bpt id="p2">**</bpt>セグメント化されたエントリ<ept id="p2">**</ept> コントロールにバインドされた勘定分析コード フィールドをクリアしなければならなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>For example, if the name of the <bpt id="p1">**</bpt>Segmented Entry<ept id="p1">**</ept> control is <bpt id="p2">**</bpt>OffsetAccount<ept id="p2">**</ept>, and the <bpt id="p3">**</bpt>Reference<ept id="p3">**</ept> field property for this control is set to <bpt id="p4">**</bpt>LedgerDimension<ept id="p4">**</ept>, the <bpt id="p5">**</bpt>modified<ept id="p5">**</ept> method in the preceding code should be changed as follows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>セグメント化されたエントリ<ept id="p1">**</ept>コントロールの名前が <bpt id="p2">**</bpt>OffsetAccount<ept id="p2">**</ept> である場合、このコントロールの<bpt id="p3">**</bpt>参照<ept id="p3">**</ept>フィールド プロパティが <bpt id="p4">**</bpt>LedgerDimension<ept id="p4">**</ept> に設定され、上記のコード内の<bpt id="p5">**</bpt>変更<ept id="p5">**</ept>メソッドが次のように変更される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>The additional line is required to clear the control when the account type is changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の明細行は、勘定タイプが変更されたときにコントロールをクリアするために必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Step 27</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 27</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>You can call the <bpt id="p1">**</bpt>parmAccountStructure()<ept id="p1">**</ept> method on the controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラーで <bpt id="p1">**</bpt>parmAccountStructure()<ept id="p1">**</ept> メソッドを呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>This method is replaced by two different methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは 2 つの異なるメソッドで置き換えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Additionally, the purpose of the new methods is the opposite of the old method: the old method turned validation off, whereas the new methods turn it on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、新しいメソッドの目的は、古いメソッドの逆です: 古いメソッドは検証を無効にしましたが、新しいメソッドはそれを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>Therefore, when you migrate code, you must reverse the Boolean parameter for the new methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、コードを移行するときは、新しいメソッドの Boolean パラメーターを逆にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>For example, for the method call in the preceding code, the new methods would look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、上記のコードでメソッドの呼び出しについては、新しいメソッドはこのようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Step 28</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 28</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>You can call the <bpt id="p1">**</bpt>parmAccountStructure()<ept id="p1">**</ept> method on the controller:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のコントローラーで <bpt id="p1">**</bpt>parmAccountStructure()<ept id="p1">**</ept> メソッドを呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>The <bpt id="p1">**</bpt>parmAccountStructureId()<ept id="p1">**</ept> method doesn't exist on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parmAccountStructureId()<ept id="p1">**</ept> メソッドは、コントロール上に存在しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Instead, separate <bpt id="p1">**</bpt>getAccountStructure()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>setAccountStructure()<ept id="p2">**</ept> methods exist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、個別の <bpt id="p1">**</bpt>getAccountStructure()<ept id="p1">**</ept> および <bpt id="p2">**</bpt>setAccountStructure()<ept id="p2">**</ept> メソッドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Therefore, the <bpt id="p1">**</bpt>parmAccountStructureId()<ept id="p1">**</ept> call must be replaced by the <bpt id="p2">**</bpt>get<ept id="p2">**</ept> or <bpt id="p3">**</bpt>set<ept id="p3">**</ept> method, depending on how the <bpt id="p4">**</bpt>parm<ept id="p4">**</ept> method was used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p1">**</bpt>parmAccountStructureId()<ept id="p1">**</ept> 呼び出しは、<bpt id="p4">**</bpt>parm<ept id="p4">**</ept> メソッドがどのように使用されていたかに応じて、<bpt id="p2">**</bpt>get<ept id="p2">**</ept> メソッドまたは <bpt id="p3">**</bpt>set<ept id="p3">**</ept> メソッドで置き換えられる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>For example, the <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> method in the preceding code was called as a setter, so the call should be replaced by a call to the <bpt id="p2">**</bpt>set<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、上記のコードで <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> メソッドはセッターとして呼び出されたので、呼び出しは<bpt id="p2">**</bpt>設定<ept id="p2">**</ept>メソッドへの呼び出しによって置換される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Step 29</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 29</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>This method is replaced by two different methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは 2 つの異なるメソッドで置き換えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>Additionally, the purpose of the new methods is opposite of the old method: the old method turned validation off, whereas the new methods turn it on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、新しいメソッドの目的は、古いメソッドの逆です: 古いメソッドは検証を無効にしましたが、新しいメソッドはそれを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>Therefore, when you migrate code, you must reverse the Boolean parameter for the new methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、コードを移行するときは、新しいメソッドの Boolean パラメーターを逆にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>For example, for the method call in the preceding code, the new methods would look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、上記のコードでメソッドの呼び出しについては、新しいメソッドはこのようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Step 30</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 30</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>Typically, call the <bpt id="p1">**</bpt>loadFromId<ept id="p1">**</ept> method on the controller in the <bpt id="p2">**</bpt>loadSegments()<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常は <bpt id="p2">**</bpt>loadSegments()<ept id="p2">**</ept> メソッド内でコントローラーの <bpt id="p1">**</bpt>loadFromId<ept id="p1">**</ept> メソッドを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Dynamics AX</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>This method has been deprecated and must not be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは推奨されておらず、使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>You should delete all calls to this method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドに対するすべての呼び出しを削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>Migrating a Segmented Entry control on a dialog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ上のセグメント化エントリ コントロールの移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>The uptake pattern for the new <bpt id="p1">**</bpt>Segmented Entry<ept id="p1">**</ept> control on a dialog has changed in Dynamics AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ上の新しい<bpt id="p1">**</bpt>セグメント化されたエントリ<ept id="p1">**</ept> コントロールの取得パターンは Dynamics AX で変更されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Instead of interacting with the controller class API, you must now interact with the <bpt id="p1">**</bpt>SegmentedEntryControlBuild<ept id="p1">**</ept> class to link the SEC with the dialog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー クラス API とのやり取りではなく、<bpt id="p1">**</bpt>SegmentedEntryControlBuild<ept id="p1">**</ept> クラスとやり取りしてダイアログと SEC をリンクする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>This section shows the code patterns for using SEC on a dialog with different controller types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、異なるコントローラー タイプのダイアログで SEC を使用するためのコード パターンを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> Help text is no longer required in Dynamics AX, so you don't have to set the Help text on dialog fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> Dynamics AX ではヘルプ テキストが不要になるため、ダイアログ フィールドにヘルプ テキストを設定する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source><bpt id="p1">**</bpt>Dynamic account:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>動的アカウント:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source><bpt id="p1">**</bpt>Before:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以前:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source><bpt id="p1">**</bpt>After:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以後:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source><bpt id="p1">**</bpt>Ledger account:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>勘定科目:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source><bpt id="p1">**</bpt>Before:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以前:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source><bpt id="p1">**</bpt>After:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以後:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source><bpt id="p1">**</bpt>Default account:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既定の勘定:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source><bpt id="p1">**</bpt>Before:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以前:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source><bpt id="p1">**</bpt>After:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以後:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source><bpt id="p1">**</bpt>Budget:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>予算:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source><bpt id="p1">**</bpt>Before:<ept id="p1">**</ept> No uptake of the <bpt id="p2">**</bpt>Budget<ept id="p2">**</ept> controller (<bpt id="p3">**</bpt>BudgetLedgerDimensionController<ept id="p3">**</ept>) for a dialog scenario was found in the existing program source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以前:<ept id="p1">**</ept> 既存のプログラム ソース コード内でダイアログ シナリオの<bpt id="p2">**</bpt>予算計画<ept id="p2">**</ept>コントローラー (<bpt id="p3">**</bpt>BudgetLedgerDimensionController<ept id="p3">**</ept>) の取り込みは見つかりませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source><bpt id="p1">**</bpt>After:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以後:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source><bpt id="p1">**</bpt>Notes:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メモ :<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>The new API lets you specify the label (<bpt id="p1">**</bpt>Budget<ept id="p1">**</ept> in the preceding example) while you set up the dialog field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい API を使用すると、ダイアログ フィールドを設定しているときに、ラベル (前述の例では <bpt id="p1">**</bpt>予算<ept id="p1">**</ept>) を指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>The default value for the control is specified via the <bpt id="p1">**</bpt>ledgerDimensionBudget<ept id="p1">**</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールのデフォルト値は、<bpt id="p1">**</bpt>ledgerDimensionBudget<ept id="p1">**</ept> 変数で指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>You must specify the account structure that should be used with the <bpt id="p1">**</bpt>Budget<ept id="p1">**</ept> controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>予算<ept id="p1">**</ept> コントローラーを用いて、使用する勘定構造を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>The <bpt id="p1">**</bpt>Dialog<ept id="p1">**</ept> class must implement a way for the user to select the account structure (outside of the SEC) and set the selected account structure on the SEC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dialog<ept id="p1">**</ept> クラスは、ユーザーが勘定構造を選択し (SEC の外部で)、選択した勘定構造を SEC で設定する方法を実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source><bpt id="p1">**</bpt>Budget planning:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>予算計画:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source><bpt id="p1">**</bpt>Before:<ept id="p1">**</ept> No uptake of the <bpt id="p2">**</bpt>Budget planning<ept id="p2">**</ept> controller (<bpt id="p3">**</bpt>BudgetPlanningLedgerDimensionController<ept id="p3">**</ept>) for a dialog scenario was found in the existing program source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以前:<ept id="p1">**</ept> 既存のプログラム ソース コード内でダイアログ シナリオの<bpt id="p2">**</bpt>予算計画<ept id="p2">**</ept>コントローラー (<bpt id="p3">**</bpt>BudgetPlanningLedgerDimensionController<ept id="p3">**</ept>) の取り込みは見つかりませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source><bpt id="p1">**</bpt>After:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>以後:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source><bpt id="p1">**</bpt>Notes:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メモ :<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>The new API lets you specify the label (<bpt id="p1">**</bpt>Budget planning<ept id="p1">**</ept> in the preceding example) while you set up the dialog field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい API を使用すると、ダイアログ フィールドを設定しているときに、ラベル (前述の例では <bpt id="p1">**</bpt>予算計画<ept id="p1">**</ept>) を指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>The default value for the control is specified via the <bpt id="p1">**</bpt>ledgerDimensionBudgetPlanning<ept id="p1">**</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールのデフォルト値は、<bpt id="p1">**</bpt>ledgerDimensionBudgetPlanning<ept id="p1">**</ept> 変数で指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>You must specify the account structure that should be used with the <bpt id="p1">**</bpt>Budget planning<ept id="p1">**</ept> controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>予算計画<ept id="p1">**</ept> コントローラーを用いて、使用する勘定構造を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>The <bpt id="p1">**</bpt>Dialog<ept id="p1">**</ept> class must implement a way for the user to select the account structure (outside of the SEC) and set the selected account structure on the SEC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dialog<ept id="p1">**</ept> クラスは、ユーザーが勘定構造を選択し (SEC の外部で)、選択した勘定構造を SEC で設定する方法を実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source><bpt id="p1">[</bpt>Segmented Entry control dialog support<ept id="p1">](segmented-entry-control-dialog-support.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>セグメント化されたエントリ コントロールのダイアログのサポート<ept id="p1">](segmented-entry-control-dialog-support.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source><bpt id="p1">[</bpt>Segmented Entry control Metadata Specification<ept id="p1">](segmented-entry-control-metadata-specification.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>セグメント化されたエントリ コントロールのメタデータ詳細<ept id="p1">](segmented-entry-control-metadata-specification.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source><bpt id="p1">[</bpt>Segmented Entry control Parm method Specification<ept id="p1">](segmented-entry-control-parm-method-specification.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>セグメント化されたエントリ コントロールの Parm メソッド詳細<ept id="p1">](segmented-entry-control-parm-method-specification.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source><bpt id="p1">[</bpt>Segmented Entry control migration<ept id="p1">](segmented-entry-control-conversion.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>セグメント化されたエントリ コントロールの移行<ept id="p1">](segmented-entry-control-conversion.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
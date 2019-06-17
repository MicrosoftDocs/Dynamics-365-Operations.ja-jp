<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="activate-financial-dimensions.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>activate-financial-dimensions.75d2f5.44499cad4a9acd0f6f87b0fa0865d9e09ca3c0e4.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>44499cad4a9acd0f6f87b0fa0865d9e09ca3c0e4</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\financial\activate-financial-dimensions.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Financial dimension activation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コードの有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic contains information about the activating financial dimension process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックには、財務分析コード プロセスの有効化に関する情報が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Financial dimension activation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コードの有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic contains information about the activating financial dimension process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックには、財務分析コード プロセスの有効化に関する情報が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When a new financial dimension is added to the system, users are prompted with a message stating that the financial dimension is not consumable until Dimension activation is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい財務分析コードがシステムに追加されると、分析コードの有効化が実行されるまで財務分析コードを使用できないことを示すメッセージがユーザーに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When Dimension activation is run, a database schema change occurs in the <bpt id="p1">**</bpt>DimensionAttributeValueCombination<ept id="p1">**</ept> and <bpt id="p2">**</bpt>DimensionAttributeValueSet<ept id="p2">**</ept> tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コードの有効化を実行すると、<bpt id="p1">**</bpt>DimensionAttributeValueCombination<ept id="p1">**</ept> および <bpt id="p2">**</bpt>DimensionAttributeValueSet<ept id="p2">**</ept> テーブルで、データベースのスキーマの変更が実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The schema change adds a new column to the table for each financial dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スキーマの変更により、各財務分析コードのテーブルに新しい列が追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>During this process, a schema lock is placed on the two tables by Microsoft SQL Server so that the table can be updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセス中に、スキーマロックは Microsoft SQL Server によって 2 つのテーブルに配置され、テーブルを更新することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>When the process is complete, the tables are no longer locked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスが完了すると、テーブルはもはやロックされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If this process is attempted when a journal is open, then a deadlock may occur.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕訳帳が開いたときにこのプロセスが実行されると、デッドロックが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>If this happens, the user could potentially receive a metadata error from the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これが発生した場合、ユーザーはサーバーからメタデータ エラーを受け取る可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Users can refresh the session to get the updated metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セッションを最新の情報に更新して、更新されたメタデータを取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The message the user receives states:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが受け取るメッセージ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>You will not be able to consume the financial dimension anywhere until the process is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスが実行されるまで、どの場所でも、財務分析コードを使用することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>This includes adding it to account structures.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには、勘定構造に追加することが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>A schema change occurs, therefore a special privilege, the Dimension activation privilege is required to run activation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スキーマの変更が発生するため、有効化を実行するには、特別な権限である分析コードの有効化権限が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You should perform this during scheduled maintenance or downtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予定されたメンテナンスまたはダウンタイムの際に、これを行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Adding a financial dimension is typically a very deliberate business process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コードを追加することは、通常、非常に意図的な業務プロセスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>If there is a multi-user environment, such as a user acceptance testing or training environment, only one person should attempt this process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー受け入れテストなどのマルチ ユーザー環境またはトレーニング環境がある場合、1 人だけがこのプロセスを試行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>A second option is available when you choose the Activate option, <bpt id="p1">**</bpt>Rebuild financial dimensions<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 番目のオプションは、有効化オプション、<bpt id="p1">**</bpt>財務分析コードの再構築<ept id="p1">**</ept>を選択したときに使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>ActWiki2<ept id="p1">](./media/actwiki2.png)](./media/actwiki2.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ActWiki2<ept id="p1">](./media/actwiki2.png)](./media/actwiki2.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The <bpt id="p1">**</bpt>Rebuild financial dimensions<ept id="p1">**</ept> option is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept> by default, as it is a process that should only be run if unexpected results occur during the initial activation process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>財務分析コードを再構築<ept id="p1">**</ept> オプションは、初期有効化プロセス中予期しない結果が発生した場合にのみ実行されるプロセスであるため、既定で <bpt id="p2">**</bpt>いいえ<ept id="p2">**</ept> に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>This will drop and re-add all financial dimensions and values to the tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、すべての財務分析コードと値がドロップされ、テーブルに再追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt>Set up financial dimensions (Task guide)<ept id="p1">](../../financials/general-ledger/tasks/define-financial-dimensions.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>財務分析コード を設定する (タスク ガイド)<ept id="p1">](../../financials/general-ledger/tasks/define-financial-dimensions.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">[</bpt>Maintenance mode<ept id="p1">](../sysadmin/maintenance-mode.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>メンテナンス モード<ept id="p1">](../sysadmin/maintenance-mode.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
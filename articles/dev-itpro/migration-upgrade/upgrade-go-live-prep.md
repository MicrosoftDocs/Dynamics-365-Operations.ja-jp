<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="upgrade-go-live-prep.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>upgrade-go-live-prep.f05c41.4f1c1dfc7f177d026eb1fd9af873f7aeb4de7087.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4f1c1dfc7f177d026eb1fd9af873f7aeb4de7087</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\upgrade-go-live-prep.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Upgrade from AX 2012 - Prepare for go-live</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - 稼働の準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how you can help guarantee that the source AX 2012 system and the upgrade process remain stable and consistent for go-live.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、ソース AX 2012 システムとアップグレード プロセスが安定した状態を保ち、運用の一貫性があることを保証する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Upgrade from AX 2012 - Prepare for go-live</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - 稼働の準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>As the go-live date approaches, it's important that you implement this series of steps to help guarantee that the source Microsoft Dynamics AX 2012 system and the upgrade process both remain stable and consistent for go-live.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">稼動日が近づくにつれ、一連の手順を実装しソース Microsoft Dynamics AX 2012 システムとアップグレード プロセスが安定した状態を保ち、運用の一貫性があることを保証することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>As part of this process, you must lock down any further code changes or application setup changes before you run the final cutover test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスの一環として、最終的な切替テストを実行する前にコード変更やアプリケーションの設定の変更をすべてロック ダウンする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Code freeze</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード凍結</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>All code changes in the AX 2012 environment should be frozen.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 環境のすべてのコード変更を凍結する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Implement an escalation process to handle any critical issues that appear in AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 で発生する重大な問題を処理するためにエスカレーション プロセスを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>By default, any new code changes that are required should be implemented only in the new system, not in the AX 2012 environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、必要な新しいコード変更は AX 2012 環境ではなく、新しいシステムでのみ実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Implementation of proposed code changes in the AX 2012 environment should be discussed at the management level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 環境での提案されたコードの変更の実装は、管理レベルで説明する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>If a code change is made in AX 2012, the same change must be made in the new system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 でコードを変更した場合、同じ変更は、新しいシステムで行われる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In that case, another iteration of cutover testing and functional testing might be required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その場合、切替テストと機能テストをもう 1 回繰り返す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Application configuration freeze</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション コンフィギュレーションの凍結</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>All application configuration changes should be frozen in the AX 2012 environment, because these changes could affect how the new system behaves or how the data upgrade scripts behave.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの変更は、新しいシステムの動作やデータ アップグレード スクリプトの動作に影響を与える可能性があるため、すべてのアプリケーション コンフィギュレーションの変更を AX 2012 環境で固定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Configuration changes are changes in the AX 2012 application that are related to the configuration of system functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションの変更は、システム機能のコンフィギュレーションに関連する AX 2012 アプリケーションの変更です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>By freezing these changes, you help guarantee the stability of the data upgrade process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの変更を凍結することで、データのアップグレード プロセスの安定性を保証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Because configuration changes are typically controlled by the AX 2012 system administrator or a small group of trusted super users, we don't recommend that you enforce the freeze by changing security access.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションの変更は通常、AX 2012 または信頼済スーパー ユーザーの小規模なグループによって制御されるため、セキュリティ アクセスを変更して凍結を実行することはお勧めしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Instead, implement the freeze through a business process that is communicated to those users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、それらのユーザーに伝達される業務プロセスを通じて凍結を実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Changes to security access might require a code change (changes to the role definitions themselves) or a configuration change (reassignment of users), and these changes could affect the upgrade process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ アクセスの変更には、コード変更 (ロール定義自体の変更) または構成変更 (ユーザーの再割り当て) が必要な場合があり、これらの変更がアップグレード プロセスに影響する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Running the final cutover test</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最終の切替テストの実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>After no further code or setup changes will occur, run a final cutover test to make sure that all data and code upgrade tasks still run as expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後のコードまたは設定の変更がない場合は、すべてのデータとコードの更新タスクが期待どおりに実行されることを確認するために、最終的な切替テストを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>You must complete this step even if you freeze code and setup changes at the beginning of the upgrade project, because the data itself changes every day.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ自体が毎日変更されるため、コードを凍結して、アップグレード プロジェクトの開始時の変更をセットアップする場合でも、このステップを完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>This final cutover test also validates that the current data is upgraded successfully.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、この最終的な切替テストは、現在のデータが正常にアップグレードされたことを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Make sure that functional testing is performed against this last upgraded copy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">機能テストがこの最後にアップグレードしたコピーに対して実行されることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>At this point in the upgrade project, we recommend that you categorize any bugs that are found:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この時点のアップグレード プロジェクトにおいて、検出されたバグを分類することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Blocking<ept id="p1">**</ept> – The upgrade project can't proceed until every bug of this type is fixed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブロック<ept id="p1">**</ept> - このタイプのすべてのバグが修正されるまで、アップグレード プロジェクトは進められません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The upgrade must be postponed, and can proceed only after the bug is remediated and the cutover test is run again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードは延期する必要があり、バグが修復され、切替テストが再度実行された後にのみ進めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For a bug to be classified as blocking, it must meet these conditions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バグをブロックとして分類するには、これらの条件を満たす必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>It prevents a critical business process from being completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、重要な業務プロセスが完了されないようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>No workaround or mitigation is available for it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それに対して利用できる対応策または軽減はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Non-blocking<ept id="p1">**</ept> – The upgrade project can proceed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブロックなし<ept id="p1">**</ept> – アップグレード プロジェクトを進めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Bugs of this type can be fixed in the upgraded system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタイプのバグは、アップグレードされたシステムで修正できます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
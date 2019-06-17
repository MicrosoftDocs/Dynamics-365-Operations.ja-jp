<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="2012-upgrade-cutover.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>2012-upgrade-cutover.166240.bf662bd96bd26e342e696c6de6902d2fc15636aa.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>bf662bd96bd26e342e696c6de6902d2fc15636aa</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\2012-upgrade-cutover.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Upgrade from AX 2012 - Go live (Cutover)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - Go live (切替)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains the final cutover process that starts after you turn off AX 2012 and completes with Dynamics 365 for Finance and Operations running an upgraded version of your code and database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、AX 2012 をオフにしてから、Dynamics 365 for Finance and Operations でコードとデータベースのアップグレード バージョンの実行が完了するまでの最終的な切替えプロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Upgrade from AX 2012 - Go live (Cutover)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - Go live (切替)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>After you have successfully completed upgrade testing in a Standard or Premier Acceptance Test environment (Sandbox Tier 2 or higher), and you have also completed a successful test cutover, the moment has arrived to upgrade your production environment and go live.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準またはプレミア承認テスト環境 (サンドボックス レベル 2 またはそれ以上) でアップグレード テストを正常に完了した場合、および正常にテスト切替を完了した後、実稼働環境をアップグレードして稼働するその時が来ました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source><bpt id="p1">*</bpt>Cutover<ept id="p1">*</ept> is the term that we use for the final process of getting a new system live.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>切替<ept id="p1">*</ept>という用語は、新しいシステムを稼働させる最後のプロセスに使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This cutover process consists of the tasks that occur after Microsoft Dynamics AX 2012 is turned off but before Microsoft Dynamics 365 for Finance and Operations, is turned on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この切替プロセスは、Microsoft Dynamics AX 2012 をオフにした後かつ Microsoft Dynamics 365 for Finance and Operations をオンにする前に発生するタスクで構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Before you plan your final cutover, you need to successfully complete one successful mock cutover as described in <bpt id="p1">[</bpt>Cutover testing<ept id="p1">](./upgrade-cutover-testing.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最終的な切替を計画する前に、<bpt id="p1">[</bpt>切替テスト<ept id="p1">](./upgrade-cutover-testing.md)</ept>で説明されているように成功した切替モックを正常に完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The following illustration shows the overall process for cutover to go-live as it will occur in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、実稼動環境で発生するような、切替中の全体的なプロセスを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Cutover process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">切替プロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>In this article, we use the term <bpt id="p1">*</bpt>sandbox<ept id="p1">*</ept> to refer to a Standard or Premier Acceptance Testing (Tier 2 or 3) or higher environment connected to a SQL Azure database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、<bpt id="p1">*</bpt>サンドボックス<ept id="p1">*</ept> という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 または 3)、またはより高度な環境を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Overall process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全体的なプロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The high-level steps of the production environment upgrade process are the same as the Mock cutover process, refer to <bpt id="p1">[</bpt>Cutover testing<ept id="p1">](./upgrade-cutover-testing.md)</ept> for detailed instructions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼動環境のアップグレード プロセスの高レベルの手順は切替モック プロセスと同じであり、詳細な指示については <bpt id="p1">[</bpt>切替テスト<ept id="p1">](./upgrade-cutover-testing.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Turn off the AX 2012 AOS instances</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 AOS インスタンスをオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Create a copy of the AX 2012 database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 データベースのコピーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>We strongly recommend that you use a copy, because you must delete some objects in the copy that will be exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートするコピーの一部のオブジェクトを削除する必要があるため、コピーを使用することを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Export the copied database to a bacpac file by using a free SQL Server tool that is named SQLPackage.exe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLPackage.exe という名前の無料の SQL Server ツールを使用して、コピーされたデータベースを bacpac ファイルにエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>This tool provides a special type of database backup that can be imported into SQL Database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールでは、SQL データベースにインポートできる特別な種類のデータベース バックアップを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Upload the bacpac file to Azure storage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure ストレージに bacpac ファイルをアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Download the bacpac file to the Application Object Server (AOS) machine in the sandbox environment, and then import it by using SQLPackage.exe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス環境で bacpac ファイルを Application Object Server (AOS) コンピューターにダウンロードし、SQLPackage.exe を使用してインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You must then run a script against the imported database to reset the SQL database users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL データベースのユーザーをリセットするには、インポートされたデータベースに対してスクリプトを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Run the appropriate data upgrade package against the imported database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートされたデータベースに対して適切なデータ アップグレード パッケージを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Before you can perform an upgrade in the production environment the following prerequisites must be met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼動環境でアップグレードを実行する前に、次の前提条件を満たす必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Complete the code upgrade and data upgrade in a sandbox environment and successfully completed a functional test pass</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス環境でコードのアップグレードとデータのアップグレードを完了し、機能テスト パスを正常に完了しました</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Deploy the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境を配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Before the option to request the deployment of the production environment lights up you must have completed:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境の配置を要求するオプションが点灯する前に完了しておく必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The Subscription estimator in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS のサブスクリプション見積もりツール。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>We use this to help us size your production environment because it provides details of the throughput you’ll require.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要なスループットの詳細を提供しているため、これを使用して実稼働環境のサイズの変更を支援します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The Test phase of the methodology in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS での手法のテスト フェーズ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This is to help ensure that you’re at the stage in your project where you’re ready to start testing in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、プロダクション環境でテストを開始する準備ができているプロジェクトの段階にあることを確認するためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>After a request is submitted to Microsoft to deploy the production environment, it will take roughly 24 hours to deploy, so ensure that you leave enough time for this to happen.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境を配置するために要求が Microsoft に送信された後、配置には、約 24 時間かかるので、そのために十分な時間を確保してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Apply all necessary updates and customizations (AOT deployable packages) to the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての必要な更新プログラムおよびカスタマイズ (AOT 配置可能パッケージ) を実稼動環境に適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>There should not be any code change after signing off on a Mock cutover.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">切替モックでサイン オフした後は、コードを変更しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To schedule an upgrade, request a timeslot with the DSE team by submitting “Other” type service requests from LCS as described in the <bpt id="p1">[</bpt>Upgrade from AX 2012 - Cutover testing (Mock cutover)<ept id="p1">](./upgrade-cutover-testing.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードをスケジュールするには、<bpt id="p1">[</bpt>AX 2012 からのアップグレード- 切替テスト (切替モック)<ept id="p1">](./upgrade-cutover-testing.md)</ept> に説明されているように、LCS から「その他」のタイプのサービスリクエストを送信して、DSE チームにタイムスロットを要求します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>This is to ensure that the preferred timeslots will be available for you.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、優先タイム スロットが使用できるようにすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Be aware that there is significantly higher demand for slots during the weekend, so requesting these as far in advance as possible will help attain your preferred schedule.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">週末の間などスロットの需要が大幅に高くなるため注意してください。できるだけ早くこれらを要求することにより優先スケジュールを達成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Related articles</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連記事</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">[</bpt>Onboarding<ept id="p1">](../../fin-and-ops/imp-lifecycle/onboard.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Onboarding<ept id="p1">](../../fin-and-ops/imp-lifecycle/onboard.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">[</bpt>Submit a service request<ept id="p1">](../lifecycle-services/submit-request-dynamics-service-engineering-team.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>サービス要求を送信する<ept id="p1">](../lifecycle-services/submit-request-dynamics-service-engineering-team.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">[</bpt>Upgrade from AX 2012 - Cutover testing<ept id="p1">](./upgrade-cutover-testing.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>AX 2012 からのアップグレード - 切替テスト<ept id="p1">](./upgrade-cutover-testing.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
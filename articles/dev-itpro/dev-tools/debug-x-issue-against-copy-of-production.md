<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="debug-x-issue-against-copy-of-production.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>debug-x-issue-against-copy-of-production.a95891.e27236865d9621354e725192ce50c16955d83fc6.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e27236865d9621354e725192ce50c16955d83fc6</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\debug-x-issue-against-copy-of-production.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Debug X++ against copies of production databases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産データベースのコピーに対する X++ のデバッグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to configure X++ debugging so that you can investigate issues in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、実稼働環境で問題を調査できるように X++ デバッグを構成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Debug X++ against copies of production databases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産データベースのコピーに対する X++ のデバッグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to configure X++ debugging so that you can investigate issues in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、実稼働環境で問題を調査できるように X++ デバッグを構成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For this procedure, you make a copy of the production database and then configure a developer environment to connect to the copy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順では、生産データベースのコピーを作成し、コピーに接続するための開発環境をコンフィギュレーションします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Solution overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When an issue that requires X++ debugging occurs in a production environment, the system administrator and developer work together to configure debugging and then debug the issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境で X++ のデバッグが必要な問題が発生したときは、システム管理者と開発者は連携して、デバッグを構成してから問題をデバッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The following illustration shows an overview of the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、プロセスの概要を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Debugging process<ept id="p1">](./media/debugxpp.jpg)](./media/debugxpp.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>デバッグ プロセス<ept id="p1">](./media/debugxpp.jpg)](./media/debugxpp.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>In Microsoft Dynamics Lifecycle Services (LCS), the system administrator requests that a copy of the database be connected to the sandbox user acceptance testing (UAT) environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) では、システム管理者がデータベースのコピーをサンドボックス ユーザー受け入れテスト (UAT) に接続するよう要求します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>(In other words, request a database refresh.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(つまり、データベース更新を要求します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In Microsoft Azure DevOps, the developer synchronizes the local code to the same build that is running in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Azure DevOps では、開発者が実稼働環境で実行されている同じビルドにローカル コードを同期します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>In the sandbox instance of Microsoft Azure SQL Database, the system administrator creates a temporary SQL sign-in for the developer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Azure SQL データベースのサンドボックス インスタンスでは、システム管理者が開発者に一時的な SQL サインインを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The developer then configures the environment to connect to the sandbox database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は、サンドボックス データベースに接続するための環境を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>A firewall exception is added so that the developer environment can connect to the sandbox database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境がサンドボックスのデータベースに接続できるように、ファイアウォールに例外が追加されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The developer debugs the issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は問題をデバッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>When debugging is completed, the system administrator can remove the temporary sign-in from the sandbox SQL database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッグが完了したら、システム管理者は、一時的なサインインをサンド ボックスの SQL データベースから削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Before you begin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Before you begin to configure X++ debugging in a production environment, note the following points:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境で X++ デバッグ を構成する前に、次の点に注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You can't debug directly against the production environment, because debugging might cause data corruption.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッグためにデータの破損が発生する可能性がありますので、実稼働環境を直接デバッグできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>However, developers can manipulate values at runtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、開発者は実行時に値を操作できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Alternatively, in their own instance, developers can make a code change that changes data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">あるいは、独自のインスタンスでは、開発者はデータを変更するコード変更を行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The developer environment that is used for debugging must exist in the same LCS project as the sandbox environment, and both of them must be Microsoft managed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッグに使用される開発環境はサンドボックス環境と同じ LCS プロジェクトに存在する必要があり、両方とも Microsoft により管理されている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>This requirement helps strengthen the security of the sandbox database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要件は、サンドボックス データベースのセキュリティを強化するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>By default, there is a firewall restriction on both the sandbox and production SQL databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、サンドボックスと生産 SQL データベースの両方にファイアウォールの制限があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>This restriction allows only servers in those environments to connect to the databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この制限により、これらの環境内のサーバーのみがデータベースに接続できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>To enable debugging, a firewall exception is added so that a developer environment can connect to the sandbox database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッグを有効にするため、開発環境がサンドボックスのデータベースに接続できるように、ファイアウォールに例外が追加されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>A one-time manual change to the developer environment is required, so that the IP address of the environment can connect to the sandbox database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の IP アドレスがサンドボックス データベースに接続できるようにするため、開発者環境への 1 回限りの手動変更が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Create a support request with Microsoft support asking to allow the IP address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マイクロソフト サポートでサポート リクエストを作成し、IP アドレスの許可を依頼します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>We recommend that you not use a build environment for debugging.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッグにビルド環境を使用しないことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Otherwise, there is a risk that the developer's activities on the computer might break the automated build process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、コンピュータで開発者の活動が自動ビルド プロセスを中断するリスクがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Solution details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションの詳細</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When an issue occurs in the production environment, the system administrator can sign in to LCS and request that a database copy be added to a sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼動環境で問題が発生する場合は、システム管理者は LCS にサインインして、データベースのコピーをサンド ボックス環境に追加するように要求できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>While the database copy is running, the system administrator can notify the developer of the issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのコピーの実行中、システム管理者は開発者に問題について通知することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The developer can then synchronize to the correct build of the code to match the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は、コードの正しいビルドに同期して、実稼働環境に合わせることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>In Microsoft Visual Studio, in Source Control Explorer, right-click the root node of the branch to synchronize, and then select <bpt id="p1">**</bpt>Advanced<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Get specific version<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio のソース管理エクスプローラーで、同期するブランチのルート ノードを右クリックしてから、<bpt id="p1">**</bpt>詳細<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> を選択して、<bpt id="p2">**</bpt>特定のバージョンを取得を選択します<ept id="p2">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>In the dialog box, select <bpt id="p1">**</bpt>Type=Label<ept id="p1">**</ept>, and then select the ellipsis (<bpt id="p2">**</bpt>...<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで、<bpt id="p1">**</bpt>Type=Label<ept id="p1">**</ept> を選択してから省略記号 (<bpt id="p2">**</bpt>...<ept id="p2">**</ept>) を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In the dialog box, select <bpt id="p1">**</bpt>Find<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで<bpt id="p1">**</bpt>検索<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>All the builds from the build server are listed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド サーバーからのすべてのビルドがリストに記載されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Select the build that is currently deployed in the production environment, and then select to run a full build.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼動環境に現在配置されているビルドを選択し、フル ビルドの実行を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>When the database is copied, only the system administrator will be able to access the sandbox database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースをコピーすると、システム管理者のみがサンド ボックス データベースにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The system administrator must complete the following tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム管理者は、次のタスクを完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Remove any data that you don't want in the sandbox database, such as employee salaries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">従業員の給与など、サンドボックス データベースに不要なデータを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Enable or add the developer as a user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーとして、開発者を有効または追加にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Create a new SQL sign-in that the developer can use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者が使用できる新しい SQL サインインを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>This step lets the system administrator maintain the security of the sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップにより、システム管理者はサンドボックス環境のセキュリティを維持できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The developer will have access to one database for only a limited time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は限られた時間だけ 1 つのデータベースにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Use the following code to create the new SQL sign-in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい SQL サインインを作成するには、次のコードを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Next, the developer edits the web.config file for Application Object Server (AOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、開発者は、Application Object Server (AOS) の web.config ファイルを編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Go to <bpt id="p1">**</bpt>J:<ph id="ph1">\\</ph>AosService<ph id="ph2">\\</ph>WebRoot<ph id="ph3">\\</ph>web.config<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>J:<ph id="ph1">\\</ph>AosService<ph id="ph2">\\</ph>WebRoot<ph id="ph3">\\</ph>web.config<ept id="p1">**</ept> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Save a copy of the original web.config file, so that you can switch back later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後で切り替えることができるように、元の web.config ファイルのコピーを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Edit the following section in the web.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">web.config ファイルの次のセクションを編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Before your changes<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>変更前<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>After your changes<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>変更後<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Debug the issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題をデバッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>After the developer has finished, the system administrator can remove devtempuser from the sandbox database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者が終了すると、 システム管理者はサンドボックス データベースから devtempuser を削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This step prevents the developer from having permanent access to the sandbox database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップにより、開発者はサンドボックス データベースに永続的にアクセスできなくなります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
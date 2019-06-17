<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="updating-environments.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>updating-environments.f78c3e.3dd56c17f92aed76c19e3e82dd32c651723d4c1c.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>3dd56c17f92aed76c19e3e82dd32c651723d4c1c</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\updating-environments.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Update code and environments for Retail projects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードおよび小売プロジェクトの環境の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes recommended practices for updating code and environments for Microsoft Dynamics 365 for Retail implementation projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Retail の更新コード、および環境の推奨事項について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Update code and environments for Retail projects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail プロジェクトのコードと環境の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>An environment can be updated by updating either its data or its code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データまたはコードのいずれかを更新することにより、環境を更新できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>There are multiple ways to update the data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データを更新する複数の方法があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For examples that show how to get data into an environment, see <bpt id="p1">[</bpt>Data entities and data packages<ept id="p1">](../../dev-itpro/data-entities/integration-overview.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境にデータを取得する方法を示す例については、<bpt id="p1">[</bpt>データ エンティティおよびデータ パッケージ<ept id="p1">](../../dev-itpro/data-entities/integration-overview.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When you update an environment, you should also consider moving the whole database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境を更新するときは、データベース全体の移動も考慮する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This approach lets you quickly and easily duplicate the data from one environment to another.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアプローチにより、データをある環境から別の環境に素早く簡単に複製できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Other updates are code updates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の更新プログラムは、コードの更新プログラムです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The environment page in Microsoft Dynamics Lifecycle Services (LCS) tracks the updates that have been applied and the updates that must be applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) の環境ページでは、適用された更新プログラムおよび適用が必要な更新プログラムを追跡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The following illustration shows an environment that has 79 outstanding X++ fixes, 14 outstanding binary updates, and nine outstanding platform binary updates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、79 の未処理 X++ ファイル、14 の未処理のバイナリ更新プログラムおよび 9 の未処理プラットフォーム バイナリ 更新プロセスを持つ環境を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>LCS environment page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS 環境ページ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Platform code is at a very low level, and no Microsoft Dynamics 365 for Retail features are implemented in the platform.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム コードは、非常に低いレベルであり、Microsoft Dynamics 365 for Retail 機能はプラットフォームに実装されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Therefore, stand-alone platform binary updates don't require that you retest any Retail-specific code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、スタンドアロン プラットフォームのバイナリ アップデート プログラムでは、Retail 固有のコードを再テストすることは不要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Examples of features that are implemented in the platform are the Data Import/Export Framework (DIXF) and the batch framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォームに実装されている機能の例としては、データのインポート/エクスポート フレームワーク (DIXF) およびバッチ フレームワークです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Binary updates or hotfixes include dynamic-link libraries (DLLs), scripts, and channel SQL schema changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バイナリ更新プログラムまた修正プログラムには、ダイナミック リンク ライブラリ (DLL)、スクリプト、およびチャネル SQL スキーマの変更が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>All channel-side hotfixes are released together as a binary update/hotfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル側のすべての修正プログラムは、バイナリ更新プログラム/修正プログラムと同時にリリースされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Because binary updates are DLLs, they are cumulative.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バイナリ更新プログラムは DLL であるため、累積されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For example, if you download a binary update on Friday, you automatically receive all binary hotfixes from Monday through Thursday.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、金曜日にバイナリの更新プログラムをダウンロードする場合は、すべてのバイナリ修正プログラムを月曜日木曜日まで自動的に受信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>If the code merge is done correctly, the version of a binary hotfix that you take matches the version of the Microsoft-version.txt file in the Retail software development kit (SDK).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード マージが正しく行われている場合、binary 修正プログラムのバージョンは Retail ソフトウェア開発キット (SDK) の Microsoft-version.txt ファイルのバージョンと一致します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Typically, binary updates are also linked to the latest platform.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、バイナリ更新プログラムは最新のプラットフォームにもリンクされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Therefore, when you take binary updates, you must stay up to date with the platform.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、バイナリ アップデートを取得する場合は、プラットフォームを最新の状態に保つ必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Platform updates help increase the stability of the platform, and they affect build environments and test efforts to some extent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラムはプラットフォームの安定性を向上させ、ビルド環境に影響を与え、いくらかの範囲の作業をテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Application updates or hotfixes are delivered in X++ source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの更新プログラムまたは修正プログラムは、X++ ソース コードで配信されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Therefore, they aren't for the channel side but for the Microsoft Dynamics 365 side (they are either Retail-related or not Retail-related).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、チャンネル側ではなく、Microsoft Dynamics 365 側 (Retail 関連または Retail 関連ではない) です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Note that some updates require both an application update and a binary update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部の更新プログラムがアプリケーションの更新プログラムとバイナリの更新プログラムの両方を必要とすることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For hotfix recommendations, see the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正プログラムの推奨事項については、次のセクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Third-party packages resemble application packages, but they are developed by other people.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サード パーティ パッケージは、アプリケーション パッケージと似ていますが、他のユーザーによって開発されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>For more information about how to use independent software vendor (ISV) packages, see <bpt id="p1">[</bpt>Manage Runtime Packages<ept id="p1">](../../dev-itpro/dev-tools/manage-runtime-packages.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">独立系ソフトウェア ベンダー (ISV) パッケージの使用方法の詳細については、<bpt id="p1">[</bpt>ランタイム パッケージの管理<ept id="p1">](../../dev-itpro/dev-tools/manage-runtime-packages.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Updating data by restoring the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを復元してデータを更新する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>In one useful and typical operation, the whole database is moved from one environment to another.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">便利で一般的な操作の 1 つでは、データベース全体が 1 つの環境から別の環境に移動されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>For example, you might move the production database to development environments when you're preparing to develop additional features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、追加機能を開発する準備をしているときに、生産データベースを開発環境に移動することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Alternatively, you might move the golden setup database to the production database as part of the go-live process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、運用プロセスの一部として、ゴールデン セットアップ データベースを生産データベースに移動することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>For more details, see <bpt id="p1">[</bpt>Copy Database From Azure SQL to SQL Server<ept id="p1">](../../dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>Azure SQL から SQL Server へのデータベースのコピー<ept id="p1">](../../dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If source and destination environments don't have the same binary version, you should also do either a build and a database synchronization (for a development environment), or a deployment (for a sandbox or production environment).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソースおよび宛先の環境に同じ binary バージョンがない場合、ビルドおよびデータベースの同期 (開発環境の) または配置 (サンドボックスまたは実稼働環境の) のいずれかを行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Every time that a database that has been moved from a different environment is restored, specific links in the database can be broken.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別の環境から移動されたデータベースを復元するたびに、データベース内の特定のリンクは、中断することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The Environment reprovisioning tool fixes all these broken links for the default database group, regardless of type of environment that is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境再プロビジョニング ツールでは、使用されている環境タイプに関係なく、既定データベース グループのすべての壊れたリンクを修正します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The general guideline is that if the database comes from a different environment, the Environment reprovisioning tool must be run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的なガイドラインでは、データベースが別の環境から来る場合、環境再プロビジョニング ツールを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In many cases, you should reset the Retail scheduler after you update the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、データベースを更新した後、小売用スケジューラをリセットする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>After you've restored the database, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを復元した後は、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Either do a build and a database synchronization, or deploy the deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドとデータベースの同期を行うか、配置可能パッケージを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>If you have table extensions that include data, you must have the metadata for those extensions in the environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データを含むテーブルの拡張機能をご使用の場合は、環境内の拡張機能のためのメタデータが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Otherwise, you can lose data, because columns and tables might be dropped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合は、列と表が削除される可能性があるため、データを失うことがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Make sure that the batch service is running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ サービスが実行中であることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Run the Environment reprovisioning tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境再プロビジョニング ツールを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>(Find the latest version in the global Shared asset library in LCS, and then deploy it by using the <bpt id="p1">**</bpt>Maintain<ept id="p1">**</ept> function.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(LCS のグローバル共有資産ライブラリで最新バージョンを見つけて、<bpt id="p1">**</bpt>Maintain<ept id="p1">**</ept> 関数を使用して展開します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Verify that the tool succeeded, the Retail channel profile is up to date with the correct URLs, and the data synchronization jobs for the Default data group succeeded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールが成功し、小売チャネル プロファイルが正しい URL で最新であり、既定のデータ グループのデータ同期ジョブが成功したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In Microsoft Dynamics 365 for Finance and Operations, run the <bpt id="p1">**</bpt>Initialize Retail scheduler<ept id="p1">**</ept> job (select to delete old data).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations では、古いデータを削除するために <bpt id="p1">**</bpt>小売用スケジューラの初期化<ept id="p1">**</ept>ジョブ (古いデータを削除するために選択) を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>This step assumes that all Commerce Data Exchange (CDX) configuration changes are automated by using a resource file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順では、すべての Commerce Data Exchange (CDX) コンフィギュレーションの変更がリソース ファイルを使用して自動化されていることを前提としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>If CDX configuration changes aren't automated, and if tables, subjobs, and jobs are manually created in the Retail channel schema, don't select the option to delete the existing configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX のコンフィギュレーションの変更が自動化されていない場合、およびテーブル、サブジョブ、およびジョブが手動で小売チャネルのスキーマで作成された場合、既存のコンフィギュレーションを削除するオプションを選択しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>We recommend that you automate CDX configuration changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX のコンフィギュレーションの変更を自動化することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Taking updates frequently</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">頻繁にプログラムを更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If your project is more than a few weeks from go-live or the final user acceptance testing (UAT), we recommend that you take all hotfixes (binary, X++, and platform) on a regular schedule.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトが go-live または最終的なユーザー受け入れテスト (UAT) から数週間以上かかる場合は、すべての修正プログラム (binary、X++、およびプラットフォーム) を定期的に実行することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Specifically, we recommend that you take all hotfixes one time per month.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">具体的には、すべての修正プログラムを月に 1 回は実行することを勧めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The more often you perform this task, the fewer issues you should experience, because the code churn of the hotfixes is smaller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスクを実行する頻度は高く、修正プログラムのコード チャーンが小さいため、少数の問題が発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>If you perform this task often, it will take significantly less than eight hours.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスクを頻繁に実行する場合、大幅に 8 時間を下回ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>We recommend that you not pick and choose hotfixes, because this approach is more likely to cause errors and probably isn't worth your time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正プログラムはエラーが発生する可能性が高く、おそらく時間をかける価値がないため、この方法を選択しないことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>If you have 500 or 1,000 outstanding hotfixes, you should consider whether you're really ready to go-live.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">500 または 1,000 の未解決の修正プログラムがある場合、go-live の準備ができているかどうか検討する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The quality of the product will be higher if the count on the update tiles in LCS is very low (fewer than 100 application fixes and fewer than ten binary fixes).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS の更新プログラムのタイル数が非常に低い場合、製品の品質は高くなります (100 未満のアプリケーションの修正プログラムおよび 10 未満のバイナリ修正プログラム)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>After you take new hotfixes, the results of a previous round of UAT become less meaningful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい修正プログラムを実行した後は前回の UAT の結果はあまり意味のないものになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Therefore, it's crucial to retest again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、もう一度再テストをすることは重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The number of files that changed determines how extensive the testing must be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更されたファイルの数は、どれくらいの広さのテストが必要か決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>If hotfixes are frequently taken, especially during the implementation phase, the number of new files isn't very large, and the retesting effort is manageable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特に実装フェーズ中に修正プログラムを頻繁に使用する場合、新しいファイルの数がそれほど多くないため、再テスト作業が管理しやすくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Another approach is to take all hotfixes frequently and run only part of the UAT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別の方法は、すべての修正プログラムを頻繁に実行し、UAT の一部のみを実行することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Then, the next time that new hotfixes are taken, run a different part of the UAT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、次回新しい修正プログラムが実行される時に、UAT の別の部分を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Run the different parts of the UAT in a circular manner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UAT の様々な部分を循環的に実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Before go-live, you should do a full UAT run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">稼働前に、UAT の全実行を行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The flow of code changes through branches and environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブランチおよび環境を介するコード変更の流れ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Just as the branching strategy is dictated by project, team, or other constraints, your project has flexibility about how the changes are propagated through the branches.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分岐戦略がプロジェクト、チーム、またはその他の制約によって決まるのと同様に、プロジェクトは分岐を通じてどのように変更が反映するかについて柔軟に対応します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The following illustration shows an example of the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、プロセスの例を表示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>However, this example might be too simple for some projects and too complex for other projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、この例は、いくつかのプロジェクトには単純過ぎ、また他のプロジェクトには複雑過ぎるかもしれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The important point is that a project should have a plan.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な点は、プロジェクトが計画を用意する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Different persons in the team will have different responsibilities (development, deployment, code merges, sign-off, and so on), and the role ownership should be clearly defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チーム内の異なる人が異なる責任 (開発、配置、コード マージ、サインオフなど) を持ち、ロールの所有権を明確に定義する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Branch diagram</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分岐図</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Steps 1–3: Obtain and apply updates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 1–3: 更新プログラムを取得および適用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>For full details about steps 1 through 3 (taking updates), see <bpt id="p1">[</bpt>Dynamics 365 for Finance and Operations hotfix and deployment cheat sheet (including Retail)<ept id="p1">](https://dynamicsnotes.com/dynamics-365-for-finance-and-operations-hotfix-and-deployment-cheat-sheet/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 1〜3 (更新を行う) の全詳細については、<bpt id="p1">[</bpt>Dynamics 365 for Finance and Operations の修正プログラムと配置のチート シート (Retail を含む)<ept id="p1">](https://dynamicsnotes.com/dynamics-365-for-finance-and-operations-hotfix-and-deployment-cheat-sheet/)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If the branches are set up in the same manner that is shown in the preceding illustration, you should do this work in the Dev branch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブランチが前の図に示されているのと同じように設定されている場合は、開発ブランチでこの作業を行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Steps 3.1–3.2: Keep development environments up to date</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 3.1–3.2: 開発環境を最新へ保持</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>You don't have to have a build environment for the Dev branch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発ブランチのためのビルド環境を用意する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>In fact, a build environment for the Dev branch isn't usually required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実際には、Dev 分岐のためのビルド環境は、通常必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>You just have to coordinate the packages that should be deployed to keep the version correct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョンを正しく保持するには、配置するパッケージを調整する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>After you download binary updates and platform updates, you can deploy them via LCS package deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バイナリ更新プログラムとプラットフォーム更新プログラムをダウンロードした後、LCS のパッケージ展開を使用して展開できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>For the X++ code, developers just synchronize the Metadata folder and do a full build and database synchronization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X ++ コードの場合、開発者はメタデータ フォルダを同期し、フル ビルドおよびデータベース同期を行うだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>If major new Retail changes have been checked in by other members of the team (for example new files, configuration changes, or a new Retail SDK), it isn't enough to synchronize and build the new files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チームの他のメンバーが新しい小売の主要な変更をチェック インした場合 (例えば、新しいファイル、コンフィギュレーションの変更、または新しい Retail SDK)、新しいファイルを同期してビルドするだけでは不十分です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Remember that a few web applications that are installed on the developer machine won't be updated through a compilation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者のマシンにインストールされているいくつかの Web アプリケーションは、コンパイルでは更新されませんので注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Those web applications must be deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それらの Web アプリケーションは、展開する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Use the LCS package deployment to deploy the retail package that can be produced at an MSBuild command prompt.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS パッケージ配置を使用して、MSBuild コマンド プロンプトで生成できる小売パッケージを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>For smaller code changes, new package deployments aren't required in order to keep the dev environments in sync if the incremental changes are dropped to the install locations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">より小規模なコード変更の際、増分変更がインストール先から削除されているなら、開発環境の同期を保つために新しいパッケージの展開は必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Environment change history</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の変更履歴</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Step 4: Move changes from the Dev branch to the Main branch</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 4: Dev ブランチから Main ブランチへの変更を移動</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>In this example, the Dev and Main branches have been separated to provide an opportunity to "leave some unwanted changes behind."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、Dev 分岐と Main 分岐が分離され、「不要な変更を残す」機会を提供しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Although this approach isn't required, it's a good option to have.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアプローチは必須ではありませんが、それは良い選択です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Microsoft Visual Studio makes the process of moving the code from Dev to Main easy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio を使用すると、Dev から Main へコードを簡単に移動できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>You can select a range of changes, select all or individual changes, and merge those changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更の範囲、すべてまたは個々の変更を選択し、それらの変更をマージすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>To keep the process simple, you can have some type of a code freeze in the Dev branch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスを単純に保つために、Dev 分岐で何らかのタイプのコード凍結を行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Then, when you're satisfied with the quality, you can merge all changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、品質に問題がなければ、すべての変更をマージできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>There is no reason to treat X++ differently than the Retail SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ を Retail SDK と異なる扱いをする理由はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>They reside next together in each branch, because they are dependent on each other.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それらは相互に依存しているので、各分岐で隣同士に配置されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Steps 4.1–4.2: Update test environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 4.1–4.2: テスト環境の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Use your build environment to produce officially built packages from the code in the Main branch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド環境を使用して、Main ブランチのコードから正式に構築されたパッケージを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Build Definitions Unified Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド定義の Unified Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>When the build is completed, find the packages that were built, download them, and rename them according to your naming conventions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドが完了したら、ビルドされたパッケージを見つけてダウンロードし、名前付け規則に従って名前を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Artifacts Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネント エクスプ ローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Then upload the packages to the LCS Asset library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、LCS アセット ライブラリにパッケージをアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Asset library</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アセット ライブラリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Finally, deploy the packages to your test environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、テスト環境にパッケージを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Environment change history UAT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の変更履歴 UAT</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Step 4.3: Deploy packages to the production environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 4.3: パッケージを運用環境に展開</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>When all the required tests are passed, you're ready to deploy the same packages to production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要なテストがすべて完了したら、同じパッケージを生産に配置する準備が整います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>After the packages have been deployed and validated in a Tier 2 or higher environment, you must mark them as Release Candidates in the LCS Asset library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージがレベル 2 以上の環境で配備され、検証されたら、それらを LCS 資産ライブラリのリリース候補としてマークする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>You must then plan the deployment and submit it via the LCS environment page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置を計画し、LCS 環境ページを使用して送信する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>There are many considerations when you update a production environment, such as downtime, downtime mitigation, data migration, store updates, and mass deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンタイム、ダウンタイムの軽減、データ移行、ストアの更新、および一括配置など、運用環境を更新するときには、多くの考慮事項があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>It's very important that you have a plan of all the steps that are required for an update, because Retail projects usually require more than just deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売プロジェクトでは、通常、配置以上のものが必要となるため、更新に必要なすべての手順を計画することが非常に重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>For some additional considerations, see the "Tips" section of this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつか追加の考慮事項は、このトピックの「ヒント」セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>It's assumed that the planning for go-live was started much earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Go-Live の計画がかなり早く開始されたと見なされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>For more details, see <bpt id="p1">[</bpt>Implementation lifecycle<ept id="p1">](../../fin-and-ops/imp-lifecycle/implementation-lifecycle.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>実装ライフサイクル<ept id="p1">](../../fin-and-ops/imp-lifecycle/implementation-lifecycle.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Step 5: Merge the code from the Main branch to the ProdRel1 branch</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 5: Main ブランチから ProdRel1 ブランチへコードをマージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Immediately after deployment to production, and before any new feature work is added to the Main branch, you should take a snapshot and move it to the ProdRel1 branch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産への配置直後、および新しい機能の作業がメインブランチに追加される前に、スナップショットを取得し、ProdRel1 ブランチに移動してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The steps are the same as in step 4.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順は、手順 4 と同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>You don't have to select individual changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">個々の変更を選択する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Instead, just merge all changes up to the last code change set that was submitted to the Main branch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、Main 分岐に提出された最後のコード変更セットまでのすべての変更をマージしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Update build environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド環境の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>You should always deploy binary updates and platform updates by using LCS package deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS パッケージ配置を使用して、常にバイナリ更新プログラムおよびプラットフォーム更新プログラムを配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Finance and Operations and Retail customization packages should not be deployed to a build environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations、および小売カスタマイズ パッケージは、ビルド環境に配置することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Environment change history build</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の変更履歴のビルド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Compare LCS tile counts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS タイル カウントの比較</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Environments that are used for work of the same release should also have the same LCS tile counts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じリリースの作業に使用される環境には、同じ LCS タイル カウントが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Here are some reasons why the tile counts might differ:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイル数が異なるいくつかの理由は以下の通りです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The same deployable packages haven't been deployed and applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ展開可能なパッケージは、展開および適用しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>You can troubleshoot this issue by inspecting and comparing the LCS deployment history.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS の配置履歴を調査し比較することで、この問題のトラブルシューティングが可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>The scheduled task that collects the version information from an environment hasn't been run yet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境からバージョン情報を収集するスケジュール タスクは、まだ実行されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>For development environments, you can force the "LCSDiagnosticsCollector" schedule task to run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境では、「LCSDiagnosticsCollector」スケジュール タスクを実行を強制できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The counts for the build environment's application updates don't match because X++ packages aren't deployed on build environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ パッケージがビルド環境に配置されていないため、ビルド環境のアプリケーション更新数は一致しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Binary and platform counts should be correct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バイナリとプラットフォームの数は正しいです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The difference might be intentional.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">違いは、意図的な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>For example, a developer might work with the next version, whereas the rest of the team is still working with a different release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、開発者は次のバージョンの作業をし、残りのチームはまだ別のリリースの作業をしている場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Alternatively, one development environment might be kept on an older version in case a production hotfix must be developed, and that production environment uses an older version than current development environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、本番環境の修正プログラムを開発しなければならない場合や、現行の開発環境より古いバージョンを使用する場合は、1 つの開発環境を古いバージョンに保つこともできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Notice that after you've finished updating an environment, the tile counts for the available updates are significantly lower than they were when you started.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の更新が完了すると、利用可能な更新プログラムのタイル カウントが、開始時よりも大幅に少なくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>LCS Dev Environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS 開発環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Move to a new version</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいバージョンへの移動</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>To upgrade to a new version (such as 7.2 to 7.3 or 7.3 to 8.0), you must deploy a new environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいバージョン (7.2 から 7.3、7.3 から 8.0 など) にアップグレードするには、新しい環境を配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>You must also run a code upgrade and a database upgrade, if these upgrades are applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのアップグレードが適用可能な場合は、コードのアップグレードとデータベースのアップグレードも実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>For more details, see <bpt id="p1">[</bpt>Code migration home page<ept id="p1">](../../dev-itpro/migration-upgrade/code-migration-home-page.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>Code の移行ホーム ページ<ept id="p1">](../../dev-itpro/migration-upgrade/code-migration-home-page.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Tips</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヒント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Decide on a good package naming convention for names in the LCS Asset library and for the names of zip packages that are downloaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS アセット ライブラリの名前とダウンロードされた zip パッケージの名前について、適切なパッケージ名の名前付け規則を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>In this way, you can more easily determine what package you've deployed and where it came from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようにして、配置したパッケージと送信元を簡単に確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Avoid spaces in package names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージ名にスペースを避けてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Here is an example of a naming convention:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前付け規則の例は次の通りです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source><bpt id="p1">**</bpt>Platform update packages:<ept id="p1">**</ept> PUXX_MMDDYY, where XX is the number of the platform update</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プラットフォームの更新プログラム:<ept id="p1">**</ept> PUXX_MMDDYY の XX はプラットフォームの更新プログラムの番号です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source><bpt id="p1">**</bpt>Binary update packages:<ept id="p1">**</ept> BIN_MMDDYY</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Binary 更新プログラム パッケージ:<ept id="p1">**</ept> BIN_MMDDYY</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source><bpt id="p1">**</bpt>X++ update packages:<ept id="p1">**</ept> APP_MMDDYY</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>X++ 更新プログラム パッケージ:<ept id="p1">**</ept> APP_MMDDYY</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source><bpt id="p1">**</bpt>Built X++ deployable packages:<ept id="p1">**</ept> AX_BRANCH_VERSION, where BRANCH is an appropriate branch name, and VERSION is the Microsoft Azure DevOps version string</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構築された X++ 配置可能パッケージ:<ept id="p1">**</ept> AX_BRANCH_VERSION の BRANCH には適切な分岐の名前、VERSION は Microsoft Azure DevOps のバージョンの文字列になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source><bpt id="p1">**</bpt>Built Retail combined package:<ept id="p1">**</ept> RET_BRANCH_VERSION, where BRANCH is an appropriate branch name, and VERSION is the Azure DevOps version string</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構築された Retail 組み合わせパッケージ:<ept id="p1">**</ept> RET_BRANCH_VERSION の BRANCH には適切な分岐の名前、VERSION には Azure DevOps のバージョン文字列になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Whenever you start a new item of work, use the <bpt id="p1">**</bpt>Get latest<ept id="p1">**</ept> option in the Visual Studio source code explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい作業項目を開始するたびに、Visual Studio のソース コード エクスプローラーで<bpt id="p1">**</bpt>最新を取得<ept id="p1">**</ept>オプションを使用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Any code submissions should use correct and detailed comments that describe the change sets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの送信は、変更セットを説明する正確かつ詳細なコメントを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Production go-live procedures are important.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産 Go-Live 手順は、重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>You should consider including the following items on your Go-live checklist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Go-live チェックリストに次の項目を含めることを検討する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Verify your Go-live checklist in a mock go-live or UAT environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モック Go-Live もしくは UAT 環境で Go-Live チェックリストを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>This list isn't exhaustive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このリストは、包括的ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>After deployment, does LCS show the expected deployment history together with the correct package names?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開後、LCS は正しいパッケージ名とともに予想される展開の履歴を表示しますか？</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>After deployment, do the LCS environment page and Finance and Operations show the correct and expected version numbers?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開後、LCS 環境ページおよび Finance and Operations は、は正しいバージョン番号と予測されるバージョン番号を表示しますか？</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Can Retail Modern Point of Sale (MPOS) offline mode be used during downtime of Operations and Finances?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern 販売時点管理 (MPOS) オフライン モードは、Operations and Finances のダウンタイム中に使用できますか？</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Package deployments will cause downtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージ配置には、ダウンタイムが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>If MPOS offline mode can be used, have you tested the procedure?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS オフラインモードが使用できる場合は、手順をテストしましたか？</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>(To test the procedure, go offline, deploy, go online, synchronize offline transactions, and update MPOS.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(プロシージャをテストするには、オフライン、展開に移動し、オンライン、オフラインのトランザクションの同期に移動し、MPOS を更新します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Does the Environment reprovisioning tool have to be run (if a database has been moved)?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境再プロビジョニング ツールを実行する必要がありますか (データベースが移動している場合)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Batch jobs for CDX synchronization must be reenabled by setting them to <bpt id="p1">**</bpt>Waiting<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX 同期のバッチ ジョブは、<bpt id="p1">**</bpt>待機中<ept id="p1">**</ept>に設定することで再び有効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>The "Initialize Retail scheduler" job should be run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「小売用スケジューラを初期化」ジョブを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Does other data have to be set up in addition to the deployable packages (for example, screens, buttons, receipt layouts, the Microsoft Azure Active Directory setup, Retail shared parameters, the tax configuration, other batch processes, and DIXF recurring jobs)?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージ (例: 画面、ボタン、レシートのレイアウト、Microsoft Azure Active Directory セットアップ、小売共有パラメーター、税コンフィギュレーション、その他のバッチ処理、DIXF の定期ジョブ) に加えて他のデータを設定する必要がありますか？</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Is a synchronization of the CDX data jobs required?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX データ ジョブの同期は必須ですか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Is a full synchronization of CDX data jobs required?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX データ ジョブの完全な同期は必須ですか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Does a deployment require that store components also be updated?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置には店舗のコンポーネントの更新も必要ですか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>If the store components had to be updated, do they show the new version numbers?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗のコンポーネント更新が必要な場合、新しいバージョン番号を表示しますか？</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Are the correct experts available during the deployment (for example, partners, ISVs, and customers)?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(たとえば、パートナー、ISV、および顧客) 配置中に正しいエキスパートが使用可能ですか？</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source><bpt id="p1">[</bpt>Set up new environments, Azure DevOps, and branches for Retail projects<ept id="p1">](./new-environments-visual-studio-teams-branch-retail-projects.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail プロジェクトの新しい環境、Azure DevOps、およびブランチの設定<ept id="p1">](./new-environments-visual-studio-teams-branch-retail-projects.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source><bpt id="p1">[</bpt>Testing and performance<ept id="p1">](./retail-implementation-testing-performance.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>テストおよびパフォーマンス<ept id="p1">](./retail-implementation-testing-performance.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
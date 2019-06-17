<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="version-models-build.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>version-models-build.2b3823.56bb21583635987cff1b7f9faa83b104622baa20.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>56bb21583635987cff1b7f9faa83b104622baa20</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\version-models-build.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Update model versions in the automated build</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動ビルドのモデル バージョンの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>The topic explains how you can update the models in a source package and deployable package of the build output with the version of the build that produced them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、ビルド出力のソース パッケージと配置可能なパッケージのモデルを、それらを生成したビルドのバージョンで更新する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Update model versions in the automated build</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動ビルドのモデル バージョンの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Platform update 6, a new task in the automated build definition updates the models in the source package and deployable package of the build output with the version of the build that produced them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 6 では、自動ビルド定義の新しいタスクが、作成したビルドのバージョンを持つビルド出力のソース パッケージと配置可能パッケージのモデルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Build definitions that were created before Platform update 6 must be manually updated to include this task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 6 以前に作成されたビルド定義はこのタスクを含めるために手動で更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>See the <bpt id="p1">[</bpt>Updating an existing build definition<ept id="p1">](#updating-an-existing-build-definition)</ept> section later in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックで後述する<bpt id="p1">[</bpt>既存のビルド定義の更新<ept id="p1">](#updating-an-existing-build-definition)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Version numbers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン番号</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Even though models are compiled into one package, the metadata information of all models is retained inside the binary package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルは 1 つのパッケージにコンパイルされますが、すべてのモデルのメタデータ情報は Binary パッケージ内に保持されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This information can be reviewed from Microsoft Dynamics Lifecycle Services (LCS) or from the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この情報は、Microsoft Dynamics Lifecycle Services (LCS) またはクライアントから確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>In LCS, follow these steps to find the version numbers of models that are installed in an environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS で、次の手順に従い、環境にインストールされているモデルのバージョン番号を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>On the <bpt id="p1">**</bpt>Full details<ept id="p1">**</ept> page for the environment, under <bpt id="p2">**</bpt>Environment Version Information<ept id="p2">**</ept>, click the <bpt id="p3">**</bpt>View detailed version information<ept id="p3">**</ept> link.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の<bpt id="p1">**</bpt>完全な詳細<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>環境バージョン情報<ept id="p2">**</ept>の下にある、<bpt id="p3">**</bpt>詳細バージョン情報の表示<ept id="p3">**</ept>リンクをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>On the <bpt id="p1">**</bpt>Installed updates<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Machine name<ept id="p2">**</ept> field, select an Application Object Server (AOS) computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インストールされた更新<ept id="p1">**</ept>ページの、<bpt id="p2">**</bpt>コンピューター名<ept id="p2">**</ept>フィールドで、Application Object Server (AOS) コンピューターを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>In the table list, find the <bpt id="p1">**</bpt>Publisher name<ept id="p1">**</ept> field of the model, and expand the list by clicking the arrow icon.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの一覧で、モデルの<bpt id="p1">**</bpt>パブリッシャー名<ept id="p1">**</ept>フィールドを探して、矢印アイコンをクリックして一覧を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>A full list of all models from that publisher is shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その発行元からのすべてのモデルの完全な一覧が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The version number is shown in the <bpt id="p1">**</bpt>Version<ept id="p1">**</ept> column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン番号は、<bpt id="p1">**</bpt>バージョン<ept id="p1">**</ept> 列に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In the client, follow these steps to find the version numbers of models that are installed in an environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントで、次の手順に従い、環境にインストールされているモデルのバージョン番号を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Open the URL for the environment, and sign in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の URL を開いて、サインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>After the dashboard is loaded, click the gear symbol at the upper right of the page, and then click <bpt id="p1">**</bpt>About<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダッシュ ボードが読み込まれた後、ページの右上にあるギヤ記号をクリックして、<bpt id="p1">**</bpt>About<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In the dialog box that appears, expand <bpt id="p1">**</bpt>Loaded Packages and their Models<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示されるダイアログ ボックスで、<bpt id="p1">**</bpt>読み込み済みパッケージとそのモデル<ept id="p1">**</ept>を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Find the package where the model resides, and expand the list by clicking the arrow icon.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルが存在するパッケージを検索し、矢印アイコンをクリックして一覧を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The list of models for the package is shown, together with the version number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージのモデル一覧とバージョン番号が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>All version numbers are in .NET assembly format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのバージョン番号は .NET アセンブリ形式です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>They consist of four numbers that are separated by a dot (.), such as <bpt id="p1">**</bpt>1.2.3.4<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それらは、<bpt id="p1">**</bpt>1.2.3.4<ept id="p1">**</ept> のようにドット (.) で区切られた 4 つの数字で構成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The purpose of model versioning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル バージョン管理の目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>As code is updated, the build is used to produce new packages that can be deployed to environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードが更新されると、環境に配置できる新しいパッケージを作成するためにビルドが使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Microsoft Azure DevOps tracks the changes that have been included in each build since the previous build.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Azure DevOps は、前回のビルド以降に各ビルドに含まれた変更を追跡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>When the version number of the build is included in the models that are produced, it provides end-to-end traceability of the code changes that are available in a specific environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドのバージョン番号が生成されるモデルに含まれている場合、その番号によって、特定の環境で使用できるコードの変更の徹底した追跡可能性が提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>You can find the build number and then review the changes that are included in that build in Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド番号を見つけてから、Azure DevOps でそのビルドに含まれている変更を確認することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>For customers and partners that use builds on different branches, or that use different build definitions for nightly builds, gated check-in builds, or deployment builds, each build can have a different versioning scheme.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">異なる分岐でビルドを使用する、または夜間ビルド、ゲート チェックイン ビルドまたは配置ビルド用の異なるビルド定義を使用する顧客およびパートナーについては、ビルドごとに異なるバージョン スキームを持つことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This approach helps differentiate the model metadata in the deployable packages and tie them back to their originating build definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法は、展開可能なパッケージのモデルメタデータを区別し、元のビルド定義に戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Setting up versioning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン管理の設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>For build definitions that are created by Platform update 6 or newer deployments, the task to include build version in models is automatically added and active.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 6 または新しい配置により作成されるビルド定義については、モデルにビルド バージョンを含めるためのタスクが自動的に追加され有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The default build number of a new build definition in Azure DevOps consists of the year, month, and day, and the incremental number of the build for that day.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps の新しいビルド定義の既定のビルド番号は、年、月、日、およびその日のビルドの増分番号で構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>For more information about build numbers in Azure DevOps, and the options that are available, see <bpt id="p1">[</bpt>Build definition options<ept id="p1">](https://www.visualstudio.com/en-us/docs/build/define/options#Buildnumberformat)</ept> on the Microsoft Visual Studio docs site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps のビルド番号、および使用できるオプションの詳細については、Microsoft Visual Studio ドキュメント サイトの<bpt id="p1">[</bpt>ビルド定義オプション<ept id="p1">](https://www.visualstudio.com/en-us/docs/build/define/options#Buildnumberformat)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The automated build will apply the build version number to the models that are built.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動ビルドは、構築されたモデルにビルド バージョン番号を適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Preventing models from being updated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルが更新されるのを防ぐ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>By default, the build task assigns versions only to models that are in layers above the ISP layer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、ビルド タスクは ISP レイヤーより上位にあるレイヤー内のモデルにのみバージョンを割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Therefore, customers can consume code models from third-party vendors without overwriting the version numbers that are supplied in their models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、モデルで提供されているバージョン番号を上書きしなくても、サード パーティ ベンダーのコード モデルを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>However, you can also prevent other models from having their version numbers overwritten during the build, regardless of layer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、レイヤーに関係なく、ビルド中に他のモデルのバージョン番号が上書きされないようにすることもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>When you edit the build definition, on the <bpt id="p1">**</bpt>Variables<ept id="p1">**</ept> tab, in the <bpt id="p2">**</bpt>ModelVersionExclusions<ept id="p2">**</ept> variable, supply a comma-separated list of model names to exclude.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド定義を編集するときは、<bpt id="p1">**</bpt>変数<ept id="p1">**</ept> タブの <bpt id="p2">**</bpt>ModelVersionExclusions<ept id="p2">**</ept> 変数で、除外するモデル名のコンマ区切りの一覧を供給します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Updating models in lower layers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">下位レイヤーのモデルの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>For third parties that develop solutions in the ISV or ISP layer, a manual change must be made to the build definition to automatically set model versions in those layers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV または ISP レイヤーでソリューションを開発するサード パーティについては、それらのレイヤーでモデル バージョンを自動で設定するため、手動変更がビルド定義に対して加えられる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Edit the build definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド定義を編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>On the <bpt id="p1">**</bpt>Tasks<ept id="p1">**</ept> tab, click the <bpt id="p2">**</bpt>Set Model Versions<ept id="p2">**</ept> task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タスク<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>モデル バージョンの設定<ept id="p2">**</ept>タスクをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In the <bpt id="p1">**</bpt>Arguments<ept id="p1">**</ept> field, add the following option at the end of the existing list of arguments: <bpt id="p2">**</bpt>-UpdateLayersAbove 7<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>引数<ept id="p1">**</ept>フィールドで、既存の引数のリストの最後に <bpt id="p2">**</bpt>-UpdateLayersAbove 7<ept id="p2">**</ept> のオプションを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Updating an existing build definition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のビルド定義の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>For build definitions that were created before Platform update 6, a new task must be manually added to the build definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 6 以前に作成されたビルド定義では、新しいタスクをビルド定義に手動で追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>This feature can be added to a build definition only after the build virtual machine (VM) has been updated to Platform update 6 or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、ビルド仮想マシン (VM) がプラットフォーム更新プログラム 6 以降に更新された後にのみ、ビルド定義に追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In Azure DevOps, on the <bpt id="p1">**</bpt>Build &amp; Release<ept id="p1">**</ept> page, under <bpt id="p2">**</bpt>Builds<ept id="p2">**</ept>, on the <bpt id="p3">**</bpt>All Definitions<ept id="p3">**</ept> tab, find your build definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps で、<bpt id="p1">**</bpt>ビルドおよびリリース<ept id="p1">**</ept> ページの<bpt id="p2">**</bpt>ビルド<ept id="p2">**</ept>にある<bpt id="p3">**</bpt>すべての定義<ept id="p3">**</ept>タブでビルド定義を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Click the ellipsis (…), and then click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">省略記号 (...)、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Edit the build definition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド定義を編集</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>On the <bpt id="p1">**</bpt>Tasks<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>+ Add Task<ept id="p2">**</ept> at the bottom of the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タスク<ept id="p1">**</ept>タブで、ページの下部にある<bpt id="p2">**</bpt>+ タスクの追加<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>In the <bpt id="p1">**</bpt>Add tasks<ept id="p1">**</ept> pane on the right side of the page, on the <bpt id="p2">**</bpt>Utility<ept id="p2">**</ept> tab, scroll down to find the <bpt id="p3">**</bpt>PowerShell<ept id="p3">**</ept> task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの右側にある<bpt id="p1">**</bpt>タスクの追加<ept id="p1">**</ept>ウィンドウの<bpt id="p2">**</bpt>ユーティリティ<ept id="p2">**</ept> タブで、下にスクロールして <bpt id="p3">**</bpt>PowerShell<ept id="p3">**</ept> タスクを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Hover the mouse pointer over the task, and click the <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> button that appears.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マウス ポインタをタスク上にポイントして、表示する<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Add a PowerShell task</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PowerShell タスクの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>In the list of tasks on the left side of the page, click to select the <bpt id="p1">**</bpt>PowerShell Script<ept id="p1">**</ept> task that is added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの左側にあるタスクの一覧で、追加される <bpt id="p1">**</bpt>PowerShell スクリプト<ept id="p1">**</ept> タスクをクリックして選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>On the right side of the page, change the <bpt id="p1">**</bpt>Display name<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Script Path<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>Arguments<ept id="p3">**</ept> properties to reflect the required settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの右側で、<bpt id="p1">**</bpt>表示名<ept id="p1">**</ept>、<bpt id="p2">**</bpt>スクリプト パス<ept id="p2">**</ept>、および<bpt id="p3">**</bpt>引数<ept id="p3">**</ept>プロパティを変更して必要な設定を反映します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Set the properties for the Set Model Versions task</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル バージョンの設定作業のプロパティを設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>In the list of tasks on the left side of the page, drag the <bpt id="p1">**</bpt>Set Model Versions<ept id="p1">**</ept> task so that it's between the <bpt id="p2">**</bpt>Prepare for build<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Build the solution<ept id="p3">**</ept> tasks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの左側にあるタスクの一覧で、<bpt id="p1">**</bpt>モデル バージョンの設定<ept id="p1">**</ept>タスクを、<bpt id="p2">**</bpt>ビルドの準備<ept id="p2">**</ept>と<bpt id="p3">**</bpt>ソリューションのビルド<ept id="p3">**</ept> タスクの間にドラッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Set the order of the Set Model Versions task</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル バージョンの設定作業の順序を設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>On the <bpt id="p1">**</bpt>Variables<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>+ Add<ept id="p2">**</ept> at the bottom of the list of variables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>変数<ept id="p1">**</ept>タブで、変数のリストの下部にある<bpt id="p2">**</bpt>+ 追加<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>In the first column, for the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> variable, enter <bpt id="p2">**</bpt>ModelVersionExclusions<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の列で、<bpt id="p1">**</bpt>名前<ept id="p1">**</ept>の変数に <bpt id="p2">**</bpt>ModelVersionExclusions<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept> to save the new task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいタスクを保存するには、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>をクリックします。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
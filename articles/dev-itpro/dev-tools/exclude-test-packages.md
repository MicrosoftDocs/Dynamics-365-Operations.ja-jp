<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="exclude-test-packages.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>exclude-test-packages.5e3654.237f8771170a863ca20d713e83caf0921d2a386d.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>237f8771170a863ca20d713e83caf0921d2a386d</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\exclude-test-packages.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Exclude test packages from build output</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド出力からテスト パッケージを除外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how you can prevent specific packages from being included in the deployable package in the build output that the automated build process generates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、自動ビルドプロセスが生成するビルド出力で、特定のパッケージが展開可能パッケージに含まれないようにする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Exclude test packages from build output</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド出力からテスト パッケージを除外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Platform update 4, the automated build process lets you prevent specific packages from being included in the deployable package in the build output.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 4 では、自動ビルド プロセスにより、ビルド出力で特定のパッケージが配置可能パッケージに含まれないようにできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This capability can be important for customers that use automated testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、自動化されたテストを使用する顧客にとって重要なことです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>These customers might want to build and run their tests, but prevent them from being added to the deployable package that the build generates as output.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの顧客は、テストをビルドして実行したいが、ビルドが出力として生成する配置可能なパッケージにテストが追加したくないと考えている場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When customers that have an existing build definition from Platform update 3 or earlier upgrade, they won't see the build definition automatically updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 3 またはそれ以前の既存のビルド定義を持っている顧客がアップグレードするとき、ビルド定義が自動的に更新されることが表示されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To use the new feature, these customers must make a few manual edits to the build definition (see below for details).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい機能を使用するには、これらの顧客はビルド定義を手動で編集する必要があります (詳細は下記参照)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The new feature exposes a new optional parameter for the package creation step in the build process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この新機能は、ビルド プロセスにおけるパッケージ作成ステップの新しいオプション パラメーターを公開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Because this parameter is managed by a build variable, you can easily adjust it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパラメーターはビルド変数で管理されるため、簡単に調整できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In Microsoft Azure DevOps, on the <bpt id="p1">**</bpt>Build &amp; Release<ept id="p1">**</ept> page, under <bpt id="p2">**</bpt>Builds<ept id="p2">**</ept>, on the <bpt id="p3">**</bpt>All Definitions<ept id="p3">**</ept> tab, find your build definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Azure DevOps で、<bpt id="p1">**</bpt>ビルドおよびリリース<ept id="p1">**</ept> ページの<bpt id="p2">**</bpt>ビルド<ept id="p2">**</ept>にある<bpt id="p3">**</bpt>すべての定義タブ<ept id="p3">**</ept>でビルド定義を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Click the ellipsis (…), and then click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">省略記号 (...)、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Edit the build definition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド定義を編集</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>On the <bpt id="p1">**</bpt>Variables<ept id="p1">**</ept> tab, notice that the new build definition has a variable that is named <bpt id="p2">**</bpt>PackagingExclusions<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>変数<ept id="p1">**</ept>タブで、新しいビルド定義が <bpt id="p2">**</bpt>PackagingExclusions<ept id="p2">**</ept> という名前の変数を持つこと通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>PackagingExclusions variable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PackagingExclusions 変数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In the <bpt id="p1">**</bpt>PackagingExclusions<ept id="p1">**</ept> variable, specify a comma-separated list of the names of packages that should not be packaged into the deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PackagingExclusions<ept id="p1">**</ept> 変数で、配置可能パッケージにパッケージする必要がないパッケージの名前をコンマで区切ったリストで指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The name of a package isn't necessarily the name of the model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージの名前は必ずしもモデルの名前ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Instead, the package name is typically the name of the folder where the model resides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、パッケージ名は通常、モデルがあるフォルダーの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Alternatively, you can copy and paste the package name from the descriptor file of one of the package's models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、パッケージ モデルのいずれかの記述子ファイルからパッケージ名をコピーして貼り付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>(In the XML, you can find the package name in the <bpt id="p1">**</bpt>ModelModule<ept id="p1">**</ept> field.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(XML では、<bpt id="p1">**</bpt>ModelModule<ept id="p1">**</ept> フィールドでパッケージ名を検索できます。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>For example, you have one package that is named MyCompanysAwesomeTests and another package that is named ContosoTaskRecordingTests, and you want to exclude both these packages from the deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、MyCompanysAwesomeTests という名前の 1 つのパッケージおよび ContosoTaskRecordingTests という名前の別のパッケージがあり、配置可能なパッケージからこれら両方のパッケージを除外します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>In this case, the value for the <bpt id="p1">**</bpt>PackagingExclusions<ept id="p1">**</ept> variable will look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、<bpt id="p1">**</bpt>PackagingExclusions<ept id="p1">**</ept> 変数の値はこのようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>PackagingExclusions example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PackagingExclusions の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>After you complete this setup, the build process will still build the code and run any tests that the packages contain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この設定を完了すると、ビルド プロセスはコードをビルドしながらパッケージに含まれているすべてのテストを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>However, the deployable package that the build creates won't include those packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ビルドが作成する配置可能なパッケージには、それらのパッケージは含まれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Update an existing build definition after upgrade to Platform update 4 or later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 4 以降へのアップグレード後に既存のビルド定義を更新する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>To use the new feature, you must manually update any existing build definitions that you deployed before Platform update 4.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい機能を使用するには、Platform update 4 より前に展開した既存のビルド定義を手動で更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The feature can be added to a build definition only after you update the build virtual machine (VM) to Platform update 4 or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、ビルド仮想マシン (VM) をプラットフォーム更新プログラム 4 以降に更新した後でのみ、ビルド定義に追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>On the <bpt id="p1">**</bpt>Variables<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>+ Add<ept id="p2">**</ept> at the bottom of the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>変数<ept id="p1">**</ept>タブで、ページの下部にある<bpt id="p2">**</bpt>+ 追加<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> column, enter <bpt id="p2">**</bpt>PackagingExclusions<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>列に、<bpt id="p2">**</bpt>PackagingExclusions<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>In the last column, select the <bpt id="p1">**</bpt>Settable at queue time<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後の列で、<bpt id="p1">**</bpt>キュー時に設定可能<ept id="p1">**</ept>チェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>On the <bpt id="p1">**</bpt>Tasks<ept id="p1">**</ept> tab, find the <bpt id="p2">**</bpt>Generate Packages<ept id="p2">**</ept> task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タスク<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>生成パッケージ<ept id="p2">**</ept>タスクを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Click to select it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クリックして選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>On the right side of the page, find the <bpt id="p1">**</bpt>Arguments<ept id="p1">**</ept> parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの右側で、<bpt id="p1">**</bpt>引数<ept id="p1">**</ept>パラメーターを見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Click in the text box, and then press the End key or scroll to the end of the text box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト ボックスをクリックし、End キーを押すか、テキスト ボックスの最後までスクロールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The new build definition will have a new argument that passes the <bpt id="p1">**</bpt>PackagingExclusions<ept id="p1">**</ept> variable that you defined earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいビルド定義には、前に定義した <bpt id="p1">**</bpt>PackagingExclusions<ept id="p1">**</ept> 変数を渡す新しい引数があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>However, for an existing build definition, add a space and then the following text to the end of the parameter: <bpt id="p1">**</bpt>-ExclusionList "$(PackagingExclusions)"<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、既存のビルド定義については、スペースを追加し、さらにパラメーターの末尾に次のテキストを追加します: <bpt id="p1">**</bpt>-ExclusionList "$(PackagingExclusions)"<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The <bpt id="p1">**</bpt>Arguments<ept id="p1">**</ept> text box should now look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>引数<ept id="p1">**</ept> テキスト ボックスは次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Generate Packages task</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージ タスクを生成します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>You can now use the new feature as described.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明の通りに、新しいフィーチャーを使用することができるようになりました。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
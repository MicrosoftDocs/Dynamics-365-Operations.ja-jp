<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="systest-filtering.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>systest-filtering.6239ed.f26dd879e421ad1dee43f54745c9466871127642.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>f26dd879e421ad1dee43f54745c9466871127642</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\perf-test\systest-filtering.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>SysTest filtering using class and method attributes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスとメソッドの属性を使用した SysTest フィルタリング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic outlines attributes that can be used with SysTest classes and methods for the purpose of test filtering.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、テストのフィルター処理の目的で SysTest クラスおよびメソッドで使用できる属性について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>SysTest Filtering using class and method attributes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスおよびメソッドの属性を使用した SysTest フィルター処理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Starting with Platform update 12, the SysTest framework contains improvements to the SysTest class and method attributes in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 12 以降、SysTest フレームワークには、X++ で SysTest クラスおよびメソッドの属性の強化が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>These improvements also change how these attributes work in the Visual Studio test window as well as the Visual Studio Test Console, which is the tool used in the automated build process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの機能強化により、これらの属性が、Visual Studio テスト ウィンドウおよび自動ビルドプロセスで使用されるツールである Visual Studio テスト コンソールでどのように機能するかも変わります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The SysTest framework now supports the major test attributes in the adaptor to be on par with the MSTest framework adaptor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysTest フレームワークは、MSTest フレームワーク アダプターと同等になるように、アダプター内の主要なテスト属性をサポートするようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This includes attributes like <bpt id="p1">**</bpt>Category<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Owner<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Priority<ept id="p3">**</ept>, and <bpt id="p4">**</bpt>Test Property<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには<bpt id="p1">**</bpt>カテゴリ<ept id="p1">**</ept>、<bpt id="p2">**</bpt>所有者<ept id="p2">**</ept>、<bpt id="p3">**</bpt>優先順位<ept id="p3">**</ept>、および<bpt id="p4">**</bpt>テスト プロパティ<ept id="p4">**</ept>などの属性が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>TestCategory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TestCategory</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The <bpt id="p1">**</bpt>Category<ept id="p1">**</ept> attribute, <bpt id="p2">**</bpt>SysTestCategory<ept id="p2">**</ept>, was already available in previous platform updates using the <bpt id="p3">**</bpt>SysTestCategory<ept id="p3">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カテゴリ<ept id="p1">**</ept>属性である <bpt id="p2">**</bpt>SysTestCategory<ept id="p2">**</ept> は、<bpt id="p3">**</bpt>SysTestCategory<ept id="p3">**</ept> 属性を使用した以前のプラットフォーム更新プログラムですでに利用可能でした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Starting with Platform update 12, you can specify multiple categories on both the class level and the individual method level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 12 以降、クラス レベルと個々のメソッド レベルの両方で複数のカテゴリを指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Additionally, <bpt id="p1">**</bpt>TestCategory<ept id="p1">**</ept> is enabled for filtering in the Visual Studio Test Console.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、<bpt id="p1">**</bpt>TestCategory<ept id="p1">**</ept> では、Visual Studio テスト コンソールでのフィルター処理が有効になっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>This means that you can create build pipelines with test filters on specific categories.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、特定のカテゴリのテスト フィルターを使用して、ビルド パイプラインを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>You can use the <bpt id="p1">**</bpt>TestFilter<ept id="p1">**</ept> variable in the build pipeline.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド パイプラインで、<bpt id="p1">**</bpt>TestFilter<ept id="p1">**</ept> 変数を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>For example, to run tests only with a category <bpt id="p1">**</bpt>Nightly<ept id="p1">**</ept>, set the variable to <bpt id="p2">**</bpt>TestCategory=Nightly<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、カテゴリ <bpt id="p1">**</bpt>Nightly<ept id="p1">**</ept> でのみテストを実行するには、変数を <bpt id="p2">**</bpt>TestCategory=Nightly<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Priority</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">優先順位</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The <bpt id="p1">**</bpt>Priority<ept id="p1">**</ept> attribute <bpt id="p2">**</bpt>SysTestPriority<ept id="p2">**</ept>, which requires an integer value, is now available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">整数値を必要とする <bpt id="p1">**</bpt>Priority<ept id="p1">**</ept> 属性の <bpt id="p2">**</bpt>SysTestPriority<ept id="p2">**</ept> が利用可能になりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>A priority can only be specified once, but is supported on both the class and method level, with method level taking precedence over class level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">優先順位は 1 回のみ指定できますが、クラスとメソッドの両方のレベルでサポートされ、メソッド レベルはクラス レベルよりも優先されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The priority is also exposed as a test filter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">優先順位は、テスト フィルターとしても公開されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>This means that you can use the <bpt id="p1">**</bpt>TestFilter<ept id="p1">**</ept> variable in the build pipeline.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、ビルド パイプラインで、<bpt id="p1">**</bpt>TestFilter<ept id="p1">**</ept> 変数を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For example, to only run tests with a priority of <bpt id="p1">**</bpt>1<ept id="p1">**</ept>, set the variable to <bpt id="p2">**</bpt>Priority=1<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、優先順位 <bpt id="p1">**</bpt>1<ept id="p1">**</ept> でのみテストを実行するには、変数を <bpt id="p2">**</bpt>Priority=1<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Owner</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">所有者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The <bpt id="p1">**</bpt>Owner<ept id="p1">**</ept> attribute, <bpt id="p2">**</bpt>SysTestOwner<ept id="p2">**</ept>, has also been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>所有者<ept id="p1">**</ept>属性である <bpt id="p2">**</bpt>SysTestOwner<ept id="p2">**</ept> も追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>This attribute was technically already supported for filtering in the <bpt id="p1">**</bpt>Test Toolbox<ept id="p1">**</ept> window, but the attribute itself was missing in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この属性は技術的には既に <bpt id="p1">**</bpt>Test Toolbox<ept id="p1">**</ept> ウィンドウでのフィルター処理に対してサポートされていましたが、属性自体は X ++ にはありませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Similar to <bpt id="p1">**</bpt>Priority<ept id="p1">**</ept>, an owner can only be specified once and is supported on both the class and method level, with the method level taking precedence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Priority<ept id="p1">**</ept> と同様に、所有者は 1 回のみ指定でき、クラスとメソッドの両方のレベルでサポートされ、メソッド レベルが優先されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Owner<ept id="p1">**</ept> is not available as a test filter for the console, which aligns with the MSTest adaptor for Visual Studio Test Console.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>所有者<ept id="p1">**</ept>は、コンソール用のテストフィルターとしては使用できません。これは、Visual Studio テスト コンソール用の MSTest アダプターに対応しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>However, <bpt id="p1">**</bpt>Owner<ept id="p1">**</ept> will appear in the <bpt id="p2">**</bpt>Test Toolbox<ept id="p2">**</ept> window in Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>所有者<ept id="p1">**</ept>は Visual Studio の <bpt id="p2">**</bpt>Test Toolbox<ept id="p2">**</ept> ウィンドウに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Test Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The <bpt id="p1">**</bpt>Test Property<ept id="p1">**</ept> attribute, <bpt id="p2">**</bpt>SysTestProperty<ept id="p2">**</ept>, has existed in previous releases of the platform, but wasn't fully functional.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テスト プロパティ<ept id="p1">**</ept> 属性の <bpt id="p2">**</bpt>SysTestProperty<ept id="p2">**</ept> は、プラットフォームの以前のリリースに存在していましたが、完全には機能しませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Unfortunately, the <bpt id="p1">**</bpt>SysTestProperty<ept id="p1">**</ept> attribute exists in the <bpt id="p2">**</bpt>Application Foundation<ept id="p2">**</ept> package as opposed to the other attributes which exist in the <bpt id="p3">**</bpt>Test Essentials<ept id="p3">**</ept> package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>SysTestProperty<ept id="p1">**</ept> 属性は <bpt id="p3">**</bpt>Test Essentials<ept id="p3">**</ept> パッケージに存在する他の属性とは対照的に、<bpt id="p2">**</bpt>アプリケーション基準<ept id="p2">**</ept>パッケージに存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Because of our commitment to backward compatibility of the platform, we currently cannot move this attribute to its expected location, so your code will need a reference to the <bpt id="p1">**</bpt>Application Foundation<ept id="p1">**</ept> package to use it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォームの下位互換性への確約のため、現在この属性を予定の場所に移動することはできません。そのため、使用するには<bpt id="p1">**</bpt>アプリケーション基準<ept id="p1">**</ept>パッケージへの参照が必要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>SysTestProperty<ept id="p1">**</ept> specifies a property and a value (two strings), and can now be used in the <bpt id="p2">**</bpt>Test Toolbox<ept id="p2">**</ept> window in Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysTestProperty<ept id="p1">**</ept> はプロパティと値 (2 つの文字列) を指定し、Visual Studio の <bpt id="p2">**</bpt>Test Toolbox<ept id="p2">**</ept> ウィンドウで使用できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Test Property<ept id="p1">**</ept> can be specified multiple times, and can exist on both the class and method level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テスト プロパティ<ept id="p1">**</ept>は複数回指定でき、クラスとメソッドの両方のレベルで存在できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Test Property<ept id="p1">**</ept> is not available for test filtering in the Visual Studio Test Console, in line with the MSTest adaptor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テスト プロパティ<ept id="p1">**</ept>は、MSTest アダプタに従って、Visual Studio テスト コンソールのフィルター処理のテストには使用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>For advanced filtering syntax that can be used with the Visual Studio Test Console and to review the filtering example for the MSTest framework, see <bpt id="p1">[</bpt>Running selective unit tests<ept id="p1">](https://docs.microsoft.com/en-us/dotnet/core/testing/selective-unit-tests)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio テスト コンソールで使用できる高度なフィルター処理構文および MSTest フレームワークのフィルター処理例の確認については、<bpt id="p1">[</bpt>選択可能な単位テストの実行<ept id="p1">](https://docs.microsoft.com/en-us/dotnet/core/testing/selective-unit-tests)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For test filtering purposes, the SysTest framework allows you to filter on <bpt id="p1">**</bpt>FullyQualifiedName<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Name<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィルター処理のテストの目的で、SysTest フレームワークを使用して <bpt id="p1">**</bpt>FullyQualifiedName<ept id="p1">**</ept> と <bpt id="p2">**</bpt>名前<ept id="p2">**</ept>でフィルター処理することができます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
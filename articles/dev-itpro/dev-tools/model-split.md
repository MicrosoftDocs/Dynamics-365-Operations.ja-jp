<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="model-split.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>model-split.e6b001.f2d562ef3028b22021267ebc90b921e619fb4bde.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>f2d562ef3028b22021267ebc90b921e619fb4bde</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\model-split.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Model split</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分割されたモデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains the split of the stack into three main models -  the Application Platform, the Application Foundation, and the Application Suite.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、スタックの 3 つの主要モデル、つまりアプリケーション プラットフォーム、アプリケーション基盤、アプリケーション スイートへの分割について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Model split</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分割されたモデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains the split of the stack into three main models -  the Application Platform, the Application Foundation, and the Application Suite.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、スタックの 3 つの主要モデル、つまりアプリケーション プラットフォーム、アプリケーション基盤、アプリケーション スイートへの分割について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Developing modular code is the driving force behind the model split.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モジュール コードを開発することは、モデル分割の原動力です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Splitting the stack into multiple models provides many benefits, including faster compile time and a greater distinction between partner's IP in production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数のモデルにスタックを分割すると、コンパイル時間の短縮、実稼動環境でのパートナー IP の適切な区別など、多くの利点が提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>There are three main models: the <bpt id="p1">**</bpt>Application Platform<ept id="p1">**</ept>, the <bpt id="p2">**</bpt>Application Foundation<ept id="p2">**</ept>, and the <bpt id="p3">**</bpt>Application Suite<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メイン モデルは、<bpt id="p1">**</bpt>アプリケーション プラットフォーム<ept id="p1">**</ept>、<bpt id="p2">**</bpt>アプリケーション基盤<ept id="p2">**</ept>、<bpt id="p3">**</bpt>アプリケーション スイート<ept id="p3">**</ept>の 3 つがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>First<ph id="ph2">\_</ph>ModelSplit<ept id="p1">](./media/first_modelsplit.png)](./media/first_modelsplit.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>First<ph id="ph2">\_</ph>ModelSplit<ept id="p1">](./media/first_modelsplit.png)](./media/first_modelsplit.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt>Application Platform<ept id="p1">&lt;/strong&gt;</ept> is the lowest model and contains the lowest level elements that interface with the kernel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>アプリケーション プラットフォーム<ept id="p1">&lt;/strong&gt;</ept>は最下位モデルであり、カーネルとやり取りする最下位レベルの要素が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt>Application Object Server **(<ept id="p1">&lt;/strong&gt;</ept>AOS<bpt id="p2">&lt;strong&gt;</bpt>) can be started with only the **Application Platform<ept id="p2">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>Application Object Server **(<ept id="p1">&lt;/strong&gt;</ept>AOS<bpt id="p2">&lt;strong&gt;</bpt>) は、**アプリケーション プラットフォーム<ept id="p2">&lt;/strong&gt;</ept>を使用してのみ起動できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt>Application Foundation<ept id="p1">&lt;/strong&gt;</ept> sits atop the <bpt id="p2">&lt;strong&gt;</bpt>Application Platform<ept id="p2">&lt;/strong&gt;</ept> and contains framework functionalities that are shared by all applications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>アプリケーション基盤<ept id="p1">&lt;/strong&gt;</ept>は、<bpt id="p2">&lt;strong&gt;</bpt>アプリケーション プラットフォーム<ept id="p2">&lt;/strong&gt;</ept>の一番上に配置され、すべてのアプリケーションによって共有されるフレームワーク機能を含みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Finally, the <bpt id="p1">&lt;strong&gt;</bpt>Application Suite<ept id="p1">&lt;/strong&gt;</ept> sits atop the <bpt id="p2">&lt;strong&gt;</bpt>Application Foundation<ept id="p2">&lt;/strong&gt;</ept> and contains application specific elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、<bpt id="p1">&lt;strong&gt;</bpt>アプリケーション スイート<ept id="p1">&lt;/strong&gt;</ept>は<bpt id="p2">&lt;strong&gt;</bpt>アプリケーション基準<ept id="p2">&lt;/strong&gt;</ept>の上部に位置し、アプリケーションの特定要素を含みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The Model Breakdown table in the appendix provides examples of components in each of these models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">付録のモデル内訳表は、これらの各モデルのコンポーネントの例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Each model is compiled into its own assembly with dependencies on lower layer model assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各モデルは、独自のアセンブリにコンパイルされ、下位レイヤー モデル アセンブリに依存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt>Application Platform<ept id="p1">&lt;/strong&gt;</ept> does not depend on any other models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>アプリケーション プラットフォーム<ept id="p1">&lt;/strong&gt;</ept>は、他のモデルには依存しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>This implies a direct mapping of the model to an assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、モデルをアセンブリに直接マッピングすることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>ModelAssembly<ph id="ph2">\_</ph>ModelSplit<ept id="p1">](./media/modelassembly_modelsplit1.jpg)](./media/modelassembly_modelsplit1.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ModelAssembly<ph id="ph2">\_</ph>ModelSplit<ept id="p1">](./media/modelassembly_modelsplit1.jpg)](./media/modelassembly_modelsplit1.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Developing in the modular stack allows changes to be made in the <bpt id="p1">**</bpt>Application Suite<ept id="p1">**</ept> and compiled without touching the rest of the stack.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モジュール スタックで開発することで、<bpt id="p1">**</bpt>アプリケーション スイート<ept id="p1">**</ept>で変更を行い、残りのスタックに触れることなくコンパイルすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Only models with new changes need to be compiled, greatly reducing compile time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい変更のあるモデルのみコンパイルされる必要があり、コンパイルの時間が大幅に短縮されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>More information can be found in the "Model Breakdown" section at the end of this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、この記事の終わりにある「モデルの内訳」セクションで確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Customizing models</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルのカスタマイズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>There are two methods for customizing: overlayering and extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズの方法には、オーバーレイと拡張の 2 種類があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Overlayering allows for changes to be made at multiple layers that alter, or overlay, elements in models at lower levels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイヤーにより、下位レベルでモデル内の要素を変更、つまりオーバーレイする複数のレイヤーに変更を加えることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Extensions allow for new elements to be added or code to be attached to element events or plug-in points.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子を使用すると、要素のイベントやプラグイン ポイントに新しい要素を追加したり、コードをアタッチすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The type of customization used impacts how a model will be compiled and ultimately packaged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用されるカスタマイズのタイプは、モデルがどのようにコンパイルされ、最終的にパッケージ化されるかに影響を与えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>One or more models are compiled into an assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つ以上のモデルが、アセンブリにコンパイルされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>An assembly, its non-code metadata, and its compiled artifacts, form a package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アセンブリ、非コード メタデータ、およびそれをコンパイルされたコンポーネントはパッケージを形成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>A package is an independent deployable unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージは、独立した配置可能な単位です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>A model that contains only extension customizations can be compiled into its own assembly and be deployed in its own package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能のカスタマイズのみが含まれるモデルは、独自のアセンブリにコンパイルして独自のパッケージに配置できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>A model that contains any overlayering must be compiled into the assembly based on the overlayed model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意のオーバーレイが含まれるモデルは、オーバーレイ モデルに基づいてアセンブリにコンパイルする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Customization Assemblies<ept id="p1">](./media/customization-assemblies.png)](./media/customization-assemblies.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>カスタマイズ アセンブリ<ept id="p1">](./media/customization-assemblies.png)](./media/customization-assemblies.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Using extensions has several advantages, including:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の使用には、以下を含むいくつかの利点があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>For application lifecycle management purposes, you need to manage only your extension artifacts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション ライフ サイクル管理の目的で、拡張コンポーネントのみを管理する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Building a customization does not require you to recompile the entire application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズの構築ではアプリケーション全体を再コンパイルする必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>In the cloud, Microsoft can install, patch, upgrade, and change internal APIs without affecting your customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウドで Microsoft はユーザーのカスタマイズに影響を与えずに、インストール、パッチ、アップグレード、および内部 API の変更を行えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>You can service your solutions independently without concerns about other customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のカスタマイズを意識せずに、ソリューションを別々に処理することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>There are currently support code extensions, table extensions, form extensions, menu extensions, and enum extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、コード拡張、テーブル拡張、フォーム拡張、メニュー拡張、列挙拡張がサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The Extensions section in <bpt id="p1">[</bpt>Customize with extensions and overlayering<ept id="p1">](../extensibility/customization-overlayering-extensions.md)</ept> and <bpt id="p2">[</bpt>Customize model elements using extensions<ept id="p2">](../extensibility/customize-model-elements-extensions.md)</ept> provide a more detailed explanation on how to use extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>拡張機能およびオーバーレイによってカスタマイズする<ept id="p1">](../extensibility/customization-overlayering-extensions.md)</ept>と<bpt id="p2">[</bpt>拡張機能を使用してモデル要素をカスタマイズする<ept id="p2">](../extensibility/customize-model-elements-extensions.md)</ept> の「拡張機能」セクションでは、拡張機能の使い方について詳しく説明されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Extensions should be used on supported elements wherever possible and are best applied when no change to existing Microsoft code is needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子は、可能な限りサポートされている要素で使用する必要があり、既存の Microsoft コードを変更する必要がない場合に最適です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>A change to mask a method’s functionality requires overlayering to change the code itself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドの機能をマスクするための変更には、コード自体を変更するためのオーバーレイが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Overlayering should be in areas not covered by extensions and when the customization alters the base functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイヤーは、カスタマイズが基本機能をカスタマイズする場合に、拡張機能がカバーしない領域に存在する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The illustration below summarizes differences between the two customization strategies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、2 つのカスタマイズ戦略の違いをまとめたものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Customization Overview<ept id="p1">](./media/customization-overview.png)](./media/customization-overview.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>カスタマイズの概要<ept id="p1">](./media/customization-overview.png)](./media/customization-overview.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Model breakdown</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルの内訳</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Model<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>モデル<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Concept<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>概念<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Application Platform</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション プラットフォーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The Application Platform interfaces to kernel functionalities that are application logic agnostic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション ロジックに対応するカーネル機能へのアプリケーション プラットフォーム インターフェイス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The AOS can be started with just this model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS は、このモデルだけで開始することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>AIF base objects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AIF 基準オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Batch</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Form base objects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム基本対象</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>RunbaseSysOperations* base objects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RunbaseSysOperations* ベース オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>DictXX objects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DictXX オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Appl, Info, Global, ClassFactory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Appl、情報、グローバル、ClassFactory</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Data access objects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ アクセス オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Helper Classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘルパー クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>ENUM/EDT/Macros/ConfigKey/LicenseCode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ENUM/EDT/Macros/ConfigKey/LicenseCode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Application Foundation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション基準</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Application foundation features:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション基準機能:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Dimension framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フレームワーク分析コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Global Address Book</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グローバル アドレス帳</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Number Sequence</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">番号順序</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>OrgModel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OrgModel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Feature areas:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">機能領域:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Business Intelligence</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス インテリジェンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Upgrade framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード フレームワーク</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Security</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>E-Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Data Import/Export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインスポート/エクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>SYS objects:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SYS オブジェクト:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Best Practices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>CheckList</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チェックリスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Policy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保険証書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>RecordTemplate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RecordTemplate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Miscellaneous:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Currency</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通貨</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Unit of Measure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">測定単位</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Application Suite</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Suite</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Supply Chain Management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サプライ チェーン マネジメント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Human Capital Management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">人材管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Professional Services, etc.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロフェッショナル サービスなど</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="customization-overlayering-extensions.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>customization-overlayering-extensions.fa8b6d.a7eb1def57fc1a74e73c92226611550a35b528bf.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>a7eb1def57fc1a74e73c92226611550a35b528bf</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\customization-overlayering-extensions.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Customize through extension and overlayering</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能とオーバーレイによってカスタマイズする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic discusses the two methods of customizing source code and metadata of model elements -  overlayering and extensions and details supported extension capabilities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、モデル要素のソース コードとメタ データをカスタマイズするオーバーレイと拡張機能の 2 つの方法、およびサポートされている拡張機能の詳細について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Customize through extension and overlayering</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能とオーバーレイによってカスタマイズする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic discusses the two methods of customizing source code and metadata of model elements -  overlayering and extensions and details supported extension capabilities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、モデル要素のソース コードとメタ データをカスタマイズするオーバーレイと拡張機能の 2 つの方法、およびサポートされている拡張機能の詳細について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Overlayering</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイヤー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You can customize source code and metadata of model elements that are shipped by Microsoft or third-party Microsoft partners.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft またはサードパーティの Microsoft パートナーによって出荷されている、モデル要素のソース コードとメタデータをカスタマイズできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In order to customize metadata and source code of a model, the developer must create a new model that overlays the model they want to customize.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルのメタデータとソース コードをカスタマイズするために、開発者はカスタマイズするモデルにオーバーレイする新しいモデルを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For example, solution developers can provide code in the SLN layer, independent software vendors can use the ISV layer, and value-added resellers can use the VAR layer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ソリューション開発者は SLN レイヤーでコードを提供でき、独立系ソフトウェア ベンダーは ISV レイヤーを使用でき、さらにますおよび付加価値再販業者は VAR レイヤーを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Functionality defined in higher layers (VAR layer in this example) can override the functionality of lower layers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上部レイヤ (この例では VAR レイヤ) で定義された機能は、下部レイヤの機能を上書きできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The overlaying model must belong to the same <bpt id="p1">**</bpt>Package<ept id="p1">**</ept> as the source model and belong to a layer that is higher than the source model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイ モデルはソース モデルと同じ <bpt id="p1">**</bpt>パッケージ<ept id="p1">**</ept>に属し、ソース モデルよりも高いレイヤーに属している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Overlayering is a powerful tool to perform advanced customizations of metadata and source code, but may increase the cost of upgrading a solution to a new version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイヤーは、メタデータとソース コードの高度なカスタマイズを実行する強力なツールですが、ソリューションを新しいバージョンにアップグレードする費用が高くなる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>You can customize an application by using <bpt id="p1">*</bpt>extensions<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>拡張機能<ept id="p1">*</ept> を使用することにより、アプリケーションをカスタマイズすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>An extension enables you to add functionality to existing model elements and source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子により既存のモデル要素およびソース コードに機能を追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Extensions provide the following capabilities:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子は、次の機能を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Creating new model elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいモデル要素を作成しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Extending existing model elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のモデル要素を拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Extending source code using class extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスの拡張子を使用して、ソース コードを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Customizing business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス ロジックのカスタマイズ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Ways to customize business logic include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス ロジックをカスタマイズする方法に以下の内容が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Creating event handlers to respond to framework events, such as data events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ イベントなどのフレームワーク イベントに応答するイベント ハンドラーを作成しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Creating event handlers to respond to event delegates that are defined by the application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションで定義されているイベントの委任に応答するイベント ハンドラーを作成しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Creating new plug-ins.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいプラグインを作成しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To get started, review or complete this tutorial: <bpt id="p1">[</bpt>Customize model elements using extensions<ept id="p1">](customize-model-elements-extensions.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始するには、[<bpt id="p1">[</bpt>拡張機能を使用してモデル要素をカスタマイズする<ept id="p1">](customize-model-elements-extensions.md)</ept>] チュートリアルを確認するか完了してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Extension models and packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張モデルおよびパッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>You can create a model that contains only new model elements, new code, or extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいモデル要素、新しいコード、または拡張機能のみを含むモデルを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This model is compiled into its own separate assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このモデルは独自の独立したアセンブリにコンパイルされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>These assemblies, along with related metadata and runtime artifacts can be packaged (as a deployable package file) and deployed on runtime sandbox or production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのアセンブリは、関連するメタデータおよびランタイム コンポーネントと一緒に (展開可能なパッケージ ファイルとして) パッケージ化し、ランタイム サンドボックスまたは実稼働環境に展開することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>To create an extension model, go through the Create model wizard and select <bpt id="p1">**</bpt>Create new package<ept id="p1">**</ept> on the second step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張モデルを作成するには、モデルの作成ウィザードを開き、2番目のステップで <bpt id="p1">**</bpt>新しいパッケージを作成<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>./media/1_cust.png</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">./media/1_cust.png</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Extension models have several advantages, including:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張モデルの使用には、以下を含むいくつかの利点があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Application lifecycle management (ALM):<ept id="p1">**</ept> Extension models simplify and improve the performance of deployments, builds, test automation and delivery to customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション ライフサイクル管理 (ALM):<ept id="p1">**</ept> 拡張モデルは、配置、ビルド、テストの自動化、および顧客への配信のパフォーマンスを簡素化し、向上させます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Design time performance:<ept id="p1">**</ept> Building your model or project doesn't require you to recompile the entire application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイン時間業績:<ept id="p1">**</ept> モデルやプロジェクトを構築しても、アプリケーション全体を再コンパイルする必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Servicing:<ept id="p1">**</ept> In the cloud, Microsoft can install, patch, upgrade, and change internal APIs without affecting your customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サービス:<ept id="p1">**</ept> クラウド上で Microsoft はユーザーのカスタマイズに影響を与えずに、インストール、パッチ、アップグレード、および内部 APIs の変更を行えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>Upgrades:<ept id="p1">**</ept> Unlike overlayering, extensions reduce the cost of upgrading to a new version, as this approach eliminates costly code and metadata conflicts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アップグレード:<ept id="p1">**</ept> オーバレイヤーとは異なり、拡張機能が新しいバージョンにアップグレードするコストを削減し、同時にこのアプローチによりコストのかかるコードとメタデータの競合を排除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The following diagram illustrates how extensions get isolated in their assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、拡張がアセンブリでどのように分離されるかを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>media/ax7customization1.png</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">media/ax7customization1.png</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Code extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの拡張子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>You can extend source code in 3 ways:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 つの方法でソース コードを拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>By subscribing to events (framework events and delegates)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント (フレームワーク イベントおよびデリゲート) をサブスクライブすることにより</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>By writing plug-ins.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグインを書き込むことによって。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>By creating class extensions (aka class Augmentation), see section below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスの拡張機能 (別名、クラス強化) を作成して、以下のセクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>You should understand the following characteristics of framework events:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フレームワーク イベントの以下の特性を理解する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Events are implemented as multi-cast delegates, which means that more than one event handler can be subscribed to any particular event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントは、マルチキャスト デリゲートとして実装されます。つまり、複数のイベント ハンドラーを特定のイベントにサブスクライブすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Events are broadcast; there's no sequencing of calls to event handlers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントはブロードキャストされます。イベント ハンドラーへの呼び出しの優先順位はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Event handlers execute within the transaction scope of the base methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準メソッドのトランザクション スコープ内で、イベント ハンドラーを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Events</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Events are raised as preceding and succeeding operations around the base methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントは、基本メソッドの前後の操作として生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>This means that you have the opportunity to run code before a base method is called and after it has completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、基本メソッドが呼び出される前と完了後にコードを実行する機会があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Microsoft Dynamics AX 2012 introduced XPP events, which are also available in this release and can be subscribed to in your extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 で XPP イベントが導入されました。このイベントは、今回のリリースでも使用でき、拡張機能でサブスクライブできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Plug-ins</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Plug-ins are extension points that are defined by the base application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグインは、基本アプリケーションで定義されている拡張ポイントです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>By using a class-factory pattern, plug-ins enable you to replace the base functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス ファクトリ パターンを使用することにより、プラグインでは基本機能を置き換えることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>You can see how to implement a plug-in in the tutorial, <bpt id="p1">[</bpt>Customize model elements using extensions<ept id="p1">](customize-model-elements-extensions.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグインの実装方法については、チュートリアル <bpt id="p1">[</bpt>拡張機能を使用してモデル要素をカスタマイズする<ept id="p1">](customize-model-elements-extensions.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Class Extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスの拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Class extensions enable you to augment a class by adding methods and variables to existing classes, tables and forms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスの拡張機能を使用すると、既存のクラス、テーブル、フォームにメソッドや変数を追加して、クラスを拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For more details refer to the topic <bpt id="p1">[</bpt>class extensions<ept id="p1">](class-extensions.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、トピック <bpt id="p1">[</bpt>クラスの拡張機能<ept id="p1">](class-extensions.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Form extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム拡張子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can extend the functionality of a form by extending its controls and data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールおよびデータ ソースを拡張することにより、フォームの機能を拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For example, in a form extension, you can:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、フォーム拡張子で、以下の点を実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Add a new control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいコントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Enable or disable a control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールを有効または無効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Change the text or label property of a control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールのテキストまたはラベルのプロパティを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Change a control's visibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの可視性を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Change a form's help text.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのヘルプ テキストを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Change a form's caption.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのキャプションを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Add a new data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータ ソースを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Add a form part.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム パーツを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Other ways to customize a form, such as reordering controls in the form are planned to be included in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームでコントロールを並べ替えるなど、フォームをカスタマイズする他の方法は、将来のリリースに含まれる予定です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>In Microsoft Dynamics AX 2012, you could override form methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 では、フォーム メソッドを上書きすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>In the current version, you use extensions to implement event handlers that are called from the base implementations of form methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のバージョンでは、フォーム メソッドの基本実装から呼び出されるイベント ハンドラーを実装するのに拡張機能を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The following table lists each method and its associated events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルに、各メソッドとそれに関連するイベントを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">**</bpt>Published form DataSource method<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>公開済フォーム DataSource メソッド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">**</bpt>Preceding event<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>前のイベント<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">**</bpt>Succeeding event<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>後続のイベント<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>active</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Activated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>delete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Deleting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除中</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Deleted</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除済</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>validateWrite</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">validateWrite</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>ValidatingWriting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatingWriting</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>ValidatedWrite</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatedWrite</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>write</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">write</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Writing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Written</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">記述済み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>create</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Creating</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成中</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Created</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成済</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>executeQuery</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">executeQuery</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>QueryExecuted</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">QueryExecuted</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>linkActive</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">linkActive</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>PostLinkActive</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PostLinkActive</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>init</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">init</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Initialized</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">初期化済み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>validateDelete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">validateDelete</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>ValidatingDelete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatingDelete</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>ValidatedDelete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatedDelete</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>reread</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">reread</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Reread</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>selectionChanged</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">selectionChanged</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>SelectionChanged</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SelectionChanged</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>markChanged</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">markChanged</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>MarkChanged</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MarkChanged</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>leaveRecord</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">leaveRecord</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>LeavingRecord</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LeavingRecord</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>LeftRecord</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LeftRecord</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source><bpt id="p1">**</bpt>Published form Object method<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>公開済フォーム オブジェクト メソッド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source><bpt id="p1">**</bpt>Preceding event<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>前のイベント<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source><bpt id="p1">**</bpt>Succeeding event<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>後続のイベント<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>init</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">init</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Initializing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">初期化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Initialized</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">初期化済み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>close</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">閉じる</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Closing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">決算済み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>run</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">run</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>PostRun</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PostRun</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>activate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Activated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source><bpt id="p1">**</bpt>Published form Control method<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>公開済フォーム コントロール メソッド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source><bpt id="p1">**</bpt>Preceding event<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>前のイベント<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source><bpt id="p1">**</bpt>Succeeding event<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>後続のイベント<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>modified</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">modified</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Modified</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更済</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>validate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Validating</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証中</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Validated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証済み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>leave</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">leave</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Leaving</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">終了</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>LostFocus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LostFocus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>enter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Enter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>gotFocus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gotFocus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>GotFocus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GotFocus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>clicked</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">clicked</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Clicked</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クリックされた</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>selectionChange</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">selectionChange</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>SelectionChanging</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SelectionChanging</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>pageActivated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">pageActivated</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>PageActivated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PageActivated</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>allowPageDeactivate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">allowPageDeactivate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>AllowPageDeactivate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AllowPageDeactivate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>expand</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">expand</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Expanding</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Expanded</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡大</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>tabChanged</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tabChanged</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>TabChanged</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TabChanged</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>dialogClosed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dialogClosed</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>DialogClosed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DialogClosed</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Code behind extension forms</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張フォームの後にあるコード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>You can use class extensions to author X++Â logic associated with form extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス拡張機能を使用して、フォーム拡張機能と関連付けられた X++ ロジックを記述することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>This allows the definition of state variables accessible to form and control event handlers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、イベント ハンドラーを形成および制御するためにアクセス可能な状態変数の定義が可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>It also allows overriding form methods without overlayering code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードをオーバーレイせずにフォーム メソッドをオーバーライドすることもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Refer to <bpt id="p1">[</bpt>this<ept id="p1">](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/10/11/code-behind-extension-forms-how-to-add-state-variable-and-override-methods-without-overlayering)</ept> blog article for an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">[</bpt>こちら<ept id="p1">](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/10/11/code-behind-extension-forms-how-to-add-state-variable-and-override-methods-without-overlayering)</ept>のブログ記事をご覧ください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Table extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>You can create a table extension to extend a table's design and logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル拡張を作成して、テーブルのデザインおよびロジックを拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>You can add new fields, field groups, indexes, mappings and relations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいフィールド、フィールド グループ、インデックス、マップおよび関係を追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>You can also add new fields to existing field groups, change the label of a table field, change the Created By, Created Date Time, Modified By, Modified Date Time properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、既存のフィールド グループに新しいフィールドを追加して、テーブル フィールドのラベルを変更し、作成者、作成日時、修正者、修正日時のプロパティを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Using table extensions, you can also change the Extended Data Type property on fields and set it to an EDT that is derived from the current EDT (<bpt id="p1">*</bpt>This is available as of platform update 8<ept id="p1">*</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル拡張機能を使用して、フィールドの拡張データ型プロパティを変更し、現在の EDT から派生した EDT にそれを設定することもできます (<bpt id="p1">*</bpt>これはプラットフォーム更新プログラム 8 の時点で使用可能です<ept id="p1">*</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>In Microsoft Dynamics AX 2012, you could override the virtual methods of a table's base class to control the behavior that occurred during table operations, such as when creating, reading, updating, or deleting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 では、テーブルの基本クラスの仮想メソッドをオーバーライドして、作成、読み取り、更新、または削除などのテーブルの処理中に発生した動作を制御できました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>In the current version, you instead use extensions to implement event handlers that are called from the base implementations of the table methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のバージョンでは、代わりにテーブル メソッドの基本実装から呼び出されるイベント ハンドラーを実装するのに拡張機能を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>The following table lists each table method and its events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルに、各テーブルとそれに関連するイベントを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source><bpt id="p1">**</bpt>Published Table method<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>公開済テーブル メソッド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source><bpt id="p1">**</bpt>Preceding event<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>前のイベント<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source><bpt id="p1">**</bpt>Succeeding event<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>後続のイベント<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>validateWrite</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">validateWrite</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>ValidatingWrite</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatingWrite</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>ValidatedWrite</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatedWrite</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>validateDelete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">validateDelete</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>ValidatingDelete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatingDelete</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>ValidatedDelete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatedDelete</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>validateField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">validateField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>ValidatingField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatingField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>ValidatedField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatedField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>validateFieldValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">validateFieldValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>ValidatingFieldValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatingFieldValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>ValidatedFieldValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidatedFieldValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>modifiedField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">modifiedField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>ModifyingField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModifyingField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>ModifiedField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModifiedField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>modifiedFieldValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">modifiedFieldValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>ModifyingFieldValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModifyingFieldValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>ModifiedFieldValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModifiedFieldValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Insert</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">挿入</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Inserting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">挿入</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Inserted</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">挿入済</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Update</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Updating</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新中</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Updated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新済</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Delete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">消去</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Deleting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除中</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Deleted</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除済</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Initvalue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Initvalue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>InitializingRecord</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InitializingRecord</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>InitializedRecord</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InitializedRecord</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>FinalDeleteValidation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FinalDeleteValidation</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Executed when a delete operation is performed on a table object, before the operation is committed to the underlying database table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作が基礎データベース テーブルにコミットされる前に、テーブル オブジェクトに対して削除操作が実行された時に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>FinalInsertValidation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FinalInsertValidation</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Executed when an insert operation is performed on a table object, before the operation is committed to the underlying database table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作が基礎データベース テーブルにコミットされる前に、テーブル オブジェクトに対して挿入操作が実行された時に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>FinalReadValidation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FinalReadValidation</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Executed when a read operation is performed on a table object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル オブジェクトに対して、読み取り操作が行われた時に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>FinalUpdateValidation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FinalUpdateValidation</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Executed when an update operation is performed on a table object, before the operation is committed to the underlying database table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作が基礎データベース テーブルにコミットされる前に、テーブル オブジェクトに対して更新操作が実行された時に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>N/A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Validation events capture and return results by using the <bpt id="p1">**</bpt>DataEventArgs<ept id="p1">**</ept> parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証イベントは、<bpt id="p1">**</bpt>DataEventArgs<ept id="p1">**</ept> パラメーターを使用して結果を取得して返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>The display and edit method modifiers are supported on table extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示および編集メソッド モディファイアーは、テーブル拡張機能でサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>View and Data entity extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示およびデータ エンティティの拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>You can extend a View or Data entity to achieve much of the functionality available with table extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの拡張機能で使用可能な機能の大半を実行できるように、ビューまたはデータ エンティティを拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Enum extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙拡張子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>You can extend any Enum that is marked extensible (IsExtensible=True).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能とマークされている (IsExtensible=True) 任意の列挙値を拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>extensibleenums<ept id="p1">](./media/extensibleenums-300x158.png)](./media/extensibleenums.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>extensibleenums<ept id="p1">](./media/extensibleenums-300x158.png)](./media/extensibleenums.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>By extending an Enum, you can add new Enum values to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型を拡張することによって、新しい列挙値を追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>It is important to keep the following in mind when dealing with extensible Enums:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能な列挙を処理するとき、次のことに留意することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>You cannot have X++ logic that depends on the integer value of Enum values (For example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、列挙値の整数値に依存する X++ ロジックを持つことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source><bpt id="p1">*</bpt>If (Enum1.v1 <ph id="ph1">&amp;gt;</ph> Enum1.v2) ...<ept id="p1">*</ept> is not supported for extensible enums)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>(Enum1.v1 <ph id="ph1">&amp;gt;</ph> Enum1.v2).の場合...<ept id="p1">*</ept>は拡張可能な列挙ではサポートされていません)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>When Enum values of extensible Enums are synchronized into the database:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能な Enums の Enums 値がデータベースに同期されると、次の操作が行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Integer values that belong to the baseline enum are deterministic, they come from the metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベースライン列挙に属している整数値は確定的であり、メタデータから生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Integer values that are an extension are generated during the synchronization process and are not deterministic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子である整数値は、同期プロセス中に生成され、確定的ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>EDT extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT 拡張子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>You can extend an EDT element in order to modify any of the following properties:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の任意のプロパティを変更するため、EDT 要素を拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Form help</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム ヘルプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Label</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>String size</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列サイズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Help text</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘルプ テキスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Query extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリの拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>You can extend a Query element to achieve the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ要素を拡張して以下の内容を達成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Add ranges to an existing data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のデータ ソースに範囲を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Add new (embedded) data sources to an existing data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のデータ ソースに新しい (埋め込み) のデータ ソースを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Add new fields to an existing data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のデータ ソースに新しいフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Menu extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニューの拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>You can extend a Menu element to achieve the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニュー要素を拡張して以下の内容を達成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Add new menu items, submenus, menu references and tile references to an existing menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいメニュー項目、サブメニュー、メニューの参照を追加し、既存のメニューへの参照を並べて表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Hide an existing menu item, tile, or sub-menu in a menu by setting the <bpt id="p1">**</bpt>Visible<ept id="p1">**</ept> property to No.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept> プロパティをいいえに設定して、既存のメニュー項目、タイル、またはメニュー内のサブメニューを非表示にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>menuextensions<ept id="p1">](./media/menuextensions-300x137.png)](./media/menuextensions.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>menuextensions<ept id="p1">](./media/menuextensions-300x137.png)](./media/menuextensions.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>Security role and duty extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ ロールおよび職務権限拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>You can extend a Security Role or a Security Duty to add new duties/privileges to these elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ ロールまたはセキュリティ職務権限を拡張して、これらの要素に新しい職務/特権を追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Report extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>You can customize reports and business docs using extensions, below is a list of tutorials that help you learn more.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用してレポートおよびビジネス ドキュメントをカスタマイズすることができます。以下のものはさらに学習するためのチュートリアルの一覧です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source><bpt id="p1">[</bpt>Customizing App Suite reports using extensions<ept id="p1">](../analytics/customize-app-suite-reports-with-extensions.md)</ept>: Customizations to reporting solutions in the standard application are fully supported using a pure ‘Extension’ model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>拡張機能を使用してアプリケーション スイート レポートをカスタマイズする<ept id="p1">](../analytics/customize-app-suite-reports-with-extensions.md)</ept>: 標準アプリケーションのレポート ソリューションのカスタマイズは、純粋な「拡張」モデルを使用して完全にサポートをされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>This article offers guidance on how to add the most common customizations to standard application reports without over-layering Application Suite artifacts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、アプリケーション スイート コンポーネントをオーバーレイすることなく、標準のアプリケーション レポートに最も一般的なカスタマイズを追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Here are some…</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次にいくつか挙げます…</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source><bpt id="p1">[</bpt>How To: Custom designs for business docs<ept id="p1">](../analytics/custom-designs-business-docs.md)</ept>: This article focuses on the steps involved in crafting a custom report design for an existing application business document using a ‘pure’ extension model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>方法: ビジネス ドキュメントのカスタム デザイン<ept id="p1">](../analytics/custom-designs-business-docs.md)</ept>: この記事では、「純粋な」拡張モデルを使用して、既存のアプリケーション ビジネス ドキュメントのカスタムレポートデザインを作成する手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>Follow the steps below to associate a custom report design with an application document instance….</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム レポート デザインをアプリケーション ドキュメント インスタンスに関連付けるには、以下の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source><bpt id="p1">[</bpt>How To: Expanding App Suite report data sets<ept id="p1">](../analytics/expand-app-suite-report-data-sets.md)</ept>: This article focuses on the expansion of an existing report data set produced using X++ business logic in a Report Data Provider (RDP) class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>方法: アプリケーション スイート レポート データ セットを展開する<ept id="p1">](../analytics/expand-app-suite-report-data-sets.md)</ept>: この記事では、レポート データ プロバイダー (RDP) クラスで X++ ビジネスロジックを使用して作成された既存のレポート データ セットの展開について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Use custom delegate handlers and table extensions to include additional field data and/or calculations without…</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタムのデリゲート ハンドラーおよびテーブル拡張機能を使用して、...なしに追加のフィールド データと計算の両方またはいずれかを含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source><bpt id="p1">[</bpt>How To: Extending report menu items<ept id="p1">](../analytics/extend-report-menu-items.md)</ept>: This article focuses on the process of extending existing application menu items to redirect navigations with minimal code changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>方法: レポート メニュー項目の拡張<ept id="p1">](../analytics/extend-report-menu-items.md)</ept>: この記事では、最小限のコード変更で、既存のアプリケーション メニューを拡大してナビゲーションをリダイレクトするプロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Using this technique you will avoid the hassle of tracking down and replacing all references to an existing application…</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手法を使用すると、既存のアプリケーションに対するすべての参照を追跡し、置き換えることの不便を避けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Label extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベルの拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>You can create label extension files in order to modify the string value of a label, add new labels to the same label file or add new languages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベルの文字列値を変更、同じラベル ファイルに新しいラベルを追加、または新しい言語を追加するために、ラベル拡張ファイルを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>To create a label extension file you must name it with a <ph id="ph1">\_</ph>extension suffix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベル拡張ファイルを作成するには、その名前に<ph id="ph1">\_</ph>拡張子の接尾辞を付ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>For example, to extend the <bpt id="p1">**</bpt>FLM<ept id="p1">**</ept> labels of the Fleet Management model, do the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、フリート管理モデルの <bpt id="p1">**</bpt>FLM<ept id="p1">**</ept> ラベルを拡張するには、次の操作をします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Create a project that belongs to a model that references Fleet Management (The model Fleet Management Extension is an example).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理を参照するモデルに属するプロジェクトを作成します (フリート管理拡張モデルの例)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Add a new label file to the project and name it <bpt id="p1">**</bpt>FLM<ph id="ph1">\_</ph>Extension<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトに新しいラベル ファイルを追加し、<bpt id="p1">**</bpt>FLM<ph id="ph1">\_</ph>Extension<ept id="p1">**</ept> という名前をつけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Within the FLM<ph id="ph1">\_</ph>Extension label file, you can create new labels or modify the value of labels that are defined in the <bpt id="p1">**</bpt>FLM<ept id="p1">**</ept> label file of the Fleet Management model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FLM<ph id="ph1">\_</ph>Extension ラベル ファイル内では、ラベルを新規作成、またはフリート管理モデルの <bpt id="p1">**</bpt>FLM<ept id="p1">**</ept> ラベル ファイルで定義されたラベルの値を修正することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Use the standard label editor to define new labels or redefine labels that already exist in the original FLM label file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいラベルを定義するか、元の FLM ラベル ファイルに既に存在するラベルを再定義するには、標準のラベル エディターを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>If your goal is to create translations of the FLM label, right-click on the FLM<ph id="ph1">\_</ph>Extension element in your project and select <bpt id="p1">**</bpt>Add new languages<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目標が FLM ラベルの翻訳を作成することである場合、プロジェクトの FLM<ph id="ph1">\_</ph>Extension 要素を右クリックして<bpt id="p1">**</bpt>新しい言語の追加<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Follow the wizard to add translation files to the FLM labels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FLM ラベルに翻訳ファイルを追加するウィザードに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>If the FLM_Extension file already exists in another model, you can name your file <bpt id="p1">**</bpt>FLM_ExtensionN<ept id="p1">**</ept> where N is any integer (For example FLM_Extension2, FLM_Extension3, ...etc)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別のモデルに FLM_Extension ファイルが既に存在する場合、N が任意の整数である (たとえば、FLM_Extension2、FLM_Extension3、... など) <bpt id="p1">**</bpt>FLM_ExtensionN<ept id="p1">**</ept> というファイル名を付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>Extension of Country/Region Codes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">国/地域コードの拡張子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>This functionality is available as of Platform update 7.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、Platform update 7 以降で利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>The <bpt id="p1">**</bpt>Country Region Codes<ept id="p1">**</ept> property enables developers to restrict functionality to certain regions or countries based on the current legal entity’s primary address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>国/地域コード<ept id="p1">**</ept> プロパティにより、開発者は現在の法人のプライマリ住所に基づく特定の地域や国に機能を制限できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Developers can extend this functionality by setting the Country Region Codes property on the following extension element types: Menu extension, Menu Item extension, Table extension (and fields), Form extensions (form controls), EDT extensions, Enum extensions, and View extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は、メニュー拡張、メニュー項目拡張、表拡張 (およびフィールド)、フォーム拡張 (フォーム制御)、EDT 拡張、列挙拡張、および表示拡張の各拡張要素タイプに国地域コード プロパティを設定することにより、この機能を拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>You can specify additional country/region codes in their extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能で追加の国/地域コードを指定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>The effective country/regions (at runtime) associated with an element will be the union of all codes from the baseline element and all its extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要素に関連付けられた有効な国/地域 (実行時) は、ベースライン要素とそのすべての拡張機能からのすべてのコードの結合になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Event argument types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント引数タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>When an event takes place, the delegates described in the sections above get triggered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントが発生すると、上記のセクションで説明したデリゲートはトリガーされた状態になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>In this section, we provide the details of the types of the arguments that are passed as the event arguments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、イベントの引数として渡される引数のタイプの詳細を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Some of the entries in the table below have a null in the column designating the event args; this means that no arguments are passed - the relevant information is in the first argument (typically called sender) in this case.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のテーブルの一部のエントリでは、イベント引数を指定する列に null があります。つまり、渡される引数はありません。この場合、関連する情報が最初の引数 (通常は送信者と呼ばれる) です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source><bpt id="p1">**</bpt>Event<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>イベント<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source><bpt id="p1">**</bpt>Argument type<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>引数タイプ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>onDefaultedField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onDefaultedField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>DefaultFieldEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DefaultFieldEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>onDefaultedRow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onDefaultedRow</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>onDefaultingField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onDefaultingField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>DefaultFieldEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DefaultFieldEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>onDefaultingRow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onDefaultingRow</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>onDeleted</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onDeleted</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>onDeletedEntityDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onDeletedEntityDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>DataEntityContextResultEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextResultEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>onDeleting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onDeleting</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>onDeletingEntityDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onDeletingEntityDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>DataEntityContextResultEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextResultEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>onFindingEntityDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onFindingEntityDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>DataValidationEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataValidationEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>onFoundEntityDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onFoundEntityDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>DataEntityContextRecordEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextRecordEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>onGettingDefaultingDependencies</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onGettingDefaultingDependencies</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>DefaultingDependenciesEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DefaultingDependenciesEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>onGotDefaultingDependencies</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onGotDefaultingDependencies</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>DefaultingDependenciesEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DefaultingDependenciesEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>onInitializedEntityDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onInitializedEntityDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>DataEntityContextEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>onInitializedRecord</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onInitializedRecord</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>onInitializingEntityDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onInitializingEntityDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>DataEntityContextEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>onInitializingRecord</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onInitializingRecord</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>onInserted</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onInserted</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>onInsertedEntityDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onInsertedEntityDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>DataEntityContextResultEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextResultEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>onInserting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onInserting</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>onInsertingEntityDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onInsertingEntityDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>DataEntityContextResultEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextResultEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>onMappedDatasourceToEntity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onMappedDatasourceToEntity</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>DataEntityContextEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>onMappedEntityToDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onMappedEntityToDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>DataEntityContextEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>onMappingDatasourceToEntity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onMappingDatasourceToEntity</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>DataEntityContextEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>onMappingEntityToDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onMappingEntityToDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>DataEntityContextEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>onModifiedField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onModifiedField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>ModifyFieldEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModifyFieldEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>onModifiedFieldValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onModifiedFieldValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>ModifyFieldValueEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModifyFieldValueEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>onModifyingField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onModifyingField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>ModifyFieldEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModifyFieldEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>onModifyingFieldValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onModifyingFieldValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>ModifyFieldValueEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModifyFieldValueEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>onPersistedEntity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onPersistedEntity</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>DataEntityContextEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>onPersistingEntity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onPersistingEntity</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>DataEntityContextEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>onPostedLoad</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onPostedLoad</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>onPostingLoad</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onPostingLoad</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>onUpdated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onUpdated</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>onUpdatedEntityDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onUpdatedEntityDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>DataEntityContextResultEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextResultEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>onUpdating</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onUpdating</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NULL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>onUpdatingEntityDataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onUpdatingEntityDataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>DataEntityContextResultEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEntityContextResultEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>onValidatedDelete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onValidatedDelete</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>ValidateEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>onValidatedField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onValidatedField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>ValidateFieldEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateFieldEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>onValidatedFieldValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onValidatedFieldValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>ValidateFieldValueEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateFieldValueEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>onValidatedWrite</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onValidatedWrite</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>ValidateEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>onValidatingDelete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onValidatingDelete</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>ValidateEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>onValidatingField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onValidatingField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>ValidateFieldEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateFieldEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>onValidattingFieldValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onValidattingFieldValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>ValidateFieldValueEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateFieldValueEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>onValidatingWrite</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onValidatingWrite</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>ValidateEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>Development tools support</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発ツール サポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>The development tools in Visual Studio provide integrated features to help you create and work with extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio の開発ツールは、拡張機能を作成して作業するための統合された機能を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>For example, when you right-click an element name in <bpt id="p1">**</bpt>Application Explorer<ept id="p1">**</ept>, you can create an extension for that element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>アプリケーション エクスプ ローラー<ept id="p1">**</ept>で要素名を右クリックするときに、その要素の拡張機能を作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>3<ph id="ph2">\_</ph>Cust<ept id="p1">](./media/3_cust.png)](./media/3_cust.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>3<ph id="ph2">\_</ph>顧客<ept id="p1">](./media/3_cust.png)](./media/3_cust.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>To create an extension, the current project in <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept> must belong to a model that references the model of the selected element in <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を作成するには、<bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>の現在のプロジェクトが、<bpt id="p2">**</bpt>アプリケーション エクスプ ローラー<ept id="p2">**</ept>で選択された要素のモデルを参照するモデルに属している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>To view the model for a particular project, view the project properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のプロジェクトのモデルを表示するには、プロジェクトのプロパティを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>4<ph id="ph2">\_</ph>Cust<ept id="p1">](./media/4_cust.png)](./media/4_cust.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>4<ph id="ph2">\_</ph>顧客<ept id="p1">](./media/4_cust.png)](./media/4_cust.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source>Visual Studio creates the extension file for you, either in the current project or in a new project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio は、現在のプロジェクトまたは新しいプロジェクトのいずれかで、拡張機能ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source>You can then work with the extension file either as source code or by using a designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース コードとして、またはデザイナーを使用することにより、拡張ファイルで作業することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source>You package a code-extension model for deployment exactly like you would package any other model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の任意のモデルをパッケージ化するのとまったく同じように、コード拡張モデルをパッケージ化し展開してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source>On the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> menu, point to <bpt id="p2">**</bpt>Deploy<ept id="p2">**</ept>, click <bpt id="p3">**</bpt>Create Deployment Package<ept id="p3">**</ept>, and then select the check box for the package name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>配置<ept id="p2">**</ept>をポイントし、<bpt id="p3">**</bpt>配置パッケージの作成<ept id="p3">**</ept>をクリックして、パッケージ名のチェック ボックスを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source>Framework events</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フレームワーク イベント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source>Tables, form data sources, form controls, and other element types that support extension events list the available events (and delegates) under an <bpt id="p1">**</bpt>Events<ept id="p1">**</ept> collection node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル、フォーム データ ソース、フォーム コントロール、拡張イベントをサポートする他の要素タイプは、<bpt id="p1">**</bpt>イベント<ept id="p1">**</ept> コレクション ノードの下に使用可能なイベント (およびデリゲート) をリストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source>For example, viewing the <bpt id="p1">**</bpt>Events<ept id="p1">**</ept> node of a table extension shows events that are defined by the framework, and delegate methods that are defined by application developers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、テーブル拡張機能の<bpt id="p1">**</bpt>イベント<ept id="p1">**</ept>ノードの表示は、フレームワークによって定義されるイベントを表示し、アプリケーション開発者により定義されるメソッドを委任します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>5<ph id="ph2">\_</ph>Cust<ept id="p1">](./media/5_cust.png)](./media/5_cust.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>5<ph id="ph2">\_</ph>顧客<ept id="p1">](./media/5_cust.png)](./media/5_cust.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: Events are exposed on the designer on different element and sub-element types, like table events, form events, form data source events, form control events, and others.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記<ept id="p1">**</ept>: テーブルのイベント、フォームイベント、フォーム データ ソース イベント、フォーム コントロール イベントなどのイベントが、さまざまな要素タイプとサブ要素タイプのデザイナーに公開されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source>Open the context menu of an event node to interact with events:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントを操作するイベント ノードのコンテキスト メニューを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>6<ph id="ph2">\_</ph>Cust<ept id="p1">](./media/6_cust.png)](./media/6_cust.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>6<ph id="ph2">\_</ph>顧客<ept id="p1">](./media/6_cust.png)](./media/6_cust.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source><bpt id="p1">**</bpt>Copy event handler method<ept id="p1">**</ept>: This option copies a method signature to the clipboard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>*イベント ハンドラー メソッドのコピー<ept id="p1">**</ept>: このオプションは、メソッドシグネチャをクリップボードにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source>You can paste it in any X++ code editor to define a method that subscribes to the selected event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意の X++ コード エディターに貼り付けて、選択したイベントをサブスクライブするメソッドを定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source><bpt id="p1">**</bpt>Find event handlers<ept id="p1">**</ept>: Searches and lists all methods subscribed to the selected event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>イベント ハンドラーの検索<ept id="p1">**</ept> – 選択したイベントに登録されているすべてのメソッドを検索して一覧表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source><bpt id="p1">[</bpt>Customize model elements using extensions<ept id="p1">](customize-model-elements-extensions.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>拡張機能を使用してモデル要素をカスタマイズする<ept id="p1">](customize-model-elements-extensions.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
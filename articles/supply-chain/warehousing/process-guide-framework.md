<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="process-guide-framework.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>process-guide-framework.a80080.d05b09aeade1f3934e43b0dbc227e706db6c9eb2.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d05b09aeade1f3934e43b0dbc227e706db6c9eb2</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>c5edff04f35a067934fddebd166906edc003e7c5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/23/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\supply-chain\warehousing\process-guide-framework.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Process guide framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセス ガイド フレームワーク</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about the process guide framework for developers who are extending our warehouse mobile processes in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、X++ で倉庫モバイル プロセスを拡張する開発者のプロセス ガイド フレームワークに関する情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Process guide framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセス ガイド フレームワーク</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information about the process guide framework for developers who are extending the warehouse mobile processes in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、X++ で倉庫モバイル プロセスを拡張する開発者のプロセス ガイド フレームワークに関する情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The warehouse mobile processes are extensible as a result of the processes being broken into small steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">倉庫モバイル プロセスは、小さなステップに分割されるプロセスの結果として拡張可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The business logic and user interface building of each step has been extracted into individual classes, which allows for extensibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各ステップのビジネス ロジックおよびユーザー インターフェイスの作成は、個々のクラスに抽出されたため、拡張可能になりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Overview of the existing design</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のデザインの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The warehouse mobile execution flows are exposed through a single custom service endpoint.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">倉庫モバイル実行フローは、1 つのカスタム サービス エンドポイントを通じて公開されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The request arrives from the mobile app in the form of an XML string, which contains the metadata of the user interface presented in the mobile app, as well as the values entered by the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが入力した値に加えて、モバイル アプリケーションで表示されるユーザー インターフェイスのメタデータが含まれている、XML 文字列の形式でモバイル アプリケーションから要求が到達します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>When the request is received, the first step is to deserialize this XML.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求が受信されると、この XML を逆シリアル化するために最初の手順が実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The <bpt id="p1">**</bpt>WHSMobileAppServiceXMLTranslator<ept id="p1">**</ept> class converts the XML into a container, which contains both the control information, as well as session information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>WHSMobileAppServiceXMLTranslator<ept id="p1">**</ept> クラスは、コントロール情報とセッション情報の両方が含まれているコンテナーに XML を変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Following this, the information in the container is used to deduce which warehouse process the user is working on, or about to start (represented by the <bpt id="p1">**</bpt>WHSWorkExecuteMode<ept id="p1">**</ept> enumeration), and accordingly instantiate a derived class of <bpt id="p2">**</bpt>WHSWorkExecuteDisplay<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、コンテナーの情報は、ユーザーが作業する倉庫プロセス、開始しようとしている倉庫プロセス (<bpt id="p1">**</bpt>WHSWorkExecuteMode<ept id="p1">**</ept> 列挙によって表される)、それに応じて <bpt id="p2">**</bpt>WHSWorkExecuteDisplay<ept id="p2">**</ept> の派生クラスをインスタンス化する倉庫プロセスを推定するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The <bpt id="p1">**</bpt>displayform()<ept id="p1">**</ept> method is invoked, which then does the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>displayform()<ept id="p1">**</ept> メソッドが呼び出された後、以下が実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Processes the data from the user (delegated to the <bpt id="p1">**</bpt>WHSRFControlData<ept id="p1">**</ept> class, but some processes implement specific logic by overriding the <bpt id="p2">**</bpt>processControl()<ept id="p2">**</ept> method).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーからのデータの処理 (<bpt id="p1">**</bpt>WHSRFControlData<ept id="p1">**</ept> クラスに委任されますが、いくつかのプロセスは、<bpt id="p2">**</bpt>processControl()<ept id="p2">**</ept> メソッドを上書きすることによって特定のロジックを実装します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Executes business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス ロジックを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Increments the step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップが増加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Builds the container representing the new user interface (typically in a <bpt id="p1">**</bpt>build…()<ept id="p1">**</ept> method).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいユーザー インターフェイスを表すコンテナーを構築します (一般に、<bpt id="p1">**</bpt>build…()<ept id="p1">**</ept> メソッドで)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The container is then returned to the translator, which then serializes the XML, and sends it back as a response to the mobile device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーは、その後、変換元に返却されて XML がシリアル化され、モバイル デバイスへの応答として返送されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following sequence diagram shows an overview of the execution flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の順序図では、実行フローの概要を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Note that the diagram is more of a schematic overview and is not a 1:1 representation of the actual code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">図は概要図以上のものでり、実際のコードを 1:1 で表したものではないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Schematic overview of the process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスの概要図</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Reason for the redesign</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再設計の理由</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The above design offers a very simple framework for building processes used in mobile flows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の設計には、モバイル フローで使用されるプロセスを作成するための非常に単純なフレームワークが用意されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>However, as is evident above, the <bpt id="p1">**</bpt>displayform()<ept id="p1">**</ept> methods take over multiple responsibilities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、上記で明らかなように、<bpt id="p1">**</bpt>displayform()<ept id="p1">**</ept> メソッドが複数の職責を引き継ぎます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>It does delegate them to other methods and classes, but in the absence of concrete class responsibilities, it is done in an inconsistent manner across classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のメソッドおよびクラスに委任されますが、具体的なクラス職責がない場合は、クラス間で一貫性のある方法で実行されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Also, as the number of supported scenarios grows organically, some of those classes can become quite complex.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、サポートされるシナリオの数が増えるにつれて、これらのクラスの一部には非常に複雑になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>To make matters more interesting, some of those classes/methods are overridden and re-used in multiple modes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題をより魅力的にするために、これらのクラス/メソッドの一部が上書きされ、複数のモードで再利用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The result is extremely long methods with high cyclomatic complexity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果は、サイクロマティック複雑度の高い非常に長いメソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>These have posed maintenance issues in the past.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">過去には、保守の問題が生じていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Fixing bugs in these methods has been risky and regression prone.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドのバグを修正することは危険であり、後戻りする傾向がありました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>For example, the <bpt id="p1">**</bpt>processWorkLine()<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>WhsWorkExecuteDisplay<ept id="p2">**</ept> class is referred from multiple processes (basically, anywhere where work execution is performed).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p2">**</bpt>WhsWorkExecuteDisplay<ept id="p2">**</ept> クラス内の <bpt id="p1">**</bpt>processWorkLine()<ept id="p1">**</ept> メソッドは、複数のプロセス (基本的に、作業の実行が実行される任意の場所) から参照されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>To make these extensible, one of the options would be to split the <bpt id="p1">**</bpt>displayForm<ept id="p1">**</ept> methods into smaller methods and introduce extensibility points.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらを拡張可能にするため、いずれかのオプションは、<bpt id="p1">**</bpt>displayForm<ept id="p1">**</ept> メソッドを小さなメソッドに分割して拡張ポイントを導入するためのものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>However, because of the scenario matrix, it would be challenging for partners to write extensions and validate against regressions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、シナリオ マトリックスのため、拡張機能を記述し、逆光を検証することはパートナーにとって困難です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Not only that, because of the lack of structured responsibility distribution noted above, the code would keep growing in unpredictable ways over time, posing challenges in building quality extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それだけでなく、上記の構造化された責任の配分がないため、コードは徐々に予期しない方法で増加し、品質の高い拡張機能を構築することが困難になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>As a result, the redesign is the sustainable option, with a goal to have clearly defined classes having independent responsibilities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その結果、再設計は、明確に定義されたクラスに独立した職責を持たせるという目標を持つ、持続可能なオプションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>A class should have one responsibility, one reason to change, and one reason to be extended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスの職責、変更する理由、拡張する理由は 1 つにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Design overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設計の概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In the redesigned framework, the core strategy revolves around two principles: divide the execution flow into individual components with well-defined responsibilities and have well-defined extension points in each of the components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再設計されたフレームワークでは、中核的な戦略は 2 つの原則を中心に展開しています。実行フローを明確に定義された責任を持つ個々のコンポーネントに分割することと、各コンポーネントに適切に定義された拡張点を持つことです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The name for the new framework is “ProcessGuide”.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいフレームワークの名前は、"ProcessGuide" です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>This is because the aim of these classes is to guide a user through a business process (as opposed to the rich client which is a form-based experiences where the user has more flexibility in how they interact with the data or in which order they perform tasks).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、これらのクラスの目的が、業務プロセスを通じてユーザーをガイドすることだからです (データとやり取りする方法、またはタスクを実行する順序に関してユーザーがさらに柔軟性を持っているフォーム ベースのエクスペリエンスであるリッチ クライアントとは対照的)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>One notable detail is the deliberate omission of the “WHS” prefix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つの重要な詳細は、"WHS" 接頭語の意図的な省略です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>While the mobile processes were initially introduced for warehousing, subsequently they have transcended boundaries to support various production and inventory management processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル プロセスは当初倉庫管理に導入されましたが、その結果、さまざまな生産および在庫管理プロセスをサポートするための超越した境界が生じました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>As a result, the warehouse reference was excluded in the name of the framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その結果、倉庫の参照はフレームワークの名前から除外されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>To identify the components, the first step is to look at the Production Start process (<bpt id="p1">**</bpt>WhsWorkExecuteDisplayProdStart<ept id="p1">**</ept> class).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネントを識別するために、まず、プロセスの生産の開始を調べます (<bpt id="p1">**</bpt>WhsWorkExecuteDisplayProdStart<ept id="p1">**</ept> クラス)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Here is a schematic of the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次にプロセスの概要図を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Image of schematic process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスの概要図の画像</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Looking at the control flow, the following are components needed:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">制御フローを見ると、次のコンポーネントが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>A controller to stitch through the entire business process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス プロセス全体を通じて合成するコントローラー。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>A step responsible for execution of a step in the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスでステップの実行を担当するステップ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>A data processor for processing the data in a step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ内のデータを処理するためのデータ プロセッサ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A page builder responsible for building the user interface for a step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップのユーザー インターフェイスの作成を担当するページ ビルダー。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>A navigation agent responsible for step transition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップの移行を担当するナビゲーション エージェント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>A class responsible for executing the business process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務プロセスの実行を担当するクラス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In the process flow diagram above, if you begin at step 1 and start processing the data from the previous step, and then end with building a UI, data would continue to be processed in the next step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上のプロセス フロー図では、手順 1 から開始し、前の手順からのデータの処理を開始した後、最後に UI を構築した場合、データは次の手順で処理され続けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>This introduces a tight coupling between consecutive steps, as a result, our new high-level schematic would look like the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、連続したステップ間に厳密な結合が生まれ、その結果、高レベルの新しい概略図は次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Image of high-level schematic process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高レベルのプロセス概略図の画像</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The following are the key components in the redesigned process:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下は、再設計されたプロセスの重要なコンポーネントです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> - This class orchestrates the overall execution of the business process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> - このクラスは、業務プロセスの全体的な実行を調整します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>It defines the factories that instantiate the step and the navigation agent, which subsequently constitute the process execution, as well as the clean-up logic for cancellation or exiting the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、ステップとナビゲーション エージェントのインスタンスを作成し、その結果、プロセスの実行と、キャンセルまたはプロセスの終了のためのクリーンアップ ロジックを構成するファクトリを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>ProcessGuideStep<ept id="p1">**</ept> - This class represents one single step in the business process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideStep<ept id="p1">**</ept> - このクラスは、業務プロセスの 1 つのステップを表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>This class contains a definition of the factories that instantiate a page builder, actions, and data processors and is responsible for invoking them in the correct sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスは、ページ ビルダー、アクション、およびデータ プロセッサのインスタンスを作成するファクトリの定義を含み、それらを正しい順序で呼び出することを担当します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>ProcessGuideNavigationAgent<ept id="p1">**</ept> - This class is responsible for navigation between the steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideNavigationAgent<ept id="p1">**</ept> - このクラスは、手順間の移動を担当します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>When a step is completed, the navigation agent is responsible for defining the next step and passes any parameters that the previous step may need to communicate to the next one.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップが完了したら、ナビゲーション エージェントは、次のステップの定義を担当し、前の手順が次の手順に伝達する必要があるすべてのパラメーターを渡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>ProcessGuidePageBuilder<ept id="p1">**</ept> - This class is responsible for instantiating the user interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuidePageBuilder<ept id="p1">**</ept> - このクラスは、ユーザー インターフェイスのインスタンス化を担当します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>ProcessGuideAction<ept id="p1">**</ept> - This class represents an action, shown as a button to the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideAction<ept id="p1">**</ept> - このクラスは、ユーザーにボタンとして表示される、アクションを表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><bpt id="p1">**</bpt>ProcessGuideDataProcessor<ept id="p1">**</ept> - This class is responsible for processing the user entered data in a field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideDataProcessor<ept id="p1">**</ept> - このクラスは、フィールド内のユーザーが入力したデータの処理を担当します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Execution flow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行フロー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The starting point of the execution flow remains unchanged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行フローの開始点は変更されないままです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>So, the request still arrives through the same endpoints, followed by deserializing the XML into the container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、要求は引き続き同じエンドポイントに到着し、その後、コンテナーに XML が逆シリアル化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>This container is then passed to <bpt id="p1">**</bpt>getNextFormState()<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコンテナーは、<bpt id="p1">**</bpt>getNextFormState()<ept id="p1">**</ept> にに渡されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>There are three important classes to note:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注目すべき次の 3 つの重要なクラスがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source><bpt id="p1">**</bpt>ProcessGuideSessionState<ept id="p1">**</ept> – This contains the session state information – mode, pass, controller, and step being executed, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideSessionState<ept id="p1">**</ept> - これは、セッション状態情報 (モード、合格、コントローラー、および実行される手順など) を含みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">**</bpt>ProcessGuidePage<ept id="p1">**</ept> – This contains a strongly-typed representation of the user interface metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuidePage<ept id="p1">**</ept> - これには、ユーザー インターフェイス メタデータの厳密に表したものが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">**</bpt>ProcessGuideRequest<ept id="p1">**</ept> – This contains the above two as members and is a strongly-typed representation of the request received from the mobile device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideRequest<ept id="p1">**</ept> - これには、メンバーとして上記の 2 つが含まれており、モバイル デバイスから受信した要求を厳密に表したものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>These classes are created using the container information (both state and user entered control data).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのクラスは、コンテナー情報を使用して作成されます (状態とユーザー入力管理データの両方)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This provides a type-safe way to access and manipulate the values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、値にアクセスして操作するためのタイプ セーフな方法が提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Compared to repeated access of the container during the process, this provides benefit both in terms of readability and performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセス中のコンテナーの繰り返しアクセスと比較して、これは、信頼性とパフォーマンスの両方に関して利点を生み出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The session state information is used to instantiate the correct <bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セッション状態情報は、適切な <bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> クラスのインスタンスを作成するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Once instantiated, the <bpt id="p1">**</bpt>createResponse()<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>ProcessGuideController<ept id="p2">**</ept> class is invoked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンスが作成されると、<bpt id="p2">**</bpt>ProcessGuideController<ept id="p2">**</ept> クラス内の <bpt id="p1">**</bpt>createResponse()<ept id="p1">**</ept> メソッドが呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This method is the entry point to the process guide logic, and after execution, comes back with the response (represented in the <bpt id="p1">**</bpt>ProcessGuideResponse<ept id="p1">**</ept> class).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、プロセス ガイド ロジックへのエントリ ポイントであり、実行後、応答で戻ります (<bpt id="p1">**</bpt>ProcessGuideResponse<ept id="p1">**</ept> クラスで表される)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>The response is then converted back to the container and handed back to the legacy logic, which then serializes it to the XML and sends the response back to the mobile device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">応答は、その後コンテナーに変換されて、レガシ トピックに戻された後、XML にシリアル化され、応答がモバイル デバイスに戻されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Next, the controller needs to find the next step to execute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、コントローラーは実行する次の手順を見つける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>If this is the start of a new process, the controller will call <bpt id="p1">**</bpt>initialStep()<ept id="p1">**</ept> to get the first step in the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これが新しいプロセスの開始である場合、コントローラーは <bpt id="p1">**</bpt>initialStep()<ept id="p1">**</ept> を呼び出して、プロセスの最初の手順を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>After that, it would call <bpt id="p1">**</bpt>execute()<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>ProcessGuideStep<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p2">**</bpt>ProcessGuideStep<ept id="p2">**</ept> で <bpt id="p1">**</bpt>execute()<ept id="p1">**</ept> メソッドを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>This method would then instantiate a <bpt id="p1">**</bpt>ProcessGuidePageBuilder<ept id="p1">**</ept> class and call <bpt id="p2">**</bpt>buildPage()<ept id="p2">**</ept>, which would return with a <bpt id="p3">**</bpt>ProcessGuidePage<ept id="p3">**</ept> object, which is a virtual representation of the user interface to be presented to the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法はその後、<bpt id="p1">**</bpt>ProcessGuidePageBuilder<ept id="p1">**</ept> クラスのインスタンスを作成し、<bpt id="p2">**</bpt>buildPage()<ept id="p2">**</ept> を呼び出します。これにより、ユーザーに表示されるユーザー インターフェイスの仮想表現である <bpt id="p3">**</bpt>ProcessGuidePage<ept id="p3">**</ept> オブジェクトが返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The step would then send the result back to the controller, which would then save the current session state and then return the result back to <bpt id="p1">**</bpt>getNextFormState()<ept id="p1">**</ept> in the form of the <bpt id="p2">**</bpt>ProcessGuideResponse<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、ステップは結果をコントローラーに戻します。それから、現在のセッションの状態が保存され、結果が <bpt id="p2">**</bpt>ProcessGuideResponse<ept id="p2">**</ept> クラスの形式で <bpt id="p1">**</bpt>getNextFormState()<ept id="p1">**</ept> に戻されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Thereafter, the response is converted back to the container, and subsequently serializes to XML and sends back the response to the mobile device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、応答はコンテナーにもう一度変換され、その結果、XML にシリアル化されて、モバイル デバイスに応答が返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The following sequence diagram explains this control flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のシーケンス図では、この制御フローについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Note that this is the most common control flow, simplified for explaining the design.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、設計を説明するために簡略化された、最も一般的な制御フローである点に注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Control flow simplified</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">簡略化された制御フロー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>When the user takes an action on the mobile device by clicking a button (or scanning a value – which typically triggers the default action) – the request arrives at the <bpt id="p1">**</bpt>createResponse()<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>ProcessGuideController<ept id="p2">**</ept> class through the same route.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがボタンをクリックして (または、通常は既定のアクションをトリガーする値をスキャンして) モバイル デバイスでアクションを実行すると、要求は同じルートを経由して <bpt id="p2">**</bpt>ProcessGuideController<ept id="p2">**</ept> クラス内の <bpt id="p1">**</bpt>createResponse()<ept id="p1">**</ept> メソッドに到着します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>This time, however, the controller knows from the session state information which step the user is in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、このとき、コントローラーはセッション状態情報から、ユーザーがいるステップを知ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Accordingly, it instantiates the appropriate <bpt id="p1">**</bpt>ProcessGuideStep<ept id="p1">**</ept> class and invokes the execute method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、適切な <bpt id="p1">**</bpt>ProcessGuideStep<ept id="p1">**</ept> クラスのインスタンスを作成し、実行メソッドを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The <bpt id="p1">**</bpt>ProcessGuideStep<ept id="p1">**</ept>, in turn, reads the action name invoked by the user and then instantiates the appropriate <bpt id="p2">**</bpt>ProcessGuideAction<ept id="p2">**</ept> class and calls <bpt id="p3">**</bpt>execute()<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、<bpt id="p1">**</bpt>ProcessGuideStep<ept id="p1">**</ept>はユーザーによって呼び出されるアクション名を読み取り、適切な <bpt id="p2">**</bpt>ProcessGuideAction<ept id="p2">**</ept> クラスをインスタンス化して <bpt id="p3">**</bpt>execute()<ept id="p3">**</ept> を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The <bpt id="p1">**</bpt>ProcessGuideAction<ept id="p1">**</ept> class is responsible for executing the specific action, however there are two notable exceptions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideAction<ept id="p1">**</ept> クラスは、特定のアクションを実行することを担当しますが、2 つの重要な例外があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>The first one is the <bpt id="p1">**</bpt>ProcessGuideOKAction<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つ目は、<bpt id="p1">**</bpt>ProcessGuideOKAction<ept id="p1">**</ept> クラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>This action implies that the user wants to confirm and move forward in the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアクションは、ユーザーがプロセスを確認して前に動かすことを求めていることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>In accordance to that – this method actually does a callback to the ProcessGuideStep class, which means that the step invokes <bpt id="p1">**</bpt>processData()<ept id="p1">**</ept> in <bpt id="p2">**</bpt>ProcessGuideDataProcessor<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それに従って、このメソッドは実際に ProcessGuideStep クラスへのコールバックを行います。これは、ステップが <bpt id="p2">**</bpt>ProcessGuideDataProcessor<ept id="p2">**</ept> で <bpt id="p1">**</bpt>processData()<ept id="p1">**</ept> を呼び出すことを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>This processes the data that the user has entered, and then updates the state of the step and sends the result back to the controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、ユーザーが入力したデータを処理し、ステップの状態を更新し、結果をコントローラーに返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Depending on the outcome of the processor, the step invokes the page builder to build the appropriate user interface or sets the status of the step as completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセッサの結果によっては、ステップは適切なユーザー インターフェイスを構築するためのページ ビルダーを起動するか、ステップのステータスを完了に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>This is reflected in the top half of the sequence diagram below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、次のシーケンス図の上半分に反映されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>The other exception is the cancellation action, implemented in the <bpt id="p1">**</bpt>ProcessGuideCancelResetProcessAction<ept id="p1">**</ept> and <bpt id="p2">**</bpt>ProcessGuideCancelExitProcessAction<ept id="p2">**</ept> classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他の例外は、<bpt id="p1">**</bpt>ProcessGuideCancelResetProcessAction<ept id="p1">**</ept> および <bpt id="p2">**</bpt>ProcessGuideCancelExitProcessAction<ept id="p2">**</ept> クラスで実装されている取消アクションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>These actions represent an intent to cancel the process and go back to either the start of the process or exit the process altogether.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのアクションは、処理をキャンセルする意図を表し、プロセスの開始またはプロセスの終了を完全に戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Similar to the <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> action, these actions also perform a callback to the step, which signals the intent to the <bpt id="p2">**</bpt>ProcessGuideController<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> アクションと同様、これらのアクションも、ステップにコールバックを実行します。これは、<bpt id="p2">**</bpt>ProcessGuideController<ept id="p2">**</ept> に意図を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>The controller then performs the necessary cleanup of state variables and either moves control to the initial step in the process or terminates the process altogether.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、コントローラーは状態変数の必要なクリーンアップを実行し、コントロールをプロセスにおける最初のステップに移動するか、プロセスを完全に終了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>After the step is completed, if the status of the step is set to <bpt id="p1">**</bpt>Completed<ept id="p1">**</ept>, then the controller instantiates the <bpt id="p2">**</bpt>ProcessGuideNavigationAgent<ept id="p2">**</ept>, which returns the name of the next step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップが完了した後、ステップのステータスが <bpt id="p1">**</bpt>完了<ept id="p1">**</ept> に設定されている場合、コントローラーは <bpt id="p2">**</bpt>ProcessGuideNavigationAgent<ept id="p2">**</ept> のインスタンスを作成し、次のステップの名前が返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>The controller then instantiates this step and invokes the <bpt id="p1">**</bpt>execute()<ept id="p1">**</ept> method – and the cycle continues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、コントローラーはこのステップをインスタンス化し、<bpt id="p1">**</bpt>execute()<ept id="p1">**</ept> メソッドを呼び出します。サイクルが続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Most commonly, the new step invokes the corresponding <bpt id="p1">**</bpt>ProcessGuidePageBuilder<ept id="p1">**</ept> to build the user interface for the next screen to be presented to the user, which is then sent back.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの場合、新しい手順は、対応する <bpt id="p1">**</bpt>ProcessGuidePageBuilder<ept id="p1">**</ept> を呼び出し、ユーザーに表示した後に戻される次の画面のユーザー インターフェイスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>This flow is depicted in the lower half of the sequence diagram below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフローは、次のシーケンス図の下半分に反映されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>sequence diagram</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シーケンス図</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Building a new process using the ProcessGuide framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProcessGuide フレームワークを使用した新しいプロセスの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>The best way to explain the control flow is by using an example that exists in the application – the Production Start process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">制御フローを説明する最善の方法は、アプリケーションに存在している例を使用することです (生産開始プロセス)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Overview of the production start process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産開始プロセスの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Let’s start by understanding the process flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">まず、プロセス フローを理解しましょう。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>In the first step, the user is prompted for production order ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の手順で、ユーザーは製造オーダー ID の入力を求められます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Prompt for production ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産 ID の確認</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>When the user enters the production order ID, the order number is validated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製造オーダー ID をユーザーが入力すると、注文番号が検証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Some of the validations that are run are based on whether the order is in the same warehouse as the user is signed in to, and the status of the order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行される検証の一部は、ユーザーがログインしているのと同じ倉庫に注文があるかどうかと、注文のステータスに基づいています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If the validation fails, the user is shown an error message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証が失敗すると、ユーザーにはエラー メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>If the validation succeeds, then the user is shown details of the production order and item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証が正常に実行された場合、ユーザーには、製造オーダーと品目の詳細が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>The user can either cancel to go back to the start of the process or click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to confirm.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーはキャンセルしてプロセスの開始に戻るか、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックして確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>In the latter case, the production order is set to <bpt id="p1">**</bpt>Started<ept id="p1">**</ept> status, the corresponding journals are posted, the control moves back to the first step, and the “Work Completed” message is shown to the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後者の場合は、製造オーダーが <bpt id="p1">**</bpt>開始済<ept id="p1">**</ept> ステータスに設定され、対応する仕訳帳が転記され、コントロールが最初の手順に戻り、ユーザーに ”作業完了" というメッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Creating the controller</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラーの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The first step in building the business process is creating the controller class, extending from the <bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> abstract class which implements the default behaviors of a controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務プロセスの作成の最初の手順は、コントローラー クラスの作成です。これは、コントローラーのデフォルトの動作を実装する <bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> 抽象クラスから拡張されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>The new class name is <bpt id="p1">**</bpt>ProdProcessGuideProductionStartController<ept id="p1">**</ept> and decorated with the <bpt id="p2">**</bpt>WHSWorkExecuteMode<ept id="p2">**</ept> value of <bpt id="p3">**</bpt>StartProdOrder<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいクラスの名前は <bpt id="p1">**</bpt>ProdProcessGuideProductionStartController<ept id="p1">**</ept> であり、<bpt id="p3">**</bpt>StartProdOrder<ept id="p3">**</ept> の <bpt id="p2">**</bpt>WHSWorkExecuteMode<ept id="p2">**</ept> で修飾されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The same <bpt id="p1">**</bpt>SysExtension<ept id="p1">**</ept> based instantiation that was used in the <bpt id="p2">**</bpt>WHSWorkExecuteDisplay<ept id="p2">**</ept> classes is used, which helps instantiate the controller when the user executes a menu item for this mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>WHSWorkExecuteDisplay<ept id="p2">**</ept> クラスで使用されたのと同じ <bpt id="p1">**</bpt>SysExtension<ept id="p1">**</ept> ベースのインスタンス化が使用されます。これは、ユーザーがこのモードのメニュー項目を実行するときにコントローラーをインスタンス化するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The naming pattern of the class is <bpt id="p1">**</bpt><ph id="ph1">\&lt;</ph>FunctionalArea<ph id="ph2">\&gt;</ph>ProcessGuide<ph id="ph3">\&lt;</ph>Businessprocessname<ph id="ph4">\&gt;</ph>Controller<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスの名前付けパターンは、<bpt id="p1">**</bpt><ph id="ph1">\&lt;</ph>FunctionalArea<ph id="ph2">\&gt;</ph>ProcessGuide<ph id="ph3">\&lt;</ph>Businessprocessname<ph id="ph4">\&gt;</ph>Controller<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>This is the pattern that is used for the controller classes and to extend to other classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コントローラー クラスに使用されるパターンであり、その他のクラスを拡張するためのものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Building the first step</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のステップの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Next, to define the first step you create the <bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept> class, extending from <bpt id="p2">**</bpt>ProcessGuideStep<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、最初のステップを定義するには、<bpt id="p2">**</bpt>ProcessGuideStep<ept id="p2">**</ept> から拡張して、<bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept> クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>The task of instantiating the class is delegated to a step factory, which is invoked by the <bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> base class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスのインスタンス化を作成するタスクは、<bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> 基本クラスによって呼び出されるステップ ファクトリに委任されます。。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The default implementation of the factory instantiates the step based on name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファクトリの既定の実装は、名前に基づいてステップをインスタンス化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Therefore, to instantiate <bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept> as the first step in the controller, you must do two things:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、コントローラーの最初のステップとして <bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept> のインスタンスを作成するには、2 つの操作を行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Decorate the <bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept> class with a <bpt id="p2">**</bpt>ProcessGuideStepName<ept id="p2">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept> クラスを <bpt id="p2">**</bpt>ProcessGuideStepName<ept id="p2">**</ept> 属性で修飾します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>In the controller class, implement the abstract method <bpt id="p1">**</bpt>initialStepName()<ept id="p1">**</ept> to return the step name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー クラスで、抽象メソッド <bpt id="p1">**</bpt>initialStepName()<ept id="p1">**</ept> を実装して、ステップの名前を戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>The value in the <bpt id="p1">**</bpt>ProcessGuideStepName<ept id="p1">**</ept> attribute does not need to exactly match the class name as shown above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideStepName<ept id="p1">**</ept> 属性の値は、上記のように、クラス名と完全に一致する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>However, implementing this allows for uniformity and type-safety around cross-references when using the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、これを実装することにより、クラスを使用する場合の相互参照に関する均一性とタイプ セーフが生じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Using this naming convention is recommended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この名前付け規則を使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The <bpt id="p1">**</bpt>ProcessGuideStepName<ept id="p1">**</ept> based instantiation of the step is implemented in the <bpt id="p2">**</bpt>ProcessGuideStepDefaultFactory<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップの <bpt id="p1">**</bpt>ProcessGuideStepName<ept id="p1">**</ept> ベースのインスタンス化は、<bpt id="p2">**</bpt>ProcessGuideStepDefaultFactory<ept id="p2">**</ept> クラスで実装されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>In the rare case that you want a different strategy for instantiating the step, you need to do the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">まれに、異なる戦略でステップのインスタンス化が必要になることがありますが、その場合は次のようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Create a new factory class inheriting from <bpt id="p1">**</bpt>ProcessGuidStepAbstractFactory<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuidStepAbstractFactory<ept id="p1">**</ept> から継承する新しいファクトリ クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Optionally, create a new parameter class implementing the <bpt id="p1">**</bpt>ProcessGuideIStepCreationParameters<ept id="p1">**</ept> interface, containing the parameters the factory would need.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、ファクトリが必要とするパラメーターを含む <bpt id="p1">**</bpt>ProcessGuideIStepCreationParameters<ept id="p1">**</ept> インターフェイスを実装する新しいパラメーター クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>In your controller class, override the <bpt id="p1">**</bpt>stepFactory()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>stepCreationParameters()<ept id="p2">**</ept> methods to return the above factory and parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー クラスで、<bpt id="p1">**</bpt>stepFactory()<ept id="p1">**</ept> および <bpt id="p2">**</bpt>stepCreationParameters()<ept id="p2">**</ept> メソッドを上書きし、上記のファクトリとパラメータを返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The next step is to implement the functionality of the <bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップでは、<bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept> クラスの機能を実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>You need to implement the logic for building the user interface, processing the user-entered data, and determining when the step is complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが入力したデータを処理し、ステップがいつ完了するかを決定するためのユーザー インターフェイスを構築するためのロジックを実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Building the user interface for the first step</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のステップのユーザー インターフェイスの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>The user interface is built using a class inheriting from the <bpt id="p1">**</bpt>ProcessGuidePageBuilder<ept id="p1">**</ept> abstract class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー インターフェイスは、<bpt id="p1">**</bpt>ProcessGuidePageBuilder<ept id="p1">**</ept> 抽象クラスからから継承するクラスを使用して作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>For this step, name the class to represent what it does – <bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdPageBuilder<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順では、<bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdPageBuilder<ept id="p1">**</ept> が何をするかを表すクラスを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>The instantiation mechanism of the class is similar to how the step was instantiated from the controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスのインスタンス化メカニズムは、ステップがコントローラーからインスタンス化された方法と似ています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Decorate the <bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdPageBuilder<ept id="p1">**</ept> class with a <bpt id="p2">**</bpt>ProcessGuidePageBuilderName<ept id="p2">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdPageBuilder<ept id="p1">**</ept> クラスを <bpt id="p2">**</bpt>ProcessGuidePageBuilderName<ept id="p2">**</ept> 属性で修飾します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In the <bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept> class, implement the abstract method <bpt id="p2">**</bpt>pageBuilderName()<ept id="p2">**</ept> to return this name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept> クラスで、抽象メソッド <bpt id="p2">**</bpt>pageBuilderName()<ept id="p2">**</ept> を実装してこの名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Similar to the step factory, there is also an abstract factory pattern implemented for the page builder factory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ ファクトリと同様、ページ ビルダ ファクトリに実装される抽象ファクトリ パターンもあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>So, in the rare case that you want a different strategy for instantiating the page builder, you can do the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ですから、まれに、異なる戦略でページ ビルダーのインスタンス化が必要になることがありますが、その場合は次のようにすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Create a new factory class inheriting from <bpt id="p1">**</bpt>ProcessGuidePageBuilderAbstractFactory<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuidePageBuilderAbstractFactory<ept id="p1">**</ept> から継承する新しいファクトリ クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Optionally, create a new parameter class implementing the <bpt id="p1">**</bpt>ProcessGuideIPageBuilderCreationParameters<ept id="p1">**</ept> interface, containing the parameters the factory would need.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、ファクトリが必要とするパラメーターを含む <bpt id="p1">**</bpt>ProcessGuideIPageBuilderCreationParameters<ept id="p1">**</ept> インターフェイスを実装する新しいパラメーター クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>In your step class, override the <bpt id="p1">**</bpt>pageBuilderFactory()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>pageBuilderCreationParameters()<ept id="p2">**</ept> methods to return the above factory and parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ クラスで、<bpt id="p1">**</bpt>pageBuilderFactory()<ept id="p1">**</ept> および <bpt id="p2">**</bpt>pageBuilderCreationParameters()<ept id="p2">**</ept> メソッドを上書きし、上記のファクトリとパラメータを返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>To implement the user interface you need a page with one text box to enter the production order ID, plus an <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> button and a <bpt id="p2">**</bpt>Cancel<ept id="p2">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー インターフェイスを実装するには、製造オーダー ID を入力するための 1 つのテキスト ボックスに加えて、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> ボタンおよび <bpt id="p2">**</bpt>キャンセル<ept id="p2">**</ept> ボタンがあるページが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>The <bpt id="p1">**</bpt>Cancel<ept id="p1">**</ept> button should exit the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>キャンセル<ept id="p1">**</ept> ボタンは、プロセスを終了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>To implement this, you need to override two methods in the <bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdPageBuilder<ept id="p1">**</ept> class:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを実装するには、<bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdPageBuilder<ept id="p1">**</ept> クラスで 2 つのメソッドを上書きする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Use the <bpt id="p1">**</bpt>addDataControls()<ept id="p1">**</ept> method to add the text box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>addDataControls()<ept id="p1">**</ept> メソッドを使用してテキスト ボックスを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Use the <bpt id="p1">**</bpt>addActionControls()<ept id="p1">**</ept> method to add the <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Cancel<ept id="p3">**</ept> buttons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>addActionControls()<ept id="p1">**</ept> メソッドを使用して <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> および <bpt id="p3">**</bpt>Cancel<ept id="p3">**</ept> ボタンを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>``protected final void addActionControls(ProcessGuidePage _page) {</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">``protected final void addActionControls(ProcessGuidePage _page) {</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>}``</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">}``</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>This adds the data controls, followed by the buttons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、ボタンの前に、データ コントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>However, if you want to build a screen with interspersed data controls and buttons, you can override the <bpt id="p1">**</bpt>addControls()<ept id="p1">**</ept> method instead for flexibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、データ コントロールとボタンが散在する画面を作成する場合、柔軟性の代わりに <bpt id="p1">**</bpt>addControls()<ept id="p1">**</ept> メソッドを上書きできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>An additional scenario to consider is how to rebuild the page in case of validation failures, for example if the user enters an incorrect production order ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">考慮すべきの追加のシナリオは、たとえば、ユーザーが正しくない製造オーダー ID を入力した場合など、検証エラーが発生した場合にページを再構築する方法です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>The <bpt id="p1">**</bpt>ProcessGuidePageBuilder<ept id="p1">**</ept> base class implements the default behavior, which rebuilds the user interface, clears out the scanned value, and adds the error control with the error message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuidePageBuilder<ept id="p1">**</ept> 基本クラスは、ユーザー インターフェイスを再構築し、スキャンした値をクリアし、エラー メッセージのあるエラー コントロールを追加するという、既定の動作を実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Because this is the default behavior that you want to use, you do not need to add any code for handling errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、使用する既定の動作であるため、エラーを処理するコードを追加する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If you want to implement custom UI behavior for error situations, you can override one or more of the methods <bpt id="p1">**</bpt>rebuildFromRequestPage()<ept id="p1">**</ept>, <bpt id="p2">**</bpt>isErrorState()<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>reuseRequestPageOnError()<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー状況のカスタム UI 動作を実装する場合は、1 つまたは複数のメソッド <bpt id="p1">**</bpt>rebuildFromRequestPage()<ept id="p1">**</ept>、<bpt id="p2">**</bpt>isErrorState()<ept id="p2">**</ept>、および <bpt id="p3">**</bpt>reuseRequestPageOnError()<ept id="p3">**</ept> を上書きすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Processing the user-entered data in the first step</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の手順でユーザーが入力したデータの処理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>The processing of the data is done in the <bpt id="p1">**</bpt>ProcessGuideDataProcessorDefault<ept id="p1">**</ept> class, which in turn invokes the legacy <bpt id="p2">**</bpt>WhsRfControlData<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データの処理は、<bpt id="p1">**</bpt>ProcessGuideDataProcessorDefault<ept id="p1">**</ept> クラスで行われ、その後、レガシ <bpt id="p2">**</bpt>WhsRfControlData<ept id="p2">**</ept> クラスが呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>No changes are needed to this default behavior, and <bpt id="p1">**</bpt>WhsRfControlData<ept id="p1">**</ept> already has logic for validating the <bpt id="p2">**</bpt>ProdId<ept id="p2">**</ept> field, so you do not need to write any logic for handling this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この既定の動作を変更する必要はありません。<bpt id="p1">**</bpt>WhsRfControlData<ept id="p1">**</ept> には、既に <bpt id="p2">**</bpt>ProdId<ept id="p2">**</ept> フィールを検証するロジックがあるため、これを処理するロジックを記述する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>In case of required extensions for the validation logic, consider using the <bpt id="p1">**</bpt>WhsControl<ept id="p1">**</ept> based extension mechanism.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証ロジックに必要な機能拡張がある場合、<bpt id="p1">**</bpt>WhsControl<ept id="p1">**</ept> ベースの拡張メカニズムを使用することを検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Determine if the first step is complete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の手順が完全であるかどうかを判断</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>When the validation is successful, it is time to mark the step as completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証に成功したらを、ステップを完了としてマークします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>This is done in the base class, however, you need to implement the condition to determine the step completion.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、基本クラスで行われますが、手順の完了を決定する条件を実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>The following overridden method does that.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーライドされた次のメソッドがそれを行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Step two: View order details and confirm</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 2: 注文の詳細を表示して確認</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>In the second step in the process, the user is shown a screen with details about the order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスの 2 番目のステップでは、ユーザーに、注文に関する詳細を含む画面が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The user can either click the <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> button to confirm the start of the production order, or click <bpt id="p2">**</bpt>Cancel<ept id="p2">**</ept> to go back to the start of the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> ボタンをクリックして製造オーダーの開始を確認するか、<bpt id="p2">**</bpt>キャンセル<ept id="p2">**</ept> をクリックしてプロセスの開始に戻ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>For this example, name the step <bpt id="p1">**</bpt>ProdProcessGuideConfirmProductionOrderStep<ept id="p1">**</ept> and the page builder class <bpt id="p2">**</bpt>ProdProcessGuideConfirmProductionOrderPageBuilder<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、ステップ <bpt id="p1">**</bpt>ProdProcessGuideConfirmProductionOrderStep<ept id="p1">**</ept> とページ ビルダー クラス <bpt id="p2">**</bpt>ProdProcessGuideConfirmProductionOrderPageBuilder<ept id="p2">**</ept> を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>The ProdProcessGuideConfirmProductionOrderStep class looks like the following.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProdProcessGuideConfirmProductionOrderStep クラスは、次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Because the user does not enter any values here, you do not need to override the <bpt id="p1">**</bpt>isComplete()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーはここに値を入力してないため、<bpt id="p1">**</bpt>isComplete()<ept id="p1">**</ept> メソッドを上書きする必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>The step is complete when the user clicks <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックすると、ステップが完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The page builder class overrides the <bpt id="p1">**</bpt>addDataControls()<ept id="p1">**</ept> method to add three labels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ ビルダー クラスは、<bpt id="p1">**</bpt>addDataControls()<ept id="p1">**</ept> メソッドを上書きして 3 つのラベルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The first label shows the production order ID, the second contains item information (such as item ID, dimensions, or description) and the third contains the quantity and unit of measure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のラベルには、製造オーダー ID が表示され、2 番目には、品目情報 (品目 ID、分析コード、説明など) が表示され、3 番目には数量との測定単位が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>The <bpt id="p1">**</bpt>addActionControls()<ept id="p1">**</ept> is then overridden to add 2 buttons – the <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> button, and the <bpt id="p3">**</bpt>Cancel<ept id="p3">**</ept> button to cancel the process and go back to the start of the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>addActionControls()<ept id="p1">**</ept> が上書きされ、2 つのボタン (<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> ボタンと、プロセスをキャンセルしてプロセスの先頭に戻る <bpt id="p3">**</bpt>Cancel<ept id="p3">**</ept> ボタン) を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Process guide page builder code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセス ガイド ページ ビルダー コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Step 3: Start the production order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 3: 製造オーダーを開始する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>The third step is where the business logic of starting the production order is executed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 番目のステップでは、製造オーダーの開始のビジネス ロジックを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>This step is somewhat different from the previous steps, in that, this step does not have a user interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップは、ユーザー インターフェイスがないという点で前のステップとは少し異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>This step gets executed silently when the user clicks <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> in the previous step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが前のステップで <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックすると、このステップがサイレントで実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>The <bpt id="p1">**</bpt>ProcessGuideStepWithoutPrompt<ept id="p1">**</ept> abstract class implements the default behavior for such steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideStepWithoutPrompt<ept id="p1">**</ept> 抽象クラスは、そのようなステップの既定の動作を実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>The current step, therefore, should extend the <bpt id="p1">**</bpt>ProcessGuideStepWithoutPrompt<ept id="p1">**</ept> class and override the <bpt id="p2">**</bpt>doExecute()<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、現在のステップは、<bpt id="p1">**</bpt>ProcessGuideStepWithoutPrompt<ept id="p1">**</ept> クラスを拡張し、<bpt id="p2">**</bpt>doExecute()<ept id="p2">**</ept> メソッドを上書きする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>The following code example shows the class and the <bpt id="p1">**</bpt>doExecute()<ept id="p1">**</ept> method implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、そのクラスと <bpt id="p1">**</bpt>doExecute()<ept id="p1">**</ept> メソッドの実装を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>The method simply retrieves the order ID and user ID from the session state and invokes the method to start this production order.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">このメソッドは単に、、セッションの状態から注文 ID とユーザー ID を取得し、この製造オーダーを開始するメソッドを呼び出すだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>doExecute() method implementation</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">doExecute() メソッドの実装</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>In case of an exception, the framework exception handling logic ensures that the process is rolled back to the previous step.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">例外が発生した場合、フレームワーク例外処理ロジックは、前の手順でプロセスがロールバックされることを保証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>The invoke to <bpt id="p1">**</bpt>addProcessCompletionMessage()<ept id="p1">**</ept> adds the “Work completed” message to the navigation parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>addProcessCompletionMessage()<ept id="p1">**</ept> の呼び出しは、ナビゲーション パラメーターに "作業完了" メッセージを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>The next step (assuming it has a user interface) will display this message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメッセージは、(ユーザー インターフェイスがあると仮定した場合) 次のステップで表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>The base classes handle this logic, and no specific code needs to be added to the process classes to achieve this behavior.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本クラスは、このロジックを処理するため、この動作を実現するために特定のコードをプロセス クラスに追加する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Building the navigation through the steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップでのナビゲーションの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>The <bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> base class instantiates the <bpt id="p2">**</bpt>ProcessGuideNavigationAgentDefault<ept id="p2">**</ept> class, which relies on a pre-defined navigation route, which is a simple map of source and destination steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> 基本クラスは、<bpt id="p2">**</bpt>ProcessGuideNavigationAgentDefault<ept id="p2">**</ept> クラスのインスタンスを作成します。これは、ソースおよび出力先のステップの簡単なマップである事前に定義されたナビゲーション工順に依存しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>For the production start scenario, because there is no conditional branching, this implementation would suffice.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産開始シナリオでは、条件分岐がないため、この実装で十分です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Therefore, you only need to override the <bpt id="p1">**</bpt>initializeNavigationRoute()<ept id="p1">**</ept> method to define the navigation route.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、必要があるのは、<bpt id="p1">**</bpt>initializeNavigationRoute()<ept id="p1">**</ept> メソッドをオーバーライドしてナビゲーション工順を定義することだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Override method code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド コードのオーバーライド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>There are processes where there will be conditional branching (based on user actions, or any other conditions).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件付き分岐が配置されるプロセスがあります (ユーザーの操作、またはその他の条件に基づく)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Such processes need to do the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようなプロセスは、次の操作を行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Implement specific navigation agents inherited from the <bpt id="p1">**</bpt>ProcessGuideNavigationAgent<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProcessGuideNavigationAgent<ept id="p1">**</ept> クラスから継承された特定のナビゲーション エージェントを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Implement the specific navigation agent factory inherited from the <bpt id="p1">**</bpt>ProcessGuideNavigationAgentAbstractFactory<ept id="p1">**</ept> class, containing logic to instantiate the correct navigation agent based on current step, session state, user action, or other logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のステップ、セッションの状態、ユーザーのアクション、または他のロジックに基づいて適切なナビゲーション エージェントのインスタンスを作成するためのロジックを含む、<bpt id="p1">**</bpt>ProcessGuideNavigationAgentAbstractFactory<ept id="p1">**</ept> クラスから継承された特定のナビゲーション エージェント ファクトリを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Optionally, override <bpt id="p1">**</bpt>navigationAgentCreationParameters()<ept id="p1">**</ept> in the controller class to pass suitable parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、コントローラー クラスで <bpt id="p1">**</bpt>navigationAgentCreationParameters()<ept id="p1">**</ept> をオーバーライドして、適切なパラメーターを渡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Override <bpt id="p1">**</bpt>navigationAgentFactory()<ept id="p1">**</ept> in the controller to instantiate the navigation agent factory created above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラーで <bpt id="p1">**</bpt>navigationAgentFactory()<ept id="p1">**</ept> をオーバーライドして、上で作成したナビゲーション エージェント ファクトリのインスタンスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Action classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>Action classes represent user actions, so this example uses the <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> action to show how the actions are created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション クラスはユーザーの操作を表すため、この例では、 <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> アクションを使用して、アクションの作成方法を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>The class must implement 2 abstract methods:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスは 2 つの抽象メソッドを実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source><bpt id="p1">**</bpt>label()<ept id="p1">**</ept>, which returns the label to be displayed in a button control tied to this action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>label()<ept id="p1">**</ept>: この操作に関連付けられているボタン コントロールに表示するためのラベルを返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source><bpt id="p1">**</bpt>doExecute()<ept id="p1">**</ept>, which performs the action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>doExecute()<ept id="p1">**</ept>: アクションを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>As mentioned earlier, the <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> button simply performs a callback to the step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既に述べたように、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> ボタンはステップでコールバックを実行するだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>However, other actions might have more complex logic here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、その他のアクションにはここにより複雑なロジックがある場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>The actions are instantiated using <bpt id="p1">**</bpt>SysExtension<ept id="p1">**</ept> framework based on the <bpt id="p2">**</bpt>ProcessGuideActionName<ept id="p2">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションは、<bpt id="p2">**</bpt>ProcessGuideActionName<ept id="p2">**</ept> 属性に基づいて <bpt id="p1">**</bpt>SysExtension<ept id="p1">**</ept> フレームワークを使用してインスタンス化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Similar to the instantiation of page builders, the step class implements the default action factory, and it is possible to override that.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ ビルダーのインスタンス化と同様、ステップ クラスは、既定のアクション ファクトリを実装し、それを上書きすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>The page builder adds a button control like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ ビルダーは、次のようにボタン コントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In doing so, it asks the step to create an action class for the passed name and ties that action to the button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うことにより、渡された名前のアクション クラスを作成するようステップに求め、そのアクションをボタンに関連付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Summary</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>To summarize everything that's been explained in this topic, here's a comprehensive summary of the code needed for the process:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックで説明したことをすべてまとめるため、プロセスに必要なコードの包括的な概要をここに示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source><bpt id="p1">**</bpt>ProdProcessGuideProductionStartController<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuideProductionStartController<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Override <bpt id="p1">**</bpt>initialStepName()<ept id="p1">**</ept> to provide the name of the first step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>initialStepName()<ept id="p1">**</ept> を上書きして、最初のステップの名前を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Override <bpt id="p1">**</bpt>initializeNavigationRoute()<ept id="p1">**</ept> to construct the navigation map.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>initializeNavigationRoute()<ept id="p1">**</ept> を上書きして、ナビゲーション マップを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Construct navigation map</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション マップの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source><bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdStep<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Override <bpt id="p1">**</bpt>isComplete()<ept id="p1">**</ept> to specify when the step is considered complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>isComplete()<ept id="p1">**</ept> を上書きし、ステップが完了と見なされるタイミングを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Override <bpt id="p1">**</bpt>pageBuilderName()<ept id="p1">**</ept> to specify the page builder to be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>pageBuilderName()<ept id="p1">**</ept> を上書きし、使用するページ ビルダーを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Specify page builder</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ ビルダーの指定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source><bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdPageBuilder<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuidePromptProductionIdPageBuilder<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Override <bpt id="p1">**</bpt>addDataControls()<ept id="p1">**</ept> to add the <bpt id="p2">**</bpt>Prod ID<ept id="p2">**</ept> textbox.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>addDataControls()<ept id="p1">**</ept> を上書きし、<bpt id="p2">**</bpt>製品 ID<ept id="p2">**</ept> テキスト ボックスを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Override <bpt id="p1">**</bpt>addActionControls()<ept id="p1">**</ept> to add the <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Cancel<ept id="p3">**</ept> buttons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>addActionControls()<ept id="p1">**</ept> をオーバーライドして <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> および <bpt id="p3">**</bpt>Cancel<ept id="p3">**</ept> ボタンを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Override addActionControls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">addActionControls のオーバーライド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source><bpt id="p1">**</bpt>ProdProcessGuideConfirmProductionOrderStep<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuideConfirmProductionOrderStep<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Override <bpt id="p1">**</bpt>pageBuilderName()<ept id="p1">**</ept> to specify the page builder to be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>pageBuilderName()<ept id="p1">**</ept> を上書きし、使用するページ ビルダーを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Override pageBuilderName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">pageBuilderName のオーバーライド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source><bpt id="p1">**</bpt>ProdProcessGuideConfirmProductionOrderPageBuilder<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuideConfirmProductionOrderPageBuilder<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Override <bpt id="p1">**</bpt>addDataControls()<ept id="p1">**</ept> to add the order, item, and quantity information labels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>addDataControls()<ept id="p1">**</ept> をオーバーライドし、注文、品目、および数量情報ラベルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Override <bpt id="p1">**</bpt>addActionControls()<ept id="p1">**</ept> to add the <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Cancel<ept id="p3">**</ept> buttons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>addActionControls()<ept id="p1">**</ept> をオーバーライドして <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> および <bpt id="p3">**</bpt>Cancel<ept id="p3">**</ept> ボタンを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Override addActionControls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">addActionControls のオーバーライド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>The <bpt id="p1">**</bpt>generateItemInfoForProdId()<ept id="p1">**</ept> method, which is used for generating the item information labels, is excluded from this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">品目情報のラベルを生成するために使用される <bpt id="p1">**</bpt>generateItemInfoForProdId()<ept id="p1">**</ept> メソッドは、このトピックから除外されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>This method queries a few tables to get item ID, description, and dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、品目 ID、説明、および分析コードを取得するいくつかのテーブルを照会します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>If you want a better understanding of <bpt id="p1">**</bpt>generateItemInfoForProdId()<ept id="p1">**</ept>, look at the source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>generateItemInfoForProdId()<ept id="p1">**</ept> についてよく理解する場合、ソース コードを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source><bpt id="p1">**</bpt>ProdProcessGuideStartProductionOrderStep<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuideStartProductionOrderStep<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Override <bpt id="p1">**</bpt>doExecute()<ept id="p1">**</ept> to perform the production start process and add the process completion message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>doExecute()<ept id="p1">**</ept> を上書きして生産プロセスの開始を実行し、プロセスの完了メッセージを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>ProdProcessGuideStartProductionOrderStep</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProdProcessGuideStartProductionOrderStep</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Note that a lot of the common patterns (regeneration of UI on error, setting process completion message, <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Cancel<ept id="p2">**</ept> behavior) have been moved to the framework – thus saving the application developer from writing boilerplate code that is both error prone, and has a risk of inconsistent behavior across processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの一般的なパターン (エラー時の UI の再生成、設定プロセスの完了メッセージ、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> および <bpt id="p2">**</bpt>キャンセル<ept id="p2">**</ept> 動作) がフレームワークに移動された点に注意してください。したがって、エラーの発生しやすい定型コードと、プロセス間で不整合な動作をする危険性を備えた定型コードの両方をアプリケーション開発者が記述しなくてよくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Where the scenario needs to deviate from the common path, though, the application developer is provided the option of overriding suitable methods – but then that is an intentional deviation that is both explicit and trackable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、共通するパスとは異なるシナリオが必要な場合、アプリケーション開発者には、適切なメソッドをオーバーライドするオプションが用意されていますが、その場合、それは明示的なかつ追跡可能な意図的な誤差です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Extending a business process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務プロセスの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>So far, this topic has highlighted how to build a new process using the <bpt id="p1">**</bpt>ProcessGuide<ept id="p1">**</ept> framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これまでのところ、このトピックでは <bpt id="p1">**</bpt>ProcessGuide<ept id="p1">**</ept> フレームワークを使用して新しいプロセスを作成する方法が強調表示されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>In this final section, you will find some examples of how this business process can be extended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この最後のセクションでは、このビジネス プロセスを拡張する方法の例をいくつか示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Add a step in a flow (using ProcessGuideNavigationAgentDefault)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フローにおけるステップの追加 (ProcessGuideNavigationAgentDefault を使用)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>Where to extend:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張場所:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Child of <bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> class for the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスの <bpt id="p1">**</bpt>ProcessGuideController<ept id="p1">**</ept> クラスの子。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>How to extend:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張方法:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Extend the <bpt id="p1">**</bpt>initializeNavigationRoute()<ept id="p1">**</ept> method in the controller class, and invoke <bpt id="p2">**</bpt>addFollowingStep()<ept id="p2">**</ept> in the <bpt id="p3">**</bpt>ProcessGuideNavigationRoute<ept id="p3">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー クラスで <bpt id="p1">**</bpt>initializeNavigationRoute()<ept id="p1">**</ept> メソッドを拡張し、<bpt id="p3">**</bpt>ProcessGuideNavigationRoute<ept id="p3">**</ept> クラスで <bpt id="p2">**</bpt>addFollowingStep()<ept id="p2">**</ept> を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Add a step in a flow (using custom navigation agent)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フローにおけるステップの追加 (カスタム ナビゲーション エージェントを使用)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Where to extend:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張場所:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Child of <bpt id="p1">**</bpt>ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent<ept id="p1">**</ept> の子。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>How to extend:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張方法:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>Create a new child class of <bpt id="p1">**</bpt>ProcessGuideNavigationAgent<ept id="p1">**</ept> that returns the desired step name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要なステップの名前を返す <bpt id="p1">**</bpt>ProcessGuideNavigationAgent<ept id="p1">**</ept> の新しい子クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Create a new class deriving from <bpt id="p1">**</bpt>ProcessGuideNavigationAgentFactory<ept id="p1">**</ept> that conditionally returns the navigation agent created above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上で作成したナビゲーション エージェントを条件付きで返す <bpt id="p1">**</bpt>ProcessGuideNavigationAgentFactory<ept id="p1">**</ept> から派生した新しいクラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Extend the <bpt id="p1">**</bpt>navigationAgentFactory()<ept id="p1">**</ept> method in the controller class to return the factory created above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー クラスで <bpt id="p1">**</bpt>navigationAgentFactory()<ept id="p1">**</ept> メソッドを拡張し、上で作成したファクトリを返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Add a new control in the UI of an existing step</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のステップの UI で新しいコントロールを追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Where to extend:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張場所:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Child of <bpt id="p1">**</bpt>ProdProcessGuidePageBuilder<ept id="p1">**</ept> for the step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップの <bpt id="p1">**</bpt>ProdProcessGuidePageBuilder<ept id="p1">**</ept> の子。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>How to extend:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張方法:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>Extend the <bpt id="p1">**</bpt>addDataControls()<ept id="p1">**</ept> method and add the additional control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>addDataControls()<ept id="p1">**</ept> メソッドを拡張し、その他のコントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Complete overhaul of the user interface in an existing step</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のステップでのユーザー インターフェイスの全体的な修正</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Where to extend:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張場所:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Child of <bpt id="p1">**</bpt>ProdProcessGuideStep<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuideStep<ept id="p1">**</ept> の子。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>How to extend:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張方法:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Create a new child class of <bpt id="p1">**</bpt>ProdProcessGuidePageBuilder<ept id="p1">**</ept> class, and implement the desired user interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuidePageBuilder<ept id="p1">**</ept> クラスの新しい子クラスを作成し、目的のユーザー インターフェイスを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Extend the <bpt id="p1">**</bpt>pageBuildeName()<ept id="p1">**</ept> method in the step class to return the <bpt id="p2">**</bpt>ProcessGuidePageBuilderNameAttribute<ept id="p2">**</ept> for the class created above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ クラスで <bpt id="p1">**</bpt>pageBuildeName()<ept id="p1">**</ept> メソッドを拡張し、上で作成したクラスの <bpt id="p2">**</bpt>ProcessGuidePageBuilderNameAttribute<ept id="p2">**</ept> を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Alter logic when a step is considered complete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップが完了と見なされたときにロジックを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Where to extend:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張場所:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>Child of <bpt id="p1">**</bpt>ProdProcessGuideStep<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdProcessGuideStep<ept id="p1">**</ept> の子。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>How to extend:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張方法:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Extend the <bpt id="p1">**</bpt>isComplete()<ept id="p1">**</ept> method to build the additional logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>isComplete()<ept id="p1">**</ept> メソッドを拡張し、追加ロジックを構築します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
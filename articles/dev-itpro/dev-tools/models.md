<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="models.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>models.f2bfa6.b96446b19fe9559b3f04fc7451ade16140e8f679.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>b96446b19fe9559b3f04fc7451ade16140e8f679</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\models.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Models and packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルとパッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes the concept of models and packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、モデルとパッケージの概念について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It also explains how to use the Development tools in Microsoft Visual Studio to create new models, how to update the parameters of existing models, and how to visualize dependencies between models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、新しいモデルを作成するために Microsoft Visual Studio の開発ツールを使用する方法、既存のモデルのパラメーターを更新する方法、およびモデル間の依存関係を表示する方法についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Models and packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルとパッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This article describes the concept of models and packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、モデルとパッケージの概念について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It also explains how to use the development tools in Microsoft Visual Studio to create new models, how to update the parameters of existing models, and how to visualize dependencies between models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、新しいモデルを作成するために Microsoft Visual Studio の開発ツールを使用する方法、既存のモデルのパラメーターを更新する方法、およびモデル間の依存関係を表示する方法についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>To work with models in the model store, you use tools in Microsoft Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル ストアのモデルを操作するには、Microsoft Visual Studio のツールを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You can create new models and change parameters for existing models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいモデルを作成、および既存のモデルのパラメータを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Conceptual overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概念に関する概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>A model is a group of elements, such as metadata and source files, that typically constitute a distributable software solution and includes customizations of an existing solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルは、通常、配布可能なソフトウェア ソリューションを構成するメタデータとソース ファイルなどの要素のグループであり、既存のソリューションのカスタマイズを含みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>A model is a design-time concept, for example a warehouse management model or a project accounting model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルは、倉庫管理モデルやプロジェクト会計モデルなどのデザイン時概念です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>A model always belongs to a package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルは、常に 1 つのパッケージに属しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>A package is a deployment and compilation unit of one or more models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージは、1 つまたは複数のモデルの配置およびコンパイル単位です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>It includes model metadata, binaries, and other associated resources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには、モデル メタデータ、バイナリ、およびその他の関連するリソースが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>One or more packages can be packaged into a deployable package, which is the vehicle used for deployment on runtime environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つ以上のパッケージは、ランタイム環境の配置に使用する車両の配置可能パッケージにパッケージすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Creating a new model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいモデルを作成しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You use the <bpt id="p1">**</bpt>Create model<ept id="p1">**</ept> wizard to create new models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデルの作成<ept id="p1">**</ept> ウィザードを使用して、新しいモデルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>You can access this wizard from <bpt id="p1">**</bpt>Model Management<ept id="p1">**</ept> on the <bpt id="p2">**</bpt>Dynamics 365<ept id="p2">**</ept>menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このウィザードには <bpt id="p2">**</bpt>Dynamics 365<ept id="p2">**</ept> メニューの <bpt id="p1">**</bpt>モデル管理<ept id="p1">**</ept> からアクセスすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>You can create two types of models:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルは 2 種類作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>A model that is deployed in its own package<ept id="p1">**</ept> – You can use this type of model to create new model elements, and extend the metadata and business logic of referenced models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>固有のパッケージに配置されているモデル<ept id="p1">**</ept> - このタイプのモデルを使用して、新しいモデル要素を作成し、参照モデルのメタデータとビジネス ロジックを拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The wizard lets you select the referenced models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このウィザードでは、参照モデルを選択できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>This type of model is compiled into its own assembly and binaries, and will simplify and reduce the cost of upgrades, deployment, and application lifecycle management in general.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタイプのモデルは、独自のアセンブリとバイナリにコンパイルされるため、一般的なアップグレード、展開、アプリケーション ライフサイクル管理のコストが削減され、簡素化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>A model that is a part of an existing package<ept id="p1">**</ept> – You can use this type of model to perform advanced customizations, such as overlayering source code and metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既存のパッケージの一部であるモデル<ept id="p1">**</ept> - このタイプのモデルを使用して、ソース コードおよびメタデータのオーバーレイなどの高度なカスタマイズを実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>When the <bpt id="p1">**</bpt>Create model<ept id="p1">**</ept> wizard is completed, if you chose to create a new project, you will be prompted to specify a name and location for it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデルの作成<ept id="p1">**</ept> ウィザードが完了したとき、新しいプロジェクトの作成を選択した場合、名前とその場所を指定するための入力を要求されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Updating model parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モード パラメーターの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>If you must change the parameters for a model, you can use the <bpt id="p1">**</bpt>Update model parameters<ept id="p1">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルのパラメーターを変更する必要がある場合は、<bpt id="p1">**</bpt>更新モデル パラメーター<ept id="p1">**</ept> ダイアログ ボックスを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>On the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> menu, point to <bpt id="p2">**</bpt>Model Management<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Update model parameters<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>モデル管理<ept id="p2">**</ept>をポイントし、<bpt id="p3">**</bpt>モデルのパラメーターの更新<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In the <bpt id="p1">**</bpt>Model name<ept id="p1">**</ept> field, select the model to update parameters for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデル名<ept id="p1">**</ept>フィールドで、パラメーターを更新するモデルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Update the parameters as you require.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じてパラメーターを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Update the dependency information for the current model, if changes are required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更が必要な場合は、現在のモデルの依存関係情報を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The summary information for the model is displayed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルの要約情報が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Click <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>完了<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The updated model parameters become effective only after you restart Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新されたモデル パラメーターは、Visual Studio を再起動した後にのみ有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Viewing package dependencies</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージの依存関係の表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>You can create a graphical representation that shows which packages and their models have dependencies on other packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どのパッケージとそのモデルに他のパッケージへの依存関係があるかを示す、グラフィック表現を作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>On the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> menu, point to <bpt id="p2">**</bpt>Model Management<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>View package dependencies<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>モデル管理<ept id="p2">**</ept>をポイントし、<bpt id="p3">**</bpt>パッケージの依存関係の表示<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>A Directed Graph Markup Language (DGML) diagram will be generated for the current packages and their models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のパッケージとそのモデルについて、有向グラフ マークアップ言語 (DGML) 図が生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>This diagram is a collection of interdependent nodes, each of which represents a package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この図は、それぞれがパッケージを表す相互依存ノードの集合です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Each node lists all the models that belong to that package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各ノードでは、パッケージに属するすべてのモデルを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Additional tools let you enhance or simplify the diagram.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加のツールは、強化または図を簡略化できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>For example, you can add comments, move nodes around, or remove nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、コメントを追加したり、ノードをあちこちに移動したり、またはノードを削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>You can also view package dependencies of a single model by following these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、次の手順で、単一モデルのパッケージ依存関係を表示することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Make sure the Application Explorer is in Model view: Right-click on the AOT node and select Model view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーがモデル ビューになっていることを確認します。AOT ノードを右クリックし、モデル ビューを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Right-click on any model and select <bpt id="p1">**</bpt>View package dependencies<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>View outgoing references.<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意のモデルを右クリックし、<bpt id="p1">**</bpt>パッケージの依存関係を表示<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>送信参照を表示<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>This will generate a graph of all packages that the selected model depends on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したモデルが依存するすべてのパッケージのグラフが生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>view dependencies</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビューの相互関係</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>directory dependencies</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ディレクトリ依存関係</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Deleting a model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>On a development or test environment, follow these steps to delete a model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発またはテスト環境では、次の手順に従ってモデルを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The following steps assume the local model store folder is C:\AOSService\PackagesLocalDirectory and your model is named MyModel1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順では、ローカル モデル ストア フォルダーが C:\AOSService\PackagesLocalDirectory であり、モデルの名前が MyModel1 であると想定しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If your model belongs to its own package (For example: An extension package with no other models in the package):</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルがそれ自身のパッケージに属している場合 (たとえば: パッケージに他のモデルがない拡張機能パッケージ):</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Stop the following services: The AOS web service and the Batch Management Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のサービスを停止: AOS Web サービスおよびバッチ管理サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Delete the package folder  C:\AOSService\PackagesLocalDirectory\MyModel1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージ フォルダー  C:\AOSService\PackagesLocalDirectory\MyModel1 を削除します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Restart the services from step 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 1 からサービスを再開</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>If Visual Studio is running, refresh your models (Visual Studio &gt; Dynamics 365 &gt; Model management &gt; Refresh models)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を実行している場合、モデルを更新します (Visual Studio &gt; Dynamics 365 &gt; モデル管理 &gt; モデルの更新)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In Visual Studio, perform a full database synchronization (Visual Studio &gt; Dynamics 365 &gt; Synchronize database...)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、完全なデータベース同期を実行します (Visual Studio &gt; Dynamics 365 &gt; データベースの同期...)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>If your model belongs to a package with multiple models (For example, MyModel1 overlays Application Suite):</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルが、複数のモデルを持つパッケージに属している場合 (MyModel1 がアプリケーション スイートにオーバーレイする場合など):</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Stop the following services: The AOS web service and the Batch Management Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のサービスを停止: AOS Web サービスおよびバッチ管理サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Delete the model folder  C:\AOSService\PackagesLocalDirectory<ph id="ph1">\&lt;</ph>PackageName&gt;\MyModel1 (In this example PackageName=ApplicationSuite)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル フォルダー  C:\AOSService\PackagesLocalDirectory<ph id="ph1">\&lt;</ph>PackageName&gt;\MyModel1 (In this example PackageName=ApplicationSuite) を削除します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Restart the services from step 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 1 からサービスを再開</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>In Visual Studio, refresh your models (Visual Studio &gt; Dynamics 365 &gt; Model management &gt; Refresh models)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、モデルを更新します (Visual Studio &gt; Dynamics 365 &gt; モデル管理 &gt; モデルの更新)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>In Visual Studio, build the package that the deleted models belonged to (Visual Studio &gt; Dynamics 365 &gt; Build models...)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、削除したモデルが属しているパッケージをビルドします (Visual Studio &gt; Dynamics 365 &gt; モデルをビルド...)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>In Visual Studio, perform a full database synchronization (Visual Studio &gt; Dynamics 365 &gt; Synchronize database...)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、完全なデータベース同期を実行します (Visual Studio &gt; Dynamics 365 &gt; データベースの同期...)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加リソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">[</bpt>Development tools overview<ept id="p1">](development-tools-overview.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>開発ツールの概要<ept id="p1">](development-tools-overview.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">[</bpt>Developer home page<ept id="p1">](developer-home-page.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>開発者ホーム ページ<ept id="p1">](developer-home-page.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">[</bpt>Distribution of models: How to export and import model files<ept id="p1">](models-export-import.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>モデルの配分: モデル ファイルをエクスポートおよびインポートする方法<ept id="p1">](models-export-import.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
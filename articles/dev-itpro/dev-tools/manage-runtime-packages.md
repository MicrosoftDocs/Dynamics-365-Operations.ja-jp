<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="manage-runtime-packages.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>manage-runtime-packages.7a73c3.fde134e037e7ffa2c385d624eeb045f4076e5f69.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>fde134e037e7ffa2c385d624eeb045f4076e5f69</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\manage-runtime-packages.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Manage third-party models and runtime packages by using source control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース コントロールを使用してサード パーティ モデルとランタイム パッケージを管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic outlines a recommended strategy for managing, distributing, and deploying third-party solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、サードパーティ ソリューションを管理、配布、展開するうえで推奨される戦略について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Manage third-party models and runtime packages by using source control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース コントロールを使用してサード パーティ モデルとランタイム パッケージを管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Customers that work with solutions from third parties might receive different solution artifacts to use in their solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サード パーティのソリューションを使用する顧客は、ソリューションで使用するさまざまなソリューション コンポーネントを受け取ることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Typically, these artifacts are distributed as code (in the form of models) or binaries (in the form of deployable packages).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、これらのアーティファクトはコード (モデルの形式) またはバイナリ (展開可能なパッケージの形式) で配布されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In some cases, third parties might provide some parts of their solution as code and other parts as a binary.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、サード パーティは、ソリューションの一部をバイナリのコードとその他のパーツとして提供する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This topic outlines a recommended strategy for managing, distributing, and deploying these third-party solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、これらのサードパーティ ソリューションを管理、配布、展開するための推奨される戦略について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Models from third parties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サード パーティからのモデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Any source code that is received from third parties must be compiled into a binary and included in a deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サード パーティから受け取ったソース コードは、バイナリにコンパイルし、配置可能パッケージに含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Models should be installed on a development virtual machine (VM) and added to source control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルは、開発仮想マシン (VM) にインストールしてソース管理に追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>From there, the build VM can pick up the source code, build it, and include it in a deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そこからは、ビルド VM はソース コードをピッキング、構築、および配置可能パッケージに含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Other developers can just synchronize the model from Microsoft Azure DevOps to their development VMs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の開発者は、Microsoft Azure DevOps のモデルをそのまま開発 VM に同期できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>They don't have to manually install it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動でインストールする必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>For information about how to install a model on a development VM, see <bpt id="p1">[</bpt>Export and import a model<ept id="p1">](models-export-import.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発 VM でモデルをインストールする方法の詳細については、<bpt id="p1">[</bpt>モデルのエクスポートとインポート<ept id="p1">](models-export-import.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>After you install the model, follow these steps to add the new model to source control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルをインストールしたら、以下の手順に従いソース管理に新しいモデルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In Microsoft Visual Studio, on the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Model Management<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Refresh Models<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio の <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>モデル管理<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>モデルの更新<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Open Application Explorer by clicking <bpt id="p1">**</bpt>View<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>をクリックして、アプリケーション エクスプ ローラーを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Right-click the <bpt id="p1">**</bpt>AOT<ept id="p1">**</ept> root node, and then click <bpt id="p2">**</bpt>Model view<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AOT<ept id="p1">**</ept>ルート ノードを右クリックし、、<bpt id="p2">**</bpt>モデル ビュー<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In the list of models, find the new model that you installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルの一覧で、インストールした新しいモデルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Make a note of the name of the package that contains the model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルを含むパッケージの名前をメモしておきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The package name appears in parentheses after the model name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージ名はモデル名の後にかっこ付きで表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>For example, in the following illustration, the <bpt id="p1">**</bpt>Tax Books<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Tax Engine Configuration<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>Tax Engine Interface<ept id="p3">**</ept> models all belong to the package that is named <bpt id="p4">**</bpt>TaxEngine<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次の図では、<bpt id="p1">**</bpt>税帳簿<ept id="p1">**</ept>、<bpt id="p2">**</bpt>税エンジン コンフィギュレーション<ept id="p2">**</ept>、および<bpt id="p3">**</bpt>税エンジン インターフェイス<ept id="p3">**</ept>モデルはすべて <bpt id="p4">**</bpt>TaxEngine<ept id="p4">**</ept> という名前のパッケージに属します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Package name for each model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各モデルのパッケージ名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Open Source Control Explorer by clicking <bpt id="p1">**</bpt>View<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Other Windows<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Source Control Explorer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>その他の Windows<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>ソース管理エクスプローラー<ept id="p3">**</ept>をクリックして、ソース管理エクスプローラーを開きます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Navigate to the metadata folder that is mapped on this development VM, such as <bpt id="p1">**</bpt>MyProject/Trunk/Main/Metadata<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MyProject/Trunk/Main/Metadata<ept id="p1">**</ept> など、この開発 VM にマップされているメタデータ フォルダーに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In the metadata folder, find the folder for the package that contains the new model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ フォルダーで、新しいモデルを含むパッケージのフォルダーを探します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Right-click the package folder, and then click <bpt id="p1">**</bpt>Add Items to Folder<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージ フォルダーを右クリックし、<bpt id="p1">**</bpt>フォルダーへの品目の追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In the <bpt id="p1">**</bpt>Add to Source Control<ept id="p1">**</ept> dialog box, select the <bpt id="p2">**</bpt>Descriptor<ept id="p2">**</ept> folder and the folder that has the name of the model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソース管理に追加<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>記述子<ept id="p2">**</ept>フォルダーとモデルの名前があるフォルダーを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Some models may also contain referenced DLLs in the <bpt id="p1">**</bpt>bin<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部のモデルには<bpt id="p1">**</bpt>在庫置場<ept id="p1">**</ept>フォルダで参照される DLL も含まれる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If these exist you'll need to also include the approriate DLL files from the <bpt id="p1">**</bpt>bin<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらが存在する場合は、<bpt id="p1">**</bpt>bin<ept id="p1">**</ept> フォルダから適切な DLL ファイルを含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Once all files have been selected, click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一度すべてのファイルが選択されると、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Review the items that will be added, and then, when you're ready, click <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加する品目を確認し、準備ができたら <bpt id="p1">**</bpt>完了<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Open the <bpt id="p1">**</bpt>Pending Changes<ept id="p1">**</ept> window from the <bpt id="p2">**</bpt>Team Explorer<ept id="p2">**</ept> pane or by clicking <bpt id="p3">**</bpt>View<ept id="p3">**</ept><ph id="ph1"> &gt; </ph><bpt id="p4">**</bpt>Other Windows<ept id="p4">**</ept><ph id="ph2"> &gt; </ph><bpt id="p5">**</bpt>Pending Changes<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保留中の変更<ept id="p1">**</ept>ウィンドウを、<bpt id="p2">**</bpt>チーム エクスプローラー<ept id="p2">**</ept>ウィンドウから、または<bpt id="p3">**</bpt>表示<ept id="p3">**</ept><ph id="ph1"> &gt; </ph><bpt id="p4">**</bpt>その他の Windows<ept id="p4">**</ept><ph id="ph2"> &gt; </ph><bpt id="p5">**</bpt>保留中の変更<ept id="p5">**</ept>をクリックして開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Review the changes, enter a check-in comment, and then click <bpt id="p1">**</bpt>Check In<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を確認してチェックイン コメントを入力し、<bpt id="p1">**</bpt>チェック イン<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Deployable packages from third parties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サード パーティから展開可能なパッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Deployable packages from third parties can be manually installed on a development VM, and the installed artifacts can then be added to source control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サード パーティの展開可能パッケージを開発用 VM に手動でインストールし、インストールされたコンポーネントをソース管理に追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Then, by synchronizing their local workspace, other developers can receive the runtime package on their VMs without having to install the deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、ローカル ワークスペースを同期させることで、他の開発者が、展開可能なパッケージをインストールしなくても、VM 上でランタイム パッケージを受け取ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The build process on the build VM will help guarantee that the runtime packages for any extensions or other dependencies are available on the build VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド VM でのビルド プロセスは、ビルド VM 上で拡張機能やその他の依存関係のランタイム パッケージを使用できるようにするのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In Platform update 6 and later, by default, these runtime packages will be included in the final deployable package that is created from the build VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 6 以降では、既定でビルド VM から作成される最終的な配置可能パッケージにこれらのランタイム パッケージが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>For more information, see the  <bpt id="p1">[</bpt>Deploying third-party code<ept id="p1">](#deploying-third-party-code)</ept> section later in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、このトピックの後半の <bpt id="p1">[</bpt>サード パーティ コードを展開する<ept id="p1">](#deploying-third-party-code)</ept> セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>For information about how to install a deployable package on a development VM, see <bpt id="p1">[</bpt>Install a deployable package<ept id="p1">](../deployment/install-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発 VM で配置可能パッケージをインストールする方法の詳細については、<bpt id="p1">[</bpt>配置可能パッケージのインストール<ept id="p1">](../deployment/install-deployable-package.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Don't install a software deployable package directly on the build VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド VM にソフトウェア配置可能パッケージを直接インストールしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Use source control as described in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックで説明するソース管理を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Only binary updates should be installed on build VMs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バイナリ更新プログラムのみビルド VM にインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>After you install the deployable package on a development VM, follow these steps to add the runtime package to source control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発 VM に配置可能パッケージをインストールした後は、以下の手順に従いソース管理にランタイム パッケージを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Open Source Control Explorer by clicking <bpt id="p1">**</bpt>View<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Other Windows<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Source Control Explorer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>その他の Windows<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>ソース管理エクスプローラー<ept id="p3">**</ept>をクリックして、ソース管理エクスプローラーを開きます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Navigate to the metadata folder that is mapped on this development VM, such as <bpt id="p1">**</bpt>MyProject/Trunk/Main/Metadata<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MyProject/Trunk/Main/Metadata<ept id="p1">**</ept> など、この開発 VM にマップされているメタデータ フォルダーに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Right-click the <bpt id="p1">**</bpt>Metadata<ept id="p1">**</ept> folder, and then click <bpt id="p2">**</bpt>Add Items to Folder<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メタデータ<ept id="p1">**</ept> フォルダーを右クリックし、<bpt id="p2">**</bpt>フォルダーへの品目の追加<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In the <bpt id="p1">**</bpt>Add to Source Control<ept id="p1">**</ept> dialog box, double-click the folder that has the package name that you want to add to source control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソース管理に追加<ept id="p1">**</ept>ダイアログ ボックスで、ソース管理に追加するパッケージ名があるフォルダーをダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Select all the folders except <bpt id="p1">**</bpt>XppMetadata<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Descriptor<ept id="p2">**</ept>, if they exist, and then click <bpt id="p3">**</bpt>Next<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>XppMetadata<ept id="p1">**</ept> および <bpt id="p2">**</bpt>Descriptor<ept id="p2">**</ept> (存在する場合) を除くすべてのフォルダーを選択し、<bpt id="p3">**</bpt>次へ<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>On the next page, on the <bpt id="p1">**</bpt>Excluded items<ept id="p1">**</ept> tab, select all files by clicking one of the files and then pressing Ctrl+A.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のページで、<bpt id="p1">**</bpt>除外した項目<ept id="p1">**</ept>タブで、ファイルのいずれかをクリックし Ctrl + A キーを押してすべてのファイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>At the bottom of the selection window, click <bpt id="p1">**</bpt>Include item(s)<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択ウィンドウの下部にある<bpt id="p1">**</bpt>項目を含める<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>When you're ready, click <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">準備ができたら、<bpt id="p1">**</bpt>完了<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Open the <bpt id="p1">**</bpt>Pending Changes<ept id="p1">**</ept> window from the <bpt id="p2">**</bpt>Team Explorer<ept id="p2">**</ept> pane or by clicking <bpt id="p3">**</bpt>View<ept id="p3">**</ept><ph id="ph1"> &gt; </ph><bpt id="p4">**</bpt>Other Windows<ept id="p4">**</ept><ph id="ph2"> &gt; </ph><bpt id="p5">**</bpt>Pending Changes<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保留中の変更<ept id="p1">**</ept>ウィンドウを、<bpt id="p2">**</bpt>チーム エクスプローラー<ept id="p2">**</ept>ウィンドウから、または<bpt id="p3">**</bpt>表示<ept id="p3">**</ept><ph id="ph1"> &gt; </ph><bpt id="p4">**</bpt>その他の Windows<ept id="p4">**</ept><ph id="ph2"> &gt; </ph><bpt id="p5">**</bpt>保留中の変更<ept id="p5">**</ept>をクリックして開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Review the changes, enter a check-in comment, and then click <bpt id="p1">**</bpt>Check In<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を確認してチェックイン コメントを入力し、<bpt id="p1">**</bpt>チェック イン<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Deploying third-party code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サード パーティのコードを展開する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Because the models and runtime packages are in source control, other developers who use other development environments can just synchronize the models and packages to their workspace by using the <bpt id="p1">**</bpt>Get latest<ept id="p1">**</ept> feature of source control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルとランタイム パッケージはソース管理のため、他の開発環境を使用する他の開発者はソース管理の<bpt id="p1">**</bpt>最新を取得<ept id="p1">**</ept>機能を使用してモデルとパッケージをワークスペースに同期させることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>As of Platform update 4, the automated build process will also pick up the runtime packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のプラットフォーム更新プログラム 4 では、自動ビルド プロセスはランタイム パッケージも取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Therefore, dependencies in packages that are built will be resolved correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、ビルドされたパッケージの依存関係は正しく解決されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>This feature is also available for Platform update 3 and Platform update 2 through a hotfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、修正プログラムを介してプラットフォーム更新プログラム 3 およびプラットフォーム更新プログラム 2 でも使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In Platform update 6, the build process will include this runtime package in the final deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 6 では、ビルド プロセスで最終的な配置可能パッケージにこのランタイム パッケージが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>This allows customers to take the deployable package from the build and have one package to deploy to their environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、お客様は、展開可能なパッケージをビルドから取り出し、1 つのパッケージを環境に展開できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>The one package includes both custom solutions and all the third party solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのパッケージにはカスタム ソリューションとすべてのサード パーティ ソリューションが含まれています。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
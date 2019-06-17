<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="copy-configuration.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>copy-configuration.3ea020.c95c4678951247ab882398b5658822a6e3b77123.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c95c4678951247ab882398b5658822a6e3b77123</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\data-entities\copy-configuration.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Copy configuration data between companies or legal entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社間また法人間の構成データをコピー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to use a configuration data project and configuration data templates to move configuration data for a company or legal entity between instances of Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、コンフィギュレーション データ プロジェクトとコンフィギュレーション データ テンプレートを使用して、Microsoft Dynamics 365 for Finance and Operations のインスタンス間で企業または法人のコンフィギュレーション データを移動する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Copy configuration data between companies or legal entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社間または法人間のコンフィギュレーション データのコピー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>There are two options for copying configuration data in Microsoft Dynamics 365 for Finance and Operations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations では、コンフィギュレーション データをコピーするために 2 つのオプションがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>To move data between instances of Finance and Operations, you must first export it from one company and then import it to another company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations のインスタンス間でデータを移動するには、最初にある会社からデータをエクスポートしてから、別の会社にインポートする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>To move data from one legal entity to another legal entity in the same instance, you can use the <bpt id="p1">**</bpt>Copy into legal entity<ept id="p1">**</ept> feature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データを同一インスタンス内のある法人から別の法人に移動するには、<bpt id="p1">**</bpt>法人にコピー<ept id="p1">**</ept>機能を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Export a configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションのエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The <bpt id="p1">**</bpt>Data management<ept id="p1">**</ept> workspace is your hub for managing configuration data projects and exporting data packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ管理<ept id="p1">**</ept> ワークスペースは、コンフィギュレーション データ プロジェクトを管理してデータ パッケージをエクスポートするためのハブとなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To build a configuration, you must define a data project and export the information that is represented by entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成をビルドするには、データ プロジェクトを定義し、エンティティによって表される情報をエクスポートする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>To create an export configuration data project, follow these step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート構成データ プロジェクトを作成するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Open the <bpt id="p1">**</bpt>Data management<ept id="p1">**</ept> workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ管理<ept id="p1">**</ept>ワークスペースを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>If you're in Standard view, select <bpt id="p1">**</bpt>Enhanced view<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準のビューを使用している場合は、<bpt id="p1">**</bpt>強化されたビュー<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Select the <bpt id="p1">**</bpt>Export<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エクスポート<ept id="p1">**</ept> タイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Select <bpt id="p1">**</bpt>New<ept id="p1">**</ept> to create an export configuration data project, and enter an ID and name for the configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept> を選択してエクスポート コンフィギュレーション データ プロジェクトを作成し、コンフィギュレーションの ID と名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Set the operation type for the data project to <bpt id="p1">**</bpt>Export<ept id="p1">**</ept>, and set the project category to <bpt id="p2">**</bpt>Configuration<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ プロジェクトの操作タイプを <bpt id="p1">**</bpt>エクスポート<ept id="p1">**</ept> に設定し、プロジェクト カテゴリを <bpt id="p2">**</bpt>コンフィギュレーション<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Add the entities that represent the information that you want to export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートする情報を表すエンティティを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can add entities by using several methods:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のいくつかのメソッドを使用してエンティティを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Add one entity<ept id="p1">**</ept> – Enter the first part of the name of the entity until it appears in the lookup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>1 つのエンティティを追加<ept id="p1">**</ept> - ルックアップに表示されるまで、エンティティの名前の最初の部分を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Add multiple entities<ept id="p1">**</ept> – Enter any part of the entity name, use the lookup for the module, enter any part of the tag name, or use the lookup for the entity category to show a list of entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>複数のエンティティを追加<ept id="p1">**</ept> - エンティティ名の一部を入力、モジュールのルックアップを使用、タグの名前の一部を入力、またはエンティティ カテゴリのルックアップを使用して、エンティティの一覧を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Press Tab to move focus away from the <bpt id="p1">**</bpt>Lookup<ept id="p1">**</ept> field and activate the filter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tab キーを押してフォーカスを <bpt id="p1">**</bpt>参照<ept id="p1">**</ept> フィールドの外に移動し、フィルターをアクティブにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In the grid, select the entities to add.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッドで、追加するエンティティを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Add a file<ept id="p1">**</ept> – Browse to a file that contains a name that matches the name of an entity and a file name extension that matches the file name extension that is in your data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ファイルを追加<ept id="p1">**</ept> - エンティティ名に一致する名前とデータ ソースにあるファイル名拡張子と一致するファイル名拡張子を含むファイルを参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Add a template<ept id="p1">**</ept> – Select from a list of templates that you've loaded in your instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テンプレートを追加する<ept id="p1">**</ept> - インスタンスでロードされたテンプレートの一覧から選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Select a target data format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット データ形式を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The system stores the last data format that you selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択した最後のデータ形式が保存されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Alternatively, if you select a file, the system automatically sets the data format to the data source that matches the file name extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、ファイルを選択する場合、ファイル名拡張子に一致するデータ ソースにシステムは自動的にデータ形式を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Composite entities require XML format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複合エンティティには、XML 形式が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>If you load a template, and the project already includes an entity that matches an entity in the template, the entity in the project will be replaced by the entity in the template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートを読み込み、そのテンプレート内のエンティティに一致するエンティティがプロジェクトにすでに含まれている場合、プロジェクト内のエンティティはテンプレート内のエンティティに置き換えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Some templates are very large, and they might take a few seconds to be loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部のテンプレートは非常に大規模であり、読み込むのに数秒かかる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Select <bpt id="p1">**</bpt>Remove entity<ept id="p1">**</ept> to remove one or more selected entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティの削除<ept id="p1">**</ept> を選択し、選択したエンティティを 1 つ以上削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>When you've completed the configuration, select <bpt id="p1">**</bpt>Export<ept id="p1">**</ept> to start the export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションが完了したら、<bpt id="p1">**</bpt>エクスポート<ept id="p1">**</ept> を選択してエクスポートを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>You can monitor the results on the <bpt id="p1">**</bpt>Execution summary<ept id="p1">**</ept> page that appears.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示される <bpt id="p1">**</bpt>実行の要約<ept id="p1">**</ept> ページで結果を監視することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Before you export a configuration, you might want to use some additional features that can help control the export process:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションをエクスポートする前に、エクスポート プロセスの管理に役立ついくつかの追加機能を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To organize the list, use the <bpt id="p1">**</bpt>Sort by<ept id="p1">**</ept> button to reorder the entities by unit, level, and sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一覧を整理するには、<bpt id="p1">**</bpt>並べ替え<ept id="p1">**</ept> ボタンを使用して、単位、レベル、シーケンスでエンティティの順序を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>To change the execution sequence of any of the entities, you can manually edit the unit, level, or sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いずれかのエンティティの実行順序を変更するには、ユニット、レベル、またはシーケンスを手動で編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Alternatively, you can use the <bpt id="p1">**</bpt>Resequence<ept id="p1">**</ept> button to update any entities that you've selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、<bpt id="p1">**</bpt>再シーケンス<ept id="p1">**</ept> ボタンを使用して選択したすべてのエンティティを更新できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The <bpt id="p1">**</bpt>Resequence<ept id="p1">**</ept> button appears only if you select more than one entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>再シーケンス<ept id="p1">**</ept> ボタンは、複数のエンティティを選択する場合にのみ表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>You can change the unit, level, and sequence individually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単位、レベル、およびシーケンスを個別に変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Alternatively, you can enable multiple changes and make them all at the same time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、複数の変更を有効にして同時に変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If you want the unit, level, or sequence to remain unchanged when you change multiple parts of the sequence, set the increment to <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シーケンスの複数の部分を変更したときにユニット、レベル、シーケンスを変更しない場合は、増分値を <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero) に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>To add filters to the entity, use the <bpt id="p1">**</bpt>Filter<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティにフィルターを追加するには、<bpt id="p1">**</bpt>フィルター<ept id="p1">**</ept> ボタンを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>If you add a filter, the <bpt id="p1">**</bpt>Filter<ept id="p1">**</ept> button changes to an <bpt id="p2">**</bpt>Edit<ept id="p2">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィルターを追加する場合、<bpt id="p1">**</bpt>フィルター<ept id="p1">**</ept> ボタンが<bpt id="p2">**</bpt>編集<ept id="p2">**</ept>ボタンに変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The data will be filtered before it's exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データはエクスポートする前にフィルタ処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If you've added a template, and the template includes filters, those filters will be added to your project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートを追加して、そのテンプレートにフィルターが含まれる場合、それらのフィルターはプロジェクトに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>However, you can modify or remove them as you require.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、必要に応じて変更または削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If you must change the entity mappings, use the <bpt id="p1">**</bpt>View map<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ マッピングを変更する必要がある場合、<bpt id="p1">**</bpt>マップの表示<ept id="p1">**</ept>ボタンを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If you've added a template, and the template includes mapping changes, those changes will be applied to your project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートを追加して、そのテンプレートにマッピングの変更が含まれる場合、それらの変更はプロジェクトに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>However, you can modify them as you require.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、必要に応じて変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>To temporarily prevent the entity from being used when you export a data project, use the check box in the <bpt id="p1">**</bpt>Disable<ept id="p1">**</ept> column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ プロジェクトをエクスポートするときにエンティティが一時的に使用されないようにするには、<bpt id="p1">**</bpt>無効化<ept id="p1">**</ept> 列のチェックボックスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>To open the contents of the grid in a Microsoft Excel workbook, use the <bpt id="p1">**</bpt>Open in Excel<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Excel ブックでグリッドの内容を開くには、<bpt id="p1">**</bpt>Excel で開く<ept id="p1">**</ept>ボタンを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Modify the entities as you require, and then use the <bpt id="p1">**</bpt>Publish<ept id="p1">**</ept> button to upload the changes back into Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じてエンティティを変更してから、<bpt id="p1">**</bpt>公開<ept id="p1">**</ept>ボタンを使用して Finance and Operations に変更をアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>When the export is completed, complete the following tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートが完了したら、次の作業を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Use the <bpt id="p1">**</bpt>Download<ept id="p1">**</ept> button on the <bpt id="p2">**</bpt>Export<ept id="p2">**</ept> page to download the configuration settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>エクスポート<ept id="p2">**</ept> ページの <bpt id="p1">**</bpt>ダウンロード<ept id="p1">**</ept> ボタンを使用して、構成をダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Use the <bpt id="p1">**</bpt>Download package<ept id="p1">**</ept> button in the <bpt id="p2">**</bpt>Data management<ept id="p2">**</ept> workspace or on the <bpt id="p3">**</bpt>Execution summary<ept id="p3">**</ept> page to download the configuration settings and the data that was exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>データ管理<ept id="p2">**</ept> ワークスペースまたは <bpt id="p3">**</bpt>実行の概要<ept id="p3">**</ept>ページの <bpt id="p1">**</bpt>パッケージのダウンロード<ept id="p1">**</ept> ボタンを使用して、エクスポートされた構成設定とデータをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Setup considerations for some entities that are used to export configurations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションのエクスポートに使用される一部のエンティティの設定に関する考慮事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Currently, several entities require additional steps when you build configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、複数のエンティティは、ビルド構成を行う際に追加の手順が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Follow these recommendations as you build your configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションを構築する際は、これらの推奨事項に従ってください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>This list will be updated as the Copy configuration feature is improved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このリストは、コピー構成機能が改善されるにつれて更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Using special-purpose entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">専用のエンティティの使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The following entities require special handling when they are used in configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のエンティティは、設定で使用されるときに特別な処理が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Area</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">面</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Action</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>System setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Global address book</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グローバル アドレス帳</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The entity no longer exports the records that are created automatically when a company is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティは、会社の作成時に自動的に作成されるレコードをエクスポートしなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The import no longer accepts those records as well, starting in the platform 9 release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートでは、プラットフォーム 9 リリース以降、これらのレコードも受け入れなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>GL Shared</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GL 共有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Account structures active group</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">勘定構造の有効なグループ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>This composite entity will export and import only the active account structures.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この複合エンティティは、アクティブな勘定構造のみをエクスポートおよびインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>If you use any other account structure entities, the status of the active account structures will be changed to <bpt id="p1">**</bpt>Draft<ept id="p1">**</ept>, and you must activate them before they can be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の勘定構造エンティティを使用している場合、有効な勘定構造のステータスは<bpt id="p1">**</bpt>ドラフト<ept id="p1">**</ept>に変更されるため、使用可能になる前に有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Advanced rule structures active group</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細ルール構造の有効なグループ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This composite entity is used in combination with the account structures active group entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この複合エンティティは、勘定構造アクティブ グループ エンティティと組み合わせて使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>It will export and import only the active advanced rule structures.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な詳細ルール構造のみをエクスポートおよびインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>If you use any other advanced rule structure entities, the status of the advanced rule structures will be changed to <bpt id="p1">**</bpt>Draft<ept id="p1">**</ept>, and you must activate them before they can be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の詳細なルール構造エンティティを使用している場合、詳細なルール構造のステータスは<bpt id="p1">**</bpt>ドラフト<ept id="p1">**</ept>に変更されるため、使用可能になる前に有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Financial dimension values</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コード値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>All dimension values will be exported, even values that are based on system-defined entities such as projects or customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての分析コード値がエクスポートされるには、基準となるシステム定義のエンティティはプロジェクトまたは顧客のような値になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Remove the system-defined values before you import them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートする前に、システム定義の値を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>If you leave the system-defined values in the package, they won't be imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム定義の値をパッケージに残したままにする場合は、インポートしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>However, they will be filled as you import the data that backs the system-defined dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、システム定義の分析コードをバックアップするデータをインポートする際、それらが満たされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Workflow version</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー バージョン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Change the owner for every record in the package data to <bpt id="p1">**</bpt>Admin<ept id="p1">**</ept>, unless the users in the workflow are already imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー内のユーザーが既にインポートされている場合を除き、パッケージ データのすべてのレコードの所有者を<bpt id="p1">**</bpt>管理者<ept id="p1">**</ept>に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Workflow expression</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー式</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Some workflow expressions might be too long for an Excel cell.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー式には、Excel セルには長すぎるものがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Use XML instead of Excel as the export format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート形式として、Excel ではなく XML を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Tax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税申告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Sales tax parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">消費税パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>The default value for the marginal base calculations method is <bpt id="p1">**</bpt>Total<ept id="p1">**</ept> for sales tax parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準金額計算方法の既定値は、売上税パラメーターの <bpt id="p1">**</bpt>合計<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>The Ledger Parameters entity doesn't set that value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">総勘定元帳パラメーター エンティティは、その値を設定しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>However, the marginal base that some tax codes use, <bpt id="p1">**</bpt>Line<ept id="p1">**</ept>, will fail validation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、一部の税コードが使用する基準金額 <bpt id="p1">**</bpt>ライン<ept id="p1">**</ept>は、検証に失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>A new entity that is named the Sales tax parameters preset entity was created so that you can import the marginal base calculation method first.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">消費税パラメーターの事前設定エンティティという名前の新しいエンティティが作成されるため、基準金額の計算方法を最初にインポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>You can then import tax codes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税コードをインポートすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Accounts receivable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">売掛金</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Customers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>The Customers entity was designed to be used for OData scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客エンティティは、OData シナリオに使用するように設計されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>For configurations, use the Customer definitions entity and the Customer details entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションでは、顧客の定義エンティティおよび顧客の詳細エンティティを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>The Customer definitions entities let you import the basic information about a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客定義エンティティを使用すると、顧客に関する基本的な情報をインポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>In this way, you enable entities that require that a customer have that information earlier in the import process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、インポート処理で顧客がより早く情報を入手する必要があるエンティティを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>The Customer details entity contains additional information about a customer that you can add after parameters and reference data have been set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客詳細エンティティには、パラメーターと参照データが設定された後に追加できる顧客に関する追加情報が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Warehouse locations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">倉庫の場所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Some warehouse locations require a location profile ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの倉庫の場所には、場所のプロファイル ID が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Location profile IDs require a location format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場所プロファイル ID には、場所の形式が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Currently, the location format information must be manually added before the warehouse location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、場所の形式情報は倉庫の場所の前に手動で入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>The entities for the location format and location profile were added in version 7.2.3, (App update 3 of the July 2017 release).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場所の形式と場所プロファイルのエンティティが、バージョン 7.2.3 で追加されました (2017 年 7 月のリリースの App Update 3)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Product information management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品情報管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Products</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The Products and Released Products entities should be used for configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品とリリース済み製品エンティティは、構成に使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>The Product master and Released product master entities should be used for OData scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData シナリオでは、製品マスターおよびリリース済み製品マスター エンティティを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Product document attachments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品ドキュメントの添付ファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>For attachments to product documents released product documents, you must never skip staging, because additional steps are performed in the staging environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品ドキュメントのリリース済製品のドキュメントの添付については、追加の手順がステージング環境で実行されるため、ステージングを決してスキップしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>You must use a data package for export and import, because the export file must be accompanied by a resources folder that contains the attachments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート ファイルには添付ファイルの入ったリソース フォルダが必要なため、エクスポートとインポート用にデータ パッケージを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The entities support images, documents, notes, and links.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティは、画像、ドキュメント、メモ、およびリンクをサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>When you export, you will see an image file that has a name that resembles a globally unique identifier (GUID).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートするとき、グローバル一意識別子 (GUID) のような名前を持つ画像ファイルが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This file is a valid data package that is required in order to complete the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルは、インポートを完了するために必要となる有効なデータ パッケージです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Product attribute values</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品属性値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Product attribute values are assigned only when a user opens the <bpt id="p1">**</bpt>Attribute values<ept id="p1">**</ept> page from the <bpt id="p2">**</bpt>Products details<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品属性値は、ユーザーが <bpt id="p2">**</bpt>製品詳細<ept id="p2">**</ept> ページから <bpt id="p1">**</bpt>属性値<ept id="p1">**</ept> ページを開いたときにのみ割り当てられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Currently, you can't import the values unless this step was performed in the golden build.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、ゴールデン ビルドでこのステップが実行されていない限り、値をインポートすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Procurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">調達</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Vendor catalog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入先カタログ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>See the "Vendor catalogs import" section of <bpt id="p1">[</bpt>Vendor catalogs in Dynamics AX<ept id="p1">](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/)</ept> on the Supply Chain Management blog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Supply Chain Management ブログで、<bpt id="p1">[</bpt>Dynamics AX の仕入先カタログ<ept id="p1">](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/)</ept>の「仕入先のカタログをインポート」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Shared category</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有カテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The Shared category entity now exposes the following fields: <bpt id="p1">**</bpt>CATEGORYID<ept id="p1">**</ept>, <bpt id="p2">**</bpt>CATEGORYNAME<ept id="p2">**</ept>, <bpt id="p3">**</bpt>EXPENSETYPE<ept id="p3">**</ept>, <bpt id="p4">**</bpt>USINEXPENSE<ept id="p4">**</ept>, <bpt id="p5">**</bpt>USINPRODUCTION<ept id="p5">**</ept>, and <bpt id="p6">**</bpt>USEINPROJECT<ept id="p6">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有カテゴリ エンティティは、フィールド <bpt id="p1">**</bpt>CATEGORYID<ept id="p1">**</ept>、<bpt id="p2">**</bpt>CATEGORYNAME<ept id="p2">**</ept>、<bpt id="p3">**</bpt>EXPENSETYPE<ept id="p3">**</ept>、<bpt id="p4">**</bpt>USINEXPENSE<ept id="p4">**</ept>、<bpt id="p5">**</bpt>USINPRODUCTION<ept id="p5">**</ept>、<bpt id="p6">**</bpt>USEINPROJECT<ept id="p6">**</ept> を公開するようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>If you change the value of the <bpt id="p1">**</bpt>USEINEXPENSE<ept id="p1">**</ept> field to <bpt id="p2">**</bpt>yes<ept id="p2">**</ept>, the <bpt id="p3">**</bpt>EXPENSETYPE<ept id="p3">**</ept> should be set to one of the valid values that are available in the <bpt id="p4">**</bpt>Expense type<ept id="p4">**</ept> field on the <bpt id="p5">**</bpt>Shared category<ept id="p5">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>USEINEXPENSE<ept id="p1">**</ept> フィールドの値を<bpt id="p2">**</bpt>はい<ept id="p2">**</ept>に変更すると、<bpt id="p3">**</bpt>EXPENSETYPE<ept id="p3">**</ept> を<bpt id="p5">**</bpt>共有カテゴリ<ept id="p5">**</ept> ページの<bpt id="p4">**</bpt>経費タイプ<ept id="p4">**</ept> フィールドで使用できる有効な値のいずれかに設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Remove the mapping and apply filters for specific entity fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マッピングを削除して、特定のエンティティ フィールドにフィルターを適用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>In a golden build, customer-specific fields might not be set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ゴールデン ビルドでは、顧客固有のフィールドを設定できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>To help guarantee that the import works, you should unmap those fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートが正しく動作するようにするためには、これらのフィールドのマッピングを解除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>For example, workers are stored in many tables, but they might not be set up in a golden build.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、作業者が多数のテーブルに格納されていても、ゴールデン ビルドで設定されていない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Filters might also be required for some fields in an entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィルターが、エンティティ内の一部のフィールドに必要な場合もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The following entities might have to be unmapped or filtered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のエンティティは、マップされていないかフィルター処理されている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Area</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">面</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Action</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>System setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Operating unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業単位</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Unmap Manager personnel number unless workers have been imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業者がインポートされていない場合は、マネージャーの従業員番号のマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>User information</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー情報</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Apply a filter where <bpt id="p1">**</bpt>ID<ept id="p1">**</ept> isn't equal to <bpt id="p2">**</bpt>Admin<ept id="p2">**</ept>. Unmap Person name, and use the User to person relationship entity to map system users to directory users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ID<ept id="p1">**</ept> が<bpt id="p2">**</bpt>管理者<ept id="p2">**</ept>と等しくないフィルターを適用します。氏名をマップ解除し、ユーザーと個人の関係エンティティを使用してシステム ユーザをディレクトリ ユーザーにマップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Accounts payable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">買掛金</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Vendors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入先</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Unmap Purchase site (DefaultPurchaseSite) and Warehouse (DefaultProcurementWarehouseID) unless they are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定されていない場合、購買サイト (DefaultPurchaseSite) と倉庫 (DefaultProcurementWarehouseID) のマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Unmap the vendor bank account ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入先の銀行口座 ID をマップ解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>The Vendor bank account entity will set up the link to the bank account when it's imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入先の銀行口座エンティティをインポートすると、銀行口座へのリンクが設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Accounts receivable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">売掛金</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Customer details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客の詳細</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Unmap Employee responsible number unless workers have been imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業者がインポートされていない場合は、従業員の担当番号のマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Unmap Collections contact person (CollectionsContactPersonID) unless workers and their contact information have been imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業者とその連絡先情報がインポートされていない場合は、コレクションの連絡担当者 (CollectionsContactPersonID) のマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Unmap the site (SiteID) and warehouse (WarehouseID) unless they have already been imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既にインポートされている場合を除き、サイト (SiteID) と倉庫 (WarehouseID) のマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Warehouse current postal address</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">倉庫の現在の住所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Unmap Picking store area and Input store area unless Retail information has been imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売情報がインポートされていない場合、店舗エリアのピッキングをマップ解除し、店舗エリアを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Product information management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品情報管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Products</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Unmap NMFCCode and STCCCode unless you are adding the transportation management template to your data project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ管理プロジェクトに輸送管理テンプレートを追加しない場合は、NMFCCode と STCCCode のマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Released products</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リリースされた製品</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Unmap the project category, default product color, default configuration, default product size, and default product style.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト カテゴリ、製品の既定の色、既定の構成、製品の既定のサイズ、および製品の既定のスタイルのマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>This entity is self-referencing and hasn't yet been updated to load these fields in a single pass.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティは自己参照型であり、これらのフィールドを単一のパスでロードするようにはまだ更新されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Period template</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">期間テンプレート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The Period template entity is a shared entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">期間テンプレート エンティティは、共有エンティティです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Although it can be filtered by legal entity, the Period template lines entity doesn't have a <bpt id="p1">**</bpt>Legal entity<ept id="p1">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人によってフィルタリングすることはできますが、期間テンプレート行のエンティティには<bpt id="p1">**</bpt>法人<ept id="p1">**</ept>フィールドはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>To import a single legal entity, you can filter the period template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単一の法人をインポートするには、期間テンプレートをフィルター処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>However, you must currently remove the period template lines that aren't related to that legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、現在、その法人に関連していない期間テンプレートの行を削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Item coverage group</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">品目補充グループ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Unmap Period template ID unless it has already been added manually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">期間テンプレート ID がすでに手動で追加されている場合を除き、そのマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Procurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">調達</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Vendors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入先</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Unmap Purchase site (DefaultPurchaseSite) and Warehouse (DefaultProcurementWarehouseID) unless they are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定されていない場合、購買サイト (DefaultPurchaseSite) と倉庫 (DefaultProcurementWarehouseID) のマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Unmap the vendor bank account ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入先の銀行口座 ID をマップ解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>The Vendor bank account entity will set up the link to the bank account when it's imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入先の銀行口座エンティティをインポートすると、銀行口座へのリンクが設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Sales and marketing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売とマーケティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Leads</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">潜在顧客</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Unmap LeadOpeningPersonnelNumber, LeadClosingPersonnelNumber, and LeadResponsiblePersonnelNumber unless workers have been imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業者がインポートされていない場合は、LeadOpeningPersonnelNumber、LeadClosingPersonnelNumber、および LeadResponsiblePersonnelNumber のマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Sales type document entry policies</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売タイプ ドキュメントのエントリ ポリシー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Unmap IsAtpGenrallyIncludingPlannedOrders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IsAtpGenrallyIncludingPlannedOrders のマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>The default for Master planning was changed to be Yes for Disable all planning processes when a legal entity is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人の作成時に、すべての計画プロセスを無効にするために、マスター プランの既定が「はい」に変更されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Project management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Projects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Unmap WorkerArchitectPersonelNumber, WorkerRespFinancialPersonelNumber, WorkerResponsiblePersonnelNumber, and WorkerRespSalesPersonelNumber unless workers have been imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業者がインポートされていない場合は、WorkerArchitectPersonelNumber、WorkerRespFinancialPersonelNumber、WorkerResponsiblePersonnelNumber、および WorkerRespSalesPersonelNumber のマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Retail</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>POS visual profiles</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 視覚プロファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Unmap Pallet because no entity is available at this time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現時点ではエンティティが存在しないため、パレットのマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The POS visual profiles entity was added to the Retail template in version 7.2.3, (App update 3 of the July 2017 release).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS ビジュアル プロファイル エンティティは、バージョン 7.2.3 の Retail テンプレート (2017 年 7 月リリースのアプリケーション更新プログラム 3) に追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Retail channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャネル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Unmap Channel profile name (ChannelProfileName) and Live database connection profile name (LiveDatabaseConnectionProfileName) because no entity is available at this time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この時点でエンティティが利用できないため、チャネル プロファイル名 (ChannelProfileName) とライブ データベース接続プロファイル名 (LiveDatabaseConnectionProfileName) のマップを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>The Retail channel entity was added to the Retail template in version 7.2.3, (App update 3 of the July 2017 release).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail チャネル エンティティは、バージョン 7.2.3 の Retail テンプレート (2017 年 7 月リリースのアプリケーション更新プログラム 3) に追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Golden builds that have multiple legal entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の法人を持つゴールデン ビルド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>The templates can be used to export data from any company in your golden build.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートを使用して、ゴールデン ビルド内の任意の会社のデータをエクスポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>When you export both shared data and company data, the templates first export the shared data for all legal entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有データと会社データの両方をエクスポートするときは、テンプレートはすべての法人の共有データを最初にエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>They then export the data for the legal entity that you're currently using.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、現在使用している法人のデータをエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>You can then switch companies and export the company data for additional legal entities by using projects that don't include the shared entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有エンティティを含まないプロジェクトを使用して、会社を切り替え、追加の法人のために会社データをエクスポートすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>If you're exporting from a golden build that contains multiple legal entities, but you want to import the data from only one of those legal entities, you must apply a filter on the legal entity fields, so that only the data that you require for that legal entity is exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の法人組織を含むゴールデン ビルドからエクスポートする場合、それらの法人組織の中から 1 つのみのデータをインポートする場合は、法人組織フィールドにフィルターを適用すると、その法人から必要なデータのみがエクスポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>This filter must remove all data for all legal entities except the legal entity that you want.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィルターは、必要な法人を除くすべての法人のデータを削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>In some cases, you must complete additional steps to clean up the exported data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、エクスポートされたデータをクリーンアップする追加の手順を完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Most of the changes that are listed in the following table occur in the <bpt id="p1">**</bpt>System setup<ept id="p1">**</ept> and <bpt id="p2">**</bpt>General ledger<ept id="p2">**</ept> areas.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表に記載されている変更のほとんどが、<bpt id="p1">**</bpt>システム設定<ept id="p1">**</ept>および<bpt id="p2">**</bpt>総勘定元帳<ept id="p2">**</ept>の領域で発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>If you export a golden build that uses a single legal entity, you should not require these filters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つの法人を使用するゴールド ビルドをエクスポートする場合は、これらのフィルターを必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>The following entities require filters or special handling when you export the data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のエンティティは、データをエクスポートするときにフィルター処理または特別な処理が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Area</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">面</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Action</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>System setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Legal entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Apply a filter to Company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Number sequence code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">番号順序コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>The number sequence codes can be shared, or they can be specific to a legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">番号順序コードは共有することも、法人に固有のものとすることもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>To import all number sequences, you must have the legal entities setup for the number sequences that are stored for a specific legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての番号シーケンスをインポートするには、特定の法人向けに保存されている番号シーケンスに法人を設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>If you want only shared number sequences, apply a filter to remove the number sequences that are specific to a legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有番号シーケンスだけが必要な場合は、フィルターを適用し、法人固有の番号シーケンスを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>If you want the number sequences only for a specific legal entity, apply a filter to Company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の法人の番号列のみを必要とする場合は、Company にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Number sequences can also have scope.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">番号順序にはスコープも設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>You must delete number sequences when the following conditions are met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の条件が満たされた場合に、番号順序を削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>The <bpt id="p1">**</bpt>SCOPETYPE<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>DataArea<ept id="p2">**</ept>, and the <bpt id="p3">**</bpt>SCOPEVALUE<ept id="p3">**</ept> value either isn't equal to the legal entity or is blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SCOPETYPE<ept id="p1">**</ept> 値は <bpt id="p2">**</bpt>DataArea<ept id="p2">**</ept> であり、<bpt id="p3">**</bpt>SCOPEVALUE<ept id="p3">**</ept> 値は法人と等しくないか空白になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>The <bpt id="p1">**</bpt>SCOPETYPE<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>LegalEntity<ept id="p2">**</ept>, and the <bpt id="p3">**</bpt>SCOPEVALUE<ept id="p3">**</ept> value isn't equal to the legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SCOPETYPE<ept id="p1">**</ept> 値は <bpt id="p2">**</bpt>LegalEntity<ept id="p2">**</ept> であり、<bpt id="p3">**</bpt>SCOPEVALUE<ept id="p3">**</ept> 値は法人と等しくありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>The <bpt id="p1">**</bpt>SCOPETYPE<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>DataAreaFiscalCalendar<ept id="p2">**</ept>, and the <bpt id="p3">**</bpt>SCOPEVALUE<ept id="p3">**</ept> value isn't equal to the legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SCOPETYPE<ept id="p1">**</ept> 値は <bpt id="p2">**</bpt>DataAreaFiscalCalendar<ept id="p2">**</ept> であり、<bpt id="p3">**</bpt>SCOPEVALUE<ept id="p3">**</ept> 値は法人と等しくありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Number sequence references</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">番号順序の参照</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Number sequence references can also have scope.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">番号順序の参照にはスコープも設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>You must delete the number sequence references when the following conditions are met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の条件が満たされた場合に、番号シーケンスの参照を削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The <bpt id="p1">**</bpt>SCOPETYPE<ept id="p1">**</ept> value is equal to <bpt id="p2">**</bpt>DataArea<ept id="p2">**</ept>, <bpt id="p3">**</bpt>DataAreaFiscalCalendar<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>LegalEntity<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SCOPETYPE<ept id="p1">**</ept> .値は <bpt id="p2">**</bpt>DataArea<ept id="p2">**</ept>、<bpt id="p3">**</bpt>DataAreaFiscalCalendar<ept id="p3">**</ept>、または <bpt id="p4">**</bpt>LegalEntity<ept id="p4">**</ept> と等しくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>The <bpt id="p1">**</bpt>SCOPEVALUE<ept id="p1">**</ept> value either isn't equal to the legal entity that you want in the data or is blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SCOPETYPE<ept id="p1">**</ept> 値はデータに含める法人と等しくないか、空白になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Organization hierarchies</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">組織階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>There is no legal entity filter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人フィルターはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>Manually remove any references to the other legal entities that you aren't importing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートしていない他の法人への参照を手動で削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>For example, if you've set up centralized payments, but you're loading only one legal entity, you must not import the Centralized payments hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、集中支払を設定しても、1 つの法人のみを読み込んでいる場合、集中支払階層をインポートしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Global address book</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グローバル アドレス帳</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Multiple entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数のエンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>The global address book contains data for all legal entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グローバル アドレス帳には、すべての法人のデータが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>All legal entities will be created when you import the data, unless you remove the data for the legal entities that you don't want to load.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データをインポートする場合、使用しない法人エンティティのデータを削除しない限りすべての法人エンティティが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>To help guarantee that other legal entities aren't created, delete all records for those other legal entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の法人が作成されないようにするには、そうした他の法人のすべてのレコードを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Alternatively, apply a filter to the Legal entity data area (<ph id="ph1">&amp;lt;</ph><ph id="ph2">&amp;gt;</ph> blank).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、法人エンティティ データ エリアに (<ph id="ph1">&amp;lt;</ph><ph id="ph2">&amp;gt;</ph> 空白) フィルターの適用をします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>You must also remove global address book records that are used in the other legal entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の法人で使用されるグローバル アドレス帳レコードを削除することも必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Party postal addresses</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係者の配送先</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Address records for legal entities other than the legal entity that you're importing must be manually deleted before import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートする法人以外の法人の住所レコードは、インポートする前に手動で削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Party contacts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係者の連絡先</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Contact records for legal entities other than the legal entity that you're importing must be manually deleted before import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートする法人以外の法人の連絡先レコードは、インポートする前に手動で削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Apply a filter on DataAreaID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataAreaID にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Many of the workflow entities can't be filtered for legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー エンティティの多くは、法人のフィルター処理ができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Therefore, import failures might occur if you don't remove the data in all workflow entities that are related to legal entities that you don't want.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、望ましくない法人組織に関連するすべてのワークフロー エンティティのデータを削除しないと、インポート エラーが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>We recommend that you manually set up workflows for this scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオのワークフローを手動で設定することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>General ledger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般会計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Ledger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ledger</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Apply a filter to Company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Ledger fiscal calendar year</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳の会計暦年</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>Apply a filter to Ledger name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳名にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Ledger fiscal calendar period</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳の会計カレンダー期間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Apply a filter to Ledger name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳名にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Main account legal entity overrides</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主勘定法人の上書き</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Apply a filter to Company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Financial dimension value legal entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コード値法人</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Financial dimension values</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コード値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>However, you can't filter out system-defined dimension values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、システム定義の分析コード値をフィルター処理することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Therefore, you must delete them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、それらを削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Those system-defined dimension values will be restored when you import data for the tables that back the system-defined dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのシステム定義の値は、システム定義の分析コードを戻すテーブルのデータをインポートするときにリストアされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>Journal names</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕訳帳名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Apply a filter to Voucher series company ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">伝票シリーズの会社 ID にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Ledger allocation basis source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳配賦基準の入力元</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Ledger allocation rule destination</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳配賦ルールの出力先</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Apply a filter to Company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Accounts receivable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">売掛金</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Customer write-off reason code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客損金処理理由コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>Apply a filter to Company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Budget</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Budget control configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算管理コンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Budget control configuration activation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算管理コンフィギュレーションの有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>Budget control cycle model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算管理サイクル モデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Budget control dimension attribute</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算管理分析コード属性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Budget control documents and journals</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算管理のドキュメントと仕訳帳</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Budget control group</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算管理グループ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Budget control group criteria</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算管理グループの基準</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>Budget control message level</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算管理メッセージ レベル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Budget control over budget permissions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算超過の許可の予算管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Budget control rule</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算管理ルール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Budget control rule criteria</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算管理ルールの基準</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Budget cost elements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算原価要素</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Apply a filter to Cost element data area ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">原価要素データ領域 ID にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Budget dimensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算分析コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Budget plan allocation schedule</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算計画の配賦スケジュール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>Apply a filter to Ledger.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Budget plan process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算計画プロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Apply a filter to Ledger.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Budget plan stage rule</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算計画ステージ ルール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>If you applied a filter to Budget plan process, errors might occur when you import stage rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算計画プロセスにフィルターを適用する場合は、ステージのルールをインポートするときにエラーが発生する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>Because the entity doesn't currently contain a ledger name that can be filtered, it will contain all companies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティには現在フィルター処理できる元帳名が含まれていないため、すべての会社が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>Budget plan priority constraint</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算計画優先順位の制約</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>You will experience the same issue that is described for the Budget plan stage rule entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算計画ステージ ルール エンティティについて記載されている同じ問題が生じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Budget plan process administration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算計画プロセス管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>You will experience the same issue that is described for the Budget plan stage rule entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算計画ステージ ルール エンティティについて記載されている同じ問題が生じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Budget transfer rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算振替ルール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>Inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>Warehouse current postal address</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">倉庫の現在の住所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>Apply a filter to Company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>Site current postal address</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイトの現在の住所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Apply a filter to Company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Tracking number groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追跡番号グループ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>The entity automatically filters the Number sequence scope data area by the legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティは、法人によって番号順序スコープ データ領域を自動的にフィルター処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>Therefore, you don't require a filter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、フィルターは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>However, if you must change the legal entity, the legal entity is stored in the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、法人を変更する必要がある場合、法人はテーブルに格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>Retail</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>POS registers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS レジスター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>Apply a filter to Legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にフィルターを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>This entity was added to the Retail template version 7.2.3, (App update 3 of the July 2017 release).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティは、Retail テンプレート バージョン 7.2.3 (2017 年のアプリケーション更新プログラム 3) に追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Retail store address book</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売店舗アドレス帳</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>There is no legal entity filter for this entity so the export will include records for all legal entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティには法人フィルターが存在しないため、エクスポートにはすべての法人のレコードが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>This entity was added to the Retail template inversion 7.2.3, (App update 3 of the July 2017 release).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティは、バージョン 7.2.3 の Retail テンプレート (2017 年 7 月リリースのアプリケーション更新プログラム 3) に追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>Retail locator group member</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売ロケーター グループのメンバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>There is no legal entity filter for this entity so the export will include records for all legal entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティには法人フィルターが存在しないため、エクスポートにはすべての法人のレコードが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>This entity was added to the Retail template in version 7.2.3, (App update 3 of the July 2017 release).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティは、バージョン 7.2.3 の Retail テンプレート (2017 年 7 月リリースのアプリケーション更新プログラム 3) に追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>Retail locator group owner</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売ロケーター グループの所有者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>There is no legal entity filter for this entity so the export will include records for all legal entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティには法人フィルターが存在しないため、エクスポートにはすべての法人のレコードが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>This entity was added to the Retail template in version 7.2.3, (App update 3 of the July 2017 release).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティは、バージョン 7.2.3 の Retail テンプレート (2017 年 7 月リリースのアプリケーション更新プログラム 3) に追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>Retail devices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売り用デバイス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>There is no legal entity filter for this entity so the export will include records for all legal entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティには法人フィルターが存在しないため、エクスポートにはすべての法人のレコードが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>This entity was added to the Retail template in version 7.2.3, (App update 3 of the July 2017 release).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティは、バージョン 7.2.3 の Retail テンプレート (2017 年 7 月リリースのアプリケーション更新プログラム 3) に追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>Changing the legal entity value before import</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート前に法人の値を変更する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>If you want to change the legal entity ID to another value, the value of all fields that resemble the fields that were listed earlier must be changed to the value of the new legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人 ID を別の値に変更する場合は、以前記載したフィールドに似ているすべてのフィールドの値を、新しい法人組織の値に変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>For example, for Legal entities, change Company from the exported value to a new value in the exported file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、法人に対して、会社をエクスポートされた値からエクスポート済ファイルの新しい値に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>The legal entity ID is stored in many places.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人 ID は多くの場所に格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>Therefore, it can be difficult to make this change, and you might cause errors if you try.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、この変更を行うことは難しく、試してみるとエラーが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>When you set up a data project to copy into a legal entity, a legal entity filter for the source legal entity is automatically added to any entity field that is determined to be a legal entity field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にコピーするデータ プロジェクトを設定すると、ソース法人の法人フィルターが、法人フィールドであると決定されているエンティティ フィールドに自動的に追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>Selecting a single legal entity for export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートする 1 つの法人を選択</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>To export a single legal entity, you can create a Copy into legal entity data project and specify the legal entity to copy as the source legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単一の法人をエクスポートするには、法人エンティティ データ プロジェクトにコピーを作成し、元の法人としてコピーする法人を指定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>When you add entities or load templates, that type of project will automatically add legal entity filters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティを追加するとき、またはテンプレートを読み込むとき、そのプロジェクト タイプによって法人フィルターを自動的に追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>You can then download the package or create a template from it on the <bpt id="p1">**</bpt>Templates<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージをダウンロード、または <bpt id="p1">**</bpt>テンプレート<ept id="p1">**</ept> ページ上でそれからテンプレートを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>The package or template can then be added to an export project and used to export the legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージまたはテンプレートは、エクスポート プロジェクトに追加して、法人をエクスポートするために使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>Import a configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>The <bpt id="p1">**</bpt>Data management<ept id="p1">**</ept> workspace is also your hub for importing configuration data projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ管理<ept id="p1">**</ept> ワークスペースは、コンフィギュレーション データ プロジェクトをインポートするためのハブともなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>You can build a configuration project from an existing data project that you exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートした既存のデータ プロジェクトから、構成プロジェクトをビルドすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>Alternatively, you can build a configuration project from individual files that contain data that is formatted correctly for import into Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、Finance and Operations にインポートするため正しく書式設定されているデータを含む個々のファイルからコンフィギュレーション プロジェクトを構築することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>To import a configuration, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成をインポートするには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>Open the <bpt id="p1">**</bpt>Data management<ept id="p1">**</ept> workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ管理<ept id="p1">**</ept>ワークスペースを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>If you're in Standard view, select <bpt id="p1">**</bpt>Enhanced view<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準のビューを使用している場合は、<bpt id="p1">**</bpt>強化されたビュー<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>Select the <bpt id="p1">**</bpt>Import<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インポート<ept id="p1">**</ept> タイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>Select <bpt id="p1">**</bpt>New<ept id="p1">**</ept> to create a configuration data project, and enter an ID and name for the configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept> を選択してコンフィギュレーション データ プロジェクトを作成し、コンフィギュレーションの ID と名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>Set the operation type for the data project to <bpt id="p1">**</bpt>Import<ept id="p1">**</ept>, and set the project category to <bpt id="p2">**</bpt>Configuration<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ プロジェクトの操作タイプを <bpt id="p1">**</bpt>インポート<ept id="p1">**</ept> に設定し、プロジェクト カテゴリを <bpt id="p2">**</bpt>コンフィギュレーション<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>Add the entities that represent the information that you want to copy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーする情報を表すエンティティを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>You can add entities by using several methods:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のいくつかのメソッドを使用してエンティティを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source><bpt id="p1">**</bpt>Add one entity<ept id="p1">**</ept> – Enter the first part of the name of the entity until it appears in the lookup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>1 つのエンティティを追加<ept id="p1">**</ept> - ルックアップに表示されるまで、エンティティの名前の最初の部分を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source><bpt id="p1">**</bpt>Add multiple entities<ept id="p1">**</ept> – Enter any part of the entity name, use the lookup for the module, enter any part of the tag name, or use the lookup for the entity category to show a list of entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>複数のエンティティを追加<ept id="p1">**</ept> - エンティティ名の一部を入力、モジュールのルックアップを使用、タグの名前の一部を入力、またはエンティティ カテゴリのルックアップを使用して、エンティティの一覧を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>Press Tab to move focus away from the <bpt id="p1">**</bpt>Lookup<ept id="p1">**</ept> field and activate the filter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tab キーを押してフォーカスを <bpt id="p1">**</bpt>参照<ept id="p1">**</ept> フィールドの外に移動し、フィルターをアクティブにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>In the grid, select the entities to add.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッドで、追加するエンティティを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source><bpt id="p1">**</bpt>Add a file<ept id="p1">**</ept> – Browse to a file that contains a name that matches the name of an entity and a file name extension that matches the file name extension that is in your data sources, and the source data format will be set automatically.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ファイルを追加<ept id="p1">**</ept> - エンティティ名に一致する名前とデータ ソースにあるファイル名拡張子と一致するファイル名拡張子を含むファイルを参照し、ソース データ形式が自動的に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>If you haven't set up the default file name extensions, you must select a source data format before you select the file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のファイル名拡張子を設定していない場合は、ファイルを選択する前に、ソース データの形式を選択する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source><bpt id="p1">**</bpt>Add a template<ept id="p1">**</ept> – Select from a list of templates that you've loaded in your instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テンプレートを追加する<ept id="p1">**</ept> - インスタンスでロードされたテンプレートの一覧から選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>When you load a package, the <bpt id="p1">**</bpt>Import<ept id="p1">**</ept> page first reads the list of entities from the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージをロードするとき、<bpt id="p1">**</bpt>インポート<ept id="p1">**</ept> ページはまずパッケージからエンティティの一覧を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>A progress indicator shows how much of the package has been read.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">進行状況インジケーターは、パッケージのどれくらいが読み込まれたかを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>After the list of entities is read, the <bpt id="p1">**</bpt>Import<ept id="p1">**</ept> page starts to load the data in the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのリストが読み込まれた後、<bpt id="p1">**</bpt>インポート<ept id="p1">**</ept> ページがパッケージ内のデータ読み込みを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>This process can take some time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスには少し時間がかかる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>Select <bpt id="p1">**</bpt>Remove entity<ept id="p1">**</ept> to remove any selected entities, as required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティの削除<ept id="p1">**</ept> を選択し、必要に応じて選択したエンティティを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>After you've completed the configuration, select <bpt id="p1">**</bpt>Import<ept id="p1">**</ept> to start the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションが完了した後は、<bpt id="p1">**</bpt>インポート<ept id="p1">**</ept>を選択しインポートを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>You can monitor the results on the <bpt id="p1">**</bpt>Execution details<ept id="p1">**</ept> page that appears.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示される <bpt id="p1">**</bpt>実行の詳細<ept id="p1">**</ept> ページで結果を監視することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>Before you import a configuration, you might want to use some additional features that can help control the import process:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションをインポートする前に、インポート プロセスの管理に役立ついくつかの追加機能を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>To organize the list, use the <bpt id="p1">**</bpt>Sort by<ept id="p1">**</ept> button to reorder the entities by unit, level, or sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一覧を整理するには、<bpt id="p1">**</bpt>並べ替え<ept id="p1">**</ept> ボタンを使用して、単位、レベル、またはシーケンスでエンティティの順序を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>To change the execution sequence of any of the entities, you can manually edit the unit, level, or sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いずれかのエンティティの実行順序を変更するには、ユニット、レベル、またはシーケンスを手動で編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>Alternatively, you can use the <bpt id="p1">**</bpt>Resequence<ept id="p1">**</ept> button to update any entities that you've selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、<bpt id="p1">**</bpt>再シーケンス<ept id="p1">**</ept> ボタンを使用して選択したすべてのエンティティを更新できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>If you must change the entity mappings, use the <bpt id="p1">**</bpt>View map<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ マッピングを変更する必要がある場合、<bpt id="p1">**</bpt>マップの表示<ept id="p1">**</ept>ボタンを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>To temporarily prevent the entity from being used when you export a data project, use the check box in the <bpt id="p1">**</bpt>Disable<ept id="p1">**</ept> column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ プロジェクトをエクスポートするときにエンティティが一時的に使用されないようにするには、<bpt id="p1">**</bpt>無効化<ept id="p1">**</ept> 列のチェックボックスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>Copy into a legal entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人へのコピー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>The <bpt id="p1">**</bpt>Data management<ept id="p1">**</ept> workspace is also your hub for copying configuration information from one legal entity to another.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ管理<ept id="p1">**</ept> ワークスペースは、法人間でコンフィギュレーション情報をコピーためのハブともなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>The process resembles an export and import that occur in one step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスは、1 ステップで発生するエクスポートおよびインポートと共通点があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>As in an import, if information that exists in the source legal entity doesn't exist in the destination legal entity, the copy process adds it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートと同様に、ソース法人に存在する情報が相手方法人に存在しない場合、プロセスのコピーが追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>If information already exists in the destination legal entity, the copy process updates it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">情報が既に相手方の法人に存在する場合、コピー処理により更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>To copy a configuration from one legal entity to another legal entity in the same instance, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じインスタンス内である法人から別の法人に構成をコピーするには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>Open the <bpt id="p1">**</bpt>Data management<ept id="p1">**</ept> workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ管理<ept id="p1">**</ept>ワークスペースを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>If you're in Standard view, select <bpt id="p1">**</bpt>Enhanced view<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準のビューを使用している場合は、<bpt id="p1">**</bpt>強化されたビュー<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>Select the <bpt id="p1">**</bpt>Copy into legal entity<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>法人にコピー<ept id="p1">**</ept> タイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>Select <bpt id="p1">**</bpt>New<ept id="p1">**</ept> to create a configuration data project, and enter an ID and name for the configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept> を選択してコンフィギュレーション データ プロジェクトを作成し、コンフィギュレーションの ID と名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source>Set the operation type for the data project to <bpt id="p1">**</bpt>Copy into legal entity<ept id="p1">**</ept>, and set the project category to <bpt id="p2">**</bpt>Configuration<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ プロジェクトの操作タイプを <bpt id="p1">**</bpt>法人にコピー<ept id="p1">**</ept> に設定し、プロジェクト カテゴリを <bpt id="p2">**</bpt>コンフィギュレーション<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>Select the legal entity that should be the source of the data to copy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーするデータのソースとする必要がある法人を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>By default, the legal entity that you're currently using is selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、現在使用している法人が選択されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>On the <bpt id="p1">**</bpt>Legal entities<ept id="p1">**</ept> FastTab, you can select existing legal entities as a destination, or you can create new legal entities:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>法人<ept id="p1">**</ept>クイック タブで、宛先として既存の法人を選択することも、新しい法人を作成することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source><bpt id="p1">**</bpt>Select<ept id="p1">**</ept> – Select one or more legal entities in the list, and then select <bpt id="p2">**</bpt>Add selected<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>選択<ept id="p1">**</ept> – リストの中から 1 つ以上の法人を選択し、<bpt id="p2">**</bpt>選択対象の追加<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source>The legal entities are added to the list of destination legal entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人は宛先の法人のリストに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source><bpt id="p1">**</bpt>Create<ept id="p1">**</ept> – Enter the legal entity ID, the legal entity name, and the region that the legal entity belongs in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>作成<ept id="p1">**</ept> - 法人 ID、法人の名前、および法人が属する地域を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source>Then select <bpt id="p1">**</bpt>Create legal entity<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>法人を作成する<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source>The legal entity is created and added to the list of destination legal entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人が作成され、宛先の法人のリストに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source>The functionality for creating destination legal entities is available in Finance and Operations 7.2.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">宛先の法人を作成する機能は、Finance and Operations 7.2.3 で利用可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source>After you've added the destination legal entities, select <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> if the number sequences should be copied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出力先の法人を追加した後、番号の順序をコピーする場合<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source>The entities that are required in order to copy the number sequence codes and number sequence references will be added to the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">番号順序コードと番号順序参照をコピーするために必要なエンティティがプロジェクトに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source>The execution unit, level, and sequence number for these entities are set to the numbers in the default System and Shared templates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのエンティティの実行単位、レベル、および順序番号は、既定のシステム テンプレートと共有テンプレートの数値に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source>If you aren't using the default templates, adjust the entity sequences so that they are first in the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のテンプレートを使用していない場合は、エンティティ順序を調整しリストの最初にくるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source>If you selected <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> for number sequences, select <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> or <bpt id="p3">**</bpt>No<ept id="p3">**</ept> to specify whether those number sequences should be reset to the smallest value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">番号順序に対して<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>を選択した場合は、これらの番号シーケンスを最小値にリセットするかどうかを指定するには、<bpt id="p2">**</bpt>はい<ept id="p2">**</ept>または<bpt id="p3">**</bpt>いいえ<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source>Add the entities that represent the information that you want to copy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーする情報を表すエンティティを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source>You can add entities by using several methods:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のいくつかのメソッドを使用してエンティティを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source><bpt id="p1">**</bpt>Add one entity<ept id="p1">**</ept> – Enter the first part of the name of the entity until it appears in the lookup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>1 つのエンティティを追加<ept id="p1">**</ept> - ルックアップに表示されるまで、エンティティの名前の最初の部分を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source><bpt id="p1">**</bpt>Add multiple entities<ept id="p1">**</ept> – Enter any part of the entity name, use the lookup for the module, enter any part of the tag name, or use the lookup for the entity category to show a list of entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>複数のエンティティを追加<ept id="p1">**</ept> - エンティティ名の一部を入力、モジュールのルックアップを使用、タグの名前の一部を入力、またはエンティティ カテゴリのルックアップを使用して、エンティティの一覧を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source>Press Tab to move focus away from the <bpt id="p1">**</bpt>Lookup<ept id="p1">**</ept> field and activate the filter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tab キーを押してフォーカスを <bpt id="p1">**</bpt>参照<ept id="p1">**</ept> フィールドの外に移動し、フィルターをアクティブにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="504">
          <source>In the grid, select the entities to add.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッドで、追加するエンティティを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="505">
          <source><bpt id="p1">**</bpt>Add a file<ept id="p1">**</ept> – Browse to a file that contains a name that matches the name of an entity and a file name extension that matches the file name extension that is in your data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ファイルを追加<ept id="p1">**</ept> - エンティティ名に一致する名前とデータ ソースにあるファイル名拡張子と一致するファイル名拡張子を含むファイルを参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="506">
          <source><bpt id="p1">**</bpt>Add a template<ept id="p1">**</ept> – Select from a list of templates that you've loaded in your instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テンプレートを追加する<ept id="p1">**</ept> - インスタンスでロードされたテンプレートの一覧から選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="507">
          <source>To help guarantee that the correct order is maintained, we recommend that you use the default templates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正しい順序が保たれるように、既定のテンプレートを使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="508">
          <source>Then add and remove entities to match the data that you want to copy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、コピーするデータと一致するエンティティを追加して削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="509">
          <source>You can remove the entities that you don't want to copy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーしないエンティティを削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="510">
          <source>If an entity has a field that represents the legal entity, a filter will be applied to that entity, so that only the data for the source legal entity is included.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティに法人を表すフィールドがある場合、ソースの法人のデータのみが含まれように、フィルターにはそのエンティティが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="511">
          <source>The value for that field will be changed to the destination legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのフィールドの値は、宛先の法人組織に変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="512">
          <source>Document, transaction, and composite entities aren't available when you copy to a legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にコピーする場合、ドキュメント、トランザクション、および複合エンティティは使用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="513">
          <source>Select <bpt id="p1">**</bpt>Remove entity<ept id="p1">**</ept> to remove any selected entities, as required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティの削除<ept id="p1">**</ept> を選択し、必要に応じて選択したエンティティを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="514">
          <source>After you've completed the configuration, select <bpt id="p1">**</bpt>Copy into legal entity<ept id="p1">**</ept> to start the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションが完了した後は、<bpt id="p1">**</bpt>法人へのコピー<ept id="p1">**</ept>を選択しインポートを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="515">
          <source>The copy process will export the data from the source legal entity into the destination legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピー プロセスは、ソースの法人から送信先の法人組織にデータをエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="516">
          <source>Each destination legal entity will have its own import data project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各相手方の法人には、独自のインポート データ プロジェクトがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="517">
          <source>You can monitor the results on the <bpt id="p1">**</bpt>Execution summary<ept id="p1">**</ept> page that appears.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示される <bpt id="p1">**</bpt>実行の要約<ept id="p1">**</ept> ページで結果を監視することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="518">
          <source>All import projects that are related to the Copy into legal entity project will appear in a list on the left of the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人プロジェクトへのコピーに関連付けられているすべてのインポート プロジェクトはページの左側の一覧に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="519">
          <source>Any errors that occur are shown on the <bpt id="p1">**</bpt>Execution summary<ept id="p1">**</ept> page, just as they are for an import project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート プロジェクトの場合と同様に、発生したエラーは<bpt id="p1">**</bpt>実行の要約<ept id="p1">**</ept>ページ上に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="520">
          <source>You can edit the errors in the staging tables and resubmit the values for each data project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステージング テーブルでエラーを編集して、各データ プロジェクトのために値を再送信することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="521">
          <source>Special considerations when you copy into a legal entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にコピーする際の特別な注意事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="522">
          <source>When you copy into a legal entity, you have the same validation that occurs when you import a file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人にコピーするときは、ファイルをインポートするときに発生する同じ検証を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="523">
          <source>It's important that you test your copy in a test environment, so that you can identify any dependencies that will cause failures.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">障害の原因となる依存関係を識別できるように、テスト環境でのコピーをテストすることが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="524">
          <source>If dependent information isn't included in your list of entities to copy, the entity will show errors when it tries to copy into the legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">依存情報は、コピーするエンティティの一覧に含まれていない場合は、エンティティでは、法人にコピーするときにエラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="525">
          <source>For example, if a customer has a default site or warehouse, you must use one of these approaches:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、顧客が既定のサイトまたは倉庫を持っている場合、これらのアプローチのいずれかを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="526">
          <source>Import the sites and warehouses as part of the copy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーの一部として、サイトおよび倉庫をインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="527">
          <source>Manually load the sites and warehouses before you copy the legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人をコピーする前に、サイトおよび倉庫を手動で読み込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="528">
          <source>Unmap the site and warehouse fields before you copy the information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">情報をコピーする前に、サイトと倉庫のフィールドをマップ解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="529">
          <source>You might also experience import errors if you copy from one region to another region.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つの領域から別の領域へコピーする場合、インポート エラーが発生する可能性もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="530">
          <source>For example, you can have 1099 fields in a legal entity in the US region.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、米国地域の法人に 1099 フィールドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="531">
          <source>However, if you try to import those values into a legal entity in a German region, you will see errors on the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ドイツ地域で法人にそれらの値をインポートしようとする場合、インポートのエラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="532">
          <source>If a template that you load has entities that are incorrect for a region, you will receive an error message that states that the incorrect entity wasn't loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロードしたテンプレートには、地域において間違ったエンティティがある場合は、間違ったエンティティが読み込まれていることを示すエラー メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="533">
          <source>However, the rest of the template will continue to be loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、テンプレートの残りは、引き続きロードされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="534">
          <source>You should copy only information that is appropriate for the destination region.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">送付先地域に適した情報のみをコピーする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="535">
          <source>The following entities require special handling when they are used to copy into a legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のエンティティは、法人へのコピーに使用される場合、特別な取り扱いが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="536">
          <source>Area</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">面</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="537">
          <source>Entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="538">
          <source>Action</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="539">
          <source>System setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="540">
          <source>Number sequences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">番号順序</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="541">
          <source>If you use a number sequence for vendors and customers on the parameters forms and then you copy customers and vendors, you need to make sure that the "Allow user to change to a lower number" settings on the number sequences to Yes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター フォームで仕入先および顧客に番号シーケンスを使用し、顧客および仕入先をコピーする場合は、番号シーケンスで「数字の小さいユーザーに変更を許可する」設定が「はい」になっていることを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="542">
          <source>The "No" settings will cause the import to reject vendor and customer numbers since they were created before using numbers lower than the next available number sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「いいえ」設定の場合、インポートで仕入先および顧客番号が拒否されます。それらの番号が、次の使用可能な番号順序よりも低い番号を使用する前に作成されるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="543">
          <source>If you use the Reset to smallest feature, you need to change the "Allow user to change to a higher number" since the vendor and customer numbers are higher than the next available number sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最小の機能にリセットする機能を使用する場合は、仕入先番号と顧客番号が次に使用可能な番号の順序よりも高いため、「ユーザーをより高い番号に変更することを許可する」を変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="544">
          <source>System setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="545">
          <source>Workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="546">
          <source>Workflow requires additional changes before it can be copied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローはコピーする前に追加の変更が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="547">
          <source>Workflow copies are not supported at this time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローのコピーは現時点ではサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="548">
          <source>Accounts payable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">買掛金</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="549">
          <source>Vendors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入先</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="550">
          <source>Vendors have many settings that are dependent on the values that come from other entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入先には、他のエンティティからの値に依存する多くの設定があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="551">
          <source>For example, if you update the matching settings to require three-way matching but you have vendors set for two-way matching, the vendor will fail validation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、スリーウェイ マッチングを要求するようマッチングの設定を更新しても、ツーウェイ マッチングに設定した仕入先がある場合、仕入先は検証に失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="552">
          <source>If you use auto sequencing for new vendor, you will need to unmap the vendor account before you do the copy into legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい仕入先に対して自動の優先順位を使用する場合は、法人にコピーを実行する前に、仕入先勘定のマップを解除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="553">
          <source>In addition, if an auto-sequenced vendor has an invoice account, that vendor account is not transformed and may fail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、自動で順序付けられた仕入先に請求先/元 ID がある場合は、その仕入先勘定は変換されず、失敗する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="554">
          <source>You may see similar issues in other areas such as vendors in posting accounts and approved vendor list by products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">転記勘定の仕入先および製品ごとの承認済仕入先リストなどの他の領域で類似の問題を確認する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="555">
          <source>Accounts receivable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">売掛金</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="556">
          <source>Customers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="557">
          <source>Customers have many settings that are dependent on the values that come from other entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客には、他のエンティティからの値に依存する多くの設定があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="558">
          <source>For example, if you have a default warehouse and site for a customer, you must add sites and warehouses first or the customer will fail validation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、顧客用の既定の倉庫とサイトがある場合、サイトおよび倉庫を最初に追加する必要があり、または顧客は検証に失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="559">
          <source>The collections contact will also fail if the contact is not available in the new company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい会社で連絡先が利用できない場合は、コレクションの連絡先も利用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="560">
          <source>If you use auto sequencing for new customers, you will need to unmap the customer account before you do the copy into legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい顧客に対して自動の優先順位を使用する場合は、法人にコピーを実行する前に、顧客勘定のマップを解除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="561">
          <source>In addition, if an auto-sequenced customer has an invoice account, that invoice account is not transformed and may fail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、自動で順序付けられた顧客に請求先/元 ID がある場合は、その請求先/元 ID は変換されず、失敗する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="562">
          <source>You may see similar issues in other areas such as customers in posting accounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">転記勘定の顧客などの他の領域で類似の問題を確認する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="563">
          <source>Budget</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="564">
          <source>Budget cost elements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算原価要素</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="565">
          <source>There is an issue when importing budget cost elements when using an annual amount and there are budget cost elements in the Earnings basis tab. The issue will be addressed in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算額の要素をインポートする際、年間金額を使用しているときに、[利益基準] タブに予算原価要素があると問題が発生します。この問題は、今後のリリースで対処される予定です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="566">
          <source>Fixed assets</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">固定資産</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="567">
          <source>Fixed assets depreciation profile manual schedule</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">固定資産減価償却プロファイル手動スケジュール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="568">
          <source>The fixed asset depreciation profile must be processed first.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">固定資産減価償却プロファイルを最初に処理する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="569">
          <source>Change the sequence on your data project for fixed asset depreciation profile to 15 (instead of 10).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">固定資産の減価償却プロファイルのデータ プロジェクトの順序を15 (10ではなく) に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="570">
          <source>We will update the default templates in the monthly application release 4 to this value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">月 1 回のアプリケーション リリース 4 の既定のテンプレートをこの値に更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="571">
          <source>General ledger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般会計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="572">
          <source>Intercompany accounting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社間会計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="573">
          <source>The copy into legal entity feature does not support intercompany accounting at this time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人へのコピー機能は、現時点では会社間会計をサポートしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="574">
          <source>The issue will be addressed in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、今後のリリースで対処される予定です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="575">
          <source>General ledger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般会計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="576">
          <source>Journal names</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕訳帳名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="577">
          <source>Only the journal names for the source legal entity will be copied to the destination companies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース法人の仕訳帳名のみ相手方の会社にコピーされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="578">
          <source>If you select the lookup in the journal names form, you will only see the number sequences that are available for that legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕訳帳名フォームのルックアップを選択した場合は、その法人に対して利用可能な番号シーケンスのみが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="579">
          <source>However, if you choose to enter a number sequence manually that is not on that list, it will not be included in the copy process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、手動でそのリストにない番号順序を入力するよう選択する場合、それはコピー処理には含まれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="580">
          <source>General ledger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般会計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="581">
          <source>Ledger allocation rules destination</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳配賦ルールの出力先</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="582">
          <source>If you are running a version of Finance and Operations earlier than version 7.3, if you have cross company allocation rules, you will not see the destination rules for legal entities that do not match the source legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations がバージョン 7.3 以前ののバージョンを実行し、会社間の配賦ルールがある場合は、ソースの法人とは一致しない法人の相手方のルールは表示されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="583">
          <source>The copy into legal entity feature will only copy the destination records when the destination is equal to the source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人へのコピー機能は、送信先がソースと等しい場合にのみ送信先レコードをコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="584">
          <source>The issue has been resolved in version 7.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題はバージョン 7.3 で解決されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="585">
          <source>General ledger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般会計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="586">
          <source>Ledger fiscal calendar year/period</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳の会計カレンダー年/期間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="587">
          <source>The process is currently exporting all of the legal entities instead of just the source legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスは、現在は、ソースの法人だけではなく、すべての法人をエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="588">
          <source>The copy process works correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピー処理は正しく動作します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="589">
          <source>The issue has been resolved in version 7.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題はバージョン 7.3 で解決されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="590">
          <source>General ledger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般会計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="591">
          <source>Ledger parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="592">
          <source>If you check for continuous number sequences but you have number sequences that are used on journal names and are not continuous, the imports will fail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">連続する番号順序を確認しますが、仕訳帳名で使用されている番号順序があり、それが継続的ではない場合、インポートが失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="593">
          <source>You should temporarily turn off that setting in the ledger parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳パラメーターの設定を一時的にオフにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="594">
          <source>In addition, the ledger parameters must be processed first.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、元帳のパラメーターを最初に処理する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="595">
          <source>Change the sequence on your data project for ledger parameters to 15 (instead of 40).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元帳パラメーターのデータ プロジェクトの順序を 15 (40 ではなく) に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="596">
          <source>We will update the default templates in the monthly application release 3 to this value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">月 1 回のアプリケーション リリース 3 の既定のテンプレートをこの値に更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="597">
          <source>Inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="598">
          <source>Inventory dimension parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫分析コード パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="599">
          <source>There is an issue where an error on import is shown but the correct number of parameters are imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート時にエラーが表示されるが、正しい数のパラメーターがインポートされるという問題があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="600">
          <source>The issue will be addressed in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、今後のリリースで対処される予定です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="601">
          <source>Inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="602">
          <source>Warehouse locations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">倉庫の場所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="603">
          <source>Some warehouse locations require a location profile ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの倉庫の場所には、場所のプロファイル ID が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="604">
          <source>Location profile IDs require a location format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場所プロファイル ID には、場所の形式が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="605">
          <source>Currently, the location format information must be manually added before the warehouse location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、場所の形式情報は倉庫の場所の前に手動で入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="606">
          <source>The entities for the location format and location profile were added in version 7.2.3, (App update 3 of the July 2017 release).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場所の形式と場所プロファイルのエンティティが、バージョン 7.2.3 で追加されました (2017 年 7 月のリリースの App Update 3)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="607">
          <source>Master planning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マスター プラン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="608">
          <source>Intercompany master plan associations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社間マスター プランのアソシエーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="609">
          <source>The copy into legal entity feature does not support intercompany master plan associations at this time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人へのコピー機能は、現時点では会社間マスター プランのアソシエーションをサポートしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="610">
          <source>The issue will be addressed in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、今後のリリースで対処される予定です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="611">
          <source>Retail</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="612">
          <source>POS registers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS レジスター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="613">
          <source>This entity is global and cannot be copied to another legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティはグローバルであり、別の法人にコピーすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="614">
          <source>Retail</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="615">
          <source>Retail channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャネル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="616">
          <source>This entity is global and cannot be copied to another legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティはグローバルであり、別の法人にコピーすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="617">
          <source>Retail</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="618">
          <source>Retail store address book</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売店舗アドレス帳</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="619">
          <source>This entity has a dependency on Retail channel so it cannot be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティは、Retail チャネルに依存するため、使用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="620">
          <source>Sales and marketing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売とマーケティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="621">
          <source>Intercompany trading partnerships</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社間取引相手</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="622">
          <source>The copy into legal entity feature does not support intercompany trading partnerships at this time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人へのコピー機能は、現時点では会社間取引相手をサポートしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="623">
          <source>The issue will be addressed in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、今後のリリースで対処される予定です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="624">
          <source>Rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="625">
          <source>The Copy into legal entity feature supports rules, which let you modify data before it's added to the import staging table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法人へのコピー機能では、ステージング テーブルに追加される前にデータの変更を許可するルールがサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="626">
          <source>For example, rules are used to change the target legal entity to the destination legal entity and modify number sequences.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、対象法人を宛先法人に変更するルールを使用し、番号順序を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="627">
          <source>You can extend rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールを拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="628">
          <source>Rule extensions require three changes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールの拡張機能には、次の 3 つの変更が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="629">
          <source>Add the name of the rule to the extensible <bpt id="p1">**</bpt>DMFRulesType<ept id="p1">**</ept> enumeration (enum).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能 <bpt id="p1">**</bpt>DMFRulesType<ept id="p1">**</ept> の列挙 (列挙) へルールの名前を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="630">
          <source>For each project definition group, insert the enum that you just created (for example, <bpt id="p1">**</bpt>DMFRulesType::NewRule<ept id="p1">**</ept>) into the DMFRules table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各プロジェクト定義グループに対して、作成したばかりの列挙 (たとえば、<bpt id="p1">**</bpt>DMFRulesType::NewRule<ept id="p1">**</ept>) を DMFRules テーブルに挿入します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="631">
          <source>Use your source legal entity, your rule type, and the definition group name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソースの法人、ルールの種類、および定義グループの名前を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="632">
          <source>If you require that more data be stored, such as various options for your rule, you can create your own table and extend the DMFRules table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールにさまざまなオプションなど、さらにデータを格納することが必要な場合は、独自のテーブルを作成し、DMFRules テーブルを拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="633">
          <source>Create your own class to handle the data that the rule acts on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールが動作するデータを処理する、独自のクラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="634">
          <source>For the DMFRules framework to instantiate the rule, you must decorate the class with the <bpt id="p1">**</bpt><ph id="ph1">\[</ph>DMFRulesBaseFactoryAttribute(DMFRulesType::NewRule)<ph id="ph2">\]</ph><ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DMFRules フレームワークでルールをインスタンス化するには、<bpt id="p1">**</bpt><ph id="ph1">\[</ph>DMFRulesBaseFactoryAttribute(DMFRulesType::NewRule)<ph id="ph2">\]</ph><ept id="p1">**</ept> 属性でクラスを修飾する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="635">
          <source>The class must also extend the <bpt id="p1">**</bpt>DMFRulesBase<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスは、<bpt id="p1">**</bpt>DMFRulesBase<ept id="p1">**</ept> クラスも拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="636">
          <source>This extension will require an implementation of the <bpt id="p1">**</bpt>DMFRulesBase.runRule(Common<ph id="ph1">\_</ph>staging)<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この拡張は、<bpt id="p1">**</bpt>DMFRulesBase.runRule(Common<ph id="ph1">\_</ph>staging)<ept id="p1">**</ept> メソッドの実装が必要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="637">
          <source>The <ph id="ph1">\_</ph>staging record will be the buffer of the staging record that the rule is applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\_</ph>staging レコードは、ルールが適用されるステージング レコードのバッファーになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="638">
          <source>Additional information about entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティに関する追加情報</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="639">
          <source>Obsolete entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">古いエンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="640">
          <source>As Finance and Operations is updated, the functionality of an entity might have to be updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations が更新されると、エンティティの機能を更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="641">
          <source>A new entity might be created that has a different name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さまざまな名前を持つ新しいエンティティが作成される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="642">
          <source>In this case, the original entity will be marked as obsolete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、元のエンティティは古いものとしてマークされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="643">
          <source>You will no longer be able to add obsolete entities to a new data project or template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータ プロジェクトまたはテンプレートに古い形式のエンティティを追加することがなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="644">
          <source>If you load a data package that contains an obsolete entity, you will receive a warning about the existence of obsolete entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">廃止されたエンティティを含むデータ パッケージを読み込むと、廃止されたエンティティの存在に関する警告が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="645">
          <source>However, you will still be able to import your data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、データをインポートすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="646">
          <source>You can find the obsolete entity by selecting the <bpt id="p1">**</bpt>Obsolete<ept id="p1">**</ept> column and filtering on <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">古いエンティティは、<bpt id="p1">**</bpt>古い形式<ept id="p1">**</ept> 列を選択して <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> をフィルタリングすることにより見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="647">
          <source>Self-referencing entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自己参照エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="648">
          <source>Some entities represent tables that have references to themselves.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部のエンティティは、自身を参照するテーブルを表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="649">
          <source>For example, when you create a cash discount, you can refer to a related cash discount that creates a tiered discount calculation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、現金割引を作成するときに、階層化された割引計算を作成する、関連付けられた現金割引を参照できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="650">
          <source>To import data, you must sequence the data so that the cash discount that is referred to in the <bpt id="p1">**</bpt>Next cash discount<ept id="p1">**</ept> field is imported before the cash discount that uses that cash discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データをインポートするには、<bpt id="p1">**</bpt>次の現金割引<ept id="p1">**</ept> フィールドで参照される現金割引がその現金割引を使用する現金割引の前にインポートされるようにデータを順序付けする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="651">
          <source>A new <bpt id="p1">**</bpt>DMFImportExportSequencer<ept id="p1">**</ept> class sequences the data in self-referencing entities and enables the data to be loaded in a single pass.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい <bpt id="p1">**</bpt>DMFImportExportSequencer<ept id="p1">**</ept> クラスによって自己参照エンティティのデータが配列され、データを 1 つのパスに読み込むことが可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="652">
          <source>In the Cash Discount entity (CashDiscountEntity), you can view the code that is required in order to update entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現金割引エンティティ (CashDiscountEntity) では、エンティティを更新するために必要なコードを表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="653">
          <source>The class has been added to several self-referencing entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスはいくつかの自己参照エンティティに追加されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="654">
          <source>It will be added to more entities as required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じてさらに多くのエンティティに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="655">
          <source>Here are some other examples of self-referencing entities:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自己参照エンティティの他の例を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="656">
          <source>Customers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="657">
          <source>Customer definitions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客の定義</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="658">
          <source>Customer details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客の詳細</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="659">
          <source>Tax codes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="660">
          <source>Budget control groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算管理グループ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="661">
          <source>Projects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="662">
          <source>Product categories</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品カテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="663">
          <source>Warehouses</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">倉庫</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="664">
          <source>Budget plan workflow stage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予算計画ワークフロー ステージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="665">
          <source>Sales units</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売単位</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="666">
          <source>Adding entities in the appropriate country/region context</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切な国/地域のコンテキストでのエンティティの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="667">
          <source>When you add entities, the mappings are created in the context of the country or region of the company that is currently active.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティを追加するとき、マッピングが、現在アクティブな会社の国または地域のコンテキストで作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="668">
          <source>If there are any issues with the mappings, a red <bpt id="p1">*</bpt>X<ept id="p1">*</ept> appears in the <bpt id="p2">**</bpt>View map<ept id="p2">**</ept> column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マッピングで問題がある場合は、<bpt id="p2">**</bpt>マップの表示<ept id="p2">**</ept>列に赤い <bpt id="p1">*</bpt>X<ept id="p1">*</ept> が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="669">
          <source>Select the red <bpt id="p1">*</bpt>X<ept id="p1">*</ept>, and repair the mappings as required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">赤色の <bpt id="p1">*</bpt>X<ept id="p1">*</ept> を選択し、必要に応じてマッピングを修復します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="670">
          <source>By default, the DAT company doesn't have a country/region context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、DAT 会社は国/地域のコンテキストを持っていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="671">
          <source>Some entities, such as the entities that are used for transaction codes and 1099 fields, won't be mapped correctly if they are added to a data project for the DAT company, because a country/region context is expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション コードおよび 1099 フィールドに使用されるエンティティなどの一部のエンティティは、国/地域コンテキストが必要なため、DAT 会社のデータ プロジェクトに追加された場合は正しくマッピングされません。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="localize-workspaces-on-server.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>localize-workspaces-on-server.b807c1.ce0cd0570772b713a25fdfe5cfca430f82a5d7a1.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>ce0cd0570772b713a25fdfe5cfca430f82a5d7a1</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\mobile-apps\platform\scenarios\localize-workspaces-on-server.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Localize mobile workspaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル ワークスペースのローカライズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how you can use workspace classes to provide localization support to workspaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、ワークスペース クラスを使用して、ワークスペースにローカライゼーション サポートを提供する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Localize mobile workspaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル ワークスペースのローカライズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can use workspace classes in several ways to provide localization support to workspaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの方法でワークスペース クラスを使用すると、ワークスペースにローカライゼーション サポートを提供することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Use config objects to pass localized labels</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Config オブジェクトを使用して、ローカライズされたラベルを渡す</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A config object can be added to the workspace metadata when it's requested by the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション オブジェクトは、モバイル アプリケーションから要求されたときに、ワークスペース メタデータに追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Later, the config object can be used to provide localization support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後で、config オブジェクトは、ローカライズ サポートを提供するために使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For example, the following workspace requires localized labels for the <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> control that you added via the business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次のワークスペースは、ビジネス ロジックを通して追加された <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> コントロールの、ローカライズされたラベルを必要とします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Customer details workspace where the Rentals link text isn't localized</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レンタル リンクのテキストがローカライズされていないお客様の詳細ワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The business logic for the app contains a call to the <bpt id="p1">**</bpt>addLink<ept id="p1">**</ept> method, as shown in the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションのビジネス ロジックには、次の図に示すように、<bpt id="p1">**</bpt>addLink<ept id="p1">**</ept> メソッドの呼び出しが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This <bpt id="p1">**</bpt>addLink<ept id="p1">**</ept> method adds a link to the <bpt id="p2">**</bpt>Rentals<ept id="p2">**</ept> page for the current customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この <bpt id="p1">**</bpt>addLink<ept id="p1">**</ept> メソッドは、現在のお客様の <bpt id="p2">**</bpt>レンタル<ept id="p2">**</ept> ページへリンクを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In this case, the label for the link is <bpt id="p1">**</bpt>Rentals<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、リンクのラベルは<bpt id="p1">**</bpt>レンタル<ept id="p1">**</ept>です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>However, because there isn't a localized label for the link, the link always appears as <bpt id="p1">**</bpt>Rentals<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、リンクのローカライズされたラベルがないため、リンクは常に<bpt id="p1">**</bpt>レンタル<ept id="p1">**</ept>として表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Call to metadataService.addLink</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">metadataService.addLink への呼び出し</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>To use a config object to provide localized labels, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成オブジェクトを使用してローカライズされたラベルを提供するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Create a config class that contains the fields for the labels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベルのフィールドを含む config クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>One field, <bpt id="p1">**</bpt>rentalLinkLabel<ept id="p1">**</ept>, is added to the class that will contain the label for the <bpt id="p2">**</bpt>pageLink<ept id="p2">**</ept> control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのフィールド、<bpt id="p1">**</bpt>rentalLinkLabel<ept id="p1">**</ept> が、<bpt id="p2">**</bpt>pageLink<ept id="p2">**</ept> コントロールのラベルを含むクラスに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The config class must be a data contract class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション クラスは、データ契約クラスでなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Config class code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス コード コンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The config class is used by a workspace class for the workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション クラスは、ワークスペースのワークスペース クラスで使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The workspace class requires the <bpt id="p1">**</bpt>appId<ept id="p1">**</ept> value of the workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース クラスには、ワークスペースの <bpt id="p1">**</bpt>appId<ept id="p1">**</ept> 値が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>You can find the app ID in the App designer, as shown in the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図に示すように、アプリ デザイナーでアプリの ID を検索することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>App ID in the workspace summary</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース概要のアプリ ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The following illustration shows what the workspace class looks like when the <bpt id="p1">**</bpt>appId<ept id="p1">**</ept> value is set on the attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、<bpt id="p1">**</bpt>appId<ept id="p1">**</ept> 値が属性に設定されているときのワークスペース クラスの外観を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The class also contains a method, <bpt id="p1">**</bpt>addConfig<ept id="p1">**</ept>, that sets a config object that contains the value for the label.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスには、ラベルの値を含む設定オブジェクトを設定するメソッド、<bpt id="p1">**</bpt>addConfig<ept id="p1">**</ept> も含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Workspace class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The following illustration shows the config object in the <bpt id="p1">**</bpt>appInit<ept id="p1">**</ept> call in the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、モバイル アプリの <bpt id="p1">**</bpt>appInit<ept id="p1">**</ept> コールの config オブジェクトを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Config object in the mobile app</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリのコンフィギュレーション オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The config object can now be used and passed to the <bpt id="p1">**</bpt>addLink<ept id="p1">**</ept> method instead of the hard-coded label.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これで、コンフィギュレーション オブジェクトを使用し、ハードコーディングされたラベルの代わりに <bpt id="p1">**</bpt>addLink<ept id="p1">**</ept> メソッドに渡すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>metadataService.addLink with a call to the config object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">config オブジェクトの呼び出しによる metadataService.addLink</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Use a workspace class to update the workspace title and description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース クラスを使用して、ワークスペースのタイトルと説明を更新する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>A workspace class can be used to provide localized strings for the workspace title and description.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース クラスは、ワークスペースのタイトルと説明のローカライズされた文字列を提供するために使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>If you don't localize the title and description, the fields will be in the language that you implemented them in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイトルと説明をローカライズしていない場合、それらを実装した言語がフィールドの言語になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In this example, we will localize a workspace where <bpt id="p1">**</bpt>MyWorkspace<ept id="p1">**</ept> is the title and <bpt id="p2">**</bpt>A sample workspace<ept id="p2">**</ept> is the description.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>MyWorkspace<ept id="p1">**</ept> がタイトルで、<bpt id="p2">**</bpt>サンプル ワークスペース<ept id="p2">**</ept>が説明となっているワークスペースをローカライズします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>List of workspaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースのリスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Selected workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択されたワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If you don't have a workspace class for your workspace, create a workspace class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースのワークスペース クラスを持っていない場合、ワークスペースのクラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Override the <bpt id="p1">**</bpt>getWorkspaceMetadata<ept id="p1">**</ept> method to get the workspace metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>getWorkspaceMetadata<ept id="p1">**</ept> メソッドをオーバーライドし、ワークスペース メタデータを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>You must have the workspace metadata to provide labels for the workspace title and description fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースのタイトルおよび説明フィールドのラベルにするワークスペース メタデータが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Use the <bpt id="p1">**</bpt>workspaceTitle<ept id="p1">**</ept> and <bpt id="p2">**</bpt>workspaceDescription<ept id="p2">**</ept> properties to set the workspace title and description from a label.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースのタイトルと説明をラベルから設定するには、<bpt id="p1">**</bpt>workspaceTitle<ept id="p1">**</ept> および <bpt id="p2">**</bpt>workspaceDescription<ept id="p2">**</ept> プロパティを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In the following illustration, placeholders are assigned to the <bpt id="p1">**</bpt>workspaceTitle<ept id="p1">**</ept> and <bpt id="p2">**</bpt>workspaceDescription<ept id="p2">**</ept> properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図では、プレースホルダーが <bpt id="p1">**</bpt>workspaceTitle<ept id="p1">**</ept> および <bpt id="p2">**</bpt>workspaceDescription<ept id="p2">**</ept> プロパティに割り当てられています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Providing a title and a description in the workspace class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース クラスのタイトルと説明を提供</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Build the workspace class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース クラスをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Update the app list on the mobile client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル クライアントのアプリ リストを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The following illustration shows the title and description on a phone that uses English and Danish.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、英語とデンマーク語を使用する電話機のタイトルと説明を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Final workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最終ワークスペース</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
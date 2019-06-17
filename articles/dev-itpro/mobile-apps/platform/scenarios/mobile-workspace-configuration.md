<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="mobile-workspace-configuration.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>mobile-workspace-configuration.1712aa.795295a5d41ea9b8205ee8aeaee911ffbea36aef.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>795295a5d41ea9b8205ee8aeaee911ffbea36aef</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\mobile-apps\platform\scenarios\mobile-workspace-configuration.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure workspaces by using the SysAppWorkspace class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysAppWorkspace クラスを使用してワークスペースを構成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how you can use the SysAppWorkspace class to configure and publish workspaces on the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、SysAppWorkspace クラスを使用してサーバー上のワークスペースを構成および公開する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Configure workspaces by using the SysAppWorkspace class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysAppWorkspace クラスを使用してワークスペースを構成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Workspace class, <bpt id="p1">**</bpt>SysAppWorkspace<ept id="p1">**</ept>, is the starting point to create, configure and publish workspaces on the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース クラス <bpt id="p1">**</bpt>SysAppWorkspace<ept id="p1">**</ept> は、サーバー上でワークスペースを作成、構成および公開する開始点です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following two categories of APIs are available for use in sysAppWorkspace;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">sysAppWorkspace で使用できる API には、次の 2 つのカテゴリがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source><bpt id="p1">**</bpt>Workspace attributes<ept id="p1">**</ept>; used to create pages, tasks, entities, lookups, relationships in order to build mobile workspaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ワークスペースの属性<ept id="p1">**</ept>; はモバイルワークスペースを構築するために、ページ、タスク、エンティティ、ルックアップ、リレーションシップの作成に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source><bpt id="p1">[</bpt>Download the sample project for Fleet Management Mobile App<ept id="p1">](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples)</ept> (.axpp file).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>フリート管理のモバイル アプリのサンプル プロジェクトをダウンロードする<ept id="p1">](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples)</ept> (.axpp ファイル)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source><bpt id="p1">*</bpt>After downloading the file, open Visual Studio on your Operations development environment, then click Dynamics 365 &gt; Import Project, and browse for the downloaded project file. On the same dialog, check "overwrite" and check "create a new solution". After the import is complete, build the solution (or build the Fleet Management model). To review the example, start by reviewing 'FMReservationManagementWorkspace' class to see all the pages and actions included in the workspace. Use Solution Explorer to find page and task classes, and all the assets included in each. Use the API reference for more details on each API.<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>ファイルをダウンロードした後、オペレーション開発環境で Visual Studio を開き、Dynamics 365 &gt; プロジェクトのインポートをクリックし、ダウンロードしたプロジェクト ファイルを閲覧します。同じダイアログで、上書きにチェックを入れ、新しいソリューションの作成にチェックを入れます。インポートが完了した後、ソリューションを構築 (またはフリート管理モデルを構築) します。例を確認するには、まず、ワークスペースに含まれるすべてのページとアクションを見るために、'FMReservationManagementWorkspace' クラスを確認します。ソリューション エクスプローラを使用して、ページおよびタスク クラスを検索し、それぞれに含まれるすべての資産を検索してください。各 API の詳細については、API リファレンスを使用してください。<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">**</bpt>A mobile workspace can be created through designer pane, using X++ attribute APIs or a combination of both. See topic 'Use the workspace class to publish workspaces from AOT resources' below for more details on importing mobile app metadata from designer to AOT. Sample above is a complete mobile app built using X++ attribute APIs.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>X++ モバイル ワークスペースは、デザイナー ウィンドウで、X++ 属性 API またはその両方の組み合わせを使用して作成できます。 デザイナーから AOT へのモバイル アプリ メタデータのインポートの詳細については、以下の「ワークスペース クラスを使用して AOT リソースのワークスペースを公開する」を参照してください。上記のサンプルは、X++ 属性 API を使用して構築された完全なモバイル アプリです。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source><bpt id="p1">**</bpt>Workspace metadata classes<ept id="p1">**</ept>; used to inspect and apply server-side business logic to metadata for mobile workspaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ワークスペース メタデータ クラス<ept id="p1">**</ept>; はモバイル ワークスペースのためのメタデータへのサーバー側のビジネス ロジックを調査し、適用するために使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source><bpt id="p1">[</bpt>See complete list of server-side APIs<ept id="p1">](../mobile-workspace-server-apis.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>サーバー側の APIs の完全な一覧を参照してください。<ept id="p1">](../mobile-workspace-server-apis.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Create a new workspace class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいワークスペース クラスを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To use the <bpt id="p1">**</bpt>SysAppWorkspace<ept id="p1">**</ept> class for your workspace, you must create a new class for the workspace by extending the <bpt id="p2">**</bpt>SysAppWorkspace<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースに <bpt id="p1">**</bpt>SysAppWorkspace<ept id="p1">**</ept> クラスを使用するには、 <bpt id="p2">**</bpt>SysAppWorkspace<ept id="p2">**</ept> クラスを拡張してワークスペース用に新しいクラスを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>You can then use the new class to modify workspace metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいクラスを使用してワークスペース メタデータを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The new class also provides hooks for life cycle management of the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいクラスは、モバイル アプリのライフ サイクル管理のフックも提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Follow these steps to create a new workspace class for your workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース用の新しいワークスペース クラスを作成するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Create a new class for your workspace, and extend it from the <bpt id="p1">**</bpt>SysAppWorkspace<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース用の新しいクラスを作成し、それを <bpt id="p1">**</bpt>SysAppWorkspace<ept id="p1">**</ept> クラスから拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Workspace class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Add the <bpt id="p1">**</bpt>SysAppWorkspaceAttribute<ept id="p1">**</ept> attribute to the new class, and provide the <bpt id="p2">**</bpt>AppID<ept id="p2">**</ept> value of your workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいクラスに <bpt id="p1">**</bpt>SysAppWorkspaceAttribute<ept id="p1">**</ept> 属性を追加し、ワークスペースの <bpt id="p2">**</bpt>AppID<ept id="p2">**</ept> 値を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You can find the app ID for your app on the <bpt id="p1">**</bpt>Summary<ept id="p1">**</ept> page in the mobile app designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリ用アプリ ID はモバイル アプリ デザイナー内の <bpt id="p1">**</bpt>概要<ept id="p1">**</ept> ページで見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>App ID in the workspace summary</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース概要のアプリ ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>AppID value in the workspace class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース クラスの AppID 値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Optional: If your workspace is an Application Object Tree (AOT) resource, provide the AOT resource name as the second parameter for the <bpt id="p1">**</bpt>SysAppWorkspaceAttribute<ept id="p1">**</ept> constructor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: ワークスペースがアプリケーション オブジェクト ツリー (AOT) リソースの場合、AOT リソースの名前を <bpt id="p1">**</bpt>SysAppWorkspaceAttribute<ept id="p1">**</ept> コンストラクターの 2 番目のパラメーターとして指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>AOT resource name in the workspace class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース クラスの AOT リソース名。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Use the workspace class to publish workspaces from AOT resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT リソースからワークスペースを発行するには、workspace クラスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Workspaces can reside in the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースはデータベース内に配置することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>They can also reside in the AOT as resources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リソースとして AOT に常駐することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>To provide visibility into workspaces that are stored in AOT resources, you must create a workspace class and point it to the name of the AOT resource that contains the workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT リソースに格納されているワークスペースを可視化するには、ワークスペース・クラスを作成し、そのワークスペースを含む AOT リソースの名前をポイントする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Workspaces that are stored as AOT resources can't be edited or deleted by using the mobile app designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT リソースとして保管されているワークスペースは、モバイル アプリ デザイナーを使用して編集または削除することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Those workspace can only be exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのワークスペースはエクスポートのみ可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Follow these steps to publish a workspace that resides in an AOT resource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT リソースとして存在するワークスペースを公開するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>When you're developing a workspace that is stored in the database, you must export it from the mobile app designer so that it can be stored as an AOT resource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースに格納されるワークスペースを作成するとき、AOT リソースとして保存できるように、それをモバイル アプリ デザイナーからエクスポートする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The workspace is exported as an XML file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースは XML ファイル形式でエクスポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Export a workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースをエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Delete the workspace from the mobile app designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリのデザイナーからワークスペースを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>You will load it from an AOT resource later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それを後で AOT リソースから読み込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Delete a workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Create a new AOT resource, and select the exported workspace for the resource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい AOT リソースを作成し、リソースのエクスポートされたワークスペースを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Workspace as resource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リソースとしてのワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Create a new class for your workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース用の新しいクラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>This class should extend <bpt id="p1">**</bpt>SysAppWorkspace<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスは、<bpt id="p1">**</bpt>SysAppWorkspace<ept id="p1">**</ept> を拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Apply the <bpt id="p1">**</bpt>SysAppWorkspaceAttribute<ept id="p1">**</ept> attribute to the class, and provide the app ID and the AOT resource name that contains the resource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysAppWorkspaceAttribute<ept id="p1">**</ept> 属性をクラスに適用し、リソースを含むアプリ ID と AOT リソース名を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>New workspace class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいワークスペース クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Build the class, and reopen the mobile app designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスをビルドして、モバイル アプリ デザイナーを再オープンします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The workspace is now published.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースが公開されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>It appears in the designer, but can't be edited or deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これはデザイナーに表示されますが、編集または削除できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Note that the workspace is loaded from metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースがメタデータから読み込まれることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Workspace in metadata</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ内のワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Update a workspace that has already been published</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発行済みワークスペースの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>If your workspace is part of an AOT resource, you can't edit it by using the mobile app designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースが AOT リソースの一部である場合、モバイル アプリ デザイナーを使用して編集することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>In the following example, a workspace that is named <bpt id="p1">**</bpt>MyWorkspace<ept id="p1">**</ept> exists in the AOT, and it has a backing class that is named <bpt id="p2">**</bpt>WorkspaceInAOT<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>MyWorkspace<ept id="p1">**</ept> というワークスペースが AOT に存在し、そこには <bpt id="p2">**</bpt>WorkspaceInAOT<ept id="p2">**</ept> というバッキング クラスがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Workspace in the AOT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT 内のワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Workspace in the AOT and published</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT 内にある公開済みのワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Follow these steps to edit the workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースを編集するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Export the workspace by using the mobile app designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリ デザイナーを使用して、ワークスペースをエキスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The designer automatically creates new app IDs for workspaces that are stored in the AOT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーは、AOT に保存されているワークスペースの新しいアプリ ID を自動的に作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Import the newly exported workspace by using the mobile app designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリ デザイナーを使用して、新しくエクスポートされたワークスペースをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Optional: Change the name so that the newly added workspace can be distinguished from other workspaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: 名前を変更します。新たに追加されたワークスペースを他のワークスペースと区別できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Copy the app ID of the newly created workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しく作成したワークスペースのアプリ ID をコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>New workspace in database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの新しいワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>New workspace details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいワークスペースの詳細</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Create a new class that extends your backing class, apply the <bpt id="p1">**</bpt>SysAppWorkspaceAttribute<ept id="p1">**</ept> attribute, and specify the new app ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッキング クラスを拡張し、<bpt id="p1">**</bpt>SysAppWorkspaceAttribute<ept id="p1">**</ept> 属性を適用し、新しいアプリ ID を指定する新しいクラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Workspace in metadata</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ内のワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>You can now continue to work with your new workspace and the backing class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいワークスペースおよびバッキング クラスでの作業を続行することができるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>After you've finished making your changes, you can merge them with the AOT-based workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を行なった後、AOT ベース ワークスペースとそれらをマージできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Delete a workspace that is an AOT resource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT リソースであるワークスペースの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>When a mobile workspace is stored as an AOT resource, you can't delete it by using the mobile app designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル ワークスペースが AOT リソースとして格納されている場合は、それをモバイル アプリ デザイナーを使用して削除することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Follow these steps to delete a workspace that exists as an AOT resource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT リソースとして存在するワークスペースを削除するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Delete the AOT resource that contains the workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースを含む AOT リソースを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Workspace to delete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除するワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Delete the workspace class that was created for the workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース用に作成されたワークスペース クラスを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Workspace class to delete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除するワークスペース クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Do a full model build that contains the AOT resource and the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT リソースおよびクラスを含む完全なモデル ビルドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The following illustrations shows a full build of the Application Foundation model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、アプリケーション基準モデルの完全なビルドを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>The Application Foundation model also contains the AOT resource and workspace class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション基盤モデルには、AOT リソースとワークスペース クラスも含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>To speed up the full build, you can clear all the selections on the <bpt id="p1">**</bpt>Options<ept id="p1">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フルビルドをスピードアップするには、<bpt id="p1">**</bpt>オプション<ept id="p1">**</ept> タブですべての選択をクリアします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Full build menu item</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全なビルド メニュー項目</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Full build</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全なビルド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>When the build is completed, reopen the mobile app designer, and verify that the workspace is no longer there.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドが完了したら、モバイル アプリ デザイナーを再オープンして、ワークスペースが存在しないことを確認します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
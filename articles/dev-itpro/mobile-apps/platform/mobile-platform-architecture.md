<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="mobile-platform-architecture.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>mobile-platform-architecture.f2cd1d.a007b7e50436a6dd223633707d7e4f6fc420e510.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>a007b7e50436a6dd223633707d7e4f6fc420e510</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\mobile-apps\platform\mobile-platform-architecture.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Architecture and design considerations for the mobile platform</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル プラットフォームのアーキテクチャと設計の考慮事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides in-depth information on designing mobile apps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、モバイル アプリの設計に関する詳細な情報を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Architecture and design considerations for the mobile platform</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル プラットフォームのアーキテクチャと設計の考慮事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>The mobile app communicates with Application Object Server (AOS) to get the metadata for the mobile workspaces (and the pages and the fields that appear on the page), and to get the data for the fields on the pages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリは、モバイル ワークスペース (およびページに表示されるページとフィールド) のメタデータを取得し、ページのフィールドのデータを取得するために Application Object Server (AOS) と通信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Each time that the mobile app requests data for a page, AOS creates a new session that uses the context of the user who is using the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリがページのデータを要求するたびに、AOS では、モバイル アプリを使うユーザーのコンテキストで使用している新しいセッションを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>AOS then uses the user's context to open the corresponding forms (by using the corresponding menu items).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOSは、次にユーザーのコンテキストを使用して、対応するフォーム (対応するメニュー項目を使用) を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>AOS can open multiple forms in quick succession and perform actions on those forms (for example, filtering, opening FactBoxes, changing tab pages, and clicking buttons).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS は、すばやく連続して複数のフォームを開くことができ、それらのフォーム (フィルター処理、情報ボックスを開く、タブ ページの変更、ボタンのクリック) に対してアクションを実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Any business logic on the forms is also run as usual.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム上のビジネス ロジックも通常どおり実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Through that process, AOS collects the data values from the requested fields and then sends that data back to the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのプロセスを通じて AOS は要求されたフィールドからデータ値を収集し、そのデータをモバイル アプリに送り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Mobile architecture</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アーキテクチャ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The mobile app platform doesn't assume connectivity to Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリ プラットフォームは、Finance and Operations への接続を想定していません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Activities such as navigation, data view, and data entry don't require server connectivity after data has been cached.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション、データの表示、データ入力などの活動は、データがキャッシュされた後にサーバー接続の必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Understanding navigation in the mobile app</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリでのナビゲーションを理解する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Navigation in the mobile app consists of four simple concepts: the dashboard, workspaces, pages, and actions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリのナビゲーションは、ダッシュボード、ワークスペース、ページ、およびアクションという 4 つの簡単な概念で構成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Navigation concepts in the mobile app</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリのナビゲーション概念</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>When you start the app, you land on the <bpt id="p1">**</bpt>dashboard<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリを起動すると、<bpt id="p1">**</bpt>ダッシュボード<ept id="p1">**</ept> が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>On the <bpt id="p1">**</bpt>dashboard<ept id="p1">**</ept>, you can see a list of <bpt id="p2">**</bpt>workspaces<ept id="p2">**</ept> that are published in your Finance and Operations environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ダッシュボード<ept id="p1">**</ept>には、Finance and Operations 環境で公開されている<bpt id="p2">**</bpt>ワークスペース<ept id="p2">**</ept>の一覧が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>In each <bpt id="p1">**</bpt>workspace<ept id="p1">**</ept>, you can see a list of <bpt id="p2">**</bpt>pages<ept id="p2">**</ept> that are available for that workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各<bpt id="p1">**</bpt>ワークスペース<ept id="p1">**</ept>では、そのワークスペースで使用可能な<bpt id="p2">**</bpt>ページ<ept id="p2">**</ept>の一覧が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>On a <bpt id="p1">**</bpt>page<ept id="p1">**</ept>, you can view data that is collected from one or more Finance and Operations forms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ページ<ept id="p1">**</ept>では、1 ページ以上の Finance and Operations のホームから収集されたデータを表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>From a <bpt id="p1">**</bpt>page<ept id="p1">**</ept>, you can navigate to other <bpt id="p2">**</bpt>pages<ept id="p2">**</ept> for related data, such as an entity details or lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ページ<ept id="p1">**</ept>からは、エンティティの詳細または明細行などの、関連データの他の<bpt id="p2">**</bpt>ページ<ept id="p2">**</ept>に移動することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>On a <bpt id="p1">**</bpt>page<ept id="p1">**</ept>, you can see a list of <bpt id="p2">**</bpt>actions<ept id="p2">**</ept> that are available for that page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ページ<ept id="p1">**</ept>では、そのページで使用可能な<bpt id="p2">**</bpt>アクション<ept id="p2">**</ept>のリストが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Actions<ept id="p1">**</ept> let you create or edit existing data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アクション<ept id="p1">**</ept> 既存のデータを作成または編集できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Notes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">摘要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>At any time, you can pull-to-refresh in the mobile app to make the mobile app update its data or metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリでデータやメタデータを更新するために、いつでもモバイル アプリでプルして更新することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>After you edit an existing workspace or publish a workspace, be sure to pull-to-refresh in the mobile app, in either the list of workspaces (if you added a workspace or business logic) or the list of pages (if you modified a page or an action).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のワークスペースを編集またはワークスペースを発行した後、モバイル アプリ、ワークスペースのリスト (ワークスペースまたはビジネス ロジックを追加した場合) またはページのリスト (アクションおよびページ修正された) で、プルリフレッシュしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Workspaces that have been published to Finance and Operations are visible to all users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations に対して公開済みのワークスペースはすべてのユーザーに対して表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>In Microsoft Dynamics 365 for Finance and Operations platform update 3, menu item security automatically hides pages that the user doesn’t have access to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operationsプラットフォームの更新プログラム 3 では、メニュー項目のセキュリティにより、ユーザーにアクセス権がないページは自動的に非表示になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>If a user doesn’t have access to any pages in a workspace, the workspace itself is hidden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースの任意のページへのへのアクセス権がユーザーにない場合、ワークスペース自体が非表示になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Using the mobile app designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリ デザイナーの使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The mobile app designer lets you select the specific data fields from forms that should appear in the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリ デザイナーでは、モバイル アプリに表示されるフォームから特定のデータ フィールドを選択できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>A mobile workspace can be created through designer, using X++ attribute APIs or a combination of both. See <bpt id="p2">[</bpt>Workspace class overview<ept id="p2">](scenarios/mobile-workspace-configuration.md)</ept> for more details on using X++ APIs for building a mobile workspace.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モバイル ワークスペースは、デザイナーを通じて、X++ 属性 API、またはその両方の組み合わせを使用して作成することができます。モバイルワークスペースの構築に X++ API を使用する方法の詳細については<ept id="p1">**</ept>、<bpt id="p2">[</bpt>ワークスペース クラスの概要<ept id="p2">](scenarios/mobile-workspace-configuration.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Mobile app designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリ デザイナー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Open the Finance and Operations client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations クライアントを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Go to <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Mobile app<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>モバイル アプリ<ept id="p2">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Create a new workspace, or select an existing workspace to edit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいワークスペースを作成するか、編集する既存のワークスペースを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Specify the name of the workspace, an icon, and a color.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース、アイコン、および色の名前を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Add pages to the workspace, or edit an existing page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースにページを追加するか、既存のページを編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Specify the name of the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの名前を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Click <bpt id="p1">**</bpt>Select Fields<ept id="p1">**</ept> to select the data fields to add to the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールドの選択<ept id="p1">**</ept>をクリックし、ページに追加するデータ フィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Open the forms that have the data fields that you want to add, and then click the yellow plus sign (+) that appears next to the fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加するデータ フィールドのあるフォームを開いて、フィールドの横に表示される黄色のプラス記号 (+) をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The fields are added in the order that you select them in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドは、選択した順序で追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>You can add fields from multiple forms, in any order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数のフォームから、任意の順序で、フィールドを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>When you've finished selecting fields, click <bpt id="p1">**</bpt>Done<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドの選択を完了したら、<bpt id="p1">**</bpt>完了<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you've added a field list to the page, you will see that the <bpt id="p1">**</bpt>List<ept id="p1">**</ept> type is specified for one of the items in the field list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド リストをページに追加した場合、<bpt id="p1">**</bpt>リスト<ept id="p1">**</ept> タイプがフィールド リスト内の項目のいずれかに指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>You can optionally add a details page for items in that list by following these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の手順に従い、必要に応じてそのリストに品目の詳細ページを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Select the list by clicking on it in the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーでクリックしてリストを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Click <bpt id="p1">**</bpt>Add details page<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>詳細ページの追加<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Repeat steps 6 through 10 as you require.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、手順 6 ～ 10 を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Refreshing the app after you make changes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更が完了したら、アプリを更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Type of change</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更のタイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>New workspaces, deleted workspaces, or changes to the name, color, or icon of a workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいワークスペース、削除されたワークスペース、またはワークスペースの名前、色、またはアイコンへの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Pull-to-refresh from the main landing page (dashboard) of the app, where you see the list of workspaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースの一覧が表示される、アプリの主要なランディング ページ (ダッシュボード) からプルして更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Pull-to-refresh from the dashboard</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダッシュボードからプルして更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>All other changes (new or changed pages or actions, or changes to business logic)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のすべての変更 (新しいまたは変更されたページまたはアクション、またはビジネス ロジックへ変更)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Pull-to-refresh from the workspace that has the edited pages or actions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">編集されたページまたはアクションを持つワークスペースからプルして更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Pull-to-refresh from a workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースからプルして更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">[</bpt>Page design guidelines<ept id="p1">](page-design-guidelines.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ページ デザインのガイドライン<ept id="p1">](page-design-guidelines.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">[</bpt>Action design guidelines<ept id="p1">](action-design-guidelines.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>アクション デザインのガイドライン<ept id="p1">](action-design-guidelines.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">[</bpt>Form design requirements<ept id="p1">](form-design-requirements.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>フォーム デザインの要件<ept id="p1">](form-design-requirements.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
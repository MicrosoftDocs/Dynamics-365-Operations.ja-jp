<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="secure-analytical-workspaces.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>secure-analytical-workspaces.91cf27.5ad0ad81f8cbf9c79559572e41da8edcbe3aea64.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>5ad0ad81f8cbf9c79559572e41da8edcbe3aea64</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\secure-analytical-workspaces.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Help secure analytical workspaces and reports by using Power BI Embedded</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI Embedded を使用して分析ワークスペースおよびレポートをセキュリティで保護</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the recommended strategies for securing access to both the reports that are delivered by using Power BI Embedded and the data set, based on viewer access rights.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Power BI Embedded を使用して提供されるレポートと、ビューアーのアクセス権に基づいてデータ セットへのアクセスを保護するための推奨方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Help secure analytical workspaces and reports by using Power BI Embedded</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI Embedded を使用して分析ワークスペースおよびレポートをセキュリティで保護</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This feature is supported in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) (version 7.2) and later releases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、Microsoft Dynamics 365 for Finance and Operations、Enterprise edition (2017年7月) (バージョン7.2) 以降のリリースでサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Introduction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">はじめに</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic provides a walk-through for application developers who want to help secure analytical workspaces and reports that are delivered by using Microsoft Power BI Embedded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Power BI Embedded を使用して提供される、分析ワークスペースとレポートのセキュリティ保護を支援するアプリケーション開発者向けにウォークスルーを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>It describes the recommended strategies for securing access to both the reports and the data set, based on viewer access rights.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビューアーのアクセス権に基づいてレポートおよびデータ セット両方へのアクセスを保護するための推奨方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>By using the techniques that are described in this topic, you can hide reports from users and filter reports to show the data set that is appropriate for a specific user, based on the active company context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックに記載されている手法を使用することにより、ユーザーからレポートを非表示にし、有効な会社のコンテキストに基づいて、特定のユーザーに適したデータ セットを表示するためにレポートをフィルター処理することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Access to a developer environment that runs Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 with Platform update 8 or later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition プラットフォーム更新プログラム 8 (2017年7月) 以降で実行する開発者環境にアクセスします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Power BI Desktop を使用して作成され、エンティティ格納 データベースから取得されたデータ モデルを持つ分析レポート (.pbix ファイル) です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Whether you're extending an existing application workspace or adding your own workspace, you can use embedded analytical views to deliver insightful and interactive views of your business data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のアプリケーション ワークスペースを拡張する場合でも、自身のワークスペースを追加する場合でも、埋め込み分析ビューを使用して、ビジネス データの洞察的でインタラクティブなビューを提供できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Before you add new analytical workspaces and reports, it's important that you establish a strategy to help secure the content.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい分析ワークスペースおよびレポートを追加する前に、コンテンツを保護するための戦略を確立することは重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>There are several considerations that you should be aware of when you develop analytical solutions by using Power BI Embedded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI Embedded を使用して分析ソリューションを開発する際には、いくつか注意すべき点があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Analytical reports are secured by using menu items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析レポートはメニュー項目を使用して保護されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>After they have access to a report, all viewers can access the underlying data model that is defined in the report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートにアクセスすると、すべての閲覧者はレポートに定義されている基礎データ モデルにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Although service options are available that automatically hide the fields that back a report data set, all viewers of the report have effective access to the fields in the data model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス オプションはレポート データ セットを戻しフィールドを自動的に非表示にすることが可能ですが、レポートのすべての閲覧者はデータ モデル内のフィールドに有効的にアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Additionally, X++ extensions are available that influence the way that the report is presented in the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、レポートがクライアントに表示される方法に影響を与える X++ 拡張機能が使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Both the <bpt id="p1">**</bpt>Filter<ept id="p1">**</ept> pane and the <bpt id="p2">**</bpt>Report<ept id="p2">**</ept> tabs can be hidden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィルター<ept id="p1">**</ept> ウィンドウと<bpt id="p2">**</bpt>レポート<ept id="p2">**</ept> タブの両方を非表示にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>However, Microsoft Power BI filters can be modified by using client-side script injections.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、Microsoft Power BI フィルターは、クライアント側スクリプト インジェクションを使用して変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Recommendation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">推奨事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Create scenario-specific .pbix files to deliver analytical views:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオ固有の .pbix ファイルを作成して分析ビューを作成する:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Area overviews that are delivered by using workspaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースを使用して提供される領域の概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Subject matter–specific analytical reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">題材固有の分析レポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>These analytical reports are often used to deliver reports that contain medium-business-impact and high-business-impact data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの分析レポートは、中堅企業や大規模企業に影響を与えるデータを含むレポートを配信するために使用されることがよくあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For more information about how to create analytical reports, see <bpt id="p1">[</bpt>Getting started with Power BI Desktop<ept id="p1">](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析レポートを作成する方法の詳細については、<bpt id="p1">[</bpt>Power BI Desktop の使い方<ept id="p1">](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>This page is a great source for insights that can help you create compelling analytical reporting solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このページは、魅力的な分析レポート作成ソリューションの作成に役立つ素晴らしいソースです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Help secure analytical views that are provided through embedded Power BI reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">埋め込み Power BI レポートを通して提供される分析ビューのセキュリティを強化する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Power BI report filters and the <bpt id="p1">**</bpt>Filter<ept id="p1">**</ept> pane serve as a mechanism for passing session context into the report that is embedded on the <bpt id="p2">**</bpt>Analytics<ept id="p2">**</ept> tab. The capability to turn the visibility of the <bpt id="p3">**</bpt>Filter<ept id="p3">**</ept> pane on and off isn't a security feature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI レポート フィルターと <bpt id="p1">**</bpt>フィルター<ept id="p1">**</ept> ウィンドウは、<bpt id="p2">**</bpt>分析<ept id="p2">**</ept> タブに埋め込まれたレポートにセッション コンテキストを渡すためのメカニズムとして機能します。<bpt id="p3">**</bpt>フィルター<ept id="p3">**</ept> ウィンドウの表示のオンとオフを切り替える機能は、セキュリティ機能ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Power BI report filters and the capability to hide and show the <bpt id="p1">**</bpt>Filter<ept id="p1">**</ept> pane are user experience (UX) decisions that the application designer makes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI レポート フィルターと、<bpt id="p1">**</bpt>フィルター<ept id="p1">**</ept> ウィンドウを非表示および表示する機能は、アプリケーション デザイナーが行うユーザー エクスペリエンス (UX) の決定です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Row-level security that is defined in Finance and Operations isn't inherited by Power BI reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations で定義されている行レベルのセキュリティは Power BI レポートによって継承されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Instead, application developers can help secure the workspace or the report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、アプリケーション開発者は、ワークスペースまたはレポートのセキュリティを高めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Help secure analytical workspaces on the Analytics tab</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析タブの分析ワークスペースのセキュリティを強化する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Analytical workspaces are embedded Power BI reports that are shown in a form control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析ワークスペースはフォーム コントロールに表示される埋め込まれた Power BI レポートです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Unless you complete the following procedure, anyone who has access to the workspace can see the <bpt id="p1">**</bpt>Analytics<ept id="p1">**</ept> tab and access the Power BI reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順を完了しない限り、ワークスペースにアクセスできるすべてのユーザーには <bpt id="p1">**</bpt>分析<ept id="p1">**</ept> タブが表示され、Power BI レポートにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Add a menu item for the analytical workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析ワークスペースのメニュー項目を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Verify that the form initialization uses the <bpt id="p1">**</bpt>hasMenuItemAccess<ept id="p1">**</ept> application programming interface (API) to verify that the user has access to the menu item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがメニュー項目にアクセスできることを確認するために、フォームの初期化に <bpt id="p1">**</bpt>hasMenuItemAccess<ept id="p1">**</ept> アプリケーション プログラミング インターフェイス (API) が使用されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The preceding logic will prevent the Power BI Viewer control from being initialized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記のロジックは、Power BI ビューアー コントロールの初期化を阻止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Therefore, an empty tab will appear on the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、空のタブがページに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>By default, the framework automatically hides empty tabs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、フレームワークは自動的に空のタブを非表示にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Therefore, the <bpt id="p1">**</bpt>Analytics<ept id="p1">**</ept> tab is hidden and can't be access if the user doesn't have access to the menu item that is associated with the analytical workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p1">**</bpt>分析<ept id="p1">**</ept> タブは非表示になっており、ユーザーが分析ワークスペースに関連付けられているメニュー項目へのアクセス権を持たない場合はアクセスできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Help secure analytical reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析レポートのセキュリティを強化する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Embedded Power BI reports in the application are secured by using menu items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの埋め込み Power BI レポートは、メニュー項目を使用してセキュリティで保護されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Users who try to access a Power BI report directly, by using a menu item in Finance and Operations, will receive an error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations メニュー項目を使用して Power BI レポートに直接アクセスを試みるユーザーに、エラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Follow these steps to help secure the analytical reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析レポートのセキュリティを確保するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Add a menu item for the report or the appropriate tab. By default, the first tab of the report will be shown if no other tab is selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートまたは適切なタブのメニュー項目を追加します。既定では、その他のタブが選択されていない場合、レポートの最初のタブが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Link the menu item to the <bpt id="p1">**</bpt>PowerBIEmbedded<ph id="ph1">\_</ph>App<ept id="p1">**</ept> configuration key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニュー項目を <bpt id="p1">**</bpt>PowerBIEmbedded<ph id="ph1">\_</ph>App<ept id="p1">**</ept> コンフィギュレーション キーにリンクします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Link the menu item to the PowerBIEmbedded_App configuration key</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニュー項目の PowerBIEmbedded_App コンフィギュレーション キーへのリンク</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The menu item is now associated with the availability of the Power BI Embedded service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメニュー項目は、Power BI Embedded サービスの可用性に関連付けられています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>If the service is unavailable, the links for the menu items will be removed from the application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービスを使用できない場合は、アプリケーションからメニュー項目のリンクが削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Help secure analytical workspaces and reports by company</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社ごとの分析ワークスペースおよびレポートのセキュリティを強化する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Power BI workspaces and reports can be secured by company (for example, <bpt id="p1">**</bpt>DataAreaID<ept id="p1">**</ept> value).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI ワークスペースとレポートは会社が保護できます (たとえば、<bpt id="p1">**</bpt>DataAreaID<ept id="p1">**</ept> 値など)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Application solutions must apply the following steps for company-level security in analytical workspaces and reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション ソリューションは、分析ワークスペースとレポートで会社レベルのセキュリティのために、次の手順を適用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In this scenario, the workspaces and reports that the sales manager from Contoso USA sees are limited to data that is related to Contoso USA.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオでは、Contoso USA の販売マネージャーが確認するワークスペースとレポートは、Contoso USA に関連するデータに限定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The report viewer must not have access to data that associated with any other company, unless the company context is changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート ビューアーは、会社のコンテキストが変更されない限り、他の会社に関連付けられたデータにアクセスできないようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Open the analytical report in Power BI Desktop by double-clicking the resource in a Microsoft Visual Studio project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio プロジェクト内のリソースをダブルクリックして、Power BI Desktop で分析レポートを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>On the <bpt id="p1">**</bpt>Modeling<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>Manage Roles<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデリング<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>ロールの管理<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Create a new role against a column in the data model that contains the <bpt id="p1">**</bpt>Company<ept id="p1">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>会社<ept id="p1">**</ept>フィールドを含むデータ モデル内の列に対して新しいロールを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Name the new role <bpt id="p1">**</bpt>CompanyFilter<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいロールに <bpt id="p1">**</bpt>CompanyFilter<ept id="p1">**</ept> と名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>A <bpt id="p1">**</bpt>COMPANY<ept id="p1">**</ept> field must be present in the data model to restrict access by company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社によるアクセスを制限するために、データ モデルに<bpt id="p1">**</bpt>会社<ept id="p1">**</ept>フィールドが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Create a new role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいロールの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>In the <bpt id="p1">**</bpt>Table filter DAX expression<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt><ph id="ph1">\[</ph>COMPANY<ph id="ph2">\]</ph>=username()<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル フィルターの DAX 式<ept id="p1">**</ept>フィールドに、<bpt id="p2">**</bpt><ph id="ph1">\[</ph>COMPANY<ph id="ph2">\]</ph>=username()<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>To make sure that the rules work, on the <bpt id="p1">**</bpt>Modeling<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>View as Roles<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールが機能することを確認するには、<bpt id="p1">**</bpt>モデリング<ept id="p1">**</ept> タブで <bpt id="p2">**</bpt>ロールとして表示<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>In the dialog box, set the following fields:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで、次のフィールドを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Clear the <bpt id="p1">**</bpt>None<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>なし<ept id="p1">**</ept>チェック ボックスをオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Select the <bpt id="p1">**</bpt>Other user<ept id="p1">**</ept> check box, and then enter <bpt id="p2">**</bpt>USMF<ept id="p2">**</ept> in the text box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>その他のユーザー<ept id="p1">**</ept> チェック ボックスをオンにし、テキスト ボックスに <bpt id="p2">**</bpt>USMF<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Select the <bpt id="p1">**</bpt>CompanyFilter<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CompanyFilter<ept id="p1">**</ept> チェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The reports will now show data as if you're running the USMF company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これでレポートに、USMF 企業を経営しているかのようなデータが表示されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
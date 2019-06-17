<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="in-memory-real-time-aggregate-models.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>in-memory-real-time-aggregate-models.d30baf.fc2b87eacafcf65a439bbe79eb561b1203ff3538.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>fc2b87eacafcf65a439bbe79eb561b1203ff3538</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\in-memory-real-time-aggregate-models.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Transition from Analysis Services cubes to aggregate models</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Analysis Services キューブから集計モデルへの移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article explains how Dynamics 365 for Finance and Operations has transitioned from using SQL Server Analysis Services (SSAS) cubes to in-memory, real-time aggregate models for analytics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Dynamics 365 for Finance and Operations でどのように分析に SQL Server Analysis Services (SSAS) キューブではなく、インメモリ、リアルタイム集計モデルが使用されるようになったかを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Transition from Analysis Services cubes to aggregate models</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Analysis Services キューブから集計モデルへの移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article explains how Microsoft Dynamics 365 for Finance and Operations has transitioned from using SQL Server Analysis Services (SSAS) cubes to in-memory, real-time aggregate models for analytics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Microsoft Dynamics 365 for Finance and Operations でどのように分析に SQL Server Analysis Services (SSAS) キューブではなく、インメモリ、リアルタイム集計モデルが使用されるようになったかを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The world is moving to real-time, proactive analytics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">世界は、リアルタイムの積極的な分析に移行しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Reporting and trending on historical data is being replaced by up-to-the-second visualizations and proactive guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">履歴データのレポートとトレンドは、最新の視覚化およびプロアクティブ ガイダンスにより置き換えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In-memory, real-time aggregate models now replace the perspectives that were previously used for analytics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メモリ内でのリアルタイムな集計モデルにより、分析に以前使用された分析視点が置換されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>A historical look at perspectives and cubes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析視点とキューブの履歴</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>We envision embedded insights playing a key role in the Microsoft Dynamics 365 for Finance and Operations user experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations のユーザー エクスペリエンスで重要な役割を果たす埋め込みインサイトを想定しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This vision has driven us to invest in building analytic capabilities within the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このビジョンにより、製品内に分析機能を構築するための投資が行われました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In Dynamics AX 4.0, we introduced the concept of <bpt id="p1">*</bpt>perspectives<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 4.0 では、<bpt id="p1">*</bpt>分析視点<ept id="p1">*</ept>の概念を導入しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The objective was to present a simpler view of the ERP schema, specifically modeled for reporting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的は、特にレポートのためにモデル化された、ERP スキーマのより簡単なビューを提示することでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This simpler view was referred to as perspectives.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このより単純なビューは、分析視点と呼ばれていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>In Dynamics AX 4.0, the system generated reporting models (SMDL models) that enabled you to create ad-hoc reports with SQL Server Report Builder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 4.0 では、システムが、SQL Server レポート ビルダーでアドホック レポートを作成できるレポート モデル (SMDL モデル) を生成していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In Dynamics AX 2009, we added the capability to generate SQL Server Analysis Services (SSAS) projects using metadata definitions in perspectives.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2009 では、分析視点でメタデータ定義を使用して、SQL Server Analysis Services (SSAS) プロジェクトを生成する機能を追加しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>These projects become cubes when deployed to an SSAS server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのプロジェクトは、SSAS サーバーに展開するとキューブになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In Dynamics AX 2012, we improved modeling in perspectives and improved tooling support for managing the lifecycle of SSAS projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 では、分析視点でのモデリングと、SSAS プロジェクトのライフ サイクルを管理するためのツール サポートが向上しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>You could use Excel, as well as Power View, to explore data and create reports with cubes in Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データを参照し、Dynamics AX 2012 のキューブでレポートを作成するには、Excel のほか Power View も使用することができました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The SMDL technology was also deprecated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SMDL テクノロジも使用されなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In Dynamics AX 2012, we stopped generating SMDL models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 では、SMDL モデルを生成しなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>How perspectives are used now</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在分析視点がどのように使用されているか</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>As a developer, your “contract” with the system was a perspective.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者として、システムとの「契約」は視点でした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The system generated “stuff” to help you achieve your end goal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムは、最終目標を達成するのに役立つ「もの」を生み出しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>In Dynamics AX 2012, the "stuff” that was generated was SSAS projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 では、生成された "もの" は SSAS プロジェクトでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>So the contract between you (the  developer) and the system (the BI framework), was as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、あなた (開発者) とシステム (BI フレームワーク) の間の契約は次のとおりでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>You modeled perspectives.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析視点をモデル化しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The system generated the "stuff" needed to enable you to build visuals and reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムは、ビジュアルとレポートを作成するために必要な「もの」を生成しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Perspectives are now modeled using Finance and Operations add-ins for Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析視点は、Visual Studio の Finance and Operations アドインを使ってモデル化されるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>(Visual Studio is now the development environment.) Perspectives are comprised of <bpt id="p1">*</bpt>aggregate measurements<ept id="p1">*</ept> and <bpt id="p2">*</bpt>aggregate dimensions<ept id="p2">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Visual Studio は開発環境になっています。) 分析視点は<bpt id="p1">*</bpt>集計の測定<ept id="p1">*</ept>および<bpt id="p2">*</bpt>集計分析コード<ept id="p2">*</ept>から構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>As a developer, you have the ability to model simpler schemas for answering business questions using aggregate measurements and aggregate dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は、集計の測定と集計分析コードを使用して業務質問に答えるための簡単なスキーマをモデル化することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Aggregate measurements can be used to define data entities (called <bpt id="p1">*</bpt>aggregate data entities<ept id="p1">*</ept>) which can be directly bound to Finance and Operations forms as a data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計測定は Finance and Operations フォームにデータ ソースとして直接バインドできるデータ エンティティ (<bpt id="p1">*</bpt>集計データ エンティティ<ept id="p1">*</ept>と呼ばれる) を定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Aggregate data entities can also be used to</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計データ エンティティは に使用することもできます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Expose data to PowerBI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PowerBI にデータを公開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Access data programmatically using the AXQuery object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXQuery オブジェクトを使用してプログラムでデータにアクセス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>how-perspectives-are-used<ept id="p1">](./media/how-perspectives-are-used.png)](./media/how-perspectives-are-used.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>how-perspectives-are-used<ept id="p1">](./media/how-perspectives-are-used.png)](./media/how-perspectives-are-used.png)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
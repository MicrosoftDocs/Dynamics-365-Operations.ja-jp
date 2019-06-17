<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="code-migration-lcs-solutions.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>code-migration-lcs-solutions.b3bdac.f686e9a6da796739b3e73b14007c3a7bd16b0a8a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>f686e9a6da796739b3e73b14007c3a7bd16b0a8a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lcs-solutions\code-migration-lcs-solutions.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Migrate code for Finance and Operations solutions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations ソリューションのコードの移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to upgrade and analyze your code in Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) で、コードをアップグレードおよび分析する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Migrate code for Finance and Operations solutions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations ソリューションのコードの移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>To complete your solution package, the first step is to upgrade your code by using the best practices in <bpt id="p1">**</bpt>Migrate and Create Finance and Operations Solutions<ept id="p1">**</ept> in Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション パッケージを完成させるための第一歩は、Microsoft Dynamics Lifecycle Services (LCS) の <bpt id="p1">**</bpt>Finance and Operations ソリューションの移行と作成<ept id="p1">**</ept>のベスト プラクティスを使用してコードをアップグレードすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>After that step is completed, you must run the Customization Analysis Report (CAR).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップが完了したら、カスタマイズ分析のレポート (CAR) を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This report analyzes your customization and extension models, and runs a predefined set of best practice rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このレポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>To generate the CAR, run the following command on a Microsoft Dynamics 365 for Finance and Operations development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CAR を生成するには、Microsoft Dynamics 365 for Finance and Operations 開発環境で次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Here is an example of this command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドの例を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The xppbp.exe file is located in c:<ph id="ph1">\\</ph>packages<ph id="ph2">\\</ph>bin or I:<ph id="ph3">\\</ph>AosService<ph id="ph4">\\</ph>Packages<ph id="ph5">\\</ph>LocalDirectory<ph id="ph6">\\</ph>bin.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">xppbp.exe ファイルは、c:<ph id="ph1">\\</ph>packages<ph id="ph2">\\</ph>bin または I:<ph id="ph3">\\</ph>AosService<ph id="ph4">\\</ph>Packages<ph id="ph5">\\</ph>LocalDirectory<ph id="ph6">\\</ph>bin に配置されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You must resolve any warnings or errors that appear on the <bpt id="p1">**</bpt>Issues<ept id="p1">**</ept> tab of the report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートの<bpt id="p1">**</bpt>問題<ept id="p1">**</ept>タブ上に表示される警告またはエラーを解決する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You must then submit a copy of the CAR to Microsoft before your validation meeting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CAR のコピーを、検証ミーティングよりも前に、Microsoft に送信する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>For more information, see <bpt id="p1">[</bpt>Customization Analysis Report<ept id="p1">](../dev-tools/customization-analysis-report.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>カスタマイズ分析のレポート<ept id="p1">](../dev-tools/customization-analysis-report.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For information about issues and exceptions, see the <bpt id="p1">[</bpt>Customization Analysis Report: Exceptions and known issues<ept id="p1">](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues)</ept> post on the Dynamics 365 Community blog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題と例外の詳細については、Dynamics 365 Community ブログの投稿<bpt id="p1">[</bpt>カスタマイズ分析のレポート: 例外と既知の問題<ept id="p1">](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Extensibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In Microsoft Dynamics 365 for Finance and Operations version 8.0 (April 2018), all product models are sealed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operationsバージョン 8.0 (2018年4月) では、すべての製品モデルがシールされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Therefore, only extension-based customizations are currently supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、拡張機能ベースのカスタマイズのみが現在サポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>For more information about extensibility, see <bpt id="p1">[</bpt>Extensibility<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/extensibility-home-page)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の詳細については、<bpt id="p1">[</bpt>拡張機能<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/extensibility-home-page)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The first step in completing your solution package is to upgrade your code using the best practices in <bpt id="p1">&lt;strong&gt;</bpt>Migrate and Create Finance and Operations Solutions<ept id="p1">&lt;/strong&gt;</ept> in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション パッケージを完成させるための第一歩は、LCS の <bpt id="p1">&lt;strong&gt;</bpt>Migrate and Create Finance and Operations Solutions<ept id="p1">&lt;/strong&gt;</ept> のベストプラクティスを使用してコードをアップグレードすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>After this step is complete, you must run the Customization Analysis report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップが完了したら、カスタマイズ分析レポートを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This report analyzes your customization and extension models, and runs a predefined set of best practice rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このレポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>To generate the Customization Analysis report (CAR), run the following command on a Microsoft Dynamics 365 for Finance and Operations development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズ分析レポート (CAR) を生成するには、Microsoft Dynamics 365 for Finance and Operations 開発環境で次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Here's an example of how this command might look.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドの見方の例を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The xppbp.exe file is located in <bpt id="p1">*</bpt>c:\packages\bin<ept id="p1">*</ept> or <bpt id="p2">*</bpt>I:\AosService\Packages\LocalDirectory\bin)<ept id="p2">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">xppbp.exe ファイルは、<bpt id="p1">*</bpt>c:\packages\bin<ept id="p1">*</ept> または <bpt id="p2">*</bpt>I:\AosService\Packages\LocalDirectory\bin)<ept id="p2">*</ept> にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Any warnings or errors that appear on the <bpt id="p1">**</bpt>Issues<ept id="p1">**</ept> tab of the report must be resolved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートの<bpt id="p1">**</bpt>問題<ept id="p1">**</ept>タブ上に表示される警告またはエラーを解決する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>A copy of the CAR report must be submitted to Microsoft prior to your validation meeting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CAR レポートのコピーは、検証ミーティングよりも前に、Microsoft に送信する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For more information, see the Finance and Operations Help topic, <bpt id="p1">[</bpt>Customization Analysis Report<ept id="p1">](../dev-tools/customization-analysis-report.md)</ept> or refer to the <bpt id="p2">[</bpt>Dynamics Community blog<ept id="p2">](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues)</ept> for issues and exceptions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、Finance and Operations ヘルプ トピック、<bpt id="p1">[</bpt>カスタマイズ分析のレポート<ept id="p1">](../dev-tools/customization-analysis-report.md)</ept> および、問題と例外に関する <bpt id="p2">[</bpt>Dynamics コミュニティのブログ<ept id="p2">](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加リソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">[</bpt>Publishing an App for Dynamics 365 for Finance and Operations in AppSource<ept id="p1">](lcs-solutions-app-source.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>AppSource の Dynamics 365 for Finance and Operations アプリを公開<ept id="p1">](lcs-solutions-app-source.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">[</bpt>Technical Concepts Guide for code migration<ept id="p1">](../dev-tools/developer-home-page.md#code-migration)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>コードの移行の技術概念ガイド<ept id="p1">](../dev-tools/developer-home-page.md#code-migration)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
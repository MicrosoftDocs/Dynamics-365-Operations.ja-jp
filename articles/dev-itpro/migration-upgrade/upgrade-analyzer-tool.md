<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="upgrade-analyzer-tool.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>upgrade-analyzer-tool.0766a9.1df1e7cead3c802079bf4faba66b91fc30e3e947.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1df1e7cead3c802079bf4faba66b91fc30e3e947</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\upgrade-analyzer-tool.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Upgrade from AX 2012 - Plan by using the Upgrade analyzer tool</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - アップグレード アナライザー ツールを使用した計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to use the Upgrade analyzer tool to plan upgrade from Dynamics AX 2012 to Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、アップグレード アナライザー ツールを使用して、Dynamics AX2012 から Dynamics 365 for Finance and Operations へのアップグレードを計画する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Upgrade from AX 2012 - Plan by using the Upgrade analyzer tool</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - アップグレード アナライザー ツールを使用した計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to use the Upgrade analyzer tool to plan your upgrade from Microsoft Dynamics AX 2012 to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、アップグレード アナライザー ツールを使用して、Microsoft Dynamics AX 2012 から Microsoft Dynamics 365 for Finance and Operations へのアップグレードを計画する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This tool is run against an AX 2012 environment and identifies data that you should clean up in AX 2012 to help reduce the subscription cost for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールは、AX 2012 環境に対して実行され、 Finance and Operations サブスクリプション コストの削減を助けるために、AX 2012 内でクリーンアップする必要のあるデータを識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The tool also suggests SQL configuration optimizations that can help speed up the upgrade processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールは、アップグレード プロセスのスピードアップに役立つ SQL 構成の最適化を提案します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Additionally, the tool warns you if any features that you use in AX 2012 are obsolete in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、AX 2012 で使用する機能が Finance and Operations で廃止されている場合は、このツールが警告します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Therefore, you can plan ways to replace or work around those features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、これらの機能を置き換える方法や回避する方法を計画できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Upgrade analyzer gathers data from your AX 2012 environment as part of the regular System diagnostic service in Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード アナライザーは、Microsoft Dynamics Lifecycle Services (LCS) の通常のシステム診断サービスの一部として、AX 2012 環境からデータを収集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>For an overview of the System diagnostic service, and for information about how data is collected and pushed back into the cloud so that you can consume it through LCS, see <bpt id="p1">[</bpt>System diagnostics (AX 2012)<ept id="p1">](../lifecycle-services/ax-2012/system-diagnostics-lcs.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム診断サービスの概要、および LCS を通じて使用できるようにデータを収集しクラウドに押し戻す方法に関する情報については、<bpt id="p1">[</bpt>システム診断 (AX 2012)<ept id="p1">](../lifecycle-services/ax-2012/system-diagnostics-lcs.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can view the results of the System diagnostic service in a Microsoft Power BI report in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS の Microsoft Power BI レポートでは、システム診断サービスの結果を表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The report presents a list of tasks that you should complete in the AX 2012 environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートには、AX 2012 環境で完了する必要のあるタスクのリストが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To access the Upgrade analyzer report, go to <ph id="ph1">https://diag.lcs.dynamics.com/UpgradeAnalysisReport/Report/</ph>"ProjectID" (Replace "ProjectID" with your current project ID, which is an integer that can be found in the URL of your current LCS project).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード分析レポートにアクセスするには、<ph id="ph1">https://diag.lcs.dynamics.com/UpgradeAnalysisReport/Report/</ph>"ProjectID" に移動します ("ProjectID" を現在のプロジェクト ID で置き換えます。これは現在の LCS プロジェクトの URL にある整数です)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The following illustration shows an overview of the procedure for using Upgrade analyzer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、アップグレード アナライザーを使用する手順の概要を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Upgrade analyzer process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アナライザー プロセスのアップグレード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>If you already use the System diagnostic service in your AX 2012 environment, you must configure a new instance of the service on a machine that differs from the existing machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 環境内のシステム診断サービスを既に使用している場合は、既存のコンピューターとは異なるコンピューターで、サービスの新しいインスタンスをコンフィギュレーションする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>For information about how to configure the System diagnostic service in your AX 2012 environment, see <bpt id="p1">[</bpt>Install and run System diagnostics (AX 2012)<ept id="p1">](../lifecycle-services/ax-2012/install-run-system-diagnostics-lcs.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 環境内のシステム診断サービスをコンフィギュレーションする方法の詳細については、<bpt id="p1">[</bpt>システム診断のインストールと実行 (AX 2012)<ept id="p1">](../lifecycle-services/ax-2012/install-run-system-diagnostics-lcs.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Within a few minutes after you configure the System diagnostic service, the AX 2012 environment will appear in your LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム診断サービスを構成してから数分で、AX 2012 環境が LCS プロジェクトに表示されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
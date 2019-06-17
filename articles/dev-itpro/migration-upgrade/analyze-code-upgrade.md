<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="analyze-code-upgrade.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>analyze-code-upgrade.689571.4d944c26e13f3307fa79b73922e702d3d787a594.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4d944c26e13f3307fa79b73922e702d3d787a594</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\analyze-code-upgrade.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Upgrade from AX 2012 - Estimate effort by using the Code upgrade service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - コードのアップグレード サービスを使用した工数見積</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to use the Code upgrade service in LCS to help estimate the tasks and effort that are required in order to upgrade a code base from Microsoft Dynamics AX 2012 to Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、LCS のコード アップグレード サービスを使用して、Microsoft Dynamics AX 2012 から Dynamics 365 for Finance and Operations にコード基準をアップグレードするために必要な作業と労力を見積もる方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Upgrade from AX 2012 - Estimate effort by using the Code upgrade service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - コードのアップグレード サービスを使用した工数見積</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to use the Code upgrade service in Microsoft Dynamics Lifecycle Services (LCS) to help estimate the tasks and effort that are required in order to upgrade a code base from Microsoft Dynamics AX 2012 to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) のコード アップグレード サービスを使用して、Microsoft Dynamics AX 2012 から Microsoft Dynamics 365 for Finance and Operations にコード基準をアップグレードするために必要な作業と労力を見積もる方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The Code upgrade service converts an export of your AX 2012 model store to the correct format for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード アップグレード サービスは、AX 2012 モデル ストアのエクスポートを Finance and Operations の適切な形式に変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>However, the new version of your code won’t be fully functional until a developer resolves any issues that the service identifies but can’t resolve itself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、サービスが識別してもまだ独自で解決できない問題を開発者が解決するまで、コードの新しいバージョンは完全に機能しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The Code upgrade service performs these actions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード アップグレード サービスは、これらのアクションを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Directly resolve some types of conflict issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかのタイプの競合問題を直接解決します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For other issues, log Microsoft Azure DevOps tasks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他の問題については、Microsoft Azure DevOps タスクにログ記録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Create a version of your code in the Finance and Operations format, and check the new version into a new branch of your Azure DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations の形式でコードのバージョンを作成し、Azure DevOps プロジェクトの新しい分岐で新しいバージョンを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the Analyze phase, we use the report to help estimate the effort that is required in order to complete code conversion activities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析フェーズでは、レポートを使用してコード変換アクティビティを完了するために必要な作業量を見積もります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The following illustration shows an overview of the process for configuring the Code upgrade service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、コードのアップグレード サービスを構成するプロセスの概要を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Configuration process for the Code upgrade service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード アップグレード サービスのコンフィギュレーション プロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>For information about how to configure the Code upgrade service, see <bpt id="p1">[</bpt>Configure the code upgrade service in Lifecycle Services<ept id="p1">](../lifecycle-services/configure-execute-code-upgrade.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード アップグレード サービスをコンフィギュレーションする方法については、「<bpt id="p1">[</bpt>Lifecycle Services でコード アップグレード サービスをコンフィギュレーションする<ept id="p1">](../lifecycle-services/configure-execute-code-upgrade.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The output of the Code upgrade service is designed to be consumed by a Finance and Operations developer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード アップグレード サービスの出力は、Finance and Operations 開発者が消費するように設計されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>This output will help the developer estimate the effort that is required in order to complete the code upgrade tasks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この出力は、開発者がコードのアップグレード タスクを完了するために必要な工数を見積もるのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>To form an estimate, the developer must review the tasks that the service generates in Azure DevOps and the new version of the code that the service generates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">見積もりを作成するには、サービスが Azure DevOps で生成するタスクと、サービスが生成する新しいバージョンのコードを確認する必要があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
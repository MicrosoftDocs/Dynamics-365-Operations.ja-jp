<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="environment-reprovision.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>environment-reprovision.33170a.795ff0c91f6e5c2ac83dd610a125d2f6fdbbec70.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>795ff0c91f6e5c2ac83dd610a125d2f6fdbbec70</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\includes\environment-reprovision.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101">
          <source>When copying a database between environments, you will need to run the environment re-provisioning tool before the copied database is fully functional, to ensure that all Retail components are up-to-date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境間でデータベースをコピーするとき、コピーされたデータベースが完全に機能するには、その前に環境の再プロビジョニング ツールを実行して、すべての Retail コンポーネントを確実に最新にしておく必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102">
          <source>We recommend that you run this procedure whether you are using Retail components or not, because Retail functionality is included in all environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 機能はすべての環境に含まれているため、Retail コンポーネントを使用しているかどうかに関係なく、このプロシージャを実行することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Before you continue, you must make sure that the following prerequisites are met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">続行する前に、次の前提条件が満たされていることを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>If you are upgrading to the July 2017 release (also known as 7.2) 7.2.11792.56024, apply the following application X++ hotfixes in the destination environment before running the data upgrade in that environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2017 年 7 月リリース (7.2 とも呼ばれる) 7.2.11792.56024 にアップグレードする場合は、移行先環境にアプリケーション X++ 修正プログラムを適用してから、その環境内でデータのアップグレードを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>These will prevent various errors occurring during the data upgrade:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、データ アップグレード中の各種エラーの発生を防止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>KB 4036156 - Retail minor version upgrade - 'Variant number sequence is not set.'</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4036156 - Retail マイナー バージョン アップグレード - 'バリアント番号順序が設定されていません。'</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This fix package also includes KB 4035399 and KB 4035751.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この修正プログラム パッケージには、KB 4035399 および KB 4035751 も含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Note that you must have a minimum of Platform Update 9 to use this package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパッケージを使用するには、最低でも Platform Update 9 が必要であることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>If you are unsure, install the latest binaries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">確信が持てない場合は、最新のバイナリをインストールしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If you are upgrading from Microsoft Dynamics AX 2012, install the following application X++ fixes in the destination environment before you run the data upgrade:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 からアップグレードする場合は、データ アップグレードを実行する前に、移行先の環境に次のアプリケーション X++ 修正プログラムをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>KB 4033183 - Dynamics AX 2012 R2 or Dynamics AX 2012 R3 Pre-CU8 non-retail upgrade fails with Object not found for dbo.RETAILTILLLAYOUTZONE.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4033183 - Dynamics AX 2012 R2 または Dynamics AX 2012 R3 Pre-CU8 non-retail アップグレードは、dbo.RETAILTILLLAYOUTZONE のオブジェクトが存在しないため失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>KB 4040692 - Dynamics AX 2012 R3 to Microsoft Dynamics 365 for Operations 7.2 upgrade fails on RetailSalesLine duplicate index on SalesLineIdx.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4040692 - Microsoft Dynamics 365 for Operations 7.2 への Dynamics AX 2012 R3 のアップグレードは、SalesLineIdx に RetailSalesLine の重複インデックスが存在するため失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>KB 4035490 - Performance issue with GeneralJournalAccountEntry MainAccount field upgrade script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4035490 - GeneralJournalAccountEntry MainAccount フィールドのアップグレード スクリプトに関するパフォーマンスの問題。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Follow these steps to run the Environment reprovisioning tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のステップに従って、環境再プロビジョニング ツールを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In the Shared asset library, select <bpt id="p1">**</bpt>Software deployable package<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有アセット ライブラリで、<bpt id="p1">**</bpt>ソフトウェア配置可能パッケージ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Download the Environment reprovisioning tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境再プロビジョニング ツールをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the asset library for your project, select <bpt id="p1">**</bpt>Software deployable package<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自身のプロジェクトのアセット ライブラリで、<bpt id="p1">**</bpt>ソフトウェア配置可能パッケージ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Select <bpt id="p1">**</bpt>New<ept id="p1">**</ept> to create a new package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規作成<ept id="p1">**</ept> コマンドを選択して、新しいパッケージを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Enter a name and description for the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージの名前と説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You can use <bpt id="p1">**</bpt>Environment reprovisioning tool<ept id="p1">**</ept> as the package name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境再プロビジョニング ツール<ept id="p1">**</ept> をパッケージ名として使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Upload the package that you downloaded earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先ほどダウンロードしたパッケージをアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>On the <bpt id="p1">**</bpt>Environment details<ept id="p1">**</ept> page for your target environment, select <bpt id="p2">**</bpt>Maintain<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Apply updates<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット環境の <bpt id="p1">**</bpt>環境の詳細<ept id="p1">**</ept> ページで、 <bpt id="p2">**</bpt>管理<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>更新プログラムを適用<ept id="p3">**</ept>を順に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Select the Environment reprovisioning tool that you uploaded earlier, and then select <bpt id="p1">**</bpt>Apply<ept id="p1">**</ept> to apply the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先ほどアップロードした環境再プロビジョニング ツールを選択し、<bpt id="p1">**</bpt>適用<ept id="p1">**</ept> を選択してパッケージを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Monitor the progress of the package deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージの配置の進捗を監視します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For more information about how to apply a deployable package, see <bpt id="p1">[</bpt>Apply a deployable package<ept id="p1">](../deployment/create-apply-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージを適用する方法の詳細については、 <bpt id="p1">[</bpt>配置可能パッケージの適用<ept id="p1">](../deployment/create-apply-deployable-package.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For more information about how to manually apply a deployable package, see <bpt id="p1">[</bpt>Install a deployable package<ept id="p1">](../deployment/install-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージを手動で適用する方法の詳細については、 <bpt id="p1">[</bpt>配置可能パッケージのインストール<ept id="p1">](../deployment/install-deployable-package.md)</ept>を参照してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
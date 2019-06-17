<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="updateenvironment-newinfrastructure.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>updateenvironment-newinfrastructure.de075c.9ec1db4f5c3a01300cc2678d4371eab7392c6223.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>9ec1db4f5c3a01300cc2678d4371eab7392c6223</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\deployment\updateenvironment-newinfrastructure.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Update an environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to update an environment that was deployed using the self-service deployment experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、セルフ サービス配置エクスペリエンスを使用して配置された環境を更新する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Update an environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic walks through the process of applying updates to a Dynamics 365 for Finance and Operations environment that was deployed using the <bpt id="p1">[</bpt>self-service deployment<ept id="p1">](infrastructure-stack.md)</ept> experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、<bpt id="p1">[</bpt>セルフサービス配置<ept id="p1">](infrastructure-stack.md)</ept>エクスペリエンスを使用して配置した Dynamics 365 for Finance and Operations 環境に更新を適用するプロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>With the next generation infrastructure, updates are applied differently from the current flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次世代のインフラストラクチャでは、現在のフローとは異なる方法で更新が適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source><bpt id="p1">**</bpt>Whatever is supplied in the package is applied to the environment and it OVERWRITES what is already present in the environment<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パッケージで提供されているものはすべて環境に適用され、既に環境に存在するものは上書きされます<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This means that you <bpt id="p1">**</bpt>must<ept id="p1">**</ept> create a single deployable package that contains all customizations and ISV solutions from your build environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、ビルド環境からのすべてのカスタマイズおよび ISV ソリューションを含む 1 つの配置可能パッケージを作成する<bpt id="p1">**</bpt>必要があります<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If there is a difference in the list of models between what is on the environment and what is in the package, you will be warned before applying the update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境上にあるものと、パッケージに含まれるものの間でモデルの一覧に差異がある場合、更新を適用する前に警告メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For details about creating a single package, see <bpt id="p1">[</bpt>Manage third-party models and runtime packages by using source control<ept id="p1">](../dev-tools/manage-runtime-packages.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのパッケージを作成する方法については、<bpt id="p1">[</bpt>ソース コントロールを使用することでサード パーティ モデルとランタイム パッケージを管理する<ept id="p1">](../dev-tools/manage-runtime-packages.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Supported package types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポートされているパッケージの種類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Because environments deployed using the <bpt id="p1">[</bpt>self-service deployment<ept id="p1">](infrastructure-stack.md)</ept> experience will be on 8.1 and later, we support the following package types:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>セルフ サービス展開<ept id="p1">](infrastructure-stack.md)</ept>エクスペリエンスを使用して展開された環境は 8.1 以降にあるため、次のパッケージ タイプがサポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>AOT deployable package<ept id="p1">**</ept> - A deployable package that is generated from application metadata and source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AOT の配置可能パッケージ<ept id="p1">**</ept> - アプリケーション メタデータおよびソース コードから生成される配置可能なパッケージ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This deployable package is created in a <bpt id="p1">**</bpt>build<ept id="p1">**</ept> environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この展開可能なパッケージは、<bpt id="p1">**</bpt>ビルド<ept id="p1">**</ept>環境で作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>Binary update package<ept id="p1">**</ept> - A deployable package that contains dynamic-link libraries (DLLs) and other binaries and metadata that the platform and application depend on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>バイナリ更新プログラム パッケージ<ept id="p1">**</ept> - ダイナミックリンク ライブラリ (DLL)と、プラットフォームとアプリケーションが依存するその他のバイナリとメタデータを含む配置可能パッケージ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>This is a package released by Microsoft.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、Microsoft によってリリースされたパッケージです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Development Application Lifecycle Management (ALM) flow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発アプリケーション ライフ サイクル管理 (ALM) フロー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>To apply code customizations to your sandbox and production environments, you need to create a deployable code package from your build environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード カスタマイズをサンドボックスおよび製造環境に適用するには、ビルド環境から配置可能なコード パッケージを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>For details on how to do this, see <bpt id="p1">[</bpt>Create deployable packages of models<ept id="p1">](create-apply-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行う方法の詳細については、<bpt id="p1">[</bpt>モデルの配置可能なパッケージを作成<ept id="p1">](create-apply-deployable-package.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Microsoft updates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft の更新プログラム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>To get access to Microsoft updates, go to the environment details page for your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft の更新プログラムへのアクセスを取得するには、環境の環境詳細ページに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You will see a <bpt id="p1">**</bpt>single tile<ept id="p1">**</ept> that shows a cumulative, binary update of all the application and platform fixes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのアプリケーションとプラットフォーム修正の累積的なバイナリ更新を示す <bpt id="p1">**</bpt>1 つのタイル<ept id="p1">**</ept> が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>To apply this update, select the package and select <bpt id="p1">**</bpt>Save Package<ept id="p1">**</ept> to save the Microsoft update to the project asset library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この更新プログラムを適用するには、パッケージを選択して <bpt id="p1">**</bpt>パッケージの保存<ept id="p1">**</ept> を選択し、プロジェクト資産ライブラリに Microsoft の更新プログラムを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Apply updates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新プログラムの適用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Tier 1 Sandbox/Develop and Test/Demo/Build environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レベル 1 サンドボックス/開発およびテスト/デモ/ビルド環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>To apply updates to a Tier 1 Sandbox/Develop and Test/Demo/Build environment deployed through Lifecycle Services (LCS), follow the steps in  <bpt id="p1">[</bpt>Apply updates to cloud environments<ept id="p1">](apply-deployable-package-system.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) を通じて配置されたレベル 1 サンドボックス/開発およびテスト/デモ/ビルド環境に更新を適用するには、<bpt id="p1">[</bpt>クラウド環境に更新を適用する<ept id="p1">](apply-deployable-package-system.md)</ept>の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Tier 2 and above Standard Acceptance Test/Sandbox environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レベル 2 以上の標準引受テスト/サンドボックス環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Applying packages causes system downtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージを適用するとシステムのダウンタイムが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>All relevant services will be stopped, and you won't be able to use your environments while the package is being applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべて関連するサービスを停止、およびパッケージを適用中のときには環境を使用できなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Before you begin, verify that the deployable package has been uploaded to the project asset library in LCS and that validations have succeeded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始する前に、配置可能パッケージが LCS のプロジェクト アセット ライブラリにアップロードされていることと、検証が成功したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>After you have this package in the project asset library, use the following steps to update your environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパッケージをプロジェクト資産ライブラリに置いたら、次の手順を使用して環境を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Open the <bpt id="p1">**</bpt>Environment details<ept id="p1">**</ept> view for the environment where you want to apply the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージを適用する環境の<bpt id="p1">**</bpt>環境の詳細<ept id="p1">**</ept>ビューを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Click <bpt id="p1">**</bpt>Maintain &gt; Apply updates<ept id="p1">**</ept> to apply an update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メンテナンス &gt; 更新プログラムの適用<ept id="p1">**</ept>をクリックし、更新プログラムを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Select the package to apply.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージを選択して適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Use the filter at the top to find your package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上部にあるフィルターを使用してパッケージを探します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You will see application and platform binary packages and application deployable packages that have passed validation from the asset library in the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションおよびプラットフォーム バイナリ パッケージと、一覧のアセット ライブラリから検証に合格したアプリケーションの配置可能なパッケージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Click <bpt id="p1">**</bpt>Apply<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>適用<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The status in the upper-right corner of the <bpt id="p1">**</bpt>Environment details<ept id="p1">**</ept> view changes from <bpt id="p2">**</bpt>Queued<ept id="p2">**</ept> to <bpt id="p3">**</bpt>Servicing<ept id="p3">**</ept>, and then after completion it changes to <bpt id="p4">**</bpt>Deployed<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境の詳細<ept id="p1">**</ept> ビューの右上隅のステータスが <bpt id="p2">**</bpt>キュー<ept id="p2">**</ept> から <bpt id="p3">**</bpt>サービス<ept id="p3">**</ept> に代わり、完了した後は <bpt id="p4">**</bpt>配置済み<ept id="p4">**</ept> に変わります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>After completion, the environment history accessible from <bpt id="p1">**</bpt>History &gt; Environment<ept id="p1">**</ept> changes on the <bpt id="p2">**</bpt>Environment details<ept id="p2">**</ept> page is updated to show the completed package deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了すると、<bpt id="p2">**</bpt>環境の詳細<ept id="p2">**</ept> ページにある <bpt id="p1">**</bpt>履歴 &gt; 環境<ept id="p1">**</ept>の変更からアクセスできる環境履歴が更新され、配置済みの完了したパッケージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>You can also download the logs from the environment history page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境履歴ページからログをダウンロードすることもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>For environments deployed in the modern infrastructure stack, if servicing fails, the environment is automatically rolled back.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新のインフラストラクチャ スタックに配置された環境では、サービスが失敗した場合、環境が自動的にロールバックされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>To understand why the operation failed, you can download the logs from the environment history page as mentioned in the steps above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">工程が失敗した理由を理解するため、上記の手順に示されているとおりに環境の履歴ページからログをダウンロードすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Production environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Applying updates to production has not been enabled yet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">運用環境に更新プログラムを適用することは、まだ有効になっていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>To improve the reliability of updates being applied to production, when this flow is enabled you have the option to move either the latest copy or a designated snapshot of the sandbox environment to production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">運用環境に適用する更新の信頼性を向上させるため、このフローが有効になると、最新のコピーとサンドボックス環境の指定されたスナップショットのどちらを運用環境に移動するかを選択できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>There is no way to select an update and move that to production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新を選択して、それを運用環境に移動する方法はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>This ensures a more reliable experience as the update will not be applied again; rather an image of the sandbox will be promoted to production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、更新がもう一度適用されなくなり、サンドボックスのイメージが運用環境に昇格されるため、エクスペリエンスの信頼性が高くなります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
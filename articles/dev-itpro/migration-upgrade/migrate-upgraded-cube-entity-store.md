<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="migrate-upgraded-cube-entity-store.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>migrate-upgraded-cube-entity-store.27c162.b889fb0c59745cc38c8e21ee6f2d926033c76295.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>b889fb0c59745cc38c8e21ee6f2d926033c76295</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\migrate-upgraded-cube-entity-store.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Migrate upgraded AX 2012 R3 sales cubes to the entity store</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードした AX 2012 R3 販売キューブのエンティティ格納への移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>In this tutorial, you'll migrate an upgraded Microsoft Dynamics AX 2012 R3 cube schema to the entity store in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、アップグレードされた Microsoft Dynamics AX 2012 R3 キューブ スキーマを、Microsoft Dynamics 365 for Finance and Operations のエンティティ格納に移行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>You'll use the sales cube that was included in Dynamics AX 2012 R3 as an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例として、Dynamics AX 2012 R3 に含まれていた販売キューブを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Migrate upgraded AX 2012 R3 sales cubes to the entity store</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードした AX 2012 R3 販売キューブのエンティティ格納への移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In this tutorial, you'll migrate an upgraded Microsoft Dynamics AX 2012 R3 cube schema to the entity store in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、アップグレードされた Microsoft Dynamics AX 2012 R3 キューブ スキーマを、Microsoft Dynamics 365 for Finance and Operations のエンティティ格納に移行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You'll use the sales cube that was included in Dynamics AX 2012 R3 as an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例として、Dynamics AX 2012 R3 に含まれていた販売キューブを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The entity store will support near real-time Microsoft Power BI integration scenarios, as shown in the following diagram.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ格納は、次の図に示すように、ほぼリアルタイムの Microsoft Power BI 統合シナリオをサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For an overview of Power BI integration with entity store, see <bpt id="p1">[</bpt>Power BI integration with entity store<ept id="p1">](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ格納と Power BI 統合の概要については、「<bpt id="p1">[</bpt>エンティティ格納と Power BI の統合<ept id="p1">](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Power BI Architecture diagram<ept id="p1">](./media/powerbiarchitecture.png)](./media/powerbiarchitecture.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Power BI アークテクチャ ダイアグラム<ept id="p1">](./media/powerbiarchitecture.png)](./media/powerbiarchitecture.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>New Power BI features included in the May 2016 and November 2016 updates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2016 年 5 月および 2016 年 11 月の更新プログラムに含まれる Power BI の新機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This tutorial requires the Dynamics 365 for Operations May 2016 update or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、Dynamics 365 for Operations の 2016 年 5 月以降の更新プログラムが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>You will use the following new capabilities in this tutorial:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、次の新しい機能を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Stage an aggregate measurement in the entity store and refresh the data from Dynamics AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ格納で集計測定をステージングし、Dynamics AX のデータを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>You might prefer this option over in-memory real time aggregate measurements when:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メモリ内リアルタイムの集計測定値には、このオプションの方を選択する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>You upgrade a Dynamics AX 2012 cube.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 キューブをアップグレードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Your aggregate measurements are very large.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計の測定は非常に大規模です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Data freshness (latency) from a few minutes up to a few hours is acceptable for reporting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データの新しさ (待機時間) は、数分から数時間まで報告することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Use the batch framework to schedule a recurring refresh.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定期的な更新をスケジュールするには、バッチ フレームワークを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For this release, only a full refresh is enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このリリースでは、完全な更新のみが有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Create reports using Power BI desktop in a developer/test environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者/テスト環境で Power BI デスクトップを使用してレポートを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Leverage the direct query option when creating Power BI content.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI コンテンツを作成するときに、直接クエリ オプションを活用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>For example, you can create larger models without relying on OData as the data refresh mechanism.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、データ更新のメカニズムとして OData に依存せず、大きなモデルを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Migrate reports from your development environment to a production environment using Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) を使用してレポートを開発環境から実稼働環境に移行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>As a partner or an ISV you can distribute Power BI content as part of an LCS solution to your customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パートナーまたは ISV として、Power BI コンテンツを LCS ソリューションの一部として顧客に配布することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>If you're using the November update (platform release 1611)<ept id="p1">**</ept> or later, some steps in this document are part of the process to refresh the entity store - you do not need to perform them manually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>11 月の更新 (プラットフォーム リリース 1611) 以降を使用している場合<ept id="p1">**</ept>、このドキュメントのいくつかの手順は、エンティティ ストアを更新するプロセスの一部です。手動で実行する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Change upgraded aggregate measurement properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードされた集計の測定プロパティの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>As part of the code upgrade process, analysis services projects from the Application Object Tree (AOT) in Dynamics AX 2012 can be migrated to the new aggregate measurements metadata format.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">コード アップグレード プロセスの一環として、Dynamics AX 2012 のアプリケーション オブジェクト ツリー (AOT) からの分析サービス プロジェクトを新しい集計測定メタデータ形式に移行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Launch Visual Studio and create a new project in Application Suite.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Visual Studio を起動し、アプリケーション スイートで新しいプロジェクトを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>You can create a model and include the customized aggregate measurement within that model.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">モデルを作成し、カスタマイズされた集計測定をそのモデルに含めることができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For more information, see <bpt id="p1">[</bpt>Customization: Overlayering and extensions<ept id="p1">](../extensibility/customization-overlayering-extensions.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>カスタマイズ: オーバーレイおよび拡張機能<ept id="p1">](../extensibility/customization-overlayering-extensions.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Open Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Navigate to <bpt id="p1">**</bpt>Analytics<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Perspectives<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Aggregate measurements<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>分析<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>分析視点<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>集計の測定<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>You will notice a set of aggregate measurements that were upgraded from Dynamics AX 2012 R3, as well as the measurements that ship in the current version of Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations の現在のバージョンに同梱されている測定だけでなく、Dynamics AX 2012 R3 からアップグレードされた集計の測定のセットが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Select <bpt id="p1">**</bpt>SalesCube<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesCube<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Right-click and select <bpt id="p1">**</bpt>Duplicate in project<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、<bpt id="p1">**</bpt>プロジェクトで複製<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>An aggregate measurement with the name <bpt id="p1">**</bpt>SalesCubeCopy<ept id="p1">**</ept> will be added to the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesCubeCopy<ept id="p1">**</ept> という名前の集計の測定がプロジェクトに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Rename this measurement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この測定値の名前を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Select <bpt id="p1">**</bpt>SalesCubeCopy<ept id="p1">**</ept> in Solution Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>SalesCubeCopy<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Right-click and select <bpt id="p1">**</bpt>Rename<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、<bpt id="p1">**</bpt>名前の変更<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Enter <bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept> as the new name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept> という新しい名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Double-click <bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept> to launch the Aggregate measurement designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aggregate measurement designer を起動するには、<bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Notice the structure of the aggregate measurement that was migrated from Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 から移行された集計の測定の構造体を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The Sales cube in Dynamics AX 2012 encompassed a broad subject area related to Sales.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 の Sales キューブは、販売に関連する広範な分野を包含していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>In this case, let’s create a smaller, more focused Power BI model using the metadata that was upgraded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、アップグレードしたメタデータを使用してより小規模で焦点を絞った Power BI モデルを作成しましょう。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Expand the <bpt id="p1">**</bpt>Sales Order Lines<ept id="p1">**</ept> measure group and review the list of measures and dimension references.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>販売注文明細行<ept id="p1">**</ept>のメジャー グループを展開し、メジャー リストおよび分析コードの参照を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Leveraging the modeling capabilities you can quickly make a few enhancements to this model.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">モデリング機能を活用することで、このモデルをすばやく機能拡張することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Suggestions for improvements:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">改善の提案:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Replace views/tables that have been used to model the measure group (and/or dimensions) with an entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メジャー グループ (または分析コード) をモデル化するために使用されたビュー/テーブルをエンティティに置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>You can model an entity using the underlying view and replace the view with the corresponding entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基になるビューを使用してエンティティをモデリングして、対応するエンティティでビューを置き換えることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>This will enable you to leverage upcoming features such as incremental refresh and security.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、インクリメンタル リフレッシュおよびセキュリティなど、今後登場する機能を活用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Remove unwanted dimension references by adding the corresponding field to the attributes node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性ノードに対応するフィールドを追加することで、不要な分析コードの参照を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>For example, the Sizes dimension reference can be removed because the <bpt id="p1">**</bpt>Size<ept id="p1">**</ept> field in the measure group is sufficiently descriptive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、メジャー グループの<bpt id="p1">**</bpt>サイズ<ept id="p1">**</ept>フィールドが十分に説明され、サイズの分析コード参照は削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>This will improve the runtime performance of queries as well as refresh times.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、クエリのランタイム パフォーマンスとリフレッシュ時間が向上します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Select the <bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept> root node in the Aggregate measurement designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計測定デザイナーで <bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept> ルート ノードを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Right-click and select <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>During upgrade, aggregate measurements are set to the legacy property flag, <bpt id="p1">**</bpt>SSASCube<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード中に、集計の測定はレガシ プロパティ フラグ <bpt id="p1">**</bpt>SSASCube<ept id="p1">**</ept> に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>You need to change this property to one of two supported usage types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポートされる使用法の 2 つのタイプのいずれかに、このプロパティを変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Previously, <bpt id="p1">**</bpt>InMemoryRealTime<ept id="p1">**</ept> was supported as usage for aggregate measurements.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">以前は、<bpt id="p1">**</bpt>InMemoryRealTime<ept id="p1">**</ept> は集計測定値の使用方法としてサポートされていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">**</bpt>StagedEntityStore<ept id="p1">**</ept> is supported as a new usage type.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>StagedEntityStore<ept id="p1">**</ept> は新しい使用タイプとしてサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Modify the usage property to InMemoryRealTime if you plan to use the Aggregate measurement for embedded BI scenarios as well as Power BI integration.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">埋め込み BI シナリオおよび Power BI 統合に集計の測定を使用する場合は、用途プロパティを InMemoryRealTime に変更します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>If you are using the Aggregate measurement only for Power BI or Cortana Intelligence Suite integration, select <bpt id="p1">**</bpt>StagedEntityStore<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI または Cortana Intelligence との統合に対してのみ集計測定を使用している場合は、<bpt id="p1">**</bpt>StagedEntityStore<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Save the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Right-click the project in Solution Explorer and select <bpt id="p1">**</bpt>Rebuild<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーでプロジェクトを選択し、<bpt id="p1">**</bpt>リビルド<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>After the rebuild operation is finished, save the project, and then close Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再構築操作を完了した後、プロジェクトを保存し、Visual Studio を閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This completes the development work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これで開発作業は完了です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>You will author reports as a report developer or a power user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート作成者またはパワー ユーザーとしてレポートを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Refresh the entity store</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ格納を更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>As an administrator you can configure the refresh of the aggregate measurement using the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者は、クライアントを使用して集計測定の更新をコンフィギュレーションできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Launch the Dynamics AX client and navigate to <bpt id="p1">**</bpt>System Administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Entity Store<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX クライアントを起動して、<bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>エンティティ格納<ept id="p3">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The <bpt id="p1">**</bpt>Entity Store<ept id="p1">**</ept> form shows a list of aggregate measurements that are available for deployment to the entity store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティ格納<ept id="p1">**</ept> フォームには、エンティティ格納に配置するために使用できる集計測定の一覧が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Notice that <bpt id="p1">**</bpt>Sales Cube<ept id="p1">**</ept> (which was upgraded from Dynamics AX 2012) is not available for deployment to the entity store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>売上キューブ<ept id="p1">**</ept> (Dynamics AX 2012 からアップグレードされた) がエンティティ格納への配置に使用できないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source><bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept>, which you created in the previous step, can be deployed to the entity store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept>、前の手順で作成したものをエンティティ格納に展開できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Select <bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept> from the list, and click the <bpt id="p2">**</bpt>Refresh<ept id="p2">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストから <bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>更新<ept id="p2">**</ept> ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The <bpt id="p1">**</bpt>Refresh<ept id="p1">**</ept> dialog box will display.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>更新<ept id="p1">**</ept> ダイアログ ボックスが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Expand the <bpt id="p1">**</bpt>Run in the background<ept id="p1">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>バックグラウンドで実行<ept id="p1">**</ept>タブを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Provide a descriptive name in the <bpt id="p1">**</bpt>Task description<ept id="p1">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タスクの説明<ept id="p1">**</ept> フィールドにわかりやすい名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Optionally, you can select the <bpt id="p1">**</bpt>Recurrence<ept id="p1">**</ept> tab and create a recurring schedule instead of a one-time refresh.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、<bpt id="p1">**</bpt>定期的なアイテム<ept id="p1">**</ept> タブを選択し、1 回限りの更新ではなく定期的なスケジュールを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The system will create a batch job for refresh of the aggregate measurement in the entity store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ ストア内の集計測定値をリフレッシュするためのバッチ ジョブが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Authoring a report on Sales by State with Power BI desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI desktop を使用して都道府県別売上レポートの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>This step requires that you the install Power BI desktop tool that can be downloaded from <bpt id="p1">[</bpt>Microsoft Power BI Desktop<ept id="p1">](https://www.microsoft.com/download/details.aspx?id=45331)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップでは、「<bpt id="p1">[</bpt>Microsoft Power BI Desktop<ept id="p1">](https://www.microsoft.com/download/details.aspx?id=45331)</ept>」からダウンロードできる Power BI デスクトップ ツールをインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Launch Power BI desktop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI デスクトップを起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>You may need to apply updates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新を適用することが必要な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>A welcome page will display.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウェルカム ページが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Click <bpt id="p1">**</bpt>Get data<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データの取得<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Alternatively, when Power BI desktop launches, on the <bpt id="p1">**</bpt>Home<ept id="p1">**</ept> tab select <bpt id="p2">**</bpt>Get Data<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>SQL Server<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、Power BI デスクトップが起動したとき、<bpt id="p1">**</bpt>ホーム<ept id="p1">**</ept>タブの<bpt id="p2">**</bpt>データの取得<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>SQL Server<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>In the <bpt id="p1">**</bpt>SQL Server Database<ept id="p1">**</ept> dialog box, enter the server name and the name of the entity store database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SQL Server データベース<ept id="p1">**</ept> ダイアログ ボックスで、サーバー名とエンティティ ストア データベースの名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>If you deployed a developer environment, you can enter “.”</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境を配置する場合は、“.” を入力できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>as the server name and <bpt id="p1">**</bpt>AxDW<ept id="p1">**</ept> as the database name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー名として、および <bpt id="p1">**</bpt>AxDW<ept id="p1">**</ept> をデータベースとして。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>If you are working in a test environment, you need to get these parameters from your system administrator</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト環境で作業している場合、システム管理者からこれらのパラメータを取得する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Select the <bpt id="p1">**</bpt>DirectQuery<ept id="p1">**</ept> option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DirectQuery<ept id="p1">**</ept> オプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>In this exercise, you will create Power BI reports that are executed directly on the entity store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この練習では、エンティティ格納に直接実行される Power BI レポートを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>If you had used the <bpt id="p1">**</bpt>Import<ept id="p1">**</ept> option, Power BI would cache data from the entity store and you would need to periodically refresh the Power BI model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インポート<ept id="p1">**</ept> オプションを使用した場合、Power BI ではエンティティ格納のデータがキャッシュされるため、Power BI モデルを定期的に更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source><bpt id="p1">**</bpt>Import mode is currently not supported with reports written using entity store<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティ格納を使用して書かれたレポートでは、インポート モードは現在サポートされていません<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Next you will see the <bpt id="p1">**</bpt>Navigator<ept id="p1">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、<bpt id="p1">**</bpt>ナビゲーター<ept id="p1">**</ept> ダイアログ ボックスが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Navigator enables you to select tables and views from the entity store that you want to report on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーターで、レポートの対象となるテーブルとビューをエンティティ格納から選択できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Enter <bpt id="p1">**</bpt>Sales<ept id="p1">**</ept> in the search box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索ボックスで<bpt id="p1">**</bpt>販売<ept id="p1">**</ept>を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>The system will filter entities that are related to the <bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept> aggregate measurement that was previously created.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">以前に作成された <bpt id="p1">**</bpt>SalesCubeV2<ept id="p1">**</ept> 集計測定に関連するエンティティがフィルタリングされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>The entity store stages the aggregate measurements that have been created.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">エンティティ ストアは作成された集計の測定をステージします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>While entities within each aggregate measurement are prefixed and stored as individual tables, Power BI desktop enables you to combine data from multiple aggregate measurements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それぞれの集計測定内のエンティティには接頭語が付けられて別々のテーブルとして保管されますが、Power BI デスクトップを使用すると複数の集計測定からのデータを結合することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>You will create a report that shows sales by state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">都道府県別の売上を表示するレポートを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Select <bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p1">**</ept> and <bpt id="p2">**</bpt>SalesCubeV2<ph id="ph2">\_</ph>CustomerInvoices<ept id="p2">**</ept> from Navigator and click <bpt id="p3">**</bpt>Load<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーターから <bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p1">**</ept> および <bpt id="p2">**</bpt>SalesCubeV2<ph id="ph2">\_</ph>CustomerInvoices<ept id="p2">**</ept> を選択し、<bpt id="p3">**</bpt>読み込み<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>You will notice Power BI designer with <bpt id="p1">**</bpt>Fields<ept id="p1">**</ept> present in the entities that you have chosen (on the far right), as well as available visualization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したエンティティ (右端) に<bpt id="p1">**</bpt>フィールド<ept id="p1">**</ept>が存在する Power BI デザイナーが、使用可能な視覚化とともに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Create a surrogate key that links customers and invoices (applies to platform versions before November 2016 update)</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">顧客と請求書をリンクする代理キーを作成する (2016 年 11 月アップデート以前のプラットフォームに適用)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>You do not need to perform this step if you are working on the November 2016 release of the platform or later.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">プラットフォームの 2016 年 11 月以降のリリースで作業している場合は、この手順を実行する必要はありません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Surrogate keys are generated in aggregate measurements staged into entity store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代理キーは、エンティティ格納にステージングされる集計測定で生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Power BI desktop does not enable you to relate table joins using multiple fields (also known as, composite keys).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI デスクトップでは、複数のフィールド (複合キーとも呼ばれます) を使用してテーブル結合を関連付けることができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The <bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p1">**</ept> entity does not have a surrogate key (such as AX RecID) defined in it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p1">**</ept> エンティティでは、代理キー (AX RecID など) が定義されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Next, you will create a surrogate key that enables relating a customer entity to invoices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、請求書に顧客エンティティを関連付けできる代理キーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Select the ellipsis (…) icon next to the <bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>CustomerInvoices<ept id="p1">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>CustomerInvoices<ept id="p1">**</ept> エンティティの横にある省略記号 (...) アイコンを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Right-click and select <bpt id="p1">**</bpt>New Column<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、<bpt id="p1">**</bpt>新しい列<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Enter the following expression in the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フォーミュラ エディタ<ept id="p1">**</ept>ウィンドウに次の式を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>When you enter the first few letters of the field name or function, the editor will display a list of candidate fields.</source><target logoport:matchpercent="96" state="translated" state-qualifier="fuzzy-match">フィールド名または関数の最初の数文字を入力すると、エディターに候補フィールドの一覧が表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>This is called a type-ahead feature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、先行入力機能と呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>You can either copy and paste this expression or use the type-ahead feature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この式をコピーして貼り付けるか、タイプ先行機能を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>When completed, your formula should look similar to the following.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了すると、式は次のようになるはずです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Power BI Formula<ept id="p1">](./media/powerbiformula.png)](./media/powerbiformula.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Power BI フォーミュラ<ept id="p1">](./media/powerbiformula.png)](./media/powerbiformula.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Notice that a new field, <bpt id="p1">**</bpt>FKCustomer<ept id="p1">**</ept>, is shown in the list of fields for the <bpt id="p2">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>CustomerInvoices<ept id="p2">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいフィールド <bpt id="p1">**</bpt>FKCustomer<ept id="p1">**</ept> が <bpt id="p2">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>CustomerInvoices<ept id="p2">**</ept> テーブルのフィールドの一覧に表示されていることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Because this field is used to relate two tables, you can hide it from end users by right-clicking the field and selecting the <bpt id="p1">**</bpt>Hide<ept id="p1">**</ept> option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは 2 つのテーブルを関連付けるために使用されるので、フィールドを右クリックして<bpt id="p1">**</bpt>非表示<ept id="p1">**</ept>オプションを選択するとエンド ユーザーから非表示にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Next, create a similar field in the <bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p1">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、<bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p1">**</ept> テーブルに類似したフィールドを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Select the ellipsis (…) icon next to <bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p1">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p1">**</ept> エンティティの横にある省略記号 (...) アイコンを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Right-click and select <bpt id="p1">**</bpt>New Column<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、<bpt id="p1">**</bpt>新しい列<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Enter the following expression in the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フォーミュラ エディタ<ept id="p1">**</ept>ウィンドウに次の式を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Notice that the field <bpt id="p1">**</bpt>FKCustomer<ept id="p1">**</ept> is shown in the list of fields for the <bpt id="p2">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p2">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド <bpt id="p1">**</bpt>FKCustomer<ept id="p1">**</ept> が <bpt id="p2">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p2">**</ept> テーブルのフィールドの一覧に表示されていることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Because this field is used for relating two tables, you can hide it from end users by right-clicking the field and selecting the <bpt id="p1">**</bpt>Hide<ept id="p1">**</ept> option.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">このフィールドは 2 つのテーブルの関連付けに使用されるため、フィールドを右クリックして<bpt id="p1">**</bpt>非表示<ept id="p1">**</ept>オプションを選択するとエンド ユーザーから非表示にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Relate invoices and customers</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">請求書および顧客を関連付ける</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>If you are on the November 2016 version of the platform or later, you can relate the surrogate keys already created within entity store.</source><target logoport:matchpercent="96" state="translated" state-qualifier="fuzzy-match">2016 年 11 月以降のバージョン プラットフォームでは、既にエンティティ ストア内で作成された代理キーを関連付けることができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>If not, you must relate the surrogate keys that you created manually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合は、手動で作成した代理キーを関連付ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Next you will create a relationship between <bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>CustomerInvoices<ept id="p1">**</ept> and <bpt id="p2">**</bpt>SalesCubeV2<ph id="ph2">\_</ph>Customers<ept id="p2">**</ept> entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、<bpt id="p1">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>CustomerInvoices<ept id="p1">**</ept> と <bpt id="p2">**</bpt>SalesCubeV2<ph id="ph2">\_</ph>Customers<ept id="p2">**</ept> のエンティティのリレーションシップを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Click the <bpt id="p1">**</bpt>Manage Relationships<ept id="p1">**</ept> button on the Power BI ribbon.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI リボンの<bpt id="p1">**</bpt>関係の管理<ept id="p1">**</ept>ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>You will see the <bpt id="p1">**</bpt>Manage Relationships<ept id="p1">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リレーションシップの管理<ept id="p1">**</ept> ダイアログ ボックスが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Click the <bpt id="p1">**</bpt>New<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept>ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>In the <bpt id="p1">**</bpt>Create Relationship<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>SalesCubeV2CustomerInvoices<ept id="p2">**</ept> as the first table in the drop-down list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係の作成<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>SalesCubeV2CustomerInvoices<ept id="p2">**</ept> をドロップダウン リストの最初のテーブルとして選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Scroll to the right and select the <bpt id="p1">**</bpt>FKCustomer<ept id="p1">**</ept> field as the column to relate to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右にスクロールし、関連する列として <bpt id="p1">**</bpt>FKCustomer<ept id="p1">**</ept> フィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>In the second drop-down list select <bpt id="p1">**</bpt>SalesCubeV2Customer<ept id="p1">**</ept> as the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 番目のドロップダウン リストで、<bpt id="p1">**</bpt>SalesCubeV2Customer<ept id="p1">**</ept> をテーブルとして選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Scroll to the right and select <bpt id="p1">**</bpt>FKCustomer<ept id="p1">**</ept> as the column to relate to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右にスクロールし、関連する列として <bpt id="p1">**</bpt>FKCustomer<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Select the <bpt id="p1">**</bpt>Make this relationship active<ept id="p1">**</ept> option if it is not already selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>この関係を有効にする<ept id="p1">**</ept> オプションがまだオンになっていない場合はオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックして続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>You will notice the newly created relationship in the <bpt id="p1">**</bpt>Manage Relationships<ept id="p1">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しく作成されたリレーションシップは <bpt id="p1">**</bpt>リレーションシップの管理<ept id="p1">**</ept> ダイアログ ボックスでわかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Click the <bpt id="p1">**</bpt>Close<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept>ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Create a Sales by state report</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">都道府県別売上レポートを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>To create a report that shows sales by customer group, drag the <bpt id="p1">**</bpt>CustomerInvoiceAmountAccountingCurrency<ept id="p1">**</ept> field from the <bpt id="p2">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>CustomerIncoices<ept id="p2">**</ept> table and drop it on the Power BI desktop canvas.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客グループによる売上を示すレポートを作成するには、<bpt id="p2">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>CustomerIncoices<ept id="p2">**</ept> テーブルから <bpt id="p1">**</bpt>CustomerInvoiceAmountAccountingCurrency<ept id="p1">**</ept> フィールドをドラッグして、Power BI デスクトップ キャンバスにドロップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Next, drag the <bpt id="p1">**</bpt>CustomerGroupName<ept id="p1">**</ept> field in the <bpt id="p2">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p2">**</ept> table to the same grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、<bpt id="p2">**</bpt>SalesCubeV2<ph id="ph1">\_</ph>Customer<ept id="p2">**</ept> テーブルの <bpt id="p1">**</bpt>CustomerGroupName<ept id="p1">**</ept> フィールドを同じグリッドにドラッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Change the chart type to a doughnut chart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グラフの種類をドーナツ グラフに変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>You should see a report similar to the following.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のようなレポートが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Power BI Doughnut Chart<ept id="p1">](./media/doughnut-chart-1024x733.png)](./media/doughnut-chart.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Power BI ドーナツ グラフ<ept id="p1">](./media/doughnut-chart-1024x733.png)](./media/doughnut-chart.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>You can create additional visuals using the Power BI desktop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI デスクトップを使用して、追加のビジュアルを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>When you save, you will notice that the file has a <bpt id="p1">**</bpt>PBIX<ept id="p1">**</ept> extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存するとき、ファイルに <bpt id="p1">**</bpt>PBIX<ept id="p1">**</ept> 拡張子が付いていることがわかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Save the report to your desktop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートをデスクトップに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>At this point the report is fully functional (with data from your environment) and you can continue to use the Power BI desktop or upload this report to PowerBI.com and continue with data exploration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この時点でレポートは (環境のデータで) 完全に機能しており、Power BI デスクトップを引き続き使用するか、このレポートを PowerBI.com にアップロードしてデータの検索を続行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Next, you will migrate this report to a production environment using LCS so that you can see this report with production data and share it with other users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、LCS を使用してこのレポートを実稼働環境に移行し、生産データとともにこのレポートを表示して、他のユーザーと共有できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Publish the report and the model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートおよびモデルを公開</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Publishing a report and model requires uploading the report to Lifecycle Services, migrating the aggregate measurement to your production environment, configuring the client to point to the correct LCS library, and publishing your reports in your production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートとモデルの発行には、Lifecycle Services へのレポートのアップロード、集計単位の実稼動環境への移行、適切な LCS ライブラリをポイントするためのクライアントの構成、実稼働環境でのレポートの発行が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Upload the report to Lifecycle Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートを Lifecycle Services にアップロード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Microsoft Dynamics Lifecycle Services (LCS) is the tool used to migrate development artifacts from developer to production environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) は、開発者から実稼働環境に開発コンポーネントを移行するために使用するツールです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>In the May 2016 update, LCS supports migrating PBIX files (authored using the entity store) between environments.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2016 年 5 月の更新プログラムで、LCS は環境間の PBIX ファイルの移行 (エンティティ格納を使用して作成) をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Open <bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/)</ept> from the developer environment.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">開発環境から <bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/)</ept> を起動します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>If you haven’t created a project in the LCS environment, create a project.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">LCS 環境で、プロジェクトを作成していない場合は、プロジェクトを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Scroll to the right and you will notice the <bpt id="p1">**</bpt>Asset Library<ept id="p1">**</ept> icon.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右にスクロールし、<bpt id="p1">**</bpt>アセット ライブラリ<ept id="p1">**</ept> アイコンを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Click the icon and launch <bpt id="p1">**</bpt>Asset Library<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アイコンをクリックし、<bpt id="p1">**</bpt>アセット ライブラリ<ept id="p1">**</ept>を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Notice that the asset library enables adding <bpt id="p1">**</bpt>PowerBI report models<ept id="p1">**</ept> (PBIX files) as implementation artifacts to a project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アセット ライブラリを使用して、プロジェクトに <bpt id="p1">**</bpt><ph id="1">Power BI</ph> レポート モデル<ept id="p1">**</ept> (PBIX ファイル) を実装コンポーネントとして追加できることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Select the plus (+) icon to add a new asset.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラス記号 (+) を選択し、新しい資産を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Provide a name and a description.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前と説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Click <bpt id="p1">**</bpt>Upload<ept id="p1">**</ept> and then locate the file that you saved in an earlier step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アップロード<ept id="p1">**</ept>をクリックし、前の手順で保存したファイルを探します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>After you successfully upload the file, click <bpt id="p1">**</bpt>Confirm<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルを正常にアップロードした後、<bpt id="p1">**</bpt>確定<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Notice that the file is uploaded into LCS as an implementation asset.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルが実装アセットとして LCS にアップロードされることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>LCS supports managing versions and releases for Power BI reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS は、バージョン管理をサポートして、Power BI レポートをリリースします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>You can maintain several versions and publish reports to other environments, just as you would for other implementation artifacts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の実装コンポーネントに対するのと同じ方法で、複数のバージョンを管理してレポートを他環境に公開することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Because you added the PBIX files as an asset within an LCS project, environments that you deployed using that project will have access to this report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PBIX ファイルを LCS プロジェクト内の資産として追加したため、そのプロジェクトを使用して配備した環境はこのレポートにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Optionally, you can publish this report so that all of your projects can access the shared assets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、すべてのプロジェクトが共用資産にアクセスできるように、このレポートを発行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>If you are a partner or an ISV, and want to share this report with your customers, you would share this asset to your global library and enable your customers to import the asset into their respective LCS projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パートナーまたは ISV であり、お客様とこのレポートを共有する場合は、グローバル ライブラリにこの資産を共有し、顧客が資産をそれぞれの LCS プロジェクトにインポートできるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>To do this, select the <bpt id="p1">**</bpt>Save to my library<ept id="p1">**</ept> option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うには、<bpt id="p1">**</bpt>マイライブラリに保存<ept id="p1">**</ept> オプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Migrate the aggregate measurement to a production environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計の測定の実稼働環境への移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>You need to migrate the aggregate measurement that you modified in the developer environment to the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境で修正した集計測定を実稼働環境に移行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>You can follow the instructions in Generate a deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージを生成の指示に従うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>create-apply-deployable-package.md.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">create-apply-deployable-package.md.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>After you successfully publish the model, perform the steps outlined in the <bpt id="p1">**</bpt>Refresh the entity store<ept id="p1">**</ept> section of this tutorial, so that the entity store is updated with data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルを正常に公開した後、このチュートリアルの<bpt id="p1">**</bpt>エンティティ ストアを更新<ept id="p1">**</ept>セクションの説明している手順に従って実行し、エンティティ ストアはデータを更新できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Configure an LCS project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトをコンフィギュレーションする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>If you haven’t already done so, associate your environment with an LCS project so that Finance and Operations is able to consume assets within the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">まだ実行していない場合は、環境と LCS プロジェクトを関連付けることで、Finance and Operations がプロジェクト内の資産を消費できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Launch the client from the instance that you want to use to deploy the Power BI reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI レポートの配置に使用するインスタンスからクライアントを起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Typically this is the test or a production instance where you want to see a report with a different set of data than what you worked with as a report developer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは通常、データ セットのレポートを表示するテストまたは本番のインスタンスであり、レポート開発者として作業したものとは異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Open <bpt id="p1">**</bpt>System Administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>System parameters<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1">&amp;gt;</ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph2">&amp;gt;</ph><bpt id="p3">**</bpt>システム パラメーター<ept id="p3">**</ept>を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Select the <bpt id="p1">**</bpt>Help<ept id="p1">**</ept> tab. Using the <bpt id="p2">**</bpt>Lifecycle services help configuration<ept id="p2">**</ept> list box, select the LCS project that you uploaded the PBIX file to.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ヘルプ<ept id="p1">**</ept> タブを選択します。<bpt id="p2">**</bpt>Lifecycle Services のヘルプ構成<ept id="p2">**</ept> ボックスの一覧を使って、PBIX ファイルをアップロードした LCS プロジェクトを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>This form will only show the LCS projects that the current user has access to.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">このフォームには、現在のユーザーがアクセスできる LCS プロジェクトのみが表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>If this step is being performed by an administrator, either the administrator needs to have access to the project, or the PBIX artifacts need to be imported into a project that the administrator has access to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップが管理者によって実行される場合、管理者がプロジェクトにアクセスする必要があるか、または PBIX コンポーネントが管理者がアクセスできるプロジェクトにインポートする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Publish Power BI reports to a production environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI レポートを実稼働環境に公開</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Open <bpt id="p1">**</bpt>System Administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Deploy PowerBI<ept id="p3">**</ept> from the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントから<bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1">&amp;gt;</ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph2">&amp;gt;</ph><bpt id="p3">**</bpt>PowerBI の配置<ept id="p3">**</ept>を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>You will see the file that you uploaded to LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS にアップロードしたファイルが分かります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Select the <bpt id="p1">**</bpt>Sales Report<ept id="p1">**</ept> file and select the <bpt id="p2">**</bpt>Deploy Power BI files<ept id="p2">**</ept> option on the menu bar.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>売上報告書<ept id="p1">**</ept> ファイルを選択し、メニュー バーで <bpt id="p2">**</bpt>Power BI ファイルの配置<ept id="p2">**</ept>オプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>You may be asked to consent publishing to the PowerBI.com service.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match">PowerBI.com サービスへの公開に同意するよう求められる場合があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Click the link to provide consent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同意するには、リンクをクリックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>When consent is complete, you need to go back to the original browser window and click the <bpt id="p1">**</bpt>Close<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同意が完了すると、元のブラウザー ウィンドウに戻り、<bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept> ボタンをクリックする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>After you successfully publish the file, the Power BI report will appear in your PowerBI.com subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルを正常に公開した後、Power BI レポートは PowerBI.com サブスクリプションに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>You will notice that the report now points to the entity store in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートが実稼働環境にあるエンティティ格納を現在指さしていることがわかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Continuing with PowerBI.com</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PowerBI.com での継続</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>As an administrator or a power user, you have successfully authored and published a Power BI report to the production environment using the entity store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者またはパワーユーザーは、エンティティ格納を使用して実稼動環境に Power BI レポートを作成し公開することに成功しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>You can perform several additional steps using Power BI functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI 機能を使用して、いくつかの追加手順を実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Optionally, you can apply record-level security to the dataset to restrict users from seeing data they are not allowed to view in Power BI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、データセットにレコード レベルのセキュリティを適用して、Power BI での表示が許可されていないデータの表示をユーザーに制限することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>You can create an organizational content pack and share it among users in a group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">組織のコンテンツ パックを作成して、グループ内のユーザーの間で共有することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>You can export datasets, reports, and dashboards from your PowerBI.com instance as a new content pack to a selected group of users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PowerBI.com インスタンスから、データベース、レポート、およびダッシュボードを、新しいコンテンツパックとして、選択したユーザーのグループにエクスポートすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Note that organizational content packs adhere to any record-level security rules that you defined at the dataset level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">組織のコンテンツ パックは、データセット レベルで定義した任意のレコード レベルのセキュリティ ルールに従うことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Users can personalize their workspaces by adding Power BI tiles or reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI タイルまたはレポートを追加することによって、自分のワークスペースをパーソナライズできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加リソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source><bpt id="p1">[</bpt>Modeling and using aggregate data<ept id="p1">](../analytics/model-aggregate-data.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>集計データのモデリングと使用<ept id="p1">](../analytics/model-aggregate-data.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
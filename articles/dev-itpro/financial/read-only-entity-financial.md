<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="read-only-entity-financial.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>read-only-entity-financial.bdae5b.092f7e566c6ac14421e772f538a61af6fa0ef2d7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>092f7e566c6ac14421e772f538a61af6fa0ef2d7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\financial\read-only-entity-financial.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Create read-only entities that expose financial dimensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コードを公開する読み取り専用エンティティの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>In this topic, we describe how to build an entity for registered transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、登録済のトランザクションのエンティティを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Create read-only entities that expose financial dimensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コードを公開する読み取り専用エンティティの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>"<ph id="ph1">[!include [banner](../includes/banner.md)]</ph>"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"<ph id="ph1">[!include [banner](../includes/banner.md)]</ph>"</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In this topic, we describe how to build an entity for registered transactions that are registered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、登録されている登録済のトランザクションのエンティティを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic comes from Per Baarsoe Jorgensen of the Solutions Architecture team.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、ソリューション アーキテクチャ チームの Per Baarsoe Jorgensen から得たものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>It describes a real-world scenario that we have encountered as we work with customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客と作業時に発生した実際のシナリオを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Imagine a scenario where we must expose all vendor invoice line transactions together with the financial dimensions that were applied through the distributions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配分を使用して適用された財務分析コードと共にすべての仕入先請求明細行のトランザクションを公開しなければならないシナリオを考えてみましょう。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Because easy consumption by a third-party tool is essential, we will create an entity for this scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サード パーティのツールによる簡単な消費が不可欠なので、このシナリオ用のエンティティを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>As a result, the entity should not have to be joined with other related entities but should be able to provide value on its own.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果として、エンティティは他の関連するエンティティと結合する必要はなく、単独で値を提供できるべきです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>We will walk through the process of creating a sample entity to meet these requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの要件を満たすために、サンプル エンティティを作成するプロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>(We will leave out instructions for integrating with Microsoft Azure DevOps, because those steps are already well documented.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(これらの手順はすでに文書化されているため、Microsoft Azure DevOps との統合の手順は省略します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Create a basic entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本エンティティの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The first step is to create a new element in a project by selecting <bpt id="p1">**</bpt>New Item<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のステップは、<bpt id="p1">**</bpt>新しい品目<ept id="p1">**</ept> を選択して、プロジェクト内に新しい要素を作成することです。.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>New item</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい項目</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>In the form that opens, under Data Model, we select the <bpt id="p1">**</bpt>Data Entity<ept id="p1">**</ept> element type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開いているフォームで、データ モデルの<bpt id="p1">**</bpt>データ エンティティ<ept id="p1">**</ept>要素のタイプを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Data element</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ要素</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Be careful when you name the entity, because you can’t rename it later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後で名前を変更できないためエンティティに名前を付けるときは注意が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Next, in the Data Entity wizard, we select the appropriate primary data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、データ エンティティ ウィザードで、適切なプライマリ データ ソースを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>For our scenario, this data source is VendInvoiceTrans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオでは、このデータ ソースは VendInvoiceTrans です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Data entity wizard</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ ウィザード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The wizard doesn’t accept tables that don’t have a natural key, as is the case with VendInvoiceTrans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendInvoiceTrans の場合のように、ウィザードは自然キーを持たないテーブルを受け入れません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Therefore, we receive the following error message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、次のエラー メッセージが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Natural key error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナチュラル キーのエラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The workaround is to select any other primary data source that has a natural key associated, such as VendGroup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を回避するには、VendGroup などの自然なキーが関連付けられている他のプライマリ データ ソースを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Because we don’t really need this data source, we also don’t need any fields for it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータ ソースは実際には必要ないので、フィールドも必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Therefore, we clear the <bpt id="p1">**</bpt>Select all<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p1">**</bpt>すべて選択<ept id="p1">**</ept> チェック ボックスをオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Clear select all</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての選択を解除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Finally, we create the template for our entity by clicking <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、<bpt id="p1">**</bpt>完了<ept id="p1">**</ept>をクリックして、エンティティのテンプレートを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Customize the basic entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本的なエンティティをカスタマイズします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The entity, staging table, and security assets have been created, and we can now produce our custom entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ、ステージング テーブル、およびセキュリティ資産が作成され、カスタム エンティティを作成できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In the project, we open the VendorInvoiceTransactionDetailsEntity entity in the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトでは、デザイナーで VendorInvoiceTransactionDetailsEntity エンティティを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>VendorInvoiceTransactionDetailsEntity in designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーの VendorInvoiceTransactionDetailsEntity</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In the designer, we replace the dummy table (VendGroup) that we applied in the wizard with the transaction table VendInvoiceTrans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーで、ウィザードに適用したダミー テーブル (VendGroup) を、トランザクション テーブル VendInvoiceTrans に変えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Because we didn't choose to add the fields, we don't have to remove fields in the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドの追加を選択しなかったため、エンティティのフィールドを削除する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Data Entity Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのタイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Because we are exposing transactional data by using this entity, it's important that we mark the entity as read-only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエンティティを使用してトランザクション データを公開するため、エンティティを読み取り専用としてマークすることが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Therefore, we set the <bpt id="p1">**</bpt>Is read only<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> on the top node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、トップ ノードで <bpt id="p1">**</bpt>Is read only<ept id="p1">**</ept> プロパティを <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Because accounting distributions are versioned, it's important that only the current version be returned when we query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">勘定配布はバージョン管理されているため、クエリを実行するときに現在のバージョンのみが返されることが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Therefore, we create a view that makes this part easily reusable across multiple entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、この部分を複数のエンティティ間で簡単に再利用できるようにするビューを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Replace with VendInvoiceTrans</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendInvoiceTrans と置き換え</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the properties, we assign <bpt id="p1">**</bpt>ReferenceDistribution<ept id="p1">**</ept> a range filter value of <bpt id="p2">**</bpt>0<ept id="p2">**</ept> and <bpt id="p3">**</bpt>ReferenceRole<ept id="p3">**</ept> a range filter value of <bpt id="p4">**</bpt>1<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティで、<bpt id="p1">**</bpt>ReferenceDistribution<ept id="p1">**</ept> に <bpt id="p2">**</bpt>0<ept id="p2">**</ept> の範囲フィルター値、<bpt id="p3">**</bpt>ReferenceRole<ept id="p3">**</ept> に <bpt id="p4">**</bpt>1<ept id="p4">**</ept> の範囲フィルター値を代入します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The join mode property for the AccountDistributionReverse data source must be <bpt id="p1">**</bpt>NoExistsJoin<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AccountDistributionReverse データ ソースの結合モード プロパティは、<bpt id="p1">**</bpt>NoExistsJoin<ept id="p1">**</ept> である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>After the new view is in place, we can add it to the VendorInvoiceTransactionDetailsEntity entity that we are currently building.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいビューを配置した後、現在作成している VendorInvoiceTransactionDetailsEntity エンティティに追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Add to VendorInvoiceTransactionDetailsEntity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendorInvoiceTransactionDetailsEntity の追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Expose financial dimensions as fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コードをフィールドとして公開</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The next important step is to expose the financial dimensions as separate fields on the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の重要なステップは、財務分析コードをエンティティ上の異なるフィールドとして公開することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Because our scenario builds on top of a posted transaction, we must add the fields to the DimensionCombinationentity entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオは転記済トランザクションの上に構築されるため、フィールドを DimensionCombinationentity エンティティに追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>We want to make the adjustments in a resilient manner by using the extension approach, so that minimal maintenance will be required when we upgrade the code base to newer versions in the future.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能による方法を使用して復元力のある方法で調整を行います。これにより、コード ベースを新しいバージョンに今後アップグレードするとき、必要なメンテナンスは最小限になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition version 1611</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition バージョン 1611</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>For version 1611 or later, you should use the wizard that is available in Microsoft Visual Studio (at <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Addins<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Add financial dimensions for Odata<ept id="p3">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン 1611 以降については、Microsoft Visual Studio (<bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アドイン<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Odata の財務分析コードの追加<ept id="p3">**</ept>) で利用できるウィザードを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For instructions, see <bpt id="p1">[</bpt>Add dimensions to the Microsoft Excel template<ept id="p1">](dimensions-overview.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順については、「<bpt id="p1">[</bpt>Microsoft Excel テンプレートに分析コードを追加する<ept id="p1">](dimensions-overview.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Earlier versions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前のバージョン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>If you're working with earlier versions, you must complete the steps that are outlined here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前のバージョンで作業している場合、ここで説明されている手順を完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>First, we add the entity extension itself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、エンティティ拡張機能自体を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Select <bpt id="p1">**</bpt>Create extension<ept id="p1">**</ept> on the context menu (shortcut menu).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテキスト メニュー (ショートカット メニュー) で <bpt id="p1">**</bpt>拡張機能を作成<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Next, we create the code that retrieves the data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、データを取得するコードを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Because the entity extension is already in place, we must create a new class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ拡張子が既に確立されているため、新しいクラスを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The following example adds code for an arbitrary dimension that is named <bpt id="p1">**</bpt>ProductLine<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>ProductLine<ept id="p1">**</ept> という名前の任意の分析コードを追加します。.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>[ExtensionOf(dataentityviewstr(DimensionCombinationentity))] public final class DimensionCombinationentity_Extension { private static server str getEmptyOrDimensionValueSqlString(str _attributeName) { str sqlStatement;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[ExtensionOf(dataentityviewstr(DimensionCombinationentity))] public final class DimensionCombinationentity_Extension { private static server str getEmptyOrDimensionValueSqlString(str _attributeName) {str sqlStatement;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>We now add fields to the newly created entity extension by using custom fields that reference these methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドを参照するカスタム フィールドを使用して、新たに作成されたエンティティ拡張機能にフィールドを追加しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Add fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Next, we set the property values to reflect the fact that the field is unmapped and should be retrieved through the code that we made for the extension class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、フィールドがマップされておらず、拡張機能クラスに対して作成したコードを通じて取得する必要があることを反映するためにプロパティ値を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>When you create the relation, also set the following values:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションを作成するとき、次の値も設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Cardinality: <bpt id="p1">**</bpt>ZeroMore<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カーディナリティ: <bpt id="p1">**</bpt>ZeroMore<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Related data entity: <bpt id="p1">**</bpt>DimensionCombinationentity<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連データ エンティティ: <bpt id="p1">**</bpt>DimensionCombinationentity<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Related data entity cardinality: <bpt id="p1">**</bpt>ZeroOne<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連データ エンティティ カーディナリティ: <bpt id="p1">**</bpt>ZeroOne<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Relationship type: <bpt id="p1">**</bpt>Association<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係タイプ: <bpt id="p1">**</bpt>関連<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Create relation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係の作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>We must fully qualify the data method with the class name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス名でデータ メソッドを完全に修飾する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>We are now ready to add the DimensionCombinationentity entity to our new VendInvoiceTransactionentity entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい VendInvoiceTransactionentity エンティティに DimensionCombinationentity エンティティを追加する準備が整いました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Add DimensionCombinationentity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DimensionCombinationentity の追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Notice that both the AccountingDistributionCurrent and the DimensionCombinationentity entity should be outer-joined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AccountingDistributionCurrent と DimensionCombinationentity エンティティの両方が外部結合であることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Outer join</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部結合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Now, we just have to drag the required fields from the various data sources to the <bpt id="p1">**</bpt>Fields<ept id="p1">**</ept> node on the new entity (that is, to our newly created ProductLine).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで、新しいエンティティで必須フィールドをさまざまなデータ ソースから<bpt id="p1">**</bpt>フィールド<ept id="p1">**</ept> ノード (つまり、新たに作成された ProductLine) にドラッグする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Drag to ProductLine</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProductLine にドラッグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>We should add a key to the entity to enable the incremental update functionality during the export configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートの構成時に差分更新機能を有効にするために、エンティティにキーを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Therefore, we must make sure that RecId from the VendInvoiceTrans data source is part of the fields named e.g. VendInvoiceTransRecId.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、VendInvoiceTrans データ ソースの RecId が、たとえば VendInvoiceTransRecId と名付けられたフィールドの一部であることを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>After the field is in the field list, we can drag it to the <bpt id="p1">**</bpt>EntityKey<ept id="p1">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドがフィールドリストに入った後、フィールドを <bpt id="p1">**</bpt>EntityKey<ept id="p1">**</ept> ノードにドラッグできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Drag to EntityKey</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EntityKey にドラッグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>To make sure that the staging table is associated with the fully configured entity, we must update it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステージング テーブルが完全に構成されたエンティティに関連付けられていることを確認するには、ステージング テーブルを更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>On the context menu for the entity, we select <bpt id="p1">**</bpt>Update staging table<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのコンテキスト メニューで、<bpt id="p1">**</bpt>ステージング テーブルの更新<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Update staging table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステージング テーブルの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The entity work is now complete, and we can build it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの作業が完了したら、それを構築することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>In this scenario, a LedgerDimension was associated with the DimensionCombinationentity entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオでは、LedgerDimension が DimensionCombinationentity エンティティに関連付けられました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>In scenarios where there is a DefaultDimension, we must associate it with the DimensionSetentity entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DefaultDimension があるシナリオでは、DimensionSetentity エンティティに関連付ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The improvements and extensions that are required are identical to the improvements and extensions that we made to the DimensionCombinationentity entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な強化と拡張は、DimensionCombinationentity エンティティに対して行った強化と拡張と同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加リソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">[</bpt>Export Dynamics AX 7 Entities to your own Azure SQL Database<ept id="p1">](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/27/export-dynamics-ax7-entities-to-your-own-azure-sql-database/)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Dynamics AX 7 のエンティティを自分の Azure SQL データベースにエクスポートする<ept id="p1">](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/27/export-dynamics-ax7-entities-to-your-own-azure-sql-database/)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
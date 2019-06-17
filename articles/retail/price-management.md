<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="price-management.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>price-management.9d0b0e.afa553fd0562b306f720f2a30c7f901db7ad1b3a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>afa553fd0562b306f720f2a30c7f901db7ad1b3a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>0fbfb9b0ab78c804f3931a083028d2ce313d6521</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/21/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\price-management.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail sales price management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売販売の価格管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the concepts for creating and managing sales prices in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Retail で販売価格を作成および管理するための概念について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail sales price management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 販売価格の管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information about the process of creating and managing sales prices in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Retail における販売価格の作成と管理のプロセスについて情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>It focuses on the concepts that are involved in this process, and on the effects of the various configuration options for sales prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスに含まれる概念、および販売価格のさまざまなコンフィギュレーション オプションへの影響に焦点を当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Terminology</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">用語</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The following terms are used in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の条件がこのトピックで使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Term</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">期間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Definition, usage, and notes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定義、使用、およびメモ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価額</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The single unit amount that a product sells for in a point of sale (POS) client or on a sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売時点管理 (POS) クライアントまたは販売注文で製品を販売する単一の金額単位。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In this topic, the term <bpt id="p1">*</bpt>price<ept id="p1">*</ept> always refers to the sales price, not the inventory price or cost price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、<bpt id="p1">*</bpt>価格<ept id="p1">*</ept> という用語は在庫価格または原価価格ではなく、常に販売価格を指します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Base price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準価格</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The price that is set in the <bpt id="p1">**</bpt>Price<ept id="p1">**</ept> field on a released product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リリースされた製品の <bpt id="p1">**</bpt>価格<ept id="p1">**</ept> フィールドで設定された価格。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Trade agreement price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">売買契約の価格</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The price that is set on a product or variant by using a trade agreement of the <bpt id="p1">**</bpt>Price (sales)<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>価格 (販売)<ept id="p1">**</ept> タイプの売買契約を使用して、製品またはバリアントに設定されている価格。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Best price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最良価格</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>When more than one price or discount can be applied to a product, the smallest price amount and/or the largest discount amount that produces the lowest possible net amount that the customer must pay.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つ以上の価格または割引が商品に適用される場合、顧客が支払うべき正味金額として生成できる最小金額または最大割引金額になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In this topic, the concept of best price is always referred to as "the best price."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、最良な価格の概念を、常に「最適な価格」と呼びます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This best price differs from and should not be confused with the <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> enumeration value for a discount's concurrency mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この最適な価格は、割引の同時モードの <bpt id="p1">**</bpt>最良価格<ept id="p1">**</ept> 列挙値とは異なり、混同しないようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Price groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格グループ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Price groups are at the heart of price and discount management in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格グループは、Retail で価格と割引管理の中核を成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Price groups are used to assign prices and discounts to retail entities (that is, channels, catalogs, affiliations, and loyalty programs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格グループは、小売エンティティ (つまり、チャンネル、カタログ、所属およびロイヤルティ プログラム) に価格および割引を割り当てるのに使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Because price groups are used for all pricing and discounts, it's very important that you plan how you will use them before you start.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての価格および割引に価格グループを使用するため、開始する前にどのように使用するかを計画することは非常に重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>By itself, a price group is just a name, a description, and, optionally, a pricing priority.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ自体では、価格グループは単に名前、説明、およびオプションで価格決定の優先順位です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The main point to remember about price groups is that they are used to manage the many-to-many relationships that discounts and prices have with retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格グループについて覚えておくべき主要な点は、割引および価格が小売エンティティを持つよう、それらが多対多関係の管理に使用されるということです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The following illustration shows how price groups are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図では、価格グループを使用する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In this illustration, notice that "Price group" is literally at the center of pricing and discount management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この図では、「価格グループ」が文字どおりに価格決定および割引管理の中心であることに注目してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The retail entities that you can use to manage differential prices and discounts are on the left, and the actual price and discount records are on the right.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格および割引の差異を管理するのに使用する小売エンティティは左側に、実際の価格および割引レコードは右側になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">![</bpt>Price groups<ept id="p1">]</ept><bpt id="p2">(./media/PriceGroups.png "</bpt>Price groups<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>価格グループ<ept id="p1">]</ept><bpt id="p2">(./media/PriceGroups.png "</bpt>価格グループ<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>When you create price groups, you should not use a single price group for multiple types of retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格グループを作成するときに、小売エンティティの複数のタイプ用に単一の価格グループを使用するべきではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Otherwise, it can be difficult to determine why a specific price or discount is being applied to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、なぜ特定の価格または割引がトランザクションに適用されるかを特定することは難しくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>As the red dashed line in the illustration shows, Retail does support the core Microsoft Dynamics 365 functionality of a price group that is set directly on a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">図にある赤い点線は、Retail が顧客に直接設定された価格グループのコアな Microsoft Dynamics 365 機能をサポートすることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>However, in this case, you get only sales price trade agreements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、この場合は、販売価格の売買契約のみを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you want to apply customer-specific prices, we recommend that you not set price groups directly on the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客固有の価格を適用する場合は、顧客に直に価格グループを設定しないようお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Instead, you should use affiliations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、所属を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The following sections provide more information about the retail entities that you can use to set distinct prices when the price groups are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、価格グループを使用する際に特徴的価格を設定するのに使用できる、小売エンティティに関する詳細情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The configuration of prices and discounts for all these entities is a two-step process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらすべてのエンティティの価格および割引のコンフィギュレーションには 2 つの手順があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>These steps can be done in either order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの手順は、いずれかの順序で実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>However, the logical order is to set the price groups on the entities first, because this step is likely to be a one-time setup that is done during implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、まず論理的な順序がエンティティの価格グループに設定されます。それはこの手順が実装時に行われる 1 回だけの設定である可能性が高いからです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Then, as prices and discounts are created, you can set the price groups on those prices and discounts individually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、価格と割引が作成され、それらの価格および割引に個別に価格グループを設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Channels</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the retail industry, it's very typical to have different prices in different channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売業界では、異なるチャンネルで異なる価格があるのが最も一般的です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The two primary factors that affect channel-specific prices are costs and local market conditions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャンネル固有の価格に影響を与える 2 つの主要な要素には、原価および国内市場の状況があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Costs<ept id="p1">**</ept> – The farther away a channel is from the product source, the more it costs to stock a product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>原価<ept id="p1">**</ept> – 製品ソースからチャンネルが離れる分、製品の保管にさらに費用がかかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>For example, fresh produce has a limited shelf life and specific production requirements (for example, a growing season).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、新規生産には限定される消費期限および特定の生産要件 (たとえば、増大する時期) があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>During the winter, fresh lettuce likely costs more in northern climates than in southern climates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">冬の間、新鮮なレタスの価格は南の気候よりも北の気候で高くなる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If you're setting prices for channels over a large geographical area, you will probably want to set different prices in different channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">大規模な地理的領域にわたってチャンネルの価格を設定する場合、異なるチャンネルに異なる価格を設定する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">**</bpt>Local market conditions<ept id="p1">**</ept> – A store that has a direct competitor across the street will be much more price-sensitive than a store that doesn't have a direct competitor nearby.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>国内市場の状況<ept id="p1">**</ept> – 直接競合他社が目の前にある店舗は、直接競合他社が付近にない店舗よりもさらに価格の影響を受けやすくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Affiliations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">所属</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The general definition of an affiliation is a link to or association with a group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">所属の一般的な定義は、グループにまたはグループの関連へのリンクです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>In Retail, affiliations are groups of customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail では、所属は顧客のグループです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Affiliations are a much more flexible tool for customer pricing and discounts than the core Microsoft Dynamics 365 concept of customer groups and discount groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">所属は、顧客グループおよび割引グループの Microsoft Dynamics 365 コア概念よりも、顧客が価格決定および割引をするのにより柔軟なツールです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>First, an affiliation can be used for both prices and discounts, whereas non-retail pricing has a different group for each type of discount and price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、所属は価格および割引の両方を使用できますが、非小売価格は価格の種類ごとに異なるグループを持ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Next, a customer can belong to multiple affiliations but can belong to only one non-retail pricing group of each type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、顧客は複数の所属に属することができますが、各タイプの 1 つの非小売価格決定グループにのみ属することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Finally, although affiliations can be set up so that they are linked to a customer, they don't have to be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、顧客にリンクされるように所属を設定できますが、必須ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>An ad-hoc affiliation can be used for anonymous customers at the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アドホック所属は、POS での匿名顧客に対して使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>A typical example of an anonymous affiliation discount is a senior or student discount, where a customer can receive a discount just by showing a group membership card.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">匿名所属の割引の一般的な例としてシニアまたは学生割引がありますが、顧客がグループ メンバーシップ カードを表示するだけで割引を受けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Although affiliations are most often associated with discounts, you can also use them to set differential pricing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、所属は割引に関連付けられているため、価格決定の差異を設定するのに使用することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For example, when a retailer sells to an employee, it might want to change the selling price instead of applying a discount on top of the regular price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、小売業者が従業員に販売する場合、正規の価格の上に割引を適用するのでなく、販売価格を変更する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>As another example, a retailer that sells to both consumer customers and business customers might offer business customers better prices, based on their purchasing volume.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別の例として、消費者顧客と法人顧客の両方に販売する小売業者は、法人顧客にはその購買数量に基づいて、より良い価格を提供する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Affiliations enable both these scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">所属は、どちらのシナリオも有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Loyalty programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロイヤルティ プログラム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>In relation to prices and discounts, loyalty programs are basically just an affiliation that has a special name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格と割引に関連して、ロイヤルティ プログラムは基本的に単に特別な名前を持つ所属です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Both prices and discounts can be set for a loyalty program, just as they can be set for an affiliation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">所属に対して設定するのと同様に、価格と割引の両方を、ロイヤルティ プログラムに対して設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>However, the way that customers get loyalty pricing during a transaction or order differs from the way that they get affiliation pricing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、顧客がトランザクションまたは注文時にロイヤルティ 価格を取得する方法は、所属価格を取得する方法とは異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Customers can get loyalty pricing only if a loyalty card is added to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客は、ロイヤルティ カードがトランザクションに追加された場合にのみロイヤルティ価格を取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>When a loyalty card is added to a transaction, the loyalty program is also added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションにロイヤルティ カードを追加するときに、ロイヤルティ プログラムも追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The loyalty program then enables special prices and discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロイヤルティ プログラムは、特別価格と割引を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Loyalty programs can have multiple tiers, and the discounts can differ for different tiers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロイヤルティ プログラムには複数の層があり、さまざまな層によって割引も異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>In this way, retailers can give frequent customers larger rewards without having to manually put those customers into a special group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、小売業者は得意先を手動で特殊グループに入れることなく、より大きな特典をそれらの顧客に提供できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Loyalty programs have additional functionality besides prices and discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロイヤルティ プログラムには、価格と割引以外にも追加の機能があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>However, from the perspective of pricing and discounts, they are the same as affiliations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、価格と割引側から、それらは所属として同じものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Catalogs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カタログ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Some retailers use physical or virtual catalogs to market products to, and price them for, focused groups of customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部の小売業者は製品の販売、およびフォーカスのある顧客グループに対する価格決定をするのに、現物または仮想カタログを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>As part of their business model to target marketing via a catalog, these retailers can set differential prices on their various catalogs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カタログを通してターゲット マーケティングへのビジネス モデルの一部として、これらの小売業者は、さまざまなカタログで差異価格を設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Microsoft Dynamics 365 supports this capability by letting you define catalog-specific discounts and prices, just as you can define channel-specific or affiliation-specific discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 では、チャンネル固有または所属固有の割引を定義できるのと同じように、カタログ固有の割引と価格を定義するよう、この機能をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>When you edit a catalog, you can associate price groups with the catalog, just as you can associate them with a channel, affiliation, or loyalty program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カタログを編集する際に、価格グループにチャンネル、所属、またはロイヤルティ プログラムに関連付けることができるのと同じように、価格グループにカタログを関連付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Best practices for price groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格グループに対するベスト プラクティス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Don't use a price group for multiple retail entity types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の小売エンティティ タイプに価格グループを使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Instead, use one set of price groups for channels, a different set of price groups for affiliations or loyalty programs, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、チャンネルに対して価格グループの 1 つのセット、所属またはロイヤルティ プログラムに対して異なる価格グループのセットなどを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>You can use a prefix or suffix in the name of the price group to visually group the various types of price groups that you're using.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用している価格グループのさまざまな種類を視覚的にグループ化するため、価格グループの名前の接頭語や接尾辞を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Avoid setting price groups directly on a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客に直接価格グループを設定することは避けてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Instead, use an affiliation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、所属を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In this way, you can assign all types of prices and discounts to customers, not just sales price trade agreements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、単なる販売価格の売買契約でなく、顧客に価格と割引のすべてのタイプを割り当てることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Pricing priority</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格決定優先順位</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>By itself, a pricing priority is just a number and a description.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ自体では、価格決定の優先順位は、単に番号と説明です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Pricing priorities can be applied to price groups, or they can be applied directly to discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格決定の優先順位は価格グループに適用でき、または割引に直接適用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>When pricing priorities are used, they let a retailer override the principle of the best price by controlling the order in which prices and discounts are applied to products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格決定の優先順位を使用する場合、製品にどの価格および割引が適用されるかの順序を管理することにより、最適な価格の原則を小売業者が上書きできるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>A larger pricing priority number is evaluated before a lower pricing priority number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">大きな価格決定の優先順位番号は、小さい価格決定の優先順位番号の前に評価されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Additionally, if a price or discount is found at any priority number, all prices or discounts that have lower priority numbers are ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、優先順位番号で価格または割引が見つかると、小さい優先順位番号を持つすべての価格または割引が無視されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The price and a discount can come from two different pricing priorities, because pricing priorities apply to prices and discounts independently.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格決定の優先順位は価格と割引別個に適用されるため、価格と割引は 2 つの異なる価格決定の優先順位から取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>To use pricing priority for prices, you must assign a pricing priority to a price group and then create a sales price trade agreement for that price group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格決定の優先順位を価格に対して使用するには、価格グループに価格決定の優先順位を割り当て、次にその価格グループに対する販売価格の売買契約を作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The pricing priority feature was introduced to support the scenario where a retailer wants to apply higher prices in a specific set of stores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格決定の優先順位機能は、小売業者が店舗の特定のセットでより高い価格を適用するシナリオをサポートするために導入されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For example, a retailer has defined regional prices for the east coast of the United States but wants higher prices for some products in New York City stores, because it costs more to sell some products in the city, and/or because the local market will bear a higher price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、小売業者が、米国の東海岸での地域価格を定義したがニューヨーク市内の店舗では一部の製品により高い価格を設定するとします。その理由として、市内でいくつかの製品を販売するにはさらに費用がかかる、またはローカル市場がより高い価格を負担することになる点が考えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>As was described in the "Best price" section of this topic, the retail pricing engine typically selects the lower of two prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックの「最適な価格」セクションで説明されたとおり、小売り価格決定エンジンは通常価格の低い方の 2 つを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Therefore, the retailer is usually prevented from using the higher of two prices in a store that has both the East coast and New York price groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、通常東海岸およびニューヨークの価格グループの両方を持つストアで、小売業者が高い方の価格の 2 つを使用するのを阻止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>To resolve this issue before the pricing priority feature was introduced, the retailer had to define prices for every product two times and not assign both price groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格決定の優先順位機能が導入される前にこの問題を解決するには、小売業者はすべての製品に対して 2 度価格を定義して、両方の価格グループを割り当てないようにする必要がありました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Alternatively, the retailer had to create extra price groups to isolate the products that have higher prices from products that have the usual, lower prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、小売業者は、より高い価格の製品を通常または低い価格の製品から取り分けるため、追加の価格グループを作成する必要がありました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>However, the pricing priority feature lets the retailer create a pricing priority for store prices that is higher than the pricing priority for regional prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、価格決定の優先順位機能は、小売業者が地域価格に対する価格決定の優先順位よりも、高い店舗価格に対する価格決定の優先順位を作成できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Alternatively, the retailer can create a pricing priority just for store prices and leave regional prices at the default pricing priority, which is 0 (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、小売業者は店舗価格に対してのみ価格決定の優先順位を作成し、地域価格を既定の価格決定の優先順位である、0 (ゼロ) のままにできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Both setups help guarantee that store prices will always be used before regional prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">両方の設定とも、地域価格以前に店舗価格を常に使用することを保証する助けになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Pricing priority example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格決定優先順位例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Let's look at an example where store prices override other prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで、店舗価格が他の価格を上書きする例を見ます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>A national retailer sets most prices per region, and it has four regions: North east, South east, Mid-west and West.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">国内の小売業者は地域ごとに大抵の価格を設定し、それには 4 つの地域が含まれます: 北東部、南東部、中西部および西部。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It has identified several high-cost markets that can support higher prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の高コスト市場が高い価格をサポートできることが確認されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>These markets are in New York City, Chicago, and the San Francisco Bay area.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの市場は、ニューヨーク市、シカゴ、およびサンフランシスコ湾近郊にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>For this example, we will drill into the North east region.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、北東地域にドリルダウンします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Store 1 is in Boston, and store 2 is in Manhattan.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗 1 はボストンに、店舗 2 はマンハッタンにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>For the Boston store, two price groups are linked to the channel: North East and Store 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボストンの店舗に対して、2 つの価格グループがチャンネルにリンクされています: 北東および店舗 1。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>For the Manhattan store, three price groups are linked to the channel: North East, NYC, and Store 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マンハッタンの店舗に対して、3 つの価格グループがチャンネルにリンクされています: 北東、ニューヨーク市、および店舗 2。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>The retailer sets up two pricing priorities: High cost has a priority number of 5, and Store prices has a priority number of 10.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売業者は、2 つの価格決定の優先順位を設定します: 5 の優先順位番号がある高コスト、および 10 の優先順位番号がある店舗価格。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>(Remember that, by default, the pricing priority is 0 <ph id="ph1">\[</ph>zero<ph id="ph2">\]</ph>, and a price or discount that has a higher priority number is used before a price or discount that has a lower priority number.) For the North East price group, the pricing priority is left at the default value of <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(既定では、価格決定の優先順位が 0 <ph id="ph1">\[</ph>ゼロ<ph id="ph2">\]</ph>であり、高い優先順位番号を持つ価格または割引が低い優先順位番号を持つ価格または割引より前に使用される点に注意してください。) 北東価格グループに対して、価格決定の優先順位は既定値の <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (ゼロ) になっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>For the NYC price group, the pricing priority is set to <bpt id="p1">**</bpt>5<ept id="p1">**</ept>, because New York City is a high-cost market.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ニューヨーク市価格グループに対して、価格決定の優先順位が <bpt id="p1">**</bpt>5<ept id="p1">**</ept> に設定されているのは、ニューヨークは高コスト市場であるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>For the Store 1 and Store 2 price groups, the pricing priority is set to <bpt id="p1">**</bpt>10<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗 1 および店舗 2 の価格グループに対して、価格決定の優先順位を <bpt id="p1">**</bpt>10<ept id="p1">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Two products that the retailer sells are product 1, a commodity T-shirt, and product 2, brand-specific fashion jeans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売業者が販売する 2 つの製品は、製品 1、商品 T シャツ、および製品 2、ブランド固有ファッション ジーンズです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Product</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">品目</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>North East price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">北東価格</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>NYC price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ニューヨーク市価格</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Store price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗価格</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>T-shirt</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">T シャツ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>$15</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Fashion jeans</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファッション ジーンズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>$50</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$50</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>$70</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$70</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The T-shirt sells for the same price (that is, $15) at both the Boston and Manhattan stores, because only one price is set in the North East price group that is linked to both channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">T シャツはボストンとマンハッタンの両方の店舗で同じ価格 (つまり、$15) で販売されます。それは 1 つの価格のみが両方のチャンネルにリンクされている北東価格グループで設定されているためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The fashion jeans sell for $50 in the Boston store, because that price is the only price that is available in that store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファッション ジーンズはボストンで $50 で販売されます。その価格がその店舗で利用可能な唯一の価格であるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>However, in the Manhattan store, two prices are available: $50 and $70.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、マンハッタンの店舗では、2 つの価格が利用可能です: $50 および $70。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Because the pricing priority of 5 for the NYC price group is higher than the pricing priority of 0 (zero) for the North East price group, the price will be rung up as $70 in the POS system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ニューヨーク市価格グループの価格決定の優先順位 5 が、北東価格グループの価格決定の優先順位 0 (ゼロ) よりも高いため、価格は POS システムで $70として繰り上げられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>For each pricing priority, a full pass through the logic for the retail pricing engine is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各価格決定の優先順位に対して、小売価格決定エンジンに対するロジックの完全な通過が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Therefore, to help maintain the performance of the price and discount calculation, you should use pricing priorities sparingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、価格および割引の計算のパフォーマンスを維持するために、価格決定の優先順位を控えめに使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Types of prices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格の種類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>In Microsoft Dynamics 365, you can set the price of a product in three places:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 では、次の 3 つの箇所で、商品の価格を設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Directly on the product (base price)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">直接製品に対して (基準価格)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In a sales price trade agreement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売価格の売買契約で</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>In a price adjustment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格調整で</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The base price and trade agreement price are part of core Microsoft Dynamics 365, and are available even if you don't use Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準価格および売買契約の価格は Microsoft Dynamics 365 コアの一部であり、Retail を使用していない場合でも利用可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The price adjustment functionality is available only in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格調整機能は、Retail でのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>The next section provides more information about each of these options for setting prices and explains how the options work together.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、価格を設定するためのこれらの各オプションについて情報を提供し、オプションが動作する方法ついて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Setting prices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格の設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Base price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準価格</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The easiest place to set the price for a product is directly on the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">商品の価格を設定する最も簡単な箇所は、直接製品に対してです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>The value that you set directly on a product is often referred to as the base price for the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品に直接設定した値は、製品の基準価格とも呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>You set the base price in the <bpt id="p1">**</bpt>Price<ept id="p1">**</ept> field on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Released product details<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>リリース済製品の詳細<ept id="p3">**</ept> ページの <bpt id="p2">**</bpt>販売<ept id="p2">**</ept> タブにある <bpt id="p1">**</bpt>価格<ept id="p1">**</ept> フィールドで、基準価格を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>The value that you enter is in the company currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社基本通貨で値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>By default, the price is for a quantity of 1 of the unit of measure (UoM) that is set in the <bpt id="p1">**</bpt>Unit<ept id="p1">**</ept> field on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab. The actual price per unit of a product is based on the UoM, the price quantity, and the currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、測定単位 (UOM) の 1 の数量の価格が <bpt id="p2">**</bpt>販売<ept id="p2">**</ept> タブの <bpt id="p1">**</bpt>単位<ept id="p1">**</ept> フィールドで設定されています。製品の単位あたりの実際の価格は UOM、価格数量、および通貨に基づきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If a product has one price for everyone, the base price offers the most efficient way to manage the price of that product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全ユーザーに対して商品に 1 つの価格がある場合、基準価格は商品の価格を管理する最も効率的な方法を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Even if you use trade agreements to set prices, you might also set the base price on a product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格を設定するのに売買契約を使用したとしても、商品の基準価格を設定する可能性もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Then, if you don't use an <bpt id="p1">**</bpt>All<ept id="p1">**</ept> trade agreement, you have a fallback price that is used when no trade agreement applies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>すべて<ept id="p1">**</ept> の売買契約を使用しない場合、売買契約が適用されない場合に使用される予備価格があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>If a retail channel's currency differs from the company currency, the base price in that retail channel is determined by using currency conversion on the price that is set on the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャンネルの通貨が会社基本通貨と異なる場合は、商品に設定されている価格の通貨換算を使用してその小売チャンネルの基準価格が決定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Although the price unit isn't a common retail scenario, the retail pricing engine supports it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格単位が一般的な小売シナリオではありませんが、小売価格決定エンジンがそのサポートをします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>If the price unit is set to a value other than <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero), the price per unit equals Price ÷ Price unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格単位が <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (ゼロ) 以外の値に設定されている場合、単位あたりの価格は価格 ÷ 価格単位と等しくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>For example, if a product's price is $10.00, and the price unit is 50, the price for a quantity of 1 is $0.20 (= $10.00 ÷ 50).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、商品の価格が $10.00、価格単位が 50 の場合、数量 1 に対する価格は $0.20 (= $10.00 ÷ 50) となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Sales price trade agreement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売価格の売買契約</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>By using the trade agreement journal, you can create sales price trade agreements for each product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">売買契約仕訳帳を使用することにより、各商品の販売価格の売買契約を作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>In Microsoft Dynamics 365, there are three customer scopes for sales price trade agreements: <bpt id="p1">**</bpt>Table<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Group<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>All<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 では、販売価格の売買契約の 3 つの顧客スコープがあります: <bpt id="p1">**</bpt>テーブル<ept id="p1">**</ept>、<bpt id="p2">**</bpt>グループ<ept id="p2">**</ept>、および<bpt id="p3">**</bpt>すべて<ept id="p3">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The customer scope determines the customers that a given sales price trade agreement applies to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客スコープは、特定の販売価格の売買契約が適用される顧客を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>A <bpt id="p1">**</bpt>Table<ept id="p1">**</ept> sales price trade agreement is for a single customer that is set directly on the trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル<ept id="p1">**</ept> 販売価格の売買契約は、売買契約に直接設定されている単一の顧客に対するものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>This scenario isn't a typical retail business-to-consumer (B2C) scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオは、一般的な企業と顧客間 (B2C) シナリオではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>However, if it occurs, the retail pricing engine uses <bpt id="p1">**</bpt>Table<ept id="p1">**</ept> trade agreements when it determines price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、そうなる場合、価格を決定する際に小売価格決定エンジンは <bpt id="p1">**</bpt>テーブル<ept id="p1">**</ept> 売買契約を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>A <bpt id="p1">**</bpt>Group<ept id="p1">**</ept> sales price trade agreement is the type that is most often used with retail functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>グループ<ept id="p1">**</ept> 販売価格の売買契約は、小売機能を最もよく使用するタイプです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Outside Retail, <bpt id="p1">**</bpt>Group<ept id="p1">**</ept> sales price trade agreements are for a simple customer group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 以外では、<bpt id="p1">**</bpt>グループ<ept id="p1">**</ept> 販売価格の売買契約は、単純な顧客グループに対するものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>However, in Retail, the concept of a customer group has been extended so that it's a more generic retail price group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、Retail では、顧客グループの概念が拡張されたため、より一般的な小売価格グループに対するものになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>A price group can be linked to a retail channel, affiliation, loyalty program, or catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格グループは、小売チャンネル、所属、ロイヤルティ プログラム、またはカタログにリンクすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>For detailed information about price groups, see the "Price groups" section earlier in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格グループの詳細については、このトピックの「価格グループ」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>A trade agreement price is always used before the base price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">売買契約価格は、基準価格より前に常に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Price adjustment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格調整</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>As the name implies, a price adjustment is used to modify the price that was either set directly on the product or set by using a trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前が意味するように、商品に対して直接設定されたかまたは売買契約を使用して設定されたかのいずれかの価格を変更するのに、価格調整を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>A price adjustment can be used only to lower the price, not raise it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格調整は、価格を上げるのでなく、下げる場合にのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>A price adjustment is the recommended way for retailers to create, track, and manage price markdowns for their products over time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売業者が長期にわたる自社製品の作成、追跡、および価格値下げを管理する方法として、価格調整をお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>There are three types of price adjustments: percentage off, amount off, and price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格調整の 3 つのタイプがあります: パーセント割引、金額割引、および価格。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>A price adjustment of the percentage off or amount off type is always applied to a sale transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パーセント割引または金額割引タイプの価格調整は、常に販売トランザクションに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>However, a price adjustment of the price type is applied only if the adjusted price is less than the price that was set by using the base price or trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、調整済価格が基準価格または売買契約価格を使用して設定された価格よりも小さい場合にのみ、価格タイプの価格調整が適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Therefore, if the price that is set in a price adjustment is more than the unadjusted price, the price adjustment isn't used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、価格調整で設定された価格が未調整の価格より大きい場合は、価格調整は使用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Determining price for a product in a transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションで商品の価格を決定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>The calculation of the price and discount on a transaction uses the principle of finding the best price for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションでの価格と割引の計算は、顧客に対する最適な価格の検索の原則を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>According to this principle, if more than one price is found, the lowest price is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この原則に従って、1 つ以上の価格が検出された場合、最低価格が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Additionally, the combination of discounts that produces the largest discount amount for the whole transaction is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、トランザクション全体に対する最大割引金額を生成する割引の組み合わせが使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>In some cases, a smaller discount must be used on a single product, so that additional discounts can be applied to other products in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、トランザクションの他の商品に割引の追加が適用されるように、少ない割引は単一の商品に使用される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>The only exception to the principle of finding the best price for the customer is an option for mix-and-match least-expensive discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客に対して最適な価格を検索する原則の唯一の例外は、最安値割引の組み合わせオプションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>This option enables least-expensive discounts that favor the retailer when products are selected and grouped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションは、商品が選択されグループ化される際に、小売業者の優先順位を高くする最安値割引を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Therefore, when a transaction includes more products than are required to qualify for the least-expensive discount, the retail pricing engine selects the products that produce the smallest possible discount amount for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、トランザクションに最安値割引の資格に要求されている以上の商品が含まれている場合、小売価格決定エンジンは顧客に対して最低割引額を生成する商品を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The retail pricing engine returns three prices for every product: the base price, the trade agreement price, and the active price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売価格決定エンジンは、すべての商品に対して 3 つの価格を返します: 基準価格、売買契約の価格、および有効な価格。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>The base price is just the property on the product and is the same for everyone everywhere.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準価格は、単に商品のプロパティであり、どのユーザーにもどの場所でも同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>On the sales price trade agreement, if the <bpt id="p1">**</bpt>Find next<ept id="p1">**</ept> option is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the lowest price that is found for applicable sales price trade agreements is used as the trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売価格の売買契約では、<bpt id="p1">**</bpt>次を検索<ept id="p1">**</ept> オプションが <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> に設定されている場合、適用可能な販売価格の売買契約で検索される最低価格が、売買契約価格として使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Trade agreements can be found by using price groups or the <bpt id="p1">**</bpt>ALL<ept id="p1">**</ept> account code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">売買契約は価格グループまたは <bpt id="p1">**</bpt>すべて<ept id="p1">**</ept> アカウント コードを使用して検出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Alternatively, trade agreements can be assigned directly to a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、売買契約を顧客に直接割り当てることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>If the <bpt id="p1">**</bpt>Find next<ept id="p1">**</ept> option is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>, the first trade agreement price that is found is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次を検索<ept id="p1">**</ept> オプションが <bpt id="p2">**</bpt>いいえ<ept id="p2">**</ept> に設定されている場合、検出される最初の売買契約価格が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>If no sales price trade agreements are found, then the trade agreement price is set equal to the base price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売価格の売買契約が見つからない場合は、基準価格に等しい売買契約価格が設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>The active price is calculated by taking the trade agreement price and applying the largest price adjustment that applies to the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な価格は、売買契約価格を取得し、商品に当てはめる最大価格調整を適用することによって計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>If no price adjustments are found, or if the calculated active price is more than the trade agreement price, the active price is set equal to the trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格調整が見つからない場合、または計算された有効な価格が売買契約価格を超える場合は、有効な価格は売買契約の価格と等しくなるように設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Remember that you can't raise the price of a product by using a price adjustment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格調整を使用して、商品の価格を上げることができないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>The applicable price adjustments can be found only by using price groups that are assigned to a channel, catalog, affiliation, or loyalty program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャンネル、カタログ、所属、またはロイヤルティ プログラムに割り当てられる価格グループを使用することによってのみ、適用可能な価格調整が検出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Category price rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カテゴリ価格ルール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>The category price rules feature in Retail gives you an easy way to create new trade agreements for all the products in a category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail のカテゴリ価格ルール機能は、カテゴリ内のすべての商品に対する新しい売買契約を作成する簡単な方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>This feature also lets you automatically find existing trade agreements for the products in the category and expire them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能により、カテゴリ内で商品に対する既存の売買契約を自動で検索し、破棄することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>When you select the option to expire existing trade agreements, the system creates a new trade agreement journal for the products in the category that have an active trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の売買契約を破棄するオプションを選択すると、システムは、有効な売買契約があるカテゴリ内で、商品に対する新しい売買契約仕訳帳を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>However, the journal must be manually posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、仕訳帳は手動で転記する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Additionally, the category price rules can find existing trade agreements only if you're using the same price rule (that is, if you create a new price rule that uses the same category that was before).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カテゴリ価格ルールは、同じ価格ルールを使用している場合 (つまり、前と同じカテゴリを使用する新しい価格ルールを作成する場合) にのみ、既存の売買契約を検索できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>If you aren't using the same price rule, the existing trade agreements won't be expired.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ価格ルールを使用していない場合は、既存の売買契約は破棄されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>The prices can be increased or decreased by using the <bpt id="p1">**</bpt>Price rule<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Price basis<ept id="p2">**</ept> fields of the category price rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カテゴリ価格ルールの <bpt id="p1">**</bpt>価格ルール<ept id="p1">**</ept> および <bpt id="p2">**</bpt>価格基準<ept id="p2">**</ept> フィールドを使用して、価格を増加または減少できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>In the <bpt id="p1">**</bpt>Price rule<ept id="p1">**</ept> field, select the type of price change to use:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>価格ルール<ept id="p1">**</ept> フィールドで、使用する価格変更のタイプを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source><bpt id="p1">**</bpt>Markup<ept id="p1">**</ept> – A percentage of the price basis is used to calculate the sales price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>マークアップ<ept id="p1">**</ept> – 価格基準のパーセントは販売価格の計算に使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a markup of 50 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例えば、コストが 10.00 で 15.00 で販売される商品に 50 パーセントのマークアップがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source><bpt id="p1">**</bpt>Margin<ept id="p1">**</ept> – A percentage of the sales price is used to calculate the amount of profit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>利益<ept id="p1">**</ept> – 利益量の計算に使用する、販売価格のパーセント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a margin of 33.3 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例えば、コストが 10.00 で 15.00 で販売される商品に 33.3 パーセントの利益があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source><bpt id="p1">**</bpt>Fixed amount<ept id="p1">**</ept> – An amount that is added to the price basis is used to calculate the sales price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>固定金額<ept id="p1">**</ept> – 販売価格の計算に使用する価格基準に追加する金額。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a fixed amount of 5.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例えば、コストが 10.00 で 15.00 で販売される製品に 5.00 の固定量があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>In the <bpt id="p1">**</bpt>Price basis<ept id="p1">**</ept> field, select the type of price to modify:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>価格基準<ept id="p1">**</ept> フィールドで、修正する価格のタイプを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source><bpt id="p1">**</bpt>Base cost<ept id="p1">**</ept> – The amount that the retailer paid to the supplier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>基準原価<ept id="p1">**</ept> – 小売業者が仕入先に支払う金額。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source><bpt id="p1">**</bpt>Base price<ept id="p1">**</ept> – The sales price before trade agreements and price adjustments are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>基準価格<ept id="p1">**</ept> – 売買契約および価格調整が適用される前の販売価格。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source><bpt id="p1">**</bpt>Current price<ept id="p1">**</ept> – The sales price after trade agreements and price adjustments are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>現在の価格<ept id="p1">**</ept> – 売買契約および価格調整が適用される後の販売価格。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>To easily update the prices of various products from different product categories, you can use the supplemental product categories together with the category price rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">異なる製品カテゴリからさまざまな製品の価格を簡単に更新するには、カテゴリ価格ルールとともに補助製品カテゴリを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Best practices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Microsoft SQL Server Express is often used for channel databases because of the cost (free).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server Express は、原価 (無料) のチャンネル データベースのため頻繁に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Keep in mind that SQL Server Express has hardware limitations and limits on data size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Express には、データ サイズ上にハードウェア制限と限度があることに留意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>If you don't plan correctly, you can quickly reach the data size limits of SQL Server Express.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正しく計画しないと、SQL Server Express のデータ サイズ制限にすぐ達してしまいます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>This consideration applies not only to pricing but also to other areas of the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この検討は、価格決定だけでなく、製品の他の部分にも適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Here are a few best practices that can help you reduce the size of your data:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのサイズを小さくするのに役立つ、いくつかのベスト プラクティスを以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>If you're using trade agreements, and your prices change, you should expire the old trade agreements by setting an end date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">売買契約を使用して、価格を変更する場合、終了日を設定することによって古い売買契約を破棄する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Over time, this approach helps reduce the number of trade agreements that are kept in channel databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">時間の経過と共に、この方法により、チャンネル データベースに保存される売買契約の数を削減できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>It also helps reduce the amount of data that the price calculation algorithm must work with.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格計算アルゴリズムと共に作動する価格のデータ量を減らすこともできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>If your prices vary by product variant, consider using the product base price as the price of the most common variant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格が商品バリエーションによって異なる場合は、最も一般的なバリアントの価格として製品の基準価格の使用を検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Then use trade agreements only for the variant prices that are exceptions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外としてバリアント価格に対してのみ売買契約を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>This approach helps reduce the number of trade agreement records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法により、売買契約レコードの数を削減できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Because it's so easy to import data into Microsoft Dynamics 365, you might be tempted to import a trade agreement for every variant of every product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データを Microsoft Dynamics 365 にインポートするのは簡単なので、各製品の各バリアントに対して売買契約をインポートしたくなる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>However, that approach can produce many trade agreements that have the same value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、この方法で、同じ値を持つ多数の売買契約を作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Therefore, it can needlessly increase the size of your data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、データのサイズが不必要に増加してしまいます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Retail processes variant-specific prices in order from most specific to least specific.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail は、最も限定的な組み合わせから最も限定的でない順にバリアント固有の価格を処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>If a product dimension doesn't affect the price, you don't have to define trade agreements for it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品分析コードが価格に影響しない場合は、売買契約を定義する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>For example, a product is available in three colors and four sizes, but the price varies only by size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、製品が 3 つの色および 4 種類のサイズで利用可能ですが、サイズによってのみ価格が異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>If you define a trade agreement for every variant, you create 12 records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのバリアントの売買契約を定義する場合は、12 のレコードを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Instead, you can define a trade agreement just for each size and leave the Color dimension blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、サイズごとにだけ売買契約を定義して、カラー分析コードを空白のままにできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>In this case, you produce only four records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合は、4 つの記録のみを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Alternatively, if not every value of a dimension produces a different price, you can define one trade agreement for the product master and leave all product dimensions blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、分析コードのすべての値が異なる価格を生成していない場合は、製品マスターの 1 つの売買契約を定義し、すべての品目分析コードを空白のままにできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Then define a separate trade agreement just for each dimension value that produces a different price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、さまざまな価格を生成する各分析コード値に対してのみ個別の売買契約を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>For example, if the XXL size has a higher price, but all other sizes have the same price, you require only two trade agreements: one for the product master and one for the XXL size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、XXL サイズが高い価格であっても、他のすべてのサイズが同じ価格である場合は、2 つの売買契約のみを要求します: 製品マスター用に 1つおよび XXL サイズ用に 1つ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Prices that include tax vs. prices that exclude tax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税込価格対税抜き価格</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>When you set sales prices in Microsoft Dynamics 365, you don't specify whether the price value that you're setting includes or excludes tax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 で販売価格を設定する場合、設定する価格の値が税を含むか含まないかを指定しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>The value is just the price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値は、単に価格を表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>However, the <bpt id="p1">**</bpt>Price includes sales tax<ept id="p1">**</ept> setting on retail channels lets you configure retail channels so that they either include or exclude tax from prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、小売チャンネルでの <bpt id="p1">**</bpt>売上税を含む価格<ept id="p1">**</ept> 設定は、価格に税を含めるかまたは除くかのいずれかになるよう小売チャンネルをコンフィギュレーションします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>This setting is set on the channel and can change even in a single company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この設定はチャンネルで設定され、単一の会社であっても変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>If you work with both inclusive and exclusive types of tax, it's very important that you set prices correctly, because the total amount that the customer pays will change if the <bpt id="p1">**</bpt>Price includes sales tax<ept id="p1">**</ept> setting on the channel is changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税の内税および外税の両方のタイプを使用する場合は、チャンネルで <bpt id="p1">**</bpt>売上税を含む価格<ept id="p1">**</ept> 設定が変更される際に、顧客が支払う合計金額が変更するため、価格を正しく設定するのは非常に重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Differences between retail pricing and non-retail pricing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売価格および非小売価格間の差額</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>A single pricing engine is used to calculate retail prices across all channels: Call center, Retail store, and Online stores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単一の価格決定エンジンはすべてのチャネル間の小売価格を計算するのに使用されます: コール センター、小売店舗、およびオンライン ストア。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>This helps in enabling the unified commerce scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、統合通商シナリオを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Retail pricing is designed to work with retail entities instead of non-retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売価格決定は、非小売エンティティの代わりに小売エンティティで使用するよう設計されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Specifically, it's designed to set prices by store, not by warehouse.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">具体的には、倉庫ごとではなく店舗ごとに価格を設定するよう設計されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>The retail pricing engine doesn't support the following pricing features:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売価格決定エンジンは、次の価格決定機能をサポートしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Setting price by using the Site and Warehouse storage dimensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイト分析コードおよび倉庫保管分析コードを使用して価格を設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Attribute-based pricing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性ベースの価格決定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Vendor discount pass-through</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入先割引のパススルー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>In addition, <bpt id="p1">**</bpt>only<ept id="p1">**</ept> the retail pricing engine supports the following pricing features:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">加えて、小売価格決定エンジン <bpt id="p1">**</bpt>のみ<ept id="p1">**</ept> が次の価格決定機能をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>The price is based on product dimensions, in order from the most-specific variant price to the least-specific variant price to the product master price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格は、製品マスター価格に最も限定的なバリアント価格から最も限定的でないバリアント価格の順に、製品分析コードに基づきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>A price that is set by using two product dimensions (for example, Color and Size) is used before a price that is set by using only one product dimension (for example, Size).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの製品分析コード (たとえば、色やサイズ) を使用して設定される価格は、1 つだけの製品分析コード (たとえば、サイズ) を使用して設定される価格の前に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>The same price group can be used to control pricing and discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">価格および割引を管理するため、同じ価格グループを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Pricing API enhancements</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">API の機能強化の価格設定</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Price is one of the most important factors that govern the buying decisions of many customers, and many customers compare prices on various sites before they make a purchase.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">価格は、多くの顧客の購買決定を管理するための最も重要な要素の 1 つであり、多くの顧客が購買を行う前に、さまざまなサイトの価格を比較しています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>To help guarantee that they provide competitive prices, retailers keep a close eye on their competitors and often run promotions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">競争力のある価格を確実に提供するために、小売業者は競合他社についての概要を把握し、プロモーションを実行することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Therefore, to help these retailers attract customers, it's very important that product search, the browse feature, lists, and the product details page show the most accurate prices.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">したがって、これらの小売業者が顧客を惹きつけには、製品検索、参照機能、一覧、および最も正確な価格を表示する製品の詳細ページが重要です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>In an upcoming release of Retail, the <bpt id="p1">**</bpt>GetActivePrices<ept id="p1">**</ept> application programming interface (API) will return prices that include simple discounts (for example, single-line discounts that don't depend on other items in the cart).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">小売の次期リリースでは、<bpt id="p1">**</bpt>GetActivePrices<ept id="p1">**</ept> アプリケーション プログラミング インターフェイス (API) から、単純割引を含む価格が返されます (たとえば、買い物カゴの他の品目に依存しない単一行の割引)。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>In this way, the prices that are shown are close to the actual amount that customers will pay for items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これにより、表示される価格は、顧客が品目に対して支払う実際の金額に近くなります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>This API will include all the types of simple discounts: affiliation-based, loyalty-based, catalog-based, and channel-based discounts.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この API には、すべてのタイプの単純割引、たとえば所属ベース、ロイヤルティベース、カタログベース、チャネルベースの割引が含まれます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Additionally, the API will return the names and validity information for the applied discounts, so that retailers can provide a more detailed description of the price and create a sense of urgency if the discount's validity will expire soon.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">さらに、この API は適用された割引の名前と有効性の情報を返すので、小売業者は、価格の詳細な説明を提供し、割引の有効期限が近づいた場合に緊急性を高めることができます。</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>
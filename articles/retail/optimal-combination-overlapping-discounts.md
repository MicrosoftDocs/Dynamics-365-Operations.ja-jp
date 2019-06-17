<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="optimal-combination-overlapping-discounts.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>optimal-combination-overlapping-discounts.e4f3cd.e327f652855f898e50f1dd853ae20f3a0ff41d9e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e327f652855f898e50f1dd853ae20f3a0ff41d9e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\optimal-combination-overlapping-discounts.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重複割引の最適な組み合わせを決定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割引が重複している場合は、最小トランザクションの合計または最上位の割引合計の重複割引の組み合わせを決定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common 'Buy 1, get 1 X percent off' (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的な「Buy 1、get X ％off」(BOGO) 小売割引のように、購入される製品の価格に応じて割引額が異なる場合、このプロセスは組合せ最適化の問題になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重複割引の最適な組み合わせを決定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割引が重複している場合は、最小トランザクションの合計または最上位の割引合計の重複割引の組み合わせを決定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common "Buy 1, get 1 X percent off" (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的な「Buy 1、get X ％off」(BOGO) 小売割引のように、購入される製品の価格に応じて割引額が異なる場合、このプロセスは組合せ最適化の問題になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This article applies to Microsoft Dynamics AX 2012 R3 with KB 3105973 (released November 2, 2015) or later, and to Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事は、Microsoft Dynamics AX 2012 R3 の KB 3105973 (2015 年 11 月 2 日リリース) もしくはそれ以降、および  Microsoft Dynamics 365 for Retail に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To determine the combination overlapping discounts to apply in a timely manner, we have introduced a method for applying overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適時に適用できるように重複する割引の組み合わせを決定するために、重複する割引を適用する方法を導入しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>We call this new method <bpt id="p1">**</bpt>marginal value ranking<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この新しいメソッドを <bpt id="p1">**</bpt>基準金額の値のランキング<ept id="p1">**</ept> と呼んでいます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Marginal value ranking is used when the time that is required in order to evaluate the possible combinations of overlapping discounts exceeds a threshold that is configurable on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準金額の値のランキングは、重複割引の可能な組み合わせを評価するために必要な時間が <bpt id="p1">**</bpt>小売パラメーター<ept id="p1">**</ept> ページでコンフィギュレーション可能なしきい値を超える場合に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the marginal value ranking method, a value is calculated for each overlapping discount by using the discount's value on the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準金額の値のランキング メソッドでは、重複する各ディスカウントについて、共有された製品のディスカウント値を使用して値が計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The overlapped discounts are then applied from the highest relative value to the lowest relative value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重複した割引は、最も高い相対値から最も低い相対値に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For details about the new method, see the "Marginal value" section, later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい方法の詳細については、この資料の後半の「基準金額の値」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Marginal value ranking isn't used when the discount amounts for a product aren't affected by another product in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準金額の値のランキングは、ある商品の割引額がその取引の他の商品の影響を受けない場合は使用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For example, this method isn't used for two simple discounts, or for a simple discount and a single product quantity discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、この方法は、2 つの単純割引、または単純割引および 1 つの製品数量割引には使用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Discount examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割引の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can create an unlimited number of retail discounts on a common set of products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共通の製品群に対して無制限の小売割引を作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, because there is no limit, performance issues can occur when you try to calculate the discounts that should be used on the various products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、制限がないため、さまざまな製品で使用する割引を計算しようとすると、パフォーマンスの問題が発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following examples illustrate this issue in more detail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、この問題をより詳細に説明しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In example 1, we start with two products and two overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例 1 では、2 つの製品と重複した 2 つの割引から始めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Then, in example 2, we show how the issue evolves as more products are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、例 2 では、製品が追加されるにつれて問題がどのように展開するかを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Example 1: Two products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例 1: 2 つの製品と 2 つの割引</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In this example, two products are required in order to qualify for each discount, and the discounts can't be combined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、各割引の資格を得るために 2 つの製品が必要で、割引を組み合わせることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The discounts in this example are <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例の割引は、<bpt id="p1">**</bpt>最良価格<ept id="p1">**</ept> 割引です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Both products qualify for both discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">どちらの製品も両方の割引の対象となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Here are the two discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ここに 2 つの割引があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Example of two Best price discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">2 つの最良価格割引の例</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For any two products, the better of these two discounts depends on the prices of the two products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">いずれの 2 つの製品についても、これらの 2 つの割引のうち、より良いものは 2 つの製品の価格によって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When the price of both products is equal or almost equal, discount 1 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">両方の製品の価格が等しいかほぼ同じであれば、割引 1 がより良いといえます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When the price of one product is significantly less than the price of the other product, discount 2 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つの製品の価格が他の製品の価格よりも大幅に低い場合、割引 2 がより良いといえます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Here is the mathematical rule for evaluating these two discounts against each other.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">これらの 2 つの割引を相互に評価するための数学的ルールは次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Rule for evaluating the discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">割引を評価する際のルール</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When the price of product 1 is equal to two-thirds of the price of product 2, the two discounts are equal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">製品 1 の価格が製品 2 の価格の 3 分の 2 に等しい場合、2 つの割引は同等です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In this example, the effective discount percentage for discount 1 varies from a few percent (when the prices of the two products are far apart) to a maximum of 25 percent (when the two products have the same price).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、割引率 1 の有効割引率は数パーセント (2 つの製品の価格が離れている場合) から最大 25 パーセント (2 つの製品が同じ価格の場合) まで変化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The effective discount percentage for discount 2 is fixed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割引 2 の有効割引率は固定されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>It's always 20 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それは常に 20 ％ です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Because the effective discount percentage for discount 1 has a range that can be more than or less than discount 2, the best discount depends on the prices of the two products that must be discounted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割引 1 の有効割引率は、割引率 2 以上であるか、またはそれ未満である可能性があるので、割り引かれなければならない 2 つの製品の価格によって最適な割引が異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In this example, the calculation is completed quickly, because only two discounts are applied on only two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、2 つの製品に 2 つの割引のみが適用されるため、計算が迅速に完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>There are only two possible combinations: one application of discount 1 or one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可能な組み合わせは 2 つしかありません: 割引 1 のアプリケーションまたは割引 2 のアプリケーションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>There are no permutations to calculate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計算する順列はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The value of each discount is calculated by using both products, and the best discount is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各割引の価値は両方の製品を使用して計算され、最適な割引が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Example 2: Four products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例 2: 4 つの製品と 2 つの割引</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Next, we will use four products and the same two discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、4 つの製品と同じ 2 つの割引を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>All four products qualify for both discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4 つの製品は両方とも割引の対象となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>There are twelve possible combinations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">12 の可能な組み合わせがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In the end, two discounts will be applied to the transaction in one of three combinations: two applications of discount 1, two applications of discount 2, or one application of discount 1 and one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、2 つの割引が、3 つの組み合わせの 1 つでトランザクションに適用されます: 割引 1 の 2 つのアプリケーション、割引 2 の 2 つのアプリケーション、または割引 1 の 1 つのアプリケーション、および割引 2 の 1 つのアプリケーション。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To illustrate the possible combinations, we will look at two different sets of four products that have different prices:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可能な組合せを説明するために、異なる価格を持つ 4 つの製品の 2 つの異なるセットを検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>All four products have the same price, $15.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4 つの製品はすべて同じ価格、$15.00 です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this case, the best discount combination is two applications of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、最高の割引組み合わせは割引 1 の 2 つのアプリケーションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Two products will be full price, and two will be 50 percent off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの製品は定価であり、2 つで 50 % 割引になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The discounted total for the transaction is $45 (15 + 15 + 7.50 + 7.50), which is $15 (25 percent) off the undiscounted total of $60.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの合計割引額は $ 45 (15 + 15 + 7.50 + 7.50) で、割引前の合計 $ 60 から $ 15 (25％) を差し引いたものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Discount 2 is only $12 (20 percent).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割引 2 はわずか $12 (20％) です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Two products are $20 each, one product is $15, and one product is $5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの製品はそれぞれ $20 であり、1 つの製品は $15、および 1 つの製品は $5 です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In this case, the best discount combination is one application of discount 2 and one application of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、最良の割引組み合わせは、割引 2 の 1 つのアプリケーションおよび割引 1 の 1 つのアプリケーションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The following tables illustrates the discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表は、割引を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To read the tables, use one product from a row and one product from a column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表を読み取るには、行の 1 つの製品と列の 1 つの製品を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For example, in the table for discount 1, when you combine the two $20 products, you get $10 off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、割引 1 の表では、2 つの $20 の製品を組み合わせると、$10 の割引が得られます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the table for discount 2, when you combine the $15 product and the $5 product, you get $4 off.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">たとえば、割引 2 の表では、$15 の製品と $5 の製品を組み合わせると、$4 の割引が得られます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Example that uses four products for the same two discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">同じ 2 つの割引に対して 4 つの製品を使用する例</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>First, we find the largest discount that is available from any two products by using either discount.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">最初に、割引を使用して、2 つの製品から得られる最大の割引を見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The two tables show the discount amount for all combinations of the two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの表は、2 つの製品のすべての組み合わせの割引金額を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The shaded portions of the tables represent either cases where a product is paired with itself, which we can't do, or a reverse pairing of two products that produces the same discount amount and can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表の網掛け部分は、製品がそれ自体とペアになっている場合 (これは不可能)、または 2 つの製品を逆にペアにして同じ割引額が生じて無視できる場合のいずれかを表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>By looking at the tables, you can see that discount 1 for the two $20 items is the largest discount that is available for either discount on all four products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表を見ると、2 つの $20 品目の割引 1 が、すべての 4 つの製品のいずれかの割引に使用できる最大割引であることがわかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>(This discount is highlighted in green in the first table.) That leaves only the $15 product and the $5 product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(この割引は、最初の表の緑色で強調表示されています。) これにより、$15 の製品と $5 の製品のみが残っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>By looking at the two tables again, you can see that, for these two products, discount 1 gives a $2.50 discount, whereas discount 2 gives a $4 discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの表を再度見ると、これらの 2 つの製品について、割引 1 は $2.50 の割引を、割引 2 は $4 の割引を提供することがわかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Therefore, we select discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、割引 2 を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The total discount is $14.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">合計割引は $14 です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>To make this discussion easier to visualize, here are two additional tables that show the effective discount percentage for all possible two-product combinations for both discount 1 and discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この説明をより簡単に視覚化するために、割引 1 と割引 2 の両方で可能な 2 つの製品の組み合わせの有効な割引率を示す 2 つの追加テーブルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Only half the list of combinations is included, because, for these two discounts, the order in which the two products are put into the discount doesn't matter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの 2 つの割引については、2 つの製品が割引に入れられる順序は重要ではないため、組合せリストの半分のみが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The highest effective discount (25 percent) is highlighted in green, and the lowest effective discount (10 percent) is highlighted in red.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">最も高い有効割引率 (25％) は緑で強調表示され、最も低い有効割引率 (10％) は赤で強調表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Effective discount percentage for all two-product combinations for both discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">両割引に対する 2 つの製品組み合わせすべてにおける有効な割引率</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>When prices vary, and two or more discount compete, the only way to guarantee the best combination of discounts is to evaluate both discounts and compare them.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">価格が変動し、2 つ以上の割引が競合する場合、割引の最良の組み合わせを保証する唯一の方法は、両方の割引を評価し、それらを比較することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Total possible combinations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての可能な組み合わせ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section continues the example from the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、前のセクションの例を続けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>We will add more products and another discount, and see how many combinations must be calculated and compared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">より多くの商品や割引を追加し、計算して比較する必要がある組み合わせを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The following table shows the number of possible discount combinations as the product quantity increases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表は、製品数量が増加するにつれて可能な割引組み合わせの数を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The table shows what happens both when there are two overlapping discounts, as in the previous example, and when there are three overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この表は、上記の例のように 2 つの重複する割引がある場合と、3 つの重複する割引がある場合の両方を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The number of possible discount combinations that must be evaluated soon exceeds what even a fast computer can calculate and compare quickly enough to be acceptable for retail transactions.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">すぐに評価する必要がある有効な割引の組み合わせの数は、高速コンピュータであっても、小売取引で受け入れられるように迅速に計算して比較できるものを超えています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Number of possible discount combinations as the product quantity increases</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">製品数量が増加するにつれて、可能な割引組み合わせの数を示しています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>When even larger quantities or more overlapping discounts are applied, the total number of possible discount combinations quickly goes into the millions, and the time that is required in order to evaluate and select the best possible combination quickly becomes noticeable.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">より大きな数量またはより重複した割引が適用される場合、可能な割引組み合わせの総数はすぐに数百万になり、可能な限り最良の組み合わせを迅速に評価して選択するために必要な時間が顕著になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Some optimizations have been done in the retail price engine to reduce the total number of combinations that must be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売価格エンジンでは、いくつかの最適化が行われ、評価する必要がある組み合わせの総数が削減されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>However, because the number overlapping discounts and the quantities in a transaction aren't limited, a large number of combinations will always have to be evaluated whenever there are overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、割引の重複数とトランザクションの数量には制限がないため、重複した割引がある場合は常に多数の組み合わせを評価する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This issue is the issue that the marginal value ranking method addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、基準金額の値のランキングが取り組む問題といえます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Marginal value method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準金額の値のメソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>To resolve the issue of an exponentially increasing number of combinations that must be evaluated, an optimization exists that calculates the value per shared product of each discount on the set of products that two or more discounts can be applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">評価されるべき指数関数的に増加する組み合わせの問題を解決するために、2 つ以上の割引を適用できる製品セットの各割引の共有製品あたりの価値を計算する最適化が存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>We refer to this value as the <bpt id="p1">**</bpt>marginal value<ept id="p1">**</ept> of the discount for the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この値を、共有製品の割引の <bpt id="p1">**</bpt>基準金額の値<ept id="p1">**</ept> と呼びます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The marginal value is the average per product increase in the total discount amount when the shared products are included in each discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準金額の値は、共有製品が各割引に含まれる場合、合計割引額における製品増加の平均といえます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The marginal value is calculated by taking the total discount amount (DTotal), subtracting the discount amount without the shared products (DMinus<ph id="ph1">\\</ph> Shared), and dividing that difference by the number of shared products (ProductsShared).</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">基準金額の値は、合計割引額 (DTotal) をとり、共有製品なしの割引額 (共有する DMinus<ph id="ph1">\\</ph>) を差し引き、その差を共有製品数 (ProductsShared) で割ることによって計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Formula for calculating marginal value</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">基準金額の計算式</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>After the marginal value of each discount on a shared set of products is calculated, the discounts are applied to the shared products in order, exhaustively, from highest marginal value to lowest marginal value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">共有製品郡における各割引の基準金額の値が計算された後、割引は最大限の基準金額の値から最低限の基準金額の値まで、徹底して順番に共有製品に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For this method, all remaining discount possibilities aren't compared every time after a single instance of a discount is applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法では、1 回の割引インスタンスが適用されるたびに、残りのすべての割引可能性が比較されることはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Instead, the overlapping discounts are compared one time and then applied in order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その代わりに、重複割引は 1 回比較され、その後順番に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>No additional comparisons are done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の比較は行われません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>You can configure the threshold to switch to the marginal value method on the <bpt id="p1">**</bpt>Discount<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>小売パラメータ<ept id="p2">**</ept> ページの <bpt id="p1">**</bpt>割引<ept id="p1">**</ept> タブで、基準金額の値のメソッドに切り替えるようにしきい値を設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The acceptable time to calculate the total discount varies across retail industries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">合計割引を計算するための許容可能な時間は、小売業によって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>However, this time generally falls in the range of tens of milliseconds to one second.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、この時間は、一般に、数 10 ミリ秒から 1 秒の範囲内に入ります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
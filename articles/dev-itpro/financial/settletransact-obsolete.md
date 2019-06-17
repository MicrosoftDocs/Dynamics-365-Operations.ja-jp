<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="settletransact-obsolete.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>settletransact-obsolete.2ba197.1368d58d3d0dcaeefe4531ce40a49c499d5eeac9.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1368d58d3d0dcaeefe4531ce40a49c499d5eeac9</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>c576b81dc3c93c09fb08fb0ba0c19f417360c5ab</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/05/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\financial\settletransact-obsolete.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Settle transactions by using CustTrans::settleTransaction</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">CustTrans::settleTransaction を使用したトランザクションの決済</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topics describes the new CustTrans::settleTransaction method and explains why CustTrans::settleTransact is now obsolete.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックでは、新しいCustTrans::settleTransactionメソッドについて説明を行い、CustTrans::settleTransact には実装されていない新機能について説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Settle transactions by using CustTrans::settleTransaction</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">CustTrans::settleTransaction を使用したトランザクションの決済</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>CustTrans::settleTransact is obsolete</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">CustTrans::settleTransact が過去のものに</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The <bpt id="p1">**</bpt>settleTransact<ept id="p1">**</ept> method on the CustTrans table has been marked as obsolete.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">CustTransテーブルの <bpt id="p1">**</bpt>settleTransact<ept id="p1">**</ept> メソッドが刷新されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Why is it marked as obsolete?</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">なぜ刷新される必要があるのか。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When many settlements are done at the same time for the same customer, database blocking occurs.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">同じ顧客に対して複数の決済が同時に行われると、データベースのブロックが発生します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Database blocking affects performance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">データベースのブロックはパフォーマンスの低下につながります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>What does the method do?</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このメソッドによってできること</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The <bpt id="p1">**</bpt>settleTransact<ept id="p1">**</ept> method settles a set of invoices and payments for a specific customer.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>settleTransact<ept id="p1">**</ept> メソッドでは、特定の顧客に対する一連の請求書と支払の決済を行います。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Settlement identifies this set of invoices by using the <bpt id="p1">**</bpt>SpecCompany<ept id="p1">**</ept>, <bpt id="p2">**</bpt>SpecTableId<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>SpecRecId<ept id="p3">**</ept> columns of the SpecTrans table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">決済処理では、SpecTrans テーブルの <bpt id="p1">**</bpt>SpecCompany<ept id="p1">**</ept>、 <bpt id="p2">**</bpt>SpecTableId<ept id="p2">**</ept>、 <bpt id="p3">**</bpt>SpecRecId<ept id="p3">**</ept> 列を使用して一連の請求書を識別します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Together, the columns define a settlement context.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">同時に、これらの列によって決済コンテキストが定義されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The <bpt id="p1">**</bpt><ph id="ph1">\_</ph>custTable<ept id="p1">**</ept> parameter of the <bpt id="p2">**</bpt>settleTransact<ept id="p2">**</ept> method defines the settlement context as the CustTable <bpt id="p3">**</bpt>DataAreaId<ept id="p3">**</ept>, <bpt id="p4">**</bpt>TableId<ept id="p4">**</ept>, and <bpt id="p5">**</bpt>RecId<ept id="p5">**</ept> values.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p2">**</bpt>settleTransact<ept id="p2">**</ept> メソッドの <bpt id="p1">**</bpt><ph id="ph1">\_</ph>custTable<ept id="p1">**</ept> パラメータが、決済コンテキストをCustTable <bpt id="p3">**</bpt>DataAreaId<ept id="p3">**</ept>, <bpt id="p4">**</bpt>TableId<ept id="p4">**</ept>, <bpt id="p5">**</bpt>RecId<ept id="p5">**</ept> の値として定義します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The following example shows two contexts.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">次の例は、2つのコンテキストを示しています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>SpecCompany</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">SpecCompany</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>SpecTableId</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">SpecTableId</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>SpecRecId</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">SpecRecId</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Transaction</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">取引</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>USMF</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">USMF</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>7589</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">7589</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>22565451428</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">22565451428</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>1</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>USMF</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">USMF</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>7589</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">7589</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>22565451428</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">22565451428</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>2</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Replacement method</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">メソッドの更新</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The <bpt id="p1">**</bpt>settleTransaction<ept id="p1">**</ept> method on the CustTrans table is the replacement method.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">CustTrans テーブル <bpt id="p1">**</bpt>settleTransaction<ept id="p1">**</ept> メソッドが メソッドの更新を行います。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>How blocking will be avoided</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ブロックがどのように回避されるか</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Every customer settlement will get a unique settlement context.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">それぞれの顧客の決済に固有の決済コンテキストが付与されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Because each settlement that is done will have a unique context, no transaction will cause blocking.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">決済にはそれぞれ固有のコンテキストが割り当てられるため、どのトランザクションもブロックを引き起こすことがなくなります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The following example shows two contexts.</source>
        <target logoport:matchpercent="85" state="translated" state-qualifier="leveraged-inherited">次の例は、2つのコンテキストを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Each context has a unique <bpt id="p1">**</bpt>SpecRecId<ept id="p1">**</ept> value.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">各コンテキストには一意の <bpt id="p1">**</bpt>SpecRecId<ept id="p1">**</ept> 値を持っています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>SpecCompany</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">SpecCompany</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>SpecTableId</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">SpecTableId</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>SpecRecId</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">SpecRecId</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Transaction</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">取引</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>USMF</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">USMF</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>7599</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">7599</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>68719604825</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">68719604825</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>1</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>USMF</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">USMF</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>7599</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">7599</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>68719604826</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">68719604826</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>2</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Replacement method parameters</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">メソッドのパラメーターを更新する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The <bpt id="p1">**</bpt>SpecTransExecutionContext<ept id="p1">**</ept> class defines a unique settlement execution context.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>SpecTransExecutionContext<ept id="p1">**</ept> クラスは、一意となる決済の実行コンテキストを定義します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>It has two parts.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これは2つの部分で構成されています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The first part defines the customer or vendor for the settlement.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">一つ目の部分は、決済の顧客または仕入先を定義します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The second part defines the source for the settlement.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">2つ目の部分では、決済のソースを定義します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The <bpt id="p1">**</bpt>newFromSource<ept id="p1">**</ept> method takes a customer or vendor and a source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>newFromSource<ept id="p1">**</ept> メソッドには、顧客、仕入先、およびソースが必要となります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The customer or vendor is always the customer, and the source is always the customer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">顧客、仕入先、ソースは常に顧客となります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The <bpt id="p1">**</bpt>parmSpecContext<ept id="p1">**</ept> method exposes the settlement context that is generated.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>parmSpecContext<ept id="p1">**</ept> メソッドは、生成された決済コンテキストを公開します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>CustTransSettleTransactionParamters<ept id="p1">**</ept> contains the other method parameters.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>CustTransSettleTransactionParamters<ept id="p1">**</ept> には、他のメソッドパラメータが含まれています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>It has a constructor method that initializes the class with default values.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これに含まれるコンストラクターメソッドは、既定値を使用してクラスの初期化を行います。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>An example is <bpt id="p1">**</bpt>LedgerVoucher<ept id="p1">**</ept>.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">その一例として <bpt id="p1">**</bpt>LedgerVoucher<ept id="p1">**</ept> が挙げられます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>How to use the settleTransaction method</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">settleTransaction メソッドの使用方法</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Settlement is done in two parts.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">決済は2つの部分で行われます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>First, you mark the invoices and payments for settlement.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">はじめに、決済処理に向けて請求書と支払を選び出します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Then you do the settlement.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">次に、決済処理を行います。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Obsolete code example</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">古いコードの例</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>New code example</source><target logoport:matchpercent="78" state="translated" state-qualifier="fuzzy-match">新しいコードの例</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Testing</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">テスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>This functionality uses flights.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この機能はフライトを使用します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>To test it, you must turn on the flight in a non-production environment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このテストを行うには、非稼働環境にてフライトを有効にする必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>For information about how to turn on a flight in a non-production environment, see <bpt id="p1">[</bpt>Features flighted in data management and enabling flighted features<ept id="p1">](../data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features)</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">非稼動環境でフライトをオンにする方法については、 <bpt id="p1">[</bpt>データ管理でフライトされる機能とフライトされた機能の有効化<ept id="p1">](../data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features)</ept>.を参照してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The name of the flight is <bpt id="p1">**</bpt>EnableCustTransSettleTransaction<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">フライトの名称は <bpt id="p1">**</bpt>EnableCustTransSettleTransaction<ept id="p1">**</ept>です。</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>
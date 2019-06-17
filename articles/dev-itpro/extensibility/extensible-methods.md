<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extensible-methods.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extensible-methods.8087cb.3b938a260fad7b9043c0e619538d4a2f03912b0a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>3b938a260fad7b9043c0e619538d4a2f03912b0a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\extensible-methods.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Write extensible methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なメソッドの書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to write extensible methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張可能メソッドを書き込む方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Write extensible methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なメソッドの書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Before you make a method extensible, you should assess the exposed functionality of the method and the impact that the extensions might have on the scenario where the method is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドを拡張する前に、メソッドの公開されている機能と、メソッドが使用されるシナリオに拡張が与える影響を評価する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For example, depending on the business scenario, there is low risk if you enable extensions to initialize a table record but high risk if you enable extensions to skip a specific validation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ビジネス シナリオによっては、テーブル レコードを初期化する拡張機能を有効にした場合に低リスクになりますが、固有の検証をスキップする拡張機能を有効にした場合にリスクが高くなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You might also want to consider the impact if the method is extended in parallel with other extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドが他の機能拡張と並行して拡張される場合の影響を検討することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>After you've made a method extensible, future modifications to the method are restricted because of the potential user impact if the method signature or logic is changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドを拡張可能にすると、メソッドのシグネチャまたはロジックが変更された場合のユーザーへの潜在的な影響のため、メソッドのさらなる変更が制限されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Here are some guidelines to follow when you write extensible code:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能コードを作成するときに準拠するべきいくつかのガイドラインを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">**</bpt>Write short and concise methods<ept id="p1">**</ept> – A method should have only one responsibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>短くて簡潔なメソッドを記述<ept id="p1">**</ept>: メソッドの責任は 1 つだけにしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This approach enables easy extensions of the method, where the extensions can act only on the specific responsibility of the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これによりでは、メソッドの拡張が簡単になり、拡張がメソッドの特定の責任でのみ機能します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>As a simple example, keep the construction and initialization of a class object in two separate methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単純な例として、クラス オブジェクトの構築および初期化を 2 つの異なるメソッドに保持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>Expose only what is necessary<ept id="p1">**</ept> – For any new class members or methods that are added, 'Keep any new class members or methods that you add private, to allow minimal access to them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>必要なものだけを公開<ept id="p1">**</ept>: 追加される新しいクラス メンバーまたはメソッドの場合、追加する新しいクラス メンバーまたはメソッドを非公開のままにし、最小限のアクセスを許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>Use private, protected, public, and final explicitly<ept id="p1">**</ept> – For methods and class fields, this approach will guide any extenders of your code to your extension points but still let you keep full control of the parts that the extenders should not care about or depend on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プライベート、保護、パブリック、最終を明示的に使用する<ept id="p1">**</ept>: メソッドおよびクラス フィールドでは、この方法により、コードの拡張担当者を拡張ポイントに導きますが、拡張担当者が注意しなかったり依存しなかった部分を完全に管理し続けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>Method parameters<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メソッド parameters<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The method is most likely long and should be refactored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、多くの場合長くなるため、リファクタリングする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Consider whether you should refactor the whole method into a class or split the method into smaller methods that require fewer parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド全体をクラスにリファクタリングするか、必要なパラメーターが少ないより小さいメソッドにメソッドを分割するかを検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In other cases, when several parameters are required, the parameters often have a coherence that can be expressed by a class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、いくつかのパラメーターが必要なときは、パラメーターには多くの場合がクラスによって表すことができる一貫性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>By encapsulating these parameters in a class, you make it easy for extenders to add additional parameters to the base method, without breaking application programming interfaces (APIs) later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスでこれらのパラメーターをカプセル化することにより、アプリケーション プログラミング インターフェイス (API) を後で中断せずに、拡張担当者が基準メソッドにパラメーターを追加しやすくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Switch blocks<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブロックの切り替え<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Avoid switch blocks in the middle of methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドの途中でブロックを切り替えないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>A switch block should be in its <bpt id="p1">**</bpt>own method<ept id="p1">**</ept> to enable it to be extended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">切り替えブロックは、拡張可能になるにはそれ<bpt id="p1">**</bpt>自身のメソッド<ept id="p1">**</ept>になければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Long case blocks<ept id="p1">**</ept> are good candidates for being refactored into a class/class hierarchy that has a subclass for each case block.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>長いケース ブロック<ept id="p1">**</ept>は、各ケース ブロックのサブクラスを持つクラス/クラス階層にリファクタリングされるのに適した候補です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>For an example, see the <bpt id="p1">**</bpt>SalesLineCopyFromSource<ept id="p1">**</ept> class hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>SalesLineCopyFromSource<ept id="p1">**</ept> クラス階層を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Avoid <bpt id="p1">**</bpt>default blocks<ept id="p1">**</ept> in switch statements, because they make the method that has the switch block non-extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">切り替えステートメントでは<bpt id="p1">**</bpt>既定のブロック<ept id="p1">**</ept>を回避してください。切り替えブロックを拡張不能にするメソッドを作成するためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Avoid <bpt id="p1">**</bpt>throw statements in the default block<ept id="p1">**</ept> of a switch statement, because they make the switch statement non-extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">切り替えステートメントの<bpt id="p1">**</bpt>既定のブロックでスロー ステートメント<ept id="p1">**</ept>を回避してください。切り替えステートメントを拡張不能にするスイッチを作成するためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>One way to handle the throw in the default case is to refactor the switch block to a separate method that is extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のケースでのスローを処理する 1 つの方法は、拡張可能な個別のメソッドに切り替えブロックをリファクタリングすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Alternatively, you can make the whole method replaceable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、メソッド全体を交換可能にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In the following example, <bpt id="p1">**</bpt>findOrderHeader<ept id="p1">**</ept> is replaceable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>findOrderHeader<ept id="p1">**</ept> が交換可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>While<ept id="p1">**</ept> – Avoid <bpt id="p2">**</bpt>while<ept id="p2">**</ept> blocks in the middle of methods, because it becomes more difficult to extend the <bpt id="p3">**</bpt>while<ept id="p3">**</ept> blocks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>While<ept id="p1">**</ept> – メソッドの途中では <bpt id="p2">**</bpt>while<ept id="p2">**</ept> ブロックを回避してください。<bpt id="p3">**</bpt>while<ept id="p3">**</ept> ブロックを拡張しにくくなるからです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Ideally, logic in a <bpt id="p1">**</bpt>while<ept id="p1">**</ept> block should be in a separate method that enables extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">理想的には、<bpt id="p1">**</bpt>while<ept id="p1">**</ept> ブロックのロジックは、拡張機能を有効にする別のメソッドに置く必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Refactoring logic within a while loop<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>while ループ内でのリファクタリング ロジック<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Refactoring a while block (before)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">while ブロックのリファクタリング (以前)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Extensible method after refactoring<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リファクタリング後の拡張可能メソッド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Refactoring a while block (after)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">while ブロックのリファクタリング (以後)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>If..else statements<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>If..else ステートメント<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>To enable extension of the conditions in an if statement, extract the logic in the if condition into a separate method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">if ステートメントで条件を拡張できるようにするには、if 条件のロジックを別のメソッドに抽出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Avoid nested if..else blocks, because they make it difficult to change the logic in one of the blocks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入れ子になった if..else ブロックは回避してください。いずれかのロジックでの変更がむずかしくなるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>One way to resolve this issue is to refactor each condition and the logic in each block into a separate method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するための 1 つの方法は、各条件および各ブロックのロジックを個別のメソッドにリファクタリングすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In this way, you can extend the conditions or the logic in each block.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法では、条件または各ブロックのロジックを拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>When the if..else blocks handle specialization, consider moving the logic into a class hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">if..else ブロックが特殊化を処理する場合、ロジックをクラス階層に移動することを検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>For an example, see <bpt id="p1">**</bpt>SalesLineCopyFromSource<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>SalesLineCopyFromSource<ept id="p1">**</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In some scenarios, a throw in an 'else' block of a method (when the method only has an if..else) makes the method non-extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部のシナリオでは、メソッドの "else" ブロックでのスロー (メソッドに if.. else のみある場合) によってメソッドが拡張不能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>One way to handle the throw in the else is to refactor the conditions for the throw into a separate method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">else でのスローを処理する 1 つの方法は、スローの条件を個別のメソッドにリファクタリングすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>Avoid using PrmIsDefault<ept id="p1">**</ept> – When the method is overridden or wrappable, the caller of <bpt id="p2">**</bpt>super()<ept id="p2">**</ept> or <bpt id="p3">**</bpt>next()<ept id="p3">**</ept> provides all parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PrmIsDefault の使用を避ける<ept id="p1">**</ept> – メソッドがオーバーライドされるか折り返し可能な場合、<bpt id="p2">**</bpt>super()<ept id="p2">**</ept> または <bpt id="p3">**</bpt>next()<ept id="p3">**</ept> の呼び出し元がすべてのパラメーターを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Therefore, <bpt id="p1">**</bpt>prmIsDefault()<ept id="p1">**</ept> always returns false.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p1">**</bpt>prmIsDefault()<ept id="p1">**</ept> は常に false を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Avoid using enumCnt<ept id="p1">**</ept> – At compile time, this method uses a numeric literal of the number of values that an enum has.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>enumCnt の使用を避ける<ept id="p1">**</ept> – コンパイル時、このメソッドは列挙が持つ値の数の数値リテラルを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If the enum is extended or made extensible later, your code will have to be recompiled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙が拡張されるか、後で拡張可能になった場合、コードを再コンパイルする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Use <bpt id="p1">**</bpt>DictEnum.values()<ept id="p1">**</ept> instead.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに <bpt id="p1">**</bpt>DictEnum.values()<ept id="p1">**</ept> を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">**</bpt>Construct methods<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Construct メソッド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Use the <bpt id="p1">**</bpt>SysExtension<ept id="p1">**</ept> framework to enable easy extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張を簡単にするには、<bpt id="p1">**</bpt>SysExtension<ept id="p1">**</ept> フレームワークを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Avoid a throw in factory methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファクトリ メソッドでのスローを回避します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>One way to resolve this issue is to extract the conditions for the throw into a separate method that is extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するための 1 つの方法は、拡張できる別のメソッドにスローの条件を抽出することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>For more details, see the guidelines for throw statements later in this list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、このリストの後方にあるスロー ステートメントのガイドラインを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Static methods<ept id="p1">**</ept> – Static methods can't be extended with extra state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>静的メソッド<ept id="p1">**</ept>: 余分な状態によって静的メソッド拡張することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>For example, a method extender can introduce properties that can be set by using parameter methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、メソッド拡張担当者は、パラメーター メソッドを使用して設定できるプロパティを導入できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Use instance methods instead, whenever this approach is possible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法が可能な場合は必ず、代わりにインスタンス メソッドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source><bpt id="p1">**</bpt>Ability to extend part of the logic in a long method<ept id="p1">**</ept> – If it isn't possible to refactor a whole method, but the goal is to make part of the method extensible, apply the extract method refactoring.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>長いメソッドでロジックの一部を拡張する機能<ept id="p1">**</ept>: メソッド全体をリファクタリングすることができないが、目標がメソッドの一部を拡張可能にすることである場合、抽出メソッド リファクタリングを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>The new protected method must have a single responsibility, and it must also have a name that conceptually and precisely describes that responsibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい保護されたメソッドには単一の責任が必要であり、その責任を概念的かつ正確に説明する名前も必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>In this way, owners and all extenders can use the method without breaking each other.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、オーナーおよびすべての拡張担当者は互いに中断することがなくメソッドを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For example, initialization, insertion, updates to a table record, or instantiation and initialization of a class can be extracted into smaller methods, and each of these smaller methods can be enabled for for extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、初期化、挿入、テーブル レコードの更新、またはクラスのインスタンス化および初期化は、小さいメソッドに抽出でき、それらの小さい各メソッドで拡張を有効にできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The original method then calls these individual methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、元のメソッドがこれらの個々のメソッドを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Therefore, the callers to this method aren't broken.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、このメソッドの呼び出し元は中断されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Throw statements<ept id="p1">**</ept> – A throw that is added to an existing method that is extensible could break extenders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>スロー ステートメント<ept id="p1">**</ept> : 拡張可能な既存のメソッドに追加されるスローは、拡張担当者を中断させる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Consider adding the conditions for the throw in an extensible method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能メソッドでスローの条件を追加することを検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>In this way, extenders can take advantage of the method, and you can get rid of the throw.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、拡張担当者はメソッドを利用でき、スローを取り除くことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><bpt id="p1">**</bpt>If condition refactored out to a protected method<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件が保護されているメソッドにリファクタリングされる場合<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Throw (before)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スロー (前)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">**</bpt>Extensible method after refactoring<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リファクタリング後の拡張可能メソッド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Throw (after)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スロー (後)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Create, read, update and delete (CRUD) statements<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>作成、読み取り、更新、および削除 (CRUD) ステートメント<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Use Query objects in scenarios where the queries should be extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリを拡張可能にする必要のある状況でクエリ オブジェクトを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Implement a protected method that builds the query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリを構築する保護されたメソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>In addition, you might want to build several separate methods to add joined data sources, ranges, and selection fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、結合されたデータ ソース、範囲、および選択フィールドを追加するために、複数の個別のメソッドを構築できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In this way, different parts of the query can be extended individually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法では、クエリのさまざまな部分を個別に拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Use <bpt id="p1">**</bpt>SysQueryInsertRecordSet<ept id="p1">**</ept> to convert insert_recordset to a query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysQueryInsertRecordSet<ept id="p1">**</ept> を使用して、insert_recordset をクエリに変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Avoid field lists in select statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">select ステートメントではフィールド リストは避けてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>In this way, you enable extenders to retrieve their additional fields without having to extend.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法では、拡張することがなく、拡張担当者が追加のフィールドを取得できるようにすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Use the <bpt id="p1">**</bpt>in<ept id="p1">**</ept> keyword in query ranges to enable extenders to add more values to the query range.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ範囲で <bpt id="p1">**</bpt>in<ept id="p1">**</ept> キーワードを使用し、拡張担当者が値をさらにクエリ範囲に追加できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>We recommend this approach especially for query ranges that have enum values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法は特に、列挙値を持つクエリ範囲にお勧めします。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
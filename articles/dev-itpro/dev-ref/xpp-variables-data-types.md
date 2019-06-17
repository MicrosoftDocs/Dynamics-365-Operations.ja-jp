<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="xpp-variables-data-types.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>xpp-variables-data-types.68408d.b663facb1230985830abc4c69d9d885753d549fd.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>b663facb1230985830abc4c69d9d885753d549fd</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ecc7c19e08da1b592fdbd9268f3314558811ca81</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/24/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-ref\xpp-variables-data-types.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>X++ variables and data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の変数とデータ型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes variables and data types in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、X++ の変数とデータ型について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>X++ variables and data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の変数とデータ型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes variables and data types in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、X++ の変数とデータ型について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Variables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A <bpt id="p1">*</bpt>variable<ept id="p1">*</ept> is an identifier that points to a memory location where information of a specific data type is stored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>変数<ept id="p1">*</ept>は、特定のデータ型の情報が格納されているメモリ位置を示す識別子です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The size, precision, default value, implicit and explicit <bpt id="p1">[</bpt>conversion<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> functions, and range depend on the variable's data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイズ、精度、既定値、暗黙的および明示的<bpt id="p1">[</bpt>変換<ept id="p1">](xpp-conversion-run-time-functions.md)</ept>関数、範囲は、変数のデータ型によって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The <bpt id="p1">*</bpt>scope<ept id="p1">*</ept> of a variable defines the area in the code where an item can be accessed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数の<bpt id="p1">*</bpt>スコープ<ept id="p1">*</ept>は、項目にアクセスできるコード内の領域を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">*</bpt>Instance variables<ept id="p1">*</ept> are declared in class declarations, and can be accessed from any methods in the class or from methods that extend the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>インスタンス変数<ept id="p1">*</ept>はクラス宣言で宣言され、クラス内の任意のメソッドからまたは拡張クラスのメソッドからアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source><bpt id="p1">*</bpt>Local variables<ept id="p1">*</ept> can be accessed only in the block where they were defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>ローカル変数<ept id="p1">*</ept>は定義されたブロック内でのみアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When a variable is declared, memory is allocated, and the variable is initialized to the default value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数が宣言されると、メモリが割り当てられ、その変数が既定値に初期化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>You can assign values to both static fields and instance fields as part of the declaration statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的フィールドおよびインスタンス フィールドの両方に、値を declaration ステートメントの一部として割り当てることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Variables can be declared anywhere in a code block in a method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数は、メソッドのコード ブロック内の任意の場所で宣言できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>They don't have to be declared at the beginning of a method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは、メソッドの先頭で宣言される必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">*</bpt>Constants<ept id="p1">*</ept> are variables where the value can't be changed when the variable is declared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>定数<ept id="p1">*</ept>は、変数が宣言されたときに値を変更できない変数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>They use the <bpt id="p1">**</bpt>const<ept id="p1">**</ept> or <bpt id="p2">**</bpt>readonly<ept id="p2">**</ept> keyword.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>const<ept id="p1">**</ept> キーワードまたは <bpt id="p2">**</bpt>readonly<ept id="p2">**</ept> キーワードを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Constants differ from <bpt id="p1">*</bpt>read-only fields<ept id="p1">*</ept> in only one way.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定数は 1 つの方法で<bpt id="p1">*</bpt>読み取り専用のフィールド<ept id="p1">*</ept>とは異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Read-only fields can be assigned a value only one time, and that value never changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">読み取り専用フィールドには値を 1 回だけ割り当てることができ、その値は変わりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The field can be assigned its value either inline, at the place where the field is declared, or in the constructor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドには、フィールドが宣言されている場所、またはコンストラクターのいずれかでインラインで値を割り当てることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>When you declare variables of managed types that aren't authored in X++, you have two options.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ で作成されていないマネージ型の変数を宣言するときは、2 つのオプションがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You can fully qualify the type names in the declaration by including the full namespace, or you can add a <bpt id="p1">**</bpt>using<ept id="p1">**</ept> statement to your file and then omit the namespace from the type name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全な名前空間を含めることにより宣言内のタイプ名を完全に修飾、または <bpt id="p1">**</bpt>using<ept id="p1">**</ept> ステートメントをファイルに追加してから名前空間をタイプ名から省略することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Variable examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>var</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">var</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>You can declare a variable without explicitly providing the type of the variable, if the compiler can determine the type from the initialization expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラが初期化式から種類を判断することができる場合は、変数の種類を明示的に提供せずに変数を宣言することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The variable is still strongly-typed into one, unambiguous type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数は、まだ厳密に型指定されている明確な型です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>You can use <bpt id="p1">**</bpt>var<ept id="p1">**</ept> only on declarations where initialization expressions are provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>var<ept id="p1">**</ept> は初期化式が提供されている宣言でのみ使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>(The compiler will infer the type from the initialization expression.) In some cases, this approach can make code easier to read.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(コンパイラは、初期化式から種類を推定します。) 場合によっては、この方法によって、コードが読みやすくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>You should use <bpt id="p1">**</bpt>var<ept id="p1">**</ept> to declare local variables in these situations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">こうした状況でローカル変数を宣言するには、<bpt id="p1">**</bpt>var<ept id="p1">**</ept> を使用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When the type of the variable is obvious from the right side of the assignment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数の型が右側の割り当てから明らかなとき</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When the exact type isn't important</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正確な型が重要でないとき</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>For the declarations of <bpt id="p1">**</bpt>for<ept id="p1">**</ept> loop counters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ループ カウンター<bpt id="p1">**</bpt>用<ept id="p1">**</ept>の申告について</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>For disposable objects inside <bpt id="p1">**</bpt>using<ept id="p1">**</ept> statements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>using<ept id="p1">**</ept> ステートメント内での破棄可能なオブジェクト対象</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Don't use <bpt id="p1">**</bpt>var<ept id="p1">**</ept> when the type isn't clear from the initialization expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">種類が初期化式からクリアされていない際は、<bpt id="p1">**</bpt>var<ept id="p1">**</ept> を使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>var examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">var の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Declare anywhere</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意の場所で宣言</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Declarations can now be provided wherever statements can be provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステートメントを提供できる場所に宣言を提供できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>A declaration is syntactically a statement, a <bpt id="p1">*</bpt>declaration statement<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">宣言は、構文的にはステートメントで、<bpt id="p1">*</bpt>宣言ステートメント<ept id="p1">*</ept>です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>You can provide declarations immediately before the variable is used, and you don’t have to declare all the variables in one place.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数は使用される直前に宣言することができます。すべての変数を 1 つの場所で宣言する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Therefore, you have precise control over the scope of your variables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、変数のスコープを正確に制御できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>You can give variables smaller scopes, outside which the variables can’t be referenced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数を参照することができない場所で、変数に小さなスコープを付与することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The lifetime of the variable is the scope that it’s declared in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数の有効期間は宣言されているスコープです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Scopes can be started at the block level (inside compound statements), in <bpt id="p1">**</bpt>for<ept id="p1">**</ept> statements, and in <bpt id="p2">**</bpt>using<ept id="p2">**</ept> statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スコープは、<bpt id="p1">**</bpt>for<ept id="p1">**</ept> ステートメントおよび <bpt id="p2">**</bpt>using<ept id="p2">**</ept> ステートメント内においてブロック レベルで開始することができます (複合ステートメント内)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>There are several advantages to making scopes small:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スコープを小さくすることにはいくつかの利点があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Readability is enhanced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">読みやすさが向上しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>You reduce the risk that a variable will be reused in an inappropriate manner during long-term maintenance of the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの長期保守中に変数が不適切な方法で再利用されるリスクを軽減します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>It's easier to refactor code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードをリファクターすることがより簡単です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>You can copy in code without having to worry that variables might be reused in contexts where they shouldn’t be reused.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再使用すべきでないコンテキストで変数が再使用される心配をせずに、コードをコピーすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In the following example, we declare the loop counter inside the <bpt id="p1">**</bpt>for<ept id="p1">**</ept> statement that it's used in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、使用される <bpt id="p1">**</bpt>for<ept id="p1">**</ept> ステートメント内のループ カウンターを宣言します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The scope of the variable is the <bpt id="p1">**</bpt>for<ept id="p1">**</ept> statement itself, and includes the condition expression and the loop update parts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数のスコープは <bpt id="p1">**</bpt>for<ept id="p1">**</ept> ステートメントそのものであり、条件式とループ更新部分を含みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The value can’t be used outside this scope.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この範囲外で値を使用することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>In the following example, when the compiler reaches the <bpt id="p1">**</bpt>info<ept id="p1">**</ept> statement, it will issue the following error message: "'i' isn't declared."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、コンパイラが <bpt id="p1">**</bpt>info<ept id="p1">**</ept> ステートメントに達すると、「'i' が宣言されていません」というエラー メッセージを発行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>You can also scope variables to a <bpt id="p1">**</bpt>using<ept id="p1">**</ept> statement, as shown in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、以下の例に示されるように、変数を <bpt id="p1">**</bpt>using<ept id="p1">**</ept> ステートメントにスコープすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>When you use an object that implements <bpt id="p1">**</bpt>IDisposable<ept id="p1">**</ept>, you should declare and instantiate that object in a <bpt id="p2">**</bpt>using<ept id="p2">**</ept> statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IDisposable<ept id="p1">**</ept> を実装するオブジェクトを使用するときは、<bpt id="p2">**</bpt>using<ept id="p2">**</ept> ステートメントで、そのオブジェクトを宣言し、インスタンスを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The <bpt id="p1">**</bpt>using<ept id="p1">**</ept> statement calls the <bpt id="p2">**</bpt>Dispose<ept id="p2">**</ept> method on the object correctly, even if an exception occurs while you're calling methods on the object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>using<ept id="p1">**</ept> ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの <bpt id="p2">**</bpt>Dispose<ept id="p2">**</ept> メソッドを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>You can achieve the same result by putting the object inside a <bpt id="p1">**</bpt>try<ept id="p1">**</ept> block and then explicitly calling <bpt id="p2">**</bpt>Dispose<ept id="p2">**</ept> in a <bpt id="p3">**</bpt>finally<ept id="p3">**</ept> block.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクトを <bpt id="p1">**</bpt>try<ept id="p1">**</ept> ブロック内に配置してから <bpt id="p3">**</bpt>finally<ept id="p3">**</ept> ブロック内で <bpt id="p2">**</bpt>Dispose<ept id="p2">**</ept> を明示的に呼び出すことにより、同じ結果を達成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>In fact, the compiler translates the <bpt id="p1">**</bpt>using<ept id="p1">**</ept> statement in just this manner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実際、コンパイラはこの方法だけで <bpt id="p1">**</bpt>using<ept id="p1">**</ept> ステートメントを変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The following example shows some of the features that we have been describing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、説明してきた機能のいくつかを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>To prevent confusion, the compiler issues an error message if you try to introduce a variable that will hide another variable in an enclosing scope, or even in the same scope.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">混乱を避けるために、コンパイラは囲みスコープ内または同じスコープであっても、別の変数を隠す変数を導入しようとすると、エラー メッセージを発行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>For example, the following code will cause the compiler to issue the following diagnostic message: "A local variable named 'i' can't be declared in this scope because it would give a different meaning to 'i', which is already used in a parent or current scope to denote something else."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次のコードは、以下の診断メッセージを発行するコンパイラの原因になります: 「i と呼ばれるローカルの変数はこのスコープでは宣言されません。それは既に親または現在のスコープで別のものを表示している i が別の意味になってしまうためです。」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Constants, read-only variables, and macros</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定数、読み取り専用変数、およびマクロ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The concept of macros is fully supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロの概念は完全にサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>However, constants have the following advantages over macros:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、定数にはマクロに比べて次のような利点があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>You can add a documentation comment to a constant but not to the value of a macro.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメント コメントは定数に対して追加することができますが、マクロの値に対して追加することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Eventually, the language service will pick up this comment and provide useful information to the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最終的に、言語サービスはこのコメントを受け取り、ユーザーに有用な情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>A constant is known by IntelliSense.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定数は、IntelliSense で知られています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>A constant is cross-referenced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定数は、相互参照です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Therefore, you can find all references for a specific constant but not for a macro.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、マクロではなく、特定の定数のすべての参照を見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>A constant is subject to access modifiers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定数は、アクセス修飾子が適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>You can use the <bpt id="p1">**</bpt>private<ept id="p1">**</ept>, <bpt id="p2">**</bpt>protected<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>public<ept id="p3">**</ept> modifiers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>private<ept id="p1">**</ept>、<bpt id="p2">**</bpt>protected<ept id="p2">**</ept>、および <bpt id="p3">**</bpt>public<ept id="p3">**</ept> モディファイアを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The accessibility of macros isn't rigorously defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロのアクセシビリティが厳密に定義されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Constant variables have scope, whereas macros don't have scope.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定数変数にはスコープがありますが、マクロにはスコープがありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>You can see the value of a constant or a read-only variable in the debugger.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッガーには定数の値または読み取り専用変数を表示することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Macros that are defined in class scopes (that is, in class declarations) are effectively available in all methods of all derived classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス スコープ (つまりクラスの宣言) で定義されているマクロは、すべての派生クラスのすべてのメソッドで効率的に使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This feature was originally a bug in the implementation of the legacy compiler macro.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は元はレガシ コンパイラ マクロの実装におけるバグでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>However, many application programmers often take advantage of it now.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、多くのアプリケーション プログラマが多くの場合それを活用できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The X++ compiler still honors this feature, but no new code that uses it should be written.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コンパイラには、この機能が残されていますが、この機能を使用する新しいコードは記述しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This feature also has a significant effect on the performance of the compiler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、コンパイラのパフォーマンスにも大きな影響を与えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Constants can be declared at the class level, as shown in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例に示すように、定数はクラス レベルで宣言できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The constants can then be referenced by using the double colon (::) syntax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、定数を二重コロン (::) 構文を使用して参照することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>If you're in the scope of the class where the constant (<bpt id="p1">**</bpt>const<ept id="p1">**</ept>) is defined, you can omit the type name prefix (<bpt id="p2">**</bpt>MyClass<ept id="p2">**</ept> in the preceding example).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定数 (<bpt id="p1">**</bpt>const<ept id="p1">**</ept>) が定義されているクラスのスコープにいる場合は、型名の接頭語 (上記の例では <bpt id="p2">**</bpt>MyClass<ept id="p2">**</ept>) を省略できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Therefore, you can easily implement the concept of a macro library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、マクロ ライブラリの概念を簡単に実装することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>The list of macro symbols becomes a class that has public <bpt id="p1">**</bpt>const<ept id="p1">**</ept> definitions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ シンボルのリストは、パブリック <bpt id="p1">**</bpt>const<ept id="p1">**</ept> の定義を持つクラスになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>You can also define constants as variables only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、定数を変数のみとして定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The compiler will maintain the invariant so that the value can't be modified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラはインバリアントを維持して、値を変更できないようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Primitive data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリミティブ データ型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The primitive data types in X++ are <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept>, <bpt id="p2">**</bpt>boolean<ept id="p2">**</ept>, <bpt id="p3">**</bpt>date<ept id="p3">**</ept>, <bpt id="p4">**</bpt>enum<ept id="p4">**</ept>, <bpt id="p5">**</bpt>guid<ept id="p5">**</ept>, <bpt id="p6">**</bpt>int<ept id="p6">**</ept>, <bpt id="p7">**</bpt>int64<ept id="p7">**</ept>, <bpt id="p8">**</bpt>real<ept id="p8">**</ept>, <bpt id="p9">**</bpt>str<ept id="p9">**</ept>, <bpt id="p10">**</bpt>timeOfDay<ept id="p10">**</ept>, and <bpt id="p11">**</bpt>utcdatetime<ept id="p11">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ のプリミティブ データ型は、<bpt id="p1">**</bpt>anytype<ept id="p1">**</ept>、<bpt id="p2">**</bpt>boolean<ept id="p2">**</ept>、<bpt id="p3">**</bpt>date<ept id="p3">**</ept>、<bpt id="p4">**</bpt>enum<ept id="p4">**</ept>、<bpt id="p5">**</bpt>guid<ept id="p5">**</ept>、<bpt id="p6">**</bpt>int<ept id="p6">**</ept>、<bpt id="p7">**</bpt>int64<ept id="p7">**</ept>、<bpt id="p8">**</bpt>real<ept id="p8">**</ept>、<bpt id="p9">**</bpt>str<ept id="p9">**</ept>、<bpt id="p10">**</bpt>timeOfDay<ept id="p10">**</ept>、および <bpt id="p11">**</bpt>utcdatetime<ept id="p11">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>anytype</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">anytype</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> data type is a placeholder for any data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> データ型は任意のデータ型のプレースホルダーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>You should use variables of this type only as arguments and return values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタイプの変数は、引数および戻り値としてのみ使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>To use <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> as a variable, you must first assign a value to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> を変数として使用するには、最初に変数に値を割り当てる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Otherwise, a run-time error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、実行時エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>After you've assigned a value to <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept>, you can't convert it to another data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> 値に割り当てた後、別のデータ型に変換することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Although you can use <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> variables in expressions, they're usually used as arguments and return types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">式に <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> の変数を使用できますが、通常は引数および戻り値の型として使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The size, precision, scope, default value, and range of <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> depend on the conversion type that you assign to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイズ、精度、有効範囲、既定値、<bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> の範囲は、割り当てた変換タイプによって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>You can use <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> just as you use the data type that you convert it to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変換対象のデータ タイプを使用するように、<bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>For example, if you assign an integer, you can then apply relational and arithmetic operators to the variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、整数を割り当てる場合、変数にリレーショナル演算子と算術演算子を適用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>An <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> variable is automatically converted to a date, enumeration (enum), integer, real, string, extended data type (EDT) (record), class, or container when a value is assigned to the type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> 変数は値をタイプに割り当てるとき、日付、列挙 (enum)、整数、実数、文字列、拡張データ型 (EDT) (レコード)、クラス、またはコンテナーを自動的に変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Additionally, the following explicit <bpt id="p1">[</bpt>conversion functions<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> can be used: <bpt id="p2">**</bpt>any2date<ept id="p2">**</ept>, <bpt id="p3">**</bpt>any2enum<ept id="p3">**</ept>, <bpt id="p4">**</bpt>any2int<ept id="p4">**</ept>, <bpt id="p5">**</bpt>any2real<ept id="p5">**</ept>, and <bpt id="p6">**</bpt>any2str<ept id="p6">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、次の明示的な <bpt id="p1">[</bpt>変換関数<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> を使用できます: <bpt id="p2">**</bpt>any2date<ept id="p2">**</ept>、<bpt id="p3">**</bpt>any2enum<ept id="p3">**</ept>、<bpt id="p4">**</bpt>any2int<ept id="p4">**</ept>、<bpt id="p5">**</bpt>any2real<ept id="p5">**</ept>、<bpt id="p6">**</bpt>any2str<ept id="p6">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>You can't change the variable to another data type after you've converted it to <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> に変換した後は、変数を別のデータ型に変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>anytype examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">anytype 例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>boolean</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブール値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>The <bpt id="p1">**</bpt>boolean<ept id="p1">**</ept> data type contains a value that is evaluated as either <bpt id="p2">**</bpt>true<ept id="p2">**</ept> or <bpt id="p3">**</bpt>false<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブール<ept id="p1">**</ept> データ型には、<bpt id="p2">**</bpt>true<ept id="p2">**</ept> または <bpt id="p3">**</bpt>false<ept id="p3">**</ept> のいずれかとして評価される値が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>You can use the reserved literal keywords <bpt id="p1">**</bpt>true<ept id="p1">**</ept> and <bpt id="p2">**</bpt>false<ept id="p2">**</ept> wherever a <bpt id="p3">**</bpt>boolean<ept id="p3">**</ept> expression is expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>ブール<ept id="p3">**</ept> 式が予期される場所では、引当済のリテラル キーワード <bpt id="p1">**</bpt>true<ept id="p1">**</ept> および <bpt id="p2">**</bpt>false<ept id="p2">**</ept> を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The size of a <bpt id="p1">**</bpt>boolean<ept id="p1">**</ept> is 1 byte.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>boolean<ept id="p1">**</ept> のサイズは 1 byte です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>The default value is <bpt id="p1">**</bpt>false<ept id="p1">**</ept>, and the internal representation is a short number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定値は、<bpt id="p1">**</bpt>false<ept id="p1">**</ept> で、内部表示は、短い番号です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>A <bpt id="p1">**</bpt>boolean<ept id="p1">**</ept> is automatically converted to an <bpt id="p2">**</bpt>int<ept id="p2">**</ept>, <bpt id="p3">**</bpt>date<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>real<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブール<ept id="p1">**</ept>は、自動的に <bpt id="p2">**</bpt>int<ept id="p2">**</ept>、<bpt id="p3">**</bpt>date<ept id="p3">**</ept>、または <bpt id="p4">**</bpt>real<ept id="p4">**</ept> に変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>It has no explicit conversion functions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明示的な変換関数はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The internal representation of a <bpt id="p1">**</bpt>boolean<ept id="p1">**</ept> is an integer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブール<ept id="p1">**</ept> の内部テーブル現は整数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>You can assign any integer value to a variable that is declared as the <bpt id="p1">**</bpt>boolean<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブール値<ept id="p1">**</ept> タイプとして宣言された変数には任意の整数値を割り当てることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The integer value <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero) is evaluated as <bpt id="p2">**</bpt>false<ept id="p2">**</ept>, and all other integer values are evaluated as <bpt id="p3">**</bpt>true<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">整数値 <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (ゼロ) は <bpt id="p2">**</bpt>false<ept id="p2">**</ept> と評価され、他のすべての整数値は <bpt id="p3">**</bpt>true<ept id="p3">**</ept> と評価されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Because the internal representation of a <bpt id="p1">**</bpt>boolean<ept id="p1">**</ept> is an integer, <bpt id="p2">**</bpt>boolean<ept id="p2">**</ept> values are automatically converted to integers and reals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブール<ept id="p1">**</ept>の内部表示は整数なので、<bpt id="p2">**</bpt>ブール<ept id="p2">**</ept>値は自動的に整数と実数に変換されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>boolean examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブール値の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>date</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The <bpt id="p1">**</bpt>date<ept id="p1">**</ept> data type contains the day, month, and year.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>date<ept id="p1">**</ept> データ型は、年、月、日を格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Dates can be written as literals by using the following syntax: <bpt id="p1">**</bpt>Date literal = day <ph id="ph1">\\</ph> month <ph id="ph2">\\</ph> year<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付は、次の構文を使用してリテラルとして記述できます。<bpt id="p1">**</bpt>日付リテラル = 日 <ph id="ph1">\\</ph> 月 <ph id="ph2">\\</ph> 年<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>You must use four digits for the year.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その年の 4 桁の数字を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>The <bpt id="p1">**</bpt>date<ept id="p1">**</ept> data type can hold dates between January 1, 1900, and December 31, 2154.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>日付<ept id="p1">**</ept>データ型は、1900 年 1 月 1 日～ 2154 年 12 月 31 日の日付を保持できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The size of a <bpt id="p1">**</bpt>date<ept id="p1">**</ept> is 32 bits.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>date<ept id="p1">**</ept> のサイズは 32 ビットです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The default value is <bpt id="p1">**</bpt>null<ept id="p1">**</ept>, and the internal representation is a date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定値は、<bpt id="p1">**</bpt>null<ept id="p1">**</ept> で、内部表示は、日付です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>A <bpt id="p1">**</bpt>date<ept id="p1">**</ept> has no implicit conversions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>日付<ept id="p1">**</ept>に暗黙的な変換はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>However, the following explicit <bpt id="p1">[</bpt>conversion functions<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> can be used: <bpt id="p2">**</bpt>str2date<ept id="p2">**</ept>, <bpt id="p3">**</bpt>date2str<ept id="p3">**</ept>, <bpt id="p4">**</bpt>date2num<ept id="p4">**</ept>, and <bpt id="p5">**</bpt>int2date<ept id="p5">**</ept>.</source><target logoport:matchpercent="96" state="translated" state-qualifier="fuzzy-match">ただし、次の明示的な <bpt id="p1">[</bpt>変換関数<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> が使用できます: <bpt id="p2">**</bpt>str2date<ept id="p2">**</ept>、 <bpt id="p3">**</bpt>date2str<ept id="p3">**</ept>、 <bpt id="p4">**</bpt>date2num<ept id="p4">**</ept>、 <bpt id="p5">**</bpt>int2date<ept id="p5">**</ept>。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>You can add and subtract integers from dates, which moves the date some days into the future and past respectively.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">日付に対し、整数を加算または減算することができます。これにより将来の日付または、過去の日付に移動します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Subtracting dates from each other will calculate the difference in days.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">それぞれの日付を減算することにより、差異が日数で計算されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>However, adding two dates together is not possible and will lead to a compiler error.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ただし、2つの日付を一緒に加算することはできず、コンパイラ エラーの原因になります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>date examples</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">date の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>enum</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">列挙型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>An <bpt id="p1">**</bpt>enum<ept id="p1">**</ept> is a list of literals.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>列挙<ept id="p1">**</ept>はリテラルのリストです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Before you can use an <bpt id="p1">**</bpt>enum<ept id="p1">**</ept>, you must declare it in Application Explorer.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>列挙<ept id="p1">**</ept>を使用する前に、アプリケーション エクスプローラーで宣言する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The literal values are represented internally as integers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リテラルの値は、内部的に整数で表されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The first literal has the number 0, the next literal has the number 1, the next literal has the number 2, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のリテラルは数字 0、次のリテラルは 1、次のリテラルは 2 というように続きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>You can use <bpt id="p1">**</bpt>enum<ept id="p1">**</ept> values as integers in expressions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">式の中では <bpt id="p1">**</bpt>列挙型<ept id="p1">**</ept> の値を整数として使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The default value for the first entry is <bpt id="p1">**</bpt>0<ept id="p1">**</ept>, and the internal representation is a short number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のエントリの既定値は、<bpt id="p1">**</bpt>0<ept id="p1">**</ept> で、内部表示は、短い番号です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>An <bpt id="p1">**</bpt>enum<ept id="p1">**</ept> value is automatically converted to a <bpt id="p2">**</bpt>boolean<ept id="p2">**</ept>, <bpt id="p3">**</bpt>int<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>real<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>列挙<ept id="p1">**</ept>値は自動的に<bpt id="p2">**</bpt>ブール<ept id="p2">**</ept>、<bpt id="p3">**</bpt>int<ept id="p3">**</ept>、または <bpt id="p4">**</bpt>real<ept id="p4">**</ept> に変換されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Additionally, the following explicit <bpt id="p1">[</bpt>conversion functions<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> can be used: <bpt id="p2">**</bpt>enum2str<ept id="p2">**</ept> and <bpt id="p3">**</bpt>str2enum<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、次の明示的な <bpt id="p1">[</bpt>変換関数<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> を使用できます: <bpt id="p2">**</bpt>enum2str<ept id="p2">**</ept> および <bpt id="p3">**</bpt>str2enum<ept id="p3">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Hundreds of enumerable types are built into the standard application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">百種類の列挙型が標準アプリケーションに組み込まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>For example, the <bpt id="p1">**</bpt>NoYes<ept id="p1">**</ept> enum has two associated literals: <bpt id="p2">**</bpt>No<ept id="p2">**</ept> has the value <bpt id="p3">**</bpt>0<ept id="p3">**</ept>, and <bpt id="p4">**</bpt>Yes<ept id="p4">**</ept> has the value <bpt id="p5">**</bpt>1<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>NoYes<ept id="p1">**</ept> 列挙には関連付けられている 2 つのリテラルがあります: <bpt id="p2">**</bpt>No<ept id="p2">**</ept> は <bpt id="p3">**</bpt>0<ept id="p3">**</ept> の値を、および<bpt id="p4">**</bpt>Yes<ept id="p4">**</ept>は <bpt id="p5">**</bpt>1<ept id="p5">**</ept> の値です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>You can create as many enum types as you want, and you can declare up to 251 (0 to 250) literals in a single enum type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要なだけ列挙型を作成して、最大で 251 (0 ~ 250) のリテラルを単一列挙型で宣言することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>To reference an <bpt id="p1">**</bpt>enum<ept id="p1">**</ept> value, enter the name of the enum, two colons, and then the name of the literal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>列挙型<ept id="p1">**</ept>の値を参照するには、列挙型の名前、2 つのコロン、およびリテラルの名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>For example, to use the literal <bpt id="p1">**</bpt>No<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>NoYes<ept id="p2">**</ept> enum, enter <bpt id="p3">**</bpt>NoYes::No<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p2">**</bpt>NoYes<ept id="p2">**</ept> 列挙でリテラルの <bpt id="p1">**</bpt>No<ept id="p1">**</ept> を使用するには、<bpt id="p3">**</bpt>NoYes::No<ept id="p3">**</ept> を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Create an enum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型を作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>In Solution Explorer, right-click the project, point to <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New Item<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、プロジェクトを右クリックして<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をポイントしてから<bpt id="p2">**</bpt>新しい項目<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Under <bpt id="p1">**</bpt>Artifacts<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Data Types<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アーティファクト<ept id="p1">**</ept> で、<bpt id="p2">**</bpt>データ型<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Click <bpt id="p1">**</bpt>Base Enum<ept id="p1">**</ept> to select the new item type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>基本列挙<ept id="p1">**</ept>をクリックし、を新しい項目の種類を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter a name for the enum, and then click <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>フィールドに、列挙型の名前を入力してから <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>A new enum is added to the project, and the enum designer for the new element is opened.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい列挙型がプロジェクトに追加され、新しい要素の列挙型デザイナーが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>In the enum designer, right-click the enum name, and then click <bpt id="p1">**</bpt>New Element<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型デザイナーで、列挙名を右クリックしてから<bpt id="p1">**</bpt>新しい要素<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, enter the name of the enum element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、列挙要素の名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>enum examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>guid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">guid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>The <bpt id="p1">**</bpt>guid<ept id="p1">**</ept> data type holds a <bpt id="p2">*</bpt>globally unique identifier<ept id="p2">*</ept> (GUID) value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>guid<ept id="p1">**</ept> データ型は、<bpt id="p2">*</bpt>グローバルに一意の識別子<ept id="p2">*</ept> (GUID) 値を保持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>A GUID is an integer that can be used across all computers and networks, wherever a unique identifier is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GUID は、固有の識別子が必要な場合に、すべてのコンピューターとネットワークで使用できる整数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>It's unlikely that the number will be duplicated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">数字が重複することはあまりありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>A valid GUID meets all the following specifications:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な GUID は、次のすべての仕様を満たします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>It must have 32 hexadecimal digits.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">32 桁の 16 進数が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>It must have four dash characters that are embedded at the following locations: 8-4-4-4-12.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の場所では埋め込まれるダッシュ文字が 4 つ必要です: 8-4-4-4-12。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Braces (<ph id="ph1">{}</ph>) at the beginning and end of a string are optional.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列の先頭と末尾の中かっこ (<ph id="ph1">{}</ph>) はオプションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>For example, both "12345678-BBBb-cCCCC-0000-123456789012" and "{12345678-BBBb-cCCCC-0000-123456789012}" are valid GUID strings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、「12345678-BBBb-cCCCC-0000-123456789012」および「{12345678-BBBb-cCCCC-0000-123456789012}」両方共有効な GUID 文字列です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>It must have a total of either 36 or 38 characters, depending on whether braces are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">かっこを追加するかどうかに応じて、合計 36 文字または 38 文字にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>The hexadecimal digits a–f (or A–F) can be uppercase, lowercase, or mixed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">a 〜 f (または A 〜 F) の 16 進数は、大文字、小文字、または混在することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The size of a <bpt id="p1">**</bpt>guid<ept id="p1">**</ept> is 16 bytes or 128 bits.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>guid<ept id="p1">**</ept> のサイズは 16 byte または 128 ビットです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>The following explicit <bpt id="p1">[</bpt>conversion functions<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> can be used: <bpt id="p2">**</bpt>any2guid<ept id="p2">**</ept>, <bpt id="p3">**</bpt>guid2str<ept id="p3">**</ept>, <bpt id="p4">**</bpt>newGuid<ept id="p4">**</ept>, <bpt id="p5">**</bpt>str2guid<ept id="p5">**</ept>, <bpt id="p6">**</bpt>Global::guidFromString<ept id="p6">**</ept>, and <bpt id="p7">**</bpt>Global::stringFromGuid<ept id="p7">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の明示的な <bpt id="p1">[</bpt>変換関数<ept id="p1">](xpp-conversion-run-time-functions.md)</ept>、<bpt id="p2">**</bpt>any2guid<ept id="p2">**</ept>、<bpt id="p3">**</bpt>guid2str<ept id="p3">**</ept>、<bpt id="p4">**</bpt>newGuid<ept id="p4">**</ept>、<bpt id="p5">**</bpt>str2guid<ept id="p5">**</ept>、<bpt id="p6">**</bpt>Global::guidFromString<ept id="p6">**</ept>、および <bpt id="p7">**</bpt>Global::stringFromGuid<ept id="p7">**</ept> も使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>guid examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">guid の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>The following set of examples shows how to use the <bpt id="p1">**</bpt>guid<ept id="p1">**</ept> functions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、<bpt id="p1">**</bpt>guid<ept id="p1">**</ept> 関数の使い方を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>The code output of these examples follows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの例のコード出力は次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>guid code output</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">guid コード出力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>The following output appears in the Infolog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の出力は、情報ログに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Note that the string includes the optional braces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列にはオプションの中かっこが含まれることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>int and int64</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">int および int64</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source><bpt id="p1">*</bpt>Integers<ept id="p1">*</ept> are numbers that have no decimal places.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>整数<ept id="p1">*</ept>は小数点以下の桁数のない数字です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>There are two integer types: <bpt id="p1">**</bpt>int<ept id="p1">**</ept> and <bpt id="p2">**</bpt>int64<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>int<ept id="p1">**</ept> および <bpt id="p2">**</bpt>int64<ept id="p2">**</ept> の、2 つの整数タイプがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Integers are used as control variables in repetitive statements or as indexes in arrays.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">整数は、繰り返しのステートメントの制御変数または配列のインデックスとして使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>You can also use <bpt id="p1">*</bpt>integer literals<ept id="p1">*</ept> anywhere that an integer expression is expected, and both relational and arithmetic operators can be applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、整数式が必要で、リレーショナル演算子と算術演算子の両方を適用することができる任意の場所で <bpt id="p1">*</bpt>整数リテラル<ept id="p1">*</ept> を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>An integer literal is the integer as it's entered directly in the code, such as <bpt id="p1">**</bpt>32768<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">整数リテラルは <bpt id="p1">**</bpt>32768<ept id="p1">**</ept> のように、コードに直接入力された整数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>An <bpt id="p1">**</bpt>int<ept id="p1">**</ept> is 32 bits wide, and an <bpt id="p2">**</bpt>int64<ept id="p2">**</ept> is 64 bits wide.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Int<ept id="p1">**</ept> は 32 ビット幅で、<bpt id="p2">**</bpt>int64<ept id="p2">**</ept> は 64 ビット幅です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>The default value is <bpt id="p1">**</bpt>0<ept id="p1">**</ept>, and the internal representation is a long number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定値は、<bpt id="p1">**</bpt>0<ept id="p1">**</ept> で、内部表示は、長い番号です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>An integer is automatically converted to a <bpt id="p1">**</bpt>boolean<ept id="p1">**</ept>, <bpt id="p2">**</bpt>enum<ept id="p2">**</ept>, or <bpt id="p3">**</bpt>real<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">整数は自動的に <bpt id="p1">**</bpt>boolean<ept id="p1">**</ept>、<bpt id="p2">**</bpt>enum<ept id="p2">**</ept> または <bpt id="p3">**</bpt>real<ept id="p3">**</ept> に変換されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Additionally, the following explicit <bpt id="p1">[</bpt>conversion functions<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> can be used: <bpt id="p2">**</bpt>str2int<ept id="p2">**</ept>, <bpt id="p3">**</bpt>int2str<ept id="p3">**</ept>, <bpt id="p4">**</bpt>str2int64<ept id="p4">**</ept>, and <bpt id="p5">**</bpt>int642str<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、次の明示的な <bpt id="p1">[</bpt>変換関数<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> を使用できます: <bpt id="p2">**</bpt>str2int<ept id="p2">**</ept>、<bpt id="p3">**</bpt>int2str<ept id="p3">**</ept>、<bpt id="p4">**</bpt>str2int64<ept id="p4">**</ept>、<bpt id="p5">**</bpt>int642str<ept id="p5">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>The range of an <bpt id="p1">**</bpt>int<ept id="p1">**</ept> is <ph id="ph1">\[</ph>-2,147,483,647 : 2,147,483,647<ph id="ph2">\]</ph>, and the range of an <bpt id="p2">**</bpt>int64<ept id="p2">**</ept> is <ph id="ph3">\[</ph>-9,223,372,036,854,775,808 : 9,223,372,036,854,775,808<ph id="ph4">\]</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>int<ept id="p1">**</ept> の範囲は <ph id="ph1">\[</ph>-2,147,483,647 : 2,147,483,647<ph id="ph2">\]</ph>、<bpt id="p2">**</bpt>int64<ept id="p2">**</ept> の範囲は <ph id="ph3">\[</ph>-9,223,372,036,854,775,808 : 9,223,372,036,854,775,808<ph id="ph4">\]</ph> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>All integers in either of these ranges can be used as literals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全整数はこれらの範囲のいずれかでリテラルとして使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>int and int64 examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">int および int64 の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>The following example shows how to declare integers and use them in expressions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、整数を宣言して式で使用する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>If you try to assign the largest integer plus 1 to an <bpt id="p1">**</bpt>int64<ept id="p1">**</ept>, you get the wrong result, because the number is interpreted as a 32-bit number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>int64<ept id="p1">**</ept> に最大整数プラス 1 を代入しようとすると、数値は 32 ビット数として解釈されるため、間違った結果になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Therefore, the number is wrapped around and stored as -2,147,483,647 instead.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、番号は折り返され、代わりに -2,147,483,647 として格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>To prevent this behavior, add "u" to the end of the number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を防ぐためには、番号の最後に "u" を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>For example, enter <bpt id="p1">**</bpt>int64 i = 0x8000 0000u<ept id="p1">**</ept> (0x8000 0000 is 2,147,483,648).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>int64 I = 0x8000 0000u<ept id="p1">**</ept> (0x8000 0000 は 2,147,483,648 です) を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>real</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">real</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>A <bpt id="p1">**</bpt>real<ept id="p1">**</ept> variable can hold decimal values in addition to integers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実数<ept id="p1">**</ept>変数は、整数に加えて小数値を保持できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>You can use <bpt id="p1">*</bpt>decimal literals<ept id="p1">*</ept> anywhere that a <bpt id="p2">**</bpt>real<ept id="p2">**</ept> is expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>10 進リテラル<ept id="p1">*</ept> は <bpt id="p2">**</bpt>実数<ept id="p2">**</ept> が予期される場所ではどこでも使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>A decimal literal is the decimal as it's entered directly in the code, such as <bpt id="p1">**</bpt>2.123876<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10 進数リテラルは、<bpt id="p1">**</bpt>2.123876<ept id="p1">**</ept> のように、コードで直接入力された 10 進数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Real literals can also be written by using exponential notation, such as <bpt id="p1">**</bpt>1.0e3<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実数リテラルは、<bpt id="p1">**</bpt>1.0e3<ept id="p1">**</ept> などの指数の表記を使用して記述することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Reals can be used in all expressions, and they can be used with both relational and arithmetic operators.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reals は、すべての式で使用することができ、リレーショナル演算子と算術演算子の両方と共に使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>A <bpt id="p1">**</bpt>real<ept id="p1">**</ept> has a precision of 16 significant digits.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実数<ept id="p1">**</ept>は、16桁の有効な数値の精度があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>The default value for a <bpt id="p1">**</bpt>real<ept id="p1">**</ept> is <bpt id="p2">**</bpt>0.0<ept id="p2">**</ept>, and the internal representation is a binary-coded digital (BCD) number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>real<ept id="p1">**</ept> の既定値は <bpt id="p2">**</bpt>0.0<ept id="p2">**</ept> で、内部表示はバイナリコード化されたデジタル (BCD) 番号です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>The BCD encoding enables exact representations of values that are multiples of 0.1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BCD エンコードにより、0.1 の倍数の値の正確な表現が可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>The range of a <bpt id="p1">**</bpt>real<ept id="p1">**</ept> variable is -(10)¹²⁷ through (10)¹²⁷.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実数<ept id="p1">**</ept> 変数の範囲は、-(10)¹²⁷ から (10)¹²⁷ です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>All reals in this range can be used as literals in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この範囲内のすべての実数は X++ でリテラルとして使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>A <bpt id="p1">**</bpt>real<ept id="p1">**</ept> variable is automatically converted to a <bpt id="p2">**</bpt>boolean<ept id="p2">**</ept>, <bpt id="p3">**</bpt>enum<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>int<ept id="p4">**</ept>. If the result is an integer, or if the operator is an integer operator, the <bpt id="p5">**</bpt>real<ept id="p5">**</ept> is converted to an integer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実数<ept id="p1">**</ept>変数は、自動的に<bpt id="p2">**</bpt>ブール<ept id="p2">**</ept>、<bpt id="p3">**</bpt>enum<ept id="p3">**</ept>、または <bpt id="p4">**</bpt>int<ept id="p4">**</ept> に変換されます。結果が整数の場合、または演算子が整数演算子の場合には、<bpt id="p5">**</bpt>実数<ept id="p5">**</ept>は整数に変換されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>If the result is a <bpt id="p1">**</bpt>boolean<ept id="p1">**</ept>, the <bpt id="p2">**</bpt>real<ept id="p2">**</ept> is converted to a <bpt id="p3">**</bpt>boolean<ept id="p3">**</ept>, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果が<bpt id="p1">**</bpt>ブール値<ept id="p1">**</ept>である場合、<bpt id="p2">**</bpt>実数<ept id="p2">**</ept>が<bpt id="p3">**</bpt>ブール値<ept id="p3">**</ept>に変換されたりします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Additionally, the following explicit <bpt id="p1">[</bpt>conversion functions<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> can be used: <bpt id="p2">**</bpt>str2num<ept id="p2">**</ept> and <bpt id="p3">**</bpt>num2str<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、次の明示的な <bpt id="p1">[</bpt>変換関数<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> を使用できます: <bpt id="p2">**</bpt>str2num<ept id="p2">**</ept>、<bpt id="p3">**</bpt>num2str<ept id="p3">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Direct assignments between X++ <bpt id="p1">**</bpt>real<ept id="p1">**</ept> and Microsoft .NET Framework <bpt id="p2">**</bpt>System.Decimal<ept id="p2">**</ept> convert the value correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ <bpt id="p1">**</bpt>実数<ept id="p1">**</ept> と Microsoft .NET Framework <bpt id="p2">**</bpt>System.Decimal<ept id="p2">**</ept> 間の直接割り当てによって、値が正しく変換されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>A call to a conversion function isn't required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">換算関数を呼び出す必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>A <bpt id="p1">*</bpt>decimal number<ept id="p1">*</ept> is a floating-point value that consists of a sign, a numeric value where each digit is in the range 0 through 9, and a scaling factor that indicates the position of a floating decimal point that separates the integral and fractional parts of the numeric value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>10 進数<ept id="p1">*</ept>は、符号、0 から 9 の範囲内の数値、および数値の整数と小数点以下を区切る浮動小数点の位置を表すスケーリング係数で構成される浮動小数点値です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>The binary representation of a <bpt id="p1">**</bpt>real<ept id="p1">**</ept> value consists of a 1-bit sign, a 96-bit integer number, and a scaling factor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実数<ept id="p1">**</ept>値のバイナリ表現は、1 ビットの符号、96ビットの整数、スケーリング係数で構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>The scaling factor is used to divide the 96-bit integer and specify what part of it is a decimal fraction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡大縮小係数は、96 ビット整数を分割し、小数部の部分を指定するのに使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>The scaling factor is implicitly the number 10 raised to an exponent in the range 0 through 28.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡大縮小係数は、0 から 28 の範囲の指数に暗黙的に 10 を引いたものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Therefore, the binary representation of a decimal value represents (<ph id="ph1">\[</ph>-2⁹⁶ through 2⁹⁶<ph id="ph2">\]</ph> ÷ 10(0<ph id="ph3">\\</ph> through<ph id="ph4">\\</ph> 28)), where -(2⁹⁶-1) is the minimum value that can be expressed and 2⁹⁶-1 is the maximum value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、10 進数のバイナリ表現は (<ph id="ph1">\[</ph>-2⁹⁶ ～ 2⁹⁶<ph id="ph2">\]</ph> ÷ 10(0<ph id="ph3">\\</ph> ～<ph id="ph4">\\</ph> 28)) を表します。ここで -(2⁹⁶-1) は表現できる最小値と等しく、2⁹⁶-1 は最大値になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The type that is used to represent <bpt id="p2">**</bpt>real<ept id="p2">**</ept> values in Microsoft Dynamics 365 for Finance and Operations has changed from the interpreted X++ of Microsoft Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> Microsoft Dynamics 365 for Finance and Operations で<bpt id="p2">**</bpt>実数<ept id="p2">**</ept>値を表すために使用されるタイプは、変換された Microsoft Dynamics AX 2012 の X++ から変更されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>However, you don't have to rewrite any code, because the new type can express all the values that the old type could express.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、新しいタイプは、古いタイプが表すことができるすべての値を表すことができるので、コードを書き直す必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>We provide this material in the interest of full disclosure only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全な開示のためにこの材料を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>All instances of the <bpt id="p1">**</bpt>real<ept id="p1">**</ept> type are now implemented as instances of the .NET decimal type (<bpt id="p2">**</bpt>System.Decimal<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実数<ept id="p1">**</ept>タイプのすべてのインスタンスが .NET 小数タイプ (<bpt id="p2">**</bpt>System.Decimal<ept id="p2">**</ept>) のインスタンスとして実装されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Just as the <bpt id="p1">**</bpt>real<ept id="p1">**</ept> type in previous versions, the decimal type in a binary-coded decimal type is resilient to rounding errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前のバージョンでの <bpt id="p1">**</bpt>real<ept id="p1">**</ept> 型と同様に、バイナリ コード化された小数点以下の型での decimal 型は丸め誤差に対する対応力があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>The range and resolution of the decimal type differ from previous versions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前のバージョンと異なる 10 進型の範囲と解像度。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>The original X++ <bpt id="p1">**</bpt>real<ept id="p1">**</ept> type supported 16 digits and an exponent that defined the position of the decimal point.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元の X++ <bpt id="p1">**</bpt>実数<ept id="p1">**</ept> 型は 16 桁と小数点の位置を定義した指数をサポートしていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>However, the X++ <bpt id="p1">**</bpt>real<ept id="p1">**</ept> type for Microsoft Dynamics 365 for Finance and Operations and later can represent decimal numbers in the range 79,228,162,514,264,337,593,543,950,335 (2⁹⁶-1) through -79,228,162,514,264,337,593,543,950,335 (-<ph id="ph1">\[</ph>2⁹⁶-1<ph id="ph2">\]</ph>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、Microsoft Dynamics 365 for Finance and Operations 以降の X++ <bpt id="p1">**</bpt>実数<ept id="p1">**</ept>タイプは 79,228,162,514,264,337,593,543,950,335 (2⁹⁶-1) から -79,228,162,514,264,337,593,543,950,335 (-<ph id="ph1">\[</ph>2⁹⁶-1<ph id="ph2">\]</ph>) の範囲の 10 進数を表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Rounding is still required for the new <bpt id="p1">**</bpt>real<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい<bpt id="p1">**</bpt>実数<ept id="p1">**</ept>タイプにはさらに丸めが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>For example, the following code produces a result of 0.9999999999999999999999999999 instead of 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次のコードは、1 ではなく 0.9999999999999999999999999999 という結果を生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>No number of decimals will suffice to represent the value of 1/3 accurately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1/3 の値を正確に表せる小数点以下の桁数はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>The discrepancy obtained here is due to the fact that only a finite number of decimals are provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで得られる不一致は、有限数の小数しか提供されないことによるものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>You should use the <bpt id="p1">**</bpt>round<ept id="p1">**</ept> function to round to the number of decimals required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な小数点以下の桁数まで丸めるには、<bpt id="p1">**</bpt>round<ept id="p1">**</ept> 関数を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>real examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">real の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>str</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">str</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>A <bpt id="p1">**</bpt>str<ept id="p1">**</ept> variable (a <bpt id="p2">*</bpt>string<ept id="p2">*</ept>) is a sequence of characters that are used as texts, help lines, addresses, telephone numbers, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>str<ept id="p1">**</ept> 変数 (<bpt id="p2">*</bpt>文字列<ept id="p2">*</ept>) は、テキスト、ヘルプ行、住所、電話番号などとして使用される文字の並びです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>To declare a string, use the <bpt id="p1">**</bpt>str<ept id="p1">**</ept> keyword.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列を宣言するには、<bpt id="p1">**</bpt>str<ept id="p1">**</ept> キーワードを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source><bpt id="p1">*</bpt>String literals<ept id="p1">*</ept> are characters that are enclosed in quotation marks ("").</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>文字列リテラル<ept id="p1">*</ept>引用符 ("") で囲まれた文字です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>String literals can be used wherever string expressions are expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列式が必要な場合はいつでも、文字列リテラルを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Examples of string literals include "StringLit" and "Hello World".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列リテラルの例には、「StringLit」および「Hello World」が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>If you want the string to span more than one line, precede it with an at sign (@).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列を複数の行にまたがるようにするには、その前にアットマーク (@) を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>You can use strings in logical expressions, such as comparisons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">比較などの論理式では文字列を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>You can also concatenate strings by using the + operator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、+ 演算子を使用することで文字列を連結することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>The default value for a string is <bpt id="p1">**</bpt>empty<ept id="p1">**</ept>, and the internal representation is a list of characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列の既定値は <bpt id="p1">**</bpt>空<ept id="p1">**</ept>で、内部表示は文字のリストです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>There are no automatic conversions for strings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列の自動変換はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>However, the following explicit <bpt id="p1">[</bpt>conversion functions<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> can be used: <bpt id="p2">**</bpt>str2int<ept id="p2">**</ept>, <bpt id="p3">**</bpt>str2int64<ept id="p3">**</ept>, <bpt id="p4">**</bpt>int2str<ept id="p4">**</ept>, <bpt id="p5">**</bpt>str2num<ept id="p5">**</ept>, <bpt id="p6">**</bpt>num2str<ept id="p6">**</ept>, <bpt id="p7">**</bpt>str2date<ept id="p7">**</ept>, and <bpt id="p8">**</bpt>date2str<ept id="p8">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、次の明示的な <bpt id="p1">[</bpt>変換関数<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> が使用できます: <bpt id="p2">**</bpt>str2int<ept id="p2">**</ept>、<bpt id="p3">**</bpt>str2int64<ept id="p3">**</ept>、<bpt id="p4">**</bpt>int2str<ept id="p4">**</ept>、<bpt id="p5">**</bpt>str2num<ept id="p5">**</ept>、<bpt id="p6">**</bpt>num2str<ept id="p6">**</ept>、<bpt id="p7">**</bpt>str2date<ept id="p7">**</ept>、および <bpt id="p8">**</bpt>date2str<ept id="p8">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>A string can hold an unlimited number of characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列は、無制限の文字数を保持できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>However, you can specify the maximum length of a string in the variable declaration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、変数の宣言で文字列の最大の長さを指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>The string is then truncated to that maximum length.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列はその最大長に切り捨てられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>An example is shown in the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例として次のセクションに表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>str examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">str の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>timeOfDay</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">timeOfDay</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>The <bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> (time) data type is an integer value that represents the number of seconds that have passed since midnight.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> (時間) データ型は、午前 0 時から経過した秒数を表す整数値です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Like integers, <bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> variables can be used as literals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">整数と同様に、<bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> 変数はリテラルとして使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Relational and arithmetic operators can be applied to <bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> variables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーショナルおよび算術演算子は、<bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> 変数に適用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>A <bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> variable can also be used in expressions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> 変数も式で使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>The range of a <bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> data type is in the closed interval <ph id="ph1">\[</ph>0; 86,400<ph id="ph2">\]</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> データ型の範囲は <ph id="ph1">\[</ph>0;86,400<ph id="ph2">\]</ph> のクローズ区間にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Values above 86,400 (23:59:59) can't be interpreted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">86,400 (23: 59:59) を超える値は解釈できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>A <bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> variable is automatically converted to a <bpt id="p2">**</bpt>boolean<ept id="p2">**</ept>, <bpt id="p3">**</bpt>enum<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>real<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>timeOfDay<ept id="p1">**</ept> 変数は、自動的に<bpt id="p2">**</bpt>ブール<ept id="p2">**</ept>、<bpt id="p3">**</bpt>enum<ept id="p3">**</ept>、または<bpt id="p4">**</bpt>実数<ept id="p4">**</ept>に変換されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Additionally, the following explicit <bpt id="p1">[</bpt>conversion functions<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> can be used: <bpt id="p2">**</bpt>str2time<ept id="p2">**</ept> and <bpt id="p3">**</bpt>time2str<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、次の明示的な <bpt id="p1">[</bpt>変換関数<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> を使用できます: <bpt id="p2">**</bpt>str2time<ept id="p2">**</ept>、<bpt id="p3">**</bpt>time2str<ept id="p3">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>timeOfDay examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">timeOfDay の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>utcdatetime</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">utcdatetime</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>The <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> data type combines the <bpt id="p2">**</bpt>date<ept id="p2">**</ept> type and the <bpt id="p3">**</bpt>timeOfDay<ept id="p3">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> データ型は、<bpt id="p2">**</bpt>date<ept id="p2">**</ept> 型と <bpt id="p3">**</bpt>timeOfDay<ept id="p3">**</ept> 型を結合します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>A <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> variable also holds information about the time zone.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> 変数には、タイム ゾーンに関する情報も含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>However, this information can't be accessed in code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、この情報はコードではアクセスできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>The format for a <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> literal is <bpt id="p2">**</bpt>yyyy-mm-ddThh:mm:ss<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> リテラルの形式は、<bpt id="p2">**</bpt>yyyy-mm-ddThh:mm:ss<ept id="p2">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>The uppercase "T" is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">大文字「T」が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>This format can be written without quotation marks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この形式は引用符を使用せずに記述できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>The minimum value is <bpt id="p1">**</bpt>1900-01-01T00:00:00<ept id="p1">**</ept>, and the maximum value is <bpt id="p2">**</bpt>1900-01-01T00:00:00<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最小値は、<bpt id="p1">**</bpt>1900-01-01T00:00:00<ept id="p1">**</ept> で、最大値は <bpt id="p2">**</bpt>1900-01-01T00:00:00<ept id="p2">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>This maximum value matches the upper range of <bpt id="p1">**</bpt>date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>timeOfDay<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この最大値は、<bpt id="p1">**</bpt>date<ept id="p1">**</ept> と <bpt id="p2">**</bpt>timeOfDay<ept id="p2">**</ept> の上位範囲に一致します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>The smallest unit of time in <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> is one second.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> の最小単位は 1 秒です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>A <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> variable that has been declared but hasn't been initialized has the default value <bpt id="p2">**</bpt>1900-01-01T00:00:00<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">宣言されているもののまた初期化されていない <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> 変数の規定値は、 <bpt id="p2">**</bpt>1900-01-01T00:00:00<ept id="p2">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>This value is the value that is returned by <bpt id="p1">**</bpt>DateTimeUtil::minValue()<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この値は、<bpt id="p1">**</bpt>DateTimeUtil::minValue()<ept id="p1">**</ept> によって返される値です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Some functions treat an input parameter of this minimum value as <bpt id="p1">**</bpt>null<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部の機能は、この最小値の入力パラメーターを <bpt id="p1">**</bpt>null<ept id="p1">**</ept> として扱います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>For example, the <bpt id="p1">**</bpt>DateTimeUtil::toStr<ept id="p1">**</ept> method returns an empty string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>DateTimeUtil::toStr<ept id="p1">**</ept> メソッドは、空の文字列を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>However, the <bpt id="p1">**</bpt>DateTimeUtil::addSeconds<ept id="p1">**</ept> method returns a usable <bpt id="p2">**</bpt>utcdatetime<ept id="p2">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>DateTimeUtil::addSeconds<ept id="p1">**</ept> メソッドは使用可能な <bpt id="p2">**</bpt>utcdatetime<ept id="p2">**</ept> 値を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>There are no implicit conversions for the <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> データ型の暗黙的な変換はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>The <bpt id="p1">**</bpt>DateTimeUtil<ept id="p1">**</ept> class provides many methods that you can use to manipulate <bpt id="p2">**</bpt>utcdatetime<ept id="p2">**</ept> values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DateTimeUtil<ept id="p1">**</ept> クラスは、<bpt id="p2">**</bpt>utcdatetime<ept id="p2">**</ept> 値を操作するために使用できるさまざまなメソッドを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>The following explicit <bpt id="p1">[</bpt>conversion functions<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> can also be used: <bpt id="p2">**</bpt>str2datetime<ept id="p2">**</ept> and <bpt id="p3">**</bpt>datetime2str<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の明示的な <bpt id="p1">[</bpt>変換関数<ept id="p1">](xpp-conversion-run-time-functions.md)</ept>、<bpt id="p2">**</bpt>str2datetime<ept id="p2">**</ept> および <bpt id="p3">**</bpt>datetime2str<ept id="p3">**</ept> も使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Additionally, the <bpt id="p1">**</bpt>Global<ept id="p1">**</ept> class provides the <bpt id="p2">**</bpt>utcDateTime2SystemDateTime<ept id="p2">**</ept> and <bpt id="p3">**</bpt>CLRSystemDateTime2UtcDateTime<ept id="p3">**</ept> conversion methods to support common language runtime (CLR) interop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p1">**</bpt>グローバル<ept id="p1">**</ept> クラスは、<bpt id="p2">**</bpt>utcDateTime2SystemDateTime<ept id="p2">**</ept> と <bpt id="p3">**</bpt>CLRSystemDateTime2UtcDateTime<ept id="p3">**</ept> 変換メソッドを提供して、共通言語ランタイム (CLR) 相互運用をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Comparison operators are the only type of operators that can be used with the <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">比較演算子は、<bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> データ型で使用できる唯一の演算子です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>The following operators can be used to compare two <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> values: !=, <ph id="ph1">&amp;lt;</ph>, <ph id="ph2">&amp;lt;</ph>=, ==, <ph id="ph3">&amp;gt;</ph>, and <ph id="ph4">&amp;gt;</ph>=.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の演算子を使用して、2つの <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> 値を比較することができます: !=、<ph id="ph1">&amp;lt;</ph>、<ph id="ph2">&amp;lt;</ph>=、==、<ph id="ph3">&amp;gt;</ph>、および <ph id="ph4">&amp;gt;</ph>=。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>When you add a <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> field to a table, we recommend that you base the field on an EDT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルに <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> フィールドを追加するときは、そのフィールドを EDT にもとづいて決めることをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>utcdatetime examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">utcdatetime の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>Composite data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複合データ型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>The composite data types in X++ are arrays, containers, classes as data types, delegates as data types, and tables as data types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の複合データ型は、配列、コンテナー、データ型としてのクラス、データ型としてのデリゲート、データ型としてのテーブルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Array</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配列</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>An <bpt id="p1">*</bpt>array<ept id="p1">*</ept> is a variable that contains a list of items that have the same data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>配列<ept id="p1">*</ept>は同じデータ型を持つ項目のリストを含む変数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>The elements of an array are accessed by using integer indexes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配列の要素は、整数インデックスを使用してアクセスされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>You use a separate statement to initialize each element in an array.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配列内の各要素を初期化するには、別のステートメントを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>When you use a container data type or an array object to create a collection, you can initialize multiple elements by using a single statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナー データ型または配列オブジェクトを使用してコレクションを作成するとき、1 つのステートメントを使用して複数の要素を初期化できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>By default, all the items in an array have the default value of the data type in the array.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、配列内のすべての項目は配列のデータ型の既定値を持ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>There are three kinds of arrays: <bpt id="p1">*</bpt>dynamic arrays<ept id="p1">*</ept>, <bpt id="p2">*</bpt>fixed-length arrays<ept id="p2">*</ept>, and <bpt id="p3">*</bpt>partly on disk arrays<ept id="p3">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>動的配列<ept id="p1">*</ept>、<bpt id="p2">*</bpt>固定長配列<ept id="p2">*</ept>、<bpt id="p3">*</bpt>ディスク配列の一部<ept id="p3">*</ept>の 3 種類の配列があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source><bpt id="p1">**</bpt>Dynamic arrays<ept id="p1">**</ept> – These arrays are declared by using an empty array option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>動的配列<ept id="p1">**</ept> - これらの配列は、空の配列オプションを使用して宣言されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>In other word, they have only brackets (<ph id="ph1">\[</ph><ph id="ph2">\]</ph>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、かっこ (<ph id="ph1">\[</ph><ph id="ph2">\]</ph>) だけがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source><bpt id="p1">**</bpt>Fixed-length arrays<ept id="p1">**</ept> – These arrays can hold the number of items that is specified in the declaration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>固定長の配列<ept id="p1">**</ept> – これらの配列は、宣言で指定されている品目の数を保持できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Fixed-length arrays are declared like dynamic arrays, but a length option is included in the brackets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">固定長の配列は動的配列と宣言されますが、かっこ内に長さのオプションが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source><bpt id="p1">**</bpt>Partly on disk arrays<ept id="p1">**</ept> – These arrays are declared as either dynamic arrays or fixed-length arrays that have an extra option that declares how many items should be held in memory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ディスク配列の一部<ept id="p1">**</ept> – これらの配列は、動的配列または固定長の配列として宣言され、メモリに保持する品目の数を宣言するオプションが追加されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>The other items are stored on disk and are automatically loaded when they are referenced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の項目はディスクに保存され、参照されると自動的に読み込まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>X++ supports only one-dimensional arrays.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ は1次元配列のみをサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>However, you can mimic the behavior of multiple array indexes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、複数の配列インデックスの動作を再現することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>(For more information, see the "Multiple array indexes" section).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(詳細については、「複数の配列インデックス」セクションを参照してください)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Variables in objects and tables can be declared as arrays.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクトとテーブル内の変数は配列として宣言することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>For example, this functionality is used in address lines in the standard application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、この機能は、標準アプリケーションの住所明細行で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>An array collection class lets you store objects in an array.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配列コレクション クラスを配列内のオブジェクトに格納できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Array indexes begin at 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配列インデックスは 1 から開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>The first item in the array is referenced as <ph id="ph1">\[</ph>1<ph id="ph2">\]</ph>, the second item is referenced as <ph id="ph3">\[</ph>2<ph id="ph4">\]</ph>, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配列の最初の項目は <ph id="ph1">\[</ph>1<ph id="ph2">\]</ph> で参照され、2番目の項目は、 <ph id="ph3">\[</ph>2<ph id="ph4">\]</ph> などで参照されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>The following syntax is used to access an array element: <bpt id="p1">**</bpt>ArrayItemReference = ArrayVariable <ph id="ph1">\[</ph> Index <ph id="ph2">\]</ph><ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の構文は、配列要素にアクセスするために使用されます: <bpt id="p1">**</bpt>ArrayItemReference = ArrayVariable <ph id="ph1">\[</ph> Index <ph id="ph2">\]</ph><ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>In this syntax, <bpt id="p1">**</bpt>ArrayVariable<ept id="p1">**</ept> is the identifier of the array, and <bpt id="p2">**</bpt>Index<ept id="p2">**</ept> is the number of the array element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この構文では、<bpt id="p1">**</bpt>ArrayVariable<ept id="p1">**</ept> は配列の識別子であり、<bpt id="p2">**</bpt>Index<ept id="p2">**</ept> は配列要素の数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source><bpt id="p1">**</bpt>Index<ept id="p1">**</ept> can be an integer expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インデックス<ept id="p1">**</ept>には整数式を指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Item zero <ph id="ph1">\[</ph>0<ph id="ph2">\]</ph> is used to clear the array.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">項目ゼロ <ph id="ph1">\[</ph>0<ph id="ph2">\]</ph> は配列をクリアするために使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>If a value is assigned to index 0 in an array, all elements in the array are reset to their default value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値が配列のインデックス 0 に割り当てられている場合は、配列内のすべての要素が既定値にリセットされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>Array examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配列の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>Multiple array indexes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の配列インデックス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Some languages, such as C++ and C<ph id="ph1">\#</ph>, let you declare arrays that have more than one index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C++ および C<ph id="ph1">\#</ph> などの一部の言語を使用すると、1 つ以上のインデックスを持つ配列を宣言できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>In other words, you can define "arrays of arrays."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、「配列の配列」を定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>In X++, you can't directly create multiple array indexes, because only one-dimensional arrays are supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ では、1 次元配列のみサポートされているため、複数の配列インデックスを直接作成できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>However, you can implement multiple indexes by using the method that is described in this section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、このセクションに記載されているメソッドを使用して、複数のインデックスを実装することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>For example, you want to declare an array that has two dimensions, to hold an amount that is earned by country by dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、国別分析コードにより獲得される量を保持するため、2 つの分析コードを持つ配列を宣言します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>There are 10 countries and three dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10 の国と 3 つの分析コードがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>In C++ and C<ph id="ph1">\#</ph>, you declare the following array.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C++ および C<ph id="ph1">\#</ph> では、次の配列を宣言します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>However, X++ doesn't support this declaration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、X++ はこの申告をサポートしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>Instead, you can define a one-dimensional array where the number of elements is the product of the elements in each dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、要素の数が各分析コード内の要素の製品である 1 次元配列を定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Here is an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Container</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>A <bpt id="p1">*</bpt>container<ept id="p1">*</ept> object is a dynamic list of items that contain primitive data types or composite data types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>コンテナー<ept id="p1">*</ept>オブジェクトは、プリミティブ データ型または複合データ型が含まれる項目の動的リストです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>A container is useful when you must pass various types of values between the client and server tiers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーは、クライアント層とサーバー層の間でさまざまな種類の値を渡す必要がある場合に便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>However, if you plan to repeatedly add to a list in a loop, a container isn't a good choice.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ループ内でのリストに繰り返し追加する予定がある場合、コンテナーは適切な選択肢ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>Containers are most suitable for processes that don't involve excessive modification to the size or contents of the container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーは、コンテナーのサイズまたは内容を過度に変更することがないプロセスに最も適しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>When a container undergoes excessive additions of data, overall system performance can decrease, because container data must be repeatedly copied, and new space must be repeatedly allocated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーに過剰にデータが追加されると、コンテナーのデータを繰り返しコピーする必要があり、また新しい領域を繰り返し割り当てる必要があるため、システム全体のパフォーマンスが低下する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>A container isn't a class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーはクラスではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>A container contains an ordered sequence of primitive values or other containers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーには、プリミティブ値またはその他のコンテナーの注文済のシーケンスが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Because of the flexibility of <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept>, a container offers a good way to store values of different types together.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> の柔軟性のために、コンテナーは異なるタイプの値を一緒に保存する良い方法を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>A container can be stored in the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーは、データベースに保管できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>A container is one of the column types that you can select when you use Application Explorer to add a column to a table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーとは、アプリケーション エクスプローラーを使用して、テーブルに列を追加する場合に選択可能な列タイプの 1 つです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>A container slightly resembles an array, or collections such as the <bpt id="p1">**</bpt>List<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Stack<ept id="p2">**</ept> classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配列に少し似た、または <bpt id="p1">**</bpt>List<ept id="p1">**</ept> や <bpt id="p2">**</bpt>Stack<ept id="p2">**</ept> クラスのようなコレクションのコンテナーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>However, you can never change the size or content of a container after the container is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、コンテナーを作成した後にコンテナーのサイズまたはコンテンツを変更できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>X++ statements that appear to modify a container are internally building a new container and copying values as required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナを変更するために表示される X++ ステートメントは、内部で新しいコンテナを構築して必要に応じ値をコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>Even an assignment of a container to another container variable creates a new copy of the container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーを別のコンテナー変数に割り当てても、コンテナーの新しいコピーは作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>All these operations can affect performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらすべての工程はパフォーマンスに影響を与えることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>In the functions that provide access to a container (such as <bpt id="p1">**</bpt>conPeek<ept id="p1">**</ept>), the container is 1-based, not 0-based.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーへのアクセスを提供する関数 (<bpt id="p1">**</bpt>conPeek<ept id="p1">**</ept> など) では、コンテナーは 0 ベースではなく、1 ベースです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>Indexing is 1-based for arrays.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックスは配列に対して 1 ベースです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>The default value of a container is <bpt id="p1">**</bpt>empty<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーの既定値は <bpt id="p1">**</bpt>空<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>The container doesn't contain any values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーには値が含まれていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>Some statements that use containers might appear to modify a container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーを使用するいくつかのステートメントは、コンテナーを変更するように見えることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>However, inside the system, containers are never modified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、システム内部では、コンテナーは決して変更されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>Instead, the data from the original container is combined with data from the command to build a new container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、元のコンテナーからのデータは、新しいコンテナーを構築するためにコマンドからのデータと結合されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>You can create a new container by using one of the following functions: <bpt id="p1">**</bpt>conDel<ept id="p1">**</ept>, <bpt id="p2">**</bpt>conIns<ept id="p2">**</ept>, or <bpt id="p3">**</bpt>conPoke<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>conDel<ept id="p1">**</ept>、<bpt id="p2">**</bpt>conIns<ept id="p2">**</ept>、または <bpt id="p3">**</bpt>conPoke<ept id="p3">**</ept> のいずれかの関数を使用して、新しいコンテナを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>Additionally, the <bpt id="p1">**</bpt>Global<ept id="p1">**</ept> class has static methods for handling containers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p1">**</bpt>グローバル<ept id="p1">**</ept> クラスには、コンテナーを処理するための静的メソッドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>These methods include <bpt id="p1">**</bpt>con2ArraySource<ept id="p1">**</ept>, <bpt id="p2">**</bpt>con2Buf<ept id="p2">**</ept>, <bpt id="p3">**</bpt>con2List<ept id="p3">**</ept>, <bpt id="p4">**</bpt>con2Str<ept id="p4">**</ept>, <bpt id="p5">**</bpt>containerFromXmlNode<ept id="p5">**</ept>, <bpt id="p6">**</bpt>conView<ept id="p6">**</ept>, and <bpt id="p7">**</bpt>str2Con<ept id="p7">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドには、<bpt id="p1">**</bpt>con2ArraySource<ept id="p1">**</ept>、<bpt id="p2">**</bpt>con2Buf<ept id="p2">**</ept>、<bpt id="p3">**</bpt>con2List<ept id="p3">**</ept>、<bpt id="p4">**</bpt>con2Str<ept id="p4">**</ept>、<bpt id="p5">**</bpt>containerFromXmlNode<ept id="p5">**</ept>、<bpt id="p6">**</bpt>conView<ept id="p6">**</ept>、<bpt id="p7">**</bpt>str2Con<ept id="p7">**</ept> が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>There are several intrinsic functions for handling a container, such as <bpt id="p1">**</bpt>conIns<ept id="p1">**</ept> and <bpt id="p2">**</bpt>conPeek<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>conIns<ept id="p1">**</ept> や <bpt id="p2">**</bpt>conPeek<ept id="p2">**</ept> のような、コンテナーを扱うためのいくつかの固有の関数があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>The X++ <bpt id="p1">**</bpt>conPeek<ept id="p1">**</ept> function returns an <bpt id="p2">**</bpt>anytype<ept id="p2">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ <bpt id="p1">**</bpt>conPeek<ept id="p1">**</ept> 関数は <bpt id="p2">**</bpt>anytype<ept id="p2">**</ept> タイプを返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>Therefore, it's easier to read the values from a container when you don't know the type of each value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、各値の型がわからない場合は、コンテナーから値を読み取る方が簡単です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>An <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> can be assigned to any X++ value type, provided that the value can be converted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> は値を変換することができればすべての X++ 値タイプに割り当てることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>Your code is easier to read when it avoids explicit data type conversions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明示的なデータ型の変換を回避すると、コードは読みやすくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>Therefore, assign values from a container to the same data type that was used to put the value into the container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、値をコンテナーに配置するために使用されたのと同じデータ型にコンテナーから値を割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>You must not assign a container to an <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept>, because the system might not be able to determine the correct conversions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーを <bpt id="p1">**</bpt>エニタイプ<ept id="p1">**</ept> に割り当てることはできません。適切な変換を決定できない可能性があるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>In these cases, unexpected behavior or errors might occur.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのような場合、予期しない動作やエラーが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>Comparing container to other options</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーと他のオプションの比較</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>The <bpt id="p1">**</bpt>container<ept id="p1">**</ept> type resembles other constructs, such as arrays and collection classes such as <bpt id="p2">**</bpt>List<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Stack<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コンテナー<ept id="p1">**</ept>型は、<bpt id="p2">**</bpt>List<ept id="p2">**</ept> や <bpt id="p3">**</bpt>Stack<ept id="p3">**</ept> などの配列およびコレクション クラスなど、他の構成要素と似ています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>The difference between a container and <bpt id="p1">**</bpt>List<ept id="p1">**</ept> is that an instance of the <bpt id="p2">**</bpt>List<ept id="p2">**</ept> class is mutable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーと <bpt id="p1">**</bpt>リスト<ept id="p1">**</ept> の違いは、<bpt id="p2">**</bpt>リスト<ept id="p2">**</ept> クラスのインスタンスが不変であるという点です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>A <bpt id="p1">**</bpt>List<ept id="p1">**</ept> object first allocates more space than its data consumes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リスト<ept id="p1">**</ept>オブジェクトは、最初にそのデータが消費するよりも多くの領域を割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>Then, as data is added, the space is filled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、データが追加されると、スペースが埋められます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>This behavior is more efficient than allocating more space every time that an element is added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この動作は、要素が追加されるたびに多くの領域を割り当てる場合よりも効率的です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>An update of a <bpt id="p1">**</bpt>List<ept id="p1">**</ept> performs faster than similar operations on a container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リスト<ept id="p1">**</ept>の更新はコンテナーの同様の操作よりも高速に実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>When you construct a <bpt id="p1">**</bpt>List<ept id="p1">**</ept> object, you determine the one type of data that the <bpt id="p2">**</bpt>List<ept id="p2">**</ept> object can store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リスト<ept id="p1">**</ept> オブジェクトを作成するときは、<bpt id="p2">**</bpt>リスト<ept id="p2">**</ept> オブジェクトが格納できるデータの 1 つのタイプを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>This restriction is less flexible for a <bpt id="p1">**</bpt>List<ept id="p1">**</ept> than it is for a container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この制限は、コンテナの場合よりも<bpt id="p1">**</bpt>リスト<ept id="p1">**</ept>の柔軟性が低くなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>However, you can store objects in a <bpt id="p1">**</bpt>List<ept id="p1">**</ept>, whereas a container can store only value types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>リスト<ept id="p1">**</ept>のオブジェクトを格納できますが、コンテナーでは値の型しか格納できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>The difference between a container and an array is that an array can hold only items of its declared type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーと配列の違いは、配列は宣言された型の項目だけを保持できるという点です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>You can allocate memory space for an array and fill that space with values later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配列にメモリ容量を割り当て、後からその容量に値を入力することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>For example, you can fill in values in a loop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ループに値を入力することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>This behavior is efficient and performs well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この動作は効率的であり、適正に動作します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>When you want to build a new container by appending new data, you can use either the <bpt id="p1">**</bpt><ph id="ph1">+=</ph><ept id="p1">**</ept> operator or the <bpt id="p2">**</bpt>conIns<ept id="p2">**</ept> function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータを追加して新しいコンテナーを作成するときは、<bpt id="p1">**</bpt><ph id="ph1">+=</ph><ept id="p1">**</ept> 演算子かまたは <bpt id="p2">**</bpt>conIns<ept id="p2">**</ept> 機能のいずれかを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>The <bpt id="p1">**</bpt><ph id="ph1">+=</ph><ept id="p1">**</ept> operator is the faster alternative.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">+=</ph><ept id="p1">**</ept> 演算子は高速の代替です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>Use the <bpt id="p1">**</bpt>conIns<ept id="p1">**</ept> function only when you want to add new data before the last index of the original data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>conIns<ept id="p1">**</ept> 関数は、元のデータの最後のインデックスの前に新しいデータを追加する場合にのみ使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>In Dynamics AX 2012, although you could use the X++ compiler to store object references in containers, the result would fail at run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 では、コンテナーのオブジェクト参照を格納するために X++ コンパイラを使用できましたが、結果は実行時に失敗していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>However, in Microsoft Dynamics 365 for Finance and Operations, when the compiler sees an attempt to store an object reference in a container, it issues an error message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、Microsoft Dynamics 365 for Finance and Operations で、コンパイラがコンテナー内のオブジェクト参照を格納しようとする試みを確認すると、エラー メッセージを出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>If the type of the element that is added to the container is <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept>, the compiler can’t determine whether the value is a reference type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーに追加される要素のタイプが <bpt id="p1">**</bpt>anytype<ept id="p1">**</ept> である場合、コンパイラーは値は参照タイプであるかどうかを決定することをできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>In this case, the compiler allows the attempt.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、コンパイラはその試行を認めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>It's assumed that the user knows what he or she is doing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは何をしているかを把握しているとみなされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>Although the compiler doesn't diagnose the code as erroneous, an error will be thrown at run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラはコードを誤っていると診断しませんが、エラーは実行時間にスローされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>Container examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>Classes as data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ型としてのクラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>A <bpt id="p1">*</bpt>class<ept id="p1">*</ept> is a type definition that describes both variables and methods for instances of the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>クラス<ept id="p1">*</ept>は、クラスのインスタンスの変数とメソッドの両方を説明するタイプ定義です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>(The instances of a class are also known as <bpt id="p1">*</bpt>objects<ept id="p1">*</ept>.) A class is only a definition for objects, and all objects are <bpt id="p2">**</bpt>null<ept id="p2">**</ept> when they are declared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(クラスのインスタンスは<bpt id="p1">*</bpt>オブジェクト<ept id="p1">*</ept>ともよばれます。) クラスはオブジェクトの定義に過ぎず、すべてのオブジェクトは宣言されると <bpt id="p2">**</bpt>null<ept id="p2">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>In Application Explorer, every application class under the <bpt id="p1">**</bpt>Classes<ept id="p1">**</ept> node is a data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーでは、<bpt id="p1">**</bpt>クラス<ept id="p1">**</ept> ノードの各アプリケーション クラスはデータ型です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>You can declare variables of these types in your code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの種類の変数をコード内で宣言することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>You can construct instances of a class and assign the instances to variables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスのインスタンスを構築してインスタンスを変数に割り当てることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>Classes can be nested in source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスはソース コードに入れ子にできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>Nested classes are available only inside forms (such as a class that extends <bpt id="p1">**</bpt>FormRun<ept id="p1">**</ept>), and are used to represent controls, data sources, or data fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入れ子になったクラスはフォーム内 (<bpt id="p1">**</bpt>FormRun<ept id="p1">**</ept> を拡張するクラスなど) でのみ使用でき、コントロール、データ ソースまたはデータ フィールドを表すために使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>An attribute decoration, such as the attribute decoration on a class or a method, can omit the suffix of the attribute name if the suffix is <bpt id="p1">**</bpt>Attribute<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性の修飾で接尾語に<bpt id="p1">**</bpt>属性<ept id="p1">**</ept>がある場合、属性の修飾などのクラスまたはメソッドで、属性名の接尾語を省略できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>Therefore, X++ allows <bpt id="p1">**</bpt><ph id="ph1">\[</ph>MyFavorite<ph id="ph2">\]</ph><ept id="p1">**</ept> instead of requiring <bpt id="p2">**</bpt><ph id="ph3">\[</ph>MyFavoriteAttribute<ph id="ph4">\]</ph><ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、X++ は <bpt id="p2">**</bpt><ph id="ph3">\[</ph>MyFavoriteAttribute<ph id="ph4">\]</ph><ept id="p2">**</ept> を必要とするのではなく、<bpt id="p1">**</bpt><ph id="ph1">\[</ph>MyFavorite<ph id="ph2">\]</ph><ept id="p1">**</ept> を許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>Additionally, attributes are now applied to the handlers of delegates and methods, to map the handlers to those targets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、属性はデリゲートとメソッドのハンドラーに現在適用され、ハンドラーをこれらのターゲットにマップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>In AX 2012 and earlier versions, you could designate a method to run on either the client or the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 およびそれ以前のバージョンでは、クライアントまたはサーバーのいずれかで実行するメソッドを指定することができました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>However, in Microsoft Dynamics 365 for Finance and Operations and later versions, all compiled X++ code is run as .NET Common Intermediate Language (CIL) on the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、Microsoft Dynamics 365 for Finance and Operations およびそれ以降のバージョンでは、コンパイルされたすべての X++ コードがサーバーの .NET 共通中間言語 (CIL) として実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>There is no longer any code that is evaluated at the client site or in the browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント サイトまたはブラウザーで評価されるコードはなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>Therefore, the <bpt id="p1">**</bpt>client<ept id="p1">**</ept> and <bpt id="p2">**</bpt>server<ept id="p2">**</ept> keywords are now ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p1">**</bpt>client<ept id="p1">**</ept> キーワードと <bpt id="p2">**</bpt>server<ept id="p2">**</ept> キーワードは無視されるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source>Although these keywords don't cause a compile error if they are used, they should not be used in any new code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのキーワードが使用される場合コンパイル エラーは発生しませんが、新しいコードを使用することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>Private and protected member variables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライベートおよび保護されたメンバー変数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>Previously, all member variables that were defined in a class were protected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前は、クラスで定義されていたすべてのメンバー変数が保護されていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>You can now make the visibility of member variables explicit by adding the <bpt id="p1">**</bpt>private<ept id="p1">**</ept>, <bpt id="p2">**</bpt>protected<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>public<ept id="p3">**</ept> keywords.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>private<ept id="p1">**</ept>、<bpt id="p2">**</bpt>protected<ept id="p2">**</ept>、および <bpt id="p3">**</bpt>public<ept id="p3">**</ept> キーワードを加えることにより、メンバー変数の表示を明示的にすることができるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source>The interpretation of these modifiers is obvious and is aligned with the semantics for methods:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの修飾子の解釈は明白であり、メソッドのセマンティクスに沿っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source><bpt id="p1">**</bpt>private<ept id="p1">**</ept> – The member variable can be used only within the class where it’s defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プライベート<ept id="p1">**</ept> – メンバー変数は、定義されているクラス内でのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source><bpt id="p1">**</bpt>protected<ept id="p1">**</ept> – The member variable can be used in the class where it’s defined and all subclasses of that class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保護されている<ept id="p1">**</ept> – メンバー変数は、それが定義されているクラスおよびクラスのすべてのサブクラスで使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source><bpt id="p1">**</bpt>public<ept id="p1">**</ept> – The member variable can be used anywhere.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パブリック<ept id="p1">**</ept> – メンバー変数を任意の場所に使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source>It’s visible outside the confines of the class hierarchy where it’s defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、定義されているクラス階層の範囲外に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source>By default, member variables that aren’t adorned with an explicit modifier are still protected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、明示的なモディファイアーで実装されていないメンバー変数は引き続き保護されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source>However, as a best practice, you should explicitly specify the visibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ベスト プラクティスとしては、可視性を明示的に指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source>As we described earlier, when a member variable is defined as <bpt id="p1">**</bpt>public<ept id="p1">**</ept>, it can be accessed outside the class where it’s defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先に説明したように、メンバー変数が<bpt id="p1">**</bpt>パブリック<ept id="p1">**</ept>として定義されている場合、メンバー変数は定義されているクラス外でアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source>In this case, you must specify a qualifier that designates the object that is hosting the variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、変数をホストしているオブジェクトを指定する修飾子を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source>To specify the qualifier, use the dot notation, as you do for method calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修飾子を指定するには、メソッド呼び出しの場合と同様にドット表記法を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source>In the following example, <bpt id="p1">**</bpt>field1<ept id="p1">**</ept> is accessed by using the explicit <bpt id="p2">**</bpt>this<ept id="p2">**</ept> qualifier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>field1<ept id="p1">**</ept> に明示的な <bpt id="p2">**</bpt>this<ept id="p2">**</ept> 修飾子を使用することでアクセスします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source>In this case, it might not be a good idea to make a member variable public, because that approach exposes the internal workings of the class to its consumers, and therefore creates a strong dependency between the class implementation and its consumers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、そのアプローチは消費者にクラスの内部作業を公開することになり、クラスの実装と消費者の間に強い依存関係が生じるため、メンバー変数をパブリックにすることをお勧めできない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source>You should always try to depend only on a contract, not an implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">常に、実装ではなくコントラクトにのみ依存させる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source>Static constructors and static fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的コンストラクターおよび静的フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source><bpt id="p1">*</bpt>Static fields<ept id="p1">*</ept> are fields that are declared by using the <bpt id="p2">**</bpt>static<ept id="p2">**</ept> keyword.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>静的フィールド<ept id="p1">*</ept>は<bpt id="p2">**</bpt>静的<ept id="p2">**</ept>キーワードを使用して宣言されているフィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source>Conceptually, static fields apply to the class, not to instances of the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概念的には、クラスのインスタンスではなく静的フィールドに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="504">
          <source>Static constructors are guaranteed to run before any static calls or instance calls are made to the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的コンストラクターは、静的呼び出しまたはインスタンス呼び出しがクラスに対して行われる前に実行されることが保証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="505">
          <source>The execution of the static constructor is relative to the user’s session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的コンストラクターの実行は、ユーザーのセッションに対して相対的です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="506">
          <source>You never call the static constructor explicitly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的コンストラクターは明示的に呼び出さないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="507">
          <source>Instead, the compiler will generate code to make sure that the constructor is called exactly one time, before any other method on the class is called.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、コンパイラはコンストラクターがクラスの他のメソッドの前に正確に 1 回呼び出されるようにするコードを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="508">
          <source>A static constructor is used to initialize any static data or perform an action that must be performed only one time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的コンストラクターは、任意の静的データを初期化したり、一度だけ実行する必要のあるアクションを実行するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="509">
          <source>You can't provide parameters for the static constructor, and it must be marked with the <bpt id="p1">**</bpt>static<ept id="p1">**</ept> keyword.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的コンストラクターのパラメーターを指定することはできず、<bpt id="p1">**</bpt>静的<ept id="p1">**</ept> キーワードでマークされる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="510">
          <source>Class elements in Application Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーのクラス要素</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="511">
          <source>Under most class nodes in Application Explorer, there are two special nodes: a <bpt id="p1">**</bpt>classDeclaration<ept id="p1">**</ept> node and a <bpt id="p2">**</bpt>new<ept id="p2">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプ ローラーのほとんどのクラス・ノードの下には、<bpt id="p1">**</bpt>classDeclaration<ept id="p1">**</ept> ノードと <bpt id="p2">**</bpt>new<ept id="p2">**</ept> ノードという 2 つの特殊ノードがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="512">
          <source>A <bpt id="p1">**</bpt>classDeclaration<ept id="p1">**</ept> always contains the X++ <bpt id="p2">**</bpt>class<ept id="p2">**</ept> keyword.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>classDeclaration<ept id="p1">**</ept> は、常に X++ <bpt id="p2">**</bpt>クラス<ept id="p2">**</ept>キーワードになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="513">
          <source>Additional keywords, such as <bpt id="p1">**</bpt>extends<ept id="p1">**</ept>, can be included to modify the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加のキーワードは、<bpt id="p1">**</bpt>拡張<ept id="p1">**</ept>のように、クラスを変更するために含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="514">
          <source>This node can also contain declarations of member variables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このノードには、メンバー変数の宣言も含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="515">
          <source>The member variables can't be initialized to a value in <bpt id="p1">**</bpt>classDeclaration<ept id="p1">**</ept>, and they can't be static.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メンバー変数は、<bpt id="p1">**</bpt>classDeclaration<ept id="p1">**</ept> の値に初期化することはできません。また静的にすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="516">
          <source>In the following example, the variables <bpt id="p1">**</bpt>m<ph id="ph1">\_</ph>priority<ept id="p1">**</ept> and <bpt id="p2">**</bpt>m<ph id="ph2">\_</ph>rectangle<ept id="p2">**</ept> are members of the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、変数 <bpt id="p1">**</bpt>m<ph id="ph1">\_</ph>priority<ept id="p1">**</ept> および <bpt id="p2">**</bpt>m<ph id="ph2">\_</ph>rectangle<ept id="p2">**</ept> はクラスのメンバーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="517">
          <source>A <bpt id="p1">**</bpt>new<ept id="p1">**</ept> operator contains logic that is run when the <bpt id="p2">**</bpt>new<ept id="p2">**</ept> operator is used to create an instance of the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しい<ept id="p1">**</ept>演算子には、<bpt id="p2">**</bpt>新しい<ept id="p2">**</ept>演算子を使用して、クラスのインスタンスを作成するときに実行されるロジックが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="518">
          <source>The logic in the <bpt id="p1">**</bpt>new<ept id="p1">**</ept> method might construct an object and assign that object to a variable that is declared in the <bpt id="p2">**</bpt>classDeclaration<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept> メソッドのロジックは、オブジェクトを作成し、そのオブジェクトを <bpt id="p2">**</bpt>classDeclaration<ept id="p2">**</ept> で宣言された変数に割り当てることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="519">
          <source>Each class can have only one <bpt id="p1">**</bpt>new<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各クラスは、<bpt id="p1">**</bpt>新しい<ept id="p1">**</ept>方法を 1 つだけ持つことが可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="520">
          <source>However, in the <bpt id="p1">**</bpt>new<ept id="p1">**</ept> method, you often should call the <bpt id="p2">**</bpt>new<ept id="p2">**</ept> method of the base class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>新しい<ept id="p1">**</ept>メソッドでは、多くの場合基本クラスの<bpt id="p2">**</bpt>新しい<ept id="p2">**</ept>メソッドを呼び出す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="521">
          <source>To call the <bpt id="p1">**</bpt>new<ept id="p1">**</ept> method of the base class, call <bpt id="p2">**</bpt>super()<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本クラスの&lt;<bpt id="p1">**</bpt>新規<ept id="p1">**</ept>メソッドを呼び出すには、<bpt id="p2">**</bpt>super()<ept id="p2">**</ept> を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="522">
          <source>The following example shows the <bpt id="p1">**</bpt>new<ept id="p1">**</ept> method for the <bpt id="p2">**</bpt>YourDerivedClass<ept id="p2">**</ept> class in the previous <bpt id="p3">**</bpt>classDeclaration<ept id="p3">**</ept> example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、前の <bpt id="p1">**</bpt>classDeclaration<ept id="p1">**</ept> の例の <bpt id="p2">**</bpt>YourDerivedClass<ept id="p2">**</ept> クラスの <bpt id="p3">**</bpt>new<ept id="p3">**</ept> メソッドを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="523">
          <source>In this <bpt id="p1">**</bpt>new<ept id="p1">**</ept> method, the code constructs an instance of the <bpt id="p2">**</bpt>Rectangle<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この<bpt id="p1">**</bpt>新しい<ept id="p1">**</ept>メソッドで、コードは<bpt id="p2">**</bpt>長方形<ept id="p2">**</ept>クラスのインスタンスを構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="524">
          <source>The instance is assigned to the <bpt id="p1">**</bpt>m<ph id="ph1">\_</ph>rectangle<ept id="p1">**</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンスは、<bpt id="p1">**</bpt>m<ph id="ph1">\_</ph>rectangle<ept id="p1">**</ept> 変数に割り当てられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="525">
          <source>The <bpt id="p1">**</bpt>this<ept id="p1">**</ept> keyword that is used in the example is optional.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例で使用される <bpt id="p1">**</bpt>this<ept id="p1">**</ept> キーワードはオプションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="526">
          <source>However, if you include it, IntelliSense might be more helpful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、それを含める場合、IntelliSense が役立つ可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="527">
          <source>Garbage collection</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ガベージ コレクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="528">
          <source>Eventually during run time, most objects no longer have any variable that points to them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最終的に実行中では、ほとんどのオブジェクトがそれらを指す変数はなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="529">
          <source>The system scans for these objects and erases them from memory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムはこれらのオブジェクトをスキャンし、それらをメモリから消去します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="530">
          <source>The memory space then becomes available for other uses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、メモリ空間は他の用途に利用できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="531">
          <source>The <bpt id="p1">**</bpt>Object<ept id="p1">**</ept> class has a method that is named <bpt id="p2">**</bpt>finalize<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Object<ept id="p1">**</ept> クラスには、<bpt id="p2">**</bpt>finalize<ept id="p2">**</ept> というメソッドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="532">
          <source>However, the <bpt id="p1">**</bpt>finalize<ept id="p1">**</ept> method isn't a destructor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>確定<ept id="p1">**</ept>メソッドはデストラクタではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="533">
          <source>The runtime never calls the <bpt id="p1">**</bpt>finalize<ept id="p1">**</ept> method, even when an object is collected as garbage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ランタイムは、オブジェクトがガベージとして収集された場合でも、<bpt id="p1">**</bpt>finalize<ept id="p1">**</ept> メソッドを呼び出すことはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="534">
          <source>System classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="535">
          <source>In Application Explorer, under <bpt id="p1">**</bpt>System Documentation<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Classes<ept id="p2">**</ept>, there is a list of the kernel classes or system classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーの<bpt id="p1">**</bpt>システムのドキュメント<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>クラス<ept id="p2">**</ept>には、カーネル クラスまたはシステム クラスの一覧があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="536">
          <source>System classes aren't written in X++, and you can't see their source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム クラスは、X++ で記述されておらず、ソース コードを表示することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="537">
          <source>You can't add system classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム クラスを追加することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="538">
          <source>System classes usually have a <bpt id="p1">**</bpt>new<ept id="p1">**</ept> method, but they don't have a <bpt id="p2">**</bpt>classDeclaration<ept id="p2">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム クラには通常、<bpt id="p1">**</bpt>new<ept id="p1">**</ept> メソッドがありますが、<bpt id="p2">**</bpt>classDeclaration<ept id="p2">**</ept> ノードはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="539">
          <source>Every application class implicitly extends the <bpt id="p1">**</bpt>Object<ept id="p1">**</ept> system class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのアプリケーション クラスは<bpt id="p1">**</bpt>オブジェクト<ept id="p1">**</ept>システム クラスを暗黙的に拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="540">
          <source>Some system classes are extended by an application class that has a similar name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部のシステム クラスは、類似した名前を持つアプリケーション クラスで拡張されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="541">
          <source>For instance, <bpt id="p1">**</bpt>xClassFactory<ept id="p1">**</ept> is extended by <bpt id="p2">**</bpt>ClassFactory<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>xClassFactory<ept id="p1">**</ept> が <bpt id="p2">**</bpt>ClassFactory<ept id="p2">**</ept> ごとに延期されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="542">
          <source>In these cases, you should not use the system class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのような場合、システム クラスは使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="543">
          <source>For more information, see "Substitute application classes for system classes" in <bpt id="p1">[</bpt>X++ classes and methods<ept id="p1">](xpp-classes-methods.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>X++ クラスおよびメソッド<ept id="p1">](xpp-classes-methods.md)</ept> で「システム クラスの代替アプリケーション クラス」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="544">
          <source>Extension methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="545">
          <source>The extension method feature lets you add extension methods to a target class by writing the methods in a separate extension class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張メソッド機能を使用すると、メソッドを別の拡張クラスに記述することによって、拡張メソッドを対象クラスに追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="546">
          <source>The following rules apply:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のルールが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="547">
          <source>The extension class must be static.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスは静的でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="548">
          <source>The name of the extension class must end with the ten-character suffix <bpt id="p1">**</bpt><ph id="ph1">\_</ph>Extension<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスの名前は、10 文字の接尾語 <bpt id="p1">**</bpt><ph id="ph1">\_</ph>Extension<ept id="p1">**</ept> で終了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="549">
          <source>However, there’s no restriction on the part of the name that precedes the suffix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、接尾辞に先行する名前の部分には制限はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="550">
          <source>Every extension method in the extension class must be declared as <bpt id="p1">**</bpt>public static<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子クラス内のすべての拡張子メソッドは、<bpt id="p1">**</bpt>パブリック静的<ept id="p1">**</ept>として宣言する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="551">
          <source>The first parameter in every extension method is the type that the extension method extends.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての拡張メソッドの最初のパラメーターは、拡張メソッドが拡張する型です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="552">
          <source>However, when the extension method is called, the caller must not pass in anything for the first parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、拡張メソッドが呼び出されると、呼び出し元は最初のパラメーターに対して何も渡す必要がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="553">
          <source>Instead, the system automatically passes in the required object for the first parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、システムが最初のパラメーターに必要なオブジェクトを自動的に渡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="554">
          <source>The target of an extension method must be a class, table, view, or map application object type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張メソッドのターゲットは、クラス、テーブル、ビュー、またはマップ アプリケーション オブジェクト タイプである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="555">
          <source>An extension class can contain private or protected static methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスはプライベートまたは保護された静的メソッドを含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="556">
          <source>These methods are typically used for implementation details and aren't exposed as extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドは通常、実装の詳細に使用され、拡張として公開されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="557">
          <source>The extension method technique doesn’t affect the source code of the class that it extends.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張メソッドの手法は、拡張するクラスのソース コードには影響しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="558">
          <source>Therefore, the addition to the class doesn't require over-layering.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、クラスへの追加はオーバーレイを必要なく行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="559">
          <source>Upgrades to the target class are never affected by any existing extension methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット クラスへのアップグレードは、既存の拡張メソッドの影響を受けることはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="560">
          <source>However, if an upgrade to the target class adds a method that has the same name as your extension method, your extension method can no longer be reached through objects of the target class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ターゲット クラスへのアップグレードで拡張メソッドとして同じ名前のメソッドが追加される場合、拡張メソッドはターゲット クラスのオブジェクトを通して到達できなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="561">
          <source>The extension method technique uses the same dot-delimited syntax that you often use to call regular instance methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張メソッドの手法では、通常のインスタンス メソッドを呼び出すときによく使うドット区切り構文と同じものを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="562">
          <source>Extension methods can access all public artifacts of the target class, but they can’t access anything that is protected or private.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張メソッドは、ターゲット クラスのすべてのパブリック コンポーネントにアクセスできますが、保護されたまたはプライベートのオブジェクトには何もアクセスできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="563">
          <source>Therefore, extension methods can be considered a type of syntactic sugar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、拡張メソッドは構文砂糖の一種と考えることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="564">
          <source>Regardless of the target type, an extension class is used to add extension methods to the type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目標タイプに関係なく、拡張機能クラスはタイプに拡張メソッドを追加するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="565">
          <source>For example, an extension table isn't used to add methods to a table, and there’s no such thing as an extension table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、拡張テーブルは、メソッドをテーブルに追加するために使用されていませんし、拡張テーブルというものは存在しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="566">
          <source>Delegates as data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ型としてのデリゲート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="567">
          <source>A <bpt id="p1">*</bpt>delegate<ept id="p1">*</ept> collects methods that subscribe to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>デリゲート<ept id="p1">*</ept>は、それをサブスクライブするメソッドを収集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="568">
          <source>The delegate specifies the parameter signature that all its subscriber methods must share.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートは、すべてのサブスクライバ メソッドが共有する必要があるパラメーター署名を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="569">
          <source>When the delegate is called, the delegate calls each of its subscribers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートが呼び出されると、デリゲートはその各サブスクライバを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="570">
          <source>A delegate never returns a value and <bpt id="p1">**</bpt>can't have a default value<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートは値を返しませんし、<bpt id="p1">**</bpt>既定値を持つことはできません<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="571">
          <source>At first, every delegate has no subscribed methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、すべてのデリゲートにはサブスクライブされたメソッドがありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="572">
          <source>There is no limit on the number of parameters that a delegate can declare, and there is no limitation on the type of those parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートが宣言できるパラメーターの数に制限はなく、これらのパラメーターの種類に制限はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="573">
          <source>The delegate body is always empty, because the delegate's only purpose is to define the contract that subscribers must conform to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートの唯一の目的は、サブスクライバが従わなければならない契約を定義することであるため、デリゲート本文は常に空です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="574">
          <source>A delegate doesn't have to be defined in a class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートは、クラスで定義をしなくてもかまいません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="575">
          <source>Delegates can also be defined in a table, form, or query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートは、テーブル、フォーム、またはクエリで定義することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="576">
          <source>Delegate examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="577">
          <source>Tables as data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ型としてのテーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="578">
          <source>All tables can be treated as class definitions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのテーブルはクラス定義として扱うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="579">
          <source>A table variable can be considered an instance (object) of the table (class) definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル変数は、テーブル (class) の定義のインスタンス (オブジェクト) と見なすことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="580">
          <source>For every field in a table variable, the default value is <bpt id="p1">**</bpt>empty<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル変数の各フィールドでは、既定値は<bpt id="p1">**</bpt>空<ept id="p1">**</ept>です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="581">
          <source>You can address fields and create methods on tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドに注意を向けてテーブル上でメソッドを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="582">
          <source>The methods can be invoked on instances of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドは、テーブルのインスタンス上で呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="583">
          <source>To manipulate (that is, read, update, insert, and delete) records in tables, you must declare at least one table variable that can hold the record in focus.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル内のレコードを操作 (つまり、読み取り、更新、挿入、削除) するには、レコードを保持しておくための少なくとも 1 つのテーブル変数を宣言する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="584">
          <source>As a best practice, you should use the name of the table as the name of the variable but use an initial lowercase letter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティスは、変数の名前としてテーブルの名前を使用する必要がありますが、最初の小文字を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="585">
          <source>Here are a few important differences between tables and objects:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルとオブジェクト間のいくつかの重要な違いを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="586">
          <source>You can't allocate space for table variables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル変数の容量を割り当てることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="587">
          <source>Allocation is done implicitly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配賦は暗黙的に行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="588">
          <source>Fields in table variables are public.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル変数のフィールドは、パブリックです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="589">
          <source>You can reference them anywhere.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意の場所でそれを参照することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="590">
          <source>Fields in table variables can be referenced by using expressions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル変数のフィールドは、式を使用して参照できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="591">
          <source>There is no automatic conversion, but table variables that are declared as <bpt id="p1">**</bpt>Common<ept id="p1">**</ept> can hold data from any table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動変換はありませんが、<bpt id="p1">**</bpt>共通<ept id="p1">**</ept>として宣言されているテーブル変数は、どのテーブルからでもデータを保持できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="592">
          <source>Scope of table variables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル変数の範囲</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="593">
          <source>In most respects, table variables can be considered objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの点で、テーブル変数をオブジェクトとみなすことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="594">
          <source>However, unlike objects, they aren't explicitly allocated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、オブジェクトとは異なり、それらは明示的に割り当てられません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="595">
          <source>Only a variable declaration is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数の宣言のみ必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="596">
          <source>All tables are compatible with the Common table, just as all objects are compatible with the <bpt id="p1">**</bpt>Object<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのテーブルには共通のテーブルと互換性があるように、すべてのオブジェクトにも<bpt id="p1">**</bpt>オブジェクト<ept id="p1">**</ept>クラスの互換性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="597">
          <source>Table variables are declared as common buffers and can be used to hold data from any table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル変数は、一般的なバッファーとして宣言され、任意のテーブルからデータを保持するために使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="598">
          <source>You can't access tables that don't have table variables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル変数を持たないテーブルにはアクセスできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="599">
          <source>The principles for declaring table variables and objects are the same, except with regard to the allocation of space.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの変数およびオブジェクトの宣言の原則は、領域の割り当てに関する点を除いて同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="600">
          <source>Table examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="601">
          <source>The syntax enables various possibilities for referencing fields in records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文は、レコード内のフィールドを参照するさまざまな可能性を高めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="602">
          <source>For example, you can use the <bpt id="p1">**</bpt>TableName.(FieldId)<ept id="p1">**</ept> syntax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>TableName.(FieldId)<ept id="p1">**</ept> 構文を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="603">
          <source>The following example prints the contents of the fields in the current record in the Customer table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、顧客テーブルの現在のレコードにあるフィールドの内容を出力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="604">
          <source>The following example uses the <bpt id="p1">**</bpt>fieldCnt<ept id="p1">**</ept> and <bpt id="p2">**</bpt>fieldCnt2Id<ept id="p2">**</ept> methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>fieldCnt<ept id="p1">**</ept> および <bpt id="p2">**</bpt>fieldCnt2Id<ept id="p2">**</ept> メソッドを使用しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="605">
          <source>The <bpt id="p1">**</bpt>fieldCnt<ept id="p1">**</ept> method counts the number of fields in a table, whereas <bpt id="p2">**</bpt>fieldCnt2Id<ept id="p2">**</ept> returns the ID for a field number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>fieldCnt<ept id="p1">**</ept> メソッドは、テーブル内のフィールドの数をカウントしますが、<bpt id="p2">**</bpt>fieldCnt2Id<ept id="p2">**</ept> はフィールド番号の ID を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="606">
          <source>For example, you can use the <bpt id="p1">**</bpt>fieldCnt2Id<ept id="p1">**</ept> method to learn that field number 6 in a table has the ID 54.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>fieldCnt2Id<ept id="p1">**</ept> メソッドを使用して、テーブルでそのフィールド番号 6 が ID 54 を持っていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="607">
          <source>This conversion is required, because there is no guarantee that the IDs of the fields in a table are consecutive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この変換は、表内のフィールドの ID が連続しているという保証がないため、この変換が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="608">
          <source>Collection classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コレクション クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="609">
          <source>The X++ language syntax provides two composite types: arrays and containers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ 言語の構文には、配列とコンテナーという 2 種類の複合が用意されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="610">
          <source>These composite types are useful for aggregating values of primitive types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの複合型は、プリミティブ型の値を集約するのに便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="611">
          <source>However, you can't store class objects in arrays or containers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、配列またはコンテナーのクラス オブジェクトを格納することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="612">
          <source><bpt id="p1">*</bpt>Collection classes<ept id="p1">*</ept> are used to store objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>コレクション クラス<ept id="p1">*</ept>はオブジェクトの格納に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="613">
          <source>They let you create arrays, lists, sets, maps, and structs that can hold any data type, even objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは、配列、リスト、セット、マップ、任意のデータ型を保持できる構造、オブジェクトさえも作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="614">
          <source>For maximum performance, the classes are implemented in C++ (they are system classes).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最大パフォーマンスについては、C++ (システム クラス) で、クラスが実装されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="615">
          <source>Collection classes were previously known as <bpt id="p1">*</bpt>foundation classes<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>ファンデーション クラス<ept id="p1">*</ept>と呼ばれていたコレクション クラス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="616">
          <source>The collection classes are <bpt id="p1">**</bpt>Array<ept id="p1">**</ept>, <bpt id="p2">**</bpt>List<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Map<ept id="p3">**</ept>, <bpt id="p4">**</bpt>Set<ept id="p4">**</ept>, and <bpt id="p5">**</bpt>Struct<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コレクション クラスは、<bpt id="p1">**</bpt>配列<ept id="p1">**</ept>、<bpt id="p2">**</bpt>リスト<ept id="p2">**</ept>、<bpt id="p3">**</bpt>マップ<ept id="p3">**</ept>、<bpt id="p4">**</bpt>設定<ept id="p4">**</ept>、および<bpt id="p5">**</bpt>構造体<ept id="p5">**</ept>です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="617">
          <source><bpt id="p1">**</bpt>Array<ept id="p1">**</ept> – This class resembles the <bpt id="p2">**</bpt>array<ept id="p2">**</ept> type in the X++ language, but it can hold values of any single type, even objects and records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>配列<ept id="p1">**</ept> - このクラスは、X++ 言語の<bpt id="p2">**</bpt>配列<ept id="p2">**</ept>タイプに似ていますが、単一タイプ、オブジェクトおよびレコードの値を保持できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="618">
          <source>Objects are accessed in a specific order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクトは、特定の順序でアクセスされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="619">
          <source><bpt id="p1">**</bpt>List<ept id="p1">**</ept> – This class contains elements that are accessed sequentially.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リスト<ept id="p1">**</ept> – このクラスには、順にアクセスされる要素が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="620">
          <source>Unlike an array, the <bpt id="p1">**</bpt>List<ept id="p1">**</ept> class provides an <bpt id="p2">**</bpt>addStart<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配列とは異なり、<bpt id="p1">**</bpt>List<ept id="p1">**</ept> クラスは <bpt id="p2">**</bpt>addStart<ept id="p2">**</ept> メソッドを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="621">
          <source>Like the <bpt id="p1">**</bpt>Set<ept id="p1">**</ept> class, the <bpt id="p2">**</bpt>List<ept id="p2">**</ept> class provides the <bpt id="p3">**</bpt>getEnumerator<ept id="p3">**</ept> and <bpt id="p4">**</bpt>getIterator<ept id="p4">**</ept> methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Set<ept id="p1">**</ept> クラスと同様に、<bpt id="p2">**</bpt>List<ept id="p2">**</ept> クラスは <bpt id="p3">**</bpt>getEnumerator<ept id="p3">**</ept> メソッドと <bpt id="p4">**</bpt>getIterator<ept id="p4">**</ept> メソッドを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="622">
          <source>You can use an iterator to insert and delete items from a <bpt id="p1">**</bpt>List<ept id="p1">**</ept> object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">反復子を使用して、<bpt id="p1">**</bpt>リスト<ept id="p1">**</ept> オブジェクトから項目を挿入および削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="623">
          <source><bpt id="p1">**</bpt>Map<ept id="p1">**</ept> – This class associates a key value with another value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>マップ<ept id="p1">**</ept> – このクラスはキー値を別の値に関連付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="624">
          <source><bpt id="p1">**</bpt>Set<ept id="p1">**</ept> – This class holds values of any single type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定<ept id="p1">**</ept> – このクラスは、1 つのタイプの値を保持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="625">
          <source>Values aren't stored in the sequence in which they are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値は、追加された順序で格納されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="626">
          <source>Instead, the <bpt id="p1">**</bpt>Set<ept id="p1">**</ept> object stores the value in a manner that optimizes performance for the <bpt id="p2">**</bpt>in<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、<bpt id="p1">**</bpt>Set<ept id="p1">**</ept> オブジェクトは <bpt id="p2">**</bpt>in<ept id="p2">**</ept> メソッドのパフォーマンスを最適化するように値を格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="627">
          <source>A <bpt id="p1">**</bpt>Set<ept id="p1">**</ept> object ignores any attempt to add a value that the <bpt id="p2">**</bpt>Set<ept id="p2">**</ept> object is already storing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セット<ept id="p1">**</ept>オブジェクトは、<bpt id="p2">**</bpt>セット<ept id="p2">**</ept>オブジェクトが既に格納している値を追加しようとする試みをすべて無視します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="628">
          <source>Unlike the <bpt id="p1">**</bpt>Array<ept id="p1">**</ept> class, the <bpt id="p2">**</bpt>Set<ept id="p2">**</ept> class provides the <bpt id="p3">**</bpt>in<ept id="p3">**</ept> and <bpt id="p4">**</bpt>remove<ept id="p4">**</ept> methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Set<ept id="p2">**</ept> クラスは、<bpt id="p1">**</bpt>Array<ept id="p1">**</ept> クラスとは異なり、<bpt id="p3">**</bpt>in<ept id="p3">**</ept> メソッドと <bpt id="p4">**</bpt>remove<ept id="p4">**</ept> メソッドを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="629">
          <source><bpt id="p1">**</bpt>Struct<ept id="p1">**</ept> – This class can contain values of more than one type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構造体<ept id="p1">**</ept> – このクラスは、1 つ以上のタイプの値を含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="630">
          <source>It's used to group information about a specific entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、特定のエンティティに関する情報をグループ化するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="631">
          <source>The constructor for every collection class except <bpt id="p1">**</bpt>Struct<ept id="p1">**</ept> takes a type parameter that is an element of the <bpt id="p2">**</bpt>Types<ept id="p2">**</ept> system enum.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構造体<ept id="p1">**</ept>を除くすべてのコレクション クラスのコンストラクターは、<bpt id="p2">**</bpt>型<ept id="p2">**</ept>システム列挙型の要素である型パラメーターをとります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="632">
          <source>The collection instance can store items of that type only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コレクション インスタンスは、その型のアイテムのみを格納できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="633">
          <source>The <bpt id="p1">**</bpt>Types::AnyType<ept id="p1">**</ept> enum element is a special case that can't be used to construct a collection object, such as a <bpt id="p2">**</bpt>Set<ept id="p2">**</ept> object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Types::AnyType<ept id="p1">**</ept> 列挙要素は、<bpt id="p2">**</bpt>Set<ept id="p2">**</ept> オブジェクトなどのコレクション オブジェクトを作成するために使用できない特殊なケースです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="634">
          <source>The <bpt id="p1">**</bpt>null<ept id="p1">**</ept> value can't be stored as an element in a <bpt id="p2">**</bpt>Set<ept id="p2">**</ept> object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>null<ept id="p1">**</ept> 値は、<bpt id="p2">**</bpt>Set<ept id="p2">**</ept> オブジェクトに要素として格納できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="635">
          <source>Additionally, <bpt id="p1">**</bpt>null<ept id="p1">**</ept> can't be a key in a <bpt id="p2">**</bpt>Map<ept id="p2">**</ept> object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p2">**</bpt>マップ<ept id="p2">**</ept> オブジェクトで <bpt id="p1">**</bpt>null<ept id="p1">**</ept> はキーになることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="636">
          <source>You can iterate through a collection object by using an iterator or enumerator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">反復子または列挙子を使用して、コレクション オブジェクトを介して反復することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="637">
          <source>Here are typical examples that show how you can obtain an iterator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">反復子を取得する方法を示す一般的な例を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="638">
          <source>For <bpt id="p1">**</bpt>Set<ept id="p1">**</ept> objects, if any elements are added or removed after an iterator is created, the iterator instance can no longer be used to read from or step through the collection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定<ept id="p1">**</ept>オブジェクトで、任意の要素が追加または反復子が作成された後に削除される場合、反復子インスタンスは読み取りまたはコレクションによるステップで使用されることはなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="639">
          <source>For <bpt id="p1">**</bpt>Map<ept id="p1">**</ept> objects, as for <bpt id="p2">**</bpt>Set<ept id="p2">**</ept> objects, if any elements are removed, the iterator is no longer valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>マップ<ept id="p1">**</ept>オブジェクトで、<bpt id="p2">**</bpt>設定<ept id="p2">**</ept>オブジェクトと同じように、任意の要素が削除されると、反復子が有効ではなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="640">
          <source>However, a <bpt id="p1">**</bpt>MapIterator<ept id="p1">**</ept> object remains valid even after a call to the <bpt id="p2">**</bpt>Map.insert<ept id="p2">**</ept> method, regardless of whether the key is new, or whether the key already exists and only the value is being updated in the <bpt id="p3">**</bpt>Map<ept id="p3">**</ept> element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、キーが新しいか、またはキーが既に存在していてその値のみが<bpt id="p3">**</bpt>マップ<ept id="p3">**</ept>要素で更新されているかどうかに関係なく、<bpt id="p2">**</bpt>Map.insert<ept id="p2">**</ept> メソッドへの呼び出し後も、<bpt id="p1">**</bpt>MapIterator<ept id="p1">**</ept> オブジェクトは有効です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="641">
          <source>Code that calls <bpt id="p1">**</bpt>Map.insert<ept id="p1">**</ept> and depends on the iterator object remaining valid might fail if it's run as .NET Framework CIL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Map.insert<ept id="p1">**</ept> を呼び出し、反復子オブジェクトが有効であることに依存するコードは、.NET Framework CIL として実行されると失敗する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="642">
          <source>You can use the collection classes to form more complex classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コレクション クラスを使用するとより複雑なクラスを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="643">
          <source>For example, you can easily implement a stack by using a list where elements are always added to the beginning of the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、リストの先頭に要素が常に追加されるリストを使用して、スタックを簡単に実装できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="644">
          <source>The newest element then occupies the top of the stack.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新の要素がスタックの先頭を占めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="645">
          <source>You can also extend the collection classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コレクション クラスを拡張することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="646">
          <source>For example, you can extend the <bpt id="p1">**</bpt>List<ept id="p1">**</ept> class to create a list of customer records where the operations are type-safe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>リスト<ept id="p1">**</ept>クラスを拡張して、操作がタイプ セーフである顧客レコードの一覧を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="647">
          <source>In this case, the derived collection class will accept only customer records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、派生したコレクション クラスは顧客レコードのみを受け入れます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="648">
          <source>Extended data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="649">
          <source><bpt id="p1">*</bpt>Extended data types<ept id="p1">*</ept> are user-defined types that are based on the <bpt id="p2">**</bpt>boolean<ept id="p2">**</ept>, <bpt id="p3">**</bpt>int<ept id="p3">**</ept>, <bpt id="p4">**</bpt>int64<ept id="p4">**</ept>, <bpt id="p5">**</bpt>real<ept id="p5">**</ept>, <bpt id="p6">**</bpt>str<ept id="p6">**</ept>, and <bpt id="p7">**</bpt>date<ept id="p7">**</ept> primitive data types, and on the <bpt id="p8">**</bpt>container<ept id="p8">**</ept> composite type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>拡張データ型<ept id="p1">*</ept>は<bpt id="p2">**</bpt>ブール<ept id="p2">**</ept>、<bpt id="p3">**</bpt>int<ept id="p3">**</ept>、<bpt id="p4">**</bpt>int64<ept id="p4">**</ept>、<bpt id="p5">**</bpt>実数<ept id="p5">**</ept>、<bpt id="p6">**</bpt>str<ept id="p6">**</ept>、および<bpt id="p7">**</bpt>日付<ept id="p7">**</ept>プリミティブ データ型、および<bpt id="p8">**</bpt>コンテナー<ept id="p8">**</ept>複合型に基づくユーザー定義型です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="650">
          <source>An EDT is a primitive data type or container that has a supplementary name and additional properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT はプリミティブ データ型または補助名および追加のプロパティを持つコンテナーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="651">
          <source>For example, you can create a new EDT that is named <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> and base it on a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、文字列を基準にして、<bpt id="p1">**</bpt>名前<ept id="p1">**</ept>という新しい EDT を作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="652">
          <source>You can then use the new EDT in variable and field declarations in the development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい EDT は、開発環境の変数とフィールド宣言で使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="653">
          <source>You can also base EDTs on other EDTs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、EDT を他の EDT の基準にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="654">
          <source>EDTs are standard data types, but they have a specific name and additional properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDTs は、標準的なデータ型ですが、特定の名前および追加のプロパティがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="655">
          <source>EDTs undergo the same value and type <bpt id="p1">[</bpt>conversions<ept id="p1">](xpp-conversion-run-time-functions.md)</ept> as the standard data types that they are based on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDTs は、それらが基づいている標準データ型と同じ値とタイプ<bpt id="p1">[</bpt>換算<ept id="p1">](xpp-conversion-run-time-functions.md)</ept>を適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="656">
          <source>Here are the benefits of EDTs:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT の利点を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="657">
          <source>Code is easier to read, because variables have a meaningful data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数は意味のあるデータ型を持つため、コードは読みやすくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="658">
          <source>For example, the data type is <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> instead of <bpt id="p2">**</bpt>str<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、データ型は <bpt id="p2">**</bpt>str<ept id="p2">**</ept> の代わりに<bpt id="p1">**</bpt>名前<ept id="p1">**</ept>です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="659">
          <source>The properties that you set for an EDT are used by all instances of that type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT に設定するプロパティは、そのタイプのすべてのインスタンスで使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="660">
          <source>Therefore, EDTs help reduce work and promote consistency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、EDT は作業を減らし、一貫性を促進するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="661">
          <source>For example, account numbers (<bpt id="p1">**</bpt>AccountNum<ept id="p1">**</ept> data type) have the same properties throughout the system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、勘定番号 (<bpt id="p1">**</bpt>AccountNum<ept id="p1">**</ept> データ型) には、システム全体で同じプロパティがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="662">
          <source>You can create hierarchies of EDTs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT の階層を作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="663">
          <source>The EDTs can inherit the appropriate properties from the parent, and you can change other properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT は、親から適切なプロパティを継承でき、その他のプロパティを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="664">
          <source>For example, the <bpt id="p1">**</bpt>ItemCode<ept id="p1">**</ept> data type is used as the basis for the <bpt id="p2">**</bpt>MarkupItemCode<ept id="p2">**</ept> and <bpt id="p3">**</bpt>PriceDiscItemCode<ept id="p3">**</ept> data types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>ItemCode<ept id="p1">**</ept> データ型が、<bpt id="p2">**</bpt>MarkupItemCode<ept id="p2">**</ept> および <bpt id="p3">**</bpt>PriceDiscItemCode<ept id="p3">**</ept> データ型の基準として使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="665">
          <source>Create an EDT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT の作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="666">
          <source>This feature isn't implemented as a language construct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、言語コンストラクトとして実装されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="667">
          <source>To create an EDT, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT を作成するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="668">
          <source>In Solution Explorer, right-click on the project, point to <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New item<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、プロジェクトを右クリックして<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をポイントしてから<bpt id="p2">**</bpt>新しい項目<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="669">
          <source>In the <bpt id="p1">**</bpt>Add New Item<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>Installed<ept id="p2">**</ept> and then <bpt id="p3">**</bpt>Artifacts<ept id="p3">**</ept> in the left pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しい項目の追加<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>インストール済み<ept id="p2">**</ept>を選択してから左ウィンドウの<bpt id="p3">**</bpt>アーティファクト<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="670">
          <source>In the middle pane, select the EDT type to create.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">中央ウィンドウで、作成する EDT タイプを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="671">
          <source>Enter a name, and then click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を入力し、次に<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="672">
          <source>EDT example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT 例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="673">
          <source>Null values for data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ型の null 値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="674">
          <source>Microsoft Dynamics 365 for Finance and Operations doesn't support the concept of <bpt id="p1">**</bpt>null<ept id="p1">**</ept> values that is available in many other database management systems (DBMSs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations は、その他の数多くのデータベース管理システム (DBMS) で使用できる <bpt id="p1">**</bpt>null<ept id="p1">**</ept> 値の概念をサポートしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="675">
          <source>A variable in X++ always has a type and a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の変数は、常にタイプと値を持ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="676">
          <source>However, for each data type, one value is considered <bpt id="p1">**</bpt>null<ept id="p1">**</ept> (for example, when the <bpt id="p2">**</bpt>validateField<ept id="p2">**</ept> table method is run).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、各データ タイプでは、1 つの値が <bpt id="p1">**</bpt>null<ept id="p1">**</ept> と見なされます (たとえば、<bpt id="p2">**</bpt>validateField<ept id="p2">**</ept> テーブル メソッドの実行時)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="677">
          <source>Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">種類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="678">
          <source>Value that is treated as null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">null として扱われる値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="679">
          <source>Date</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="680">
          <source>1900-01-01</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1900-01-01</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="681">
          <source>Enum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="682">
          <source>An element that has its value set to <bpt id="p1">**</bpt>0<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その値が <bpt id="p1">**</bpt>0<ept id="p1">**</ept> に設定されている要素</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="683">
          <source>Integer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">整数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="684">
          <source>0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="685">
          <source>Real</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="686">
          <source>0.0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">0.0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="687">
          <source>String</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="688">
          <source>An empty string</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">空の文字列</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="689">
          <source>Time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">時刻</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="690">
          <source>00:00:00</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">00:00:00</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="691">
          <source>Utcdatetime</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Utcdatetime</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="692">
          <source>Any value that has its date portion set to <bpt id="p1">**</bpt>1900-01-01<ept id="p1">**</ept>, regardless of the value of the time portion For example, the value <bpt id="p2">**</bpt>1900-01-01T22:33:44<ept id="p2">**</ept> is treated as <bpt id="p3">**</bpt>null<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">時間部分の値に関係なく、日付部分が <bpt id="p1">**</bpt>1900-01-01<ept id="p1">**</ept> に設定されている値たとえば、値 <bpt id="p2">**</bpt>1900-01-01T22:33:44<ept id="p2">**</ept> は <bpt id="p3">**</bpt>null<ept id="p3">**</ept> として扱われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="693">
          <source>Note that any <bpt id="p1">**</bpt>utcDateTime<ept id="p1">**</ept> value that has its date portion set to <bpt id="p2">**</bpt>1900-01-01<ept id="p2">**</ept> is shown as blank by the X++ <bpt id="p3">**</bpt>print<ept id="p3">**</ept> statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付部分が <bpt id="p2">**</bpt>1900-01-01<ept id="p2">**</ept> に設定されている <bpt id="p1">**</bpt>utcDateTime<ept id="p1">**</ept> 値は X++ <bpt id="p3">**</bpt>print<ept id="p3">**</ept> ステートメントでは空白で表示されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="694">
          <source>Only the value <bpt id="p1">**</bpt>1900-01-01T00:00:00<ept id="p1">**</ept> is shown as blank by the <bpt id="p2">**</bpt>Global::info<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>1900-01-01T00:00:00<ept id="p1">**</ept> 値のみ空白として <bpt id="p2">**</bpt>Global::info<ept id="p2">**</ept> メソッドにより表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="695">
          <source>That value is the value from the <bpt id="p1">**</bpt>DateTimeUtil::MinValue<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値は、<bpt id="p1">**</bpt>DateTimeUtil::MinValue<ept id="p1">**</ept> メソッドの値です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="696">
          <source>Therefore, when the <bpt id="p1">**</bpt>validateField<ept id="p1">**</ept> method checks whether a user has entered a value in a mandatory field, <bpt id="p2">**</bpt>0<ept id="p2">**</ept> isn't accepted in an <bpt id="p3">**</bpt>integer<ept id="p3">**</ept> type field, the first entry isn't accepted in an <bpt id="p4">**</bpt>enum<ept id="p4">**</ept> type field, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p1">**</bpt>validateField<ept id="p1">**</ept> メソッドによりユーザーが必須項目に入力したかどうかがチェックされる際、たとえば、<bpt id="p2">**</bpt>0<ept id="p2">**</ept> は <bpt id="p3">**</bpt>integer<ept id="p3">**</ept> タイプ フィールドで許容されず、最初のエントリは <bpt id="p4">**</bpt>enum<ept id="p4">**</ept> タイプ フィールドで許容されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="697">
          <source>Additionally, in SQL X++ statements, the values that are listed in the previous table yield <bpt id="p1">**</bpt>false<ept id="p1">**</ept> in a Boolean comparison.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、SQL X++ ステートメントで、前のテーブルにリストされている値は、ブール値比較で <bpt id="p1">**</bpt>false<ept id="p1">**</ept> になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="698">
          <source>However, In non-SQL X++ statements, the equal and relational operators work with these values, just as they work with other values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、非 SQL X++ ステートメントでは、同等演算子およびリレーショナル演算子は他の値に対して動作するのと同じように、これらの値に対して動作します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="699">
          <source>Variables of the <bpt id="p1">**</bpt>container<ept id="p1">**</ept> type, and classes and variables of the <bpt id="p2">**</bpt>table<ept id="p2">**</ept> type can be <bpt id="p3">**</bpt>null<ept id="p3">**</ept> in the traditional DBMS sense.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">従来の DBMS の意味では、<bpt id="p1">**</bpt>コンテナー<ept id="p1">**</ept>型と<bpt id="p2">**</bpt>テーブル<ept id="p2">**</ept>型のクラスおよび変数は <bpt id="p3">**</bpt>null<ept id="p3">**</ept> とすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="700">
          <source>A <bpt id="p1">**</bpt>table<ept id="p1">**</ept> type is <bpt id="p2">**</bpt>null<ept id="p2">**</ept> if all its fields have their <bpt id="p3">**</bpt>null<ept id="p3">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル<ept id="p1">**</ept>タイプは、すべてのフィールドに <bpt id="p3">**</bpt>null<ept id="p3">**</ept> 値がある場合は <bpt id="p2">**</bpt>null<ept id="p2">**</ept> です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
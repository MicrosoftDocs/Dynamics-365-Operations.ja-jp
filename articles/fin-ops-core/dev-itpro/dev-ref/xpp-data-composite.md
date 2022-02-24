---
title: X++ 複合データ型
description: このトピックでは、X++ の複合データ型について説明します。
author: RobinARH
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150183
ms.assetid: 0ff4e759-851d-4b53-aa67-6f03eee53f02
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75c9a9694441ceed2e9f12700e0aca3170fb5c94
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644859"
---
# <a name="x-composite-data-types"></a>X++ 複合データ型

[!include [banner](../includes/banner.md)]

このトピックでは、X++ の複合データ型について説明します。 X++ の複合データ型は、配列、コンテナー、データ型としてのクラス、データ型としてのデリゲート、データ型としてのテーブルです。

## <a name="array"></a>配列

*配列* は同じデータ型を持つ項目のリストを含む変数です。 配列の要素は、整数インデックスを使用してアクセスされます。 配列内の各要素を初期化するには、別のステートメントを使用します。 コンテナー データ型または配列オブジェクトを使用してコレクションを作成するとき、1 つのステートメントを使用して複数の要素を初期化できます。 既定では、配列内のすべての項目は配列のデータ型の既定値を持ちます。 *動的配列*、*固定長配列*、*ディスク配列の一部* の 3 種類の配列があります。

- **動的配列** - これらの配列は、空の配列オプションを使用して宣言されます。 つまり、かっこ (\[\]) だけがあります。
- **固定長の配列** – これらの配列は、宣言で指定されている品目の数を保持できます。 固定長の配列は動的配列と宣言されますが、かっこ内に長さのオプションが含まれます。
- **ディスク配列の一部** – これらの配列は、動的配列または固定長の配列として宣言され、メモリに保持する品目の数を宣言するオプションが追加されています。 他の項目はディスクに保存され、参照されると自動的に読み込まれます。

X++ は1次元配列のみをサポートしています。 ただし、複数の配列インデックスの動作を再現することができます。 (詳細については、[複数の配列インデックス](#multiple-array-indexes) セクションを参照してください)。 オブジェクトとテーブル内の変数は配列として宣言することができます。 たとえば、この機能は、標準アプリケーションの住所明細行で使用されます。 配列コレクション クラスを配列内のオブジェクトに格納できます。 

配列インデックスは 1 から開始されます。 配列の最初の項目は \[1\] で参照され、2番目の項目は、 \[2\] などで参照されます。 次の構文は、配列要素にアクセスするために使用されます: **ArrayItemReference = ArrayVariable \[ Index \]**。 この構文では、**ArrayVariable** は配列の識別子であり、**Index** は配列要素の数です。 **インデックス** には整数式を指定できます。 項目ゼロ \[0\] は配列をクリアするために使用します。 値が配列のインデックス 0 に割り当てられている場合は、配列内のすべての要素が既定値にリセットされます。

### <a name="array-examples"></a>配列の例

```xpp
public void ArrayMethod()
{
    int myArray[10]; // Fixed-length array with 10 integers.
    myArray[4] = 1; // Accessing the 4th element in the array.
    myArray[0] = 0; // Resets all elements in intArray. 

    // Dynamic array of integers.
    int intArray[];

    // Dynamic array of variables of type Datatype.
    //Datatype arrayVariable[];

    // Fixed-length arrays.
    boolean boolArray[100]; // Fixed-length array of booleans with 100 items.

    // Two examples of Partly On Disk Arrays.
    // Dynamic integer array with only 100 elements in memory.
    int arrayVariable [ ,100];
    // Fixed-length string array with 1000 elements, and only 200 in memory.
    str arrayVariable2 [1000,200];

    // A dynamic array of integers.
    int i[];
    // A fixed-length real array with 100 elements.
    real r[100];
    // A dynamic array of dates with only 10 elements in memory.
    date d[,10];
    // A fixed length array of NoYes variables with 100 elements and 10 in memory.
    NoYes ny[100,10];
}
```

### <a name="multiple-array-indexes"></a>複数の配列インデックス

C++ および C\# などの一部の言語を使用すると、1 つ以上のインデックスを持つ配列を宣言できます。 つまり、「配列の配列」を定義することができます。 X++ では、1 次元配列のみサポートされているため、複数の配列インデックスを直接作成できません。 ただし、このセクションに記載されているメソッドを使用して、複数のインデックスを実装することができます。 たとえば、国別分析コードにより獲得される量を保持するため、2 つの分析コードを持つ配列を宣言します。 10 の国と 3 つの分析コードがあります。 C++ および C\# では、次の配列を宣言します。

```xpp
// This is C# or C++ code, not X++ code.
real earning[10, 3];
```

ただし、X++ はこの申告をサポートしていません。 代わりに、要素の数が各分析コード内の要素の製品である 1 次元配列を定義することができます。 次に例を示します。

```xpp
public void MultipleArrayMethod()
{
    // Step 1: define a one-dimensional array with the number
    // of elements that is the product of the elements in each dimension.
    real earnings[10*3];

    // Step 2: to refer to a specific element, such as earnings[i,j], write the following:
    // declare i and j (maybe) and assign the value to something
    int i = 1;
    int j = 2;
    real element = earnings[(i-1)*3 + j];
}

// This can be written into a macro like this:
#localmacro.earningIndex
(%1-1)*3+%2
#endmacro

public void CallTheMacro()
{
    // Next, call the specific element within the macro like this:
    int i = 1;
    int j = 2;
    real element = earnings[#earningIndex(i,j)];

    // The previous scheme can be extended to any number of dimensions.
    // The element a[i1, i2, ..., ik] can be accessed by computing the
    // offset into an array containing (d1*d2*...*dk) elements.
    //(i1 - 1)*d2*d3*..*dk +
    //(i2 - 1)*d3*d4*...*dk + .... +
    //(ik-1 -1)*dk +
    //(ik-1)
}
```

## <a name="container"></a>コンテナー

*コンテナー* オブジェクトは、プリミティブ データ型または複合データ型が含まれる項目の動的リストです。 コンテナーは、クライアント層とサーバー層の間でさまざまな種類の値を渡す必要がある場合に便利です。 ただし、ループ内でのリストに繰り返し追加する予定がある場合、コンテナーは適切な選択肢ではありません。 コンテナーは、コンテナーのサイズまたは内容を過度に変更することがないプロセスに最も適しています。 コンテナーに過剰にデータが追加されると、コンテナーのデータを繰り返しコピーする必要があり、また新しい領域を繰り返し割り当てる必要があるため、システム全体のパフォーマンスが低下する可能性があります。 

コンテナーはクラスではありません。 コンテナーには、プリミティブ値またはその他のコンテナーの注文済のシーケンスが含まれています。 **anytype** の柔軟性のために、コンテナーは異なるタイプの値を一緒に保存する良い方法を提供します。 コンテナーは、データベースに保管できます。 コンテナーとは、アプリケーション エクスプローラーを使用して、テーブルに列を追加する場合に選択可能な列タイプの 1 つです。 配列に少し似た、または **List** や **Stack** クラスのようなコレクションのコンテナーです。 ただし、コンテナーを作成した後にコンテナーのサイズまたはコンテンツを変更できません。 

コンテナを変更するために表示される X++ ステートメントは、内部で新しいコンテナを構築して必要に応じ値をコピーします。 コンテナーを別のコンテナー変数に割り当てても、コンテナーの新しいコピーは作成されます。 これらすべての工程はパフォーマンスに影響を与えることがあります。 コンテナーへのアクセスを提供する関数 (**conPeek** など) では、コンテナーは 0 ベースではなく、1 ベースです。 インデックスは配列に対して 1 ベースです。 コンテナーの既定値は **空** です。 コンテナーには値が含まれていません。 コンテナーを使用するステートメントの中には、コンテナーを変更しようとして表示されることがありますが、システム内では、コンテナーが変更されることはありません。 代わりに、元のコンテナーからのデータは、新しいコンテナーを構築するためにコマンドからのデータと結合されます。 **conDel**、**conIns**、または **conPoke** のいずれかの関数を使用して、新しいコンテナを作成することができます。 

また、**グローバル** クラスには、コンテナーを処理するための静的メソッドがあります。 これらのメソッドには、**con2ArraySource**、**con2Buf**、**con2List**、**con2Str**、**containerFromXmlNode**、**conView**、**str2Con** が含まれます。 **conIns** や **conPeek** のような、コンテナーを扱うためのいくつかの固有の関数があります。 X++ **conPeek** 関数は **anytype** 型を返すため、各値の型がわからない場合はコンテナーから値を読み取る方が簡単です。 **anytype** は値を変換することができればすべての X++ 値タイプに割り当てることができます。 明示的なデータ型の変換を回避すると、コードは読みやすくなります。 したがって、値をコンテナーに配置するために使用されたのと同じデータ型にコンテナーから値を割り当てます。 コンテナーを **エニタイプ** に割り当てることはできません。適切な変換を決定できない可能性があるためです。 そのような場合、予期しない動作やエラーが発生する可能性があります。

### <a name="comparing-container-to-other-options"></a>コンテナーと他のオプションの比較

**コンテナー** 型は、**List** や **Stack** などの配列およびコレクション クラスなど、他の構成要素と似ています。 **コンテナー** と **リスト** の違いは、**リスト** クラスのインスタンスが不変であるという点です。 **リスト** オブジェクトは、最初にそのデータが消費するよりも多くの領域を割り当てます。 その後、データが追加されると、スペースが埋められます。 この動作は、要素が追加されるたびに多くの領域を割り当てる場合よりも効率的です。 **リスト** の更新はコンテナーの同様の操作よりも高速に実行します。 

**リスト** オブジェクトを作成するときは、**リスト** オブジェクトが格納できるデータの 1 つのタイプを決定します。 この制限は、コンテナの場合よりも **リスト** の柔軟性が低くなります。 ただし、**リスト** のオブジェクトを格納できますが、コンテナーでは値の型しか格納できません。 コンテナーと配列の違いは、配列は宣言された型の項目だけを保持できるという点です。 配列にメモリ容量を割り当て、後からその容量に値を入力することができます。 たとえば、ループに値を入力することができます。 この動作は効率的であり、適正に動作します。 新しいデータを追加して新しいコンテナーを作成するときは、**+=** 演算子かまたは **conIns** 機能のいずれかを使用します。 **+=** 演算子は高速の代替です。 **conIns** 関数は、元のデータの最後のインデックスの前に新しいデータを追加する場合にのみ使用します。 

Dynamics AX 2012 では、コンテナーのオブジェクト参照を格納するために X++ コンパイラを使用できましたが、結果は実行時に失敗していました。 ただし、Finance and Operations アピリケーションでは、コンテナー内のオブジェクト参照を格納しようとすると、コンパイラがエラー メッセージを表示します。 コンテナーに追加される要素のタイプが **anytype** である場合、コンパイラーは値は参照タイプであるかどうかを決定することをできません。 この場合、コンパイラはその試行を認めます。 コンパイラはコードを誤っていると診断しませんが、エラーは実行時間にスローされます。

### <a name="container-examples"></a>コンテナーの例

```xpp
public void ContainerExample() 
{
    // First, declare the variables you are using.  
    container myContainer;
    container myContainer4;
    container myContainer5; 
    // Three ways to declare a container.
    myContainer = [1];
    myContainer += [2];
    myContainer4 = myContainer5;

    // Declare a container.
    container cr3;

    // Assign a literal container to a container variable.
    cr3 = [22, "blue"];

    // Declare and assign a container.
    container cr2 = [1, "blue", true];

    // Mimic container modification (implicitly creates a copy).
    cr3 += [16, strMyColorString];
    cr3 = conIns(cr3, 1, 3.14);
    cr3 = conPoke(cr3, 2, "violet");

    // Assignment of a container (implicitly creates a copy).
    cr2 = cr3;

    // Read a value from the container.
    str  myStr = conPeek(cr2, 1);

    // One statement that does multiple assignments from a container.
    str myStr;
    int myInt;
    container cr4 = ["Hello", 22, 20\07\1988];
    [myStr, myInt] = cr4; // "Hello", 22

    // Example of applying the = operator to a container. The example
    // initializes myContainer2 and myContainer33.
    myContainer2 = [2, "apple"];

    // Next, you make a copy of myContainer33 and assign the copy to myContainer2.
    myContainer33 = [33, "grape"];
    myContainer2 = myContainer33;  // The container that myContainer2 had been holding is no longer available and cannot be recovered.
    // An example of building a new container by
    // assigning a new value to myContainer33 through the += operator.
    myContainer33 += [34, "banana"];
}

// Container example. In this example, variable2 and variable33 hold different containers.
static void JobC(Args _args)
{
    container variable2, variable33;
    variable2 += [98];
    variable33 = variable2;
    variable2 += [97];
}

// List class example. In this example, variable2 and variable33 refer to the same List object.
static void JobL(Args _args)
{
    List variable2,variable33;
    variable2 = new List(Types::Integer);
    variable2.addEnd(98);
    variable33 = variable2;
    variable2.addEnd(97);
}

// The automatic type conversion by anytype also applies to the special syntax for making multiple
// assignments from a container in one statement. This is shown in the following code example,
// which assigns a str to an int, and an int to a str.
static void JobContainerMultiAssignmentUsesAnytype(Args _args)
{
    container con2;
    int int4;
    str str7;
    con2 = ["11", 222];
    [int4, str7] = con2;
    info(strfmt("int4==11==(%1), str7==222==(%2)", int4, str7));
}

/**_  Output:
Message (10:36:22 am)
int4==11==(11), str7==222==(222)
_*_/

static void UseQuery()
{
    // An example of how the compiler diagnoses attempts to store object in containers
    container c = [new Query()];   // This statement will cause the error message shown below.
    /_*_ Instance of type 'Query' cannot be added to a container. _*_/

    // An example of a code that won't cause an error message, but will
    // cause an error message to be thrown at runtime.
    anytype a = new Query();
    container d = [a];
}
```

## <a name="classes-as-data-types"></a>データ型としてのクラス

クラス*は、クラスのインスタンスの変数とメソッドの両方を説明するタイプ定義です。 (クラスのインスタンスは *オブジェクト* ともよばれます。) クラスはオブジェクトの定義に過ぎず、すべてのオブジェクトは宣言されると **null** です。 アプリケーション エクスプローラーでは、**クラス** ノードの各アプリケーション クラスはデータ型です。 これらの種類の変数をコード内で宣言することができます。 クラスのインスタンスを構築してインスタンスを変数に割り当てることができます。 

クラスはソース コードに入れ子にできます。 入れ子になったクラスはフォーム内 (**FormRun** を拡張するクラスなど) でのみ使用でき、コントロール、データ ソースまたはデータ フィールドを表すために使用します。 属性の修飾で接尾語に **属性** がある場合、属性の修飾などのクラスまたはメソッドで、属性名の接尾語を省略できます。 したがって、X++ は **\[MyFavoriteAttribute\]** を必要とするのではなく、**\[MyFavorite\]** を許可します。 また、属性はデリゲートとメソッドのハンドラーに現在適用され、ハンドラーをこれらのターゲットにマップします。 

AX 2012 およびそれ以前のバージョンでは、クライアントまたはサーバーのいずれかで実行するメソッドを指定することができました。 ただし、Finance and Operations のアプリケーションでは、コンパイルされたすべての X++ コードがサーバーの .NET 共通の中間言語 (CIL) として実行されます。 クライアント サイトまたはブラウザーで評価されるコードはなくなりました。 したがって、**client** キーワードと **server** キーワードは無視されるようになりました。 これらのキーワードが使用される場合コンパイル エラーは発生しませんが、新しいコードを使用することはできません。

### <a name="private-and-protected-member-variables"></a>プライベートおよび保護されたメンバー変数

以前は、クラスで定義されていたすべてのメンバー変数が保護されていました。 **private**、**protected**、および **public** キーワードを加えることにより、メンバー変数の表示を明示的にすることができるようになりました。 これらの修飾子の解釈は明白であり、メソッドのセマンティクスに沿っています。

-   **プライベート** – メンバー変数は、定義されているクラス内でのみ使用できます。
-   **保護されている** – メンバー変数は、それが定義されているクラスおよびクラスのすべてのサブクラスで使用できます。
-   **パブリック** – メンバー変数を任意の場所に使用することができます。 これは、定義されているクラス階層の範囲外に表示されます。

既定では、明示的なモディファイアーで実装されていないメンバー変数は引き続き保護されています。 ただし、ベスト プラクティスとしては、可視性を明示的に指定する必要があります。 先に説明したように、メンバー変数が **パブリック** として定義されている場合、メンバー変数は定義されているクラス外でアクセスできます。 この場合、変数をホストしているオブジェクトを指定する修飾子を指定する必要があります。 修飾子を指定するには、メソッド呼び出しの場合と同様にドット表記法を使用します。 

次の例では、**field1** に明示的な **this** 修飾子を使用することでアクセスします。 この場合、そのアプローチは消費者にクラスの内部作業を公開することになり、クラスの実装と消費者の間に強い依存関係が生じるため、メンバー変数をパブリックにすることをお勧めできない場合があります。 常に、実装ではなくコントラクトにのみ依存させる必要があります。

```xpp
public class AnotherClass3
{
    int field1;
    str field2;
    void new()
    {
        this.field1 = 1;   // Explicit object designated.
        field2 = "Banana";  // 'this' assumed, as usual.
    }
}
```

### <a name="static-constructors-and-static-fields"></a>静的コンストラクターおよび静的フィールド

*静的フィールド* は **静的** キーワードを使用して宣言されているフィールドです。 概念的には、クラスのインスタンスではなく静的フィールドに適用されます。 静的コンストラクターは、静的呼び出しまたはインスタンス呼び出しがクラスに対して行われる前に実行されることが保証されます。 静的コンストラクターの実行は、ユーザーのセッションに対して相対的です。 静的コンストラクターは明示的に呼び出さないでください。 代わりに、コンパイラはコンストラクターがクラスの他のメソッドの前に正確に 1 回呼び出されるようにするコードを生成します。 静的コンストラクターは、任意の静的データを初期化したり、一度だけ実行する必要のあるアクションを実行するために使用されます。 静的コンストラクターのパラメーターを指定することはできず、**静的** キーワードでマークされる必要があります。

```xpp
// An example of how a singleton (call instance in the example below)
// can be created using the static constructor.
public class Singleton
{
    private static Singleton instance;
    private void new()
    {
    }
    static void TypeNew()    // This is the static constructor.
    {
        instance = new Singleton();
    }

    public static Singleton Instance()
    {
        return Singleton::instance;
    }
}

// The singleton ensures that only one instance of the class
// will be called, which is consumed by the following. 
{
    // Your code here.
    Singleton i = Singleton::Instance();
}
```

### <a name="class-elements-in-application-explorer"></a>アプリケーション エクスプローラーのクラス要素

アプリケーション エクスプ ローラーのほとんどのクラス・ノードの下には、**classDeclaration** ノードと **new** ノードという 2 つの特殊ノードがあります。 **classDeclaration** は、常に X++ **クラス** キーワードになります。 追加のキーワードは、**拡張** のように、クラスを変更するために含めることができます。 このノードには、メンバー変数の宣言も含めることができます。 メンバー変数は、**classDeclaration** の値に初期化することはできません。また静的にすることはできません。 

次の例では、変数 **m\_priority** および **m\_rectangle** はクラスのメンバーです。

```xpp
// An example of a classDeclaration.
public class YourDerivedClass extends YourBaseClass
{
    int m_priority;
    Rectangle m_rectangle;
    void new(int _length, int _width)
    {
        this.m_rectangle = new Rectangle(_length, _width);
    }
}
```

**新しい** 演算子には、**新しい** 演算子を使用して、クラスのインスタンスを作成するときに実行されるロジックが含まれます。 **新規** メソッドのロジックは、オブジェクトを作成し、そのオブジェクトを **classDeclaration** で宣言された変数に割り当てることができます。 各クラスは、**新しい** 方法を 1 つだけ持つことが可能です。 ただし、**新しい** メソッドでは、多くの場合基本クラスの **新しい** メソッドを呼び出す必要があります。 基本クラスの<**新規** メソッドを呼び出すには、**super()** を呼び出します。 

次の例は、前の **classDeclaration** の例の **YourDerivedClass** クラスの **new** メソッドを示しています。 この **新しい** メソッドで、コードは **長方形** クラスのインスタンスを構築します。 インスタンスは、**m\_rectangle** 変数に割り当てられます。 **この** 例で使用されているキーワードは省略可能ですが、指定した場合は、IntelliSense を使用する方が便利な場合があります。

```xpp
// An example of the new method from the previous classDeclaration example.
void new(int _length, int _width)
{
    this.m_rectangle = new Rectangle(_length, _width);
}
```

### <a name="garbage-collection"></a>ガベージ コレクション

最終的に実行中では、ほとんどのオブジェクトがそれらを指す変数はなくなります。 システムはこれらのオブジェクトをスキャンし、それらをメモリから消去します。 その後、メモリ空間は他の用途に利用できるようになります。 **Object** クラスには、**finalize** というメソッドがあります。 ただし、**確定** メソッドはデストラクタではありません。 ランタイムは、オブジェクトがガベージとして収集された場合でも、**finalize** メソッドを呼び出すことはありません。

### <a name="system-classes"></a>システム クラス

アプリケーション エクスプローラーの **システムのドキュメント** &gt; **クラス** には、カーネル クラスまたはシステム クラスの一覧があります。 システム クラスは、X++ で記述されておらず、ソース コードを表示することはできません。 システム クラスを追加することはできません。 システム クラには通常、**new** メソッドがありますが、**classDeclaration** ノードはありません。 すべてのアプリケーション クラスは **オブジェクト** システム クラスを暗黙的に拡張します。 一部のシステム クラスは、類似した名前を持つアプリケーション クラスで拡張されます。 たとえば、**xClassFactory** が **ClassFactory** ごとに延期されます。 そのような場合、システム クラスは使用しないでください。 詳細については、[クラスおよびメソッド](xpp-classes-methods.md) で「システム クラスの代替アプリケーション クラス」を参照してください。

### <a name="extension-methods"></a>拡張メソッド

拡張メソッド機能を使用すると、メソッドを別の拡張クラスに記述することによって、拡張メソッドを対象クラスに追加できます。 次のルールが適用されます。

-   拡張クラスは静的でなければなりません。
-   拡張クラスの名前は、10 文字の接尾辞 **\_Extension** で終了する必要がありますが、接尾辞に先行する名前の部分には制限はありません。
-   拡張子クラス内のすべての拡張子メソッドは、**パブリック静的** として宣言する必要があります。
-   すべての拡張メソッドの最初のパラメーターは、拡張メソッドが拡張する型です。 ただし、拡張メソッドが呼び出されると、呼び出し元は最初のパラメーターに対して何も渡す必要がありません。 代わりに、システムが最初のパラメーターに必要なオブジェクトを自動的に渡します。
-   拡張メソッドのターゲットは、クラス、テーブル、ビュー、またはマップ アプリケーション オブジェクト タイプである必要があります。

拡張クラスはプライベートまたは保護された静的メソッドを含めることができます。 これらのメソッドは通常、実装の詳細に使用され、拡張として公開されません。 拡張メソッドの手法は、それを拡張するクラスのソースコードには影響しません。そのため、クラスへの追加はオーバーレイを必要なく行うことができます。 

ターゲット クラスへのアップグレードは、既存の拡張メソッドの影響を受けることはありません。 ただし、ターゲット クラスへのアップグレードで拡張メソッドとして同じ名前のメソッドが追加される場合、拡張メソッドはターゲット クラスのオブジェクトを通して到達できなくなります。 拡張メソッドの手法では、通常のインスタンス メソッドを呼び出すときによく使うドット区切り構文と同じものを使用します。 拡張メソッドは、ターゲット クラスのすべてのパブリック コンポーネントにアクセスできますが、保護されたまたはプライベートのオブジェクトには何もアクセスできません。 したがって、拡張メソッドは構文砂糖の一種と考えることができます。 目標タイプに関係なく、拡張機能クラスはタイプに拡張メソッドを追加するために使用されます。 たとえば、拡張テーブルは、メソッドをテーブルに追加するために使用されていませんし、拡張テーブルというものは存在しません。

```xpp
// An example of an extension class holding a few extension methods.
public static class AtlInventLocation_Extension
{
    public static InventLocation refillEnabled(
        InventLocation _warehouse,
        boolean _isRefillEnabled = true)
    {
        _warehouse.ReqRefill = _isRefillEnabled;
        return _warehouse;
    }

    public static InventLocation save(InventLocation _warehouse)
    {
        _warehouse.write();
        return _warehouse;
    }
}
```

## <a name="delegates-as-data-types"></a>データ型としてのデリゲート

*デリゲート* は、それをサブスクライブするメソッドを収集します。 デリゲートは、すべてのサブスクライバ メソッドが共有する必要があるパラメーター署名を指定します。 デリゲートが呼び出されると、デリゲートはその各サブスクライバを呼び出します。 デリゲートは値を返しませんし、**既定値を持つことはできません**。 最初に、すべてのデリゲートにはサブスクライブされたメソッドがありません。 デリゲートが宣言できるパラメーターの数に制限はなく、これらのパラメーターの種類に制限はありません。 デリゲートの唯一の目的は、サブスクライバが従わなければならない契約を定義することであるため、デリゲート本文は常に空です。 デリゲートは、クラスで定義をしなくてもかまいません。 デリゲートは、テーブル、フォーム、またはクエリで定義することもできます。

### <a name="delegate-examples"></a>デリゲートの例

```xpp
abstract class VarDatClass
{
    // delegatemethod examples
    // An example of declaring a delegate.
    delegate void notifyChange(utcdatetime _dateTime, str _changeDescription)
    {
    }

    // An example of subscribing an event handler to a delegate.
    public static void notifyStatic(utcDateTime _dateTime, str _changeDescription)
    {
        info("A notification has occurred calling static handler:" +
            DateTimeUtil::toStr(_dateTime) +
            " Message:" +
            _changeDescription);
    }
}
```

## <a name="tables-as-data-types"></a>データ型としてのテーブル

すべてのテーブルはクラス定義として扱うことができます。 テーブル変数は、テーブル (class) の定義のインスタンス (オブジェクト) と見なすことができます。 テーブル変数の各フィールドでは、既定値は **空** です。 フィールドに注意を向けてテーブル上でメソッドを作成することができます。 これらのメソッドは、テーブルのインスタンス上で呼び出すことができます。 テーブル内のレコードを操作 (つまり、読み取り、更新、挿入、削除) するには、レコードを保持しておくための少なくとも 1 つのテーブル変数を宣言する必要があります。 ベスト プラクティスは、変数の名前としてテーブルの名前を使用する必要がありますが、最初の小文字を使用します。 テーブルとオブジェクト間のいくつかの重要な違いを次に示します。

-   テーブル変数の容量を割り当てることはできません。 配賦は暗黙的に行われます。
-   テーブル変数のフィールドは、パブリックです。 任意の場所でそれを参照することができます。
-   テーブル変数のフィールドは、式を使用して参照できます。

自動変換はありませんが、**共通** として宣言されているテーブル変数は、どのテーブルからでもデータを保持できます。

### <a name="scope-of-table-variables"></a>テーブル変数の範囲

テーブル変数は、ほとんどの点で、オブジェクトと見なされますが、ただし、オブジェクトとは異なり、それらは明示的に割り当てられません。 変数の宣言のみ必要です。 すべてのテーブルには **共通** のテーブルと互換性があるように、すべてのオブジェクト にも **オブジェクト** クラスの互換性があります。 テーブル変数は、一般的なバッファーとして宣言され、任意のテーブルからデータを保持するために使用できます。 テーブル変数を持たないテーブルにはアクセスできません。 テーブルの変数およびオブジェクトの宣言の原則は、領域の割り当てに関する点を除いて同じです。

### <a name="table-examples"></a>テーブルの例

構文は、レコード内のフィールドを参照するさまざまな可能性を高めます。 たとえば、**TableName.(FieldId)** 構文を使用できます。 

次の例では、顧客テーブルの現在のレコードにあるフィールドの内容を出力します。

```xpp
// Declares and allocates space for one CustTable record.
public void myMethod()
{
    CustomerTable custTable;
}

// An example of referencing table variables.
public void printAccountNo()
{
    CustomerTable custTable;
    print custTable.AccountNo;  // Prints the field reference.
}
```

次の例では、**fieldCnt** および **fieldCnt2Id** メソッドを使用しています。 **fieldCnt** メソッドは、テーブル内のフィールドの数をカウントしますが、**fieldCnt2Id** はフィールド番号の ID を返します。 たとえば、**fieldCnt2Id** メソッドを使用して、テーブルでそのフィールド番号 6 が ID 54 を持っていることを確認します。 この変換は、表内のフィールドの ID が連続しているという保証がないため、この変換が必要です。

```xpp
// An example of the various possibilities for referencing fields in records.
public void printCust()
{
    int i, n, k;
    CustomerTable custTable;
    DictTable dictTable;
    dictTable = new DictTable(custTable.TableId);
    n = dictTable.fieldCnt();
    print "Number of fields in table: ", n;
    for(i=1; i<=n; i++)
    {
        k = dictTable.fieldCnt2Id(i);
        print "The ", dictTable.fieldName(k),
        " field with Id=",k, " contains '",
        custTable.(k), "'";
    }
}
```

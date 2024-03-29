---
title: クラスおよびメソッド
description: この記事では、X++ でクラスを作成および使用する方法について説明します。
author: josaw1
ms.date: 08/27/2021
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06672b0bc69552a6a7b44807ad1b6dab5d29278b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271411"
---
# <a name="classes-and-methods"></a>クラスおよびメソッド

[!include [banner](../includes/banner.md)]

この記事では、X++ でクラスを作成および使用する方法について説明します。

*クラス* は、そのクラスから後に構築されるインスタンスのデータおよびメソッドを定義するソフトウェア構造です。 *クラス* は、問題のあるドメイン内の *オブジェクト* を抽象化したものです。 この *クラス* から構築されるインスタンスは、*インスタンス* または *オブジェクト* として知られます。 この記事では、*インスタンス* という用語を使用します。 データはオブジェクトの状態を表し、メソッドはオブジェクトの動作を表します。

*変数* にはクラスのデータが含まれており、*フィールド* と呼ばれます。 クラス宣言から構築されたすべてのインスタンスには、独自の変数のコピーがあります。 これらの変数は *インスタンス変数* または *インスタンス フィールド* と呼ばれます。 この記事では、ほとんどの場合、*フィールド* という用語を使用します。

メソッドはクラスの動作を定義します。 データに作用する一連のステートメントです (インスタンス フィールド)。 既定では、メソッドはクラスのインスタンス フィールドを操作するように宣言されます。 これらのメソッドは、*instance メソッド* または *object メソッド* と呼ばれます。

*インスタンス フィールド* にアクセスできない *静的メソッド* および *静的フィールド* を宣言できます。 これらはすべて[X++ 静的クラス](xpp-static-classes.md)に記述されています。

## <a name="declare-a-class"></a>クラスを宣言します

プロジェクトにクラスを追加するには、Visual Studio で **新しい項目の追加** ダイアログを使用する必要があります。

1. サーバー エクスプローラーで、プロジェクトを右クリックしてから **追加** をクリックします。
2. **新しい項目** のダイアログ ボックスの左側のナビゲーションで、**インストール済み > Dynamics 365 品目 > Code** の順に選択します。 その後、**クラス** を選択し、クラス名を入力します。
3. **追加** をクリックします。

すべてのクラスはパブリックです。 **パブリック** モディファイアーを削除すると、システムではクラスはパブリック クラスとして扱われます。 クラス宣言では、**final** および **extends** などの、他の修飾子を指定することができます。

## <a name="fields"></a>フィールド

インスタンス フィールドは既定で **保護** されています。 これは、同じクラスまたは [派生クラス](xpp-inheritance.md) の中でしかアクセスできないことを意味します。 **private**、**protected**、または **public** キーワードを使用して、インスタンス フィールド宣言を変更できます。

> [!NOTE]
> メンバー フィールドを公開することは、クラスの内部動作をそのコンシューマーに公開し、クラスの実装とそのコンシューマー間に強い依存関係を作成するため、あまり推奨されていません。 常に、実装ではなくコントラクトにのみ依存させる必要があります。

フィールド自体の宣言などと共に、フィールド インラインに値を割り当てることができます。 これは、静的フィールドとインスタンス フィールドの両方に適用されます。

次の例は、アクセサー メソッドを使用してフィールド データを公開する方法を示しています。 フィールド **firstName** は保護されているため、保護されたフィールドへのアクセスを可能にするために、アクセサー (取得および設定) メソッドが実装されます。 フィールド **lastName** は公開されているため、コードはフィールドの値を直接取得および設定できます。

```xpp
// This is the class definition.
public class HasAFirstName
{
    str firstName = "";
    public str lastName = "";
    public str getFirstName()
    {
        return firstName;
    }

    public void setFirstName(str newName)
    {
       firstName = newName;
    }
}

// This code creates an instance of the class and gets the fields.
public static void TestLastName()
{
    HasAFirstName hasFirstName = new HasAFirstName();
    hasFirstName.setFirstName("Dion");
    info(hasFirstName.getFirstName());
    hasFirstName.lastName = ("Townes");
    info(hasFirstName.lastName);
}
// The output is "Dion" and "Townes".
```

### <a name="field-attributes"></a>フィールド属性

属性がクラスおよびメソッドを修飾できるのと同じ方法で、フィールドを属性で修飾できます。 次の例では、**MyField** フィールドを **MyAtribute** 属性で修飾します。

```xpp
class MyClass
{
    [MyAttribute]
    public int myField;
}
```

特に有用な属性の 1 つは、**SysObsolete** 属性です。 **SysObsolete** 属性がフィールドに適用されると、コンパイラはそのフィールドへの任意の参照に対してエラーまたは警告を生成します。 警告かエラーかは、属性の 2 番目のパラメーターによって異なります。

```xpp
class MyClass
{
    [SysObsolete("This field is obsolete.", true)]
    public int myField;
}
```

## <a name="constructors"></a>コンストラクター

クラスのインスタンスを作成するには、*コンストラクタ* を使用してクラスのインスタンスを生成する必要があります。

+ クラスでは、**新しい** メソッド (コンストラクター) を 1 つだけ定義できます。
+ コンストラクターを定義しない場合は、パラメーターのない既定のコンストラクターが、コンパイラによって自動的に作成されます。
+ 既定のコンストラクターは、**新しい** メソッドでパラメーターに既定値を割り当てることによってシミュレーションできます。

次の例では、**Point** クラスのパラメーター コンストラクターを定義します。

```xpp
class Point
{

    // Instance fields that are public. In practice, you would probably make this protected or private.
    // and create accessor methods.
    public real x = 0.0;
    public real y = 0.0;

    void new() {
    }
}
```

次に、クリーンな継承モデルを作成し、コードがアップグレードされたときの問題を最小限に抑える方法について説明します。

+ 抽象クラスでない場合、各クラスは単一のパブリック構築メソッドを持つ必要があります。 初期化が不要な場合は、静的コンストラクトのメソッドを使用します。 それ以外の場合は、静的な **新しい** メソッドを使用します (クラスの既定のコンストラクターは保護する必要があります)。
+ 各クラスには、少なくとも 1 つの静的 **コンストラクト** メソッドが必要です。
+ 各クラスは少なくとも 1 つの **新しい** 静的メソッドを持つ必要があります。
+ 各クラスに **新しい** メソッド (既定のコンストラクター) が必要です。 このメソッドは **保護** する必要があります。
+ クラス フィールドを取得および設定するアクセサー メソッドを作成します。
+ インスタンス化の後に実行する必要のある特殊な初期化タスクを実行するための **init** メソッドを作成します。

### <a name="create-other-objects-in-a-constructor"></a>コンストラクターでその他のオブジェクトを作成する

クラス コンストラクターは、クラスのインスタンスを作成するだけでなく、他のオブジェクトをインスタンス化することもできます。 たとえば、次のコードは、境界を定義するため 2 つの **ポイント** オブジェクトを使用する **長方形** クラスを申告します。 この場合、**ポイント** クラスには 2 つの **実数** パラメーターを持つコンストラクターが存在します。

```xpp

class Point
{
    // Instance fields that are public. In practice, you would probably make this protected or private.
    // and create accessor methods.
    public real x = 0.0;
    public real y = 0.0;

    // Constructor to initialize to a specific or default value
    void new(real _x = 10, real _y = 10)
    {
        x = _x;
        y = _y;
    }
}

class Rectangle
{
    public Point lowerLeft;
    public Point upperRight;

    void new(real _topLeftX = 0.0, real _topLeftY = 0.0, real _bottomRightX = 1.0, real _bottomRightY = 1.0)
    {
        lowerLeft  = new Point(_topLeftX, _topLeftY);
        upperRight = new Point(_bottomRightX, _bottomRightY);
    }

}

// This code creates two instances of the Rectangle class.
Rectangle defaultRectangle = new Rectangle();
info(any2Str(defaultRectangle.lowerLeft.x));
info(any2Str(defaultRectangle.lowerLeft.y));
// Output is "0.0" and "0.0".

Rectangle customRectangle = new Rectangle(1.0, 1.0, 2.0, 2.0);
info(any2Str(customRectangle.lowerLeft.x));
info(any2Str(customRectangle.lowerLeft.y));
// Output is "1.0" and "1.0".
```

## <a name="create-an-instance-of-an-object"></a>オブジェクトのインスタンスを作成する

コンストラクター、**新規** は、クラスの新しいインスタンスを返します。 次のコード例は、ポイント クラスのインスタンスを 2 つ作成する方法を示しています。

```xpp
// Declare a field to refer to a Point instance.
Point myPoint;

// Create an instance of the Point class.
myPoint = new Point();

// Declare and instantiate a Point instance.
Point ap = new Point();
```

## <a name="destructors"></a>デストラクター

*デストラクター* は、クラス インスタンスを明示的に破棄するために使用されます。 インスタンスは、インスタンスに関する参照がない場合は自動的に破棄されます。 ただし、たとえば、次の方法で対象を明示的に破棄できます。

+ **finalize** メソッドを使用します。
+ 参照変数を **Null** に設定します。

### <a name="use-the-finalize-method"></a>ファイナライズ メソッドを使用する

オブジェクトを明示的に破棄するには **finalize** メソッドを使用します。 **finalize** メソッドへの暗黙的な呼び出しはありません。 そこでステートメントを実行するメソッドを呼び出す必要があります。 **finalize** メソッドでは、必要なクリーンアップ コードも配置する必要があります。 たとえば、クラスがダイナミックリンク ライブラリ (DLL) モジュールを使用する場合、必要ではなくなったときに DLL をリリースする **確定** メソッドを使用できます。 **finalize** メソッドは慎重に使用してください。 オブジェクトへの参照がある場合オブジェクトを破棄します。

次の例は、**finalize** メソッドの呼び出しの基本構造を示しています。

```xpp
// From any method in a class.
if (condition)
{
    // Removes object from memory.
    this.finalize();
}
```

### <a name="set-reference-variable-to-null"></a>参照変数を Null に設定する

参照変数を **Null** に設定してオブジェクトを終了します。 この方法を使用すると、他の変数がそのオブジェクトをポイントしていない場合にのみオブジェクトが破棄されます。 他のコードが変数を使用していないことを確認する必要があります。 次の例では、参照変数を作成し、**null** に設定します。

```xpp
Point myPoint = new Point();
myPoint = null;
```

## <a name="methods"></a>メソッド

### <a name="instance-methods"></a>インスタンス メソッド

インスタンス メソッドは、クラスから作成される各インスタンスに埋め込まれます。 メソッドの使用前に、オブジェクトのインスタンスを作成する必要があります。 次のコードは、インスタンス メソッドを定義して、それをインスタンスから呼び出す方法を示しています。

```xpp
class Square
{

    int side = 0;

    void new(int _side = 1) {
        side = _side;
    }

    int getArea() {
        return side * side;
    }

}

// This code creates an instance of Square and calls getArea.
Square square = new Square(15);
int area = square.getArea();
info(int2Str(area));
// Output is "225".
```

### <a name="static-methods"></a>静的メソッド

*クラス メソッド* とも呼ばれる静的メソッドは、クラスに属しており、キーワード **static** を使用して作成されます。 静的メソッドを使用する前に、オブジェクトのインスタンスを作成する必要はありません。 静的メソッドは多くの場合、テーブルに格納されているデータを操作するために使用します。 メンバー フィールドは静的メソッドからはアクセスできません。

静的メソッドを呼び出すには、次の構文を使用します。

```xpp
ClassName::methodName();
```

インスタンス メソッドを静的メソッドに変換する場合は、クライアントを再起動する必要があります。 それ以外の場合、コンパイラは変更を検出しません。 インスタンス メソッドを静的メソッドに変換した後は、クラスのインスタンスからメソッドを呼び出すことができなくなります。 代わりに、クラス自体からメソッドを呼び出す必要があります。 静的メソッドの詳細については、[X++ 静的クラス](xpp-static-classes.md)を参照してください。

### <a name="main-methods"></a>主要メソッド

**メイン** メソッドは、メニュー オプションから直接実行されるクラス メソッドです。 このメソッドでは、オブジェクトのインスタンスを作成してから、必要なメンバー メソッドを呼び出す必要があります。 **\_args** パラメーターを使用して、メソッドにデータを転送できます。

```xpp
static void main (Args _args)
{
    // Your code here.
}
```

### <a name="declaration-of-methods"></a>メソッドの宣言

メソッドの宣言は、ヘッダーと本文で構成されます。 メソッド ヘッダーは、メソッドの名前と戻り値の型、メソッド モディファイア、およびパラメーターを宣言します。 (戻り値の型が **無効** である可能性があります。) メソッド本体は、フィールド宣言、メソッド宣言、および明細書で構成されます。

### <a name="return-type"></a>戻り値の型

各メソッドには、戻り値の型が必要です。 メソッドが何も返さない場合、**無効** キーワードを戻り値の型として使用します。

次の例は、2 つのメソッドを示しています。 1 つの方法に戻り値の型がありますが、他の方法には戻り値の型がありません。

```xpp
void methodNameNoReturnValue()
{
    // Your code here.
}

// If a method returns something, you must specify the return type and include a return statement.
int methodNameIntegerReturnValue()
{
    return 1;
}
```

### <a name="syntax"></a>構文

メソッド宣言 = *見出し*  *本文* 見出し = **\[** *モディファイアー* **\]**  *戻り値の型*  *MethodName*  **(**  *パラメーター リスト*  **)**

モディファイアー = **\[クライアント\] \[サーバー\] \[編集 | 表示 | パブリック | 保護 |プライベート\] \[静的 | 抽象 | 最終\]**

ReturnType = *データ型*  **| void | anytype**

MethodName = *識別子*

パラメーター リスト = **\[** *パラメーター*  **{、**  *パラメーター*  **}\]**

パラメーター = *データ型* *変数識別子* **\[ =**  *式*  **\]**

本文 = **{ \[**  *変数宣言*  **\] \[**  *埋め込み関数用の宣言*  **\] \[**  *明細書*  **\] }**

埋め込み関数用の宣言 = *見出し*  **{\[**  *変数宣言*  **\] \[**  *明細書*  **\]}**

**Anytype** 戻り値の型を使用すると、メソッドは任意のデータ型を返すことができます。

### <a name="example-of-a-method-that-doesnt-have-a-return-type"></a>戻り値の型を設定していないメソッドの例

```xpp
void update ()
{
    // Field declared and initialized
    CustTable this_Orig = this.orig();

    // First statement in body (begin transaction)
    ttsBegin;
    this.setNameAlias();
    // Calls super's implementation of update
    super();
    this.setAccountOnVend(this_Orig);
    if (this_Orig.custGroup != this.custGroup)
        ForecastSales::setCustGroupId(
            this.accountNum,
            this_Orig.custGroup,
            this.custGroup);
    // Commits transaction
    ttsCommit;
}
```

### <a name="example-of-a-method-that-has-parameters"></a>パラメーターを持つメソッドの例

次の例では、**checkAccountBlocked** メソッドはブール値を返し、**amountCur** パラメーターで動作します。

```xpp
boolean checkAccountBlocked(AmountCur amountCur)
{
    if (this.blocked == CustVendorBlocked::All
        ||(this.blocked == CustVendorBlocked::Invoice
        && amountCur > 0 ))
    return checkFailed(strFmt("@SYS7987",this.accountNum));
    return true;
}
```

## <a name="method-modifiers"></a>メソッド modifiers

いくつかのモディファイアーは、メソッドの宣言に適用することができます。 一部の修飾子を結合できます (たとえば、**final static**)。 メソッド モディファイア キーワードを次に示します。

+ **抽象**: メソッドは宣言されていますが、親クラスで実装されていません。 このメソッドはサブクラスで上書きする必要があります。 サブクラスに親クラスに属する 1 つ以上の抽象メソッドがあり、オーバーライドされていません。そのサブクラスからオブジェクトを作成しようとすると、コンパイラ エラーが発生します。

    クラスは抽象クラスにすることもできます。 場合によっては、抽象的な概念を表す場合でもクラスをインスタンス化しないでください。 サブクラスのみインスタンスを作成する必要があります。 このタイプの基本クラスは **抽象** として宣言できます。 たとえば、勘定の概念をモデル化します。 実際の世界には派生クラス (勘定科目など) しか存在しないため、勘定は抽象です。 この例では、**勘定** クラスを **抽象** として宣言する必要があるという明確なケースについて説明します。
+ **ディスプレイ**: メソッドの戻り値は、ページまたはレポートに表示される必要があります。 ページまたはレポートで値を変更することはできません。 通常、戻り値は合計などの計算された値です。
+ **編集**: メソッドの戻り値のタイプは、ページで使用されるフィールドの情報を提供するために使用する必要があります。 このフィールドの値は修正できます。
+ **最終**: 同じクラスから派生したクラスのメソッドに上書きすることはできません。
+ **パブリック**: **パブリック** として宣言されるメソッドは、クラスがアクセスできるどの場所にもアクセスでき、サブクラスによって上書きすることができます。 アクセス修飾子を持たないメソッドは暗黙的にパブリックとなります。
+ **保護**: **保護** として宣言されるメソッドは、クラス、およびメソッドが宣言されているクラスを拡張するサブクラスのメソッドからのみ呼び出すことができます。
+ **プライベート**:  **プライベート** として宣言されるメソッドは、プライベートメソッドが宣言されているクラスのメソッドからのみ呼び出すことができます。
+ **静的**: このメソッドはクラス メソッドであり、インスタンスを実行しません。 静的メソッドは、インスタンス フィールドを参照できません。 クラスのインスタンスでは呼び出されません。 代わりに、クラス名を使用して呼び出されます (たとえば、**MyClass::aStaticProcedure()**)。

### <a name="methods-that-have-modifiers"></a>モディファイアーのあるメソッド

次の例は、メソッドの見出しのみを示しています。

```xpp
// A method that cannot be overridden
final int dontAlterMe()

// A static method
static void noChange()

// A display method that returns an integer
display int value()
```

## <a name="method-access-control"></a>メソッド アクセス制御

その他のクラスのメソッドがお客様のクラスのメソッドを呼び出すことができるかどうかを制御するには、アクセサー キーワード **public**、**protected**、および **private** を使用します。 メソッドのアクセス キーワードは、クラス継承のルールとも連携します。 メソッドを使用するアクセサー キーワードを次に示します。

+ **パブリック** – **パブリック** として宣言されるメソッドは、クラスがアクセスできるどの場所からでも呼び出すことができます。 さらに、メソッドが **最終** として宣言されていない限り、パブリック メソッドをサブクラスでオーバーライドできます。
+ **保護**: **保護** として宣言されるメソッドは、次のメソッドからのみ呼び出すことができます。
    + クラスのメソッド。
    + 保護されたメソッドを含むクラスのサブクラス内のメソッド。 保護されているメソッドは、サブクラスで上書きできます。
+ **プライベート**:  **プライベート** として宣言されるメソッドは、プライベートメソッドが宣言されているクラスのメソッドからのみ呼び出すことができます。 サブクラスでプライベート メソッドをオーバーライドできません。 既定では、新しいメソッドを作成するときに、**プライベート** アクセサー キーワードがコード エディターに表示されます。 最大限のセキュリティについては、**プライベート** が最も保守的な既定のアクセス キーワードです。

### <a name="static-and-instance-methods"></a>静的およびインスタンス メソッド

メソッドのアクセサー キーワードは、どのメソッドが静的であるか、静的でないかに関係なく、同じクラスにある 2 つのメソッド間の呼び出しを制限することはありません。 静的メソッドでは、**新しい** コンストラクター メソッドが **プライベート** モディファイアーで修飾されている場合でも、**新しい** コンストラクター メソッドに対する呼び出しは有効です。 これらの呼び出しの構文では、**新しい** キーワードを使用する必要があります。 静的メソッドのコードは、クラスのインスタンス メソッドを呼び出す前に、独自のクラスのインスタンス オブジェクトを構築する必要があります。

### <a name="increasing-access-during-overrides"></a>オーバーライド中のアクセス増加

サブクラス内でメソッドがオーバーライドされると、オーバーライドするメソッドは少なくともオーバーライドされるメソッドと同程度のアクセスが可能なことが必要です。 たとえば、次のコンパイラ ルールは、サブクラスで保護されたメソッドが上書きされる時に適用されます。

+ スーパークラスのパブリック メソッドは、サブクラスのパブリック メソッドによってのみ上書きできます。
+ サブクラスでは、パブリック メソッドまたは保護対象のメソッドはスーパークラスの保護対象のメソッドをオーバーライドできません。
+ サブクラスでは、プライベート メソッドはスーパークラスの保護対象のメソッドをオーバーライドできません。

## <a name="optional-parameters"></a>オプションのパラメーター

パラメーターは、メソッド宣言で初期化することができます。 この場合、パラメーターは *オプションのパラメーター* となります。 メソッドの呼び出しの値が指定されていない場合は、既定値が使用されます。 すべての必須パラメータは最初のオプション パラメーターの前に一覧表示する必要があります。 次の例では、オプションのパラメーターを持つメソッドを作成して呼び出す方法を示しています。 **AddThreeInts** メソッドの例は、メソッドを呼び出すときにデフォルトのパラメーターをスキップできないことを示しています。

### <a name="examples-of-optional-parameters"></a>オプション パラメーターの例

既定のパラメータを持つクラスのコード例を次に示します。

```xpp
// This is an example of a function being used as the default.
class Person
{
    date birthDate;

    // The constructor that takes a date type as a parameter.
    // That value is assigned to the field member birthDate.
    void new(date _date)
    {
        birthDate = _date;
    }

    // The CalculateAgeAsOfDate method references the birthDate field and has an
    // optional parameter. In this example, the default value is the
    // return value of a function.
    public real CalculateAgeAsOfDate(date _calcToDate = DateTimeUtil::getToday(DateTimeUtil::getUserPreferredTimeZone()) )
    {
        return (_calcToDate - birthDate) / 365;
    }

    public static void callPerson()
    {

        Person person = new Person(13\5\2010);

        // Optional parameter's default is used.
        Info(strFmt('Age in years today is %1 years',
                real2int(person.CalculateAgeAsOfDate())));

        // January 2, 2044  is the parameter value for _date.
        Info(strFmt('Age in years on %1 is %2 years',
                2\1\2044,
                real2int(person.CalculateAgeAsOfDate(2\1\2044))));
    }

}
```

次の例では、2 番目の省略可能なパラメーターにスキップできないことを示します。 **AddThreeInts** メソッドには 2 つの任意のパラメータがあります。 **callAdditions** メソッドは、**AddThreeInts** メソッドを呼び出します。 コメント化されたコードは、**\_i3** の既定値のみのオーバーライドを試行しますが、コンパイラでは、呼び出し時に先行するすべての任意のパラメータのオーバーライドを要求します。

```xpp
class Additions
{
    public static int AddThreeInts(int _i1, int _i2 = 2,int _i3 = 3)
    {
        return _i1 + _i2 + _i3;
    }

    public static void callAdditions()
    {
        // The next statement does not compile, because it skips the _i2 parameter.
        // info(int2Str(Additions::AddThreeInts(1, , 99)));

        // You must specify both optional parameters.
        info(int2Str(Additions::AddThreeInts(1, 2, 99)));
    }

}
```

## <a name="accessor-methods"></a>アクセサー メソッド

クラス フィールドは既定で保護されています。 クラスの内部実装の詳細を非表示にすることで、そのクラスを使用するコードを破棄することなくクラスの実装を後で変更することができます。 参照フィールドからデータにアクセスするには、アクセサー メソッドを作成する必要があります。 次の例では、アクセス メソッドを使用してフィールド **x** および **y** にアクセスする **Point** クラスを定義します。

```xpp
class Point
{
    // Instance fields
    real x;
    real y;

    // Constructor to initialize to a specific or default value
    void new(real _x = 10, real _y = 10)
    {
        x = _x;
        y = _y;
    }

    // Accessor methods
    void setX(real _x)
    {
        x = _x;
    }

    void setY(real _y)
    {
        y = _y;
    }

    real getX()
    {
        return x;
    }

    real getY()
    {
        return y;
    }
}
```

これらのメソッド宣言は、**Point** クラスが外部からのフィールドへのアクセスを提供する方法を示しています。 その他のオブジェクトは、アクセサー メソッドを使ってインスタンス フィールド **Point** オブジェクトを操作できます。

```xpp
Point myPoint = new Point();
// Set the x fields using the accessor method.
myPoint.setX(4.0);
// Get the x fields using the accessor method.
info(any2Str(myPoint.getX()));
```

## <a name="parameters"></a>パラメーター

すべてのメソッドは独自の *スコープ* を持っています。 メソッドは、1 つ以上のパラメーターを受け取ることができます。 メソッドのスコープ内では、これらのパラメーターはローカル変数として処理され、メソッド呼び出しのパラメーターからの値で初期化されます。 すべてのパラメーターは値で渡されるため、元の変数の値を変更することはできません。 メソッド内のローカル変数のみを変更することができます。 このローカル変数は元の変数のコピーです。

## <a name="scope-of-variables-in-methods"></a>メソッドでの変数の範囲

スコープは、品目にアクセスできるエリアを定義します。 クラスで定義されている変数は、そのクラス内のメソッドで使用できます。 メソッド内の変数は、現在のブロック内でのみアクセスできます。

## <a name="local-functions"></a>ローカル関数

メソッド内部のローカル関数を宣言することができます。 これは、ローカル関数と呼ばれます。 可能ではあるものの、ベスト プラクティスではありません。 代わりに、プライベート メソッドをクラスに追加する必要があります。

+ ローカル関数の宣言は、メソッド内の宣言されていないステートメントの前に物理的に先行する必要があります。
+ メソッド内で 1 つ以上のローカル関数を宣言することができます。 ただし、ローカル関数はすべて、中断のないシリーズで宣言する必要があります。
+ ローカル関数内にあるコードは、ローカル関数を含むメソッドで宣言されている変数にアクセスできます。
+ ローカル関数の外にあるコードは、ローカル関数で宣言された変数にアクセスすることはできません。
+ ローカル関数は、ローカル関数が宣言されているのと同じメソッド内のコードによってのみ呼び出すことができます。
+ ローカル関数が、それ自体を呼び出すことはありません。 このような再帰は、正常に行われるコンパイルを防ぐことができます。

次の例は、2 つのローカル関数である **localFunctionA** および **localFunctionB** の有効な宣言を示しています。 ローカル関数への呼び出しは、必要に応じて、この例の関数宣言の後に行われます。

```xpp
static void StaticFunction()
{
    int number = 654;

    void localFunctionA(int _iNum)  // The local function.
    {
        str innerString = "String in localFunctionA";
        str output = strFmt("localFunctionA: %1 , %2 , %3", _iNum, innerString, number);
        info(output);
    }

    void localFunctionB()
    {
        info("Printing from inside localFunctionB.");
    }

    localFunctionA(55);
    localFunctionB();
    // Next info statement would fail to compile,
    // because innerString is restricted to the
    // scope of the local function in which it is declared.
    // print innerString;
}

// When called, the output is:
// localFunctionA: 55 , String in localFunctionA , 654
// Printing from inside localFunctionB.
```

## <a name="extension-methods"></a>拡張メソッド

拡張メソッド機能を使用すると、メソッドを別の拡張クラスに記述することによって、拡張メソッドを対象クラスに追加できます。 次のルールが適用されます。

- 拡張クラスは静的でなければなりません。
- 拡張クラスの名前は、10 文字の接尾語 \_Extension で終了する必要があります。 ただし、接尾辞に先行する名前の部分には制限はありません。
- 拡張子クラス内のすべての拡張子メソッドは、パブリック静的として宣言する必要があります。
- すべての拡張メソッドの最初のパラメーターは、拡張メソッドが拡張する型です。 ただし、拡張メソッドが呼び出されると、呼び出し元は最初のパラメーターに対して何も渡す必要がありません。 代わりに、システムが最初のパラメーターに必要なオブジェクトを自動的に渡します。

拡張クラスにプライベートまたは保護された静的メソッドを含めることは完全に有効です。 これらは通常、実装の詳細に使用され、拡張として公開されません。 次の例は、いくつかの拡張メソッドを保持している拡張機能クラスを示しています。

```xpp
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

### <a name="reasons-to-use-extension-methods"></a>拡張メソッドを使用する理由

拡張メソッドの手法は、拡張するクラスのソース コードには影響しません。 したがって、クラスへの追加はオーバーレイなしで行うことができます。 ターゲット クラスへのアップグレードは、既存の拡張メソッドの影響を受けることはありません。 ただし、ターゲット クラスへのアップグレードで拡張メソッドとして同じ名前のメソッドが追加される場合、拡張メソッドはターゲット クラスのオブジェクトを通して到達できなくなります。 拡張メソッドは使いやすいです。 拡張メソッドの手法では、通常のインスタンス メソッドを呼び出すときによく使うドット区切り構文と同じものを使用します。 拡張メソッドは、ターゲット クラスのすべてのパブリック コンポーネントにアクセスできますが、保護されたまたはプライベートのオブジェクトにはアクセスできません。 この方法では、拡張メソッドは糖衣構文の種類とみなすことができます。

### <a name="where-can-extension-methods-be-applied"></a>拡張メソッドはどこに適用できるか

拡張メソッドのターゲットは、次のアプリケーション オブジェクト タイプのいずれかである必要があります。

- クラス
- テーブル
- 表示
- マップ

目標タイプに関係なく、拡張機能 *クラス* はタイプに拡張メソッドを追加するために使用されます。 たとえば、拡張テーブルは、メソッドをテーブルに追加するために使用されて *いません* し、拡張テーブルというものは存在しません。

## <a name="the-this-keyword"></a>このキーワード

**this** キーワードは、**this** キーワードが使用されるクラスやテーブルのインスタンスへの参照です。 **this** 参照が必須になることはありませんが、コードを明確にし、コード エディターで IntelliSense の動作を強化することができます。 すべての呼び出しインスタンス メソッドは **これ** を参照または変数のいずれかにより修飾される必要があります。 **this** 参照は、次の情報を修飾するために使用できます。

+ **this** 参照が使用されている同じクラス内の他のインスタンス (静的でない) メソッドの名前。 次の例を示します: `boolColorChanged = this.colorItOrange();`
+ **this** オブジェクトによって継承されるメソッドの名前。
+ **this** キーワードが使用されるメソッドを含むテーブル上のフィールドの名前。

**this** 参照は、次の方法で使用できません。

+ **classDeclaration** コードで宣言されているメンバー変数の名前を限定することはできません。
+ 静的メソッドで使用できません。
+ クラスやテーブルの静的メソッドの名前を限定することはできません。

## <a name="nested-classes"></a>入れ子になったクラス

クラスは X++ ソース コードに入れ子にできます。 入れ子になったクラスはフォーム内 (FormRun を拡張するクラスなど) でのみ使用でき、コントロール、データ ソースまたはデータ フィールドを表します。

## <a name="jobs"></a>職務

プレビュー バージョン (AX2102 以前) からの X++ ジョブの概念はありません。 X++ メソッドをすばやく簡単に実行するには、`static Main` メソッドをクラスに追加し、そのクラスを Microsoft Visual Studio のプロジェクトのスタートアップ オブジェクト フォームとして設定します。 プロジェクトが実行されるときは、`Main`メソッドが実行されます。

## <a name="call-stack-limitation"></a>呼び出しスタック制限

コール スタックの深さは 100 に制限されています。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

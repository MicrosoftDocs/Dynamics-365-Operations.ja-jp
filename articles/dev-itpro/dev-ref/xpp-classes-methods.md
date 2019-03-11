---
title: X++ クラスおよびメソッド
description: このトピックでは、X++ でクラスやインターフェイスを作成および使用する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 150303
ms.assetid: 1b2d76d1-52d9-46b2-937f-5a3b62f2d516
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ee078c78dabcc5a0e0e36e9495b8bc9891bbc40
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368634"
---
# <a name="x-classes-and-methods"></a>X++ クラスおよびメソッド

[!include [banner](../includes/banner.md)]

このトピックでは、X++ でクラスやインターフェイスを作成および使用する方法について説明します。

<a name="classes-in-x"></a>X++ のクラス
--------------

*クラス*は、そのクラスから後に構築されるオブジェクトのデータとメソッドを定義するソフトウェア構造です。 構築されるオブジェクトは、*インスタンス* または *オブジェクト* と呼ばれます。 (このトピックでは、2 つの用語を同じ意味で使用しています。) データはオブジェクトの状態を表し、メソッドはオブジェクトの動作を表します。 *変数*にはクラスのデータが含まれます。 クラス内の変数は、そのクラスから構成されるオブジェクトに固有です。 クラス宣言から構築されたすべてのオブジェクトには、独自の変数のコピーがあります。 これらの変数は*インスタンス変数*と呼ばれます。 メソッドはクラスの動作を定義します。 データに作用する一連のステートメントです。 通常、メソッドはクラスのインスタンス変数を操作するように宣言されます。 これらのメソッドは、*instance メソッド*または *object メソッド*と呼ばれます。 また、*静的メソッド* および *静的フィールド* を宣言することができます。

## <a name="declaration-of-classes"></a>クラスの宣言
### <a name="create-a-class-in-visual-studio"></a>Visual Studio でのクラスの作成

Microsoft Visual Studio でクラスを作成するには、次の手順に従います。

1.  サーバー エクスプローラーで、プロジェクトを右クリックしてから**追加**をクリックします。
2.  **新しい項目**ダイアログ ボックスで、**クラス**を選択してからクラスの名前を入力します。
3.  **追加** をクリックします。

すべてのクラスはパブリックです。 **パブリック** モディファイアーを削除すると、システムではクラスはパブリック クラスとして扱われます。 クラス宣言では、**final** および **extends** などの、他の修飾子を指定することができます。

### <a name="creating-variables-in-a-class"></a>クラスで変数を作成しています

すべてのクラスはパブリックですが、すべてのメンバー変数は暗黙的に保護されています。 ただし、private、protected または public キーワードを使用してメンバー変数宣言を変更することができます。 すべてのメンバー変数はクラスのオブジェクト インスタンスにのみ属しています。 次の例は、アクセサー メソッドを使用して変数データを公開する方法を示しています。

    public class HasAFirstName
    {
        str firstName;
        public str getFirstName()
        {
            return firstName;
        }

        public void setFirstName(str newName)
        {
           firstName = newName;
        }
    }

## <a name="constructors"></a>コンストラクター
クラスのインスタンスを作成するには、*コンストラクタ*を使用してクラスのインスタンスを生成する必要があります。 既定のコンストラクターは、**新規** メソッドです。

    // Declare a variable to refer to a Point object
    Point myPoint; 

    // Create an instance of a Point object
    myPoint = new Point(); 

ベスト プラクティスとして、**新しい**メソッドを保護する必要があります。 代わりに、初期化が必要ない場合、**静的コンストラクト** メソッドをクラスのパブリック コンストラクターとして使用する必要があります。 それ以外の場合、**新しい静的**なメソッドを使う必要があります。

### <a name="creating-other-objects-in-a-constructor"></a>コンストラクターでその他のオブジェクトを作成しています

クラス コンストラクターは、クラスのインスタンスを作成するだけでなく、他のオブジェクトをインスタンス化することもできます。 たとえば、次のコードは、境界を定義するため 2 つの**ポイント**オブジェクトを使用する**長方形**クラスを申告します。

    class Rectangle1
    {
        Point lowerLeft;
        Point upperRight;

        void new(real _topLeftX, real _topLeftY, real _bottomRightX, real _bottomRightY)
        {
            lowerLeft  = new Point(_topLeftX, _topLeftY);
            upperRight = new Point(_bottomRightX, _bottomRightY);
        }
    }

## <a name="destructors"></a>デストラクター
*デストラクター*は、クラス オブジェクトを明示的に破棄するために使用されます。 オブジェクトはへの参照がない場合、自動的に破棄されます。 ただし、たとえば、次の方法で対象を明示的に破棄できます。

-   **finalize** メソッドを使用します。
-   オブジェクト ハンドルを **null** に設定します。

### <a name="using-the-finalize-method"></a>finalize メソッドの使用

オブジェクトを明示的に破棄するには **finalize** メソッドを使用します。 **finalize** メソッドへの暗黙的な呼び出しはありません。 そこでステートメントを実行するメソッドを呼び出す必要があります。 次の例は、**finalize** メソッドの呼び出しの基本構造を示しています。

    // From any method in a class.
    if (condition)
    {
        // Removes object from memory.
        this.finalize(); 
    }

**finalize** メソッドでは、必要なクリーンアップ コードも配置する必要があります。 たとえば、クラスがダイナミックリンク ライブラリ (DLL) モジュールを使用する場合、必要ではなくなったときに DLL をリリースする**確定**メソッドを使用できます。 **finalize** メソッドは慎重に使用してください。 オブジェクトへの参照がある場合オブジェクトを破棄します。

### <a name="setting-an-object-handle-to-null"></a>オブジェクト ハンドルを null に設定

オブジェクト ハンドルを **null** に設定してオブジェクトを終了します。 この方法は、他のオブジェクト ハンドルがそのオブジェクトを指していない場合にのみオブジェクトを破棄します。 他のコードがオブジェクト ハンドルを使用していないことを確認する必要があります。 次の例では、オブジェクト ハンドルを作成し、**null** に設定します。

    // Create an object handle of the type MyObject.
    MyObject mo;
    // Create an object of MyObject type and link it to the object handle.
    mo = new myObject();
    // Terminate the object.
    mo = null;

## <a name="creating-a-subclass"></a>サブクラスを作成しています
*サブクラス*は拡張または他のクラスから継承されるクラスです。 クラスは、他の 1 つのクラスのみ拡張することができます。 複数の継承はサポートされていません。 クラスを拡張する場合、サブクラスが親クラスの (*スーパークラス*) すべてのメソッドと変数を継承します。 サブクラスを使用すると、より特殊な目的で既存のコードを再利用できます。 したがって、設計、開発、テストの時間を節約できます。 スーパークラスの動作をカスタマイズするには、サブクラスのメソッドをオーバーライドします。 多くの場合、スーパークラスは、*基本クラス*として知られており、サブクラスは、*派生クラス*として知られています。

### <a name="subclass-example"></a>サブクラスの例

次の例では、まず **Point** という名前のクラスを作成します。 その後、**Point** クラスを拡張して、**ThreePoint** という新しいクラスを作成します。

    class Point
    {
        // Instance fields.
        real x; 
        real y; 

        // Constructor to initialize fields x and y.
        void new(real _x, real _y)
        { 
            x = _x;
            y = _y;
        }
    }

    class ThreePoint extends Point
    {
        // Additional instance fields z. Fields x and y are inherited.
        real z; 

        // Constructor is overridden to initialize z.
        void new(real _x, real _y, real _z)
        {
            // Initialize the fields.
            super(_x, _y); 
            z = _z;
        }
    }

### <a name="preventing-class-inheritance"></a>クラスの継承を禁止する

**最終** モディファイアーを使用して、クラスが継承されないようにすることができます。

    public final class Attribute
    {
        int objectField;
    }

## <a name="methods"></a>メソッド
次のコード ブロック タイプは、アプリケーション クラスの標準です。

- *<strong><em>classDescription</em>* 申告ブロック</strong> – この申告ブロックには<strong>パブリック</strong>、<strong>プライベート</strong>、および<strong>拡張</strong>などのクラス モディファイアーが含まれます。 これには、クラスから作成されたオブジェクトのフィールドのメンバーも含まれます。 <strong>this</strong> というキーワードを入力すると、IntelliSense にメンバーのリストを表示することができます。
- *<strong><em>新規</em>* メソッド</strong> – このメソッドは、クラスのインスタンスを作成します。 コンストラクターは、<strong>新しい</strong>キーワードを使用することによってのみ呼び出すことができます。 派生クラスは、<strong>super</strong> メソッドの参照を呼ぶことにとって、コントラクターの<strong>新しい</strong>メソッドを呼び出すことができます。
- *<strong><em>確定</em>* メソッド</strong> – このメソッドは、クラスのインスタンスを確定します。 このメソッドはデストラクター メソッドです。 ただし、規則のみのデストラクタです。 ガベージ コレクション中に <strong>finalize</strong> メソッドが自動的に呼び出されることはありません。

クラスの追加メソッドには、次のタイプがあります。

-   インスタンス メソッド
-   静的メソッド
-   主要メソッド

さまざまな種類の項目でメソッドを作成することができます。 次にいくつか例を挙げます。

-   クラス
-   マップ
-   ビュー
-   データ セット
-   フォーム
-   クエリ

### <a name="instance-methods"></a>インスタンス メソッド

インスタンス メソッド、またはオブジェクト メソッドは、クラスから作成される各オブジェクトに埋め込まれます。 メソッドの使用前に、オブジェクトのインスタンスを作成する必要があります。 後でインスタンス メソッドを静的メソッドに変換する場合は、クライアントを再起動する必要があります。 それ以外の場合、コンパイラは変更を検出しません。 インスタンス メソッドを静的メソッドに変換した後は、クラスのインスタンスからメソッドを呼び出すことができなくなります。 代わりに、クラス自体からメソッドを呼び出す必要があります。 静的メソッドは、次のセクションで説明します。 インスタンス メソッドを呼び出すには、次の構文を使用します。

    ClassName objectHandleName = new ClassName();
    objectHandleName.methodName();

### <a name="static-methods"></a>静的メソッド

*クラス メソッド*とも呼ばれる静的メソッドは、クラスに属しており、キーワード **static** を使用して作成されます。 静的メソッドを使用する前に、オブジェクトのインスタンスを作成する必要はありません。 静的メソッドは多くの場合、テーブルに格納されているデータを操作するために使用します。 メンバー変数は静的メソッドで使用できません。 静的メソッドを呼び出すには、次の構文を使用します。

    ClassName::methodName();

### <a name="main-methods"></a>主要メソッド

**メイン**メソッドは、メニュー オプションから直接実行されるクラス メソッドです。 このメソッドでは、オブジェクトのインスタンスを作成してから、必要なメンバー メソッドを呼び出す必要があります。 **\_args** パラメーターを使用して、メソッドにデータを転送できます。

    static void main (Args _args)
    {
        // Your code here.
    }

### <a name="declaration-of-methods"></a>メソッドの宣言

メソッドの宣言は、ヘッダーと本文で構成されます。 メソッド ヘッダーは、メソッドの名前と戻り値の型、メソッド モディファイア、およびパラメーターを宣言します。 (戻り値の型が**無効**である可能性があります。) メソッド本体は、変数宣言、メソッド宣言、および明細書で構成されます。

### <a name="return-type"></a>戻り値の型

メソッドが何も返さない場合、**無効**キーワードを使用する必要があります。 次の例は、2 つのメソッドを示しています。 1 つの方法に戻り値の型がありますが、他の方法には戻り値の型がありません。

    void methodNameNoReturnValue()
    {
        // Your code here.
    }

    // If a method returns something, you must specify the return type and include a return statement.
    int methodNameIntegerReturnValue()
    {
        return 1;
    }

### <a name="syntax"></a>構文

メソッドの宣言 = *ヘッダー*  *本文*ヘッダー = **\[** *モディファイアー* **\]**  *ReturnType*  *MethodName*  **(**  *ParameterList*  **)** モディファイアー = **\[クライアント\] \[サーバー\] \[edit | display | public | protected | private\] \[static | abstract | final \]** ReturnType = *Datatype*  **| void | anytype** MethodName = *識別子* ParameterList = **\[** *パラメーター*  **{ ,**  *パラメーター*  **}\]** パラメーター = *Datatype*  *Variableidentifier*  **\[ =**  *式*  **\]** 本文 = **{\[**  *VariableDeclarations*  **\] \[** *EmbeddedFunctionDeclarations*  **\] \[**  *ステートメント*  **\] }** EmbeddedFunctionDeclaration = *ヘッダー*  **{\[**  *VariableDeclarations*  **\] \[** *ステートメント*  **\]}** **anytype** の戻り値の型を使用した場合、メソッドはあらゆるデータ型を返すことができます。

### <a name="example-of-a-method-that-doesnt-have-a-return-type"></a>戻り値の型を設定していないメソッドの例

    void update ()
    {   
        // Variable declared and initialized
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

### <a name="example-of-a-method-that-has-parameters"></a>パラメーターを持つメソッドの例

次の例では、**checkAccountBlocked** メソッドはブール値を返し、**amountCur** パラメーターで動作します。

    boolean checkAccountBlocked(AmountCur amountCur)
    {
        if (this.blocked == CustVendorBlocked::All 
            ||(this.blocked == CustVendorBlocked::Invoice 
            && amountCur > 0 ))
        return checkFailed(strFmt("@SYS7987",this.accountNum));
        return true;
    }

## <a name="method-modifiers"></a>メソッド modifiers
いくつかのモディファイアーは、メソッドの宣言に適用することができます。 一部の修飾子を結合できます (たとえば、**final static**)。 メソッド モディファイア キーワードを次に示します。

-   **抽象** – メソッドは宣言されていますが、親クラスで実装されていません。 このメソッドはサブクラスで上書きする必要があります。 サブクラスに親クラスに属する 1 つ以上の抽象メソッドがあり、オーバーライドされていません。そのサブクラスからオブジェクトを作成しようとすると、コンパイラ エラーが発生します。 クラスは抽象クラスにすることもできます。 場合によっては、抽象的な概念を表す場合でもクラスをインスタンス化しないでください。 サブクラスのみインスタンスを作成する必要があります。 このタイプの基本クラスは**抽象**として宣言できます。 たとえば、勘定の概念をモデル化します。 実際の世界には派生クラス (勘定科目など) しか存在しないため、勘定は抽象です。 この例では、**勘定** クラスを**抽象**として宣言する必要があるという明確なケースについて説明します。
-   **ディスプレイ** – メソッドの戻り値は、ページまたはレポートに表示される必要があります。 ページまたはレポートで値を変更することはできません。 通常、戻り値は合計などの計算された値です。
-   **編集** – メソッドの戻り値のタイプは、ページで使用されるフィールドの情報を提供するために使用する必要があります。 このフィールドの値は修正できます。
-   **最終** – 同じクラスから派生したクラスのメソッドに上書きすることはできません。
-   **パブリック** – **パブリック**として宣言されるメソッドは、クラスがアクセスできるどの場所にもアクセスでき、サブクラスによって上書きすることができます。 アクセス修飾子を持たないメソッドは暗黙的にパブリックとなります。
-   **保護されている** – **保護されている**として宣言されるメソッドは、クラスおよびメソッドが宣言されている拡張されたクラスであるサブクラスの中のメソッドからのみ呼び出すことができます。
-   **プライベート** – **プライベート**として宣言されるメソッドは、プライベートメソッドが宣言されているクラスのメソッドからのみ呼び出すことができます。
-   **静的** – このメソッドはクラス メソッドであり、インスタンスを実行しません。 静的メソッドは、インスタンス変数を参照できません。 クラスのインスタンスでは呼び出されません。 代わりに、クラス名を使用して呼び出されます (たとえば、**MyClass::aStaticProcedure()**)。

### <a name="methods-that-have-modifiers"></a>モディファイアーのあるメソッド

**注記:** 次の例は、メソッド ヘッダーのみを示しています。

    // A method that cannot be overridden
    final int dontAlterMe() 

    // A static method 
    static void noChange()

    // A display method that returns an integer
    display int value()

## <a name="static-class-members"></a>静的クラス メンバー
静的クラス メンバーを宣言するには、**静的** キーワードを使用します。 **static** キーワードは、**new** を呼び出す回数に関係なく、メソッドの 1 つのインスタンスだけを作成するようシステムに指示します。 この 1 つのインスタンスは、セッション全体で使用されます。 一般に、静的メソッドは次の基準を満たしている場合を意図しています。

-   このメソッドは、クラス内で宣言されているメンバー変数にアクセスする必要はありません。
-   このメソッドは、クラスのインスタンス (静的でない) メソッドを呼び出す理由はありません。

#### <a name="static-methods"></a>静的メソッド

このセクションでは、違法コピーを防止するためにソフトウェア キー タイプを使用するシナリオについて説明します。 ソフトウェア キーの各インスタンスには、固有の値を持つことが可能です。 ただし、すべてのソフトウェア キーはソフトウェア キー設計のルールに準拠する必要があるため、ソフトウェア キーへの適合をテストするロジックはすべてのソフトウェア キーに対して同じです。 したがって、適合性検証ロジックを含むメソッドは静的でなければなりません。 **静的**キーワード使用して宣言されるメソッドの例を次に示します。

    static public boolean validateSoftwareKey(str _softwareKeyString)
    {
          // Your code here.
    }

次の例では、クラスで静的メソッドを呼び出す前に **SoftwareKey** クラスのインスタンスを構築する必要はありません。 静的な **validateSoftwareKey** メソッドを呼び出すときは、構文はそのメソッドを含むクラスの名前で始まります。 コロンのペア (::) は、クラス名を静的メソッド名に接続するために使用します。

    boolean yourBool = SoftwareKey::validateSoftwareKey(yourSoftwareKeyString);

#### <a name="static-fields"></a>静的フィールド

静的フィールドは**静的**キーワードを使用して宣言されているフィールドです。 概念的には、クラスに適用され、クラスのインスタンスには適用されません。

### <a name="static-constructors"></a>静的コンストラクター

静的コンストラクターは、静的またはインスタンス呼び出しがクラスに対して行われる前に実行されることが保証されます。 C\# では、*静的*の概念が実行中のアプリケーション ドメイン全体に関係します。 ただし、X++ では、静的コンストラクターの実行は、ユーザーのセッションに対して相対的です。 静的コンストラクターには、次の構文があります。

    static void TypeNew() 

静的コンストラクターは明示的に呼び出さないでください。 コンパイラは、コンストラクターがクラスの他のメソッドの前に正確に 1 回呼び出されるようにするコードを生成します。 静的コンストラクターは、任意の静的データを初期化したり、一度だけ実行する必要のある特定のアクションを実行するために使用されます。 静的コンストラクターに指定できるパラメーターはなく、**静的**としてマークする必要があります。 次の例は、静的コンストラクターを使用して単一のインスタンスを作成する方法を示しています。

    public class Singleton
    {
      private static Singleton instance;

      private void new()
      {
      }

      static void TypeNew()
      {
        instance = new Singleton();
      }

      public static Singleton Instance()
      {
        return Singleton::instance;
      }
    }

単一は、クラスのインスタンスが 1 つしか呼び出されないことを保証します。 次の例は、単一をインスタンス化する方法を示しています。

    {
        Singleton i = Singleton::Instance();
    }

## <a name="method-access-control"></a>メソッド アクセス制御
その他のクラスのメソッドがお客様のクラスのメソッドを呼び出すことができるかどうかを制御するには、アクセサー キーワード **public**、**protected**、および **private** を使用します。 メソッドのアクセス キーワードは、クラス継承のルールとも連携します。 メソッドを使用するアクセサー キーワードを次に示します。

-   **パブリック** – **パブリック**として宣言されるメソッドは、クラスがアクセスできるどの場所からでも呼び出すことができます。 さらに、メソッドが**最終**として宣言されていない限り、パブリック メソッドをサブクラスでオーバーライドできます。
-   **保護されている** – **保護されている**として宣言されるメソッドは、次のメソッドからのみ呼び出すことができます。
    -   クラスのメソッド。
    -   保護されたメソッドを含むクラスのサブクラス内のメソッド。 保護されているメソッドは、サブクラスで上書きできます。
-   **プライベート** – **プライベート**として宣言されるメソッドは、プライベートメソッドが宣言されているクラスのメソッドからのみ呼び出すことができます。 サブクラスでプライベート メソッドをオーバーライドできません。 既定では、新しいメソッドを作成するときに、**プライベート** アクセサー キーワードがコード エディターに表示されます。 最大限のセキュリティについては、**プライベート**が最も保守的な既定のアクセス キーワードです。

### <a name="static-and-instance-methods"></a>静的およびインスタンス メソッド

メソッドのアクセサー キーワードは、どのメソッドが静的であるか、静的でないかに関係なく、同じクラスにある 2 つのメソッド間の呼び出しを制限することはありません。 静的メソッドでは、**新しい**コンストラクター メソッドが**プライベート** モディファイアーで修飾されている場合でも、**新しい**コンストラクター メソッドに対する呼び出しは有効です。 これらの呼び出しの構文では、**新しい**キーワードを使用する必要があります。 静的メソッドのコードは、クラスのインスタンス メソッドを呼び出す前に、独自のクラスのインスタンス オブジェクトを構築する必要があります。

### <a name="increasing-access-during-overrides"></a>オーバーライド中のアクセス増加

サブクラス内でメソッドがオーバーライドされると、オーバーライドするメソッドは少なくともオーバーライドされるメソッドと同程度のアクセスが可能なことが必要です。 たとえば、次のコンパイラ ルールは、サブクラスで保護されたメソッドが上書きされる時に適用されます。

-   スーパークラスのパブリック メソッドは、サブクラスのパブリック メソッドによってのみ上書きできます。
-   サブクラスでは、パブリック メソッドまたは保護対象のメソッドはスーパークラスの保護対象のメソッドをオーバーライドできません。
-   サブクラスでは、プライベート メソッドはスーパークラスの保護対象のメソッドをオーバーライドできません。

## <a name="optional-parameters"></a>オプションのパラメーター
パラメーターは、メソッド宣言で初期化することができます。 この場合、パラメーターは*オプションのパラメーター*となります。 メソッドの呼び出しの値が指定されていない場合は、既定値が使用されます。 すべての必須パラメータは最初のオプション パラメーターの前に一覧表示する必要があります。 次の例では、オプションのパラメーターを持つメソッドを作成して呼び出す方法を示しています。 **AddThreeInts** メソッドの例は、メソッドを呼び出すときにデフォルトのパラメーターをスキップできないことを示しています。

### <a name="examples-of-optional-parameters"></a>オプション パラメーターの例

    // This is an example of a function being used as the default.
    public class Person 
    {
        date birthDate;

        // The constructor that takes a date type as
        // a parameter. That value is assigned to the field member birthDate. 
        void new(date _date)
        {
            birthDate = _date;
        }

        // The CalculateAgeAsOfDate method references
        // the birthDate field, is called by the Main method, and has an 
        // optional parameter. In this example, the default value is the
        // return value of a function. 
        public real CalculateAgeAsOfDate(date _calcToDate = DateTimeUtil::getToday(DateTimeUtil::getUserPreferredTimeZone()) )  
        {
            return (_calcToDate - birthDate) / 365;
        }

        // The Main method calls the CalculateAgeAsOfDate method twice. 
        static public void Main(Args _args)
        {
            Person mc = new Person(13\5\2010);   // birthDate is initialized.
            // Optional parameter's default is used.
            print( "Age in years: " + num2str(mc.CalculateAgeAsOfDate(),2,0,0,0));
            // January 2, 2044  is the parameter value for _date.
            print "Age in years: " + num2str(mc.CalculateAgeAsOfDate(2\1\2044),2,0,0,0);
        }
    }

    // This is an example of how you cannot skip to a second optional parameter. 
    // The first method has two optional parameters. The second method is a caller 
    // of the first method. The caller wants to override only the _i3 default value, but the 
    // compiler requires that all prior optional parameters also 
    // be overridden in the call. 
    public class Additions {
        static public int AddThreeInts(int _i1, int _i2 = 2,int _i3 = 3)
        {
            return _i1 + _i2 + _i3;
        }
    }

    // The second method has a commented section showing the
    // failed attempt to accept the default of the first optional 
    // parameter (_i2) while trying to override the final optional 
    // parameter (_i3).
    static public void Main(Args _args)
    { 
        // No way to skip the first optional parameter (so it can default)
        // while also specifying the value of the second optional parameter.
        // The next statement does not compile.
        //print Additions::AddThreeInts(1, , 99);

        // Settle for overriding both optional parameters.
        print Additions::AddThreeInts(1, 2, 99);
    }

## <a name="accessor-methods"></a>アクセサー メソッド
クラス変数はプライベートです。 クラスの内部実装の詳細を非表示にすることで、そのクラスを使用するコードを破棄することなくクラスの実装を後で変更することができます。 参照変数からデータにアクセスするには、アクセサー メソッドを作成する必要があります。 次の例では、アクセス メソッドを使用して変数 **x** および **y** にアクセスする **Point** クラスを定義します。

    class Point
    {
        // Instance variables
        real x; 
        real y;

        //Constructor to initialize to a specific or default value
        void new(real _x=10, real _y=10) 
        {
            x = _x;
            y = _y;
        }

        //Accessor methods
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

これらのメソッド宣言は、**Point** クラスが外部からの変数へのアクセスを提供する方法を示しています。 その他のオブジェクトは、アクセサー メソッドを使ってインスタンス変数 **Point** オブジェクトを操作できます。

    // Declare a variable to refer to a Point object
    Point myPoint; 
    // Create a Point object
    myPoint = new Point(); 
    // Set the x variable using the accessor method
    myPoint.setX(10.0); 
    // Set the y variable by means of the accessor method
    myPoint.setY(25.7);

コール スタックの深さは 100 に制限されています。

## <a name="overriding-a-method"></a>メソッドのオーバーライド
クラス内のメソッドは、それを拡張するクラスによって継承されます。 継承されたメソッドの機能を変更するには、サブクラスでメソッドを作成し、そのメソッドにスーパークラスのメソッドと同じ名前とパラメーターを指定します。 このプロセスは、メソッドを*オーバーライドする*として知られています。 次の例では、**ColorAttribute** は**属性**のサブクラスであるため、**methodAttr** メソッドを継承します。 ただし、**ColorAttribute** は同じ名前および同じ数の引数を持つメソッドを定義するため、スーパークラスのメソッドは上書きされます。

    // Superclass: Attribute
    public class Attribute
    {
        int objectVariable;

        void methodAtt()
        {
            //Some statements
        }
    }

    // Subclass: ColorAttribute
    public class ColorAttribute extends Attribute
    {
        int addedObjectVariable;

        void methodAtt()
        {
            //Some statements
        }
    }

### <a name="preventing-method-overrides"></a>メソッドのオーバーライドを禁止する

静的メソッドは、クラスごとに存在するため上書きすることはできません。 他の重要なメソッドやコア メソッドがオーバーライドされないようにするには、**final** 修飾子を使用します。 次の例では、**methodAtt** が **final** として宣言されているため、**属性**を拡張するクラスでオーバーライドできません **最終** に **新規** または **確定** のメソッドを指定しないでください。 次の例は、**final** キーワードの使用方法を示しています。

    public class Attribute
    {
        int objectVariable;

        final void methodAtt()
        {
            //Some statements
        }
    }

### <a name="overriding-vs-overloading"></a>オーバーライドとオーバーロード

オーバーライドは、メソッドのスーパークラスの実装がそのメソッドのサブクラスの実装によって変更されるが、両方のメソッドのシグネチャが同じ場合に行われます。 対照的に、*オーバーロード*は複数のメソッドが同じ名前を持つ場合に発生しますが、メソッドは異なるシグネチャ (戻り値の型、パラメーター リスト、または両方) を持ちます。 X++ はオーバーライドをサポートしますが、オーバーロードはサポートしていません。

## <a name="parameters"></a>パラメーター
すべてのメソッドは独自の*スコープ*を持っています。 メソッドは、1 つ以上のパラメーターを受け取ることができます。 メソッドのスコープ内では、これらのパラメーターはローカル変数として処理され、メソッド呼び出しのパラメーターからの値で初期化されます。 すべてのパラメーターは値で渡されます。 元の変数の値を変更することはできません。 メソッド内のローカル変数のみを変更することができます。 このローカル変数は元の変数のコピーです。

## <a name="scope-of-variables-in-methods"></a>メソッドでの変数の範囲
スコープは、品目にアクセスできるエリアを定義します。 クラスで定義されている変数は、そのクラス内のメソッドで使用できます。 メソッド内の変数は、現在のブロック内でのみアクセスできます。

## <a name="local-functions"></a>ローカル関数
メソッド内部のローカル関数を宣言することができます。 ただし、ベスト プラクティスとしては、メソッド内のローカル機能を追加する必要はありません。 代わりに、プライベート メソッドをクラスに追加する必要があります。 次の例は、2 つのローカル関数、**localFunc55b** および **localFunc66c** の有効な宣言を示しています。 ローカル関数への呼び出しは、必要に応じて、この例の関数宣言の後に行われます。

    static void G_LocalFuncJob2(Args _args) 
    {
        int nn = 654;
        void localFunc55b(int _iNum)  // The local function.
        {
            str sInnerString;
            sInnerString = "String_in_localFunc55b";
            info(strFmt("localFunc55b: %1 , %2 , %3", 
                _iNum, sInnerString, nn));
        }

        void localFunc66c()
        {
            info("Printing from inside localFunc66c.");
        }

        localFunc55b(55);
        localFunc66c();
        // Next print statement would fail to compile,
        // because sInnerString is restricted to the
        // scope of the local function in which it is declared.
        // print sInnerString; 
    }
    /***  Infolog window display:
    Message (07:38:54 pm)
    localFunc55b: 55 , String_in_localFunc55b , 654
    Printing from inside localFunc66c.
    ***/

### <a name="declaration-of-local-functions"></a>ローカルの関数の宣言

-   ローカル関数の宣言は、メソッド内の宣言されていないステートメントの前に物理的に先行する必要があります。
-   メソッド内で 1 つ以上のローカル関数を宣言することができます。 ただし、すべてのローカル関数は中断のないシリーズで宣言され、セットは 1 つのセミコロン (;) で終了する必要があります。

### <a name="variable-scope"></a>変数のスコープ

-   ローカル関数内にあるコードは、ローカル関数を含むメソッドで宣言されている変数にアクセスできます。
-   ローカル関数の外にあるコードは、ローカル関数で宣言された変数にアクセスすることはできません。

### <a name="calls-to-local-functions"></a>ローカルの関数への呼び出し

-   ローカル関数は、ローカル関数が宣言されているのと同じメソッド内のコードによってのみ呼び出すことができます。
-   ローカル関数が、それ自体を呼び出すことはありません。 このような再帰は、正常に行われるコンパイルを防ぐことができます。

## <a name="the-this-keyword"></a>このキーワード
**this** キーワードは、**this** キーワードが使用されるクラスやテーブルのインスタンスへの参照です。 **this** 参照が必須になることはありませんが、コードを明確にし、コード エディターで IntelliSense の動作を強化することができます。 すべての呼び出しインスタンス メソッドは**これ**を参照または変数のいずれかにより修飾される必要があります。 **this** 参照は、次の情報を修飾するために使用できます。

-   **this** 参照が使用されている同じクラス内の他のインスタンス (静的でない) メソッドの名前。 次に例を示します: **boolColorChanged = this.colorItOrange();**
-   **this** オブジェクトによって継承されるメソッドの名前。
-   **this** キーワードが使用されるメソッドを含むテーブル上のフィールドの名前。

**this** 参照は、次の方法で使用できません。

-   **classDeclaration** コードで宣言されているメンバー変数の名前を限定することはできません。
-   静的メソッドで使用できません。
-   クラスやテーブルの静的メソッドの名前を限定することはできません。

## <a name="interfaces"></a>インターフェイス
<em>インターフェイス</em>はパブリック インスタンス メソッドのセットを指定します。 他から 1 つのクラスを派生させることなく、インターフェイスは無関係なクラス間の類似点を定義し適用します。 *<strong><em>*</em>classDeclaration</strong> コード内の<strong>インターフェイス キーワード*<em>の前に</em></strong><strong>パブリック</strong> キーワード*を明示的に追加しなくても、すべてのインターフェイスはパブリックです。 インターフェイス上のメソッドも公開されています。 この場合も、<strong>パブリック</strong>というキーワードを明示的に含めることはオプションです。 インターフェイスを作成するには、次の手順を実行します。

1.  サーバー エクスプローラーで、プロジェクトを右クリックしてから**追加**をクリックします。
2.  **新しい項目**ダイアログ ボックスで、**インターフェイス**を選択してからインターフェイスの名前を入力します。
3.  **追加** をクリックします。

クラス宣言に **implements** キーワードを追加すると、そのクラスは、インターフェイスによって指定されるメソッドを宣言する必要があります。 クラス宣言では、複数のインターフェイスを実装することができます。 **implements** キーワードの単一の発生後にインターフェイスを一覧表示し、インターフェイス名をコンマで区切ります。 クラスで実装するすべてのインターフェイス メソッドはクラスの**パブリック**を使用して**パブリック**キーワードを明示的に宣言する必要があります。 インターフェイスを実装するクラスも**パブリック**として宣言する必要があります。 インターフェイスを**拡張**キーワードを使用して別のインターフェイスに拡張できます。 ただし、インターフェイスは、複数のインターフェイスを拡張することはできません。

### <a name="interface-example"></a>インターフェイスの例

次の例では、**Automobile** クラスは **IDrivable** インターフェイスを実装しています。 **is** キーワードはサポートされており、クラスがインターフェイスを実装するかどうかをテストすることができます。

    public interface IDrivable
    {
        public int getSpeed()
        {
        }

        public void setSpeed(int newSpeed)
        {
        }
    }

    class Automobile implements IDrivable
    {
        int m_speed;

        public int getSpeed()
        {
            return m_speed;
        }

        public void setSpeed(int newSpeed)
        {
            m_speed = newSpeed;
        }
    }

    class UseAnAutomobile
    {
        void DriveAutomobile()
        {
            IDrivable yourIDrivable;
            Automobile myAutomobile;
            str sTemp = "object is not an IDrivable";

            myAutomobile = new Automobile();

            if (myAutomobile is IDrivable)
            {
                yourIDrivable = myAutomobile;
                yourIDrivable.setSpeed(42);
                sTemp = int2str(yourIDrivable.getSpeed());
            }

            Global::info(sTemp);
            return;
            // output
            // Message (06:46:33 pm)
            // 42
        }
    }

## <a name="class-library-overview"></a>クラス ライブラリの概要
*アプリケーション クラス*および*システム クラス*の、2 種類のクラスがあります。

-   **アプリケーション クラス** - これらのクラスは X++ で実装されています。 これらはアプリケーション エクスプローラーの **Classes** ノードで使用できます。
-   **システム クラス** – これらのクラスは *カーネル クラス* としても知られており、C++ では実装されています。 アプリケーション エクスプローラーの **System Documentation** &gt; **Classes** ノードの下に一覧表示されます。 ただし、これらのクラスのソース コードは使用できません。

これらのクラスの一覧については、[API、クラス、およびテーブルの参照](api-reference.md) を参照してください。

## <a name="substituting-application-classes-for-system-classes"></a>システム クラス用のアプリケーション クラスの置き換え
拡張するシステム クラスの代わりに *アプリケーション クラスの置き換え* を呼び出す必要があります。 アプリケーション エクスプローラーの**システムのドキュメント** &gt; **クラス**で、いくつかのカーネルまたはシステム クラスの名前は小文字 *x* で始まります。 これらのクラスは、*x-system classes* とも呼ばれています。 これらのシステム クラスの例には、**xApplication** および **xVersionControl** が存在します。 これらのクラスのいくつかは、アプリケーション クラスによって拡張されます。 たとえば、**アプリケーション**クラスは **xApplication** システム クラスを拡張します。 X システム クラスから派生するクラスは、アプリケーション クラスの代用として知られています。 アプリケーション エクスプローラーの**クラス** ノードで、代替アプリケーション クラスの横にあるアイコンは標準のアイコンと異なります。

### <a name="x-system-classes"></a>x システム クラス

代替アプリケーション クラスの一部は、クラスのインスタンスを表す特殊なグローバル変数に関連付けられます。 たとえば、**appl** 変数は、**アプリケーション**クラスから事前にインスタンス化されたオブジェクトを参照します。 **appl** 変数の利点は、セッションの範囲全体にわたってシステムがオブジェクトを保持することです。 **Application** クラスのインスタンスを取得するために **new Application()** 構文を繰り返し使用した場合、コードの効率が低下します。 **xApplication** システム クラスは使用しないでください。 代わりに、**アプリケーション**の代替アプリケーション クラスを使用します。 標準構文 **Application::checkForNewBatchJobs()** を使用することにより、**アプリケーション** クラスの静的メンバーを参照することができます。 ただし、**アプリケーション**クラスのインスタンス メンバーを参照するには、そのクラスの **appl** 変数 (存在する場合) を使用する必要があります。 このパターンは、ほとんどの x システム クラスに適用されます。 **セッション** 代替アプリケーション クラスは、**セッション** の特殊なグローバル変数がないため 1 つの例外です。 次のテーブルは、対応するアプリケーション クラスの代用を持つ x システム クラスの一覧です。 特殊なグローバル変数は、それらを持つクラスに対しても表示されます。

| アプリケーション クラス | x システム クラス  | グローバル変数    |
|-------------------|-----------------|--------------------|
| 引数              | xArgs           | 該当なし     |
| 申請       | xApplication    | **appl**           |
| ClassFactory      | xClassFactory   | **classFactory**   |
| 法人           | xCompany        | **appl.company**   |
| グローバル            | xGlobal         | 該当なし     |
| 情報              | xInfo           | **情報ログ**        |
| MenuFunction      | xMenuFunction   | 該当なし     |
| セッション           | xSession        | 該当なし     |
| VersionControl    | xVersionControl | **versionControl** |

### <a name="example-of-x-system-classes"></a>x システム クラスの例

次の例は、代替アプリケーション クラスのインスタンスを参照するいくつかの特殊な変数を使用するための構文を示しています。

    static void UseSpecialSystemVariablesForXJob(Args _a)
    {
        TreeNode treeNode2;
        Args     args3;
        FormRun  formRun4;
        // appl variable
        print appl.buildNo();
        // company variable
        appl.company().reloadRights(); // referenced through appl
        // Infolog variable
        treeNode2 = infolog.findNode("\\forms\\custTable");
        print treeNode2.AOTgetProperty("Name");

        // classFactory variable
        args3 = new Args(formstr(vendTable));
        formRun4 = classFactory.formRunClass(args3);
        formRun4.init();
        formRun4.run();
        formRun4.detach();
        Global::info("Method is ending. This is a message in the Infolog.");
    }

## <a name="running-startup-commands"></a>起動コマンドの実行
起動時にコマンドを実行するには、**SysStartupCmd** クラス フレームワークを使用します。 Finance and Operations の起動時に、アプリケーション代替カーネル クラスである **Application** (**Application.startup**) および **Info** (**Info.startup**) の ***startup** メソッドへの呼び出しが行われます。 **startup** メソッドは必須システムおよびバージョン固有の呼び出しで使用されるものであり、直接変更することはできません。 代わりに、**SysStartupCmd** フレームワークを使用します。 SYS レイヤ バージョンの **startup** メソッドが呼び出されなかった場合、深刻な問題が生じる可能性があります。 次の例は、Finance and Operations の起動時に呼び出しが実行される順序を示しています。

    appl.startup() // The SysStartupCmd class is instantiated here.
    sysStartupCmd.applInit()
    super()
    sysStartupCmd.applRun()
    info.startup()
    sysStartupCmd.infoInit()
    super()
    sysStartupCmd.infoRun()

### <a name="commands-that-are-available-when-finance-and-operations-starts"></a>Finance and Operations 起動時に使用できるコマンド

**SysStartupCmd.construct** メソッドは、Finance and Operations が起動したときに使用できるコマンドを一覧表示します。 これらのコマンド例を次に示します。

-   AutoRun
-   AOTImport
-   同期

次の例は、Finance and Operations の起動時に新しいコマンドを実行する方法を示しています。 最初に、<strong>SysStartupCmd</strong> を拡張するクラスが作成されます。 この新しいクラスは特定のタスクを実行します。 次に、自分のクラスを呼び出すために、<strong>SysStartupCmd</strong> の construct メソッドを変更します。 Finance and Operations のコンフィギュレーション ユーティリティの<strong>一般</strong>タブにある<strong>アプリケーション起動時に実行するコマンド</strong> フィールドで、起動時に実行するコマンドを追加できます。 または、<strong>-startupcmd= *MyCommand</strong>* コマンド ライン パラメーターを使用できます。

    public class SysStartupCmdAutoRun : extends SysStartupCmd 
    {
        void new(str s, str parm) 
        {
            // Your code here.
        }
    }

    // This is a framework class. Customizing this class may cause problems with future upgrades to the software.
    class SysStartupCmd
    {
        // Code delete for readability

        static SysStartupCmd construct(str startupCommand)
        {
            // Code delete for readability
            switch (s)
            {
                // Other cases delete for readability    
                case 'autorun':
                    sysStartupCmd = new SysStartupCmdAutoRun(s,parm);
                    break;
                // Other cases delete for readability
            }
            // Code delete for readability
        }
    }

## <a name="batch-processing-classes"></a>バッチ処理クラス
クラスを実装するには、バッチ処理システムを使用し、**RunBase** および **RunBaseBatch** クラスを拡張します。 **バッチ処理**ダイアログ ボックスから**繰り返し**ボタンを削除するには、**Args::parmEnum** メソッドを使用します。 サーバー バインド バッチ メソッドとして実行するクラスを指定することをお勧めします。 サーバー バインド バッチ メソッドは、以下の理由のため、サーバー バインドでないバッチ メソッドより安全です。

-   このメソッドは、メソッドを送信したユーザーのアクセス許可を使用して実行されます。
-   このメソッドは、特定の **情報** および **グローバル** クラス メソッドのみを使用して、それを処理しているクライアントと対話できます。 この制限により、クライアントとのやり取りが制限されます。

### <a name="enable-a-class-to-run-as-a-server-bound-batch-method"></a>サーバー バインド バッチ メソッドとして実行するクラスを有効化

1.  **RunBaseBatch** クラスを拡張するクラスを作成します。
2.  次の例に示すように、**RunBaseBatch.runsImpersonated** メソッドをオーバーライドし、値 **true** を返します。

        public boolean runsImpersonated()
        {
            return true;
        }

3.  クラスが次の**情報**および**グローバル**クラスのメソッドのみを呼び出すことを確認します。
    -   追加
    -   Info.copy
    -   Info.cut
    -   Info.import
    -   Info.export
    -   Info.line
    -   Info.num
    -   Global::error
    -   Global::info
    -   Global::warning

    **注記:** **Info.line** および **Info.num** メソッドは、**xInfo** クラスから継承されます。

### <a name="removing-the-recurrence-button-from-the-batch-processing-dialog-box"></a>バッチ処理ダイアログ ボックスから定期的なアイテムを削除

バッチ処理システムを使用してクラスを実装するときは、**Args.parmEnum** メソッドを呼び出し、**NoYes::Yes** システム列挙値を渡して、**再実行**ボタンを削除できます。 **NoYes** システム列挙は、**繰り返し** ボタンがダイアログ ボックスから削除されるかどうかを決定します。 既定値は **NoYes::No** です。 次の例では、**InventTransferMultiShip** クラスが実装されています。 **BatchDialog::main** メソッドは、**バッチ処理**ダイアログ ボックスを作成します。

    static void noRecurrenceButton(Args _args)
    {
        Args a;
        InventTransferMultiShip inventTransferMultiShip;
        a = new Args();
        inventTransferMultiShip = InventTransferMultiShip::construct();
        a.caller(inventTransferMultiShip);
        a.parmEnum(NoYes::Yes);
        BatchDialog::main(a);
    }

## <a name="image-manipulation-classes"></a>イメージ操作クラス
**Image** と **Imagelist** の 2 つのシステム クラスにより、グラフィックスとアイコンを操作できます。

- **Image** – このクラスでは、個々の画像の読み込み、保存、操作などができます。 たとえば、画面をキャプチャして画像として保存し、画像をトリミングまたは回転させる、または色深度を操作します。
- <strong>Imagelist</strong> - このクラスを使用すると、サイズや透明色などの一般的なプロパティを持つ一連の画像を操作できます。 <strong>ImageListAppl\_\</strong>* アプリケーション クラス の Finance and Operations で使用されるイメージ リストを表示できます。

## <a name="query-object-model"></a>クエリ オブジェクト モデル
クエリ オブジェクト モデルには、クエリの定義と実行に使用されるクラスが含まれています。 クエリ オブジェクトは、クエリ データ ソース、返されるフィールド、レコード範囲、子データ ソースとの関係を定義するために使用されます。 動的クエリをコードで作成すると、クエリ クラスの可視性が高まります。さらに、これらは、アプリケーション エクスプローラーで静的クエリを作成するときにもシーン裏で使用されます。 次のテーブルでは、クエリ オブジェクト モデルのクラスについて説明します。

| システム クラス         | 説明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| QueryRun             | このクラスは、クエリを実行し、データをフェッチします。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| クエリ                | このクラスはいくつかのプロパティを保持し、1 つ以上の関連するデータ ソースを持ちます。 クエリの定義の最上位です。                                                                                                                                                                                                                                                                                                                                                                                                                             |
| QueryBuildDataSource | このクラスは、クエリ内の単一のデータ ソースへのアクセスを定義します。 クエリに同じレベルの 1 つ以上のデータ ソースある場合、独立した SQL ステートメントが生産され、順番に実行されます。 データ ソースが別のデータ ソースの子である場合は、2 つのデータ ソース間に結合が作成されます。                                                                                                                                                                                                                                            |
| QueryBuildFieldList  | このクラスは、データベースから返されるフィールドを定義します。 既定では、フィールド リストは動的であり、すべてのフィールドはデータ ソース テーブル、マップ、またはビューから戻されます。 各データ ソースには、**QueryBuildFieldList** オブジェクトが 1 つだけあります。 このオブジェクトには、選択したすべてのフィールドに関する情報が含まれます。 フィールド リスト オブジェクトで、**SUM**、**COUNT**、および **AVG** などの、集計関数を指定することができます。                                                                                                                                   |
| QueryBuildRange      | このクラスは、単一フィールドに基づいて、返されるレコードのサブセットを定義します。 範囲は、クエリ SQL ステートメントの **WHERE** 句に変換されます。 クエリを制限するために 1 つ以上のフィールドが使用されている場合 (**WHERE**句)、データ ソースには 1 つ以上の範囲が含まれます。                                                                                                                                                                                                                                                                 |
| QueryBuildDynalink   | このクラスには、外部レコードとの関係 (制限) に関する情報が含まれます。 クエリを実行すると、この情報は、クエリ SQL ステートメントの **WHERE** 句内で追加のエントリに変換されます。 このクラスは、クエリの親データ ソースにのみ存在できます。 フォームは、2 つのデータ ソースが同期されるときにこの機能を使用します。 子データ ソースは、親データ ソース に対する 1 つ以上の DLL を格納します。 この関数は、2 つのデータソースが 2 つの異なる形式になっていて、まだ同期されている場合でも使用されます。 |
| QueryBuildLink       | このクラスは、結合に 2 つのデータ ソースの間の関係を指定します。 このクラスは、子データ ソースにのみ存在できます。                                                                                                                                                                                                                                                                                                                                                                                                                       |

## <a name="system-classes-overview"></a>システム クラスの概要
システム クラス (またはカーネル クラス) は C++ で実装されます。 これらのクラスのソースは使用できません。 システム クラスは、次の特性を持つことができます。

-   静的メソッド (またはクラス メソッド)
-   動的メソッド
-   プロパティ - これらのプロパティは、プロパティを設定するために使用されるメンバー関数です。 たとえば **LeftMargin** です。

システム クラスのメソッドをオーバーライドすることはできません。 最初からアプリケーション オブジェクトをデザインするためにシステム クラスを使用することを意図していません。 代わりに、アプリケーション エクスプローラーで既存の機能を拡張または変更するために使用します。 たとえば、既存のレポートに追加情報を動的に追加することができます。 または、前のページでのユーザーの選択に基づいて、ページ上で使用可能なオプションを変更することができます。

### <a name="collection-classes"></a>コレクション クラス

*コレクション クラス*を使用すると、リスト、セット、構造体、マップ、および配列を作成できます。

### <a name="application-object-classes"></a>アプリケーション オブジェクト クラス

これらのシステム クラスは、アプリケーション エクスプローラーを使用してアプリケーションを作成するたびにアクティブ化される関数を保持します。 たとえば、システムは、アプリケーション エクスプローラーの**設計**ノードでフォームのレイアウトを定義する時、**FormDesign** クラスを使用します。 これらのクラスを使用すると、アプリケーション オブジェクトを作成したり変更したりすることもできます。

### <a name="integration-classes"></a>統合クラス

環境との統合は、通常、クラスによって実装されます。 このカテゴリ内のクラスの例を次に示します。

-   **COM** - COM オブジェクトのメソッドの呼び出しです。
-   **DLL** – Microsoft Windows DLL 関数の呼び出し。
-   **IO** – 外部ファイルの読み取りと書き込みを行います。
-   **ODBCConnection** – 外部データベースへの Open Database Connectivity (ODBC) インターフェイス。

## <a name="event-terminology-and-keywords"></a>イベントの用語およびキーワード
イベント設計パターンを使用すると、コードをさらにモジュール化して再使用可能にすることができます。 *イベント* という用語は、デリゲートの使用方法を説明するメタファです。 プログラム実行中に何か重要なことが発生したときは、他のモジュールがその発生を処理することが必要な場合があります。 これらの重要な出来事は*イベント*と呼ばれています。 イベントが発生すると、プログラムは、Notifier がイベントに関する通知を送信する必要があることを、そのイベントの Notifier に指示します。 通知は、通知のサブスクライバーであるすべてのイベント ハンドラーに送信する必要があります。 プログラムがその通知機能に通知を送信するように指示するとき、そのプロセスをイベントの *発生* と呼んでいます。 次のテーブルは、イベント メタファを説明するために使用される用語を示しています。

| 期間          | 説明                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------|
| イベント         | 追加モジュールは発生を処理するプログラム モジュールで重要な発生です。                         |
| 通知機能      | 通知機能に登録されているすべてのイベント ハンドラーに、イベントに関する情報を送信するプログラム要素。 |
| サブスクライバー    | イベント通知機能を登録しているプログラム機能またはメソッド。                                                |
| イベント ハンドラー | イベント通知を購読するメソッド。 適切な種類のメソッドのみ、イベント ハンドラーになることができます。              |

### <a name="keywords-that-are-used-for-programming-that-uses-delegates"></a>デリゲートを使用するプログラミングに使用されるキーワード

次のテーブルに、デリゲートの使用方法を説明するキーワードを示します。

| キーワードや用語                         | 区分                                                                     | 説明                                                                                                                                                                                                                                                                             |
|-----------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| デリゲート                                | delegate myDelegate(str \_information) {}                                | このコードは、Microsoft MorphX クライアントのメソッド エディターでのデリゲートの外観を示しています。 戻り値の型は常に**無効**なので、構文には示されていません。 かっこ ({}) 内にコードは使用できません。                                                               |
| eventHandler                            | myClassInstance.myDelegate += eventHandler(otherClass.myInstanceMethod); | **eventHandler** キーワードの構文は **eventHandler** X++ 関数であるという印象を与えますが、それは関数ではありません。 **eventHandler** キーワードは、メソッドがデリゲートにサブスクライブされることをコンパイラに伝えます。                                           |
| デリゲートにメソッドをサブスクライブまたは追加 | myClassInstance.myDelegate += eventHandler(OtherClass::aStaticMethod);   | コードでは、静的メソッド **OtherClass::aStaticMethod** がデリゲートにサブスクライブされます。                                                                                                                                                                                        |
| デリゲートの呼び出し                         | myClassInstance.myDelegate("Hello");                                     | デリゲートへのこの呼び出しは、デリゲートにサブスクライブしている各メソッドを呼び出すようにデリゲートに要求します。 サブスクライブされたメソッドは、デリゲートに追加されたのと同じ順序で呼び出されます。 1 つのサブスクライブされたメソッドは、そのデリゲードが次のメソッドを呼び出す前に完了される必要があります。 |






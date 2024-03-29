---
title: X++ 継承
description: この記事では、X++ の継承について説明します。
author: josaw1
ms.date: 06/18/2019
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3192d79084642c45c76bf6ee0b5e53344c35c838
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271315"
---
# <a name="x-inheritance"></a>X++ 継承

[!include [banner](../includes/banner.md)]

この記事では、X++ の継承について、サブクラスを作成する方法とメソッドを上書きする方法を含めて説明します。

## <a name="creating-a-subclass"></a>サブクラスを作成しています
*サブクラス* は拡張または他のクラスから継承されるクラスです。 クラスは、他の 1 つのクラスのみ拡張することができます。 複数の継承はサポートされていません。 クラスを拡張する場合、サブクラスが親クラスの (*スーパークラス*) すべてのメソッドと変数を継承します。 サブクラスを使用すると、より特殊な目的で既存のコードを再利用できます。 したがって、設計、開発、テストの時間を節約できます。 スーパークラスの動作をカスタマイズするには、サブクラスのメソッドをオーバーライドします。 多くの場合、スーパークラスは、*基本クラス* として知られており、サブクラスは、*派生クラス* として知られています。

### <a name="subclass-example"></a>サブクラスの例

次の例では、まず **Point** という名前のクラスを作成します。 その後、**Point** クラスを拡張して、**ThreePoint** という新しいクラスを作成します。

```xpp
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
```

### <a name="preventing-class-inheritance"></a>クラスの継承を禁止する

**最終** モディファイアーを使用して、クラスが継承されないようにすることができます。

```xpp
public final class Attribute
{
    int objectField;
}
```

## <a name="overriding-a-method"></a>メソッドのオーバーライド
クラス内のメソッドは、そのクラスを拡張するクラスによって継承されます。 継承されたメソッドの機能を変更するには、サブクラスでメソッドを作成し、そのメソッドにスーパークラスのメソッドと同じ名前およびパラメーターを指定します。 このプロセスは、メソッドを *オーバーライドする* として知られています。 

サブクラスのインスタンスを作成するとき、スーパークラスの型の変数またはサブクラスの型の変数のいずれかに照会を割り当てることができます。 変数の型に関係なく、上書きされたメソッドが呼び出されます。 

次のコード例は、サブクラスが **書き込み** メソッドを上書きします。 2 つの変数、**ポイント** する両方の型が作成されます。 一方に **1 ポイント** オブジェクトが割り当てられ、もう一方には、**3 ポイント** オブジェクトが割り当てられます。 **書き込み** メソッドが **3 ポイント** オブジェクトに対して呼び出されるとき、このメソッドの **3 ポイント** バージョンが呼び出されます。

```xpp
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

    void write()
    {
        info("(" + any2Str(x) + ", " + any2Str(y) + ")");
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

    void write()
    {
        info("(" + any2Str(x) + ", " + any2Str(y) + ", " + any2Str(z) + ")");
    }

}

// Code that creates Point objects and calls the write method.
Point point2 = new Point(1.0, 2.0);
Point point3 = new ThreePoint(3.0, 4.0, 5.0);

point2.write();
// Output is "(1.0, 2.0)".

point3.write();
// Output is "(3.0, 4.0, 5.0)".
```


### <a name="preventing-method-overrides"></a>メソッドのオーバーライドを禁止する

静的メソッドは、クラスごとに存在するため上書きすることはできません。 他の重要なメソッドやコア メソッドがオーバーライドされないようにするには、**final** 修飾子を使用します。 次の例では、**methodAtt** が **final** として宣言されているため、**属性** を拡張するクラスでオーバーライドできません **最終** に **新規** または **確定** のメソッドを指定しないでください。 

次の例は、**final** キーワードの使用方法を示しています。

```xpp
public class Attribute
{
    int objectVariable;

    final void methodAtt()
    {
        //Some statements
    }
}
```

### <a name="overriding-vs-overloading"></a>オーバーライドとオーバーロード

オーバーライドは、メソッドのスーパークラスの実装がそのメソッドのサブクラスの実装によって変更されるが、両方のメソッドのシグネチャが同じ場合に行われます。 

対照的に、*オーバーロード* は複数のメソッドが同じ名前を持つ場合に発生しますが、メソッドは異なるシグネチャ (戻り値の型、パラメーター リスト、または両方) を持ちます。 X++ はオーバーライドをサポートしますが、オーバーロードはサポートしていません。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

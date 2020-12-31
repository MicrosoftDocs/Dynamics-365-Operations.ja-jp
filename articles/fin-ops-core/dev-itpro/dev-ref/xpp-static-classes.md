---
title: X++ 静的クラス
description: このトピックでは、 X++ の静的クラスについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150303
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb0735a20985c3b1d2464231f50f202c34586f09
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408728"
---
# <a name="x-static-classes"></a>X++ 静的クラス

[!include [banner](../includes/banner.md)]

このトピックでは、 X++ の静的クラス メンバーについて説明します。 一般に、静的メソッドは次のような場合を対象とします。

-   このメソッドは、クラス内で宣言されているメンバー変数にアクセスする必要はありません。
-   このメソッドは、クラスのインスタンス (静的でない) メソッドを呼び出す理由はありません。

静的クラス メンバーを宣言するには、**静的** キーワードを使用します。 **静的** キーワードは、存在するクラスのインスタンス数に関係なく、メソッドの 1 つのインスタンスだけを作成するようシステムに指示します。 この 1 つのインスタンスは、セッション全体で使用されます。 

### <a name="static-methods"></a>静的メソッド

このセクションでは、違法コピーを防止するためにソフトウェア キー タイプを使用するシナリオについて説明します。 ソフトウェア キーの各インスタンスには、固有の値を持つことが可能です。 ただし、すべてのソフトウェア キーはソフトウェア キー設計のルールに準拠する必要があるため、ソフトウェア キーへの適合をテストするロジックはすべてのソフトウェア キーに対して同じです。 したがって、適合性検証ロジックを含むメソッドは静的でなければなりません。 

**静的** キーワード使用して宣言されるメソッドの例を次に示します。

```xpp
public class SoftwareKey
{
    static public boolean validateSoftwareKey(str _softwareKeyString)
    {
        // Your code here.
        return false;
    }
}
```

次の例では、クラスで静的メソッドを呼び出す前に **SoftwareKey** クラスのインスタンスを構築する必要はありません。 静的な **validateSoftwareKey** メソッドを呼び出すときは、構文はそのメソッドを含むクラスの名前で始まります。 コロンのペア (::) は、クラス名を静的メソッド名に接続するために使用します。

```xpp
boolean yourBool = SoftwareKey::validateSoftwareKey(yourSoftwareKeyString);
```

### <a name="static-fields"></a>静的フィールド

静的フィールドは、**静的** キーワードを使用して宣言される変数です。 概念的には、クラスに適用され、クラスのインスタンスには適用されません。

## <a name="static-constructors"></a>静的コンストラクター

静的コンストラクターは、静的またはインスタンス呼び出しがクラスに対して行われる前に実行されることが保証されます。 静的コンストラクターの実行は、ユーザーのセッションに対して相対的です。 静的コンストラクターには、次の構文があります。

```xpp
static void TypeNew()
```

静的コンストラクターは明示的に呼び出さないでください。 コンパイラは、コンストラクターがクラスの他のメソッドの前に正確に 1 回呼び出されるようにするコードを生成します。 静的コンストラクターは、任意の静的データを初期化したり、一度だけ実行する必要のある特定のアクションを実行するために使用されます。 静的コンストラクターに指定できるパラメーターはなく、**静的** としてマークする必要があります。 

次のコード例は、静的コンストラクターを使用して単一のインスタンスを作成する方法を示しています。

```xpp
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
```

単一は、クラスのインスタンスが 1 つしか呼び出されないことを保証します。 次の例は、単一をインスタンス化する方法を示しています。

```xpp
Singleton i = Singleton::Instance();
```

## <a name="static-methods"></a>静的メソッド

*クラス メソッド* とも呼ばれる静的メソッドは、クラスに属しており、キーワード **static** を使用して作成されます。 静的メソッドを使用する前に、オブジェクトのインスタンスを作成する必要はありません。 静的メソッドは多くの場合、テーブルに格納されているデータを操作するために使用します。 メンバー変数は静的メソッドで使用できません。 静的メソッドを呼び出すには、次の構文を使用します。

```xpp
ClassName::methodName();
```

## <a name="static-and-instance-methods"></a>静的およびインスタンス メソッド

メソッドのアクセサー キーワードは、どのメソッドが静的であるか、静的でないかに関係なく、同じクラスにある 2 つのメソッド間の呼び出しを制限することはありません。 静的メソッドでは、**新しい** コンストラクター メソッドが **プライベート** モディファイアーで修飾されている場合でも、**新しい** コンストラクター メソッドに対する呼び出しは有効です。 これらの呼び出しの構文では、**新しい** キーワードを使用する必要があります。 静的メソッドのコードは、クラスのインスタンス メソッドを呼び出す前に、独自のクラスのインスタンス オブジェクトを構築する必要があります。


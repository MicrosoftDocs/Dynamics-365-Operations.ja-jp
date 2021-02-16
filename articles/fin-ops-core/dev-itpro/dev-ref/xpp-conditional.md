---
title: X++ 条件付きステートメント
description: このトピックでは、X++の条件付きステートメントについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150213
ms.assetid: 16b30ff1-bb31-4f9d-8105-c73abd2455f6
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ab74d2c838243b897fc80bbd8646aa682e5b509
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408748"
---
# <a name="x-conditional-statements"></a>X++ 条件付きステートメント

[!include [banner](../includes/banner.md)]

このトピックでは、X++の条件付きステートメントについて説明します。 条件付きステートメントは、**if**、**if**...**else**、**switch**、および 3 項演算子 (**?**) です。 条件付きステートメントを使用して、コードのブロックを実行するかどうかを指定します。 異なる条件文は、異なる状況において利点を提供する。

## <a name="if-and-ifelse-statements"></a>if および if...else ステートメント

**if** ステートメントは、条件式を評価した後、条件式が **true** として評価された場合にステートメントまたは一連のステートメントを実行します。 **else** 句を使用すると、条件が **false** と評価される場合に実行される代替ステートメントまたは一連のステートメントを提供することができます。 **if**...**else** ステートメントの構文は次のとおりです。

**if (** *式* **)** *ステートメント* 
**\[else** *ステートメント* 
**\]**

この構文では、 どちらの *ステートメント* も複合ステートメント (中括弧で囲まれたステートメント) にすることができます。 かっこで囲まれた *式* (条件式) は、**true** または **false** として評価される有効な式にすることができます。 0 (ゼロ) を除くすべての番号は **true** です。 空でない文字列はすべて **true** です。 **if** ステートメントは入れ子にすることができます。 ただし、**if** ステートメントの入れ子が深すぎる場合、**switch** ステートメントを代わりに使用することを考慮する必要があります。

### <a name="examples-of-if-and-ifelse-statements"></a>if および if...else ステートメントの例

```xpp
// if statement
if (a > 4)
{
   info("a is greater than 4");
}

// if... else statement 
if (a > 4)
{
   info("a is greater than 4");
}
else
{
   info("a is less than or equal to 4");
}
```

## <a name="switch-statements"></a>switch ステートメント

**Switch** ステートメントは、ネストされた **if** と同じ動作をするマルチブランチ言語コンストラクトです。 **switch** ステートメントの式が評価され、それぞれの Case の値に対してチェックされます。 大文字と小文字の値は、コンパイラが評価できる定数でなければなりません。 

- ケース定数が **切り替え** 式と一致する場合、**case** ステートメントを実行します。 
- そのケースに **break** ステートメントが含まれている場合、プログラムはスイッチからジャンプ アウトします。 
- ケースに **break** ステートメントが含まれていない場合、プログラムは継続し、次の **ケース** ステートメントを実行します。 
- 一致が見つからない場合、**既定** ステートメントを実行します。 
- 一致するものがなく、**default** ステートメントがない場合、**switch** ステートメント内のステートメントは実行されません。 

**switch** ステートメントの構文を次に示します。

**switch** **(** *式* **)** **{** **{ ケース }** **\[既定:** *ステートメント* **\]** **}**

**case** ステートメントの構文は次のとおりです。

**case** *式* **{ 、** *式* **} :** *ステートメント*

**switch** ステートメントおよび **case** ステートメントの両方の構文で、 *ステートメント* があるごとに、かっこ ({}) でブロックを囲むことでステートメントのブロックを置き換えることができます。

### <a name="examples-of-switch-statements"></a>切り替え明細書の例

Switch ステートメントに **break** キーワードを含めると、case ブランチの実行は終了し、switch に続くステートメントが実行されます。 次の例のように、Debtor のアカウント番号が 1000 の場合、プログラムは "作業をする" が実行され、 switch ステートメントの後で実行が継続されます。

```xpp
switch (Debtor.AccountNo)
{
    case "1000":
        // do something
        break;
    case "2000":
        // do something else
        break;
    default:
        // default statement
        break;
}
```

次のコード例では、breakステートメントを省略して最初のcase 分岐から実行をドロップします。 Xが10の場合、bはaに割り当てられ、dはcに割り当てられます。 Xが11の場合、dはcに割り当てられます。 Xが12の場合、fはeに割り当てられます。

```xpp
 switch (x)
 {
     case 10:
         a = b;
     case 11:
         c = d;
         break;
     case 12:
         e = f;
         break;
 }
```

Break ステートメントを使用しない場合は、switch ステートメントのプログラム フローが次のケースに進みます。 コード セグメント AとBには同じ動作が設定されています。 

```xpp
// Code segment A (break omitted)
case 13:
case 17:
case 21:
case 500:
    info("g");
    break;

// Code segment B (the values are comma-delimited)
case 13, 17, 21, 500;
    info("g");
    break;
```

## <a name="ternary-operator-"></a>三項演算子 (?)

三項演算子 (**?**) は、2 つの式のうちの 1 つに解決される条件文です。 結果は、変数に割り当てることができます。 対照的に、**if** ステートメントはプログラム フローの条件付き分岐を提供しますが、変数に割り当てることはできません。 三項演算子の構文を次に示します:

*式1* **?** *式2* **:** *式3*

この構文では、*expression1* は **true** または **false** の値を返す必要があります。 *expression1* が **true** である場合、三項全体の明細書は *式* を返します。 それ以外の場合、ステートメントは *expression3* を返します。 *expression2* と *expression3* の両方は同じタイプである必要があります。

### <a name="examples-of-the-ternary-operator-"></a>三項演算子 (?) の例

次のコード例では、メソッド呼び出しからのブール値の戻り値に基づいて、2つの文字列のいずれかを返します。 ブール式は、CustTable テーブルに、RecIdフィールド値を1とする行が含まれているかどうかを示します。 このブール式が true (つまり、RecId! = 0) である場合は、found が結果に割り当てられます。 それ以外の場合、代替のnot foundが結果に割り当てられます。

```xpp
result = (custTable::find("1").RecId) ? "found" : "not found";
```

三項演算子を使用してステートメントをネストできます。 次の例では、 **x** の値に基づいて、3つの値のいずれかを **レベル** に割り当てます。

```xpp
int x = 1001;
str level = x <= 1000 ? "A" : (x <= 2000 ? "B" : "C");
info(level);
// Output is "B".
```

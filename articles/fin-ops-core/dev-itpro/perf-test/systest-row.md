---
title: 複数の値をテストする SysTestRow 属性
description: この記事では、SysTest 方法を使用して複数の値をテストできる SysTestRow 属性について説明します。
author: jorisdg
ms.date: 01/13/2022
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2022-01-13
ms.openlocfilehash: e57b57c41e7afc2668d507b3783180c94a451876
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854578"
---
# <a name="systestrow-attribute-for-testing-multiple-values"></a>複数の値をテストするための SysTestRow 属性

[!include [banner](../includes/banner.md)]


テストでは、同じ機能の複数の入力値をテストしなければならない場合があります。 トラブルシューティングとレポートを簡単に行う場合は、同じテスト方法で複数のテストを行うのを避ける必要があります。 複数のメソッドを作成する代わりに、SysTest フレームワークでサポートする **SysTestRow** 属性を使用できます。 この属性は、C\# の **DataRow** 属性と同様に動作します。

> [!NOTE]
> **SysTestRow** 属性は、バージョン 10.0.25 以降で使用できます。

## <a name="systestrow-example"></a>SysTestRow の例

この例では、数値を四角くする方法を作成します。

```xpp
public class MyMath
{
    public static int square(int _i)
    {
        return _i * _i;
    }
}
```

数種類の異なる数を使用して、この方法をテストします。 これらの数値の中には、機能する特殊なケースを含める必要があります。 したがって、**SysTestRow** 属性を使用して同じ方法の複数の値をテストする、テスト方法を次に示します。

```xpp
public class MathTests extends SysTestCase
{
    [SysTestMethod,
    SysTestRow(0,0),
    SysTestRow(1,1),
    SysTestRow(-1, 1),
    SysTestRow(4, 16),
    SysTestRow(-4, 16)]
    public void SquareTests(int _value, int _result)
    {
        int testResult = MyMath::square(_value);

        this.assertEquals(_result, testResult);
    }
}
```

Microsoft Visual Studio では、各テスト行が個別の番号付き結果として表示されます。

- `SquareTests#1`
- `SquareTests#2`
- `SquareTests#3`
- `SquareTests#4`
- `SquareTests#5`

## <a name="systestrowinactive"></a>SysTestRowInactive

すべての **SysTestRow** 属性は、**SysTestRowInactive** 属性で置き換えできます。 この場合、Visual Studio では、無効テストとしてテスト行が表示されます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

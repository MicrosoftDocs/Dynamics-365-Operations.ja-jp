---
title: 入力、テーブル、およびグリッド コントロール用のフォントと背景
description: このトピックでは、色を選択できるようにするための新しいカラー ピッカー コントロールについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 11/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 90513
ms.assetid: 84e06ee2-be1c-443b-b595-9309eaea84c5
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 659b38d5861a60618a359fcccf5799c79300a76f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688549"
---
# <a name="font-and-background-colors-for-input-table-and-grid-controls"></a>入力、テーブル、およびグリッド コントロール用のフォントと背景

[!include [banner](../includes/banner.md)]

このトピックでは、色を選択できるようにするための新しいカラー ピッカー コントロールについて説明します。

伝統的に、色はユーザーとコミュニケーションする理想的な方法と考えられてきました。 たとえば、赤色は、重要な情報へのユーザーの注意を引くためによく使用されます。 ただし、一部のユーザーは特定の色または色調を区別できず、一部のユーザーは視覚障害があります。 したがって、ユーザーに情報を伝達するために、色のみを使用することはお勧めしません。 代わりに、すべてのユーザーに情報を伝えるために、記号または追加のテキストとともに色を使用する必要があります。

## <a name="color-selection-in-dynamics-ax-2012"></a>Dynamics AX 2012 での色の選択
Microsoft Dynamics AX 2012 では、色の選択に次の特性がありました。

-   Win32 カラー ピッカーが使用されていました。
-   これには、RGB/10 進の変換に Win32 アプリケーション プログラミング インターフェイス (API) が必要でした。 (入力コントロールは RGB の 10 進値を受け入れました。)

```xpp
Public void lookup()
{
    #DEFINE.COLORVALUE(64)
    Int r,g,b
    container choosencolor;
    Binary customcolors = new Binary(#COLORVALUE);
    CCColor colorvalue;

    Super();

    [r,g,b] = WinAPI::RGBint2Con(this.backgroundColor());

    chosenColor = WinAPI::chooseColor(element.hWnd(),r,g,b, customColors, true);

    If(chosencolor)
    {
        [r, g, b] = chosencolor;
        Colorvalue = WinAPI::RGB2int(r,g,b);
        This.backgroundColor(colorValue);
        employeeWorkPlannerForm.parmAbsensceColor(colorvalue);
        Employeetable.columns(employeeworkplannerform.numberofcolumns());
        Absenscecolorparm = colorvalue;
    }
}
```

## <a name="color-selection-for-input-controls"></a>入力コントロールの色の選択
現在のバージョンでは、カラー ピッカー コントロールは標準コントロールの種類です。 カラー ピッカー コントロールは、フォームに直接配置することも、整数または文字列コントロールのカスタム ルックアップの一部として使用することもできます。 次の例は、カスタム ルックアップでカラー ピッカー コントロールとやり取りする方法を示しています。 ただし、フォームでカラー ピッカーを配置し、色を選択するためのボタンをユーザーに提供する場合、コードは似たものになります。

-   カラー ピッカー コントロールは、ユーザーが視覚的に色を選択したり RGB 値を指定できるように、フォームまたはカスタム ルックアップをホストすることができます。
-   戻り値は、入力コントロール プロパティに直接割り当てることができる 10 進数値です。 (ランタイム RGB 変換は必要ありません。)

```xpp
[Control("String")]
class stringControl
{
    /// <summary>
    ///
    /// </summary>

    public void lookup()
    {
        int color = hex2Int(this.valueStr());
        color = ColorSelection::selectColorStringControl(this, color);
        this.text(int2hex(color));
        this.backgroundColor(color);
    }
}

[Control("Integer")]
class integerControl
{
    /// <summary>
    ///
    /// </summary>
    public void lookup()
    {
        int color = this.value();
        color = ColorSelection::selectColor(this, color);
        this.value(color);
        this.backgroundColor(color);
    }
}
```

## <a name="using-color-in-a-table-control"></a>テーブル コントロールでの色の使用
入力コントロールの色付けにはデザイン時の操作はありません。 つまり、既定で「青」となるように入力コントロールをモデル化できません。 ただし、色の値を変更できるランタイム機能があります。 次の例は、テーブル コントロールのセルの色を変更する方法を示しています。

```xpp
public FormControl editControl(int column, int row)
{
    stringEdit.colorScheme(FormColorScheme::RGB);
    stringEdit.backgroundColor(WinAPI::RGB2int(225,225,125));
    stringEdit.foregroundColor(WinAPI::RGB2int(8,10,200));
}
```

[![色分けされたセルのあるテーブル コントロールの例](./media/tablecontrol_withcolor.png)](./media/tablecontrol_withcolor.png)

## <a name="using-color-in-a-grid-control"></a>グリッド コントロールでの色の使用

```xpp
public void displayOption(Common _record, FormRowDisplayOption _options)
{
    CLIParentTable table;
    table = _record;

    if(!cleared)
    {
        _options.affectedElementsByControl(CliParentTable_AInt.id());
        _options.affectedElementsByControl(CliParentTable_AEnum.id());
        _options.affectedElementsByControl(CliParentTable_AString.id());
        _options.affectedElementsByControl(CliParentTable_EditMethodString.id());

        if(table.AInt<=20)
        {
            _options.backColor(WinAPI::RGB2int(255,165,0));
        }
        else if( table.AInt>20 &&  table.AInt <60)
        {
            _options.backColor(WinAPI::RGB2int(255,255,0));
            _options.fontItalic(true);
            _options.textColor(WinAPI::RGB2int(255,0,127 ));
            _options.fontStrikethrough(true);
        }
        else
        {
            _options.backColor(WinAPI::RGB2int(128,0,128));
                _options.fontUnderline(true);
        }
    }

    super(_record, _options);
}
```

## <a name="static-rgb-instead-of-run-time-conversion-from-integer-to-rgb-values"></a>整数から RGB 値への実行時の変換ではなく静的 RGB
以前は、Win32 カラー ピッカーが RGB 値を返す一方、背景色 API が整数を受け入れていたため、**WinAPI::RGB2Int** を使用したランタイム変換が必要でした。 この新しいカラー ピッカーは、コントロールの整数の消費に合わせて整数を返すため、このランタイム変換は不要です。 また、.NET コードは、色に RGB 値を頻繁に使用すると理解されます。 したがって、そのような場合は、使用するたびにランタイム変換を行う必要はありません。 代わりに、静的色変数を定義することができます。 次に 3 つの例を挙げます。

```xpp
Static int GrayColor = 220 + 220 <<#offset8 + 220<<offset16;

Static int GrayColor = 0xdcdcdc

Static int GrayColor = 14474460; // DCDCDC or 220,220,220
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
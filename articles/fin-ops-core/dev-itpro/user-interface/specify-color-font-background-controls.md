---
title: 入力、テーブル、およびグリッド コントロール用のフォントと背景
description: このトピックでは、色を選択できるようにするための新しいカラー ピッカー コントロールについて説明します。
author: RobinARH
ms.date: 11/09/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 90513
ms.assetid: 84e06ee2-be1c-443b-b595-9309eaea84c5
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8bfe4b93ec81b1394832b60f688117820888a3c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744183"
---
# <a name="font-and-background-colors-for-input-table-and-grid-controls"></a><span data-ttu-id="43f61-103">入力、テーブル、およびグリッド コントロール用のフォントと背景</span><span class="sxs-lookup"><span data-stu-id="43f61-103">Font and background colors for input, table, and grid controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43f61-104">このトピックでは、色を選択できるようにするための新しいカラー ピッカー コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="43f61-104">This topic provides information about the new color picker control that lets users select a color.</span></span>

<span data-ttu-id="43f61-105">伝統的に、色はユーザーとコミュニケーションする理想的な方法と考えられてきました。</span><span class="sxs-lookup"><span data-stu-id="43f61-105">Traditionally, color has been considered an ideal way to communicate with a user.</span></span> <span data-ttu-id="43f61-106">たとえば、赤色は、重要な情報へのユーザーの注意を引くためによく使用されます。</span><span class="sxs-lookup"><span data-stu-id="43f61-106">For example, the color red is often used to draw the user's attention to information that is important.</span></span> <span data-ttu-id="43f61-107">ただし、一部のユーザーは特定の色または色調を区別できず、一部のユーザーは視覚障害があります。</span><span class="sxs-lookup"><span data-stu-id="43f61-107">However, some users can't distinguish certain colors or shades, and some users are blind.</span></span> <span data-ttu-id="43f61-108">したがって、ユーザーに情報を伝達するために、色のみを使用することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="43f61-108">Therefore, we don't recommend that you use color alone to communicate information to the user.</span></span> <span data-ttu-id="43f61-109">代わりに、すべてのユーザーに情報を伝えるために、記号または追加のテキストとともに色を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43f61-109">Instead, you should use color together with a symbol or additional text to convey information to all users.</span></span>

## <a name="color-selection-in-dynamics-ax-2012"></a><span data-ttu-id="43f61-110">Dynamics AX 2012 での色の選択</span><span class="sxs-lookup"><span data-stu-id="43f61-110">Color selection in Dynamics AX 2012</span></span>
<span data-ttu-id="43f61-111">Microsoft Dynamics AX 2012 では、色の選択に次の特性がありました。</span><span class="sxs-lookup"><span data-stu-id="43f61-111">In Microsoft Dynamics AX 2012, color selection had these characteristics:</span></span>

-   <span data-ttu-id="43f61-112">Win32 カラー ピッカーが使用されていました。</span><span class="sxs-lookup"><span data-stu-id="43f61-112">It used the Win32 color picker.</span></span>
-   <span data-ttu-id="43f61-113">これには、RGB/10 進の変換に Win32 アプリケーション プログラミング インターフェイス (API) が必要でした。</span><span class="sxs-lookup"><span data-stu-id="43f61-113">It required Win32 application programming interfaces (APIs) for RGB/decimal conversion.</span></span> <span data-ttu-id="43f61-114">(入力コントロールは RGB の 10 進値を受け入れました。)</span><span class="sxs-lookup"><span data-stu-id="43f61-114">(The input control accepted a decimal value for RGB.)</span></span>

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

## <a name="color-selection-for-input-controls"></a><span data-ttu-id="43f61-115">入力コントロールの色の選択</span><span class="sxs-lookup"><span data-stu-id="43f61-115">Color selection for input controls</span></span>
<span data-ttu-id="43f61-116">現在のバージョンでは、カラー ピッカー コントロールは標準コントロールの種類です。</span><span class="sxs-lookup"><span data-stu-id="43f61-116">In the current version, the color picker control is a standard control type.</span></span> <span data-ttu-id="43f61-117">カラー ピッカー コントロールは、フォームに直接配置することも、整数または文字列コントロールのカスタム ルックアップの一部として使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="43f61-117">The color picker control can be put directly in a form, or it can be used as part of a custom lookup for an integer or string control.</span></span> <span data-ttu-id="43f61-118">次の例は、カスタム ルックアップでカラー ピッカー コントロールとやり取りする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="43f61-118">The following example shows how to interact with the color picker control in a custom lookup.</span></span> <span data-ttu-id="43f61-119">ただし、フォームでカラー ピッカーを配置し、色を選択するためのボタンをユーザーに提供する場合、コードは似たものになります。</span><span class="sxs-lookup"><span data-stu-id="43f61-119">However, the code is similar if you put the color picker in a form and provide the user with a button to select a color.</span></span>

-   <span data-ttu-id="43f61-120">カラー ピッカー コントロールは、ユーザーが視覚的に色を選択したり RGB 値を指定できるように、フォームまたはカスタム ルックアップをホストすることができます。</span><span class="sxs-lookup"><span data-stu-id="43f61-120">A color picker control can be hosted in a form or a custom lookup to let the user visually pick a color or specify an RGB value.</span></span>
-   <span data-ttu-id="43f61-121">戻り値は、入力コントロール プロパティに直接割り当てることができる 10 進数値です。</span><span class="sxs-lookup"><span data-stu-id="43f61-121">The return value is a decimal value that can be assigned directly to an input control property.</span></span> <span data-ttu-id="43f61-122">(ランタイム RGB 変換は必要ありません。)</span><span class="sxs-lookup"><span data-stu-id="43f61-122">(No run-time RGB conversion is required.)</span></span>

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

## <a name="using-color-in-a-table-control"></a><span data-ttu-id="43f61-123">テーブル コントロールでの色の使用</span><span class="sxs-lookup"><span data-stu-id="43f61-123">Using color in a table control</span></span>
<span data-ttu-id="43f61-124">入力コントロールの色付けにはデザイン時の操作はありません。</span><span class="sxs-lookup"><span data-stu-id="43f61-124">There is no design-time experience for coloring input controls.</span></span> <span data-ttu-id="43f61-125">つまり、既定で「青」となるように入力コントロールをモデル化できません。</span><span class="sxs-lookup"><span data-stu-id="43f61-125">In other words, you can’t model an input control so that it's “blue” by default.</span></span> <span data-ttu-id="43f61-126">ただし、色の値を変更できるランタイム機能があります。</span><span class="sxs-lookup"><span data-stu-id="43f61-126">However, there are run-time capabilities that let you change color values.</span></span> <span data-ttu-id="43f61-127">次の例は、テーブル コントロールのセルの色を変更する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="43f61-127">The following example shows how you can change the way that the cells of a table control are colored.</span></span>

```xpp
public FormControl editControl(int column, int row)
{
    stringEdit.colorScheme(FormColorScheme::RGB);
    stringEdit.backgroundColor(WinAPI::RGB2int(225,225,125));
    stringEdit.foregroundColor(WinAPI::RGB2int(8,10,200));
}
```

<span data-ttu-id="43f61-128">[![色分けされたセルのあるテーブル コントロールの例](./media/tablecontrol_withcolor.png)](./media/tablecontrol_withcolor.png)</span><span class="sxs-lookup"><span data-stu-id="43f61-128">[![Example of a table control that has colored cells](./media/tablecontrol_withcolor.png)](./media/tablecontrol_withcolor.png)</span></span>

## <a name="using-color-in-a-grid-control"></a><span data-ttu-id="43f61-129">グリッド コントロールでの色の使用</span><span class="sxs-lookup"><span data-stu-id="43f61-129">Using color in a grid control</span></span>

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

## <a name="static-rgb-instead-of-run-time-conversion-from-integer-to-rgb-values"></a><span data-ttu-id="43f61-130">整数から RGB 値への実行時の変換ではなく静的 RGB</span><span class="sxs-lookup"><span data-stu-id="43f61-130">Static RGB instead of run-time conversion from integer to RGB values</span></span>
<span data-ttu-id="43f61-131">以前は、Win32 カラー ピッカーが RGB 値を返す一方、背景色 API が整数を受け入れていたため、**WinAPI::RGB2Int** を使用したランタイム変換が必要でした。</span><span class="sxs-lookup"><span data-stu-id="43f61-131">Previously, run-time conversion that used **WinAPI::RGB2Int** was required, because the Win32 color picker returned an RGB value, whereas the background color APIs accepted an integer.</span></span> <span data-ttu-id="43f61-132">この新しいカラー ピッカーは、コントロールの整数の消費に合わせて整数を返すため、このランタイム変換は不要です。</span><span class="sxs-lookup"><span data-stu-id="43f61-132">This run-time conversion isn't required, because the new color picker returns an integer to match the control's consumption of an integer.</span></span> <span data-ttu-id="43f61-133">また、.NET コードは、色に RGB 値を頻繁に使用すると理解されます。</span><span class="sxs-lookup"><span data-stu-id="43f61-133">Additionally, it’s understood that .NET code often uses RGB values for colors.</span></span> <span data-ttu-id="43f61-134">したがって、そのような場合は、使用するたびにランタイム変換を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="43f61-134">Therefore, in those cases, run-time conversion of colors isn't required for each use.</span></span> <span data-ttu-id="43f61-135">代わりに、静的色変数を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="43f61-135">Instead, you can define static color variables.</span></span> <span data-ttu-id="43f61-136">次に 3 つの例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="43f61-136">Here are three examples.</span></span>

```xpp
Static int GrayColor = 220 + 220 <<#offset8 + 220<<offset16;

Static int GrayColor = 0xdcdcdc

Static int GrayColor = 14474460; // DCDCDC or 220,220,220
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
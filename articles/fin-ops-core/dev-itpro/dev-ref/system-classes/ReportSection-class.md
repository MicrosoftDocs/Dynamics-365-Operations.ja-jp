---
title: ReportSection クラス
description: このトピックでは、ReportSection クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 900c5a2782429a67fb585216b75a160fdcce1b03
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502831"
---
# <a name="class-reportsection"></a>クラス ReportSection

[!include [banner](../../includes/banner.md)]

```xpp
class ReportSection extends TreeNode
```

ReportSection クラスには、レポート コントロールのコレクションが含まれています。

## <a name="remarks"></a>備考

セクションは、レポートのクエリが実行されたとき、またはレポートのメソッドが実行されたときに、レポートに印刷されます。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 レポート セクションは、プロローグ、ページ ヘッダー、ヘッダー、フッター、ページ フッター、エピローグ、プログラム可能なセクション、ヘッダー、本文またはフッターのいずれかを指定できます。 セクション テンプレート ノード タイプを使用すると、セクションを一度定義して、さまざまなレポートで何度も再利用できます。 この一般的な例は、小切手または振替です。

## <a name="examples"></a>例

次の例では、セクションをレポートに追加します。

```xpp
static void test(args a) 
{  
    report r; 
    reportDesign rd; 
    reportSection rs; 
    reportRun rr; 
    // Create a simple report that is not present in  
    // the Application Object Tree. 
    r = new report(); 
    rd = r.addDesign("myDesign"); 
    rs = rd.addProgrammableSection(1);  
    // Add a section triggered by execute(1). 
    rs.addTextControl("Hello world"); 
    // Run the report. 
    rr = new reportRun(r); 
    if (rr.prompt()) // Run the sysPrintForm form. 
    { 
        rr.execute(1); // Execute the programmableSection. 
        rr.print();   // Print report to the target 
                      // (for example, printer or screen) 
                      // selected during the previous prompt call. 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                       | 説明                                                                                                                               |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public ReportBitmapControl addBitmapControl()                                                | レポート セクションにビットマップ コントロールを追加します。                                                                                                |
| public ReportShapeControl addBoxControl(\[ShapeType type\])                                  | レポート セクションにシェイプ コントロールを追加します。                                                                                                 |
| public ReportControl addControl(TableId tableId, FieldId fieldId, \[int arrayIndex\])        | レポート セクションにレポート コントロールを追加します。                                                                                                |
| public ReportDateControl addDateControl(TableId tableId, FieldId fieldId)                    | レポート セクションにデータ コントロールを追加します。                                                                                                  |
| public ReportDateControl addDateDisplayControl(str displayFunc, \[TableId tableId\])         | レポート セクションにデータ コントロールを追加します。                                                                                                  |
| public ReportDateTimeControl addDateTimeControl(TableId tableId, FieldId fieldId)            |                                                                                                                                           |
| public ReportDateTimeControl addDateTimeDisplayControl(str displayFunc, \[TableId tableId\]) |                                                                                                                                           |
| public ReportControl addDisplayControl(str displayFunc, \[TableId tableId\])                 |                                                                                                                                           |
| public ReportEnumControl addEnumControl(TableId tableId, FieldId fieldId)                    |                                                                                                                                           |
| public ReportEnumControl addEnumDisplayControl(str displayFunc, \[TableId tableId\])         |                                                                                                                                           |
| public ReportFieldGroup addFieldGroup(TableId tableId, str name)                             |                                                                                                                                           |
| public ReportGuidControl addGuidControl(TableId tableId, FieldId fieldId)                    |                                                                                                                                           |
| public ReportGuidControl addGuidDisplayControl(str displayFunc, \[TableId tableId\])         |                                                                                                                                           |
| public ReportInt64Control addInt64Control(TableId tableId, FieldId fieldId)                  |                                                                                                                                           |
| public ReportInt64Control addInt64DisplayControl(str displayFunc, \[TableId tableId\])       |                                                                                                                                           |
| public ReportIntegerControl addIntegerControl(TableId tableId, FieldId fieldId)              |                                                                                                                                           |
| public ReportIntegerControl addIntegerDisplayControl(str displayFunc, \[TableId tableId\])   |                                                                                                                                           |
| public ReportPromptControl addPromptControl(TableId tableId, \[FieldId fieldId\])            |                                                                                                                                           |
| public ReportRealControl addRealControl(TableId tableId, FieldId fieldId)                    |                                                                                                                                           |
| public ReportRealControl addRealDisplayControl(str displayFunc, \[TableId tableId\])         |                                                                                                                                           |
| public ReportSectionGroup addSection(TableId tableId, \[FieldId fieldId\])                   |                                                                                                                                           |
| public ReportShapeControl addShapeControl(\[ShapeType type\])                                |                                                                                                                                           |
| public ReportStringControl addStringControl(TableId tableId, FieldId fieldId)                |                                                                                                                                           |
| public ReportStringControl addStringDisplayControl(str displayFunc, \[TableId tableId\])     |                                                                                                                                           |
| public ReportSumControl addSumControl(TableId tableId, FieldId fieldId)                      |                                                                                                                                           |
| public ReportSumControl addSumNameControl(str name)                                          |                                                                                                                                           |
| public ReportTextControl addTextControl(str text)                                            |                                                                                                                                           |
| public ReportTimeControl addTimeControl(TableId tableId, FieldId fieldId)                    |                                                                                                                                           |
| public ReportTimeControl addTimeDisplayControl(str displayFunc, \[TableId tableId\])         |                                                                                                                                           |
| public int arrange()                                                                         |                                                                                                                                           |
| public int arrangeMethod(\[int value\])                                                      |                                                                                                                                           |
| public int arrangeWhen(\[int value\])                                                        |                                                                                                                                           |
| public boolean autoDeclaration(\[boolean value\])                                            | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                        |
| public boolean autoHeader(\[boolean value\])                                                 |                                                                                                                                           |
| public int bold(\[int value\])                                                               | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                               |
| public int bottomMarginAndFrame()                                                            |                                                                                                                                           |
| public int bottomMarginMode(\[int value\])                                                   |                                                                                                                                           |
| public str bottomMarginStr(\[str value\])                                                    |                                                                                                                                           |
| public Units bottomMarginUnit(\[Units value\])                                               |                                                                                                                                           |
| public Real bottomMarginValue(\[Real value\])                                                |                                                                                                                                           |
| public int bottomMode(\[int value\])                                                         |                                                                                                                                           |
| public str bottomStr(\[str value\])                                                          |                                                                                                                                           |
| public Units bottomUnit(\[Units value\])                                                     |                                                                                                                                           |
| public Real bottomValue(\[Real value\])                                                      |                                                                                                                                           |
| public int characterSet(\[int value\])                                                       | フォントの文字セットを取得または設定します。                                                                                               |
| public int colorScheme(\[int value\])                                                        | コントロールの配色を取得または設定します。                                                                                             |
| public int columnHeadingsStrategy(\[int value\])                                             |                                                                                                                                           |
| public int columns(\[int value\], \[ColumnsMode mode\])                                      |                                                                                                                                           |
| public ColumnsMode columnsMode(\[ColumnsMode mode\])                                         |                                                                                                                                           |
| public int columnspaceMode(\[int value\])                                                    |                                                                                                                                           |
| public str columnspaceStr(\[str value\])                                                     |                                                                                                                                           |
| public Units columnspaceUnit(\[Units value\])                                                |                                                                                                                                           |
| public Real columnspaceValue(\[Real value\])                                                 |                                                                                                                                           |
| public int columnsValue(\[int value\])                                                       |                                                                                                                                           |
| public ReportControl control(FieldId fieldId, \[TableId tableId\])                           | コントロールのテーブルおよび dataField プロパティに基づいて、セクションのコントロールを検索します。                                                    |
| public int controlCount()                                                                    |                                                                                                                                           |
| public ReportControl controlName(str name)                                                   | コントロールの Name プロパティに基づいて、セクションのコントロールを検索します。                                                                       |
| public ReportControl controlNo(int number)                                                   |                                                                                                                                           |
| public int controlNumber(\[int value\])                                                      |                                                                                                                                           |
| public int delete()                                                                          | 現在のノードを AOT から削除します。                                                                                                    |
| public str font(\[str value\])                                                               | 使用するコントロールのフォントの名前を取得または設定します。                                                                                 |
| public int fontSize(\[int value\])                                                           | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                 |
| public str footerText(\[str value\])                                                         |                                                                                                                                           |
| public int foregroundColor(\[int value\])                                                    | 使用するコントロールのテキストの色を取得または設定します。                                                                                       |
| public boolean grandHeader(\[boolean value\])                                                |                                                                                                                                           |
| public boolean grandTotal(\[boolean value\])                                                 | FooterText プロパティ値が表示されるかどうかを決定します。                                                                        |
| public boolean hasButtons(\[boolean value\])                                                 |                                                                                                                                           |
| public int headerDetailLevel(\[int value\], \[AutoMode mode\])                               |                                                                                                                                           |
| public AutoMode headerDetailLevelMode(\[AutoMode mode\])                                     |                                                                                                                                           |
| public int headerDetailLevelValue(\[int value\])                                             |                                                                                                                                           |
| public str headerText(\[str value\])                                                         |                                                                                                                                           |
| public int height100mm(\[int height\])                                                       | 枠線および上下の余白の高さを除く、セクションの高さを取得または設定します。                                  |
| public int heightmm100(\[int heightInclMargins\])                                            | 枠線および上下の余白の高さを含む、セクションの高さを取得または設定します。                                  |
| public int heightMode(\[int value\])                                                         | コントロールの高さの計算方法を取得または設定します。                                                                            |
| public str heightStr(\[str value\])                                                          |                                                                                                                                           |
| public Units heightUnit(\[Units value\])                                                     |                                                                                                                                           |
| public Real heightValue(\[Real value\])                                                      | コントロールの高さを取得または設定します。                                                                                                   |
| public boolean italic(\[boolean value\])                                                     |                                                                                                                                           |
| public str label()                                                                           | AOT 内のセクション ノードの説明を取得します。                                                                                      |
| public int labelBottomMarginMode(\[int value\])                                              |                                                                                                                                           |
| public str labelBottomMarginStr(\[str value\])                                               |                                                                                                                                           |
| public Units labelBottomMarginUnit(\[Units value\])                                          |                                                                                                                                           |
| public Real labelBottomMarginValue(\[Real value\])                                           |                                                                                                                                           |
| public int labelTopMarginMode(\[int value\])                                                 |                                                                                                                                           |
| public str labelTopMarginStr(\[str value\])                                                  |                                                                                                                                           |
| public Units labelTopMarginUnit(\[Units value\])                                             |                                                                                                                                           |
| public Real labelTopMarginValue(\[Real value\])                                              |                                                                                                                                           |
| public int leftMarginMode(\[int value\])                                                     |                                                                                                                                           |
| public int leftMarginsEtc()                                                                  |                                                                                                                                           |
| public str leftMarginStr(\[str value\])                                                      |                                                                                                                                           |
| public Units leftMarginUnit(\[Units value\])                                                 |                                                                                                                                           |
| public Real leftMarginValue(\[Real value\])                                                  |                                                                                                                                           |
| public LineType lineAbove(\[LineType value\])                                                |                                                                                                                                           |
| public LineType lineBelow(\[LineType value\])                                                |                                                                                                                                           |
| public LineType lineLeft(\[LineType value\])                                                 | セクションの左枠として使用される明細行のタイプを取得または設定します。                                                               |
| public LineType lineRight(\[LineType value\])                                                |                                                                                                                                           |
| public TableId map(\[TableId value\])                                                        |                                                                                                                                           |
| public str name(\[str value\])                                                               | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int noOfHeadingLines(\[int value\], \[AutoMode mode\])                                |                                                                                                                                           |
| public AutoMode noOfHeadingLinesMode(\[AutoMode mode\])                                      |                                                                                                                                           |
| public int noOfHeadingLinesValue(\[int value\])                                              |                                                                                                                                           |
| public str resolutionX(\[str value\])                                                        |                                                                                                                                           |
| public int resolutionXStr(str value)                                                         |                                                                                                                                           |
| public Units resolutionXUnit(\[Units value\])                                                |                                                                                                                                           |
| public str resolutionY(\[str value\])                                                        |                                                                                                                                           |
| public int resolutionYStr(str value)                                                         |                                                                                                                                           |
| public Units resolutionYUnit(\[Units value\])                                                |                                                                                                                                           |
| public int rightMarginMode(\[int value\])                                                    |                                                                                                                                           |
| public int rightMarginsEtc()                                                                 |                                                                                                                                           |
| public str rightMarginStr(\[str value\])                                                     |                                                                                                                                           |
| public Units rightMarginUnit(\[Units value\])                                                |                                                                                                                                           |
| public Real rightMarginValue(\[Real value\])                                                 |                                                                                                                                           |
| public int ruler(\[int value\])                                                              |                                                                                                                                           |
| public ReportSectionGroup sectionGroup(TableId tableId, \[FieldId fieldId\])                 | 生成されたデザインで、既存のセクション グループを検索します。                                                                                  |
| public ReportBlockType sectionType()                                                         | ReportBlockType::Prolog、ReportBlockType::PageHeader、ReportBlockType::Body などの特定のレポート セクションのタイプを取得します。     |
| public int sumDetailLevel(\[int value\], \[AutoMode mode\])                                  |                                                                                                                                           |
| public AutoMode sumDetailLevelMode(\[AutoMode mode\])                                        |                                                                                                                                           |
| public int sumDetailLevelValue(\[int value\])                                                |                                                                                                                                           |
| public TableId table(\[TableId value\])                                                      | オブジェクトに関連付けられているテーブル ID を取得または設定します。                                                                                     |
| public LineThickness thickness(\[LineThickness value\])                                      |                                                                                                                                           |
| public int topMarginAndFrame()                                                               |                                                                                                                                           |
| public int topMarginMode(\[int value\])                                                      |                                                                                                                                           |
| public str topMarginStr(\[str value\])                                                       |                                                                                                                                           |
| public Units topMarginUnit(\[Units value\])                                                  |                                                                                                                                           |
| public Real topMarginValue(\[Real value\])                                                   |                                                                                                                                           |
| public int topMode(\[int value\])                                                            |                                                                                                                                           |
| public str topStr(\[str value\])                                                             |                                                                                                                                           |
| public Units topUnit(\[Units value\])                                                        |                                                                                                                                           |
| public Real topValue(\[Real value\])                                                         |                                                                                                                                           |
| public boolean underline(\[boolean value\])                                                  |                                                                                                                                           |
| public void columnspace(Real value, Units unit)                                              |                                                                                                                                           |
| public void bottom(Real value, Units unit)                                                   |                                                                                                                                           |
| public void labelBottomMargin(Real value, Units unit)                                        |                                                                                                                                           |
| public void labelTopMargin(Real value, Units unit)                                           |                                                                                                                                           |
| public void executeColumnHeadings()                                                          |                                                                                                                                           |
| public void executeSection()                                                                 | レポートにセクションを印刷します。                                                                                                         |
| public void rightMargin(Real value, Units unit)                                              |                                                                                                                                           |
| public void bottomMargin(Real value, Units unit)                                             |                                                                                                                                           |
| public void topMargin(Real value, Units unit)                                                |                                                                                                                                           |
| public void leftMargin(Real value, Units unit)                                               |                                                                                                                                           |
| public void top(Real value, Units unit)                                                      |                                                                                                                                           |
| public void height(Real value, Units unit)                                                   | コントロールの高さを取得または設定します。                                                                                                   |

## <a name="method-addbitmapcontrol"></a>メソッド addBitmapControl

レポート セクションにビットマップ コントロールを追加します。

```xpp
public ReportBitmapControl addBitmapControl()
```

### <a name="return-value---addbitmapcontrol"></a>戻り値 - addBitmapControl

ビットマップ コントロールが作成されます。

## <a name="method-addboxcontrol"></a>メソッド addBoxControl

レポート セクションにシェイプ コントロールを追加します。

```xpp
public ReportShapeControl addBoxControl([ShapeType type])
```

### <a name="parameters---addboxcontrol"></a>パラメーター - addBoxControl

タイプ  
追加するシェイプコントロールのタイプ (オプション)。

### <a name="return-value---addboxcontrol"></a>戻り値 - addBoxControl

作成されるシェイプ コントロール。

## <a name="method-addcontrol"></a>メソッド addControl

レポート セクションにレポート コントロールを追加します。

```xpp
public ReportControl addControl(TableId tableId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---addcontrol"></a>パラメーター - addControl

tableId  

<!-- -->

fieldId  

<!-- -->

arrayIndex  

### <a name="return-value---addcontrol"></a>戻り値 - addControl

作成されるレポート コントロール。

### <a name="remarks---addcontrol"></a>備考 - addControl

このメソッドは、引数で指定されたフィールドの型に応じて、文字列、列挙、整数、実数、日付など、指定したコントロールの種類を追加します。

## <a name="method-adddatecontrol"></a>メソッド addDateControl

レポート セクションにデータ コントロールを追加します。

```xpp
public ReportDateControl addDateControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---adddatecontrol"></a>パラメーター - addDateControl

tableId  
フィールド ID。

<!-- -->

fieldId  
フィールド ID。

### <a name="return-value---adddatecontrol"></a>戻り値 - addDateControl

日付コントロールが作成されます。

### <a name="examples---adddatecontrol"></a>例 - addDateControl

```xpp
static void test(args a) 
{ 
    reportRun rr; 
    inventTrans rec; 
    int i; 
    // Create a simple report that is not present in 
    // the Application Object Tree. 
    report r = new report(); 
    reportDesign rd = r.addDesign("myDesign"); 
    reportSection rs = rd.AddSection(reportBlockType::body,  
    tablenum(inventTrans)); 
    int t = tablenum(inventTrans); 
    int f; 
    f = fieldnum(inventTrans, datePhysical); 
    rs.addDateControl(t,f); 
    // run the report 
    rr = new reportRun(r); 
    // Run the sysPrintForm form. 
    if (rr.prompt())  
    { 
        while select rec 
            rr.send(rec); 
        // Print report to the target (e.g. printer or screen) selected during the  
        // prompt call above. 
        rr.print();  
    } 
}
```

## <a name="method-adddatedisplaycontrol"></a>メソッド addDateDisplayControl

レポート セクションにデータ コントロールを追加します。

```xpp
public ReportDateControl addDateDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---adddatedisplaycontrol"></a>パラメーター - addDateDisplayControl

displayFunc  
表示メソッドが宣言されているテーブルの名前 (オプション)。

<!-- -->

tableId  
表示メソッドが宣言されているテーブルの名前 (オプション)。

### <a name="return-value---adddatedisplaycontrol"></a>戻り値 - addDateDisplayControl

日付コントロールが作成されます。

### <a name="remarks---adddatedisplaycontrol"></a>備考 - addDateDisplayControl

データ コントロールは、表示メソッドが日付を返すときの結果を示します。

## <a name="method-adddatetimecontrol"></a>メソッド addDateTimeControl

```xpp
public ReportDateTimeControl addDateTimeControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---adddatetimecontrol"></a>パラメーター - addDateTimeControl

tableId  

<!-- -->

fieldId  

### <a name="return-value---adddatetimecontrol"></a>戻り値 - addDateTimeControl

## <a name="method-adddatetimedisplaycontrol"></a>メソッド addDateTimeDisplayControl

```xpp
public ReportDateTimeControl addDateTimeDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---adddatetimedisplaycontrol"></a>パラメーター - addDateTimeDisplayControl

displayFunc  

<!-- -->

tableId  

### <a name="return-value---adddatetimedisplaycontrol"></a>戻り値 - addDateTimeDisplayControl

## <a name="method-adddisplaycontrol"></a>メソッド addDisplayControl

```xpp
public ReportControl addDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---adddisplaycontrol"></a>パラメーター - addDisplayControl

displayFunc  

<!-- -->

tableId  

### <a name="return-value---adddisplaycontrol"></a>戻り値 - addDisplayControl

## <a name="method-addenumcontrol"></a>メソッド addEnumControl

```xpp
public ReportEnumControl addEnumControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addenumcontrol"></a>パラメーター - addEnumControl

tableId  

<!-- -->

fieldId  

### <a name="return-value---addenumcontrol"></a>戻り値 - addEnumControl

## <a name="method-addenumdisplaycontrol"></a>メソッド addEnumDisplayControl

```xpp
public ReportEnumControl addEnumDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addenumdisplaycontrol"></a>パラメーター - addEnumDisplayControl

displayFunc  

<!-- -->

tableId  

### <a name="return-value---addenumdisplaycontrol"></a>戻り値 - addEnumDisplayControl

## <a name="method-addfieldgroup"></a>メソッド addFieldGroup

```xpp
public ReportFieldGroup addFieldGroup(TableId tableId, str name)
```

### <a name="parameters---addfieldgroup"></a>パラメーター - addFieldGroup

tableId  

<!-- -->

名前  

### <a name="return-value---addfieldgroup"></a>戻り値 - addFieldGroup

## <a name="method-addguidcontrol"></a>メソッド addGuidControl

```xpp
public ReportGuidControl addGuidControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addguidcontrol"></a>パラメーター - addGuidControl

tableId  

<!-- -->

fieldId  

### <a name="return-value---addguidcontrol"></a>戻り値 - addGuidControl

## <a name="method-addguiddisplaycontrol"></a>メソッド addGuidDisplayControl

```xpp
public ReportGuidControl addGuidDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addguiddisplaycontrol"></a>パラメーター - addGuidDisplayControl

displayFunc  

<!-- -->

tableId  

### <a name="return-value---addguiddisplaycontrol"></a>戻り値 - addGuidDisplayControl

## <a name="method-addint64control"></a>メソッド addInt64Control

```xpp
public ReportInt64Control addInt64Control(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addint64control"></a>パラメーター - addInt64Control

tableId  

<!-- -->

fieldId  

### <a name="return-value---addint64control"></a>戻り値 - addInt64Control

## <a name="method-addint64displaycontrol"></a>メソッド addInt64DisplayControl

```xpp
public ReportInt64Control addInt64DisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addint64displaycontrol"></a>パラメーター - addInt64DisplayControl

displayFunc  

<!-- -->

tableId  

### <a name="return-value---addint64displaycontrol"></a>戻り値 - addInt64DisplayControl

## <a name="method-addintegercontrol"></a>メソッド addIntegerControl

```xpp
public ReportIntegerControl addIntegerControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addintegercontrol"></a>パラメーター - addIntegerControl

tableId  

<!-- -->

fieldId  

### <a name="return-value---addintegercontrol"></a>戻り値 - addIntegerControl

## <a name="method-addintegerdisplaycontrol"></a>メソッド addIntegerDisplayControl

```xpp
public ReportIntegerControl addIntegerDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addintegerdisplaycontrol"></a>パラメーター - addIntegerDisplayControl

displayFunc  

<!-- -->

tableId  

### <a name="return-value---addintegerdisplaycontrol"></a>戻り値 - addIntegerDisplayControl

## <a name="method-addpromptcontrol"></a>メソッド addPromptControl

```xpp
public ReportPromptControl addPromptControl(TableId tableId, [FieldId fieldId])
```

### <a name="parameters---addpromptcontrol"></a>パラメーター - addPromptControl

tableId  

<!-- -->

fieldId  

### <a name="return-value---addpromptcontrol"></a>戻り値 - addPromptControl

## <a name="method-addrealcontrol"></a>メソッド addRealControl

```xpp
public ReportRealControl addRealControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addrealcontrol"></a>パラメーター - addRealControl

tableId  

<!-- -->

fieldId  

### <a name="return-value---addrealcontrol"></a>戻り値 - addRealControl

## <a name="method-addrealdisplaycontrol"></a>メソッド addRealDisplayControl

```xpp
public ReportRealControl addRealDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addrealdisplaycontrol"></a>パラメーター - addRealDisplayControl

displayFunc  

<!-- -->

tableId  

### <a name="return-value---addrealdisplaycontrol"></a>戻り値 - addRealDisplayControl

## <a name="method-addsection"></a>メソッド addSection

```xpp
public ReportSectionGroup addSection(TableId tableId, [FieldId fieldId])
```

### <a name="parameters---addsection"></a>パラメーター - addSection

tableId  

<!-- -->

fieldId  

### <a name="return-value---addsection"></a>戻り値 - addSection

## <a name="method-addshapecontrol"></a>メソッド addShapeControl

```xpp
public ReportShapeControl addShapeControl([ShapeType type])
```

### <a name="parameters---addshapecontrol"></a>パラメーター - addShapeControl

タイプ  

### <a name="return-value---addshapecontrol"></a>戻り値 - addShapeControl

## <a name="method-addstringcontrol"></a>メソッド addStringControl

```xpp
public ReportStringControl addStringControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addstringcontrol"></a>パラメーター - addStringControl

tableId  

<!-- -->

fieldId  

### <a name="return-value---addstringcontrol"></a>戻り値 - addStringControl

## <a name="method-addstringdisplaycontrol"></a>メソッド addStringDisplayControl

```xpp
public ReportStringControl addStringDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addstringdisplaycontrol"></a>パラメーター - addStringDisplayControl

displayFunc  

<!-- -->

tableId  

### <a name="return-value---addstringdisplaycontrol"></a>戻り値 - addStringDisplayControl

## <a name="method-addsumcontrol"></a>メソッド addSumControl

```xpp
public ReportSumControl addSumControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addsumcontrol"></a>パラメーター - addSumControl

tableId  

<!-- -->

fieldId  

### <a name="return-value---addsumcontrol"></a>戻り値 - addSumControl

## <a name="method-addsumnamecontrol"></a>メソッド addSumNameControl

```xpp
public ReportSumControl addSumNameControl(str name)
```

### <a name="parameters---addsumnamecontrol"></a>パラメーター - addSumNameControl

名前  

### <a name="return-value---addsumnamecontrol"></a>戻り値 - addSumNameControl

## <a name="method-addtextcontrol"></a>メソッド addTextControl

```xpp
public ReportTextControl addTextControl(str text)
```

### <a name="parameters---addtextcontrol"></a>パラメーター - addTextControl

テキスト  

### <a name="return-value---addtextcontrol"></a>戻り値 - addTextControl

## <a name="method-addtimecontrol"></a>メソッド addTimeControl

```xpp
public ReportTimeControl addTimeControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addtimecontrol"></a>パラメーター - addTimeControl

tableId  

<!-- -->

fieldId  

### <a name="return-value---addtimecontrol"></a>戻り値 - addTimeControl

## <a name="method-addtimedisplaycontrol"></a>メソッド addTimeDisplayControl

```xpp
public ReportTimeControl addTimeDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addtimedisplaycontrol"></a>パラメーター - addTimeDisplayControl

displayFunc  

<!-- -->

tableId  

### <a name="return-value---addtimedisplaycontrol"></a>戻り値 - addTimeDisplayControl

## <a name="method-arrange"></a>メソッド arrange

```xpp
public int arrange()
```

### <a name="return-value---arrange"></a>戻り値 - arrange

## <a name="method-arrangemethod"></a>メソッド arrangeMethod

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a>パラメーター - arrangeMethod

値  

### <a name="return-value---arrangemethod"></a>戻り値 - arrangeMethod

## <a name="method-arrangewhen"></a>メソッド arrangeWhen

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a>パラメーター - arrangeWhen

値  

### <a name="return-value---arrangewhen"></a>戻り値 - arrangeWhen

## <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a>パラメーター - autoDeclaration

値  

### <a name="return-value---autodeclaration"></a>戻り値 - autoDeclaration

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

### <a name="remarks---autodeclaration"></a>備考 - autoDeclaration

コントロールには同じ名前を付けることはできません。

## <a name="method-autoheader"></a>メソッド autoHeader

```xpp
public boolean autoHeader([boolean value])
```

### <a name="parameters---autoheader"></a>パラメーター - autoHeader

値  

### <a name="return-value---autoheader"></a>戻り値 - autoHeader

## <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a>パラメーター - bold

値  

### <a name="return-value---bold"></a>戻り値 - bold

0 から 9 までの間の整数値。

### <a name="remarks---bold"></a>備考 - bold

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

## <a name="method-bottommarginandframe"></a>メソッド bottomMarginAndFrame

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a>戻り値 - bottomMarginAndFrame

## <a name="method-bottommarginmode"></a>メソッド bottomMarginMode

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a>パラメーター - bottomMarginMode

値  

### <a name="return-value---bottommarginmode"></a>戻り値 - bottomMarginMode

## <a name="method-bottommarginstr"></a>メソッド bottomMarginStr

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a>パラメーター - bottomMarginStr

値  

### <a name="return-value---bottommarginstr"></a>戻り値 - bottomMarginStr

## <a name="method-bottommarginunit"></a>メソッド bottomMarginUnit

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a>パラメーター - bottomMarginUnit

値  

### <a name="return-value---bottommarginunit"></a>戻り値 - bottomMarginUnit

## <a name="method-bottommarginvalue"></a>メソッド bottomMarginValue

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a>パラメーター - bottomMarginValue

値  

### <a name="return-value---bottommarginvalue"></a>戻り値 - bottomMarginValue

## <a name="method-bottommode"></a>メソッド bottomMode

```xpp
public int bottomMode([int value])
```

### <a name="parameters---bottommode"></a>パラメーター - bottomMode

値  

### <a name="return-value---bottommode"></a>戻り値 - bottomMode

## <a name="method-bottomstr"></a>メソッド bottomStr

```xpp
public str bottomStr([str value])
```

### <a name="parameters---bottomstr"></a>パラメーター - bottomStr

値  

### <a name="return-value---bottomstr"></a>戻り値 - bottomStr

## <a name="method-bottomunit"></a>メソッド bottomUnit

```xpp
public Units bottomUnit([Units value])
```

### <a name="parameters---bottomunit"></a>パラメーター - bottomUnit

値  

### <a name="return-value---bottomunit"></a>戻り値 - bottomUnit

## <a name="method-bottomvalue"></a>メソッド bottomValue

```xpp
public Real bottomValue([Real value])
```

### <a name="parameters---bottomvalue"></a>パラメーター - bottomValue

値  

### <a name="return-value---bottomvalue"></a>戻り値 - bottomValue

## <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a>パラメーター - characterSet

値  

### <a name="return-value---characterset"></a>戻り値 - characterSet

フォントの文字セット示す整数値。

### <a name="remarks---characterset"></a>備考 - characterSet

返される整数の値は、次のテーブルに従って文字セットを示します。

| 値です。 | 説明。         |
|--------|----------------------|
| 0      | ANSI\_CHARSET        |
| 1      | DEFAULT\_CHARSET     |
| 2      | SYMBOL\_CHARSET      |
| 77     | MAC\_CHARSET         |
| 128    | SHIFTJIS\_CHARSET    |
| 129    | HANGUL\_CHARSET      |
| 134    | GB2312\_CHARSET      |
| 136    | CHINESEBIG5\_CHARSET |
| 161    | GREEK\_CHARSET       |
| 162    | TURKISH\_CHARSET     |
| 163    | VIETNAMESE\_CHARSET  |
| 186    | BALTIC\_CHARSET      |
| 204    | RUSSIAN\_CHARSET     |
| 238    | EASTEUROPE\_CHARSET  |
| 255    | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 値です。 | 説明。   |
|--------|----------------|
| 130    | JOHAB\_CHARSET |

次のテーブルの値は、中東言語語版 Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

## <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a>パラメーター - colorScheme

値  

### <a name="return-value---colorscheme"></a>戻り値 - colorScheme

ゼロから 2 までの整数。

### <a name="remarks---colorscheme"></a>備考 - colorScheme

配色は次の表に従って定義されます。

| 値です。 | スタイル。                 |
|--------|------------------------|
| 0      | 既定。               |
| 1      | Windows パレット。   |
| 2      | 真の配色。 |

## <a name="method-columnheadingsstrategy"></a>メソッド columnHeadingsStrategy

```xpp
public int columnHeadingsStrategy([int value])
```

### <a name="parameters---columnheadingsstrategy"></a>パラメーター - columnHeadingsStrategy

値  

### <a name="return-value---columnheadingsstrategy"></a>戻り値 - columnHeadingsStrategy

## <a name="method-columns"></a>メソッド columns

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a>パラメーター - columns

値  

<!-- -->

モード  

### <a name="return-value---columns"></a>戻り値 - columns

## <a name="method-columnsmode"></a>メソッド columnsMode

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a>パラメーター - columnsMode

モード  

### <a name="return-value---columnsmode"></a>戻り値 - columnsMode

## <a name="method-columnspacemode"></a>メソッド columnspaceMode

```xpp
public int columnspaceMode([int value])
```

### <a name="parameters---columnspacemode"></a>パラメーター - columnspaceMode

値  

### <a name="return-value---columnspacemode"></a>戻り値 - columnspaceMode

## <a name="method-columnspacestr"></a>メソッド columnspaceStr

```xpp
public str columnspaceStr([str value])
```

### <a name="parameters---columnspacestr"></a>パラメーター - columnspaceStr

値  

### <a name="return-value---columnspacestr"></a>戻り値 - columnspaceStr

## <a name="method-columnspaceunit"></a>メソッド columnspaceUnit

```xpp
public Units columnspaceUnit([Units value])
```

### <a name="parameters---columnspaceunit"></a>パラメーター - columnspaceUnit

値  

### <a name="return-value---columnspaceunit"></a>戻り値 - columnspaceUnit

## <a name="method-columnspacevalue"></a>メソッド columnspaceValue

```xpp
public Real columnspaceValue([Real value])
```

### <a name="parameters---columnspacevalue"></a>パラメーター - columnspaceValue

値  

### <a name="return-value---columnspacevalue"></a>戻り値 - columnspaceValue

## <a name="method-columnsvalue"></a>メソッド columnsValue

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a>パラメーター - columnsValue

値  

### <a name="return-value---columnsvalue"></a>戻り値 - columnsValue

## <a name="method-control"></a>メソッド control

コントロールのテーブルおよび dataField プロパティに基づいて、セクションのコントロールを検索します。

```xpp
public ReportControl control(FieldId fieldId, [TableId tableId])
```

### <a name="parameters---control"></a>パラメーター - control

fieldId  
コントロールのテーブル プロパティ (オプション)。

<!-- -->

tableId  
コントロールのテーブル プロパティ (オプション)。

### <a name="return-value---control"></a>戻り値 - control

検索されるレポート コントロール。

### <a name="remarks---control"></a>備考 - control

テーブル ID が指定されていない場合は、セクションの親セクション グループからテーブル プロパティが使用されます。

## <a name="method-controlcount"></a>メソッド controlCount

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a>戻り値 - controlCount

## <a name="method-controlname"></a>メソッド controlName

コントロールの Name プロパティに基づいて、セクションのコントロールを検索します。

```xpp
public ReportControl controlName(str name)
```

### <a name="parameters---controlname"></a>パラメーター - controlName

名前  
コントロール Name プロパティ。

### <a name="return-value---controlname"></a>戻り値 - controlName

見つかったコントロール。

## <a name="method-controlno"></a>メソッド controlNo

```xpp
public ReportControl controlNo(int number)
```

### <a name="parameters---controlno"></a>パラメーター - controlNo

番号  

### <a name="return-value---controlno"></a>戻り値 - controlNo

## <a name="method-controlnumber"></a>メソッド controlNumber

```xpp
public int controlNumber([int value])
```

### <a name="parameters---controlnumber"></a>パラメーター - controlNumber

値  

### <a name="return-value---controlnumber"></a>戻り値 - controlNumber

## <a name="method-delete"></a>メソッド delete

現在のノードを AOT から削除します。

```xpp
public int delete()
```

### <a name="return-value---delete"></a>戻り値 - delete

## <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

```xpp
public str font([str value])
```

### <a name="parameters---font"></a>パラメーター - font

値  

### <a name="return-value---font"></a>戻り値 - font

Tahoma や Verdana など、使用するフォントの名前。

## <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a>パラメーター - fontSize

値  

### <a name="return-value---fontsize"></a>戻り値 - fontSize

ポイント単位のフォントの高さ。

## <a name="method-footertext"></a>メソッド footerText

```xpp
public str footerText([str value])
```

### <a name="parameters---footertext"></a>パラメーター - footerText

値  

### <a name="return-value---footertext"></a>戻り値 - footerText

## <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a>パラメーター - foregroundColor

値  

### <a name="return-value---foregroundcolor"></a>戻り値 - foregroundColor

パックされた RGB カラーを含む整数。

### <a name="remarks---foregroundcolor"></a>備考 - foregroundColor

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

## <a name="method-grandheader"></a>メソッド grandHeader

```xpp
public boolean grandHeader([boolean value])
```

### <a name="parameters---grandheader"></a>パラメーター - grandHeader

値  

### <a name="return-value---grandheader"></a>戻り値 - grandHeader

## <a name="method-grandtotal"></a>メソッド grandTotal

FooterText プロパティ値が表示されるかどうかを決定します。

```xpp
public boolean grandTotal([boolean value])
```

### <a name="parameters---grandtotal"></a>パラメーター - grandTotal

値  

### <a name="return-value---grandtotal"></a>戻り値 - grandTotal

FooterText プロパティ値が表示される場合は true。それ以外の場合は、false。

### <a name="remarks---grandtotal"></a>備考 - grandTotal

grandTotal プロパティは、レポートに複数のデータ ソースがネストされていない場合にのみ使用できます。

## <a name="method-hasbuttons"></a>メソッド hasButtons

```xpp
public boolean hasButtons([boolean value])
```

### <a name="parameters---hasbuttons"></a>パラメーター - hasButtons

値  

### <a name="return-value---hasbuttons"></a>戻り値 - hasButtons

## <a name="method-headerdetaillevel"></a>メソッド headerDetailLevel

```xpp
public int headerDetailLevel([int value], [AutoMode mode])
```

### <a name="parameters---headerdetaillevel"></a>パラメーター - headerDetailLevel

値  

<!-- -->

モード  

### <a name="return-value---headerdetaillevel"></a>戻り値 - headerDetailLevel

## <a name="method-headerdetaillevelmode"></a>メソッド headerDetailLevelMode

```xpp
public AutoMode headerDetailLevelMode([AutoMode mode])
```

### <a name="parameters---headerdetaillevelmode"></a>パラメーター - headerDetailLevelMode

モード  

### <a name="return-value---headerdetaillevelmode"></a>戻り値 - headerDetailLevelMode

## <a name="method-headerdetaillevelvalue"></a>メソッド headerDetailLevelValue

```xpp
public int headerDetailLevelValue([int value])
```

### <a name="parameters---headerdetaillevelvalue"></a>パラメーター - headerDetailLevelValue

値  

### <a name="return-value---headerdetaillevelvalue"></a>戻り値 - headerDetailLevelValue

## <a name="method-headertext"></a>メソッド headerText

```xpp
public str headerText([str value])
```

### <a name="parameters---headertext"></a>パラメーター - headerText

値  

### <a name="return-value---headertext"></a>戻り値 - headerText

## <a name="method-height100mm"></a>メソッド height100mm

枠線および上下の余白の高さを除く、セクションの高さを取得または設定します。

```xpp
public int height100mm([int height])
```

### <a name="parameters---height100mm"></a>パラメーター - height100mm

height  
1/100 mm の新しい値 (オプション)。

### <a name="return-value---height100mm"></a>戻り値 - height100mm

1/100 mm 単位の高さ。

### <a name="remarks---height100mm"></a>備考 - height100mm

このメソッドは、heightExclBorderAndMargins メソッドとして機能します。 返される高さは、height プロパティの値に対応します。 この関数を使用して height プロパティを設定する前に、height プロパティが AUTO に設定されていないことを確認してください。 それ以外の場合、組み込みロジックは、値を再計算する可能性があります。

## <a name="method-heightmm100"></a>メソッド heightmm100

枠線および上下の余白の高さを含む、セクションの高さを取得または設定します。

```xpp
public int heightmm100([int heightInclMargins])
```

### <a name="parameters---heightmm100"></a>パラメーター - heightmm100

heightInclMargins  
セクションの新しい合計高さ (1/100 mm) (オプション)。

### <a name="return-value---heightmm100"></a>戻り値 - heightmm100

1/100 mm 単位の高さ。

### <a name="remarks---heightmm100"></a>備考 - heightmm100

このメソッドは、heightInclBorderAndMargins メソッドとして機能します。 この関数を使用して height プロパティを設定する前に、height プロパティが AUTO に設定されていないことを確認してください。 それ以外の場合、組み込みロジックは、高さを設定する可能性があります。 Heightmm100 メソッドに 1000 が返される場合は、セクションの合計の高さは 10 mm になります。

## <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a>パラメーター - heightMode

値  

### <a name="return-value---heightmode"></a>戻り値 - heightMode

計算モード。

### <a name="remarks---heightmode"></a>備考 - heightMode

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

## <a name="method-heightstr"></a>メソッド heightStr

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a>パラメーター - heightStr

値  

### <a name="return-value---heightstr"></a>戻り値 - heightStr

## <a name="method-heightunit"></a>メソッド heightUnit

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a>パラメーター - heightUnit

値  

### <a name="return-value---heightunit"></a>戻り値 - heightUnit

## <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a>パラメーター - heightValue

値  

### <a name="return-value---heightvalue"></a>戻り値 - heightValue

ピクセル単位の高さ。

### <a name="remarks---heightvalue"></a>備考 - heightValue

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

## <a name="method-italic"></a>メソッド italic

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a>パラメーター - italic

値  

### <a name="return-value---italic"></a>戻り値 - italic

## <a name="method-label"></a>メソッド label

AOT 内のセクション ノードの説明を取得します。

```xpp
public str label()
```

### <a name="return-value---label"></a>戻り値 - label

セクション ノードの説明を含む文字列。

## <a name="method-labelbottommarginmode"></a>メソッド labelBottomMarginMode

```xpp
public int labelBottomMarginMode([int value])
```

### <a name="parameters---labelbottommarginmode"></a>パラメーター - labelBottomMarginMode

値  

### <a name="return-value---labelbottommarginmode"></a>戻り値 - labelBottomMarginMode

## <a name="method-labelbottommarginstr"></a>メソッド labelBottomMarginStr

```xpp
public str labelBottomMarginStr([str value])
```

### <a name="parameters---labelbottommarginstr"></a>パラメーター - labelBottomMarginStr

値  

### <a name="return-value---labelbottommarginstr"></a>戻り値 - labelBottomMarginStr

## <a name="method-labelbottommarginunit"></a>メソッド labelBottomMarginUnit

```xpp
public Units labelBottomMarginUnit([Units value])
```

### <a name="parameters---labelbottommarginunit"></a>パラメーター - labelBottomMarginUnit

値  

### <a name="return-value---labelbottommarginunit"></a>戻り値 - labelBottomMarginUnit

## <a name="method-labelbottommarginvalue"></a>メソッド labelBottomMarginValue

```xpp
public Real labelBottomMarginValue([Real value])
```

### <a name="parameters---labelbottommarginvalue"></a>パラメーター - labelBottomMarginValue

値  

### <a name="return-value---labelbottommarginvalue"></a>戻り値 - labelBottomMarginValue

## <a name="method-labeltopmarginmode"></a>メソッド labelTopMarginMode

```xpp
public int labelTopMarginMode([int value])
```

### <a name="parameters---labeltopmarginmode"></a>パラメーター - labelTopMarginMode

値  

### <a name="return-value---labeltopmarginmode"></a>戻り値 - labelTopMarginMode

## <a name="method-labeltopmarginstr"></a>メソッド labelTopMarginStr

```xpp
public str labelTopMarginStr([str value])
```

### <a name="parameters---labeltopmarginstr"></a>パラメーター - labelTopMarginStr

値  

### <a name="return-value---labeltopmarginstr"></a>戻り値 - labelTopMarginStr

## <a name="method-labeltopmarginunit"></a>メソッド labelTopMarginUnit

```xpp
public Units labelTopMarginUnit([Units value])
```

### <a name="parameters---labeltopmarginunit"></a>パラメーター - labelTopMarginUnit

値  

### <a name="return-value---labeltopmarginunit"></a>戻り値 - labelTopMarginUnit

## <a name="method-labeltopmarginvalue"></a>メソッド labelTopMarginValue

```xpp
public Real labelTopMarginValue([Real value])
```

### <a name="parameters---labeltopmarginvalue"></a>パラメーター - labelTopMarginValue

値  

### <a name="return-value---labeltopmarginvalue"></a>戻り値 - labelTopMarginValue

## <a name="method-leftmarginmode"></a>メソッド leftMarginMode

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a>パラメーター - leftMarginMode

値  

### <a name="return-value---leftmarginmode"></a>戻り値 - leftMarginMode

## <a name="method-leftmarginsetc"></a>メソッド leftMarginsEtc

```xpp
public int leftMarginsEtc()
```

### <a name="return-value---leftmarginsetc"></a>戻り値 - leftMarginsEtc

## <a name="method-leftmarginstr"></a>メソッド leftMarginStr

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a>パラメーター - leftMarginStr

値  

### <a name="return-value---leftmarginstr"></a>戻り値 - leftMarginStr

## <a name="method-leftmarginunit"></a>メソッド leftMarginUnit

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a>パラメーター - leftMarginUnit

値  

### <a name="return-value---leftmarginunit"></a>戻り値 - leftMarginStr

## <a name="method-leftmarginvalue"></a>メソッド leftMarginValue

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a>パラメーター - leftMarginValue

値  

### <a name="return-value---leftmarginvalue"></a>戻り値 - leftMarginValue

## <a name="method-lineabove"></a>メソッド lineAbove

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a>パラメーター - lineAbove

値  

### <a name="return-value---lineabove"></a>戻り値 - lineAbove

## <a name="method-linebelow"></a>メソッド lineBelow

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a>パラメーター - lineBelow

値  

### <a name="return-valu"></a>戻り値

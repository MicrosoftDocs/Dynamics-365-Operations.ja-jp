---
title: Report クラス
description: このトピックでは、Report クラスについて説明します。
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
ms.openlocfilehash: 05da263dd215d3bffdd602fc79728aa2235dd96c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502849"
---
# <a name="class-report"></a>クラス レポート

[!include [banner](../../includes/banner.md)]

```xpp
class Report extends TreeNode
```

Report クラスを使用すると、ユーザーは AOT ではなくコードを使用することにより、アプリケーション オブジェクト ツリー (AOT) とレポート作成に格納されているレポートを使用できます。

## <a name="remarks"></a>備考

レポート オブジェクトには、クエリと、ゼロかそれ以上のデザインが含まれます。 各デザインは、画面に表示または印刷が可能なレポートのレイアウトの定義です。 レポート オブジェクトには、上書きできる ReportRun メソッドもあります。 このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。

## <a name="examples"></a>例

次のコード例は、AOT には存在しないレポートを作成して実行します。

```xpp
static void test(args a) 
{ 
    report r; 
    reportDesign rd; 
    reportSection rs; 
    reportRun rr; 
    // Creates a simple report that is not present in  
    // the AOT. 
    r = new report(); 
    rd = r.addDesign("myDesign"); 
    // Adds a section that is triggered by execute(1). 
    rs = rd.addProgrammableSection(1);
    rs.addTextControl("Hello world"); 
    // Runs the report. 
    rr = new reportRun(r); 
    // Runs the SysPrintForm form. 
    if (rr.prompt())  
    { 
        // Executes the programmable section. 
        rr.execute(1);  
        // Prints the report to the target selected 
        // during the previous prompt call. 
        rr.print();    
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                              | 説明                                                                                                                               |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public ReportDesign addDesign(\[str name\], \[container buffer\])   | レポートが属している reportDesign を作成します。                                                                                          |
| public boolean allowCheck(\[boolean value\])                        |                                                                                                                                           |
| public boolean autoJoin(\[boolean value\])                          |                                                                                                                                           |
| public str changedBy(\[str value\])                                 | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])                             | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                             |
| public str changedTime(\[str value\])                               | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                             |
| public str createdBy(\[str value\])                                 | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public Date creationDate(\[Date value\])                            | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])                              |                                                                                                                                           |
| public ReportDesign design(\[str name\])                            | 既存のデザインを取得します。                                                                                                             |
| public int designCount()                                            | 特定のレポートのデザインの数を取得します。                                                                                        |
| public ReportDesign designNumber(\[int number\])                    | 既存のデザインを取得します。                                                                                                                  |
| public boolean interactive(\[boolean value\])                       |                                                                                                                                           |
| public str name(\[str value\])                                      | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                                  |                                                                                                                                           |
| public container pack()                                             | Report クラスの現在のインスタンスをシリアル化します。                                                                                      |
| public Query query(\[Query query\])                                 |                                                                                                                                           |
| public boolean saved()                                              | レポートがディスクに保存されたかどうかを示します。                                                                                      |
| public void new(\[AnyType nameOrContainer\], \[AnyType container\]) | TreeNode クラスの新しいインスタンスを初期化します。                                                                                         |
| public void dump()                                                  | レポートの内容の概要を情報ログに記述します。                                                                               |

## <a name="method-adddesign"></a>メソッド addDesign

レポートが属している reportDesign を作成します。

```xpp
public ReportDesign addDesign([str name], [container buffer])
```

### <a name="parameters---adddesign"></a>パラメーター - addDesign

名前  
デザインでバッファで指定されたコンテンツを準備します。

<!-- -->

バッファ  
デザインでバッファで指定されたコンテンツを準備します。

### <a name="return-value---adddesign"></a>戻り値 - addDesign

作成した reportDesign。

### <a name="remarks---adddesign"></a>備考 - addDesign

バッファ引数は、pack メソッドによって作成されたコンテナーにすることができます。

### <a name="examples---adddesign"></a>例 - addDesign

このジョブは、別のデザインのコピーであるデザインを生成するために addDesign を使用する方法を示しています。

```xpp
static void demoAddDesign(args a) 
{  
    report r1; 
    report r2; 
    reportDesign rd; 
    reportSection rs; 
    reportRun rr; 
    container c; 
    // Create a simple report r1. 
    r1 = new report(); 
    rd = r1.addDesign("Design1"); 
    rs = rd.addProgrammableSection(1); 
    rs.addTextControl("Hello world"); 
    c = rd.Pack(); // make a container containing r1's design 
    // Create a report r2 having a design that is a copy of r1's design. 
    r2 = new report(); 
    r2.AddDesign("design2", c); 
    // Run the report. 
    rr = new reportRun(r2, "design2"); 
    // Run the sysPrintForm form. 
    if (rr.prompt()) 
    { 
        // Execute the programableSection. 
        rr.execute(1);  
        // Print report to the target, such as printer or screen. 
        rr.print();    
    } 
}
```

## <a name="method-allowcheck"></a>メソッド allowCheck

```xpp
public boolean allowCheck([boolean value])
```

### <a name="parameters---allowcheck"></a>パラメーター - allowCheck

値  

### <a name="return-value---allowcheck"></a>戻り値 - allowCheck

## <a name="method-autojoin"></a>メソッド autoJoin

```xpp
public boolean autoJoin([boolean value])
```

### <a name="parameters---autojoin"></a>パラメーター - autoJoin

値  

### <a name="return-value---autojoin"></a>戻り値 - autoJoin

## <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  

### <a name="return-value---changedby"></a>戻り値 - changedBy

ユーザーの名前。

## <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  

### <a name="return-value---changeddate"></a>戻り値 - changedDate

アプリケーション オブジェクトが最後に変更された日付。

## <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  

### <a name="return-value---changedtime"></a>戻り値 - changedTime

アプリケーション オブジェクトが最後に変更された時間。

## <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a>パラメーター - createdBy

値  

### <a name="return-value---createdby"></a>戻り値 - createdBy

ユーザーの名前。

## <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a>パラメーター - creationDate

値  

### <a name="return-value---creationdate"></a>戻り値 - creationDate

アプリケーション オブジェクトが作成された日付。

## <a name="method-creationtime"></a>メソッド creationTime

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a>パラメーター - creationTime

値  

### <a name="return-value---creationtime"></a>戻り値 - creationTime

## <a name="method-design"></a>メソッド design

既存のデザインを取得します。

```xpp
public ReportDesign design([str name])
```

### <a name="parameters---design"></a>パラメーター - design

名前  
返されるレポートの名前 (オプション)。

### <a name="return-value---design"></a>戻り値 - design

指定した名前を持つデザイン、または見つからなかった場合は nullNothingnullptrunita null 参照 (Visual Basic にはない)。

### <a name="remarks---design"></a>備考 - design

引数が指定されず、レポートに 1 つのデザインのみ含まれている場合は、1 つのデザインを返します。

### <a name="examples---design"></a>例 - design

```xpp
static void testDesign(args a) 
{ 
    report r; 
    reportDesign rd; 
    r = new report("Cust"); 
    rd = r.Design(); 
    if (rd) 
        print "a) r.design() : ", rd.Name(); 
    rd = r.Design(""); 
    if (rd) 
        print "b) r.design(emptyString) : ", rd.Name(); 
    rd = r.Design('customer'); 
    if (rd) 
        print "c) r.design(customer) : ", rd.Name(); 
    pause; 
}
```

## <a name="method-designcount"></a>メソッド designCount

特定のレポートのデザインの数を取得します。

```xpp
public int designCount()
```

### <a name="return-value---designcount"></a>戻り値 - designCount

デザインの番号。

### <a name="examples---designcount"></a>例 - designCount

```xpp
static void testDesign(args a) 
{ 
    report r = new report(); 
    print "A newly created report has ", r.DesignCount(), " designs"; 
    pause; 
}
```

## <a name="method-designnumber"></a>メソッド designNumber

既存のデザインを取得します。

```xpp
public ReportDesign designNumber([int number])
```

### <a name="parameters---designnumber"></a>パラメーター - designNumber

番号  
希望するデザインを指定する整数。オプション。

### <a name="return-value---designnumber"></a>戻り値 - designNumber

指定した reportDesign、またはデザインが存在しない場合は nullNothingnullptrunita null 参照 (Visual Basic にはない)。

### <a name="remarks---designnumber"></a>備考 - designNumber

番号が &lt; 1 である場合は、デザイン 1 が返されます。

### <a name="examples---designnumber"></a>例 - designNumber

```xpp
void testDesign(args a) 
{ 
    report r; 
    reportDesign rd; 
    int i; 
    r = new report("myReport"); 
    if (r.DesignCount() == 0) 
    { 
        print "The report has no designs"; pause; 
    } 
    for (i=1; i<=r.DesignCount();i++) 
    { 
        rd = r.DesignNumber(i); 
        print "Design No. ", i, " has name ", rd.Name(); 
    } 
    pause; 
}
```

## <a name="method-interactive"></a>メソッド interactive

```xpp
public boolean interactive([boolean value])
```

### <a name="parameters---interactive"></a>パラメーター - interactive

値  

### <a name="return-value---interactive"></a>戻り値 - interactive

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-pack"></a>メソッド pack

Report クラスの現在のインスタンスをシリアル化します。

```xpp
public container pack()
```

### <a name="return-value---pack"></a>戻り値 - pack

Report クラスの現在のインスタンスを含むコンテナーです。

### <a name="remarks---pack"></a>備考 - pack

返されたコンテナーは、レポート コンストラクターの最初の引数として使用できます。

### <a name="examples---pack"></a>例 - pack

次の例では、「cust」という名前のレポートをコンテナーに格納し、そのコンテナーでレポートを実行します (AOT のコンテナではありません)。

```xpp
static void testReportPack(args a) 
{ 
    report r1; 
    report r2; 
    reportRun rr; 
    container c; 
    r1 = new report("cust"); 
    c = r1.Pack(); 
    r2 = new report(c); 
    rr = new reportrun(r2); 
    rr.Run(); 
}
```

## <a name="method-query"></a>メソッド query

```xpp
public Query query([Query query])
```

### <a name="parameters---query"></a>パラメーター - query

クエリ  

### <a name="return-value---query"></a>戻り値 - query

## <a name="method-saved"></a>メソッド saved

レポートがディスクに保存されたかどうかを示します。

```xpp
public boolean saved()
```

### <a name="return-value---saved"></a>戻り値 - saved

レコードがディスクに保存されている場合は true。それ以外の場合は、false。

### <a name="remarks---saved"></a>備考 - saved

AOT のレポートは、ディスクに保存されている場合にのみ実行できます。

### <a name="examples---saved"></a>例 - saved

```xpp
static void testReportSaved(args a) 
{ 
    report r; 
    reportRun rr; 
    r = new report(); 
    r.AddDesign(); 
    print "before save, saved : ", r.Saved(); pause; 
    r.saved(); 
    print "after save, saved : ", r.Saved(); pause; 
    rr = new reportrun(r); 
    rr.Run(); 
}
```

## <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

```xpp
public void new([AnyType nameOrContainer], [AnyType container])
```

### <a name="parameters---new"></a>パラメーター - new

nameOrContainer  

<!-- -->

コンテナー  

### <a name="remarks---new"></a>備考 - new

パラメーターの形式は次のとおりです。

-   () � AOT 内に存在しないレポート オブジェクトを作成します。
-   (c) � AOT には存在しないレポート オブジェクトを作成します。その内容はコンテナー c によって与えられます。
-   ("existingReportName") � AOT 内にあるレポート オブジェクトを取得します。
-   ("nonExistingReportName") � AOT 内でレポート オブジェクトを作成します。
-   ("nonExistingReportName", c) � AOT 内でレポート オブジェクトを作成します。内容はコンテナ c によって与えられます。

コンテナー c は、pack メソッドで作成する必要があります。

## <a name="method-dump"></a>メソッド dump

レポートの内容の概要を情報ログに記述します。

```xpp
public void dump()
```

### <a name="remarks---dump"></a>備考 - dump

情報ログに書き込まれる行は、AOT でレポートを展開するときに表示される情報と同じです。

### <a name="examples---dump"></a>例 - dump

```xpp
static void testReportDump(args a) 
{ 
    report r = new report("cust"); 
    r.Dump(); 
}
```


---
title: ReportAutoDesignSpecs クラス
description: このトピックでは、ReportAutoDesignSpecs クラスについて説明します。
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
ms.openlocfilehash: 59471ab8b56da13773ed6bf83ca9535ab9795193
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502847"
---
# <a name="class-reportautodesignspecs"></a>クラス ReportAutoDesignSpecs

[!include [banner](../../includes/banner.md)]

```xpp
class ReportAutoDesignSpecs extends TreeNode
```

ReportAutoDesignSpecs クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                            | 説明                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| public ReportSection addProgrammableSection(int number)                           |                                                                    |
| public ReportSection addSection(ReportBlockType sectionType, \[TableId tableId\]) |                                                                    |
| public boolean autoHeader(\[boolean value\])                                      |                                                                    |
| public str footerText(\[str value\])                                              |                                                                    |
| public boolean grandHeader(\[boolean value\])                                     |                                                                    |
| public boolean grandTotal(\[boolean value\])                                      | FooterText プロパティ値が表示されるかどうかを決定します。 |
| public str headerText(\[str value\])                                              |                                                                    |
| public boolean view()                                                             |                                                                    |

## <a name="method-addprogrammablesection"></a>メソッド addProgrammableSection

```xpp
public ReportSection addProgrammableSection(int number)
```

### <a name="parameters---addprogrammablesection"></a>パラメーター - addProgrammableSection

番号  

### <a name="return-value---addprogrammablesection"></a>戻り値 - addProgrammableSection

## <a name="method-addsection"></a>メソッド addSection

```xpp
public ReportSection addSection(ReportBlockType sectionType, [TableId tableId])
```

### <a name="parameters---addsection"></a>パラメーター - addSection

sectionType  

<!-- -->

tableId  

### <a name="return-value---addsection"></a>戻り値 - addSection

## <a name="method-autoheader"></a>メソッド autoHeader

```xpp
public boolean autoHeader([boolean value])
```

### <a name="parameters---autoheader"></a>パラメーター - autoHeader

値  

### <a name="return-value---autoheader"></a>戻り値 - autoHeader

## <a name="method-footertext"></a>メソッド footerText

```xpp
public str footerText([str value])
```

### <a name="parameters---footertext"></a>パラメーター - footerText

値  

### <a name="return-value---footertext"></a>戻り値 - footerText

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

grandTotal プロパティは、レポートに複数のデータ ソースがテストされていない場合にのみ使用できます。

## <a name="method-headertext"></a>メソッド headerText

```xpp
public str headerText([str value])
```

### <a name="parameters---headertext"></a>パラメーター - headerText

値  

### <a name="return-value---headertext"></a>戻り値 - headerText

## <a name="method-view"></a>メソッド view

```xpp
public boolean view()
```

### <a name="return-value---view"></a>戻り値 - view


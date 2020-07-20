---
title: SSRSReportConceptNode クラス
description: このトピックでは、SSRSReportConceptNode クラスについて説明します。
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
ms.openlocfilehash: 73a20aa8bc7704f0aa7887a63035450433feb724
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502820"
---
# <a name="class-ssrsreportconceptnode"></a>クラス SSRSReportConceptNode

[!include [banner](../../includes/banner.md)]

```xpp
class SSRSReportConceptNode extends xResourceNode
```

SSRSReportConceptNode クラスを使うと、アプリケーション オブジェクト ツリー (AOT) の SSRS レポート、データ ソース、スタイル テンプレート、イメージを作成、読み取り、更新、削除できます。

## <a name="remarks"></a>備考

ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------|
| public str AOTgetSource()                                  | このノードのソース コードを返します。                                         |
| public str getCrossReferences()                            | 指定した SSRSReportConceptNode オブジェクトによる相互参照を取得します。 |
| public void allowCaching(\[boolean allow\])                |                                                                               |
| public void setCrossReferences(str crossReferences)        | 指定した SSRSReportConceptNode オブジェクトによる相互参照を設定します。      |
| public void AOTsetSource(str source, \[boolean isStatic\]) | このノードのソース コードを設定します。                                            |

## <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a>戻り値 - AOTgetSource

ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

### <a name="remarks---aotgetsource"></a>備考 - AOTgetSource

この関数はソース コードを持つノードによってオーバーライドされます。

## <a name="method-getcrossreferences"></a>メソッド getCrossReferences

指定した SSRSReportConceptNode オブジェクトによる相互参照を取得します。

```xpp
public str getCrossReferences()
```

### <a name="return-value---getcrossreferences"></a>戻り値 - getCrossReferences

XML 形式 で指定した SSRSReportConceptNode オブジェクトによる相互参照。

## <a name="method-allowcaching"></a>メソッド allowCaching

```xpp
public void allowCaching([boolean allow])
```

### <a name="parameters---allowcaching"></a>パラメーター - allowCaching

allow  

## <a name="method-setcrossreferences"></a>メソッド setCrossReferences

指定した SSRSReportConceptNode オブジェクトによる相互参照を設定します。

```xpp
public void setCrossReferences(str crossReferences)
```

### <a name="parameters---setcrossreferences"></a>パラメーター - setCrossReferences

crossReferences  
XML 形式 で指定した SSRSReportConceptNode オブジェクトによる相互参照。

### <a name="remarks---setcrossreferences"></a>備考 - setCrossReferences

このメソッドは、指定された SSRSReportConceptNode オブジェクトに格納されている相互参照 XML のみを更新します。 相互参照システムは更新されません。

## <a name="method-aotsetsource"></a>メソッド AOTsetSource

このノードのソース コードを設定します。

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a>パラメーター - AOTsetSource

ソース  
メソッドが静的かどうかを指定する値 (オプション)。

<!-- -->

isStatic  
メソッドが静的かどうかを指定する値 (オプション)。

### <a name="remarks---aotsetsource"></a>備考 - AOTgetSource

このメソッドは、ソース コードを持つノードによって上書きされます。


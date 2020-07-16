---
title: SSRSReportDesignNode クラス
description: このトピックでは、SSRSReportDesignNode クラスについて説明します。
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
ms.openlocfilehash: b209a61c35dbb8751846fd6c78a5fe6e87ff1b98
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502819"
---
# <a name="class-ssrsreportdesignnode"></a>クラス SSRSReportDesignNode

[!include [banner](../../includes/banner.md)]

```xpp
class SSRSReportDesignNode extends xResourceNode
```

SSRSReportDesignNode クラスを使うと、アプリケーション オブジェクト ツリー (AOT) の Microsoft SQL Server Reporting Services レポート、データ ソース、スタイル テンプレート、イメージを作成、読み取り、更新、削除できます。

## <a name="remarks"></a>備考

ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                              | 説明                                                                  |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| public str getCrossReferences()                     | 指定した SSRSReportDesignNode オブジェクトによる相互参照を取得します。 |
| public void setCrossReferences(str crossReferences) | 指定した SSRSReportDesignNode オブジェクトによる相互参照を設定します。      |

## <a name="method-getcrossreferences"></a>メソッド getCrossReferences

指定した SSRSReportDesignNode オブジェクトによる相互参照を取得します。

```xpp
public str getCrossReferences()
```

### <a name="return-value---getcrossreferences"></a>戻り値 - getCrossReferences

XML 形式 で指定した SSRSReportDesignNode オブジェクトによる相互参照。

## <a name="method-setcrossreferences"></a>メソッド setCrossReferences

指定した SSRSReportDesignNode オブジェクトによる相互参照を設定します。

```xpp
public void setCrossReferences(str crossReferences)
```

### <a name="parameters---setcrossreferences"></a>パラメーター - setCrossReferences

crossReferences  
XML 形式 で指定した SSRSReportDesignNode オブジェクトによる相互参照。

### <a name="remarks---setcrossreferences"></a>備考 - setCrossReferences

このメソッドは、指定された SSRSReportDesignNode オブジェクトに格納されている相互参照 XML のみを更新します。 相互参照システムは更新されません。


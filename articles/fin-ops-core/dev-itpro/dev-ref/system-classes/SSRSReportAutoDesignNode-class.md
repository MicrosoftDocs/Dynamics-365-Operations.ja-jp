---
title: SSRSReportAutoDesignNode クラス
description: このトピックでは、SSRSReportAutoDesignNode クラスについて説明します。
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
ms.openlocfilehash: 9d4e5f11ad9c285dc2edb26fd669019c3f8fd03a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503006"
---
# <a name="class-ssrsreportautodesignnode"></a>クラス SSRSReportAutoDesignNode

[!include [banner](../../includes/banner.md)]

```xpp
class SSRSReportAutoDesignNode extends SSRSReportDesignNode
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                              | 説明                                                                        |
|-----------------------------------------------------|------------------------------------------------------------------------------------|
| public str getCrossReferences()                     | 指定した SSRSReportDesignNode オブジェクトを使用することで相互参照を取得します。 |
| public void setCrossReferences(str crossReferences) | 指定した SSRSReportDesignNode オブジェクトを使用して相互参照を設定します。      |

## <a name="method-getcrossreferences"></a>メソッド getCrossReferences

指定した SSRSReportDesignNode オブジェクトを使用することで相互参照を取得します。

```xpp
public str getCrossReferences()
```

### <a name="return-value---getcrossreferences"></a>戻り値 - getCrossReferences

XML 形式での相互参照。

## <a name="method-setcrossreferences"></a>メソッド setCrossReferences

指定した SSRSReportDesignNode オブジェクトを使用して相互参照を設定します。

```xpp
public void setCrossReferences(str crossReferences)
```

### <a name="parameters---setcrossreferences"></a>パラメーター - setCrossReferences

crossReferences  
XML 形式での相互参照。

### <a name="remarks---setcrossreferences"></a>備考 - setCrossReferences

このメソッドは、指定された SSRSReportDesignNode オブジェクトに格納されている相互参照 XML のみを更新します。 相互参照システムは更新されません。


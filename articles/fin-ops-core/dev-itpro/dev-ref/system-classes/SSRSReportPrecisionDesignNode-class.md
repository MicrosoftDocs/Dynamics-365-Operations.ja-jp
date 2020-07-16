---
title: SSRSReportPrecisionDesignNode クラス
description: このトピックでは、SSRSReportPrecisionDesignNode クラスについて説明します。
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
ms.openlocfilehash: f190ee46bd8ae6b07ef00adb99022b4b0a77f572
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502818"
---
# <a name="class-ssrsreportprecisiondesignnode"></a><span data-ttu-id="8e1cb-103">クラス SSRSReportPrecisionDesignNode</span><span class="sxs-lookup"><span data-stu-id="8e1cb-103">Class SSRSReportPrecisionDesignNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SSRSReportPrecisionDesignNode extends SSRSReportDesignNode
```

## <a name="remarks"></a><span data-ttu-id="8e1cb-104">備考</span><span class="sxs-lookup"><span data-stu-id="8e1cb-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="8e1cb-105">例</span><span class="sxs-lookup"><span data-stu-id="8e1cb-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="8e1cb-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="8e1cb-106">Methods</span></span>

| <span data-ttu-id="8e1cb-107">方法</span><span class="sxs-lookup"><span data-stu-id="8e1cb-107">Method</span></span>                                              | <span data-ttu-id="8e1cb-108">説明</span><span class="sxs-lookup"><span data-stu-id="8e1cb-108">Description</span></span>                                                                  |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8e1cb-109">public str getCrossReferences()</span><span class="sxs-lookup"><span data-stu-id="8e1cb-109">public str getCrossReferences()</span></span>                     | <span data-ttu-id="8e1cb-110">指定した SSRSReportDesignNode オブジェクトへの相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e1cb-110">Retrieves the cross-references to the specified SSRSReportDesignNode object.</span></span> |
| <span data-ttu-id="8e1cb-111">public void setCrossReferences(str crossReferences)</span><span class="sxs-lookup"><span data-stu-id="8e1cb-111">public void setCrossReferences(str crossReferences)</span></span> | <span data-ttu-id="8e1cb-112">指定した SSRSReportDesignNode オブジェクトに相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="8e1cb-112">Sets the cross-references to the specified SSRSReportDesignNode object.</span></span>      |

## <a name="method-getcrossreferences"></a><span data-ttu-id="8e1cb-113">メソッド getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="8e1cb-113">Method getCrossReferences</span></span>

<span data-ttu-id="8e1cb-114">指定した SSRSReportDesignNode オブジェクトへの相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e1cb-114">Retrieves the cross-references to the specified SSRSReportDesignNode object.</span></span>

```xpp
public str getCrossReferences()
```

### <a name="return-value---getcrossreferences"></a><span data-ttu-id="8e1cb-115">戻り値 - getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="8e1cb-115">Return Value - getCrossReferences</span></span>

<span data-ttu-id="8e1cb-116">XML 形式 で指定した SSRSReportDesignNode オブジェクトに対する相互参照。</span><span class="sxs-lookup"><span data-stu-id="8e1cb-116">The cross-references to the specified SSRSReportDesignNode object in XML format.</span></span>

## <a name="method-setcrossreferences"></a><span data-ttu-id="8e1cb-117">メソッド setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="8e1cb-117">Method setCrossReferences</span></span>

<span data-ttu-id="8e1cb-118">指定した SSRSReportDesignNode オブジェクトに相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="8e1cb-118">Sets the cross-references to the specified SSRSReportDesignNode object.</span></span>

```xpp
public void setCrossReferences(str crossReferences)
```

### <a name="parameters---setcrossreferences"></a><span data-ttu-id="8e1cb-119">パラメーター - setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="8e1cb-119">Parameters - setCrossReferences</span></span>

<span data-ttu-id="8e1cb-120">crossReferences</span><span class="sxs-lookup"><span data-stu-id="8e1cb-120">crossReferences</span></span>  
<span data-ttu-id="8e1cb-121">XML 形式 で指定した SSRSReportDesignNode オブジェクトに対する相互参照。</span><span class="sxs-lookup"><span data-stu-id="8e1cb-121">The cross-references to the specified SSRSReportDesignNode object in XML format.</span></span>

### <a name="remarks---setcrossreferences"></a><span data-ttu-id="8e1cb-122">備考 - setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="8e1cb-122">Remarks - setCrossReferences</span></span>

<span data-ttu-id="8e1cb-123">このメソッドは、指定された SSRSReportDesignNode オブジェクトに格納されている相互参照 XML のみを更新します。</span><span class="sxs-lookup"><span data-stu-id="8e1cb-123">This method only updates the cross-reference XML that is stored on the specified SSRSReportDesignNode object.</span></span> <span data-ttu-id="8e1cb-124">相互参照システムは更新されません。</span><span class="sxs-lookup"><span data-stu-id="8e1cb-124">It does not update the cross-reference system.</span></span>


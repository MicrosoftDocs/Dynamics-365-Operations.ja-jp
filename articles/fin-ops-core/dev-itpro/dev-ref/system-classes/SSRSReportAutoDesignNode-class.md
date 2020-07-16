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
# <a name="class-ssrsreportautodesignnode"></a><span data-ttu-id="3b926-103">クラス SSRSReportAutoDesignNode</span><span class="sxs-lookup"><span data-stu-id="3b926-103">Class SSRSReportAutoDesignNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SSRSReportAutoDesignNode extends SSRSReportDesignNode
```

## <a name="remarks"></a><span data-ttu-id="3b926-104">備考</span><span class="sxs-lookup"><span data-stu-id="3b926-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3b926-105">例</span><span class="sxs-lookup"><span data-stu-id="3b926-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3b926-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3b926-106">Methods</span></span>

| <span data-ttu-id="3b926-107">方法</span><span class="sxs-lookup"><span data-stu-id="3b926-107">Method</span></span>                                              | <span data-ttu-id="3b926-108">説明</span><span class="sxs-lookup"><span data-stu-id="3b926-108">Description</span></span>                                                                        |
|-----------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b926-109">public str getCrossReferences()</span><span class="sxs-lookup"><span data-stu-id="3b926-109">public str getCrossReferences()</span></span>                     | <span data-ttu-id="3b926-110">指定した SSRSReportDesignNode オブジェクトを使用することで相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="3b926-110">Retrieves the cross-references by using the specified SSRSReportDesignNode object.</span></span> |
| <span data-ttu-id="3b926-111">public void setCrossReferences(str crossReferences)</span><span class="sxs-lookup"><span data-stu-id="3b926-111">public void setCrossReferences(str crossReferences)</span></span> | <span data-ttu-id="3b926-112">指定した SSRSReportDesignNode オブジェクトを使用して相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="3b926-112">Sets the cross-references by using the specified SSRSReportDesignNode object.</span></span>      |

## <a name="method-getcrossreferences"></a><span data-ttu-id="3b926-113">メソッド getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="3b926-113">Method getCrossReferences</span></span>

<span data-ttu-id="3b926-114">指定した SSRSReportDesignNode オブジェクトを使用することで相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="3b926-114">Retrieves the cross-references by using the specified SSRSReportDesignNode object.</span></span>

```xpp
public str getCrossReferences()
```

### <a name="return-value---getcrossreferences"></a><span data-ttu-id="3b926-115">戻り値 - getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="3b926-115">Return Value - getCrossReferences</span></span>

<span data-ttu-id="3b926-116">XML 形式での相互参照。</span><span class="sxs-lookup"><span data-stu-id="3b926-116">The cross-references in XML format.</span></span>

## <a name="method-setcrossreferences"></a><span data-ttu-id="3b926-117">メソッド setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="3b926-117">Method setCrossReferences</span></span>

<span data-ttu-id="3b926-118">指定した SSRSReportDesignNode オブジェクトを使用して相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="3b926-118">Sets the cross-references by using the specified SSRSReportDesignNode object.</span></span>

```xpp
public void setCrossReferences(str crossReferences)
```

### <a name="parameters---setcrossreferences"></a><span data-ttu-id="3b926-119">パラメーター - setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="3b926-119">Parameters - setCrossReferences</span></span>

<span data-ttu-id="3b926-120">crossReferences</span><span class="sxs-lookup"><span data-stu-id="3b926-120">crossReferences</span></span>  
<span data-ttu-id="3b926-121">XML 形式での相互参照。</span><span class="sxs-lookup"><span data-stu-id="3b926-121">The cross-references in XML format.</span></span>

### <a name="remarks---setcrossreferences"></a><span data-ttu-id="3b926-122">備考 - setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="3b926-122">Remarks - setCrossReferences</span></span>

<span data-ttu-id="3b926-123">このメソッドは、指定された SSRSReportDesignNode オブジェクトに格納されている相互参照 XML のみを更新します。</span><span class="sxs-lookup"><span data-stu-id="3b926-123">This method only updates the cross-reference XML stored on the specified SSRSReportDesignNode object.</span></span> <span data-ttu-id="3b926-124">相互参照システムは更新されません。</span><span class="sxs-lookup"><span data-stu-id="3b926-124">It does not update the cross-reference system.</span></span>


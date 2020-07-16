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
# <a name="class-ssrsreportdesignnode"></a><span data-ttu-id="d8b11-103">クラス SSRSReportDesignNode</span><span class="sxs-lookup"><span data-stu-id="d8b11-103">Class SSRSReportDesignNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SSRSReportDesignNode extends xResourceNode
```

<span data-ttu-id="d8b11-104">SSRSReportDesignNode クラスを使うと、アプリケーション オブジェクト ツリー (AOT) の Microsoft SQL Server Reporting Services レポート、データ ソース、スタイル テンプレート、イメージを作成、読み取り、更新、削除できます。</span><span class="sxs-lookup"><span data-stu-id="d8b11-104">The SSRSReportDesignNode class lets you create, read, update, and delete Microsoft SQL Server Reporting Services reports, data sources, style templates, and images in the  Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8b11-105">備考</span><span class="sxs-lookup"><span data-stu-id="d8b11-105">Remarks</span></span>

<span data-ttu-id="d8b11-106">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d8b11-106">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

## <a name="examples"></a><span data-ttu-id="d8b11-107">例</span><span class="sxs-lookup"><span data-stu-id="d8b11-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="d8b11-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="d8b11-108">Methods</span></span>

| <span data-ttu-id="d8b11-109">方法</span><span class="sxs-lookup"><span data-stu-id="d8b11-109">Method</span></span>                                              | <span data-ttu-id="d8b11-110">説明</span><span class="sxs-lookup"><span data-stu-id="d8b11-110">Description</span></span>                                                                  |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d8b11-111">public str getCrossReferences()</span><span class="sxs-lookup"><span data-stu-id="d8b11-111">public str getCrossReferences()</span></span>                     | <span data-ttu-id="d8b11-112">指定した SSRSReportDesignNode オブジェクトによる相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="d8b11-112">Retrieves the cross-references by the specified SSRSReportDesignNode object.</span></span> |
| <span data-ttu-id="d8b11-113">public void setCrossReferences(str crossReferences)</span><span class="sxs-lookup"><span data-stu-id="d8b11-113">public void setCrossReferences(str crossReferences)</span></span> | <span data-ttu-id="d8b11-114">指定した SSRSReportDesignNode オブジェクトによる相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="d8b11-114">Sets the cross-references by the specified SSRSReportDesignNode object.</span></span>      |

## <a name="method-getcrossreferences"></a><span data-ttu-id="d8b11-115">メソッド getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="d8b11-115">Method getCrossReferences</span></span>

<span data-ttu-id="d8b11-116">指定した SSRSReportDesignNode オブジェクトによる相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="d8b11-116">Retrieves the cross-references by the specified SSRSReportDesignNode object.</span></span>

```xpp
public str getCrossReferences()
```

### <a name="return-value---getcrossreferences"></a><span data-ttu-id="d8b11-117">戻り値 - getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="d8b11-117">Return Value - getCrossReferences</span></span>

<span data-ttu-id="d8b11-118">XML 形式 で指定した SSRSReportDesignNode オブジェクトによる相互参照。</span><span class="sxs-lookup"><span data-stu-id="d8b11-118">The cross-references by the specified SSRSReportDesignNode object in XML format.</span></span>

## <a name="method-setcrossreferences"></a><span data-ttu-id="d8b11-119">メソッド setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="d8b11-119">Method setCrossReferences</span></span>

<span data-ttu-id="d8b11-120">指定した SSRSReportDesignNode オブジェクトによる相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="d8b11-120">Sets the cross-references by the specified SSRSReportDesignNode object.</span></span>

```xpp
public void setCrossReferences(str crossReferences)
```

### <a name="parameters---setcrossreferences"></a><span data-ttu-id="d8b11-121">パラメーター - setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="d8b11-121">Parameters - setCrossReferences</span></span>

<span data-ttu-id="d8b11-122">crossReferences</span><span class="sxs-lookup"><span data-stu-id="d8b11-122">crossReferences</span></span>  
<span data-ttu-id="d8b11-123">XML 形式 で指定した SSRSReportDesignNode オブジェクトによる相互参照。</span><span class="sxs-lookup"><span data-stu-id="d8b11-123">The cross-references by the specified SSRSReportDesignNode object in XML format.</span></span>

### <a name="remarks---setcrossreferences"></a><span data-ttu-id="d8b11-124">備考 - setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="d8b11-124">Remarks - setCrossReferences</span></span>

<span data-ttu-id="d8b11-125">このメソッドは、指定された SSRSReportDesignNode オブジェクトに格納されている相互参照 XML のみを更新します。</span><span class="sxs-lookup"><span data-stu-id="d8b11-125">This method only updates the cross-reference XML stored on the specified SSRSReportDesignNode object.</span></span> <span data-ttu-id="d8b11-126">相互参照システムは更新されません。</span><span class="sxs-lookup"><span data-stu-id="d8b11-126">It does not update the cross-reference system.</span></span>


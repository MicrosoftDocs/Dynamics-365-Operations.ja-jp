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
# <a name="class-ssrsreportconceptnode"></a><span data-ttu-id="bca05-103">クラス SSRSReportConceptNode</span><span class="sxs-lookup"><span data-stu-id="bca05-103">Class SSRSReportConceptNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SSRSReportConceptNode extends xResourceNode
```

<span data-ttu-id="bca05-104">SSRSReportConceptNode クラスを使うと、アプリケーション オブジェクト ツリー (AOT) の SSRS レポート、データ ソース、スタイル テンプレート、イメージを作成、読み取り、更新、削除できます。</span><span class="sxs-lookup"><span data-stu-id="bca05-104">The SSRSReportConceptNode class lets you create, read, update, and delete SSRS reports, data sources, style templates, and images in the  Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="bca05-105">備考</span><span class="sxs-lookup"><span data-stu-id="bca05-105">Remarks</span></span>

<span data-ttu-id="bca05-106">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bca05-106">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

## <a name="examples"></a><span data-ttu-id="bca05-107">例</span><span class="sxs-lookup"><span data-stu-id="bca05-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="bca05-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="bca05-108">Methods</span></span>

| <span data-ttu-id="bca05-109">方法</span><span class="sxs-lookup"><span data-stu-id="bca05-109">Method</span></span>                                                     | <span data-ttu-id="bca05-110">説明</span><span class="sxs-lookup"><span data-stu-id="bca05-110">Description</span></span>                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="bca05-111">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="bca05-111">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="bca05-112">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="bca05-112">Returns the source code of this node.</span></span>                                         |
| <span data-ttu-id="bca05-113">public str getCrossReferences()</span><span class="sxs-lookup"><span data-stu-id="bca05-113">public str getCrossReferences()</span></span>                            | <span data-ttu-id="bca05-114">指定した SSRSReportConceptNode オブジェクトによる相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="bca05-114">Retrieves the cross-references by the specified SSRSReportConceptNode object.</span></span> |
| <span data-ttu-id="bca05-115">public void allowCaching(\[boolean allow\])</span><span class="sxs-lookup"><span data-stu-id="bca05-115">public void allowCaching(\[boolean allow\])</span></span>                |                                                                               |
| <span data-ttu-id="bca05-116">public void setCrossReferences(str crossReferences)</span><span class="sxs-lookup"><span data-stu-id="bca05-116">public void setCrossReferences(str crossReferences)</span></span>        | <span data-ttu-id="bca05-117">指定した SSRSReportConceptNode オブジェクトによる相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="bca05-117">Sets the cross-references by the specified SSRSReportConceptNode object.</span></span>      |
| <span data-ttu-id="bca05-118">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="bca05-118">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="bca05-119">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="bca05-119">Sets the source code of this node.</span></span>                                            |

## <a name="method-aotgetsource"></a><span data-ttu-id="bca05-120">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="bca05-120">Method AOTgetSource</span></span>

<span data-ttu-id="bca05-121">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="bca05-121">Returns the source code of this node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="bca05-122">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="bca05-122">Return Value - AOTgetSource</span></span>

<span data-ttu-id="bca05-123">ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="bca05-123">The string that contains the source code, if any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---aotgetsource"></a><span data-ttu-id="bca05-124">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="bca05-124">Remarks - AOTgetSource</span></span>

<span data-ttu-id="bca05-125">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="bca05-125">This function is overridden by nodes that have source code.</span></span>

## <a name="method-getcrossreferences"></a><span data-ttu-id="bca05-126">メソッド getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="bca05-126">Method getCrossReferences</span></span>

<span data-ttu-id="bca05-127">指定した SSRSReportConceptNode オブジェクトによる相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="bca05-127">Retrieves the cross-references by the specified SSRSReportConceptNode object.</span></span>

```xpp
public str getCrossReferences()
```

### <a name="return-value---getcrossreferences"></a><span data-ttu-id="bca05-128">戻り値 - getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="bca05-128">Return Value - getCrossReferences</span></span>

<span data-ttu-id="bca05-129">XML 形式 で指定した SSRSReportConceptNode オブジェクトによる相互参照。</span><span class="sxs-lookup"><span data-stu-id="bca05-129">The cross-references by the specified SSRSReportConceptNode object in XML format.</span></span>

## <a name="method-allowcaching"></a><span data-ttu-id="bca05-130">メソッド allowCaching</span><span class="sxs-lookup"><span data-stu-id="bca05-130">Method allowCaching</span></span>

```xpp
public void allowCaching([boolean allow])
```

### <a name="parameters---allowcaching"></a><span data-ttu-id="bca05-131">パラメーター - allowCaching</span><span class="sxs-lookup"><span data-stu-id="bca05-131">Parameters - allowCaching</span></span>

<span data-ttu-id="bca05-132">allow</span><span class="sxs-lookup"><span data-stu-id="bca05-132">allow</span></span>  

## <a name="method-setcrossreferences"></a><span data-ttu-id="bca05-133">メソッド setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="bca05-133">Method setCrossReferences</span></span>

<span data-ttu-id="bca05-134">指定した SSRSReportConceptNode オブジェクトによる相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="bca05-134">Sets the cross-references by the specified SSRSReportConceptNode object.</span></span>

```xpp
public void setCrossReferences(str crossReferences)
```

### <a name="parameters---setcrossreferences"></a><span data-ttu-id="bca05-135">パラメーター - setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="bca05-135">Parameters - setCrossReferences</span></span>

<span data-ttu-id="bca05-136">crossReferences</span><span class="sxs-lookup"><span data-stu-id="bca05-136">crossReferences</span></span>  
<span data-ttu-id="bca05-137">XML 形式 で指定した SSRSReportConceptNode オブジェクトによる相互参照。</span><span class="sxs-lookup"><span data-stu-id="bca05-137">The cross-references by the specified SSRSReportConceptNode object in XML format.</span></span>

### <a name="remarks---setcrossreferences"></a><span data-ttu-id="bca05-138">備考 - setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="bca05-138">Remarks - setCrossReferences</span></span>

<span data-ttu-id="bca05-139">このメソッドは、指定された SSRSReportConceptNode オブジェクトに格納されている相互参照 XML のみを更新します。</span><span class="sxs-lookup"><span data-stu-id="bca05-139">This method only updates the cross-reference XML stored on the specified SSRSReportConceptNode object.</span></span> <span data-ttu-id="bca05-140">相互参照システムは更新されません。</span><span class="sxs-lookup"><span data-stu-id="bca05-140">It does not update the cross-reference system.</span></span>

## <a name="method-aotsetsource"></a><span data-ttu-id="bca05-141">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="bca05-141">Method AOTsetSource</span></span>

<span data-ttu-id="bca05-142">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="bca05-142">Sets the source code of this node.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="bca05-143">パラメーター - AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="bca05-143">Parameters - AOTsetSource</span></span>

<span data-ttu-id="bca05-144">ソース</span><span class="sxs-lookup"><span data-stu-id="bca05-144">source</span></span>  
<span data-ttu-id="bca05-145">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="bca05-145">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="bca05-146">isStatic</span><span class="sxs-lookup"><span data-stu-id="bca05-146">isStatic</span></span>  
<span data-ttu-id="bca05-147">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="bca05-147">The value that specifies whether the method is static; optional.</span></span>

### <a name="remarks---aotsetsource"></a><span data-ttu-id="bca05-148">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="bca05-148">Remarks - AOTsetSource</span></span>

<span data-ttu-id="bca05-149">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="bca05-149">This method is overridden by nodes that have source code.</span></span>


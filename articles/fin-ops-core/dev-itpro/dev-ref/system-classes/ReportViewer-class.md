---
title: ReportViewer クラス
description: このトピックでは、ReportViewer クラスについて説明します。
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
ms.openlocfilehash: 2662b9622e6f8d5cf92e57d0cf193ea81abf1f21
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502824"
---
# <a name="class-reportviewer"></a><span data-ttu-id="87541-103">クラス ReportViewer</span><span class="sxs-lookup"><span data-stu-id="87541-103">Class ReportViewer</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportViewer extends ReportOutput
```

<span data-ttu-id="87541-104">ReportViewer クラスを使用すると、ユーザーがレポートをプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="87541-104">The ReportViewer class lets the user preview a report.</span></span>

## <a name="remarks"></a><span data-ttu-id="87541-105">備考</span><span class="sxs-lookup"><span data-stu-id="87541-105">Remarks</span></span>

<span data-ttu-id="87541-106">レポート プレビューはクライアントでのみ可能なため、クライアント上にのみ ReportViewer オブジェクトが存在することができます。</span><span class="sxs-lookup"><span data-stu-id="87541-106">ReportViewer objects can exist only on the client, because a report preview can occur only on a client.</span></span>

## <a name="examples"></a><span data-ttu-id="87541-107">例</span><span class="sxs-lookup"><span data-stu-id="87541-107">Examples</span></span>

<span data-ttu-id="87541-108">次のコードは、現在の日付の printArchive に挿入されているジョブの説明とジョブのページ番号を出力し、ページ 1 をレポート ビューアーに表示します。</span><span class="sxs-lookup"><span data-stu-id="87541-108">The following code will print the job descriptions and the page numbers of jobs that are inserted in the printArchive on the current date, and it will show page 1 in the report viewer.</span></span>

```xpp
static void aaaReportOutputExample(args a) 
{ 
    PrintJobHeader printJobHeader; 
    PrintJobPages printJobPages; 
    int myrecId; 
    reportViewer reportViewer; 
    while select printJobHeader where printJobHeader.CreatedDate >= 
            str2datetime("01/01/2011 12:00:00 am",123)
    { 
        myrecId = printJobHeader.recId; 
        print printJobHeader.jobDescription; 
        while select printJobPages  
            where printJobPages.pagesHeaderRecId == myRecId 
                print printJobPages.PageNo; 
        reportViewer = new reportViewer(printJobHeader); 
        reportViewer.showPage(1); 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="87541-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="87541-109">Methods</span></span>

| <span data-ttu-id="87541-110">方法</span><span class="sxs-lookup"><span data-stu-id="87541-110">Method</span></span>                                                                                                          | <span data-ttu-id="87541-111">説明</span><span class="sxs-lookup"><span data-stu-id="87541-111">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="87541-112">public boolean setNumberOfPages(int pageNo, \[boolean updataProgressForm\])</span><span class="sxs-lookup"><span data-stu-id="87541-112">public boolean setNumberOfPages(int pageNo, \[boolean updataProgressForm\])</span></span>                                     |                                                 |
| <span data-ttu-id="87541-113">public void nextPage()</span><span class="sxs-lookup"><span data-stu-id="87541-113">public void nextPage()</span></span>                                                                                          |                                                 |
| <span data-ttu-id="87541-114">public void lastPage()</span><span class="sxs-lookup"><span data-stu-id="87541-114">public void lastPage()</span></span>                                                                                          |                                                 |
| <span data-ttu-id="87541-115">public void new(PrintJobHeader jobsCursor, \[PrintJobPages pagesCursor\], \[container packedPrintJobSettings\])</span><span class="sxs-lookup"><span data-stu-id="87541-115">public void new(PrintJobHeader jobsCursor, \[PrintJobPages pagesCursor\], \[container packedPrintJobSettings\])</span></span> | <span data-ttu-id="87541-116">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="87541-116">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="87541-117">public void gotoPage(int pageNo)</span><span class="sxs-lookup"><span data-stu-id="87541-117">public void gotoPage(int pageNo)</span></span>                                                                                |                                                 |
| <span data-ttu-id="87541-118">public void pause()</span><span class="sxs-lookup"><span data-stu-id="87541-118">public void pause()</span></span>                                                                                             |                                                 |
| <span data-ttu-id="87541-119">public void showPage(int pageNo)</span><span class="sxs-lookup"><span data-stu-id="87541-119">public void showPage(int pageNo)</span></span>                                                                                |                                                 |
| <span data-ttu-id="87541-120">public void firstPage()</span><span class="sxs-lookup"><span data-stu-id="87541-120">public void firstPage()</span></span>                                                                                         |                                                 |
| <span data-ttu-id="87541-121">public void setAborted()</span><span class="sxs-lookup"><span data-stu-id="87541-121">public void setAborted()</span></span>                                                                                        |                                                 |
| <span data-ttu-id="87541-122">public void close()</span><span class="sxs-lookup"><span data-stu-id="87541-122">public void close()</span></span>                                                                                             |                                                 |
| <span data-ttu-id="87541-123">public void prevPage()</span><span class="sxs-lookup"><span data-stu-id="87541-123">public void prevPage()</span></span>                                                                                          |                                                 |
| <span data-ttu-id="87541-124">public void setCompleted()</span><span class="sxs-lookup"><span data-stu-id="87541-124">public void setCompleted()</span></span>                                                                                      |                                                 |

## <a name="method-setnumberofpages"></a><span data-ttu-id="87541-125">メソッド setNumberOfPages</span><span class="sxs-lookup"><span data-stu-id="87541-125">Method setNumberOfPages</span></span>

```xpp
public boolean setNumberOfPages(int pageNo, [boolean updataProgressForm])
```

### <a name="parameters---setnumberofpages"></a><span data-ttu-id="87541-126">パラメーター - setNumberOfPages</span><span class="sxs-lookup"><span data-stu-id="87541-126">Parameters - setNumberOfPages</span></span>

<span data-ttu-id="87541-127">pageNo</span><span class="sxs-lookup"><span data-stu-id="87541-127">pageNo</span></span>  

<!-- -->

<span data-ttu-id="87541-128">updataProgressForm</span><span class="sxs-lookup"><span data-stu-id="87541-128">updataProgressForm</span></span>  

### <a name="return-value---setnumberofpages"></a><span data-ttu-id="87541-129">戻り値 - setNumberOfPages</span><span class="sxs-lookup"><span data-stu-id="87541-129">Return Value - setNumberOfPages</span></span>

## <a name="method-nextpage"></a><span data-ttu-id="87541-130">メソッド nextPage</span><span class="sxs-lookup"><span data-stu-id="87541-130">Method nextPage</span></span>

```xpp
public void nextPage()
```

## <a name="method-lastpage"></a><span data-ttu-id="87541-131">メソッド lastPage</span><span class="sxs-lookup"><span data-stu-id="87541-131">Method lastPage</span></span>

```xpp
public void lastPage()
```

## <a name="method-new"></a><span data-ttu-id="87541-132">メソッド new</span><span class="sxs-lookup"><span data-stu-id="87541-132">Method new</span></span>

<span data-ttu-id="87541-133">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="87541-133">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(PrintJobHeader jobsCursor, [PrintJobPages pagesCursor], [container packedPrintJobSettings])
```

### <a name="parameters---new"></a><span data-ttu-id="87541-134">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="87541-134">Parameters - new</span></span>

<span data-ttu-id="87541-135">jobsCursor</span><span class="sxs-lookup"><span data-stu-id="87541-135">jobsCursor</span></span>  

<!-- -->

<span data-ttu-id="87541-136">pagesCursor</span><span class="sxs-lookup"><span data-stu-id="87541-136">pagesCursor</span></span>  

<!-- -->

<span data-ttu-id="87541-137">packedPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="87541-137">packedPrintJobSettings</span></span>  

## <a name="method-gotopage"></a><span data-ttu-id="87541-138">メソッド gotoPage</span><span class="sxs-lookup"><span data-stu-id="87541-138">Method gotoPage</span></span>

```xpp
public void gotoPage(int pageNo)
```

### <a name="parameters---gotopage"></a><span data-ttu-id="87541-139">パラメーター - gotoPage</span><span class="sxs-lookup"><span data-stu-id="87541-139">Parameters - gotoPage</span></span>

<span data-ttu-id="87541-140">pageNo</span><span class="sxs-lookup"><span data-stu-id="87541-140">pageNo</span></span>  

## <a name="method-pause"></a><span data-ttu-id="87541-141">メソッド pause</span><span class="sxs-lookup"><span data-stu-id="87541-141">Method pause</span></span>

```xpp
public void pause()
```

## <a name="method-showpage"></a><span data-ttu-id="87541-142">メソッド showPage</span><span class="sxs-lookup"><span data-stu-id="87541-142">Method showPage</span></span>

```xpp
public void showPage(int pageNo)
```

### <a name="parameters---showpage"></a><span data-ttu-id="87541-143">パラメーター - showPage</span><span class="sxs-lookup"><span data-stu-id="87541-143">Parameters - showPage</span></span>

<span data-ttu-id="87541-144">pageNo</span><span class="sxs-lookup"><span data-stu-id="87541-144">pageNo</span></span>  

## <a name="method-firstpage"></a><span data-ttu-id="87541-145">メソッド firstPage</span><span class="sxs-lookup"><span data-stu-id="87541-145">Method firstPage</span></span>

```xpp
public void firstPage()
```

## <a name="method-setaborted"></a><span data-ttu-id="87541-146">メソッド setAborted</span><span class="sxs-lookup"><span data-stu-id="87541-146">Method setAborted</span></span>

```xpp
public void setAborted()
```

## <a name="method-close"></a><span data-ttu-id="87541-147">メソッド close</span><span class="sxs-lookup"><span data-stu-id="87541-147">Method close</span></span>

```xpp
public void close()
```

## <a name="method-prevpage"></a><span data-ttu-id="87541-148">メソッド prevPage</span><span class="sxs-lookup"><span data-stu-id="87541-148">Method prevPage</span></span>

```xpp
public void prevPage()
```

## <a name="method-setcompleted"></a><span data-ttu-id="87541-149">メソッド setCompleted</span><span class="sxs-lookup"><span data-stu-id="87541-149">Method setCompleted</span></span>

```xpp
public void setCompleted()
```


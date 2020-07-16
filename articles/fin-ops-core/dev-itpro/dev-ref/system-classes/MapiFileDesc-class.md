---
title: MapiFileDesc クラス
description: このトピックでは、MapiFileDesc クラスについて説明します。
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
ms.openlocfilehash: d38168ee5890f50d0068dea0e879725f3de1b107
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502580"
---
# <a name="class-mapifiledesc"></a><span data-ttu-id="3d56a-103">クラス MapiFileDesc</span><span class="sxs-lookup"><span data-stu-id="3d56a-103">Class MapiFileDesc</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MapiFileDesc extends Object
```

<span data-ttu-id="3d56a-104">MapiFileDesc クラスは、メッセージに関連付けられているファイルを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="3d56a-104">The MapiFileDesc class gets and sets the files that are attached to messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d56a-105">備考</span><span class="sxs-lookup"><span data-stu-id="3d56a-105">Remarks</span></span>

<span data-ttu-id="3d56a-106">ファイルの説明は、ファイルの 2 つのタイプの情報で構成されています。</span><span class="sxs-lookup"><span data-stu-id="3d56a-106">The file description consists of two types of information for the file:</span></span>

-   <span data-ttu-id="3d56a-107">ディスク上のファイルをポイントするパス メソッド</span><span class="sxs-lookup"><span data-stu-id="3d56a-107">A path method, which points to a file on disk</span></span>
-   <span data-ttu-id="3d56a-108">fileName メソッドには、ユーザーに表示されるファイル名が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3d56a-108">A fileName method, which contains the file name as it will be presented to the user.</span></span>

## <a name="examples"></a><span data-ttu-id="3d56a-109">例</span><span class="sxs-lookup"><span data-stu-id="3d56a-109">Examples</span></span>

```xpp
static void example() 
{ 
    MapiMessage msg = New MapiMessage(); 
    MapiFileDesc attach = new MapiFileDesc(); 
    attach.Path("C:\\files\\myfile.txt"); 
}
```

## <a name="methods"></a><span data-ttu-id="3d56a-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="3d56a-110">Methods</span></span>

| <span data-ttu-id="3d56a-111">方法</span><span class="sxs-lookup"><span data-stu-id="3d56a-111">Method</span></span>                                | <span data-ttu-id="3d56a-112">説明</span><span class="sxs-lookup"><span data-stu-id="3d56a-112">Description</span></span>                                           |
|---------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="3d56a-113">public str fileName(\[str filename\])</span><span class="sxs-lookup"><span data-stu-id="3d56a-113">public str fileName(\[str filename\])</span></span> |                                                       |
| <span data-ttu-id="3d56a-114">public str path(\[str thePath\])</span><span class="sxs-lookup"><span data-stu-id="3d56a-114">public str path(\[str thePath\])</span></span>      |                                                       |
| <span data-ttu-id="3d56a-115">public void new()</span><span class="sxs-lookup"><span data-stu-id="3d56a-115">public void new()</span></span>                     | <span data-ttu-id="3d56a-116">MapiFileDesc クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3d56a-116">Initializes a new instance of the MapiFileDesc class.</span></span> |
| <span data-ttu-id="3d56a-117">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="3d56a-117">public void finalize()</span></span>                |                                                       |

## <a name="method-filename"></a><span data-ttu-id="3d56a-118">メソッド fileName</span><span class="sxs-lookup"><span data-stu-id="3d56a-118">Method fileName</span></span>

```xpp
public str fileName([str filename])
```

### <a name="parameters---filename"></a><span data-ttu-id="3d56a-119">パラメーター - fileName</span><span class="sxs-lookup"><span data-stu-id="3d56a-119">Parameters - fileName</span></span>

<span data-ttu-id="3d56a-120">filename</span><span class="sxs-lookup"><span data-stu-id="3d56a-120">filename</span></span>  

### <a name="return-value---filename"></a><span data-ttu-id="3d56a-121">戻り値 - fileName</span><span class="sxs-lookup"><span data-stu-id="3d56a-121">Return Value - fileName</span></span>

## <a name="method-path"></a><span data-ttu-id="3d56a-122">メソッド path</span><span class="sxs-lookup"><span data-stu-id="3d56a-122">Method path</span></span>

```xpp
public str path([str thePath])
```

### <a name="parameters---path"></a><span data-ttu-id="3d56a-123">パラメーター - path</span><span class="sxs-lookup"><span data-stu-id="3d56a-123">Parameters - path</span></span>

<span data-ttu-id="3d56a-124">thePath</span><span class="sxs-lookup"><span data-stu-id="3d56a-124">thePath</span></span>  

### <a name="return-value---path"></a><span data-ttu-id="3d56a-125">戻り値 - path</span><span class="sxs-lookup"><span data-stu-id="3d56a-125">Return Value - path</span></span>

## <a name="method-new"></a><span data-ttu-id="3d56a-126">メソッド new</span><span class="sxs-lookup"><span data-stu-id="3d56a-126">Method new</span></span>

<span data-ttu-id="3d56a-127">MapiFileDesc クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3d56a-127">Initializes a new instance of the MapiFileDesc class.</span></span>

```xpp
public void new()
```

## <a name="method-finalize"></a><span data-ttu-id="3d56a-128">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="3d56a-128">Method finalize</span></span>

```xpp
public void finalize()
```


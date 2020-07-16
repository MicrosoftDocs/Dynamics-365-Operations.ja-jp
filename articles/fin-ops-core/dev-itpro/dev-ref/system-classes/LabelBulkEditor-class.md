---
title: LabelBulkEditor クラス
description: このトピックでは、LabelBulkEditor クラスについて説明します。
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
ms.openlocfilehash: a7532c770f75df8fb61875cd44379216f9eb007e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502895"
---
# <a name="class-labelbulkeditor"></a><span data-ttu-id="8ac06-103">クラス LabelBulkEditor</span><span class="sxs-lookup"><span data-stu-id="8ac06-103">Class LabelBulkEditor</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class LabelBulkEditor extends Object
```

<span data-ttu-id="8ac06-104">LabelBulkEditor クラスを使用すると、ラベル ファイルが簡単に変更されます。</span><span class="sxs-lookup"><span data-stu-id="8ac06-104">The LabelBulkEditor class is used to quickly modify label files.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ac06-105">備考</span><span class="sxs-lookup"><span data-stu-id="8ac06-105">Remarks</span></span>

<span data-ttu-id="8ac06-106">LabelBulkEditor クラスは、Label.bulkEditor() メソッドを通じてインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="8ac06-106">The LabelBulkEditor class is instantiated through the Label.bulkEditor() method.</span></span> <span data-ttu-id="8ac06-107">ラベル ファイルは、クラスのインスタンスが作成されたときに変更用に開かれ、インスタンスがガベージ コレクションされたときにラベル ファイルは閉じられます。</span><span class="sxs-lookup"><span data-stu-id="8ac06-107">The label file is opened for modification when the instance of the class is created, and the label file is closed when the instance has garbage collected.</span></span>

## <a name="examples"></a><span data-ttu-id="8ac06-108">例</span><span class="sxs-lookup"><span data-stu-id="8ac06-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="8ac06-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="8ac06-109">Methods</span></span>

| <span data-ttu-id="8ac06-110">方法</span><span class="sxs-lookup"><span data-stu-id="8ac06-110">Method</span></span>                                                      | <span data-ttu-id="8ac06-111">説明</span><span class="sxs-lookup"><span data-stu-id="8ac06-111">Description</span></span>                                                                  |
|-------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8ac06-112">public boolean delete(str label)</span><span class="sxs-lookup"><span data-stu-id="8ac06-112">public boolean delete(str label)</span></span>                            | <span data-ttu-id="8ac06-113">指定したラベルを削除します。</span><span class="sxs-lookup"><span data-stu-id="8ac06-113">Deletes a specified label.</span></span>                                                   |
| <span data-ttu-id="8ac06-114">public boolean modify(str label, str text, \[str comment\])</span><span class="sxs-lookup"><span data-stu-id="8ac06-114">public boolean modify(str label, str text, \[str comment\])</span></span> | <span data-ttu-id="8ac06-115">指定されたラベル ID に関連付けられているテキストおよびコメントを変更します。</span><span class="sxs-lookup"><span data-stu-id="8ac06-115">Modifies the text and comment that are associated with a specified label ID.</span></span> |
| <span data-ttu-id="8ac06-116">public void new()</span><span class="sxs-lookup"><span data-stu-id="8ac06-116">public void new()</span></span>                                           | <span data-ttu-id="8ac06-117">LabelBulkEditor クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8ac06-117">Initializes an instance of the LabelBulkEditor class.</span></span>                        |

## <a name="method-delete"></a><span data-ttu-id="8ac06-118">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="8ac06-118">Method delete</span></span>

<span data-ttu-id="8ac06-119">指定したラベルを削除します。</span><span class="sxs-lookup"><span data-stu-id="8ac06-119">Deletes a specified label.</span></span>

```xpp
public boolean delete(str label)
```

### <a name="parameters---delete"></a><span data-ttu-id="8ac06-120">パラメーター - delete</span><span class="sxs-lookup"><span data-stu-id="8ac06-120">Parameters - delete</span></span>

<span data-ttu-id="8ac06-121">ラベル</span><span class="sxs-lookup"><span data-stu-id="8ac06-121">label</span></span>  
<span data-ttu-id="8ac06-122">ラベル ID を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="8ac06-122">A string that specifies the label ID.</span></span> <span data-ttu-id="8ac06-123">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ac06-123">The string must include an at sign (@) followed by a label file ID and a number.</span></span>

### <a name="return-value---delete"></a><span data-ttu-id="8ac06-124">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="8ac06-124">Return Value - delete</span></span>

<span data-ttu-id="8ac06-125">ラベルが削除された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="8ac06-125">true if the label is deleted; otherwise, false.</span></span>

## <a name="method-modify"></a><span data-ttu-id="8ac06-126">メソッド modify</span><span class="sxs-lookup"><span data-stu-id="8ac06-126">Method modify</span></span>

<span data-ttu-id="8ac06-127">指定されたラベル ID に関連付けられているテキストおよびコメントを変更します。</span><span class="sxs-lookup"><span data-stu-id="8ac06-127">Modifies the text and comment that are associated with a specified label ID.</span></span>

```xpp
public boolean modify(str label, str text, [str comment])
```

### <a name="parameters---modify"></a><span data-ttu-id="8ac06-128">パラメーター - modify</span><span class="sxs-lookup"><span data-stu-id="8ac06-128">Parameters - modify</span></span>

<span data-ttu-id="8ac06-129">ラベル</span><span class="sxs-lookup"><span data-stu-id="8ac06-129">label</span></span>  
<span data-ttu-id="8ac06-130">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="8ac06-130">A string that specifies the comment that is associated with the label ID.</span></span>

<!-- -->

<span data-ttu-id="8ac06-131">テキスト</span><span class="sxs-lookup"><span data-stu-id="8ac06-131">text</span></span>  
<span data-ttu-id="8ac06-132">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="8ac06-132">A string that specifies the comment that is associated with the label ID.</span></span>

<!-- -->

<span data-ttu-id="8ac06-133">comment</span><span class="sxs-lookup"><span data-stu-id="8ac06-133">comment</span></span>  
<span data-ttu-id="8ac06-134">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="8ac06-134">A string that specifies the comment that is associated with the label ID.</span></span>

### <a name="return-value---modify"></a><span data-ttu-id="8ac06-135">戻り値 - modify</span><span class="sxs-lookup"><span data-stu-id="8ac06-135">Return Value - modify</span></span>

<span data-ttu-id="8ac06-136">ラベルが修正された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="8ac06-136">true if the label is modified; otherwise, false.</span></span>

## <a name="method-new"></a><span data-ttu-id="8ac06-137">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8ac06-137">Method new</span></span>

<span data-ttu-id="8ac06-138">LabelBulkEditor クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8ac06-138">Initializes an instance of the LabelBulkEditor class.</span></span>

```xpp
public void new()
```


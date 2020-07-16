---
title: ControlNode クラス
description: このトピックでは、ControlNode クラスについて説明します。
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
ms.openlocfilehash: 25abfbe55ffa5b6cb615966b08b815d2d843ab63
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502703"
---
# <a name="class-controlnode"></a><span data-ttu-id="c7bbf-103">クラス ControlNode</span><span class="sxs-lookup"><span data-stu-id="c7bbf-103">Class ControlNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ControlNode extends TreeNode
```

<span data-ttu-id="c7bbf-104">ControlNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c7bbf-104">The ControlNode class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7bbf-105">備考</span><span class="sxs-lookup"><span data-stu-id="c7bbf-105">Remarks</span></span>

<span data-ttu-id="c7bbf-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c7bbf-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="c7bbf-107">例</span><span class="sxs-lookup"><span data-stu-id="c7bbf-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c7bbf-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="c7bbf-108">Methods</span></span>

| <span data-ttu-id="c7bbf-109">方法</span><span class="sxs-lookup"><span data-stu-id="c7bbf-109">Method</span></span>                                         | <span data-ttu-id="c7bbf-110">説明</span><span class="sxs-lookup"><span data-stu-id="c7bbf-110">Description</span></span>                                       |
|------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c7bbf-111">public void new(str name, \[TreeNode parent\])</span><span class="sxs-lookup"><span data-stu-id="c7bbf-111">public void new(str name, \[TreeNode parent\])</span></span> | <span data-ttu-id="c7bbf-112">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c7bbf-112">Initializes a new instance of the TreeNode class.</span></span> |

## <a name="method-new"></a><span data-ttu-id="c7bbf-113">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c7bbf-113">Method new</span></span>

<span data-ttu-id="c7bbf-114">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c7bbf-114">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new(str name, [TreeNode parent])
```

### <a name="parameters---new"></a><span data-ttu-id="c7bbf-115">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="c7bbf-115">Parameters - new</span></span>

<span data-ttu-id="c7bbf-116">名前</span><span class="sxs-lookup"><span data-stu-id="c7bbf-116">name</span></span>  

<!-- -->

<span data-ttu-id="c7bbf-117">parent</span><span class="sxs-lookup"><span data-stu-id="c7bbf-117">parent</span></span>  


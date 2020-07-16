---
title: ProjectListNode クラス
description: このトピックでは、ProjectListNode クラスについて説明します。
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
ms.openlocfilehash: ae88f94543e15ebfba443cec30739dee8d86c53e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502870"
---
# <a name="class-projectlistnode"></a><span data-ttu-id="5e167-103">クラス ProjectListNode</span><span class="sxs-lookup"><span data-stu-id="5e167-103">Class ProjectListNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ProjectListNode extends TreeNode
```

<span data-ttu-id="5e167-104">ProjectListNode クラスは、プロジェクトの概要ウィンドウ内のプロジェクトのプライベートと共有のリストに対応します。</span><span class="sxs-lookup"><span data-stu-id="5e167-104">The ProjectListNode class corresponds to the Private and Shared lists of projects in the project overview window.</span></span> <span data-ttu-id="5e167-105">X++ コードから新しいプロジェクトを追加するのにには、ProjectListNode.addProject メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5e167-105">Use the ProjectListNode.addProject method to add a new project from X++ code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e167-106">備考</span><span class="sxs-lookup"><span data-stu-id="5e167-106">Remarks</span></span>

<span data-ttu-id="5e167-107">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5e167-107">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="5e167-108">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5e167-108">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

## <a name="examples"></a><span data-ttu-id="5e167-109">例</span><span class="sxs-lookup"><span data-stu-id="5e167-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="5e167-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="5e167-110">Methods</span></span>

| <span data-ttu-id="5e167-111">方法</span><span class="sxs-lookup"><span data-stu-id="5e167-111">Method</span></span>                                                               | <span data-ttu-id="5e167-112">説明</span><span class="sxs-lookup"><span data-stu-id="5e167-112">Description</span></span>                     |
|----------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="5e167-113">public ProjectNode addProject(str projectName, \[str projectClass\])</span><span class="sxs-lookup"><span data-stu-id="5e167-113">public ProjectNode addProject(str projectName, \[str projectClass\])</span></span> | <span data-ttu-id="5e167-114">リストに新しいプロジェクトを追加します。</span><span class="sxs-lookup"><span data-stu-id="5e167-114">Adds a new project to the list.</span></span> |

## <a name="method-addproject"></a><span data-ttu-id="5e167-115">メソッド addProject</span><span class="sxs-lookup"><span data-stu-id="5e167-115">Method addProject</span></span>

<span data-ttu-id="5e167-116">リストに新しいプロジェクトを追加します。</span><span class="sxs-lookup"><span data-stu-id="5e167-116">Adds a new project to the list.</span></span>

```xpp
public ProjectNode addProject(str projectName, [str projectClass])
```

### <a name="parameters---addproject"></a><span data-ttu-id="5e167-117">パラメーター - addProject</span><span class="sxs-lookup"><span data-stu-id="5e167-117">Parameters - addProject</span></span>

<span data-ttu-id="5e167-118">projectName</span><span class="sxs-lookup"><span data-stu-id="5e167-118">projectName</span></span>  
<span data-ttu-id="5e167-119">projecttype の名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5e167-119">The name of the projecttype; optional.</span></span> <span data-ttu-id="5e167-120">これは、プロジェクトに関連付けられたクラスの名前でなければなりません (setProjectClass メソッドを参照)。</span><span class="sxs-lookup"><span data-stu-id="5e167-120">This should be the name of a class associated with the project (see the setProjectClass method).</span></span> <span data-ttu-id="5e167-121">値が指定されていない場合は、標準のプロジェクトがプロジェクトになります。</span><span class="sxs-lookup"><span data-stu-id="5e167-121">If no value is supplied, the project becomes a standard project.</span></span>

<!-- -->

<span data-ttu-id="5e167-122">projectClass</span><span class="sxs-lookup"><span data-stu-id="5e167-122">projectClass</span></span>  
<span data-ttu-id="5e167-123">projecttype の名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5e167-123">The name of the projecttype; optional.</span></span> <span data-ttu-id="5e167-124">これは、プロジェクトに関連付けられたクラスの名前でなければなりません (setProjectClass メソッドを参照)。</span><span class="sxs-lookup"><span data-stu-id="5e167-124">This should be the name of a class associated with the project (see the setProjectClass method).</span></span> <span data-ttu-id="5e167-125">値が指定されていない場合は、標準のプロジェクトがプロジェクトになります。</span><span class="sxs-lookup"><span data-stu-id="5e167-125">If no value is supplied, the project becomes a standard project.</span></span>

### <a name="return-value---addproject"></a><span data-ttu-id="5e167-126">戻り値 - addProject</span><span class="sxs-lookup"><span data-stu-id="5e167-126">Return Value - addProject</span></span>

<span data-ttu-id="5e167-127">新たに追加された projectNode。</span><span class="sxs-lookup"><span data-stu-id="5e167-127">The newly added projectNode.</span></span>


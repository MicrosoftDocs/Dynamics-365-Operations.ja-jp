---
title: WebDisplayContentItem クラス
description: このトピックでは、WebDisplayContentItem クラスについて説明します。
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
ms.openlocfilehash: 60459a8c2aa122c7e7ff237706dd4cf7b66c6555
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503003"
---
# <a name="class-webdisplaycontentitem"></a><span data-ttu-id="efda2-103">クラス WebDisplayContentItem</span><span class="sxs-lookup"><span data-stu-id="efda2-103">Class WebDisplayContentItem</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class WebDisplayContentItem extends WebContentItem
```

<span data-ttu-id="efda2-104">WebDisplayContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="efda2-104">The WebDisplayContentItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="efda2-105">備考</span><span class="sxs-lookup"><span data-stu-id="efda2-105">Remarks</span></span>

<span data-ttu-id="efda2-106">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="efda2-106">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="efda2-107">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="efda2-107">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

## <a name="examples"></a><span data-ttu-id="efda2-108">例</span><span class="sxs-lookup"><span data-stu-id="efda2-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="efda2-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="efda2-109">Methods</span></span>

| <span data-ttu-id="efda2-110">方法</span><span class="sxs-lookup"><span data-stu-id="efda2-110">Method</span></span>                    | <span data-ttu-id="efda2-111">説明</span><span class="sxs-lookup"><span data-stu-id="efda2-111">Description</span></span>                          |
|---------------------------|--------------------------------------|
| <span data-ttu-id="efda2-112">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="efda2-112">public void new(str name)</span></span> | <span data-ttu-id="efda2-113">新しい WebDisplayContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="efda2-113">Creates a new WebDisplayContentItem.</span></span> |

## <a name="method-new"></a><span data-ttu-id="efda2-114">メソッド new</span><span class="sxs-lookup"><span data-stu-id="efda2-114">Method new</span></span>

<span data-ttu-id="efda2-115">新しい WebDisplayContentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="efda2-115">Creates a new WebDisplayContentItem.</span></span>

```xpp
public void new(str name)
```

### <a name="parameters---new"></a><span data-ttu-id="efda2-116">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="efda2-116">Parameters - new</span></span>

<span data-ttu-id="efda2-117">名前</span><span class="sxs-lookup"><span data-stu-id="efda2-117">name</span></span>  


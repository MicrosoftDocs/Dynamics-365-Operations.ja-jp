---
title: UserSetup クラス
description: このトピックでは、UserSetup クラスについて説明します。
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
ms.openlocfilehash: ebbd3ff0570dc6af83a805b7a5b81e5ba33b34d2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502781"
---
# <a name="class-usersetup"></a><span data-ttu-id="606b0-103">クラス UserSetup</span><span class="sxs-lookup"><span data-stu-id="606b0-103">Class UserSetup</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class UserSetup extends TreeNode
```

<span data-ttu-id="606b0-104">UserSetup クラスは、ユーザー パラメーターを設定するためのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="606b0-104">The UserSetup class provides an interface for setting user parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="606b0-105">備考</span><span class="sxs-lookup"><span data-stu-id="606b0-105">Remarks</span></span>

<span data-ttu-id="606b0-106">このクラスは、主に SysUserSetup フォームで使用されます。</span><span class="sxs-lookup"><span data-stu-id="606b0-106">This class is used mainly in the SysUserSetup form.</span></span> <span data-ttu-id="606b0-107">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="606b0-107">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="606b0-108">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="606b0-108">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="606b0-109">例</span><span class="sxs-lookup"><span data-stu-id="606b0-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="606b0-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="606b0-110">Methods</span></span>

| <span data-ttu-id="606b0-111">方法</span><span class="sxs-lookup"><span data-stu-id="606b0-111">Method</span></span>                                  | <span data-ttu-id="606b0-112">説明</span><span class="sxs-lookup"><span data-stu-id="606b0-112">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="606b0-113">public boolean xRef(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="606b0-113">public boolean xRef(\[boolean enable\])</span></span> |             |
| <span data-ttu-id="606b0-114">public void setUserSetup(Common cursor)</span><span class="sxs-lookup"><span data-stu-id="606b0-114">public void setUserSetup(Common cursor)</span></span> |             |
| <span data-ttu-id="606b0-115">public void setDefaults(Common cursor)</span><span class="sxs-lookup"><span data-stu-id="606b0-115">public void setDefaults(Common cursor)</span></span>  |             |

## <a name="method-xref"></a><span data-ttu-id="606b0-116">メソッド xRef</span><span class="sxs-lookup"><span data-stu-id="606b0-116">Method xRef</span></span>

```xpp
public boolean xRef([boolean enable])
```

### <a name="parameters---xref"></a><span data-ttu-id="606b0-117">パラメーター - xRef</span><span class="sxs-lookup"><span data-stu-id="606b0-117">Parameters - xRef</span></span>

<span data-ttu-id="606b0-118">enable</span><span class="sxs-lookup"><span data-stu-id="606b0-118">enable</span></span>  

### <a name="return-value---xref"></a><span data-ttu-id="606b0-119">戻り値 - xRef</span><span class="sxs-lookup"><span data-stu-id="606b0-119">Return Value - xRef</span></span>

## <a name="method-setusersetup"></a><span data-ttu-id="606b0-120">メソッド setUserSetup</span><span class="sxs-lookup"><span data-stu-id="606b0-120">Method setUserSetup</span></span>

```xpp
public void setUserSetup(Common cursor)
```

### <a name="parameters---setusersetup"></a><span data-ttu-id="606b0-121">パラメーター - setUserSetup</span><span class="sxs-lookup"><span data-stu-id="606b0-121">Parameters - setUserSetup</span></span>

<span data-ttu-id="606b0-122">cursor</span><span class="sxs-lookup"><span data-stu-id="606b0-122">cursor</span></span>  

## <a name="method-setdefaults"></a><span data-ttu-id="606b0-123">メソッド setDefaults</span><span class="sxs-lookup"><span data-stu-id="606b0-123">Method setDefaults</span></span>

```xpp
public void setDefaults(Common cursor)
```

### <a name="parameters---setdefaults"></a><span data-ttu-id="606b0-124">パラメーター - setDefaults</span><span class="sxs-lookup"><span data-stu-id="606b0-124">Parameters - setDefaults</span></span>

<span data-ttu-id="606b0-125">cursor</span><span class="sxs-lookup"><span data-stu-id="606b0-125">cursor</span></span>  


---
title: SecurityTableRights クラス
description: このトピックでは、SecurityTableRights クラスについて説明します。
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
ms.openlocfilehash: 319dd41615c3609001c38295dd3574815450ac65
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502809"
---
# <a name="class-securitytablerights"></a><span data-ttu-id="da84d-103">クラス SecurityTableRights</span><span class="sxs-lookup"><span data-stu-id="da84d-103">Class SecurityTableRights</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SecurityTableRights extends Object
```

<span data-ttu-id="da84d-104">SecurityTableRights クラスには、テーブル セキュリティ権限に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="da84d-104">The SecurityTableRights class holds the information about the table security rights.</span></span>

## <a name="remarks"></a><span data-ttu-id="da84d-105">備考</span><span class="sxs-lookup"><span data-stu-id="da84d-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="da84d-106">例</span><span class="sxs-lookup"><span data-stu-id="da84d-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="da84d-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="da84d-107">Methods</span></span>

| <span data-ttu-id="da84d-108">方法</span><span class="sxs-lookup"><span data-stu-id="da84d-108">Method</span></span>                                                   | <span data-ttu-id="da84d-109">説明</span><span class="sxs-lookup"><span data-stu-id="da84d-109">Description</span></span>                                               |
|----------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="da84d-110">public AccessRight fieldAccessRight(FieldName fieldName)</span><span class="sxs-lookup"><span data-stu-id="da84d-110">public AccessRight fieldAccessRight(FieldName fieldName)</span></span> | <span data-ttu-id="da84d-111">テーブルのフィールドのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="da84d-111">Gets the access rights for the field of the table.</span></span>        |
| <span data-ttu-id="da84d-112">public AccessRight tableAccessRight()</span><span class="sxs-lookup"><span data-stu-id="da84d-112">public AccessRight tableAccessRight()</span></span>                    | <span data-ttu-id="da84d-113">テーブルのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="da84d-113">Gets the access rights for the table.</span></span>                     |
| <span data-ttu-id="da84d-114">private void new()</span><span class="sxs-lookup"><span data-stu-id="da84d-114">private void new()</span></span>                                       | <span data-ttu-id="da84d-115">SecurityTableRights クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="da84d-115">Initializes an instance of the SecurityTableRights class.</span></span> |

## <a name="method-fieldaccessright"></a><span data-ttu-id="da84d-116">メソッド fieldAccessRight</span><span class="sxs-lookup"><span data-stu-id="da84d-116">Method fieldAccessRight</span></span>

<span data-ttu-id="da84d-117">テーブルのフィールドのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="da84d-117">Gets the access rights for the field of the table.</span></span>

```xpp
public AccessRight fieldAccessRight(FieldName fieldName)
```

### <a name="parameters---fieldaccessright"></a><span data-ttu-id="da84d-118">パラメーター - fieldAccessRight</span><span class="sxs-lookup"><span data-stu-id="da84d-118">Parameters - fieldAccessRight</span></span>

<span data-ttu-id="da84d-119">fieldName</span><span class="sxs-lookup"><span data-stu-id="da84d-119">fieldName</span></span>  

### <a name="return-value---fieldaccessright"></a><span data-ttu-id="da84d-120">戻り値 - fieldAccessRight</span><span class="sxs-lookup"><span data-stu-id="da84d-120">Return Value - fieldAccessRight</span></span>

<span data-ttu-id="da84d-121">フィールドの AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="da84d-121">The AccesRight instance for the field.</span></span>

## <a name="method-tableaccessright"></a><span data-ttu-id="da84d-122">メソッド tableAccessRight</span><span class="sxs-lookup"><span data-stu-id="da84d-122">Method tableAccessRight</span></span>

<span data-ttu-id="da84d-123">テーブルのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="da84d-123">Gets the access rights for the table.</span></span>

```xpp
public AccessRight tableAccessRight()
```

### <a name="return-value---tableaccessright"></a><span data-ttu-id="da84d-124">戻り値 - tableAccessRight</span><span class="sxs-lookup"><span data-stu-id="da84d-124">Return Value - tableAccessRight</span></span>

<span data-ttu-id="da84d-125">テーブルの AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="da84d-125">The AccesRight instance for the table.</span></span>

## <a name="method-new"></a><span data-ttu-id="da84d-126">メソッド new</span><span class="sxs-lookup"><span data-stu-id="da84d-126">Method new</span></span>

<span data-ttu-id="da84d-127">SecurityTableRights クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="da84d-127">Initializes an instance of the SecurityTableRights class.</span></span>

```xpp
private void new()
```


---
title: PageData タイプ
description: ページに読み込まれたデータを表します。
author: robinarh
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d9752b3b9f5ec77a194ad73caab9c5fb814f7fa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749259"
---
# <a name="pagedata-type"></a><span data-ttu-id="cbb01-103">PageData タイプ</span><span class="sxs-lookup"><span data-stu-id="cbb01-103">PageData type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="cbb01-104">ページに読み込まれたデータを表します。</span><span class="sxs-lookup"><span data-stu-id="cbb01-104">Represents the data that is loaded into a page.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="cbb01-105">階層</span><span class="sxs-lookup"><span data-stu-id="cbb01-105">Hierarchy</span></span>

<span data-ttu-id="cbb01-106">PageData</span><span class="sxs-lookup"><span data-stu-id="cbb01-106">PageData</span></span> <br>

## <a name="index"></a><span data-ttu-id="cbb01-107">指数</span><span class="sxs-lookup"><span data-stu-id="cbb01-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="cbb01-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="cbb01-108">Methods</span></span>

* [<span data-ttu-id="cbb01-109">getControlValue</span><span class="sxs-lookup"><span data-stu-id="cbb01-109">getControlValue</span></span>](services-business-logic-services-ipagedata.md#getcontrolvalue)
* [<span data-ttu-id="cbb01-110">setControlValue</span><span class="sxs-lookup"><span data-stu-id="cbb01-110">setControlValue</span></span>](services-business-logic-services-ipagedata.md#setcontrolvalue)

## <a name="methods"></a><span data-ttu-id="cbb01-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="cbb01-111">Methods</span></span>

### <a name="getcontrolvalue"></a><span data-ttu-id="cbb01-112">getControlValue</span><span class="sxs-lookup"><span data-stu-id="cbb01-112">getControlValue</span></span>


<span data-ttu-id="cbb01-113">getControlValue(controlName: string): any</span><span class="sxs-lookup"><span data-stu-id="cbb01-113">getControlValue(controlName: string): any</span></span>

<span data-ttu-id="cbb01-114">ページでデータ セットから直接読み込まれるコントロールの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="cbb01-114">Gets the value of a control directly from the data set loaded in the page.</span></span>
<span data-ttu-id="cbb01-115">「値」は、あらゆる種類のコントロールで柔軟に定義されており、通常は、コントロールと共に表示または操作されるプライマリ単一フィールド値を示します。</span><span class="sxs-lookup"><span data-stu-id="cbb01-115">The "value" is loosely defined across all different types of controls and generally indicates the primary single field value displayed or interacted with the control.</span></span> <span data-ttu-id="cbb01-116">一部の複雑なコントロール (ルックアップやリストなど) には、単純な値がない場合があるため、この API を通じてアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="cbb01-116">Some complex controls (e.g a lookup or a list) may not have a simple value and thus cannot be accessed via this API.</span></span>


#### <a name="parameters"></a><span data-ttu-id="cbb01-117">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cbb01-117">Parameters</span></span>

| <span data-ttu-id="cbb01-118">氏名</span><span class="sxs-lookup"><span data-stu-id="cbb01-118">Name</span></span> | <span data-ttu-id="cbb01-119">種類</span><span class="sxs-lookup"><span data-stu-id="cbb01-119">Type</span></span> | <span data-ttu-id="cbb01-120">説明</span><span class="sxs-lookup"><span data-stu-id="cbb01-120">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="cbb01-121">controlName</span><span class="sxs-lookup"><span data-stu-id="cbb01-121">controlName</span></span>|<span data-ttu-id="cbb01-122">string</span><span class="sxs-lookup"><span data-stu-id="cbb01-122">string</span></span>|<span data-ttu-id="cbb01-123">値を取得する対象のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="cbb01-123">name of the control whose value is to be retrieved</span></span>|

#### <a name="returns-any"></a><span data-ttu-id="cbb01-124">any を返します</span><span class="sxs-lookup"><span data-stu-id="cbb01-124">Returns any</span></span>

### <a name="setcontrolvalue"></a><span data-ttu-id="cbb01-125">setControlValue</span><span class="sxs-lookup"><span data-stu-id="cbb01-125">setControlValue</span></span>


<span data-ttu-id="cbb01-126">setControlValue(controlName: string, value: any): any</span><span class="sxs-lookup"><span data-stu-id="cbb01-126">setControlValue(controlName: string, value: any): any</span></span>

<span data-ttu-id="cbb01-127">ページでデータ セットに直接読み込まれるコントロールの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="cbb01-127">Sets the value of a control directly into the data set loaded in the page.</span></span>
<span data-ttu-id="cbb01-128">「値」は、あらゆる種類のコントロールで柔軟に定義されており、通常は、コントロールと共に表示または操作されるプライマリ単一フィールド値を示します。</span><span class="sxs-lookup"><span data-stu-id="cbb01-128">The "value" is loosely defined across all different types of controls and generally indicates the primary single field value displayed or interacted with the control.</span></span> <span data-ttu-id="cbb01-129">一部の複雑なコントロール (ルックアップやリストなど) には、単純な値がない場合があるため、この API を通じてアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="cbb01-129">Some complex controls (e.g a lookup or a list) may not have a simple value and thus cannot be accessed via this API.</span></span>


#### <a name="parameters"></a><span data-ttu-id="cbb01-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cbb01-130">Parameters</span></span>

| <span data-ttu-id="cbb01-131">氏名</span><span class="sxs-lookup"><span data-stu-id="cbb01-131">Name</span></span> | <span data-ttu-id="cbb01-132">種類</span><span class="sxs-lookup"><span data-stu-id="cbb01-132">Type</span></span> | <span data-ttu-id="cbb01-133">説明</span><span class="sxs-lookup"><span data-stu-id="cbb01-133">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="cbb01-134">controlName</span><span class="sxs-lookup"><span data-stu-id="cbb01-134">controlName</span></span>|<span data-ttu-id="cbb01-135">string</span><span class="sxs-lookup"><span data-stu-id="cbb01-135">string</span></span>|<span data-ttu-id="cbb01-136">値を設定する対象のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="cbb01-136">Name of the control whose value is to be set</span></span>|
| <span data-ttu-id="cbb01-137">値</span><span class="sxs-lookup"><span data-stu-id="cbb01-137">value</span></span>|<span data-ttu-id="cbb01-138">any</span><span class="sxs-lookup"><span data-stu-id="cbb01-138">any</span></span>|<span data-ttu-id="cbb01-139">設定する値</span><span class="sxs-lookup"><span data-stu-id="cbb01-139">The value to be set</span></span>|

#### <a name="returns-any"></a><span data-ttu-id="cbb01-140">any を返します</span><span class="sxs-lookup"><span data-stu-id="cbb01-140">Returns any</span></span>



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
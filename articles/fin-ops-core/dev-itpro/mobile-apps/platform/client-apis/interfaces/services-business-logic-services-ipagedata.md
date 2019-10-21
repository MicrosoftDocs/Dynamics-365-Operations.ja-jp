---
title: PageData タイプ
description: ページに読み込まれたデータを表します。
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b91d4388c375c3a813862b5fea5ea1d473242893
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191864"
---
# <a name="pagedata-type"></a><span data-ttu-id="a55d8-103">PageData タイプ</span><span class="sxs-lookup"><span data-stu-id="a55d8-103">PageData type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="a55d8-104">ページに読み込まれたデータを表します。</span><span class="sxs-lookup"><span data-stu-id="a55d8-104">Represents the data that is loaded into a page.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="a55d8-105">階層</span><span class="sxs-lookup"><span data-stu-id="a55d8-105">Hierarchy</span></span>

<span data-ttu-id="a55d8-106">PageData</span><span class="sxs-lookup"><span data-stu-id="a55d8-106">PageData</span></span> <br>

## <a name="index"></a><span data-ttu-id="a55d8-107">指数</span><span class="sxs-lookup"><span data-stu-id="a55d8-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="a55d8-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="a55d8-108">Methods</span></span>

* [<span data-ttu-id="a55d8-109">getControlValue</span><span class="sxs-lookup"><span data-stu-id="a55d8-109">getControlValue</span></span>](services-business-logic-services-ipagedata.md#getcontrolvalue)
* [<span data-ttu-id="a55d8-110">setControlValue</span><span class="sxs-lookup"><span data-stu-id="a55d8-110">setControlValue</span></span>](services-business-logic-services-ipagedata.md#setcontrolvalue)

## <a name="methods"></a><span data-ttu-id="a55d8-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="a55d8-111">Methods</span></span>

### <a name="getcontrolvalue"></a><span data-ttu-id="a55d8-112">getControlValue</span><span class="sxs-lookup"><span data-stu-id="a55d8-112">getControlValue</span></span>


<span data-ttu-id="a55d8-113">getControlValue(controlName: string): any</span><span class="sxs-lookup"><span data-stu-id="a55d8-113">getControlValue(controlName: string): any</span></span>

<span data-ttu-id="a55d8-114">ページでデータ セットから直接読み込まれるコントロールの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a55d8-114">Gets the value of a control directly from the data set loaded in the page.</span></span>
<span data-ttu-id="a55d8-115">「値」は、あらゆる種類のコントロールで柔軟に定義されており、通常は、コントロールと共に表示または操作されるプライマリ単一フィールド値を示します。</span><span class="sxs-lookup"><span data-stu-id="a55d8-115">The "value" is loosely defined across all different types of controls and generally indicates the primary single field value displayed or interacted with the control.</span></span> <span data-ttu-id="a55d8-116">一部の複雑なコントロール (ルックアップやリストなど) には、単純な値がない場合があるため、この API を通じてアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="a55d8-116">Some complex controls (e.g a lookup or a list) may not have a simple value and thus cannot be accessed via this API.</span></span>


#### <a name="parameters"></a><span data-ttu-id="a55d8-117">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a55d8-117">Parameters</span></span>

| <span data-ttu-id="a55d8-118">氏名</span><span class="sxs-lookup"><span data-stu-id="a55d8-118">Name</span></span> | <span data-ttu-id="a55d8-119">種類</span><span class="sxs-lookup"><span data-stu-id="a55d8-119">Type</span></span> | <span data-ttu-id="a55d8-120">説明</span><span class="sxs-lookup"><span data-stu-id="a55d8-120">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="a55d8-121">controlName</span><span class="sxs-lookup"><span data-stu-id="a55d8-121">controlName</span></span>|<span data-ttu-id="a55d8-122">string</span><span class="sxs-lookup"><span data-stu-id="a55d8-122">string</span></span>|<span data-ttu-id="a55d8-123">値を取得する対象のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="a55d8-123">name of the control whose value is to be retrieved</span></span>|

#### <a name="returns-any"></a><span data-ttu-id="a55d8-124">any を返します</span><span class="sxs-lookup"><span data-stu-id="a55d8-124">Returns any</span></span>

### <a name="setcontrolvalue"></a><span data-ttu-id="a55d8-125">setControlValue</span><span class="sxs-lookup"><span data-stu-id="a55d8-125">setControlValue</span></span>


<span data-ttu-id="a55d8-126">setControlValue(controlName: string, value: any): any</span><span class="sxs-lookup"><span data-stu-id="a55d8-126">setControlValue(controlName: string, value: any): any</span></span>

<span data-ttu-id="a55d8-127">ページでデータ セットに直接読み込まれるコントロールの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a55d8-127">Sets the value of a control directly into the data set loaded in the page.</span></span>
<span data-ttu-id="a55d8-128">「値」は、あらゆる種類のコントロールで柔軟に定義されており、通常は、コントロールと共に表示または操作されるプライマリ単一フィールド値を示します。</span><span class="sxs-lookup"><span data-stu-id="a55d8-128">The "value" is loosely defined across all different types of controls and generally indicates the primary single field value displayed or interacted with the control.</span></span> <span data-ttu-id="a55d8-129">一部の複雑なコントロール (ルックアップやリストなど) には、単純な値がない場合があるため、この API を通じてアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="a55d8-129">Some complex controls (e.g a lookup or a list) may not have a simple value and thus cannot be accessed via this API.</span></span>


#### <a name="parameters"></a><span data-ttu-id="a55d8-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a55d8-130">Parameters</span></span>

| <span data-ttu-id="a55d8-131">氏名</span><span class="sxs-lookup"><span data-stu-id="a55d8-131">Name</span></span> | <span data-ttu-id="a55d8-132">種類</span><span class="sxs-lookup"><span data-stu-id="a55d8-132">Type</span></span> | <span data-ttu-id="a55d8-133">説明</span><span class="sxs-lookup"><span data-stu-id="a55d8-133">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="a55d8-134">controlName</span><span class="sxs-lookup"><span data-stu-id="a55d8-134">controlName</span></span>|<span data-ttu-id="a55d8-135">string</span><span class="sxs-lookup"><span data-stu-id="a55d8-135">string</span></span>|<span data-ttu-id="a55d8-136">値を設定する対象のコントロールの名前</span><span class="sxs-lookup"><span data-stu-id="a55d8-136">Name of the control whose value is to be set</span></span>|
| <span data-ttu-id="a55d8-137">値</span><span class="sxs-lookup"><span data-stu-id="a55d8-137">value</span></span>|<span data-ttu-id="a55d8-138">any</span><span class="sxs-lookup"><span data-stu-id="a55d8-138">any</span></span>|<span data-ttu-id="a55d8-139">設定する値</span><span class="sxs-lookup"><span data-stu-id="a55d8-139">The value to be set</span></span>|

#### <a name="returns-any"></a><span data-ttu-id="a55d8-140">any を返します</span><span class="sxs-lookup"><span data-stu-id="a55d8-140">Returns any</span></span>


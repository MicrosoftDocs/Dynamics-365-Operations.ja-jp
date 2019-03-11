---
title: PageSubmitArgs タイプ
description: ページの OnSubmit イベントに指定された引数。
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2bdb0c78b6d15cec6ace5044d50008618fbc49d7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368870"
---
# <a name="pagesubmitargs-type"></a><span data-ttu-id="9a998-103">PageSubmitArgs タイプ</span><span class="sxs-lookup"><span data-stu-id="9a998-103">PageSubmitArgs type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="9a998-104">ページの OnSubmit イベントに指定された引数。</span><span class="sxs-lookup"><span data-stu-id="9a998-104">Args supplied to the OnSubmit event of the page.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="9a998-105">階層</span><span class="sxs-lookup"><span data-stu-id="9a998-105">Hierarchy</span></span>

<span data-ttu-id="9a998-106">PageSubmitArgs</span><span class="sxs-lookup"><span data-stu-id="9a998-106">PageSubmitArgs</span></span> <br>

## <a name="index"></a><span data-ttu-id="9a998-107">指数</span><span class="sxs-lookup"><span data-stu-id="9a998-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="9a998-108">プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a998-108">Properties</span></span>

* [<span data-ttu-id="9a998-109">dataValues</span><span class="sxs-lookup"><span data-stu-id="9a998-109">dataValues</span></span>](view-model-ipage-ipagesubmitargs.md#datavalues)
* [<span data-ttu-id="9a998-110">送信者</span><span class="sxs-lookup"><span data-stu-id="9a998-110">sender</span></span>](view-model-ipage-ipagesubmitargs.md#sender)

### <a name="methods"></a><span data-ttu-id="9a998-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="9a998-111">Methods</span></span>

* [<span data-ttu-id="9a998-112">addMessage</span><span class="sxs-lookup"><span data-stu-id="9a998-112">addMessage</span></span>](view-model-ipage-ipagesubmitargs.md#addmessage)
* [<span data-ttu-id="9a998-113">キャンセル</span><span class="sxs-lookup"><span data-stu-id="9a998-113">cancel</span></span>](view-model-ipage-ipagesubmitargs.md#cancel)
* [<span data-ttu-id="9a998-114">getMessages</span><span class="sxs-lookup"><span data-stu-id="9a998-114">getMessages</span></span>](view-model-ipage-ipagesubmitargs.md#getmessages)
* [<span data-ttu-id="9a998-115">isCancelled</span><span class="sxs-lookup"><span data-stu-id="9a998-115">isCancelled</span></span>](view-model-ipage-ipagesubmitargs.md#iscancelled)
* [<span data-ttu-id="9a998-116">待機</span><span class="sxs-lookup"><span data-stu-id="9a998-116">wait</span></span>](view-model-ipage-ipagesubmitargs.md#wait)

## <a name="properties"></a><span data-ttu-id="9a998-117">プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a998-117">Properties</span></span>

### <a name="datavalues"></a><span data-ttu-id="9a998-118">dataValues</span><span class="sxs-lookup"><span data-stu-id="9a998-118">dataValues</span></span>

<span data-ttu-id="9a998-119">dataValues: any</span><span class="sxs-lookup"><span data-stu-id="9a998-119">dataValues: any</span></span>

<span data-ttu-id="9a998-120">送信アクションの伝送データを取得します。</span><span class="sxs-lookup"><span data-stu-id="9a998-120">Get the payload of the submit action.</span></span>


### <a name="sender"></a><span data-ttu-id="9a998-121">sender</span><span class="sxs-lookup"><span data-stu-id="9a998-121">sender</span></span>

<span data-ttu-id="9a998-122">sender: [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="9a998-122">sender: [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="9a998-123">送信アクションの送信者ページ インスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="9a998-123">Get the sender page instance of the submit action.</span></span>


## <a name="methods"></a><span data-ttu-id="9a998-124">メソッド</span><span class="sxs-lookup"><span data-stu-id="9a998-124">Methods</span></span>

### <a name="addmessage"></a><span data-ttu-id="9a998-125">addMessage</span><span class="sxs-lookup"><span data-stu-id="9a998-125">addMessage</span></span>


<span data-ttu-id="9a998-126">addMessage(message: string, type: any): any</span><span class="sxs-lookup"><span data-stu-id="9a998-126">addMessage(message: string, type: any): any</span></span>

<span data-ttu-id="9a998-127">表示される検証/エラー メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="9a998-127">Add a validation/error message to be displayed.</span></span>


#### <a name="parameters"></a><span data-ttu-id="9a998-128">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9a998-128">Parameters</span></span>

| <span data-ttu-id="9a998-129">氏名</span><span class="sxs-lookup"><span data-stu-id="9a998-129">Name</span></span> | <span data-ttu-id="9a998-130">種類</span><span class="sxs-lookup"><span data-stu-id="9a998-130">Type</span></span> | <span data-ttu-id="9a998-131">説明</span><span class="sxs-lookup"><span data-stu-id="9a998-131">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="9a998-132">メッセージ</span><span class="sxs-lookup"><span data-stu-id="9a998-132">message</span></span>|<span data-ttu-id="9a998-133">string</span><span class="sxs-lookup"><span data-stu-id="9a998-133">string</span></span>||
| <span data-ttu-id="9a998-134">タイプ</span><span class="sxs-lookup"><span data-stu-id="9a998-134">type</span></span>|<span data-ttu-id="9a998-135">any</span><span class="sxs-lookup"><span data-stu-id="9a998-135">any</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="9a998-136">any を返します</span><span class="sxs-lookup"><span data-stu-id="9a998-136">Returns any</span></span>

### <a name="cancel"></a><span data-ttu-id="9a998-137">キャンセル</span><span class="sxs-lookup"><span data-stu-id="9a998-137">cancel</span></span>


<span data-ttu-id="9a998-138">cancel(): any</span><span class="sxs-lookup"><span data-stu-id="9a998-138">cancel(): any</span></span>

<span data-ttu-id="9a998-139">アクションの送信を禁止します。</span><span class="sxs-lookup"><span data-stu-id="9a998-139">Prevent the action from submitting.</span></span>

#### <a name="returns-any"></a><span data-ttu-id="9a998-140">any を返します</span><span class="sxs-lookup"><span data-stu-id="9a998-140">Returns any</span></span>

### <a name="getmessages"></a><span data-ttu-id="9a998-141">getMessages</span><span class="sxs-lookup"><span data-stu-id="9a998-141">getMessages</span></span>


<span data-ttu-id="9a998-142">getMessages(): string [ ]</span><span class="sxs-lookup"><span data-stu-id="9a998-142">getMessages(): string [ ]</span></span>

<span data-ttu-id="9a998-143">以前に追加されたすべてのメッセージを取得します</span><span class="sxs-lookup"><span data-stu-id="9a998-143">Get all previously added messages</span></span>

#### <a name="returns-string--"></a><span data-ttu-id="9a998-144">string [ ] を返します</span><span class="sxs-lookup"><span data-stu-id="9a998-144">Returns string [ ]</span></span>



### <a name="iscancelled"></a><span data-ttu-id="9a998-145">isCancelled</span><span class="sxs-lookup"><span data-stu-id="9a998-145">isCancelled</span></span>


<span data-ttu-id="9a998-146">isCancelled(): boolean</span><span class="sxs-lookup"><span data-stu-id="9a998-146">isCancelled(): boolean</span></span>

<span data-ttu-id="9a998-147">送信アクションがキャンセルされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a998-147">Check if the submit action is cancelled.</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="9a998-148">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="9a998-148">Returns boolean</span></span>



### <a name="wait"></a><span data-ttu-id="9a998-149">wait</span><span class="sxs-lookup"><span data-stu-id="9a998-149">wait</span></span>


<span data-ttu-id="9a998-150">wait(promise: Promise &lt;any&gt;): any</span><span class="sxs-lookup"><span data-stu-id="9a998-150">wait(promise: Promise &lt;any&gt;): any</span></span>

<span data-ttu-id="9a998-151">送信を続行する前に、指定された約束を待ちます。</span><span class="sxs-lookup"><span data-stu-id="9a998-151">Wait on a given promise before continuing with the submission.</span></span>
<span data-ttu-id="9a998-152">待機を介して添付されたすべての約束は、送信アクションが実行される前に解決される必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a998-152">All promises attached via wait must resolve before the submit action is performed.</span></span>


#### <a name="parameters"></a><span data-ttu-id="9a998-153">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9a998-153">Parameters</span></span>

| <span data-ttu-id="9a998-154">氏名</span><span class="sxs-lookup"><span data-stu-id="9a998-154">Name</span></span> | <span data-ttu-id="9a998-155">種類</span><span class="sxs-lookup"><span data-stu-id="9a998-155">Type</span></span> | <span data-ttu-id="9a998-156">説明</span><span class="sxs-lookup"><span data-stu-id="9a998-156">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="9a998-157">promise</span><span class="sxs-lookup"><span data-stu-id="9a998-157">promise</span></span>|<span data-ttu-id="9a998-158">&lt;任意&gt;の約束</span><span class="sxs-lookup"><span data-stu-id="9a998-158">Promise &lt;any&gt;</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="9a998-159">any を返します</span><span class="sxs-lookup"><span data-stu-id="9a998-159">Returns any</span></span>


---
title: MyLeaveRequests の概要
description: Microsoft Dynamics 365 Human Resourcesの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419303"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="7612f-103">MyLeaveRequests の概要</span><span class="sxs-lookup"><span data-stu-id="7612f-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="7612f-104">Microsoft Dynamics 365 Human Resourcesの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。</span><span class="sxs-lookup"><span data-stu-id="7612f-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="7612f-105">キー</span><span class="sxs-lookup"><span data-stu-id="7612f-105">Key</span></span>

  | <span data-ttu-id="7612f-106">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="7612f-106">Property Name</span></span> | <span data-ttu-id="7612f-107">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="7612f-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="7612f-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="7612f-108">dataAreaId</span></span>    | <span data-ttu-id="7612f-109">文字列</span><span class="sxs-lookup"><span data-stu-id="7612f-109">String</span></span>    |
  | <span data-ttu-id="7612f-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="7612f-110">RequestId</span></span>     | <span data-ttu-id="7612f-111">文字列</span><span class="sxs-lookup"><span data-stu-id="7612f-111">String</span></span>    |
  | <span data-ttu-id="7612f-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="7612f-112">LeaveType</span></span>     | <span data-ttu-id="7612f-113">文字列</span><span class="sxs-lookup"><span data-stu-id="7612f-113">String</span></span>    |
  | <span data-ttu-id="7612f-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="7612f-114">LeaveDate</span></span>     | <span data-ttu-id="7612f-115">日</span><span class="sxs-lookup"><span data-stu-id="7612f-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="7612f-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7612f-116">Properties</span></span>

  | <span data-ttu-id="7612f-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="7612f-117">Property Name</span></span>     | <span data-ttu-id="7612f-118">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="7612f-118">Data Type</span></span> | <span data-ttu-id="7612f-119">必須</span><span class="sxs-lookup"><span data-stu-id="7612f-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="7612f-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="7612f-120">dataAreaId</span></span>        | <span data-ttu-id="7612f-121">文字列</span><span class="sxs-lookup"><span data-stu-id="7612f-121">String</span></span>    | <span data-ttu-id="7612f-122">x</span><span class="sxs-lookup"><span data-stu-id="7612f-122">X</span></span>        |
  | <span data-ttu-id="7612f-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="7612f-123">RequestId</span></span>         | <span data-ttu-id="7612f-124">文字列</span><span class="sxs-lookup"><span data-stu-id="7612f-124">String</span></span>    | <span data-ttu-id="7612f-125">x</span><span class="sxs-lookup"><span data-stu-id="7612f-125">X</span></span>        |
  | <span data-ttu-id="7612f-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="7612f-126">LeaveType</span></span>         | <span data-ttu-id="7612f-127">文字列</span><span class="sxs-lookup"><span data-stu-id="7612f-127">String</span></span>    | <span data-ttu-id="7612f-128">x</span><span class="sxs-lookup"><span data-stu-id="7612f-128">X</span></span>        |
  | <span data-ttu-id="7612f-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="7612f-129">LeaveDate</span></span>         | <span data-ttu-id="7612f-130">日</span><span class="sxs-lookup"><span data-stu-id="7612f-130">Date</span></span>      | <span data-ttu-id="7612f-131">x</span><span class="sxs-lookup"><span data-stu-id="7612f-131">X</span></span>        |
  | <span data-ttu-id="7612f-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="7612f-132">ReasonCodeId</span></span>      | <span data-ttu-id="7612f-133">文字列</span><span class="sxs-lookup"><span data-stu-id="7612f-133">String</span></span>    |          |
  | <span data-ttu-id="7612f-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="7612f-134">PersonnelNumber</span></span>   | <span data-ttu-id="7612f-135">文字列</span><span class="sxs-lookup"><span data-stu-id="7612f-135">String</span></span>    | <span data-ttu-id="7612f-136">x</span><span class="sxs-lookup"><span data-stu-id="7612f-136">X</span></span>        |
  | <span data-ttu-id="7612f-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="7612f-137">RequestDate</span></span>       | <span data-ttu-id="7612f-138">日</span><span class="sxs-lookup"><span data-stu-id="7612f-138">Date</span></span>      | <span data-ttu-id="7612f-139">x</span><span class="sxs-lookup"><span data-stu-id="7612f-139">X</span></span>        |
  | <span data-ttu-id="7612f-140">コメント</span><span class="sxs-lookup"><span data-stu-id="7612f-140">Comment</span></span>           | <span data-ttu-id="7612f-141">文字列</span><span class="sxs-lookup"><span data-stu-id="7612f-141">String</span></span>    |          |
  | <span data-ttu-id="7612f-142">ステータス</span><span class="sxs-lookup"><span data-stu-id="7612f-142">Status</span></span>            | <span data-ttu-id="7612f-143">列挙</span><span class="sxs-lookup"><span data-stu-id="7612f-143">Enum</span></span>      | <span data-ttu-id="7612f-144">x</span><span class="sxs-lookup"><span data-stu-id="7612f-144">X</span></span>        |
  | <span data-ttu-id="7612f-145">量</span><span class="sxs-lookup"><span data-stu-id="7612f-145">Amount</span></span>            | <span data-ttu-id="7612f-146">実績</span><span class="sxs-lookup"><span data-stu-id="7612f-146">Real</span></span>      |          |
  | <span data-ttu-id="7612f-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="7612f-147">HalfDayDefinition</span></span> | <span data-ttu-id="7612f-148">列挙</span><span class="sxs-lookup"><span data-stu-id="7612f-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="7612f-149">アクション</span><span class="sxs-lookup"><span data-stu-id="7612f-149">Actions</span></span>

 | <span data-ttu-id="7612f-150">アクション名</span><span class="sxs-lookup"><span data-stu-id="7612f-150">Action Name</span></span>                               | <span data-ttu-id="7612f-151">説明</span><span class="sxs-lookup"><span data-stu-id="7612f-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="7612f-152">送信</span><span class="sxs-lookup"><span data-stu-id="7612f-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="7612f-153">ワークフローで処理される要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="7612f-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7612f-154">参照</span><span class="sxs-lookup"><span data-stu-id="7612f-154">See also</span></span>

- [<span data-ttu-id="7612f-155">休暇申請をワークフローに送信する</span><span class="sxs-lookup"><span data-stu-id="7612f-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="7612f-156">認証</span><span class="sxs-lookup"><span data-stu-id="7612f-156">Authentication</span></span>](hr-developer-api-authentication.md)
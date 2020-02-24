---
title: MyLeaveRequests の概要
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009671"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="cb92f-102">MyLeaveRequests の概要</span><span class="sxs-lookup"><span data-stu-id="cb92f-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="cb92f-103">Microsoft Dynamics 365 Human Resourcesの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。</span><span class="sxs-lookup"><span data-stu-id="cb92f-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="cb92f-104">キー</span><span class="sxs-lookup"><span data-stu-id="cb92f-104">Key</span></span>

  | <span data-ttu-id="cb92f-105">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="cb92f-105">Property Name</span></span> | <span data-ttu-id="cb92f-106">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="cb92f-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="cb92f-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="cb92f-107">dataAreaId</span></span>    | <span data-ttu-id="cb92f-108">文字列</span><span class="sxs-lookup"><span data-stu-id="cb92f-108">String</span></span>    |
  | <span data-ttu-id="cb92f-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="cb92f-109">RequestId</span></span>     | <span data-ttu-id="cb92f-110">文字列</span><span class="sxs-lookup"><span data-stu-id="cb92f-110">String</span></span>    |
  | <span data-ttu-id="cb92f-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="cb92f-111">LeaveType</span></span>     | <span data-ttu-id="cb92f-112">文字列</span><span class="sxs-lookup"><span data-stu-id="cb92f-112">String</span></span>    |
  | <span data-ttu-id="cb92f-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="cb92f-113">LeaveDate</span></span>     | <span data-ttu-id="cb92f-114">日</span><span class="sxs-lookup"><span data-stu-id="cb92f-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="cb92f-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb92f-115">Properties</span></span>

  | <span data-ttu-id="cb92f-116">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="cb92f-116">Property Name</span></span>     | <span data-ttu-id="cb92f-117">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="cb92f-117">Data Type</span></span> | <span data-ttu-id="cb92f-118">必須</span><span class="sxs-lookup"><span data-stu-id="cb92f-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="cb92f-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="cb92f-119">dataAreaId</span></span>        | <span data-ttu-id="cb92f-120">文字列</span><span class="sxs-lookup"><span data-stu-id="cb92f-120">String</span></span>    | <span data-ttu-id="cb92f-121">x</span><span class="sxs-lookup"><span data-stu-id="cb92f-121">X</span></span>        |
  | <span data-ttu-id="cb92f-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="cb92f-122">RequestId</span></span>         | <span data-ttu-id="cb92f-123">文字列</span><span class="sxs-lookup"><span data-stu-id="cb92f-123">String</span></span>    | <span data-ttu-id="cb92f-124">x</span><span class="sxs-lookup"><span data-stu-id="cb92f-124">X</span></span>        |
  | <span data-ttu-id="cb92f-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="cb92f-125">LeaveType</span></span>         | <span data-ttu-id="cb92f-126">文字列</span><span class="sxs-lookup"><span data-stu-id="cb92f-126">String</span></span>    | <span data-ttu-id="cb92f-127">x</span><span class="sxs-lookup"><span data-stu-id="cb92f-127">X</span></span>        |
  | <span data-ttu-id="cb92f-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="cb92f-128">LeaveDate</span></span>         | <span data-ttu-id="cb92f-129">日</span><span class="sxs-lookup"><span data-stu-id="cb92f-129">Date</span></span>      | <span data-ttu-id="cb92f-130">x</span><span class="sxs-lookup"><span data-stu-id="cb92f-130">X</span></span>        |
  | <span data-ttu-id="cb92f-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="cb92f-131">ReasonCodeId</span></span>      | <span data-ttu-id="cb92f-132">文字列</span><span class="sxs-lookup"><span data-stu-id="cb92f-132">String</span></span>    |          |
  | <span data-ttu-id="cb92f-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="cb92f-133">PersonnelNumber</span></span>   | <span data-ttu-id="cb92f-134">文字列</span><span class="sxs-lookup"><span data-stu-id="cb92f-134">String</span></span>    | <span data-ttu-id="cb92f-135">x</span><span class="sxs-lookup"><span data-stu-id="cb92f-135">X</span></span>        |
  | <span data-ttu-id="cb92f-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="cb92f-136">RequestDate</span></span>       | <span data-ttu-id="cb92f-137">日</span><span class="sxs-lookup"><span data-stu-id="cb92f-137">Date</span></span>      | <span data-ttu-id="cb92f-138">x</span><span class="sxs-lookup"><span data-stu-id="cb92f-138">X</span></span>        |
  | <span data-ttu-id="cb92f-139">コメント</span><span class="sxs-lookup"><span data-stu-id="cb92f-139">Comment</span></span>           | <span data-ttu-id="cb92f-140">文字列</span><span class="sxs-lookup"><span data-stu-id="cb92f-140">String</span></span>    |          |
  | <span data-ttu-id="cb92f-141">ステータス</span><span class="sxs-lookup"><span data-stu-id="cb92f-141">Status</span></span>            | <span data-ttu-id="cb92f-142">列挙</span><span class="sxs-lookup"><span data-stu-id="cb92f-142">Enum</span></span>      | <span data-ttu-id="cb92f-143">x</span><span class="sxs-lookup"><span data-stu-id="cb92f-143">X</span></span>        |
  | <span data-ttu-id="cb92f-144">量</span><span class="sxs-lookup"><span data-stu-id="cb92f-144">Amount</span></span>            | <span data-ttu-id="cb92f-145">実績</span><span class="sxs-lookup"><span data-stu-id="cb92f-145">Real</span></span>      |          |
  | <span data-ttu-id="cb92f-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="cb92f-146">HalfDayDefinition</span></span> | <span data-ttu-id="cb92f-147">列挙</span><span class="sxs-lookup"><span data-stu-id="cb92f-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="cb92f-148">アクション</span><span class="sxs-lookup"><span data-stu-id="cb92f-148">Actions</span></span>

 | <span data-ttu-id="cb92f-149">アクション名</span><span class="sxs-lookup"><span data-stu-id="cb92f-149">Action Name</span></span>                               | <span data-ttu-id="cb92f-150">説明</span><span class="sxs-lookup"><span data-stu-id="cb92f-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="cb92f-151">送信</span><span class="sxs-lookup"><span data-stu-id="cb92f-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="cb92f-152">ワークフローで処理される要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="cb92f-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cb92f-153">参照</span><span class="sxs-lookup"><span data-stu-id="cb92f-153">See also</span></span>

- [<span data-ttu-id="cb92f-154">休暇申請をワークフローに送信する</span><span class="sxs-lookup"><span data-stu-id="cb92f-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="cb92f-155">認証</span><span class="sxs-lookup"><span data-stu-id="cb92f-155">Authentication</span></span>](hr-developer-api-authentication.md)
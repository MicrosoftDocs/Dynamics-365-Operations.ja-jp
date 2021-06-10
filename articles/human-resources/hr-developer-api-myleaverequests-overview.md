---
title: MyLeaveRequests の概要
description: Microsoft Dynamics 365 Human Resourcesの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054959"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="d353d-103">MyLeaveRequests の概要</span><span class="sxs-lookup"><span data-stu-id="d353d-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d353d-104">Microsoft Dynamics 365 Human Resourcesの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。</span><span class="sxs-lookup"><span data-stu-id="d353d-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="d353d-105">キー</span><span class="sxs-lookup"><span data-stu-id="d353d-105">Key</span></span>

  | <span data-ttu-id="d353d-106">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="d353d-106">Property Name</span></span> | <span data-ttu-id="d353d-107">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="d353d-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="d353d-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="d353d-108">dataAreaId</span></span>    | <span data-ttu-id="d353d-109">文字列</span><span class="sxs-lookup"><span data-stu-id="d353d-109">String</span></span>    |
  | <span data-ttu-id="d353d-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="d353d-110">RequestId</span></span>     | <span data-ttu-id="d353d-111">文字列</span><span class="sxs-lookup"><span data-stu-id="d353d-111">String</span></span>    |
  | <span data-ttu-id="d353d-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="d353d-112">LeaveType</span></span>     | <span data-ttu-id="d353d-113">文字列</span><span class="sxs-lookup"><span data-stu-id="d353d-113">String</span></span>    |
  | <span data-ttu-id="d353d-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="d353d-114">LeaveDate</span></span>     | <span data-ttu-id="d353d-115">日</span><span class="sxs-lookup"><span data-stu-id="d353d-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="d353d-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="d353d-116">Properties</span></span>

  | <span data-ttu-id="d353d-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="d353d-117">Property Name</span></span>     | <span data-ttu-id="d353d-118">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="d353d-118">Data Type</span></span> | <span data-ttu-id="d353d-119">必須</span><span class="sxs-lookup"><span data-stu-id="d353d-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="d353d-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="d353d-120">dataAreaId</span></span>        | <span data-ttu-id="d353d-121">文字列</span><span class="sxs-lookup"><span data-stu-id="d353d-121">String</span></span>    | <span data-ttu-id="d353d-122">x</span><span class="sxs-lookup"><span data-stu-id="d353d-122">X</span></span>        |
  | <span data-ttu-id="d353d-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="d353d-123">RequestId</span></span>         | <span data-ttu-id="d353d-124">文字列</span><span class="sxs-lookup"><span data-stu-id="d353d-124">String</span></span>    | <span data-ttu-id="d353d-125">x</span><span class="sxs-lookup"><span data-stu-id="d353d-125">X</span></span>        |
  | <span data-ttu-id="d353d-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="d353d-126">LeaveType</span></span>         | <span data-ttu-id="d353d-127">文字列</span><span class="sxs-lookup"><span data-stu-id="d353d-127">String</span></span>    | <span data-ttu-id="d353d-128">x</span><span class="sxs-lookup"><span data-stu-id="d353d-128">X</span></span>        |
  | <span data-ttu-id="d353d-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="d353d-129">LeaveDate</span></span>         | <span data-ttu-id="d353d-130">日</span><span class="sxs-lookup"><span data-stu-id="d353d-130">Date</span></span>      | <span data-ttu-id="d353d-131">x</span><span class="sxs-lookup"><span data-stu-id="d353d-131">X</span></span>        |
  | <span data-ttu-id="d353d-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="d353d-132">ReasonCodeId</span></span>      | <span data-ttu-id="d353d-133">文字列</span><span class="sxs-lookup"><span data-stu-id="d353d-133">String</span></span>    |          |
  | <span data-ttu-id="d353d-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="d353d-134">PersonnelNumber</span></span>   | <span data-ttu-id="d353d-135">文字列</span><span class="sxs-lookup"><span data-stu-id="d353d-135">String</span></span>    | <span data-ttu-id="d353d-136">x</span><span class="sxs-lookup"><span data-stu-id="d353d-136">X</span></span>        |
  | <span data-ttu-id="d353d-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="d353d-137">RequestDate</span></span>       | <span data-ttu-id="d353d-138">日</span><span class="sxs-lookup"><span data-stu-id="d353d-138">Date</span></span>      | <span data-ttu-id="d353d-139">x</span><span class="sxs-lookup"><span data-stu-id="d353d-139">X</span></span>        |
  | <span data-ttu-id="d353d-140">コメント</span><span class="sxs-lookup"><span data-stu-id="d353d-140">Comment</span></span>           | <span data-ttu-id="d353d-141">文字列</span><span class="sxs-lookup"><span data-stu-id="d353d-141">String</span></span>    |          |
  | <span data-ttu-id="d353d-142">ステータス</span><span class="sxs-lookup"><span data-stu-id="d353d-142">Status</span></span>            | <span data-ttu-id="d353d-143">列挙</span><span class="sxs-lookup"><span data-stu-id="d353d-143">Enum</span></span>      | <span data-ttu-id="d353d-144">x</span><span class="sxs-lookup"><span data-stu-id="d353d-144">X</span></span>        |
  | <span data-ttu-id="d353d-145">量</span><span class="sxs-lookup"><span data-stu-id="d353d-145">Amount</span></span>            | <span data-ttu-id="d353d-146">実績</span><span class="sxs-lookup"><span data-stu-id="d353d-146">Real</span></span>      |          |
  | <span data-ttu-id="d353d-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="d353d-147">HalfDayDefinition</span></span> | <span data-ttu-id="d353d-148">列挙</span><span class="sxs-lookup"><span data-stu-id="d353d-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="d353d-149">アクション</span><span class="sxs-lookup"><span data-stu-id="d353d-149">Actions</span></span>

 | <span data-ttu-id="d353d-150">アクション名</span><span class="sxs-lookup"><span data-stu-id="d353d-150">Action Name</span></span>                               | <span data-ttu-id="d353d-151">説明</span><span class="sxs-lookup"><span data-stu-id="d353d-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="d353d-152">送信</span><span class="sxs-lookup"><span data-stu-id="d353d-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="d353d-153">ワークフローで処理される要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="d353d-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d353d-154">参照</span><span class="sxs-lookup"><span data-stu-id="d353d-154">See also</span></span>

- [<span data-ttu-id="d353d-155">休暇申請をワークフローに送信する</span><span class="sxs-lookup"><span data-stu-id="d353d-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="d353d-156">認証</span><span class="sxs-lookup"><span data-stu-id="d353d-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
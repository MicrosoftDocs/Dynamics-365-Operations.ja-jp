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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803636"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="28414-103">MyLeaveRequests の概要</span><span class="sxs-lookup"><span data-stu-id="28414-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="28414-104">Microsoft Dynamics 365 Human Resourcesの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。</span><span class="sxs-lookup"><span data-stu-id="28414-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="28414-105">キー</span><span class="sxs-lookup"><span data-stu-id="28414-105">Key</span></span>

  | <span data-ttu-id="28414-106">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="28414-106">Property Name</span></span> | <span data-ttu-id="28414-107">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="28414-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="28414-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="28414-108">dataAreaId</span></span>    | <span data-ttu-id="28414-109">文字列</span><span class="sxs-lookup"><span data-stu-id="28414-109">String</span></span>    |
  | <span data-ttu-id="28414-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="28414-110">RequestId</span></span>     | <span data-ttu-id="28414-111">文字列</span><span class="sxs-lookup"><span data-stu-id="28414-111">String</span></span>    |
  | <span data-ttu-id="28414-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="28414-112">LeaveType</span></span>     | <span data-ttu-id="28414-113">文字列</span><span class="sxs-lookup"><span data-stu-id="28414-113">String</span></span>    |
  | <span data-ttu-id="28414-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="28414-114">LeaveDate</span></span>     | <span data-ttu-id="28414-115">日</span><span class="sxs-lookup"><span data-stu-id="28414-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="28414-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="28414-116">Properties</span></span>

  | <span data-ttu-id="28414-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="28414-117">Property Name</span></span>     | <span data-ttu-id="28414-118">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="28414-118">Data Type</span></span> | <span data-ttu-id="28414-119">必須</span><span class="sxs-lookup"><span data-stu-id="28414-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="28414-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="28414-120">dataAreaId</span></span>        | <span data-ttu-id="28414-121">文字列</span><span class="sxs-lookup"><span data-stu-id="28414-121">String</span></span>    | <span data-ttu-id="28414-122">x</span><span class="sxs-lookup"><span data-stu-id="28414-122">X</span></span>        |
  | <span data-ttu-id="28414-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="28414-123">RequestId</span></span>         | <span data-ttu-id="28414-124">文字列</span><span class="sxs-lookup"><span data-stu-id="28414-124">String</span></span>    | <span data-ttu-id="28414-125">x</span><span class="sxs-lookup"><span data-stu-id="28414-125">X</span></span>        |
  | <span data-ttu-id="28414-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="28414-126">LeaveType</span></span>         | <span data-ttu-id="28414-127">文字列</span><span class="sxs-lookup"><span data-stu-id="28414-127">String</span></span>    | <span data-ttu-id="28414-128">x</span><span class="sxs-lookup"><span data-stu-id="28414-128">X</span></span>        |
  | <span data-ttu-id="28414-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="28414-129">LeaveDate</span></span>         | <span data-ttu-id="28414-130">日</span><span class="sxs-lookup"><span data-stu-id="28414-130">Date</span></span>      | <span data-ttu-id="28414-131">x</span><span class="sxs-lookup"><span data-stu-id="28414-131">X</span></span>        |
  | <span data-ttu-id="28414-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="28414-132">ReasonCodeId</span></span>      | <span data-ttu-id="28414-133">文字列</span><span class="sxs-lookup"><span data-stu-id="28414-133">String</span></span>    |          |
  | <span data-ttu-id="28414-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="28414-134">PersonnelNumber</span></span>   | <span data-ttu-id="28414-135">文字列</span><span class="sxs-lookup"><span data-stu-id="28414-135">String</span></span>    | <span data-ttu-id="28414-136">x</span><span class="sxs-lookup"><span data-stu-id="28414-136">X</span></span>        |
  | <span data-ttu-id="28414-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="28414-137">RequestDate</span></span>       | <span data-ttu-id="28414-138">日</span><span class="sxs-lookup"><span data-stu-id="28414-138">Date</span></span>      | <span data-ttu-id="28414-139">x</span><span class="sxs-lookup"><span data-stu-id="28414-139">X</span></span>        |
  | <span data-ttu-id="28414-140">コメント</span><span class="sxs-lookup"><span data-stu-id="28414-140">Comment</span></span>           | <span data-ttu-id="28414-141">文字列</span><span class="sxs-lookup"><span data-stu-id="28414-141">String</span></span>    |          |
  | <span data-ttu-id="28414-142">ステータス</span><span class="sxs-lookup"><span data-stu-id="28414-142">Status</span></span>            | <span data-ttu-id="28414-143">列挙</span><span class="sxs-lookup"><span data-stu-id="28414-143">Enum</span></span>      | <span data-ttu-id="28414-144">x</span><span class="sxs-lookup"><span data-stu-id="28414-144">X</span></span>        |
  | <span data-ttu-id="28414-145">量</span><span class="sxs-lookup"><span data-stu-id="28414-145">Amount</span></span>            | <span data-ttu-id="28414-146">実績</span><span class="sxs-lookup"><span data-stu-id="28414-146">Real</span></span>      |          |
  | <span data-ttu-id="28414-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="28414-147">HalfDayDefinition</span></span> | <span data-ttu-id="28414-148">列挙</span><span class="sxs-lookup"><span data-stu-id="28414-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="28414-149">アクション</span><span class="sxs-lookup"><span data-stu-id="28414-149">Actions</span></span>

 | <span data-ttu-id="28414-150">アクション名</span><span class="sxs-lookup"><span data-stu-id="28414-150">Action Name</span></span>                               | <span data-ttu-id="28414-151">説明</span><span class="sxs-lookup"><span data-stu-id="28414-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="28414-152">送信</span><span class="sxs-lookup"><span data-stu-id="28414-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="28414-153">ワークフローで処理される要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="28414-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="28414-154">参照</span><span class="sxs-lookup"><span data-stu-id="28414-154">See also</span></span>

- [<span data-ttu-id="28414-155">休暇申請をワークフローに送信する</span><span class="sxs-lookup"><span data-stu-id="28414-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="28414-156">認証</span><span class="sxs-lookup"><span data-stu-id="28414-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
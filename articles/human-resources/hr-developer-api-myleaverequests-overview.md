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
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092040"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="10bbf-103">MyLeaveRequests の概要</span><span class="sxs-lookup"><span data-stu-id="10bbf-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="10bbf-104">Microsoft Dynamics 365 Human Resourcesの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。</span><span class="sxs-lookup"><span data-stu-id="10bbf-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="10bbf-105">キー</span><span class="sxs-lookup"><span data-stu-id="10bbf-105">Key</span></span>

  | <span data-ttu-id="10bbf-106">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="10bbf-106">Property Name</span></span> | <span data-ttu-id="10bbf-107">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="10bbf-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="10bbf-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="10bbf-108">dataAreaId</span></span>    | <span data-ttu-id="10bbf-109">文字列</span><span class="sxs-lookup"><span data-stu-id="10bbf-109">String</span></span>    |
  | <span data-ttu-id="10bbf-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="10bbf-110">RequestId</span></span>     | <span data-ttu-id="10bbf-111">文字列</span><span class="sxs-lookup"><span data-stu-id="10bbf-111">String</span></span>    |
  | <span data-ttu-id="10bbf-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="10bbf-112">LeaveType</span></span>     | <span data-ttu-id="10bbf-113">文字列</span><span class="sxs-lookup"><span data-stu-id="10bbf-113">String</span></span>    |
  | <span data-ttu-id="10bbf-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="10bbf-114">LeaveDate</span></span>     | <span data-ttu-id="10bbf-115">日</span><span class="sxs-lookup"><span data-stu-id="10bbf-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="10bbf-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="10bbf-116">Properties</span></span>

  | <span data-ttu-id="10bbf-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="10bbf-117">Property Name</span></span>     | <span data-ttu-id="10bbf-118">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="10bbf-118">Data Type</span></span> | <span data-ttu-id="10bbf-119">必須</span><span class="sxs-lookup"><span data-stu-id="10bbf-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="10bbf-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="10bbf-120">dataAreaId</span></span>        | <span data-ttu-id="10bbf-121">文字列</span><span class="sxs-lookup"><span data-stu-id="10bbf-121">String</span></span>    | <span data-ttu-id="10bbf-122">x</span><span class="sxs-lookup"><span data-stu-id="10bbf-122">X</span></span>        |
  | <span data-ttu-id="10bbf-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="10bbf-123">RequestId</span></span>         | <span data-ttu-id="10bbf-124">文字列</span><span class="sxs-lookup"><span data-stu-id="10bbf-124">String</span></span>    | <span data-ttu-id="10bbf-125">x</span><span class="sxs-lookup"><span data-stu-id="10bbf-125">X</span></span>        |
  | <span data-ttu-id="10bbf-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="10bbf-126">LeaveType</span></span>         | <span data-ttu-id="10bbf-127">文字列</span><span class="sxs-lookup"><span data-stu-id="10bbf-127">String</span></span>    | <span data-ttu-id="10bbf-128">x</span><span class="sxs-lookup"><span data-stu-id="10bbf-128">X</span></span>        |
  | <span data-ttu-id="10bbf-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="10bbf-129">LeaveDate</span></span>         | <span data-ttu-id="10bbf-130">日</span><span class="sxs-lookup"><span data-stu-id="10bbf-130">Date</span></span>      | <span data-ttu-id="10bbf-131">x</span><span class="sxs-lookup"><span data-stu-id="10bbf-131">X</span></span>        |
  | <span data-ttu-id="10bbf-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="10bbf-132">ReasonCodeId</span></span>      | <span data-ttu-id="10bbf-133">文字列</span><span class="sxs-lookup"><span data-stu-id="10bbf-133">String</span></span>    |          |
  | <span data-ttu-id="10bbf-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="10bbf-134">PersonnelNumber</span></span>   | <span data-ttu-id="10bbf-135">文字列</span><span class="sxs-lookup"><span data-stu-id="10bbf-135">String</span></span>    | <span data-ttu-id="10bbf-136">x</span><span class="sxs-lookup"><span data-stu-id="10bbf-136">X</span></span>        |
  | <span data-ttu-id="10bbf-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="10bbf-137">RequestDate</span></span>       | <span data-ttu-id="10bbf-138">日</span><span class="sxs-lookup"><span data-stu-id="10bbf-138">Date</span></span>      | <span data-ttu-id="10bbf-139">x</span><span class="sxs-lookup"><span data-stu-id="10bbf-139">X</span></span>        |
  | <span data-ttu-id="10bbf-140">コメント</span><span class="sxs-lookup"><span data-stu-id="10bbf-140">Comment</span></span>           | <span data-ttu-id="10bbf-141">文字列</span><span class="sxs-lookup"><span data-stu-id="10bbf-141">String</span></span>    |          |
  | <span data-ttu-id="10bbf-142">ステータス</span><span class="sxs-lookup"><span data-stu-id="10bbf-142">Status</span></span>            | <span data-ttu-id="10bbf-143">列挙</span><span class="sxs-lookup"><span data-stu-id="10bbf-143">Enum</span></span>      | <span data-ttu-id="10bbf-144">x</span><span class="sxs-lookup"><span data-stu-id="10bbf-144">X</span></span>        |
  | <span data-ttu-id="10bbf-145">量</span><span class="sxs-lookup"><span data-stu-id="10bbf-145">Amount</span></span>            | <span data-ttu-id="10bbf-146">実績</span><span class="sxs-lookup"><span data-stu-id="10bbf-146">Real</span></span>      |          |
  | <span data-ttu-id="10bbf-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="10bbf-147">HalfDayDefinition</span></span> | <span data-ttu-id="10bbf-148">列挙</span><span class="sxs-lookup"><span data-stu-id="10bbf-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="10bbf-149">アクション</span><span class="sxs-lookup"><span data-stu-id="10bbf-149">Actions</span></span>

 | <span data-ttu-id="10bbf-150">アクション名</span><span class="sxs-lookup"><span data-stu-id="10bbf-150">Action Name</span></span>                               | <span data-ttu-id="10bbf-151">説明</span><span class="sxs-lookup"><span data-stu-id="10bbf-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="10bbf-152">送信</span><span class="sxs-lookup"><span data-stu-id="10bbf-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="10bbf-153">ワークフローで処理される要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="10bbf-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="10bbf-154">参照</span><span class="sxs-lookup"><span data-stu-id="10bbf-154">See also</span></span>

- [<span data-ttu-id="10bbf-155">休暇申請をワークフローに送信する</span><span class="sxs-lookup"><span data-stu-id="10bbf-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="10bbf-156">認証</span><span class="sxs-lookup"><span data-stu-id="10bbf-156">Authentication</span></span>](hr-developer-api-authentication.md)
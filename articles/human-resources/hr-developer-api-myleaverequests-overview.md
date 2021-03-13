---
title: MyLeaveRequests の概要
description: Microsoft Dynamics 365 Human Resourcesの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115539"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="6aa44-103">MyLeaveRequests の概要</span><span class="sxs-lookup"><span data-stu-id="6aa44-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="6aa44-104">Microsoft Dynamics 365 Human Resourcesの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。</span><span class="sxs-lookup"><span data-stu-id="6aa44-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="6aa44-105">キー</span><span class="sxs-lookup"><span data-stu-id="6aa44-105">Key</span></span>

  | <span data-ttu-id="6aa44-106">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="6aa44-106">Property Name</span></span> | <span data-ttu-id="6aa44-107">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="6aa44-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="6aa44-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="6aa44-108">dataAreaId</span></span>    | <span data-ttu-id="6aa44-109">文字列</span><span class="sxs-lookup"><span data-stu-id="6aa44-109">String</span></span>    |
  | <span data-ttu-id="6aa44-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="6aa44-110">RequestId</span></span>     | <span data-ttu-id="6aa44-111">文字列</span><span class="sxs-lookup"><span data-stu-id="6aa44-111">String</span></span>    |
  | <span data-ttu-id="6aa44-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="6aa44-112">LeaveType</span></span>     | <span data-ttu-id="6aa44-113">文字列</span><span class="sxs-lookup"><span data-stu-id="6aa44-113">String</span></span>    |
  | <span data-ttu-id="6aa44-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="6aa44-114">LeaveDate</span></span>     | <span data-ttu-id="6aa44-115">日</span><span class="sxs-lookup"><span data-stu-id="6aa44-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="6aa44-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="6aa44-116">Properties</span></span>

  | <span data-ttu-id="6aa44-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="6aa44-117">Property Name</span></span>     | <span data-ttu-id="6aa44-118">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="6aa44-118">Data Type</span></span> | <span data-ttu-id="6aa44-119">必須</span><span class="sxs-lookup"><span data-stu-id="6aa44-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="6aa44-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="6aa44-120">dataAreaId</span></span>        | <span data-ttu-id="6aa44-121">文字列</span><span class="sxs-lookup"><span data-stu-id="6aa44-121">String</span></span>    | <span data-ttu-id="6aa44-122">x</span><span class="sxs-lookup"><span data-stu-id="6aa44-122">X</span></span>        |
  | <span data-ttu-id="6aa44-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="6aa44-123">RequestId</span></span>         | <span data-ttu-id="6aa44-124">文字列</span><span class="sxs-lookup"><span data-stu-id="6aa44-124">String</span></span>    | <span data-ttu-id="6aa44-125">x</span><span class="sxs-lookup"><span data-stu-id="6aa44-125">X</span></span>        |
  | <span data-ttu-id="6aa44-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="6aa44-126">LeaveType</span></span>         | <span data-ttu-id="6aa44-127">文字列</span><span class="sxs-lookup"><span data-stu-id="6aa44-127">String</span></span>    | <span data-ttu-id="6aa44-128">x</span><span class="sxs-lookup"><span data-stu-id="6aa44-128">X</span></span>        |
  | <span data-ttu-id="6aa44-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="6aa44-129">LeaveDate</span></span>         | <span data-ttu-id="6aa44-130">日</span><span class="sxs-lookup"><span data-stu-id="6aa44-130">Date</span></span>      | <span data-ttu-id="6aa44-131">x</span><span class="sxs-lookup"><span data-stu-id="6aa44-131">X</span></span>        |
  | <span data-ttu-id="6aa44-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="6aa44-132">ReasonCodeId</span></span>      | <span data-ttu-id="6aa44-133">文字列</span><span class="sxs-lookup"><span data-stu-id="6aa44-133">String</span></span>    |          |
  | <span data-ttu-id="6aa44-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="6aa44-134">PersonnelNumber</span></span>   | <span data-ttu-id="6aa44-135">文字列</span><span class="sxs-lookup"><span data-stu-id="6aa44-135">String</span></span>    | <span data-ttu-id="6aa44-136">x</span><span class="sxs-lookup"><span data-stu-id="6aa44-136">X</span></span>        |
  | <span data-ttu-id="6aa44-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="6aa44-137">RequestDate</span></span>       | <span data-ttu-id="6aa44-138">日</span><span class="sxs-lookup"><span data-stu-id="6aa44-138">Date</span></span>      | <span data-ttu-id="6aa44-139">x</span><span class="sxs-lookup"><span data-stu-id="6aa44-139">X</span></span>        |
  | <span data-ttu-id="6aa44-140">コメント</span><span class="sxs-lookup"><span data-stu-id="6aa44-140">Comment</span></span>           | <span data-ttu-id="6aa44-141">文字列</span><span class="sxs-lookup"><span data-stu-id="6aa44-141">String</span></span>    |          |
  | <span data-ttu-id="6aa44-142">ステータス</span><span class="sxs-lookup"><span data-stu-id="6aa44-142">Status</span></span>            | <span data-ttu-id="6aa44-143">列挙</span><span class="sxs-lookup"><span data-stu-id="6aa44-143">Enum</span></span>      | <span data-ttu-id="6aa44-144">x</span><span class="sxs-lookup"><span data-stu-id="6aa44-144">X</span></span>        |
  | <span data-ttu-id="6aa44-145">量</span><span class="sxs-lookup"><span data-stu-id="6aa44-145">Amount</span></span>            | <span data-ttu-id="6aa44-146">実績</span><span class="sxs-lookup"><span data-stu-id="6aa44-146">Real</span></span>      |          |
  | <span data-ttu-id="6aa44-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="6aa44-147">HalfDayDefinition</span></span> | <span data-ttu-id="6aa44-148">列挙</span><span class="sxs-lookup"><span data-stu-id="6aa44-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="6aa44-149">アクション</span><span class="sxs-lookup"><span data-stu-id="6aa44-149">Actions</span></span>

 | <span data-ttu-id="6aa44-150">アクション名</span><span class="sxs-lookup"><span data-stu-id="6aa44-150">Action Name</span></span>                               | <span data-ttu-id="6aa44-151">説明</span><span class="sxs-lookup"><span data-stu-id="6aa44-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="6aa44-152">送信</span><span class="sxs-lookup"><span data-stu-id="6aa44-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="6aa44-153">ワークフローで処理される要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="6aa44-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6aa44-154">参照</span><span class="sxs-lookup"><span data-stu-id="6aa44-154">See also</span></span>

- [<span data-ttu-id="6aa44-155">休暇申請をワークフローに送信する</span><span class="sxs-lookup"><span data-stu-id="6aa44-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="6aa44-156">認証</span><span class="sxs-lookup"><span data-stu-id="6aa44-156">Authentication</span></span>](hr-developer-api-authentication.md)
---
title: MyLeaveRequests の概要
description: この記事では、MyLeaveRequests エンティティの参照資料を提供します。
author: gboyko
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: gboyko
ms.search.validFrom: 2019-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 3bf2aa784d85882d657c1d0f00f1417534a89dc3
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833197"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="7452e-103">MyLeaveRequests の概要</span><span class="sxs-lookup"><span data-stu-id="7452e-103">MyLeaveRequests overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7452e-104">Microsoft Dynamics 365 Talentの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。</span><span class="sxs-lookup"><span data-stu-id="7452e-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Talent provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="7452e-105">キー</span><span class="sxs-lookup"><span data-stu-id="7452e-105">Key</span></span>

  | <span data-ttu-id="7452e-106">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="7452e-106">Property Name</span></span> | <span data-ttu-id="7452e-107">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="7452e-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="7452e-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="7452e-108">dataAreaId</span></span>    | <span data-ttu-id="7452e-109">文字列</span><span class="sxs-lookup"><span data-stu-id="7452e-109">String</span></span>    |
  | <span data-ttu-id="7452e-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="7452e-110">RequestId</span></span>     | <span data-ttu-id="7452e-111">文字列</span><span class="sxs-lookup"><span data-stu-id="7452e-111">String</span></span>    |
  | <span data-ttu-id="7452e-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="7452e-112">LeaveType</span></span>     | <span data-ttu-id="7452e-113">文字列</span><span class="sxs-lookup"><span data-stu-id="7452e-113">String</span></span>    |
  | <span data-ttu-id="7452e-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="7452e-114">LeaveDate</span></span>     | <span data-ttu-id="7452e-115">日</span><span class="sxs-lookup"><span data-stu-id="7452e-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="7452e-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7452e-116">Properties</span></span>

  | <span data-ttu-id="7452e-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="7452e-117">Property Name</span></span>     | <span data-ttu-id="7452e-118">データ タイプ</span><span class="sxs-lookup"><span data-stu-id="7452e-118">Data Type</span></span> | <span data-ttu-id="7452e-119">必須</span><span class="sxs-lookup"><span data-stu-id="7452e-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="7452e-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="7452e-120">dataAreaId</span></span>        | <span data-ttu-id="7452e-121">文字列</span><span class="sxs-lookup"><span data-stu-id="7452e-121">String</span></span>    | <span data-ttu-id="7452e-122">x</span><span class="sxs-lookup"><span data-stu-id="7452e-122">X</span></span>        |
  | <span data-ttu-id="7452e-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="7452e-123">RequestId</span></span>         | <span data-ttu-id="7452e-124">文字列</span><span class="sxs-lookup"><span data-stu-id="7452e-124">String</span></span>    | <span data-ttu-id="7452e-125">x</span><span class="sxs-lookup"><span data-stu-id="7452e-125">X</span></span>        |
  | <span data-ttu-id="7452e-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="7452e-126">LeaveType</span></span>         | <span data-ttu-id="7452e-127">文字列</span><span class="sxs-lookup"><span data-stu-id="7452e-127">String</span></span>    | <span data-ttu-id="7452e-128">x</span><span class="sxs-lookup"><span data-stu-id="7452e-128">X</span></span>        |
  | <span data-ttu-id="7452e-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="7452e-129">LeaveDate</span></span>         | <span data-ttu-id="7452e-130">日</span><span class="sxs-lookup"><span data-stu-id="7452e-130">Date</span></span>      | <span data-ttu-id="7452e-131">x</span><span class="sxs-lookup"><span data-stu-id="7452e-131">X</span></span>        |
  | <span data-ttu-id="7452e-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="7452e-132">ReasonCodeId</span></span>      | <span data-ttu-id="7452e-133">文字列</span><span class="sxs-lookup"><span data-stu-id="7452e-133">String</span></span>    |          |
  | <span data-ttu-id="7452e-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="7452e-134">PersonnelNumber</span></span>   | <span data-ttu-id="7452e-135">文字列</span><span class="sxs-lookup"><span data-stu-id="7452e-135">String</span></span>    | <span data-ttu-id="7452e-136">x</span><span class="sxs-lookup"><span data-stu-id="7452e-136">X</span></span>        |
  | <span data-ttu-id="7452e-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="7452e-137">RequestDate</span></span>       | <span data-ttu-id="7452e-138">日</span><span class="sxs-lookup"><span data-stu-id="7452e-138">Date</span></span>      | <span data-ttu-id="7452e-139">x</span><span class="sxs-lookup"><span data-stu-id="7452e-139">X</span></span>        |
  | <span data-ttu-id="7452e-140">コメント</span><span class="sxs-lookup"><span data-stu-id="7452e-140">Comment</span></span>           | <span data-ttu-id="7452e-141">文字列</span><span class="sxs-lookup"><span data-stu-id="7452e-141">String</span></span>    |          |
  | <span data-ttu-id="7452e-142">ステータス</span><span class="sxs-lookup"><span data-stu-id="7452e-142">Status</span></span>            | <span data-ttu-id="7452e-143">列挙</span><span class="sxs-lookup"><span data-stu-id="7452e-143">Enum</span></span>      | <span data-ttu-id="7452e-144">x</span><span class="sxs-lookup"><span data-stu-id="7452e-144">X</span></span>        |
  | <span data-ttu-id="7452e-145">量</span><span class="sxs-lookup"><span data-stu-id="7452e-145">Amount</span></span>            | <span data-ttu-id="7452e-146">実績</span><span class="sxs-lookup"><span data-stu-id="7452e-146">Real</span></span>      |          |
  | <span data-ttu-id="7452e-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="7452e-147">HalfDayDefinition</span></span> | <span data-ttu-id="7452e-148">列挙</span><span class="sxs-lookup"><span data-stu-id="7452e-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="7452e-149">アクション</span><span class="sxs-lookup"><span data-stu-id="7452e-149">Actions</span></span>

 | <span data-ttu-id="7452e-150">アクション名</span><span class="sxs-lookup"><span data-stu-id="7452e-150">Action Name</span></span>                               | <span data-ttu-id="7452e-151">説明</span><span class="sxs-lookup"><span data-stu-id="7452e-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="7452e-152">送信</span><span class="sxs-lookup"><span data-stu-id="7452e-152">submit</span></span>](api-myleaverequests-submit.md)   | <span data-ttu-id="7452e-153">ワークフローで処理される要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="7452e-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7452e-154">参照</span><span class="sxs-lookup"><span data-stu-id="7452e-154">See also</span></span>

[<span data-ttu-id="7452e-155">ワークフローへの休暇要求の送信</span><span class="sxs-lookup"><span data-stu-id="7452e-155">Submit a leave request to workflow</span></span>](api-myleaverequests-submit.md)
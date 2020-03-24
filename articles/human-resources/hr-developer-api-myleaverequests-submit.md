---
title: 休暇申請をワークフローに送信する
description: Microsoft Dynamics 365 Human Resources では、MyLeaveRequests submit () アプリケーション プログラミング インターフェイス (API) を使用して、休暇要求をワークフローに送信できます。
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
ms.openlocfilehash: 7552a4c921dc4a88034b5d2c87d5a9b47d699ae3
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092017"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="fdd1d-103">休暇申請をワークフローに送信する</span><span class="sxs-lookup"><span data-stu-id="fdd1d-103">Submit a leave request to workflow</span></span>

<span data-ttu-id="fdd1d-104">Microsoft Dynamics 365 Human Resources では、MyLeaveRequests submit () アプリケーション プログラミング インターフェイス (API) を使用して、休暇要求をワークフローに送信できます。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="fdd1d-105">この API は、MyLeaveRequests OData エンティティでアクションとして公開されます。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fdd1d-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="fdd1d-106">Prerequisites</span></span>

<span data-ttu-id="fdd1d-107">休暇要求はデータベースに保存する必要があり、MyLeaveRequests エンティティを通じて取得できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="fdd1d-108">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="fdd1d-108">Permissions</span></span>

<span data-ttu-id="fdd1d-109">この API を呼び出すには、次のアクセス許可の 1 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="fdd1d-110">アクセス許可およびその選択方法の詳細については、[認証](hr-developer-api-authentication.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="fdd1d-111">アクセス許可のタイプ</span><span class="sxs-lookup"><span data-stu-id="fdd1d-111">Permission type</span></span>                    | <span data-ttu-id="fdd1d-112">アクセス許可 (最小の特権から最大の特権)</span><span class="sxs-lookup"><span data-stu-id="fdd1d-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="fdd1d-113">委任 (勤務先または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="fdd1d-113">Delegated (work or school account)</span></span> | <span data-ttu-id="fdd1d-114">ユーザー \_ 偽装</span><span class="sxs-lookup"><span data-stu-id="fdd1d-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="fdd1d-115">HTTPS 要求</span><span class="sxs-lookup"><span data-stu-id="fdd1d-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="fdd1d-116">この要求は OData の標準に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-116">The request conforms to OData standards.</span></span> <span data-ttu-id="fdd1d-117">{requestId}、{leaveType}、{leaveDate}、{dataArea} の各パラメーターは、MyLeaveRequests エンティティの複合ナチュラル キーを構成するフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="fdd1d-118">MyLeaveRequests エンティティのフィールドは休暇要求の個々の行を参照しますが、送信 API を呼び出すと、休暇要求全体 (すべての行) がワークフローに送信されます。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="fdd1d-119">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="fdd1d-119">Request headers</span></span>

| <span data-ttu-id="fdd1d-120">表題</span><span class="sxs-lookup"><span data-stu-id="fdd1d-120">Header</span></span>         | <span data-ttu-id="fdd1d-121">金額</span><span class="sxs-lookup"><span data-stu-id="fdd1d-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="fdd1d-122">承認</span><span class="sxs-lookup"><span data-stu-id="fdd1d-122">Authorization</span></span>  | <span data-ttu-id="fdd1d-123">ベアラー {token} (必須)</span><span class="sxs-lookup"><span data-stu-id="fdd1d-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="fdd1d-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="fdd1d-124">Content-Type</span></span>   | <span data-ttu-id="fdd1d-125">アプリケーション /json</span><span class="sxs-lookup"><span data-stu-id="fdd1d-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="fdd1d-126">要求の本文</span><span class="sxs-lookup"><span data-stu-id="fdd1d-126">Request body</span></span>

<span data-ttu-id="fdd1d-127">このメソッドの要求の本文を供給しないでください。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="fdd1d-128">応答</span><span class="sxs-lookup"><span data-stu-id="fdd1d-128">Response</span></span>

<span data-ttu-id="fdd1d-129">成功したときの応答は常に **204 No Content (内容なし)** です。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="fdd1d-130">未承認の呼び出し元は、**401 Unauthorized (未承認)** または **403 Forbidden (許可されていません)** といった応答を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="fdd1d-131">送信が失敗した場合 (たとえば検証のため)、応答は **500 Server Error (サーバー エラー)** になり、応答本文には詳細を含む JSON オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="fdd1d-132">例</span><span class="sxs-lookup"><span data-stu-id="fdd1d-132">Example</span></span>

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a><span data-ttu-id="fdd1d-133">検証とエラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="fdd1d-133">Validation and error messages</span></span>

<span data-ttu-id="fdd1d-134">送信 API の呼び出しの一環として、人事管理は送信前にビジネス ロジック検証を実行することにより、休暇要求は送信に対して有効な状態にあることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="fdd1d-135">検証が失敗した場合に応答で受け取る可能性のあるエラー メッセージは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="fdd1d-136">この要求による '{LeaveTypeId}' の残日数は、{date} の最小許容残日数を下回っています。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="fdd1d-137">完了状態の休暇申請要求は送信できません。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="fdd1d-138">変更が行われていないため、要求を送信または保存できません。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="fdd1d-139">量または休暇タイプを追加または更新して、もう一度やり直してください。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="fdd1d-140">入力された休暇申請には、既存の保留中の申請と同じ休暇タイプおよび日付が 1 日以上含まれています。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="fdd1d-141">変更を加えるには、既存の要求を取り消してください。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="fdd1d-142">理由コード '{ReasonCodeId}' は申請における休暇のタイプのいずれにも適用されません。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="fdd1d-143">休暇タイプ '{LeaveTypeId}' には理由コードが必要です。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="fdd1d-144">適切なタイプと理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="fdd1d-145">休暇申請が正常に送信されていません。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="fdd1d-146">休暇申請は下書きの要求として保存されました。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="fdd1d-147">参照</span><span class="sxs-lookup"><span data-stu-id="fdd1d-147">See also</span></span>

- [<span data-ttu-id="fdd1d-148">MyLeaveRequests の概要</span><span class="sxs-lookup"><span data-stu-id="fdd1d-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="fdd1d-149">認証</span><span class="sxs-lookup"><span data-stu-id="fdd1d-149">Authentication</span></span>](hr-developer-api-authentication.md)
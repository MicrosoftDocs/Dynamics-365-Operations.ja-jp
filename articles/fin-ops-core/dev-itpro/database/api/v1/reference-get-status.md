---
title: データベース移動の API - 参照 - v1 - ステータスの取得
description: このトピックでは、データベース移動に関するアプリケーション プログラミング インターフェイス (API) バージョン 1 (v1) の参照資料を提供します。
author: laneswenka
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 57b44810be6c0d1b5d9841036bd350ec97523fce
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744547"
---
# <a name="get-status"></a><span data-ttu-id="25c58-103">ステータスの取得</span><span class="sxs-lookup"><span data-stu-id="25c58-103">Get status</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="25c58-104">進行中の操作のステータスを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="25c58-104">You can get the status of an ongoing operation.</span></span>

## <a name="permissions"></a><span data-ttu-id="25c58-105">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="25c58-105">Permissions</span></span>

<span data-ttu-id="25c58-106">このアプリケーション プログラミング インターフェイス (API) を呼び出すには、次のアクセス許可の 1 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="25c58-106">One of the following permissions is required to call this application programming interface (API).</span></span> <span data-ttu-id="25c58-107">アクセス許可およびその選択方法の詳細については、[認証](../dbmovement-api-authentication.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25c58-107">For more information about permissions and how to select them, see [Authentication](../dbmovement-api-authentication.md).</span></span>

| <span data-ttu-id="25c58-108">アクセス許可のタイプ</span><span class="sxs-lookup"><span data-stu-id="25c58-108">Permission type</span></span>                    | <span data-ttu-id="25c58-109">アクセス許可 (最小の特権から最大の特権)</span><span class="sxs-lookup"><span data-stu-id="25c58-109">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="25c58-110">委任 (勤務先または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="25c58-110">Delegated (work or school account)</span></span> | <span data-ttu-id="25c58-111">ユーザー \_ 偽装</span><span class="sxs-lookup"><span data-stu-id="25c58-111">user\_impersonation</span></span>                                    |

## <a name="http-request"></a><span data-ttu-id="25c58-112">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="25c58-112">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /databasemovement/v1/fetchstatus/project/{projectId}/environment/{environmentId}/operationactivity/{operationactivityId}
```

## <a name="request-headers"></a><span data-ttu-id="25c58-113">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="25c58-113">Request headers</span></span>

| <span data-ttu-id="25c58-114">表題</span><span class="sxs-lookup"><span data-stu-id="25c58-114">Header</span></span>         | <span data-ttu-id="25c58-115">金額</span><span class="sxs-lookup"><span data-stu-id="25c58-115">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="25c58-116">承認</span><span class="sxs-lookup"><span data-stu-id="25c58-116">Authorization</span></span>  | <span data-ttu-id="25c58-117">ベアラー {token} (必須)</span><span class="sxs-lookup"><span data-stu-id="25c58-117">Bearer {token} (required)</span></span> |
| <span data-ttu-id="25c58-118">「x-ms-version」</span><span class="sxs-lookup"><span data-stu-id="25c58-118">'x-ms-version'</span></span> | <span data-ttu-id="25c58-119">「2017-09-15」 (必須)</span><span class="sxs-lookup"><span data-stu-id="25c58-119">'2017-09-15' (required)</span></span>   |
| <span data-ttu-id="25c58-120">Content-Type</span><span class="sxs-lookup"><span data-stu-id="25c58-120">Content-Type</span></span>   | <span data-ttu-id="25c58-121">アプリケーション /json</span><span class="sxs-lookup"><span data-stu-id="25c58-121">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="25c58-122">要求の本文</span><span class="sxs-lookup"><span data-stu-id="25c58-122">Request body</span></span>

<span data-ttu-id="25c58-123">このメソッドの要求の本文を供給しないでください。</span><span class="sxs-lookup"><span data-stu-id="25c58-123">Don't supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="25c58-124">応答</span><span class="sxs-lookup"><span data-stu-id="25c58-124">Response</span></span>

<span data-ttu-id="25c58-125">正しく認証されていない場合を除き、応答は常に **200 OK** 応答になります。</span><span class="sxs-lookup"><span data-stu-id="25c58-125">The response is always a **200 OK** response, unless you aren't correctly authenticated.</span></span> <span data-ttu-id="25c58-126">アクションの成功または失敗を検証するには、**IsSuccess** プロパティを使用してください。</span><span class="sxs-lookup"><span data-stu-id="25c58-126">Be sure to use the **IsSuccess** property to evaluate the success or failure of the action.</span></span>

## <a name="example"></a><span data-ttu-id="25c58-127">例</span><span class="sxs-lookup"><span data-stu-id="25c58-127">Example</span></span>

```http
GET /databasemovement/v1/fetchstatus/project/12345/environment/5362377c-bc37-4f92-b30e-fe0c1e664cc0/operationactivity/55eb4327-9346-4c7b-82bd-fe8ef15112c6
```

```json
{
    "IsSuccess": true,
    "OperationActivityId": "6a90b45f-1764-4077-b924-3f4671540237",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999",
    "ProjectId": 12345,
    "EnvironmentId": "5362377c-bc37-4f92-b30e-fe0c1e664cc0",
    "ActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "CompletionDate": null,
    "OperationStatus": "InProgress"
}
```

### <a name="operationstatus-property"></a><span data-ttu-id="25c58-128">OperationStatus プロパティ</span><span class="sxs-lookup"><span data-stu-id="25c58-128">OperationStatus property</span></span>

| <span data-ttu-id="25c58-129">ステータス</span><span class="sxs-lookup"><span data-stu-id="25c58-129">Status</span></span>             | <span data-ttu-id="25c58-130">説明</span><span class="sxs-lookup"><span data-stu-id="25c58-130">Description</span></span>                                           |
|--------------------|-------------------------------------------------------|
| <span data-ttu-id="25c58-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="25c58-131">NotStarted</span></span>         | <span data-ttu-id="25c58-132">アクションはまだ開始されていません。</span><span class="sxs-lookup"><span data-stu-id="25c58-132">The action hasn't yet been started.</span></span>                   |
| <span data-ttu-id="25c58-133">InProgress</span><span class="sxs-lookup"><span data-stu-id="25c58-133">InProgress</span></span>         | <span data-ttu-id="25c58-134">アクションは進行中です。</span><span class="sxs-lookup"><span data-stu-id="25c58-134">The action is in progress.</span></span>                            |
| <span data-ttu-id="25c58-135">完成</span><span class="sxs-lookup"><span data-stu-id="25c58-135">Completed</span></span>          | <span data-ttu-id="25c58-136">アクションが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="25c58-136">The action was successfully completed.</span></span>                |
| <span data-ttu-id="25c58-137">失敗</span><span class="sxs-lookup"><span data-stu-id="25c58-137">Failed</span></span>             | <span data-ttu-id="25c58-138">アクションが停止されました。</span><span class="sxs-lookup"><span data-stu-id="25c58-138">The action was halted.</span></span>                                |
| <span data-ttu-id="25c58-139">SignedOff</span><span class="sxs-lookup"><span data-stu-id="25c58-139">SignedOff</span></span>          | <span data-ttu-id="25c58-140">アクションが正常に完了し、サインオフしました。</span><span class="sxs-lookup"><span data-stu-id="25c58-140">The action was successfully completed and signed off.</span></span> |
| <span data-ttu-id="25c58-141">中止</span><span class="sxs-lookup"><span data-stu-id="25c58-141">Aborted</span></span>            | <span data-ttu-id="25c58-142">アクションは自動クリーンアップなしでキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="25c58-142">The action was canceled without automated cleanup.</span></span>    |
| <span data-ttu-id="25c58-143">RollbackInProgress</span><span class="sxs-lookup"><span data-stu-id="25c58-143">RollbackInProgress</span></span> | <span data-ttu-id="25c58-144">アクションは取消中です。</span><span class="sxs-lookup"><span data-stu-id="25c58-144">Reversal of the action is in progress.</span></span>                |
| <span data-ttu-id="25c58-145">RollbackFailed</span><span class="sxs-lookup"><span data-stu-id="25c58-145">RollbackFailed</span></span>     | <span data-ttu-id="25c58-146">アクションの取消が停止されました。</span><span class="sxs-lookup"><span data-stu-id="25c58-146">Reversal of the action was halted.</span></span>                    |
| <span data-ttu-id="25c58-147">RollbackCompleted</span><span class="sxs-lookup"><span data-stu-id="25c58-147">RollbackCompleted</span></span>  | <span data-ttu-id="25c58-148">アクションの取り消しが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="25c58-148">Reversal of the action was successfully completed.</span></span>    |


[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]
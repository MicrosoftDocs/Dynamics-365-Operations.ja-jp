---
title: データベース移動 API - 参照 - v1 - 環境の開始および停止
description: このトピックでは、データベース移動 API のバージョン 1 の参照資料を提供します。
author: laneswenka
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fe5bcdc3d74f442cb7a485f2ad14c9cb791445ec
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753052"
---
# <a name="start-and-stop-environments"></a><span data-ttu-id="9be88-103">環境の開始および停止</span><span class="sxs-lookup"><span data-stu-id="9be88-103">Start and stop environments</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="9be88-104">データベース移動 API を介した Microsoft Dynamics Lifecycle Services (LCS) を通じて、環境の開始および停止をすることができます。</span><span class="sxs-lookup"><span data-stu-id="9be88-104">You can start and stop environments through Microsoft Dynamics Lifecycle Services (LCS) via the Database Movement API.</span></span> <span data-ttu-id="9be88-105">これらの API を使用することにより、確実に LCS 環境の状態を実際の環境と同期させることができます。</span><span class="sxs-lookup"><span data-stu-id="9be88-105">Using these APIs will ensure the LCS environment status is synced with the actual environment.</span></span> 

<span data-ttu-id="9be88-106">LCS の詳細ページと同じ検証ルールが、API に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9be88-106">Note that the same validation rules from the details page in LCS apply to the API.</span></span>

> [!NOTE]
> - <span data-ttu-id="9be88-107">**顧客管理** 環境のみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="9be88-107">Only **Customer-managed** environments are supported.</span></span> <span data-ttu-id="9be88-108">セルフサービス環境は、停止と開始の概念が同じではなく、この API ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9be88-108">Self-service environments do not have the same concept of stop and start and are not supported by this API.</span></span> <span data-ttu-id="9be88-109">Microsoft 管理環境はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="9be88-109">Microsoft-managed environments are not supported.</span></span>
> - <span data-ttu-id="9be88-110">これらの API によって、操作をトリガー/呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9be88-110">These APIs will trigger/invoke the operation.</span></span> <span data-ttu-id="9be88-111">正常な応答は、トリガーが成功したことを示すだけです。</span><span class="sxs-lookup"><span data-stu-id="9be88-111">A successful response only indicates that the trigger was successful.</span></span>
> - <span data-ttu-id="9be88-112">**停止** については、環境がすでに別の操作を実行しているか、または環境がすでに停止されている場合に、成功しなかったと返されます。</span><span class="sxs-lookup"><span data-stu-id="9be88-112">For **stop**, non-success will be returned if the environment is already undergoing another operation or if the environment is already stopped.</span></span>
> - <span data-ttu-id="9be88-113">**開始** については、環境がすでに別の操作を実行している場合には成功しなかったと返されますが、環境がすでに開始されている場合は成功が返されます。</span><span class="sxs-lookup"><span data-stu-id="9be88-113">For **start**, non-success will be returned if the environment is already undergoing another operation but will return success if the environment is already started.</span></span>


## <a name="permissions"></a><span data-ttu-id="9be88-114">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="9be88-114">Permissions</span></span>

<span data-ttu-id="9be88-115">この API を呼び出すには、次のアクセス許可の 1 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="9be88-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="9be88-116">アクセス許可およびその選択方法の詳細については、[認証](../dbmovement-api-authentication.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9be88-116">For more information about permissions and how to select them, see [Authentication](../dbmovement-api-authentication.md).</span></span>

| <span data-ttu-id="9be88-117">アクセス許可のタイプ</span><span class="sxs-lookup"><span data-stu-id="9be88-117">Permission type</span></span>                    | <span data-ttu-id="9be88-118">アクセス許可 (最小の特権から最大の特権)</span><span class="sxs-lookup"><span data-stu-id="9be88-118">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="9be88-119">委任 (勤務先または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="9be88-119">Delegated (work or school account)</span></span> | <span data-ttu-id="9be88-120">ユーザー \_ 偽装</span><span class="sxs-lookup"><span data-stu-id="9be88-120">user\_impersonation</span></span>                                    |

## <a name="http-request"></a><span data-ttu-id="9be88-121">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="9be88-121">HTTP request</span></span>

<span data-ttu-id="9be88-122">次の POST メソッドを使用して、環境を停止または開始する HTTP 要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="9be88-122">Use the following POST method to send an HTTP request to stop or start an environment.</span></span> 

<span data-ttu-id="9be88-123">**環境の停止**</span><span class="sxs-lookup"><span data-stu-id="9be88-123">**Stop an environment**</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /environment/v1/stop/project/{projectId}/environment/{environmentId}
```
<span data-ttu-id="9be88-124">**環境の開始**</span><span class="sxs-lookup"><span data-stu-id="9be88-124">**Start an environment**</span></span>
```http
POST /environment/v1/start/project/{projectId}/environment/{environmentId}
```

## <a name="request-headers"></a><span data-ttu-id="9be88-125">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="9be88-125">Request headers</span></span>

<span data-ttu-id="9be88-126">HTTP 要求のヘッダーで次のヘッダー値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9be88-126">Use the following header value in the HTTP request header.</span></span> 

| <span data-ttu-id="9be88-127">表題</span><span class="sxs-lookup"><span data-stu-id="9be88-127">Header</span></span>         | <span data-ttu-id="9be88-128">先頭値</span><span class="sxs-lookup"><span data-stu-id="9be88-128">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="9be88-129">認証</span><span class="sxs-lookup"><span data-stu-id="9be88-129">Authorization</span></span>  | <span data-ttu-id="9be88-130">ベアラー {token} (必須)</span><span class="sxs-lookup"><span data-stu-id="9be88-130">Bearer {token} (required)</span></span> |
| <span data-ttu-id="9be88-131">「x-ms-version」</span><span class="sxs-lookup"><span data-stu-id="9be88-131">'x-ms-version'</span></span> | <span data-ttu-id="9be88-132">「2017-09-15」 (必須)</span><span class="sxs-lookup"><span data-stu-id="9be88-132">'2017-09-15' (required)</span></span>   |
| <span data-ttu-id="9be88-133">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9be88-133">Content-Type</span></span>   | <span data-ttu-id="9be88-134">アプリケーション /json</span><span class="sxs-lookup"><span data-stu-id="9be88-134">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="9be88-135">要求の本文</span><span class="sxs-lookup"><span data-stu-id="9be88-135">Request body</span></span>

<span data-ttu-id="9be88-136">このメソッドの要求の本文を供給しないでください。</span><span class="sxs-lookup"><span data-stu-id="9be88-136">Don't supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9be88-137">応答</span><span class="sxs-lookup"><span data-stu-id="9be88-137">Response</span></span>

<span data-ttu-id="9be88-138">正しく認証されていない場合を除き、応答は常に **200 OK** 応答になります。</span><span class="sxs-lookup"><span data-stu-id="9be88-138">The response is always a **200 OK** response, unless you aren't correctly authenticated.</span></span> <span data-ttu-id="9be88-139">アクションの成功または失敗を検証するには、**IsSuccess** プロパティを使用してください。</span><span class="sxs-lookup"><span data-stu-id="9be88-139">Be sure to use the **IsSuccess** property to evaluate the success or failure of the action.</span></span>

## <a name="example"></a><span data-ttu-id="9be88-140">例</span><span class="sxs-lookup"><span data-stu-id="9be88-140">Example</span></span>

<span data-ttu-id="9be88-141">**環境の停止要求**</span><span class="sxs-lookup"><span data-stu-id="9be88-141">**Request to stop an environment**</span></span>
```http
POST /environment/v1/stop/project/{projectId}/environment/{environmentId}
```

<span data-ttu-id="9be88-142">**正常な応答**</span><span class="sxs-lookup"><span data-stu-id="9be88-142">**Successful response**</span></span>
```json
{
    "IsSuccess": true,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```



[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]
---
title: データベース移動 API - 参照 - v1 - 環境の開始および停止
description: このトピックでは、データベース移動 API のバージョン 1 の参照資料を提供します。
author: laneswenka
manager: AnnBe
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: d1ba79f6dc8eec9ebab20cded084e6404ff47176
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035828"
---
# <a name="start-and-stop-environments"></a><span data-ttu-id="7d738-103">環境の開始および停止</span><span class="sxs-lookup"><span data-stu-id="7d738-103">Start and stop environments</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="7d738-104">データベース移動 API を介した Microsoft Dynamics Lifecycle Services (LCS) を通じて、環境の開始および停止をすることができます。</span><span class="sxs-lookup"><span data-stu-id="7d738-104">You can start and stop environments through Microsoft Dynamics Lifecycle Services (LCS) via the Database Movement API.</span></span> <span data-ttu-id="7d738-105">これらの API を使用することにより、確実に LCS 環境の状態を実際の環境と同期させることができます。</span><span class="sxs-lookup"><span data-stu-id="7d738-105">Using these APIs will ensure the LCS environment status is synced with the actual environment.</span></span> 

<span data-ttu-id="7d738-106">LCS の詳細ページと同じ検証ルールが、API に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7d738-106">Note that the same validation rules from the details page in LCS apply to the API.</span></span>

> [!NOTE]
> - <span data-ttu-id="7d738-107">**顧客管理** 環境のみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7d738-107">Only **Customer Managed** environments are supported.</span></span> <span data-ttu-id="7d738-108">セルフサービス環境は、停止と開始の概念が同じではなく、この API ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7d738-108">Self-service environments do not have the same concept of stop and start and are not supported by this API.</span></span> <span data-ttu-id="7d738-109">これらの API は、操作をトリガーまたは呼び出し、成功した応答のみがトリガーが成功したことを示します。</span><span class="sxs-lookup"><span data-stu-id="7d738-109">These APIs will trigger/invoke the operation and successful response only indicates the trigger was successful.</span></span>
> - <span data-ttu-id="7d738-110">**停止** については、環境がすでに別の操作を実行しているか、または環境がすでに停止されている場合に、成功しなかったと返されます。</span><span class="sxs-lookup"><span data-stu-id="7d738-110">For **stop**, non-success will be returned if the environment is already undergoing another operation or if the environment is already stopped.</span></span>
> - <span data-ttu-id="7d738-111">**開始** については、環境がすでに別の操作を実行している場合には成功しなかったと返されますが、環境がすでに開始されている場合は成功が返されます。</span><span class="sxs-lookup"><span data-stu-id="7d738-111">For **start**, non-success will be returned if the environment is already undergoing another operation but will return success if the environment is already started.</span></span>


## <a name="permissions"></a><span data-ttu-id="7d738-112">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="7d738-112">Permissions</span></span>

<span data-ttu-id="7d738-113">この API を呼び出すには、次のアクセス許可の 1 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="7d738-113">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="7d738-114">アクセス許可およびその選択方法の詳細については、[認証](../dbmovement-api-authentication.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d738-114">For more information about permissions and how to select them, see [Authentication](../dbmovement-api-authentication.md).</span></span>

| <span data-ttu-id="7d738-115">アクセス許可のタイプ</span><span class="sxs-lookup"><span data-stu-id="7d738-115">Permission type</span></span>                    | <span data-ttu-id="7d738-116">アクセス許可 (最小の特権から最大の特権)</span><span class="sxs-lookup"><span data-stu-id="7d738-116">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="7d738-117">委任 (勤務先または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="7d738-117">Delegated (work or school account)</span></span> | <span data-ttu-id="7d738-118">ユーザー \_ 偽装</span><span class="sxs-lookup"><span data-stu-id="7d738-118">user\_impersonation</span></span>                                    |

## <a name="http-request"></a><span data-ttu-id="7d738-119">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="7d738-119">HTTP request</span></span>

<span data-ttu-id="7d738-120">次の POST メソッドを使用して、環境を停止または開始する HTTP 要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="7d738-120">Use the following POST method to send an HTTP request to stop or start an environment.</span></span> 

<span data-ttu-id="7d738-121">**環境の停止**</span><span class="sxs-lookup"><span data-stu-id="7d738-121">**Stop an environment**</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /environment/v1/stop/project/{projectId}/environment/{environmentId}
```
<span data-ttu-id="7d738-122">**環境の開始**</span><span class="sxs-lookup"><span data-stu-id="7d738-122">**Start an environment**</span></span>
```http
POST /environment/v1/start/project/{projectId}/environment/{environmentId}
```

## <a name="request-headers"></a><span data-ttu-id="7d738-123">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="7d738-123">Request headers</span></span>

<span data-ttu-id="7d738-124">HTTP 要求のヘッダーで次のヘッダー値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7d738-124">Use the following header value in the HTTP request header.</span></span> 

| <span data-ttu-id="7d738-125">表題</span><span class="sxs-lookup"><span data-stu-id="7d738-125">Header</span></span>         | <span data-ttu-id="7d738-126">先頭値</span><span class="sxs-lookup"><span data-stu-id="7d738-126">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="7d738-127">認証</span><span class="sxs-lookup"><span data-stu-id="7d738-127">Authorization</span></span>  | <span data-ttu-id="7d738-128">ベアラー {token} (必須)</span><span class="sxs-lookup"><span data-stu-id="7d738-128">Bearer {token} (required)</span></span> |
| <span data-ttu-id="7d738-129">「x-ms-version」</span><span class="sxs-lookup"><span data-stu-id="7d738-129">'x-ms-version'</span></span> | <span data-ttu-id="7d738-130">「2017-09-15」 (必須)</span><span class="sxs-lookup"><span data-stu-id="7d738-130">'2017-09-15' (required)</span></span>   |
| <span data-ttu-id="7d738-131">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7d738-131">Content-Type</span></span>   | <span data-ttu-id="7d738-132">アプリケーション /json</span><span class="sxs-lookup"><span data-stu-id="7d738-132">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="7d738-133">要求の本文</span><span class="sxs-lookup"><span data-stu-id="7d738-133">Request body</span></span>

<span data-ttu-id="7d738-134">このメソッドの要求の本文を供給しないでください。</span><span class="sxs-lookup"><span data-stu-id="7d738-134">Don't supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7d738-135">応答</span><span class="sxs-lookup"><span data-stu-id="7d738-135">Response</span></span>

<span data-ttu-id="7d738-136">正しく認証されていない場合を除き、応答は常に **200 OK** 応答になります。</span><span class="sxs-lookup"><span data-stu-id="7d738-136">The response is always a **200 OK** response, unless you aren't correctly authenticated.</span></span> <span data-ttu-id="7d738-137">アクションの成功または失敗を検証するには、**IsSuccess** プロパティを使用してください。</span><span class="sxs-lookup"><span data-stu-id="7d738-137">Be sure to use the **IsSuccess** property to evaluate the success or failure of the action.</span></span>

## <a name="example"></a><span data-ttu-id="7d738-138">例</span><span class="sxs-lookup"><span data-stu-id="7d738-138">Example</span></span>

```http
POST /environment/v1/stop/project/{projectId}/environment/{environmentId}
```

```json
{
    "IsSuccess": true,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```


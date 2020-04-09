---
title: データベース移動の API - 参照 - v1 - データベース更新の作成
description: このトピックでは、データベース移動に関するアプリケーション プログラミング インターフェイス (API) バージョン 1 (v1) の参照資料を提供します。
author: laneswenka
manager: AnnBe
ms.date: 09/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: ac5ce59fc98abc4d3f10eb5d9c441c5d6e147c2c
ms.sourcegitcommit: 0d9ca44b48fb2e33d8160faccc1e6bd932e58934
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150781"
---
# <a name="create-a-database-refresh"></a><span data-ttu-id="53f2b-103">データベース更新の作成</span><span class="sxs-lookup"><span data-stu-id="53f2b-103">Create a database refresh</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="53f2b-104">2 つの環境間でのデータベース更新を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="53f2b-104">You can create a database refresh between two environments.</span></span> <span data-ttu-id="53f2b-105">Microsoft Dynamics Lifecycle Services (LCS) の詳細ページと同じ検証ルールは、 アプリケーション プログラミング インターフェイス (API) に適用されます。</span><span class="sxs-lookup"><span data-stu-id="53f2b-105">Note that the same validation rules from the details page in Microsoft Dynamics Lifecycle Services (LCS) apply to the application programming interface (API).</span></span>

## <a name="permissions"></a><span data-ttu-id="53f2b-106">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="53f2b-106">Permissions</span></span>

<span data-ttu-id="53f2b-107">この API を呼び出すには、次のアクセス許可の 1 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="53f2b-107">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="53f2b-108">アクセス許可およびその選択方法の詳細については、[認証](../dbmovement-api-authentication.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53f2b-108">For more information about permissions and how to select them, see [Authentication](../dbmovement-api-authentication.md).</span></span>

| <span data-ttu-id="53f2b-109">アクセス許可のタイプ</span><span class="sxs-lookup"><span data-stu-id="53f2b-109">Permission type</span></span>                    | <span data-ttu-id="53f2b-110">アクセス許可 (最小の特権から最大の特権)</span><span class="sxs-lookup"><span data-stu-id="53f2b-110">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="53f2b-111">委任 (勤務先または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="53f2b-111">Delegated (work or school account)</span></span> | <span data-ttu-id="53f2b-112">ユーザー \_ 偽装</span><span class="sxs-lookup"><span data-stu-id="53f2b-112">user\_impersonation</span></span>                                    |

## <a name="http-request"></a><span data-ttu-id="53f2b-113">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="53f2b-113">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /databasemovement/v1/refresh/project/{projectId}/source/{sourceEnvironmentId}/target/{targetEnvironmentId}
```

## <a name="request-headers"></a><span data-ttu-id="53f2b-114">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="53f2b-114">Request headers</span></span>

| <span data-ttu-id="53f2b-115">表題</span><span class="sxs-lookup"><span data-stu-id="53f2b-115">Header</span></span>         | <span data-ttu-id="53f2b-116">金額</span><span class="sxs-lookup"><span data-stu-id="53f2b-116">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="53f2b-117">承認</span><span class="sxs-lookup"><span data-stu-id="53f2b-117">Authorization</span></span>  | <span data-ttu-id="53f2b-118">ベアラー {token} (必須)</span><span class="sxs-lookup"><span data-stu-id="53f2b-118">Bearer {token} (required)</span></span> |
| <span data-ttu-id="53f2b-119">「x-ms-version」</span><span class="sxs-lookup"><span data-stu-id="53f2b-119">'x-ms-version'</span></span> | <span data-ttu-id="53f2b-120">「2017-09-15」 (必須)</span><span class="sxs-lookup"><span data-stu-id="53f2b-120">'2017-09-15' (required)</span></span>   |
| <span data-ttu-id="53f2b-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="53f2b-121">Content-Type</span></span>   | <span data-ttu-id="53f2b-122">アプリケーション /json</span><span class="sxs-lookup"><span data-stu-id="53f2b-122">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="53f2b-123">要求の本文</span><span class="sxs-lookup"><span data-stu-id="53f2b-123">Request body</span></span>

<span data-ttu-id="53f2b-124">このメソッドの要求の本文を供給しないでください。</span><span class="sxs-lookup"><span data-stu-id="53f2b-124">Don't supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="53f2b-125">応答</span><span class="sxs-lookup"><span data-stu-id="53f2b-125">Response</span></span>

<span data-ttu-id="53f2b-126">正しく認証されていない場合を除き、応答は常に **200 OK** 応答になります。</span><span class="sxs-lookup"><span data-stu-id="53f2b-126">The response is always a **200 OK** response, unless you aren't correctly authenticated.</span></span> <span data-ttu-id="53f2b-127">アクションの成功または失敗を検証するには、**IsSuccess** プロパティを使用してください。</span><span class="sxs-lookup"><span data-stu-id="53f2b-127">Be sure to use the **IsSuccess** property to evaluate the success or failure of the action.</span></span>

## <a name="example"></a><span data-ttu-id="53f2b-128">例</span><span class="sxs-lookup"><span data-stu-id="53f2b-128">Example</span></span>

```http
POST /databasemovement/v1/refresh/project/12345/source/5362377c-bc37-4f92-b30e-fe0c1e664cc0/target/6a90b45f-1764-4077-b924-3f4671540237
```

```json
{
    "IsSuccess": true,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```

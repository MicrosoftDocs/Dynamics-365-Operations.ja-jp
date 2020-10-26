---
title: データベース移動 API - 照会 - v1 - データベース エクスポートの作成
description: このトピックでは、データベース移動に関するアプリケーション プログラミング インターフェイス (API) バージョン 1 (v1) の参照資料を提供します。
author: laneswenka
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fd1a617b979ea812b4528a3966db13d248a8f456
ms.sourcegitcommit: 42dbebced4a99dfe703689b7e38c3c5caecd12e1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949156"
---
# <a name="create-a-database-export"></a><span data-ttu-id="136a3-103">データベース エクスポートの作成</span><span class="sxs-lookup"><span data-stu-id="136a3-103">Create a database export</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="136a3-104">サンドボックス環境からプロジェクトの資産ライブラリへのデータベース エクスポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="136a3-104">You can create a database export from a sandbox environment to the project's asset library.</span></span> <span data-ttu-id="136a3-105">Microsoft Dynamics Lifecycle Services (LCS) の詳細ページと同じ検証ルールは、 アプリケーション プログラミング インターフェイス (API) に適用されます。</span><span class="sxs-lookup"><span data-stu-id="136a3-105">Note that the same validation rules from the details page in Microsoft Dynamics Lifecycle Services (LCS) apply to the application programming interface (API).</span></span>

## <a name="permissions"></a><span data-ttu-id="136a3-106">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="136a3-106">Permissions</span></span>

<span data-ttu-id="136a3-107">この API を呼び出すには、次のアクセス許可の 1 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="136a3-107">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="136a3-108">アクセス許可およびその選択方法の詳細については、[認証](../dbmovement-api-authentication.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="136a3-108">For more information about permissions and how to select them, see [Authentication](../dbmovement-api-authentication.md).</span></span>

| <span data-ttu-id="136a3-109">アクセス許可のタイプ</span><span class="sxs-lookup"><span data-stu-id="136a3-109">Permission type</span></span>                    | <span data-ttu-id="136a3-110">アクセス許可 (最小の特権から最大の特権)</span><span class="sxs-lookup"><span data-stu-id="136a3-110">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="136a3-111">委任 (勤務先または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="136a3-111">Delegated (work or school account)</span></span> | <span data-ttu-id="136a3-112">ユーザー \_ 偽装</span><span class="sxs-lookup"><span data-stu-id="136a3-112">user\_impersonation</span></span>                                    |

## <a name="http-request"></a><span data-ttu-id="136a3-113">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="136a3-113">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /databasemovement/v1/export/project/{projectId}/environment/{environmentId}/backupName/{backupName}
```

## <a name="request-headers"></a><span data-ttu-id="136a3-114">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="136a3-114">Request headers</span></span>

| <span data-ttu-id="136a3-115">表題</span><span class="sxs-lookup"><span data-stu-id="136a3-115">Header</span></span>         | <span data-ttu-id="136a3-116">先頭値</span><span class="sxs-lookup"><span data-stu-id="136a3-116">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="136a3-117">認証</span><span class="sxs-lookup"><span data-stu-id="136a3-117">Authorization</span></span>  | <span data-ttu-id="136a3-118">ベアラー {token} (必須)</span><span class="sxs-lookup"><span data-stu-id="136a3-118">Bearer {token} (required)</span></span> |
| <span data-ttu-id="136a3-119">Content-Type</span><span class="sxs-lookup"><span data-stu-id="136a3-119">Content-Type</span></span>   | <span data-ttu-id="136a3-120">アプリケーション /json</span><span class="sxs-lookup"><span data-stu-id="136a3-120">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="136a3-121">要求の本文</span><span class="sxs-lookup"><span data-stu-id="136a3-121">Request body</span></span>

<span data-ttu-id="136a3-122">このメソッドの要求の本文を供給しないでください。</span><span class="sxs-lookup"><span data-stu-id="136a3-122">Don't supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="136a3-123">応答</span><span class="sxs-lookup"><span data-stu-id="136a3-123">Response</span></span>

<span data-ttu-id="136a3-124">正しく認証されていない場合を除き、応答は常に **200 OK** 応答になります。</span><span class="sxs-lookup"><span data-stu-id="136a3-124">The response is always a **200 OK** response, unless you aren't correctly authenticated.</span></span> <span data-ttu-id="136a3-125">アクションの成功または失敗を検証するには、**IsSuccess** プロパティを使用してください。</span><span class="sxs-lookup"><span data-stu-id="136a3-125">Be sure to use the **IsSuccess** property to evaluate the success or failure of the action.</span></span>

## <a name="example"></a><span data-ttu-id="136a3-126">例</span><span class="sxs-lookup"><span data-stu-id="136a3-126">Example</span></span>

```http
POST /databasemovement/v1/export/project/12345/environment/5362377c-bc37-4f92-b30e-fe0c1e664cc0/backupName/TestBackupViaAPI
```

```json
{
    "IsSuccess": true,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```

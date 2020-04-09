---
title: データベース移動 API - 照会 - v1 - データベース エクスポートの作成
description: このトピックでは、データベース移動に関するアプリケーション プログラミング インターフェイス (API) バージョン 1 (v1) の参照資料を提供します。
author: laneswenka
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: 8429e4d8d4f5bfd9d0640b40d6a469a85f9288cd
ms.sourcegitcommit: 0d9ca44b48fb2e33d8160faccc1e6bd932e58934
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150851"
---
# <a name="create-a-database-export"></a><span data-ttu-id="e6fd9-103">データベース エクスポートの作成</span><span class="sxs-lookup"><span data-stu-id="e6fd9-103">Create a database export</span></span>

[!include [banner](../../../includes/banner.md)]
[!include [banner](../../../includes/preview-banner.md)]

<span data-ttu-id="e6fd9-104">サンドボックス環境からプロジェクトの資産ライブラリへのデータベース エクスポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e6fd9-104">You can create a database export from a sandbox environment to the project's asset library.</span></span> <span data-ttu-id="e6fd9-105">Microsoft Dynamics Lifecycle Services (LCS) の詳細ページと同じ検証ルールは、 アプリケーション プログラミング インターフェイス (API) に適用されます。</span><span class="sxs-lookup"><span data-stu-id="e6fd9-105">Note that the same validation rules from the details page in Microsoft Dynamics Lifecycle Services (LCS) apply to the application programming interface (API).</span></span>

## <a name="permissions"></a><span data-ttu-id="e6fd9-106">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="e6fd9-106">Permissions</span></span>

<span data-ttu-id="e6fd9-107">この API を呼び出すには、次のアクセス許可の 1 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="e6fd9-107">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="e6fd9-108">アクセス許可およびその選択方法の詳細については、[認証](../dbmovement-api-authentication.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e6fd9-108">For more information about permissions and how to select them, see [Authentication](../dbmovement-api-authentication.md).</span></span>

| <span data-ttu-id="e6fd9-109">アクセス許可のタイプ</span><span class="sxs-lookup"><span data-stu-id="e6fd9-109">Permission type</span></span>                    | <span data-ttu-id="e6fd9-110">アクセス許可 (最小の特権から最大の特権)</span><span class="sxs-lookup"><span data-stu-id="e6fd9-110">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="e6fd9-111">委任 (勤務先または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="e6fd9-111">Delegated (work or school account)</span></span> | <span data-ttu-id="e6fd9-112">ユーザー \_ 偽装</span><span class="sxs-lookup"><span data-stu-id="e6fd9-112">user\_impersonation</span></span>                                    |

## <a name="http-request"></a><span data-ttu-id="e6fd9-113">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="e6fd9-113">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /databasemovement/v1/export/project/{projectId}/environment/{environmentId}/backupName/{backupName}
```

## <a name="request-headers"></a><span data-ttu-id="e6fd9-114">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="e6fd9-114">Request headers</span></span>

| <span data-ttu-id="e6fd9-115">表題</span><span class="sxs-lookup"><span data-stu-id="e6fd9-115">Header</span></span>         | <span data-ttu-id="e6fd9-116">先頭値</span><span class="sxs-lookup"><span data-stu-id="e6fd9-116">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="e6fd9-117">認証</span><span class="sxs-lookup"><span data-stu-id="e6fd9-117">Authorization</span></span>  | <span data-ttu-id="e6fd9-118">ベアラー {token} (必須)</span><span class="sxs-lookup"><span data-stu-id="e6fd9-118">Bearer {token} (required)</span></span> |
| <span data-ttu-id="e6fd9-119">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e6fd9-119">Content-Type</span></span>   | <span data-ttu-id="e6fd9-120">アプリケーション /json</span><span class="sxs-lookup"><span data-stu-id="e6fd9-120">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="e6fd9-121">要求の本文</span><span class="sxs-lookup"><span data-stu-id="e6fd9-121">Request body</span></span>

<span data-ttu-id="e6fd9-122">このメソッドの要求の本文を供給しないでください。</span><span class="sxs-lookup"><span data-stu-id="e6fd9-122">Don't supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e6fd9-123">応答</span><span class="sxs-lookup"><span data-stu-id="e6fd9-123">Response</span></span>

<span data-ttu-id="e6fd9-124">正しく認証されていない場合を除き、応答は常に **200 OK** 応答になります。</span><span class="sxs-lookup"><span data-stu-id="e6fd9-124">The response is always a **200 OK** response, unless you aren't correctly authenticated.</span></span> <span data-ttu-id="e6fd9-125">アクションの成功または失敗を検証するには、**IsSuccess** プロパティを使用してください。</span><span class="sxs-lookup"><span data-stu-id="e6fd9-125">Be sure to use the **IsSuccess** property to evaluate the success or failure of the action.</span></span>

## <a name="example"></a><span data-ttu-id="e6fd9-126">例</span><span class="sxs-lookup"><span data-stu-id="e6fd9-126">Example</span></span>

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

---
title: データベース移動 API - 参照 - v1 - データベースのバックアップのリスト
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
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: c79c86784fc48e7df68f39e7833e1b293c8ed914
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681106"
---
# <a name="list-database-backups"></a><span data-ttu-id="b822e-103">データベースのバックアップのリスト</span><span class="sxs-lookup"><span data-stu-id="b822e-103">List database backups</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="b822e-104">データベースのバックアップのリストは、プロジェクトの資産ライブラリから取得することができます。</span><span class="sxs-lookup"><span data-stu-id="b822e-104">You can retrieve a list of database backups from the Project asset library.</span></span>

## <a name="permissions"></a><span data-ttu-id="b822e-105">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="b822e-105">Permissions</span></span>

<span data-ttu-id="b822e-106">このアプリケーション プログラミング インターフェイス (API) を呼び出すには、次のアクセス許可の 1 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="b822e-106">One of the following permissions is required to call this application programming interface (API).</span></span> <span data-ttu-id="b822e-107">アクセス許可およびその選択方法の詳細については、[認証](../dbmovement-api-authentication.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b822e-107">For more information about permissions and how to select them, see [Authentication](../dbmovement-api-authentication.md).</span></span>

| <span data-ttu-id="b822e-108">アクセス許可のタイプ</span><span class="sxs-lookup"><span data-stu-id="b822e-108">Permission type</span></span>                    | <span data-ttu-id="b822e-109">アクセス許可 (最小の特権から最大の特権)</span><span class="sxs-lookup"><span data-stu-id="b822e-109">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="b822e-110">委任 (勤務先または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="b822e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b822e-111">ユーザー \_ 偽装</span><span class="sxs-lookup"><span data-stu-id="b822e-111">user\_impersonation</span></span>                                    |

## <a name="http-request"></a><span data-ttu-id="b822e-112">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="b822e-112">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /databasemovement/v1/databases/project/{projectId}
```

## <a name="request-headers"></a><span data-ttu-id="b822e-113">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="b822e-113">Request headers</span></span>

| <span data-ttu-id="b822e-114">表題</span><span class="sxs-lookup"><span data-stu-id="b822e-114">Header</span></span>         | <span data-ttu-id="b822e-115">金額</span><span class="sxs-lookup"><span data-stu-id="b822e-115">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="b822e-116">承認</span><span class="sxs-lookup"><span data-stu-id="b822e-116">Authorization</span></span>  | <span data-ttu-id="b822e-117">ベアラー {token} (必須)</span><span class="sxs-lookup"><span data-stu-id="b822e-117">Bearer {token} (required)</span></span> |
| <span data-ttu-id="b822e-118">「x-ms-version」</span><span class="sxs-lookup"><span data-stu-id="b822e-118">'x-ms-version'</span></span> | <span data-ttu-id="b822e-119">「2017-09-15」 (必須)</span><span class="sxs-lookup"><span data-stu-id="b822e-119">'2017-09-15' (required)</span></span>   |
| <span data-ttu-id="b822e-120">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b822e-120">Content-Type</span></span>   | <span data-ttu-id="b822e-121">アプリケーション /json</span><span class="sxs-lookup"><span data-stu-id="b822e-121">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="b822e-122">要求の本文</span><span class="sxs-lookup"><span data-stu-id="b822e-122">Request body</span></span>

<span data-ttu-id="b822e-123">このメソッドの要求の本文を供給しないでください。</span><span class="sxs-lookup"><span data-stu-id="b822e-123">Don't supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b822e-124">応答</span><span class="sxs-lookup"><span data-stu-id="b822e-124">Response</span></span>

<span data-ttu-id="b822e-125">正しく認証されていない場合を除き、応答は常に **200 OK** 応答になります。</span><span class="sxs-lookup"><span data-stu-id="b822e-125">The response is always a **200 OK** response, unless you aren't correctly authenticated.</span></span> <span data-ttu-id="b822e-126">アクションの成功または失敗を検証するには、**IsSuccess** プロパティを使用してください。</span><span class="sxs-lookup"><span data-stu-id="b822e-126">Be sure to use the **IsSuccess** property to evaluate the success or failure of the action.</span></span>

## <a name="example"></a><span data-ttu-id="b822e-127">例</span><span class="sxs-lookup"><span data-stu-id="b822e-127">Example</span></span>

```http
GET /databasemovement/v1/databases/project/12345
```

```json
{

    "DatabaseAssets": [
        {
            "Id": "4a2c52d4-49ca-4606-94a9-92b3a6b42985",
            "ProjectId": 12345,
            "OrganizationId": 1,
            "Name": "LanesBackupRecord",
            "FileName": "RandomFile.bacpac",
            "FileDescription": "",
            "FileLocation": "https://scrubbed.blob.core.windows.net/product-ax7productname/e6244b15-5112-4d1d-a422-49c63496ab6d/AX7ProductName-12-17-83c6e642-676a-4048-b413-6e284f5d1f55-e6244b15-5112-4d1d-a422-49c63496ab6d?sv=2015-12-11&sr=b&sig=rO3zmAZ3zM6s%2FV%2BeihBA2LMVvqMsxbtsnbauvd8keYo%3D&se=2019-09-28T15%3A18%3A05Z&sp=r",
            "ModifiedDateTime": "2019-09-27T15:17:35.867",
            "CreatedDateTime": "2019-09-27T15:17:35.867",
            "CreatedByName": null,
            "ModifiedByName": null
        }
    ],
    "IsSuccess": true,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```

---
title: データベース移動 API - バージョン管理とサポート
description: このトピックでは、データベース移動アプリケーション プログラミング インターフェイス (API) のバージョン管理と重大な変更ポリシーの概要について説明します。
author: laneswenka
manager: AnnBe
ms.date: 02/20/2020
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
ms.openlocfilehash: bee7948b0f8ab9d0fcaf92a59ad90bbea382b80e
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113627"
---
# <a name="versioning-and-support"></a><span data-ttu-id="9d817-103">バージョン管理とサポート</span><span class="sxs-lookup"><span data-stu-id="9d817-103">Versioning and support</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9d817-104">このトピックでは、データベース移動アプリケーション プログラミング インターフェイス (API) のバージョン管理と重大な変更ポリシーの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="9d817-104">This topic provides an overview of the versioning and breaking change policies for the Database Movement application programming interface (API).</span></span>

## <a name="support-and-deprecation-information"></a><span data-ttu-id="9d817-105">サポートおよび廃止に関する情報</span><span class="sxs-lookup"><span data-stu-id="9d817-105">Support and deprecation information</span></span>

<span data-ttu-id="9d817-106">REST API の新しいバージョンがリリースされると、それ以前のバージョンは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="9d817-106">As new versions of the REST APIs are released, earlier versions will be retired.</span></span> <span data-ttu-id="9d817-107">Microsoft は、API エンドポイントを廃止する少なくとも 6 か月前に廃止されたバージョンを宣言します。</span><span class="sxs-lookup"><span data-stu-id="9d817-107">Microsoft will declare a version deprecated at least six months before it retires an API endpoint.</span></span>

<span data-ttu-id="9d817-108">API のバージョン番号を増やす (たとえば v1 から v2 に) ことにより、Microsoft は最も低いバージョン (この例では v1) が直ちに廃止され、通知の 6 か月後にサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="9d817-108">By incrementing the version number of the API (for example, from v1 to v2), Microsoft announces that the lowest version (in this example, v1) is immediately deprecated and will no longer be supported six months after the announcement.</span></span> <span data-ttu-id="9d817-109">ただし、Microsoft はサービスの正常性およびセキュリティ問題に対するこのポリシーの例外を作成する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9d817-109">However, Microsoft might make exceptions to this policy for service health and security issues.</span></span>

<span data-ttu-id="9d817-110">API が廃止済としてマークされている場合は、**VersionEOL** (バージョンのサポート終了) フィールドに日付値が入力されます。</span><span class="sxs-lookup"><span data-stu-id="9d817-110">When an API is marked as deprecated, a date value will be entered in the **VersionEOL** (Version end of life) field.</span></span> <span data-ttu-id="9d817-111">したがって、このフィールドを事前に監視して、今後の変更を計画することができます。</span><span class="sxs-lookup"><span data-stu-id="9d817-111">Therefore, you can proactively monitor this field and plan for upcoming changes.</span></span>

### <a name="compatible-and-breaking-changes"></a><span data-ttu-id="9d817-112">互換性のある重大な変更</span><span class="sxs-lookup"><span data-stu-id="9d817-112">Compatible and breaking changes</span></span>

<span data-ttu-id="9d817-113">Microsoft では、プライベート プレビュー グループにおける API 変更の詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d817-113">Microsoft will provide details of API changes in the private preview group.</span></span> <span data-ttu-id="9d817-114">変更が本質的に中断されない場合、API のバージョン番号は変わりません。</span><span class="sxs-lookup"><span data-stu-id="9d817-114">If the changes are non-breaking in nature, the API version number will remain the same.</span></span> <span data-ttu-id="9d817-115">変更が本質的に中断される場合、Microsoft は API のバージョン番号を大きくします。</span><span class="sxs-lookup"><span data-stu-id="9d817-115">If the changes are breaking in nature, Microsoft will increment the API version number.</span></span>

<span data-ttu-id="9d817-116">重大な変更の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="9d817-116">Here are some examples of breaking changes:</span></span>

* <span data-ttu-id="9d817-117">URL または基本要求/応答が変更されます。</span><span class="sxs-lookup"><span data-stu-id="9d817-117">The URL or fundamental request/response is changed.</span></span>
* <span data-ttu-id="9d817-118">宣言されたプロパティが削除または名前変更されたか、またはタイプが変更されています。</span><span class="sxs-lookup"><span data-stu-id="9d817-118">A declared property is removed or renamed, or its type is changed.</span></span>
* <span data-ttu-id="9d817-119">API または API パラメーターは削除されるか、名前変更されます。</span><span class="sxs-lookup"><span data-stu-id="9d817-119">The API or API parameters are removed or renamed.</span></span>
* <span data-ttu-id="9d817-120">必要な要求パラメーターが追加されます。</span><span class="sxs-lookup"><span data-stu-id="9d817-120">A required request parameter is added.</span></span>

<span data-ttu-id="9d817-121">中断されない変更の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="9d817-121">Here are some examples of non-breaking changes:</span></span>

* <span data-ttu-id="9d817-122">nullable または既定値を持つプロパティが追加されます。</span><span class="sxs-lookup"><span data-stu-id="9d817-122">Properties are added that are nullable or have a default value.</span></span>
* <span data-ttu-id="9d817-123">列挙にメンバーが追加されます。</span><span class="sxs-lookup"><span data-stu-id="9d817-123">A member is added to an enumeration.</span></span>
* <span data-ttu-id="9d817-124">ページングが既存のコレクションに導入されます。</span><span class="sxs-lookup"><span data-stu-id="9d817-124">Paging is introduced to existing collections.</span></span>
* <span data-ttu-id="9d817-125">エラーコードが変更されます。</span><span class="sxs-lookup"><span data-stu-id="9d817-125">Error codes are changed.</span></span>
* <span data-ttu-id="9d817-126">要求または応答のプロパティの順序が変更されます。</span><span class="sxs-lookup"><span data-stu-id="9d817-126">The order of properties in requests or responses is changed.</span></span>

### <a name="example-of-versioneol-in-a-response-contract"></a><span data-ttu-id="9d817-127">応答契約での VersionEOL の例</span><span class="sxs-lookup"><span data-stu-id="9d817-127">Example of VersionEOL in a response contract</span></span>

<span data-ttu-id="9d817-128">次の例は、JavaScript Object Notation (JSON) 形式の応答契約を示します。</span><span class="sxs-lookup"><span data-stu-id="9d817-128">The following example shows a response contract in JavaScript Object Notation (JSON) format.</span></span> <span data-ttu-id="9d817-129">すべての応答契約には、**VersionEOL** プロパティがあり、Microsoft .NET フレームワークから DateMax() の既定値があります。</span><span class="sxs-lookup"><span data-stu-id="9d817-129">All response contracts contain the **VersionEOL** property of which has a default value of DateMax() from the Microsoft .NET Framework.</span></span> <span data-ttu-id="9d817-130">アプリケーションは、Microsoft からの応答でこのフィールドの値を監視して、Microsoft が特定のエンドポイントまたは API バージョン全体を廃止した場合にすぐに警告を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="9d817-130">Your applications can monitor the value of this field on responses from Microsoft to get an immediate alert when Microsoft has deprecated a specific endpoint or a whole API version.</span></span>

```json
{
    "IsSuccess": true,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```

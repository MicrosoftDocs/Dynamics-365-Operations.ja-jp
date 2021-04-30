---
title: 開発の概要
description: この開発者ガイドでは、API とカスタム フィールドの参照資料を提供します。 また、他のアプリケーションとの統合についても説明します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b1f8264c5496761232f4856212e3cc4bdea584c7
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893152"
---
# <a name="development-overview"></a><span data-ttu-id="2e986-104">開発の概要</span><span class="sxs-lookup"><span data-stu-id="2e986-104">Development overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2e986-105">この開発者ガイドでは、API とカスタム フィールドの参照資料を提供します。</span><span class="sxs-lookup"><span data-stu-id="2e986-105">This Developer Guide provides an API and custom fields reference.</span></span> <span data-ttu-id="2e986-106">また、他のアプリケーションとの統合についても説明します。</span><span class="sxs-lookup"><span data-stu-id="2e986-106">It also provides information on integrating with other apps.</span></span>

- [<span data-ttu-id="2e986-107">概要</span><span class="sxs-lookup"><span data-stu-id="2e986-107">Overview</span></span>](hr-developer-overview.md)

- [<span data-ttu-id="2e986-108">Power Apps および Power Automate での拡張</span><span class="sxs-lookup"><span data-stu-id="2e986-108">Extend with Power Apps and Power Automate</span></span>](hr-developer-power-apps.md)

- [<span data-ttu-id="2e986-109">Dataverse の Human Resources エンティティ</span><span class="sxs-lookup"><span data-stu-id="2e986-109">Human Resources entities in Dataverse</span></span>](hr-developer-entities.md)

- [<span data-ttu-id="2e986-110">カスタム フィールド</span><span class="sxs-lookup"><span data-stu-id="2e986-110">Custom fields</span></span>](hr-developer-custom-fields.md)

- <span data-ttu-id="2e986-111">データ統合の設定</span><span class="sxs-lookup"><span data-stu-id="2e986-111">Set up data integration</span></span>
  - [<span data-ttu-id="2e986-112">データ統合テクノロジの選択</span><span class="sxs-lookup"><span data-stu-id="2e986-112">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)
  - [<span data-ttu-id="2e986-113">Dataverse 統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2e986-113">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)
  - [<span data-ttu-id="2e986-114">Finance との統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2e986-114">Configure integration with Finance</span></span>](hr-admin-integration-finance.md)
  - [<span data-ttu-id="2e986-115">Dayforce との統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2e986-115">Configure integration with Dayforce</span></span>](hr-admin-integration-dayforce.md)
  - [<span data-ttu-id="2e986-116">定期的なデータ エクスポート アプリの作成</span><span class="sxs-lookup"><span data-stu-id="2e986-116">Create a recurring data export app</span></span>](hr-admin-integration-recurring-data-export.md)
  - <span data-ttu-id="2e986-117">Office との統合</span><span class="sxs-lookup"><span data-stu-id="2e986-117">Integrate with Office</span></span>
    - [<span data-ttu-id="2e986-118">Office 統合のチュートリアル</span><span class="sxs-lookup"><span data-stu-id="2e986-118">Office integration tutorial</span></span>](../fin-ops-core/dev-itpro/office-integration/office-integration-tutorial.md?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json)
    - [<span data-ttu-id="2e986-119">Excel でのエンティティ データの更新</span><span class="sxs-lookup"><span data-stu-id="2e986-119">Update entity data in Excel</span></span>](../fin-ops-core/dev-itpro/office-integration/use-excel-add-in.md?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json)
    - <span data-ttu-id="2e986-120">[[Excel で開く] エクスペリエンスの作成](../fin-ops-core/dev-itpro/office-integration/office-integration-edit-excel.md?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="2e986-120">[Create Open in Excel experiences](../fin-ops-core/dev-itpro/office-integration/office-integration-edit-excel.md?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json)</span></span>
    - [<span data-ttu-id="2e986-121">Office 統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="2e986-121">Troubleshoot Office integration</span></span>](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json)

- <span data-ttu-id="2e986-122">エンティティ API 照会</span><span class="sxs-lookup"><span data-stu-id="2e986-122">Entity API reference</span></span>
  - [<span data-ttu-id="2e986-123">認証</span><span class="sxs-lookup"><span data-stu-id="2e986-123">Authentication</span></span>](hr-developer-api-authentication.md)
  - <span data-ttu-id="2e986-124">エンティティ</span><span class="sxs-lookup"><span data-stu-id="2e986-124">Entities</span></span>
    - [<span data-ttu-id="2e986-125">MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="2e986-125">MyLeaveRequests</span></span>](hr-developer-api-myleaverequests-overview.md)
    - [<span data-ttu-id="2e986-126">休暇申請をワークフローに送信する</span><span class="sxs-lookup"><span data-stu-id="2e986-126">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)

## <a name="see-also"></a><span data-ttu-id="2e986-127">参照</span><span class="sxs-lookup"><span data-stu-id="2e986-127">See also</span></span>

- [<span data-ttu-id="2e986-128">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="2e986-128">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="2e986-129">管理者ガイド</span><span class="sxs-lookup"><span data-stu-id="2e986-129">Administrator Guide</span></span>](hr-admin-overview.md)
- [<span data-ttu-id="2e986-130">ユーザー ガイド</span><span class="sxs-lookup"><span data-stu-id="2e986-130">User Guide</span></span>](hr-hrpro-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
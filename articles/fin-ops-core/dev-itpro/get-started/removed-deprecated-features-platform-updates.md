---
title: 削除済みまたは非推奨のプラットフォーム機能
description: このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラムから削除された、または削除される予定の機能について説明します。
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095777"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="426e4-103">削除済みまたは非推奨のプラットフォーム機能</span><span class="sxs-lookup"><span data-stu-id="426e4-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="426e4-104">このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラムから削除された、または削除される予定の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="426e4-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="426e4-105">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="426e4-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="426e4-106">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="426e4-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="426e4-107">このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="426e4-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="426e4-108">Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="426e4-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="426e4-109">これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。</span><span class="sxs-lookup"><span data-stu-id="426e4-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="426e4-110">プラットフォーム update 32</span><span class="sxs-lookup"><span data-stu-id="426e4-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="426e4-111">ワークフロー要求の変更ダイアログ ボックスにユーザー選択ドロップダウン リストは表示されなくなります</span><span class="sxs-lookup"><span data-stu-id="426e4-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="426e4-112">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="426e4-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="426e4-113">変更要求が意図しないユーザーに送信される可能性があったため、これはセキュリティ上の問題でした。</span><span class="sxs-lookup"><span data-stu-id="426e4-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="426e4-114">また、これはワークフローの作成者が誰であるかをユーザーが決定し、手動で選択するよう促すものであったため、操作性の問題でもありました。</span><span class="sxs-lookup"><span data-stu-id="426e4-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="426e4-115">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="426e4-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="426e4-116">いいえ</span><span class="sxs-lookup"><span data-stu-id="426e4-116">No</span></span> |
| <span data-ttu-id="426e4-117">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="426e4-117">**Product areas affected**</span></span>         | <span data-ttu-id="426e4-118">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="426e4-118">Workflow</span></span> |
| <span data-ttu-id="426e4-119">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="426e4-119">**Deployment option**</span></span>              | <span data-ttu-id="426e4-120">すべて</span><span class="sxs-lookup"><span data-stu-id="426e4-120">All</span></span> |
| <span data-ttu-id="426e4-121">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="426e4-121">**Status**</span></span>                         | <span data-ttu-id="426e4-122">Platform update 32 の要求変更ダイアログ ボックスからユーザー選択ドロップダウン リストが削除されました。</span><span class="sxs-lookup"><span data-stu-id="426e4-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="426e4-123">変更要求は、作成者に対して意図したとおりに自動的に送信されます。</span><span class="sxs-lookup"><span data-stu-id="426e4-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="426e4-124">この機能の詳細については、[ワークフロー承認プロセスでのアクション](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="426e4-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a><span data-ttu-id="426e4-125">埋め込み型のドリルスルー リンクは、クラウドでホストされるサービスによって表示されるページ番号付きドキュメントではサポートされなくなりました</span><span class="sxs-lookup"><span data-stu-id="426e4-125">Embedded drill-through links are no longer supported in paginated documents rendered by the cloud-hosted service</span></span> 
|   |  |
|------------|--------------------|
| <span data-ttu-id="426e4-126">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="426e4-126">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="426e4-127">サービスによって表示されるドキュメントに埋め込まれたナビゲーション URL には、機密業務データが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="426e4-127">Navigation URLs embedded in documents rendered by the service may contain sensitive business data.</span></span> <span data-ttu-id="426e4-128">顧客データをさらに保護するセキュリティ上の事前措置として、ドキュメントでの埋め込み型のドリルスルー リンクのサポートを削除しています。</span><span class="sxs-lookup"><span data-stu-id="426e4-128">We are removing support for embedded drill-through links in documents as a security precaution to further protect customer's data.</span></span> <span data-ttu-id="426e4-129">また、ユーザーは、この変更の結果として対話的にドキュメントを作成する際にパフォーマンスを向上させることもできます。</span><span class="sxs-lookup"><span data-stu-id="426e4-129">Users will also benefit from improved performance while interactively producing documents as a result of this change.</span></span>  |
| <span data-ttu-id="426e4-130">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="426e4-130">**Replaced by another feature?**</span></span>   | <span data-ttu-id="426e4-131">無</span><span class="sxs-lookup"><span data-stu-id="426e4-131">No</span></span> |
| <span data-ttu-id="426e4-132">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="426e4-132">**Product areas affected**</span></span>         | <span data-ttu-id="426e4-133">レポート</span><span class="sxs-lookup"><span data-stu-id="426e4-133">Reporting</span></span> |
| <span data-ttu-id="426e4-134">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="426e4-134">**Deployment option**</span></span>              | <span data-ttu-id="426e4-135">すべて</span><span class="sxs-lookup"><span data-stu-id="426e4-135">All</span></span> |
| <span data-ttu-id="426e4-136">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="426e4-136">**Status**</span></span>                         | <span data-ttu-id="426e4-137">この機能は、サービスからアクティブに削除されています。</span><span class="sxs-lookup"><span data-stu-id="426e4-137">This feature is actively being removed from the service.</span></span><br><br><span data-ttu-id="426e4-138">最新のクライアントには、アプリケーションのナビゲーションを支援する自動生成リンクを含むさまざまなオプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="426e4-138">The modern client offers numerous options for producing views that include auto-generated links to assist in navigating the application.</span></span> <span data-ttu-id="426e4-139">サービスによって表示されるページ番号付きドキュメントは、受信者向けに電子メールで送信、アーカイブ、印刷される外部通信に推奨されます。</span><span class="sxs-lookup"><span data-stu-id="426e4-139">Paginated documents rendered by the service are recommended for external communications that are emailed, archived, and printed for recipients.</span></span> <span data-ttu-id="426e4-140">ドキュメントを直接ブラウザーでプレビューするエクスペリエンスが改善され、ローカル プリンターに直接アクセスできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="426e4-140">We have improved the experience for previewing documents directly in the browser, which offers direct access to local printers.</span></span> <span data-ttu-id="426e4-141">詳細については、[埋め込みビュアーを使用してPDFドキュメントのプレビューをする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="426e4-141">For more information, see [Preview PDF documents with an embedded viewer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="426e4-142">削除済みまたは非推奨の機能に関する以前の発表</span><span class="sxs-lookup"><span data-stu-id="426e4-142">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="426e4-143">以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../migration-upgrade/deprecated-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="426e4-143">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>


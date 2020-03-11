---
title: 削除済みまたは非推奨のプラットフォーム機能
description: このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラムから削除された、または削除される予定の機能について説明します。
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
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
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087886"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="1efda-103">削除済みまたは非推奨のプラットフォーム機能</span><span class="sxs-lookup"><span data-stu-id="1efda-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1efda-104">このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラムから削除された、または削除される予定の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="1efda-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="1efda-105">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="1efda-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="1efda-106">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1efda-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="1efda-107">このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1efda-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="1efda-108">Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1efda-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="1efda-109">これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。</span><span class="sxs-lookup"><span data-stu-id="1efda-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="1efda-110">プラットフォーム update 32</span><span class="sxs-lookup"><span data-stu-id="1efda-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="1efda-111">ワークフロー要求の変更ダイアログ ボックスにユーザー選択ドロップダウン リストは表示されなくなります</span><span class="sxs-lookup"><span data-stu-id="1efda-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="1efda-112">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="1efda-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="1efda-113">変更要求が意図しないユーザーに送信される可能性があったため、これはセキュリティ上の問題でした。</span><span class="sxs-lookup"><span data-stu-id="1efda-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="1efda-114">また、これはワークフローの作成者が誰であるかをユーザーが決定し、手動で選択するよう促すものであったため、操作性の問題でもありました。</span><span class="sxs-lookup"><span data-stu-id="1efda-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="1efda-115">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="1efda-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="1efda-116">いいえ</span><span class="sxs-lookup"><span data-stu-id="1efda-116">No</span></span> |
| <span data-ttu-id="1efda-117">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="1efda-117">**Product areas affected**</span></span>         | <span data-ttu-id="1efda-118">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="1efda-118">Workflow</span></span> |
| <span data-ttu-id="1efda-119">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="1efda-119">**Deployment option**</span></span>              | <span data-ttu-id="1efda-120">すべて</span><span class="sxs-lookup"><span data-stu-id="1efda-120">All</span></span> |
| <span data-ttu-id="1efda-121">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="1efda-121">**Status**</span></span>                         | <span data-ttu-id="1efda-122">Platform update 32 の要求変更ダイアログ ボックスからユーザー選択ドロップダウン リストが削除されました。</span><span class="sxs-lookup"><span data-stu-id="1efda-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="1efda-123">変更要求は、作成者に対して意図したとおりに自動的に送信されます。</span><span class="sxs-lookup"><span data-stu-id="1efda-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="1efda-124">この機能の詳細については、[ワークフロー承認プロセスでのアクション](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1efda-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="1efda-125">削除済みまたは非推奨の機能に関する以前の発表</span><span class="sxs-lookup"><span data-stu-id="1efda-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="1efda-126">以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../migration-upgrade/deprecated-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1efda-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>


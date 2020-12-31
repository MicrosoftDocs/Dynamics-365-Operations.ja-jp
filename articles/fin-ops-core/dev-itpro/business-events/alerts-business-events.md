---
title: ビジネス イベントとしての警告
description: このトピックでは、ビジネス イベントとしての警告について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 11/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: Platform update 25
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: f52b9f823c269e6e94fadf2de6a3ba3144ffaa6d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687365"
---
# <a name="alerts-as-business-events"></a><span data-ttu-id="9733d-103">ビジネス イベントとしての警告</span><span class="sxs-lookup"><span data-stu-id="9733d-103">Alerts as business events</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9733d-104">ユーザーが設定できる警告は 2 種類あります。</span><span class="sxs-lookup"><span data-stu-id="9733d-104">There are two kinds of alerts that can be configured by users.</span></span> <span data-ttu-id="9733d-105">これらは変更ベースの警告と期日の警告です。</span><span class="sxs-lookup"><span data-stu-id="9733d-105">These are change-based alerts and due date alerts.</span></span> <span data-ttu-id="9733d-106">警告機能の詳細については [警告](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/alerts-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9733d-106">For more information about the alerts functionality, see [Alerts](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/alerts-overview).</span></span>

<span data-ttu-id="9733d-107">変更ベースの警告および期日の警告は、外部のアプリケーションやシステムを通知またはトリガーするメカニズムとして、ビジネス イベントを送信するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="9733d-107">The change-based alerts and due date alerts can be configured to send out a business event as a mechanism to notify or trigger external applications or systems.</span></span> <span data-ttu-id="9733d-108">これにより、警告は高度なユーザー通知シナリオやシステム間の業務プロセス統合に関与できます。</span><span class="sxs-lookup"><span data-stu-id="9733d-108">This allows alerts to participate in advanced user notification scenarios and also in business process integration across systems.</span></span>

<span data-ttu-id="9733d-109">警告からビジネス イベントを作成するには、**警告ルールの作成** ダイアログ ボックスで、**警告の対象** > **外部に送信** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9733d-109">To generate a business event from an alert, in the **Create alert rule** dialog box, set **Alert me with** > **Send externally** to **Yes**.</span></span> 

<span data-ttu-id="9733d-110">警告が処理されるようにするには、変更ベースまたは期日の警告のバッチ処理を、期日イベントのバッチ処理に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9733d-110">In order for alerts to be processed, the batch processes for change-based and/or due-date alerts should be set for batch processing for due-date events.</span></span> <span data-ttu-id="9733d-111">詳細については、[期日イベントに関するバッチ処理](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/alerts-managing#set-up-processing-for-change-based-alerts) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9733d-111">For more information, see [Batch processing for due-date events](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/alerts-managing#set-up-processing-for-change-based-alerts).</span></span>

<span data-ttu-id="9733d-112">警告をビジネス イベントとして送信するには、変更ベースの警告や期日の警告のビジネス イベントも有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9733d-112">The business event for the change-based alert and/or the due date alert must also be active for the alert to be sent out as a business event.</span></span> <span data-ttu-id="9733d-113">有効化プロセスの詳細については、[ビジネス イベントの有効化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/home-page#activating-business-events) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9733d-113">To learn more about the activation process, see [Activating business events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/home-page#activating-business-events).</span></span>

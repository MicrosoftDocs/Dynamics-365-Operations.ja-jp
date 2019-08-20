---
title: ビジネス イベントとしての警告
description: このトピックでは、ビジネス イベントとしての警告について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: Platform update 25
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: ec7161e5e49a66e532dd4c89e248729a50df3782
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741371"
---
# <a name="alerts-as-business-events"></a><span data-ttu-id="4b29b-103">ビジネス イベントとしての警告</span><span class="sxs-lookup"><span data-stu-id="4b29b-103">Alerts as business events</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4b29b-104">Dynamics 365 for Finance and Operations でユーザーが設定できる警告は 2 種類あります。</span><span class="sxs-lookup"><span data-stu-id="4b29b-104">In Dynamics 365 for Finance and Operations, there are two kinds of alerts that can be configured by users.</span></span> <span data-ttu-id="4b29b-105">これらは変更ベースの警告と期日の警告です。</span><span class="sxs-lookup"><span data-stu-id="4b29b-105">These are change-based alerts and due date alerts.</span></span> <span data-ttu-id="4b29b-106">警告機能の詳細については [警告](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/alerts-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b29b-106">For more information about the alerts functionality, see [Alerts](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/alerts-overview).</span></span>

<span data-ttu-id="4b29b-107">変更ベースの警告および期日の警告は、外部のアプリケーションやシステムを通知またはトリガーするメカニズムとして、ビジネス イベントを送信するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="4b29b-107">The change-based alerts and due date alerts can be configured to send out a business event as a mechanism to notify or trigger external applications or systems.</span></span> <span data-ttu-id="4b29b-108">これにより、警告は高度なユーザー通知シナリオやシステム間の業務プロセス統合に関与できます。</span><span class="sxs-lookup"><span data-stu-id="4b29b-108">This allows alerts to participate in advanced user notification scenarios and also in business process integration across systems.</span></span>

<span data-ttu-id="4b29b-109">警告を構成するには、**外部に送信** 設定を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b29b-109">To configure an alert, the **Send external** setting must be enabled.</span></span> <span data-ttu-id="4b29b-110">警告をビジネス イベントとして送信するには、変更ベースの警告や期日の警告のビジネス イベントも有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b29b-110">The business event for the change-based alert and/or the due date alert must also be active for the alert to be sent out as a business event.</span></span>

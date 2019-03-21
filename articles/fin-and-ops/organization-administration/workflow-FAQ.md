---
title: ワークフローに関するよく寄せられる質問
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについてよく寄せられる質問に回答します。
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/01/2019
ms.locfileid: "773219"
---
# <a name="workflow-system"></a><span data-ttu-id="a4160-103">ワークフロー システム</span><span class="sxs-lookup"><span data-stu-id="a4160-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4160-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについてよく寄せられる質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="a4160-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="a4160-105">通知</span><span class="sxs-lookup"><span data-stu-id="a4160-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="a4160-106">作業項目が否認された場合に複数の通知が受信されるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="a4160-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="a4160-107">作業項目が否認されると、その作業項目は否認済として完了します。</span><span class="sxs-lookup"><span data-stu-id="a4160-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="a4160-108">別の作業項目が作成され、作成者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="a4160-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="a4160-109">これは、否認された作業項目に関する発信者への通知と、新しい「変更要求済」の作業項目に割り当てられたユーザーへの個別の通知があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="a4160-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="a4160-110">各通知は異なる作業項目に対するものですが、類似性により混乱が生じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a4160-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="a4160-111">将来のリリースでこれを改善する方法を検討しています。</span><span class="sxs-lookup"><span data-stu-id="a4160-111">We are looking at ways to improve this in a future release.</span></span>

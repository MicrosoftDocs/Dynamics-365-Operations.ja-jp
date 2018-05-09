---
title: "モバイル デバイスで最も古いバッチをピッキング"
description: "このトピックでは、最も古いバッチをピッキングづつオプションを適用する方法について説明します。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 205317cccbde220d9198246f47076fc186286969
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="76322-103">モバイル デバイスで最も古いバッチをピッキング</span><span class="sxs-lookup"><span data-stu-id="76322-103">Pick oldest batch on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76322-104">モバイル デバイス メニューから [最も古いバッチをピッキング] の構成にアクセスすることができるため、これにより、倉庫作業者が現在の場所で一番古いバッチを選択するように強制するまたは警告することができます。</span><span class="sxs-lookup"><span data-stu-id="76322-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="76322-105">該当する場合</span><span class="sxs-lookup"><span data-stu-id="76322-105">Where it applies</span></span>
<span data-ttu-id="76322-106">最も古いバッチをピッキングがモバイル デバイスのメニュー項目で構成され、下記にある項目のバッチのピッキングに影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="76322-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="76322-107">最も古いバッチをピッキングの構成を設定する方法</span><span class="sxs-lookup"><span data-stu-id="76322-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="76322-108">既存の作業を使用するように設定されている品目については、モバイル デバイス メニューで [最も古いバッチをピッキング] を [なし]、[警告]、または [強制] に設定できます。</span><span class="sxs-lookup"><span data-stu-id="76322-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="76322-109">\[なし\]: 作業者にはメッセージは表示されず、現在の場所にあるどのバッチでもピッキングが許可されています。</span><span class="sxs-lookup"><span data-stu-id="76322-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="76322-110">[警告] および \[強制\]: 作業者が、バッチを選択すると、有効期限日がもっとも古いバッチの一覧がバッチ コントロールの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="76322-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="76322-111">場所がライセンス プレートで制御されている場合、最も古いバッチを持つナンバー プレートのリストがナンバー プレート コントロールの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="76322-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="76322-112">\[警告\]: 表示されている一覧の上にあるライセンス プレートまたはバッチを選択すると、コントロールが非表示になり、古いバッチを選択できるという警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="76322-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="76322-113">作業を続行できるようにするには、作業者は同じライセンス プレートまたはバッチを再度選択できます。</span><span class="sxs-lookup"><span data-stu-id="76322-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="76322-114">**強制**: 作業者には、さらに古いバッチのピッキングがあるというメッセージが引き続き表示されます。</span><span class="sxs-lookup"><span data-stu-id="76322-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>


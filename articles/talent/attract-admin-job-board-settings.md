---
title: Microsoft Dynamics 365 for Talent - Attract における Broadbean 統合の有効化
description: このトピックでは、Broadbean などの外部の職務ボードへジョブを転記するための Microsoft Dynamics 365 for Talent - Attract のコンフィギュレーション方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 2334c2bd0edccf3000f8d91651afafd4619ad0b8
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739682"
---
# <a name="enable-broadbean-integration"></a><span data-ttu-id="1d1f7-103">Broadbean との統合を有効にする</span><span class="sxs-lookup"><span data-stu-id="1d1f7-103">Enable Broadbean integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1d1f7-104">できるだけ多くの資格のある候補者の前で、空いている職位を獲得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="1d1f7-105">Broadbean などの採用サイトは、この目標を達成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="1d1f7-106">Microsoft Dynamics 365 for Talent: Attract では Broadbean にジョブを転記し、Microsoft がこの領域で新製品を常に提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-106">Microsoft Dynamics 365 for Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="1d1f7-107">外部サイトへジョブを転記するには、[包括採用アドオン](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) が必要です。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="1d1f7-108">Attract から Broadbean にジョブを転記するには、Broadbean サブスクリプションが必要です。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="1d1f7-109">現在プレビューにある機能です。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-109">This feature is currently in preview.</span></span> <span data-ttu-id="1d1f7-110">試行する場合は、[Attract 管理者の設定で有効にする](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) を実行します。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="1d1f7-111">Broadbean との統合をコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="1d1f7-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="1d1f7-112">Attract に管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="1d1f7-113">ページの右上隅にある**設定**ボタン (ギヤ記号) を選択して、**管理者センター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="1d1f7-114">Broadbean に連絡して、**ユーザー名**、**クライアント ID**、および**暗号化トークン**フィールドに情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="1d1f7-115">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="1d1f7-116">Broadbean の資格情報は機密性が高いものです。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="1d1f7-117">したがって、責任を持ってそれらを格納および共有します。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="1d1f7-118">Attract の管理者ロールを持つすべてのユーザーは、これらの資格情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="1d1f7-119">Microsoft と Attract は、これらの値を作成し管理することには関与していません。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="1d1f7-120">Attract でそれらを最新の状態に保ち、Broadbean と協力してユーザーの資格情報に関連する問題を解決するのはユーザー個人の責任となりす。</span><span class="sxs-lookup"><span data-stu-id="1d1f7-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

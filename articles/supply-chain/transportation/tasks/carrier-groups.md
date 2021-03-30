---
title: 配送業者グループ
description: このトピックでは、配送業者グループのデータ設定方法について説明します。
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 95517153dda06cecf8e57b1f9b080aa07966c111
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247265"
---
# <a name="carrier-groups"></a><span data-ttu-id="634f7-103">配送業者グループ</span><span class="sxs-lookup"><span data-stu-id="634f7-103">Carrier groups</span></span>

<span data-ttu-id="634f7-104">配送業者グループは、出荷の配送業者と配送業者のサービスの集合体です。</span><span class="sxs-lookup"><span data-stu-id="634f7-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="634f7-105">各配送業者グループは、配送業者とそれに属する配送業者サービスの優先順位を指定します。</span><span class="sxs-lookup"><span data-stu-id="634f7-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="634f7-106">同じ工順セグメントの配送業者と配送業者サービスが複数存在する場合は、特定の配送業者と配送業者サービスの代わりに、工順計画または工順指示書で配送業者グループを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="634f7-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="634f7-107">配送業者グループの作成</span><span class="sxs-lookup"><span data-stu-id="634f7-107">Create a carrier group</span></span>

1. <span data-ttu-id="634f7-108">**輸送管理 &gt; 設定 &gt; 配送業者 &gt; 配送業者グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="634f7-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="634f7-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="634f7-109">Select **New**.</span></span>
1. <span data-ttu-id="634f7-110">**配送業者グループ** フィールドで、そのグループに対して一意識別子 (ID) を入力します。</span><span class="sxs-lookup"><span data-stu-id="634f7-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="634f7-111">**名前** フィールドに、グループの内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="634f7-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="634f7-112">**詳細** クイックタブで、行を追加し、その行の配送業者と配送業者サービスを選択します。</span><span class="sxs-lookup"><span data-stu-id="634f7-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="634f7-113">グループに必要な数の配送業者を追加するまで、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="634f7-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="634f7-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="634f7-114">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
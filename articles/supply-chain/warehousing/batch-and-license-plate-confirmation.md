---
title: "バッチおよびライセンス プレートの確認"
description: "このトピックでは、モバイル デバイスからバッチおよびライセンス プレートの確認を設定して適用する方法について説明します。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm
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
ms.openlocfilehash: 615590352b8ec1cef64f7243b260a3c92ae9c2a1
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="f3c95-103">バッチおよびライセンス プレートの確認</span><span class="sxs-lookup"><span data-stu-id="f3c95-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3c95-104">バッチの確認では、適切なバッチがピッキングされていることをモバイル デバイスから確認することができます。</span><span class="sxs-lookup"><span data-stu-id="f3c95-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="f3c95-105">上の品目のみのバッチ作業の最初のピッキング時、上のバッチの表示は、検索階層内のバッチ範囲の場所を超えることを示し、ピッキングされているバッチが作業明細行のバッチと一致していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3c95-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="f3c95-106">ライセンス プレートの確認では、適切なライセンス プレートがピッキングされていることをモバイル デバイスから確認することができます。</span><span class="sxs-lookup"><span data-stu-id="f3c95-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="f3c95-107">ステージの場所からのピッキング作業時に、ピッキングされるライセンス プレートが作業に関連付けられているライセンス プレートと一致していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3c95-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="f3c95-108">ライセンス プレートをスキャンして作業を起動する場合、この確認手順はスキップされます。</span><span class="sxs-lookup"><span data-stu-id="f3c95-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="f3c95-109">該当する場合</span><span class="sxs-lookup"><span data-stu-id="f3c95-109">Where it applies</span></span>
<span data-ttu-id="f3c95-110">確認は、以下のシナリオで適用されます。</span><span class="sxs-lookup"><span data-stu-id="f3c95-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="f3c95-111">バッチ確認は、上の品目のバッチ作業の最初のピッキング時に適用されます。</span><span class="sxs-lookup"><span data-stu-id="f3c95-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="f3c95-112">ライセンス プレートの確認は、ステージの場所からのピッキングに適用されます。</span><span class="sxs-lookup"><span data-stu-id="f3c95-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="f3c95-113">バッチおよびライセンス プレートの確認の設定</span><span class="sxs-lookup"><span data-stu-id="f3c95-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="f3c95-114">モバイル デバイスのメニュー項目から、バッチとライセンス プレートの確認をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="f3c95-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="f3c95-115">モバイル デバイス メニュー項目から、[作業確認の設定] に進みます。</span><span class="sxs-lookup"><span data-stu-id="f3c95-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="f3c95-116">バッチの確認またはライセンス プレートの確認のどちらかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f3c95-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="f3c95-117">自動確認が有効でない作業タイプのピッキングでは、両方のオプションが有効です。</span><span class="sxs-lookup"><span data-stu-id="f3c95-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  


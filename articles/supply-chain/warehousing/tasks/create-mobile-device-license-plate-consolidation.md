---
title: ライセンス プレートの連結用のモバイル デバイス メニュー項目の作成
description: この手順では、ライセンスプレート結合作業に必要なモバイル端末のメニュー項目を作成する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3f5f572461de007f137ffa7ea05c535371f95b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977241"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="daa3f-103">ライセンス プレートの連結用のモバイル デバイス メニュー項目の作成</span><span class="sxs-lookup"><span data-stu-id="daa3f-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="daa3f-104">この手順では、ライセンスプレート結合作業に必要なモバイル端末のメニュー項目を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="daa3f-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="daa3f-105">これにより、倉庫従事者は同じ場所内で、品目付きライセンスプレートと別の場所のライセンスプレートとを結合することができます。</span><span class="sxs-lookup"><span data-stu-id="daa3f-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="daa3f-106">たとえば、この方法を用いると両方の作業指示で手順が同一の場合、結合された品目についての作業は1回で済むわけです。</span><span class="sxs-lookup"><span data-stu-id="daa3f-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="daa3f-107">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="daa3f-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="daa3f-108">通常、この作業を行うのは倉庫責任者です。</span><span class="sxs-lookup"><span data-stu-id="daa3f-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="daa3f-109">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="daa3f-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="daa3f-110">[倉庫管理] > [設定] > [モバイル デバイス] > [モバイル デバイスのメニュー品目] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="daa3f-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="daa3f-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="daa3f-111">Click New.</span></span>
3. <span data-ttu-id="daa3f-112">[メニュー項目名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="daa3f-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="daa3f-113">[タイトル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="daa3f-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="daa3f-114">[モード] フィールドで [間接] を選択します。</span><span class="sxs-lookup"><span data-stu-id="daa3f-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="daa3f-115">[活動コード] フィールドでは、[ライセンスプレートを結合する] を選択します。</span><span class="sxs-lookup"><span data-stu-id="daa3f-115">In the Activity code field, select 'Consolidate license plates'.</span></span>


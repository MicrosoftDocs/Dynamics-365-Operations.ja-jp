---
title: 混合ライセンス プレートの受取
description: このトピックでは、混合ライセンス プレート受取の登録方法とモバイル デバイスの複数品目の作業方法について説明します。
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a44165bc59d65a9dfdf8e591152f427b97930b34
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569385"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="3da88-103">混合ライセンス プレートの受取</span><span class="sxs-lookup"><span data-stu-id="3da88-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3da88-104">混合ライセンス プレート受取では、プット アウェイ作業を登録し作成する前に、複数品目で構成されているライセンス プレートを構築することができます。</span><span class="sxs-lookup"><span data-stu-id="3da88-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="3da88-105">複数品目で構成されるライセンス プレートは、各品目を登録するための入荷ドックで分割する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3da88-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="3da88-106">元伝票の明細行を識別するために、フローに関連する品目を使用する場合は、品目コントロール上のバーコードをスキャンすることができます。</span><span class="sxs-lookup"><span data-stu-id="3da88-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="3da88-107">バーコードに数量とコンフィギュレーションされた測定単位 (UOM) がある場合は、品目および数量が自動的に混在ライセンス プレートに追加され、もう 1 つの品目をスキャンする画面に戻ります。</span><span class="sxs-lookup"><span data-stu-id="3da88-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="3da88-108">これにより、ステップごとに確認することなく、素早くすべての品目をスキャンすることができます。</span><span class="sxs-lookup"><span data-stu-id="3da88-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="3da88-109">混合ライセンス プレートの受取フローでは、ライセンス プレートに既にスキャンされた品目の一覧を表示し、ここから正しい品目の数量に修正することができます。</span><span class="sxs-lookup"><span data-stu-id="3da88-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="3da88-110">該当する場所</span><span class="sxs-lookup"><span data-stu-id="3da88-110">Where it applies</span></span>

<span data-ttu-id="3da88-111">混合ライセンス プレート受取とは、同時に複数明細行 / 品目の作業を登録し作成するモバイル デバイスの受取フローです。</span><span class="sxs-lookup"><span data-stu-id="3da88-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="3da88-112">これは、複数品目を含む入庫ライセンス プレートを受け取る場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="3da88-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="3da88-113">混合ライセンス プレートの受取の設定方法</span><span class="sxs-lookup"><span data-stu-id="3da88-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="3da88-114">混合ライセンス プレートの受取は、モバイル デバイスのメニュー品目として設定されます。</span><span class="sxs-lookup"><span data-stu-id="3da88-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="3da88-115">既存の作業ではなく、次の方法のいずれかを使用するモード作業で、新しいメニュー品目を作成します。</span><span class="sxs-lookup"><span data-stu-id="3da88-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="3da88-116">混合ライセンス プレートの受取</span><span class="sxs-lookup"><span data-stu-id="3da88-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="3da88-117">混合ライセンス プレートの受取とプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="3da88-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="3da88-118">元伝票の明細行を識別するためのオプションとして、発注書の品目、発注書の明細行、返品注文、移動オーダーの品目、および在庫移動指示明細行があります。</span><span class="sxs-lookup"><span data-stu-id="3da88-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="3da88-119">これらのオプションは、1 つのライセンス プレートの入荷注文に変更できます。</span><span class="sxs-lookup"><span data-stu-id="3da88-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="3da88-120">最後のオプションは、負荷品目によるものです。</span><span class="sxs-lookup"><span data-stu-id="3da88-120">The last option is by load item.</span></span> <span data-ttu-id="3da88-121">複数の品目をライセンス プレートに追加することはできますが、複数の負荷を切り替えることはできません。</span><span class="sxs-lookup"><span data-stu-id="3da88-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>

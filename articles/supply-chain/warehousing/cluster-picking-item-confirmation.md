---
title: クラスター ピッキングの製品の確認
description: このトピックでは、クラスタ ピッキングと共に品目検証を設定する方法について説明します。
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272c3a13b68e2b862faf20cc269ca790322b61de
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432002"
---
# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="dd815-103">クラスター ピッキングの製品の確認</span><span class="sxs-lookup"><span data-stu-id="dd815-103">Product confirmation for cluster picking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd815-104">クラスタ ピッキングでは、複数の注文に対する品目のピッキングを同時にすることができます。</span><span class="sxs-lookup"><span data-stu-id="dd815-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="dd815-105">クラスタ ピッキングが適用される場合、クラスタに追加される品目を確認するための品目確認書は重要です。</span><span class="sxs-lookup"><span data-stu-id="dd815-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="dd815-106">クラスタ ピッキング プロセス中にクラスタ ピッキングの品目を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="dd815-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="dd815-107">該当する場合</span><span class="sxs-lookup"><span data-stu-id="dd815-107">Where it applies</span></span>

<span data-ttu-id="dd815-108">クラスタ ピッキングの品目の検証は、非クラスタ ピッキング プロセスで品目を確認する場合と同様に働きます。</span><span class="sxs-lookup"><span data-stu-id="dd815-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="dd815-109">設定は、製品バー コード設定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="dd815-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="dd815-110">クラスタ ピッキングの品目の検証の設定</span><span class="sxs-lookup"><span data-stu-id="dd815-110">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="dd815-111">モバイル デバイスのメニュー項目で、作業確認の設定フォームを開きます: **倉庫管理** > **倉庫管理** > **設定** > **モバイル デバイス** > **モバイル デバイスのメニュー項目** に進みます。</span><span class="sxs-lookup"><span data-stu-id="dd815-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
1. <span data-ttu-id="dd815-112">モバイル デバイス メニュー品目から、**作業確認の設定** を開きます。</span><span class="sxs-lookup"><span data-stu-id="dd815-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="dd815-113">オプション</span><span class="sxs-lookup"><span data-stu-id="dd815-113">Option</span></span>        |                                    <span data-ttu-id="dd815-114">説明</span><span class="sxs-lookup"><span data-stu-id="dd815-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dd815-115">製品の確認</span><span class="sxs-lookup"><span data-stu-id="dd815-115">Product confirmation</span></span> | <span data-ttu-id="dd815-116">スキャンしたときに、モバイル デバイスから各在庫を確認できます。</span><span class="sxs-lookup"><span data-stu-id="dd815-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |

---
title: 新しいサイトがマッピングされた後、製品とカテゴリが Commerce サイト ビルダーに表示されない
description: このトピックでは、新しいサイトがマッピングされた後、製品とカテゴリが Commerce サイト ビルダーに表示されない場合に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3d7cd2274cb447a622f9ffe6f00b1b27ecc7db52
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801582"
---
# <a name="products-and-categories-dont-appear-in-commerce-site-builder-after-a-new-site-is-mapped"></a><span data-ttu-id="fcef1-103">新しいサイトがマッピングされた後、製品とカテゴリが Commerce サイト ビルダーに表示されない</span><span class="sxs-lookup"><span data-stu-id="fcef1-103">Products and categories don't appear in Commerce site builder after a new site is mapped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fcef1-104">このトピックでは、新しいサイトがマッピングされた後、製品とカテゴリが Commerce サイト ビルダーに表示されない場合に役立つトラブルシューティング ガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="fcef1-104">This topic provides troubleshooting guidance that can help when products and categories don't appear in Commerce site builder after a new site is mapped.</span></span>

## <a name="description"></a><span data-ttu-id="fcef1-105">説明</span><span class="sxs-lookup"><span data-stu-id="fcef1-105">Description</span></span>

<span data-ttu-id="fcef1-106">新しいサイトがマッピングされた後、製品とカテゴリが Commerce サイト ビルダーに表示されません。</span><span class="sxs-lookup"><span data-stu-id="fcef1-106">Products and categories don't appear in Commerce site builder after a new site is mapped.</span></span>

## <a name="resolution"></a><span data-ttu-id="fcef1-107">解像度</span><span class="sxs-lookup"><span data-stu-id="fcef1-107">Resolution</span></span>

### <a name="add-products-to-channel-categories-in-commerce-headquarters"></a><span data-ttu-id="fcef1-108">Commerce 本社のチャネル カテゴリへの製品の追加</span><span class="sxs-lookup"><span data-stu-id="fcef1-108">Add products to channel categories in Commerce headquarters</span></span>

<span data-ttu-id="fcef1-109">Commerce 本社のチャネル カテゴリに製品を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fcef1-109">To add products to channel categories in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="fcef1-110">**Retail と Commerce \> チャネル設定 \> チャネル カテゴリと製品属性** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fcef1-110">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="fcef1-111">左のナビゲーションで、eコマース サイトに表示するカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="fcef1-111">In the left navigation, select the category that should appear on the e-commerce site.</span></span>
1. <span data-ttu-id="fcef1-112">**製品** クイックタブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fcef1-112">On the **Products** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="fcef1-113">**利用できる製品** セクションで、表示する製品を選択し、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fcef1-113">In the **Available Products** section, select the products that should appear, and then select **Add**.</span></span>
1. <span data-ttu-id="fcef1-114">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fcef1-114">Select **OK**.</span></span>
1. <span data-ttu-id="fcef1-115">**製品** クイックタブに製品が表示されたら、アクション ウィンドウで **チャネル更新の公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fcef1-115">After the products appear on the **Products** FastTab, select **Publish channel updates** on the Action Pane.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcef1-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fcef1-116">Additional resources</span></span>

[<span data-ttu-id="fcef1-117">チャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="fcef1-117">Configure a channel to use a channel navigation hierarchy</span></span>](../configure-channel-hierarchy.md)

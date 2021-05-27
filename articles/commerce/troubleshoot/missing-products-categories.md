---
title: 環境コピーの後に製品とカテゴリが欠落している
description: このトピックでは、環境間または同じ環境内でサイトがコピーされた後で製品とカテゴリが欠落している場合に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 4964b9623a91286d4f8260bcae7941feb48f8962
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022401"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="d177d-103">環境コピーの後に製品とカテゴリが欠落している</span><span class="sxs-lookup"><span data-stu-id="d177d-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d177d-104">このトピックでは、環境間または同じ環境内でサイトがコピーされた後で製品とカテゴリが欠落している場合に役立つトラブルシューティング ガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="d177d-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="d177d-105">説明</span><span class="sxs-lookup"><span data-stu-id="d177d-105">Description</span></span>

<span data-ttu-id="d177d-106">サイトが環境間で、または同じ環境内でコピーされた後、製品とカテゴリはサイトから欠落します。</span><span class="sxs-lookup"><span data-stu-id="d177d-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="d177d-107">製品とカテゴリが e コマース サイト ビルダーで e コマース ウェブストアと **製品** タブから欠落しています。</span><span class="sxs-lookup"><span data-stu-id="d177d-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="d177d-108">解像度</span><span class="sxs-lookup"><span data-stu-id="d177d-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="d177d-109">Commerce サイト ビルダーの新しくコピーされたサイトにチャンネルの作業単位番号をマップする</span><span class="sxs-lookup"><span data-stu-id="d177d-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="d177d-110">Commerce サイト ビルダーの新しくコピーされたサイトにチャンネルの作業単位番号 (OUN) をマップするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d177d-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d177d-111">新しくコピーされたサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="d177d-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="d177d-112">**サイトの設定** で、**チャネル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d177d-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="d177d-113">チャネル名の横にある省略記号 (**...**) を選択し、**オンライン店舗チャネルの変更** を選択します 。</span><span class="sxs-lookup"><span data-stu-id="d177d-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="d177d-114">**オンライン店舗のチャネルの変更** ダイアログボックスで、新しくコピーされたサイトにマップするチャネルを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d177d-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="d177d-115">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d177d-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d177d-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d177d-116">Additional resources</span></span>

[<span data-ttu-id="d177d-117">オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="d177d-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)

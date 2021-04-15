---
title: 輸送管理番号順序
description: このトピックでは、輸送管理用の番号順序の設定方法について説明します。
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3da757cbf47e0e1af781b720d17a673e19aeb3b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807683"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="2e3d5-103">輸送管理番号順序</span><span class="sxs-lookup"><span data-stu-id="2e3d5-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e3d5-104">さまざまな製品番号を設定するには、輸送管理モジュールの **番号順序** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="2e3d5-105">製品番号は、配送業者が各出荷の進行状況を整理および追跡するために使用します。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="2e3d5-106">製品番号の番号順序の作成</span><span class="sxs-lookup"><span data-stu-id="2e3d5-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="2e3d5-107">製品番号の番号順序を作成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="2e3d5-108">**輸送管理 \> 設定 \> 配送業者 \> 番号順序** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="2e3d5-109">**新規作成** を選択して、新しい番号順序を作成します。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="2e3d5-110">番号順序のための固有 ID および説明のついた名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="2e3d5-111">**番号順序タイプ** フィールドでは、*製品番号* のみ選択できます。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="2e3d5-112">**チェック ディジット** フィールドでは、*チェック ディジット* が唯一のオプションであり、汎用エンジンとして設定されています。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="2e3d5-113">**シーケンス** クイックタブに、順序に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="2e3d5-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="2e3d5-115">出荷配送業者への番号順序のリンク</span><span class="sxs-lookup"><span data-stu-id="2e3d5-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="2e3d5-116">配送業者に番号順序をリンクするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="2e3d5-117">**輸送管理 \> 設定 \> 配送業者 \> 出荷の配送業者** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="2e3d5-118">出荷配送業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="2e3d5-119">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-119">Select **Edit**.</span></span>
1. <span data-ttu-id="2e3d5-120">**概要** クイックタブで、**製品番号順序** フィールドのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="2e3d5-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2e3d5-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
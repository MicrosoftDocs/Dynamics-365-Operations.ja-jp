---
title: 輸送管理番号順序
description: このトピックでは、輸送管理用の番号順序の設定方法について説明します。
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2c3f087ac76412cd2dce93dcb31b796ce2cb3bc4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2020
ms.locfileid: "4432427"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="b4f9d-103">輸送管理番号順序</span><span class="sxs-lookup"><span data-stu-id="b4f9d-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4f9d-104">さまざまな製品番号を設定するには、輸送管理モジュールの **番号順序** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="b4f9d-105">製品番号は、配送業者が各出荷の進行状況を整理および追跡するために使用します。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="b4f9d-106">製品番号の番号順序の作成</span><span class="sxs-lookup"><span data-stu-id="b4f9d-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="b4f9d-107">製品番号の番号順序を作成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="b4f9d-108">**輸送管理 \> 設定 \> 配送業者 \> 番号順序** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="b4f9d-109">**新規作成** を選択して、新しい番号順序を作成します。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="b4f9d-110">番号順序のための固有 ID および説明のついた名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="b4f9d-111">**番号順序タイプ** フィールドでは、*製品番号* のみ選択できます。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="b4f9d-112">**チェック ディジット** フィールドでは、*チェック ディジット* が唯一のオプションであり、汎用エンジンとして設定されています。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="b4f9d-113">**シーケンス** クイックタブに、順序に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="b4f9d-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="b4f9d-115">出荷配送業者への番号順序のリンク</span><span class="sxs-lookup"><span data-stu-id="b4f9d-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="b4f9d-116">配送業者に番号順序をリンクするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="b4f9d-117">**輸送管理 \> 設定 \> 配送業者 \> 出荷の配送業者** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="b4f9d-118">出荷配送業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="b4f9d-119">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-119">Select **Edit**.</span></span>
1. <span data-ttu-id="b4f9d-120">**概要** クイックタブで、**製品番号順序** フィールドのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="b4f9d-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b4f9d-121">Close the page.</span></span>

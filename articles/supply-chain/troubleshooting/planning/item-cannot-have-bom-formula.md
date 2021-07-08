---
title: 品目に BOM または数式を含めることはできない
description: 注文を確定しようとする際、品目の検証中にエラー メッセージが表示されます。 品目に部品表 (BOM) または数式を含めることはできないことを示しています。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294119"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="0b1bd-104">品目に BOM または数式を含めることはできない</span><span class="sxs-lookup"><span data-stu-id="0b1bd-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="0b1bd-105">エラーコード: PRO2614</span><span class="sxs-lookup"><span data-stu-id="0b1bd-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="0b1bd-106">現象</span><span class="sxs-lookup"><span data-stu-id="0b1bd-106">Symptoms</span></span>

<span data-ttu-id="0b1bd-107">注文を確定しようとする際、品目の検証中に次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="0b1bd-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="0b1bd-108">品目に BOM または数式を含めることができない</span><span class="sxs-lookup"><span data-stu-id="0b1bd-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="0b1bd-109">解決策</span><span class="sxs-lookup"><span data-stu-id="0b1bd-109">Resolution</span></span>

<span data-ttu-id="0b1bd-110">部品表 (BOM) または数式を含む品目は、タイプが *計画品目*、*BOM*、または *数式* である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b1bd-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="0b1bd-111">品目タイプを変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0b1bd-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="0b1bd-112">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0b1bd-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="0b1bd-113">関連する製品を開きます。</span><span class="sxs-lookup"><span data-stu-id="0b1bd-113">Open the relevant product.</span></span>
1. <span data-ttu-id="0b1bd-114">**エンジニア** クイックタブにおいて、**生産タイプ** フィールドを *計画品目*、*BOM*、または *数式* に設定します。</span><span class="sxs-lookup"><span data-stu-id="0b1bd-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>

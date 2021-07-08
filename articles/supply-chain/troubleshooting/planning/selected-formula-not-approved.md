---
title: 選択したフォーミュラ番号がバッチ オーダーに対して承認されていない場合
description: 計画オーダーを確定しようとすると、選択したフォーミュラ番号がバッチ オーダーに対して承認されていないことを示すエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294115"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="a1e80-103">選択したフォーミュラ番号がバッチ オーダーに対して承認されていない場合</span><span class="sxs-lookup"><span data-stu-id="a1e80-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="a1e80-104">エラーコード: PRO2614</span><span class="sxs-lookup"><span data-stu-id="a1e80-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="a1e80-105">現象</span><span class="sxs-lookup"><span data-stu-id="a1e80-105">Symptoms</span></span>

<span data-ttu-id="a1e80-106">計画オーダーを確定しようとする際に、次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="a1e80-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="a1e80-107">選択したフォーミュラ番号は、オーダー (バッチ) に承認されていません。</span><span class="sxs-lookup"><span data-stu-id="a1e80-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="a1e80-108">原因</span><span class="sxs-lookup"><span data-stu-id="a1e80-108">Cause</span></span>

<span data-ttu-id="a1e80-109">システムは、確定操作を検証して、承認済みのフォーミュラが有効な品目に使用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a1e80-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="a1e80-110">数式を承認することが必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a1e80-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="a1e80-111">解決策</span><span class="sxs-lookup"><span data-stu-id="a1e80-111">Resolution</span></span>

<span data-ttu-id="a1e80-112">フォーミュラを承認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a1e80-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="a1e80-113">**製品情報管理 \> 部品表およびフォーミュラ \> フォーミュラ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a1e80-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="a1e80-114">関連するフォーミュラを選択します。</span><span class="sxs-lookup"><span data-stu-id="a1e80-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="a1e80-115">アクション ウィンドウで、**フォーミュラ** タブの **管理** グループで、**フォーミュラの承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a1e80-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="a1e80-116">**BOM またはフォーミュラの承認** ダイアログ ボックスで、承認者を選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a1e80-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>

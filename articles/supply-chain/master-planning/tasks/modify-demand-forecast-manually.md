---
title: 'ガイド: 需要予測の手動変更'
description: このトピックでは、品目の予測を変更する方法を説明します
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224013"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="e5612-103">ガイド: 需要予測の手動変更</span><span class="sxs-lookup"><span data-stu-id="e5612-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5612-104">この手順では、品目の予測を変更する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e5612-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="e5612-105">この手順は、生産の計画者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="e5612-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="e5612-106">選択された品目の予測の変更</span><span class="sxs-lookup"><span data-stu-id="e5612-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="e5612-107">選択された品目の予測を変更するには:</span><span class="sxs-lookup"><span data-stu-id="e5612-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="e5612-108">**モジュール \> 生産情報管理 \> 製品 \> リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e5612-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e5612-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e5612-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="e5612-110">予測を変更する品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5612-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="e5612-111">アクション ペインで、**計画** タブを開き、**需要予測** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5612-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="e5612-112">一覧で行を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5612-112">In the list, select a row.</span></span> <span data-ttu-id="e5612-113">予測明細行がない場合は、アクション ペインで **新規** を選択して、新しい行を作成します。</span><span class="sxs-lookup"><span data-stu-id="e5612-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="e5612-114">**販売数量** フィールドに正の数を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5612-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="e5612-115">この数値は、品目の予測数量を表わします。</span><span class="sxs-lookup"><span data-stu-id="e5612-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="e5612-116">負の数を入力するとエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5612-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="e5612-117">必要に応じて、その他のフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="e5612-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="e5612-118">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5612-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="e5612-119">Microsoft Excel を使って、1 つ以上のアイテムの予測を変更する</span><span class="sxs-lookup"><span data-stu-id="e5612-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="e5612-120">Microsoft Excel を使って、1 つ以上のアイテムの予測を変更するには:</span><span class="sxs-lookup"><span data-stu-id="e5612-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="e5612-121">次のどちらかを実行します。</span><span class="sxs-lookup"><span data-stu-id="e5612-121">Do one of the following:</span></span>
    - <span data-ttu-id="e5612-122">前のセクションで説明したように、任意の品目 (どちらでも構いません) の **需要予測** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="e5612-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="e5612-123">**マスター プラン \> 予測 \> 手動予測入力エントリ \> 需要予測明細行** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e5612-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="e5612-124">アクション ペインで、**Microsoft Office で開く \> 需要予測エントリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5612-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="e5612-125">ダウンロード場所を選択し、保存してから、ダウンロードしたファイルを Excel で開きます。</span><span class="sxs-lookup"><span data-stu-id="e5612-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="e5612-126">警告が表示された場合は、**編集を有効にする** を選択 します。</span><span class="sxs-lookup"><span data-stu-id="e5612-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="e5612-127">Excel で、Microsoft Dynamics 作業ウィンドウを使用して Supply Chain Management にサインインします。</span><span class="sxs-lookup"><span data-stu-id="e5612-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="e5612-128">**サインインしたままにする** オプションを有効にしてサインインする必要があり、データ接続アプリを信頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5612-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="e5612-129">Excel スプレッドシートに、会社の現在の需要予測明細行がすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5612-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="e5612-130">必要に応じて、需要予測明細行を追加、削除、および編集できます。</span><span class="sxs-lookup"><span data-stu-id="e5612-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="e5612-131">Microsoft Dynamics 作業ウィンドウで **発行** を選択 して、変更を Supply Chain Management にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="e5612-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

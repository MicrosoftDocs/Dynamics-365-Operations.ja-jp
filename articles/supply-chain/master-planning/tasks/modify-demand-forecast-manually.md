---
title: 需要予測の手動変更
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
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889027"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="aedaf-103">需要予測の手動変更</span><span class="sxs-lookup"><span data-stu-id="aedaf-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aedaf-104">この手順では、品目の予測を変更する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="aedaf-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="aedaf-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="aedaf-106">この手順は、生産の計画者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="aedaf-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="aedaf-107">選択された品目の予測の変更</span><span class="sxs-lookup"><span data-stu-id="aedaf-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="aedaf-108">選択された品目の予測を変更するには:</span><span class="sxs-lookup"><span data-stu-id="aedaf-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="aedaf-109">**モジュール \> 生産情報管理 \> 製品 \> リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="aedaf-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="aedaf-111">予測を変更する品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="aedaf-112">アクション ペインで、**計画** タブを開き、**需要予測** を選択します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="aedaf-113">一覧で行を選択します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-113">In the list, select a row.</span></span> <span data-ttu-id="aedaf-114">予測明細行がない場合は、アクション ペインで **新規** を選択して、新しい行を作成します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="aedaf-115">**販売数量** フィールドに正の数を入力します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="aedaf-116">この数値は、品目の予測数量を表わします。</span><span class="sxs-lookup"><span data-stu-id="aedaf-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="aedaf-117">負の数を入力するとエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aedaf-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="aedaf-118">必要に応じて、その他のフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="aedaf-119">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="aedaf-120">1 つ以上の品目の予測を変更する Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="aedaf-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="aedaf-121">1 つ以上のアイテムの予測を変更するには Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="aedaf-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="aedaf-122">次のどちらかを実行します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-122">Do one of the following:</span></span>
    - <span data-ttu-id="aedaf-123">前のセクションで説明したように、任意の品目 (どちらでも構いません) の **需要予測** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="aedaf-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="aedaf-124">**マスター プラン \> 予測 \> 手動予測入力エントリ \> 需要予測明細行** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="aedaf-125">アクション ペインで、**Microsoft Office で開く \> 需要予測エントリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="aedaf-126">ダウンロード場所を選択し、保存してから、ダウンロードしたファイルを Excel で開きます。</span><span class="sxs-lookup"><span data-stu-id="aedaf-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="aedaf-127">警告が表示された場合は、**編集を有効にする** を選択 します。</span><span class="sxs-lookup"><span data-stu-id="aedaf-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="aedaf-128">Excel で、Microsoft Dynamics 作業ウィンドウを使用して Supply Chain Management にサインインします。</span><span class="sxs-lookup"><span data-stu-id="aedaf-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="aedaf-129">**サインインしたままにする** オプションを有効にしてサインインする必要があり、データ接続アプリを信頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aedaf-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="aedaf-130">Excel スプレッドシートに、会社の現在の需要予測明細行がすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="aedaf-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="aedaf-131">必要に応じて、需要予測明細行を追加、削除、および編集できます。</span><span class="sxs-lookup"><span data-stu-id="aedaf-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="aedaf-132">Microsoft Dynamics 作業ウィンドウで **発行** を選択 して、変更を Supply Chain Management にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="aedaf-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

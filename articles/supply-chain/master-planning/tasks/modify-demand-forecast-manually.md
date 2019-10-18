---
title: 需要予測の手動変更
description: この手順では、品目の予測を変更する方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec51c1a500b5c9ff2c363cfb69cc1d404e939df9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250648"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="8f387-103">需要予測の手動変更</span><span class="sxs-lookup"><span data-stu-id="8f387-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f387-104">この手順では、品目の予測を変更する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8f387-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="8f387-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="8f387-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8f387-106">この記録は、生産計画担当者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="8f387-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="8f387-107">品目の予測の変更</span><span class="sxs-lookup"><span data-stu-id="8f387-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="8f387-108">**ナビゲーション ウィンドウ**で、**モジュール > 製品情報管理 > 製品 > リリース済製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8f387-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="8f387-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8f387-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="8f387-110">予測を変更する品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f387-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="8f387-111">たとえば、品目「D0001」を選択できます。</span><span class="sxs-lookup"><span data-stu-id="8f387-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="8f387-112">**アクション** ペインで**計画**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f387-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="8f387-113">**需要予測**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f387-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="8f387-114">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="8f387-114">In the list, mark the selected row.</span></span> <span data-ttu-id="8f387-115">予測明細行がない場合は、アプリ バーで新規をクリックして、新しい行を作成します。</span><span class="sxs-lookup"><span data-stu-id="8f387-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="8f387-116">**販売数量**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8f387-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="8f387-117">この数値は、品目の予測数量を表わします。</span><span class="sxs-lookup"><span data-stu-id="8f387-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="8f387-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f387-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="8f387-119">Excel での予測の編集</span><span class="sxs-lookup"><span data-stu-id="8f387-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="8f387-120">Microsoft Office で**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f387-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="8f387-121">Excel で**需要予測の編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f387-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="8f387-122">Excel では、需要予測明細行を追加、削除、および編集できます。</span><span class="sxs-lookup"><span data-stu-id="8f387-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="8f387-123">Excel でデータを検索できない場合、「サインインしたままにする」オプションを有効化することによってサイン インし、データ接続のアプリを信頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f387-123">If you are not able to see the data in Excel, you need to sign in with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  


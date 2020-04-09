---
title: ハブ付帯サービス請求金額および付帯サービス マスターの設定
description: この手順は、ハブ付帯サービス マスターの作成方法と、ハブ付帯サービス請求金額を作成するためのマスターの使用方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ea59326a85d97d53795104f80486f2fac24148a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148528"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="c714b-103">ハブ付帯サービス請求金額および付帯サービス マスターの設定</span><span class="sxs-lookup"><span data-stu-id="c714b-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c714b-104">この手順は、ハブ付帯サービス マスターの作成方法と、ハブ付帯サービス請求金額を作成するためのマスターの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c714b-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="c714b-105">この手順は、USMF データセットを使用します。</span><span class="sxs-lookup"><span data-stu-id="c714b-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="c714b-106">この設定は、通常、配送コーディネーターが実行します。</span><span class="sxs-lookup"><span data-stu-id="c714b-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="c714b-107">ハブ マスターの設定</span><span class="sxs-lookup"><span data-stu-id="c714b-107">Set up a hub master</span></span>
1. <span data-ttu-id="c714b-108">[輸送管理] > [設定] > [評価] > [付帯サービス マスター] に移動します。</span><span class="sxs-lookup"><span data-stu-id="c714b-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="c714b-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c714b-109">Click New.</span></span>
3. <span data-ttu-id="c714b-110">[配送付帯サービス マスター] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c714b-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="c714b-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c714b-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c714b-112">[付帯サービス タイプ] フィールドで、「ハブ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c714b-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="c714b-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c714b-113">Click Save.</span></span>
7. <span data-ttu-id="c714b-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c714b-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="c714b-115">ハブ付帯サービス請求金額の設定</span><span class="sxs-lookup"><span data-stu-id="c714b-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="c714b-116">[輸送管理] > [設定] > [評価] > [ハブ付帯サービス請求金額] に移動します。</span><span class="sxs-lookup"><span data-stu-id="c714b-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="c714b-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c714b-117">Click New.</span></span>
3. <span data-ttu-id="c714b-118">[ハブ付帯サービス ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c714b-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="c714b-119">[ハブ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c714b-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c714b-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c714b-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="c714b-121">[ハブの位置] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c714b-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="c714b-122">集荷または配送として請求金額を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c714b-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="c714b-123">選択内容に応じて、請求金額は、工順に対応する輸送区分に適用されます。</span><span class="sxs-lookup"><span data-stu-id="c714b-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="c714b-124">[配送付帯サービス マスター] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c714b-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c714b-125">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c714b-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c714b-126">作成したマスターを選択します。</span><span class="sxs-lookup"><span data-stu-id="c714b-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="c714b-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c714b-127">Click Save.</span></span>
10. <span data-ttu-id="c714b-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c714b-128">Close the page.</span></span>


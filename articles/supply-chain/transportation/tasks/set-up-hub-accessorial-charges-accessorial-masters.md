---
title: ハブ付帯サービス請求金額および付帯サービス マスターの設定
description: この手順は、ハブ付帯サービス マスターの作成方法と、ハブ付帯サービス請求金額を作成するためのマスターの使用方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f385c8079216de0b5e5d16cbdfc9636dd5bc7725
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214880"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="31780-103">ハブ付帯サービス請求金額および付帯サービス マスターの設定</span><span class="sxs-lookup"><span data-stu-id="31780-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31780-104">この手順は、ハブ付帯サービス マスターの作成方法と、ハブ付帯サービス請求金額を作成するためのマスターの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="31780-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="31780-105">この手順は、USMF データセットを使用します。</span><span class="sxs-lookup"><span data-stu-id="31780-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="31780-106">この設定は、通常、配送コーディネーターが実行します。</span><span class="sxs-lookup"><span data-stu-id="31780-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="31780-107">ハブ マスターの設定</span><span class="sxs-lookup"><span data-stu-id="31780-107">Set up a hub master</span></span>
1. <span data-ttu-id="31780-108">[輸送管理] > [設定] > [評価] > [付帯サービス マスター] に移動します。</span><span class="sxs-lookup"><span data-stu-id="31780-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="31780-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31780-109">Click New.</span></span>
3. <span data-ttu-id="31780-110">[配送付帯サービス マスター] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31780-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="31780-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31780-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="31780-112">[付帯サービス タイプ] フィールドで、「ハブ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="31780-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="31780-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31780-113">Click Save.</span></span>
7. <span data-ttu-id="31780-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="31780-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="31780-115">ハブ付帯サービス請求金額の設定</span><span class="sxs-lookup"><span data-stu-id="31780-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="31780-116">[輸送管理] > [設定] > [評価] > [ハブ付帯サービス請求金額] に移動します。</span><span class="sxs-lookup"><span data-stu-id="31780-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="31780-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31780-117">Click New.</span></span>
3. <span data-ttu-id="31780-118">[ハブ付帯サービス ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31780-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="31780-119">[ハブ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="31780-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="31780-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="31780-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="31780-121">[ハブの位置] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31780-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="31780-122">集荷または配送として請求金額を作成できます。</span><span class="sxs-lookup"><span data-stu-id="31780-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="31780-123">選択内容に応じて、請求金額は、工順に対応する輸送区分に適用されます。</span><span class="sxs-lookup"><span data-stu-id="31780-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="31780-124">[配送付帯サービス マスター] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="31780-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="31780-125">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="31780-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="31780-126">作成したマスターを選択します。</span><span class="sxs-lookup"><span data-stu-id="31780-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="31780-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31780-127">Click Save.</span></span>
10. <span data-ttu-id="31780-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="31780-128">Close the page.</span></span>


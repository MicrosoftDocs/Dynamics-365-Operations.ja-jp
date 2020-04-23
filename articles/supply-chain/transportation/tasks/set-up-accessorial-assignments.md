---
title: 付帯サービス割り当ての設定
description: この手順では、付帯サービスの割り当てを設定する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
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
ms.openlocfilehash: 9c86461f980112e2d759dfd0c905ae2ef05e7041
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214990"
---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="99821-103">付帯サービス割り当ての設定</span><span class="sxs-lookup"><span data-stu-id="99821-103">Set up accessorial assignments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99821-104">この手順では、付帯サービスの割り当てを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="99821-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="99821-105">この設定は、通常、配送コーディネーターにより実行されます。</span><span class="sxs-lookup"><span data-stu-id="99821-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="99821-106">このガイドを使用する前に、「ハブ付帯請求金額および付帯サービス マスターの設定」ガイドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99821-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="99821-107">付帯サービス割り当ての設定</span><span class="sxs-lookup"><span data-stu-id="99821-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="99821-108">[輸送管理] > [設定] > [評価] > [付帯サービス割り当て] に移動します。</span><span class="sxs-lookup"><span data-stu-id="99821-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="99821-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99821-109">Click New.</span></span>
3. <span data-ttu-id="99821-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="99821-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="99821-111">[詳細] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="99821-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="99821-112">[ハブ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="99821-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="99821-113">一覧で、「ハブ付帯請求金額および付帯サービス マスターの設定」ガイドを実行し、付帯サービス マスターを作成したときに使用したハブを選択します。</span><span class="sxs-lookup"><span data-stu-id="99821-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="99821-114">[ハブ付帯サービス ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="99821-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="99821-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="99821-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="99821-116">[基準] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="99821-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="99821-117">条件セクションでは、ここで提供される異なる値に基づいて、請求金額が適用される日付を特定するための正確な条件を選択できます。</span><span class="sxs-lookup"><span data-stu-id="99821-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="99821-118">[常に適用する] オプションをオンに設定します。</span><span class="sxs-lookup"><span data-stu-id="99821-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="99821-119">[付帯サービス割り当てレベル] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="99821-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="99821-120">[計算] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="99821-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="99821-121">[付帯サービス手数料タイプ] フィールドで、「一律」を選択します。</span><span class="sxs-lookup"><span data-stu-id="99821-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="99821-122">付帯サービス手数料タイプによって実際の請求金額の計算方法が特定されます。</span><span class="sxs-lookup"><span data-stu-id="99821-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="99821-123">この例では、一律手数料です。</span><span class="sxs-lookup"><span data-stu-id="99821-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="99821-124">[付帯サービス手数料タイプ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="99821-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="99821-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99821-125">Click Save.</span></span>


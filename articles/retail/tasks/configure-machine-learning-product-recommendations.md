--- 
title: "機械学習を利用する製品の推奨事項のコンフィギュレーション"
description: "この手順では、製品の推奨項目を促進する機械学習システムが使用するエンティティストアが更新され、その後製品の推奨項目がPOSクライアントで有効になります。"
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 46d98ad66aebf89653d9330d3c09118999205d49
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="518e4-103">機械学習を利用する製品の推奨事項のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="518e4-103">Configure machine learning-powered product recommendations</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="518e4-104">この手順では、製品の推奨項目を促進する機械学習システムが使用するエンティティストアが更新され、その後製品の推奨項目がPOSクライアントで有効になります。</span><span class="sxs-lookup"><span data-stu-id="518e4-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="518e4-105">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="518e4-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="518e4-106">[システム管理] > [設定] > [エンティティストア] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="518e4-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="518e4-107">リストで、記録のRetailSalesを検索、選択します。</span><span class="sxs-lookup"><span data-stu-id="518e4-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="518e4-108">[更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="518e4-108">Click Refresh.</span></span>
4. <span data-ttu-id="518e4-109">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="518e4-109">Click OK.</span></span>
5. <span data-ttu-id="518e4-110">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="518e4-110">Close the page.</span></span>
6. <span data-ttu-id="518e4-111">[小売りとコマース] > [本社の設定] > [パラメーター] > [小売パラメーター] に移動します。</span><span class="sxs-lookup"><span data-stu-id="518e4-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="518e4-112">機械学習のタブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="518e4-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="518e4-113">[製品の推薦項目を有効化] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="518e4-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="518e4-114">「推奨モデルが取得できませんでした」というメッセージが表示された場合は、それはエンティティ・ストアが最近更新され、システムが新しいデータとの同化を終了していないことが原因です。</span><span class="sxs-lookup"><span data-stu-id="518e4-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="518e4-115">待機時間は2～3時間です。再度お試しください。</span><span class="sxs-lookup"><span data-stu-id="518e4-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="518e4-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="518e4-116">Click Save.</span></span>
10. <span data-ttu-id="518e4-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="518e4-117">Close the page.</span></span>



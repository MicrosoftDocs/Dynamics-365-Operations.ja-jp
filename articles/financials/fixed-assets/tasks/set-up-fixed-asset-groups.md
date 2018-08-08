--- 
title: "固定資産グループを設定します"
description: "この手順では、新しい固定資産グループを作成する方法を説明します。"
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: d6a4468a05e3e9560c52b9b88071ec5893610c24
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="3df39-103">固定資産グループを設定します</span><span class="sxs-lookup"><span data-stu-id="3df39-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3df39-104">この手順では、新しい固定資産グループを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="3df39-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="3df39-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="3df39-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="3df39-106">[固定資産] > [設定] > [固定資産グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3df39-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="3df39-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3df39-107">Click New.</span></span>
3. <span data-ttu-id="3df39-108">[固定資産グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3df39-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="3df39-109">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3df39-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="3df39-110">固定資産グループにおける固定資産の自動採番と番号順序コードは、固定資産のパラメータの設定より優先されます。</span><span class="sxs-lookup"><span data-stu-id="3df39-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="3df39-111">この固定資産グループの資産に他のグループからの異なる番号付けがある場合、ここでこれを変更できます。</span><span class="sxs-lookup"><span data-stu-id="3df39-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="3df39-112">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3df39-112">Click Books.</span></span>
6. <span data-ttu-id="3df39-113">[帳簿] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3df39-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="3df39-114">[減価償却の計算] フィールドが [はい] に設定されている場合、資産帳簿は償却提案に含まれます。</span><span class="sxs-lookup"><span data-stu-id="3df39-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="3df39-115">減価償却の計算が [いいえ] に設定されている場合、資産は自動的に償却されません。</span><span class="sxs-lookup"><span data-stu-id="3df39-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="3df39-116">資産の耐用年数を設定します。</span><span class="sxs-lookup"><span data-stu-id="3df39-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="3df39-117">耐用年数を設定した後に減価償却期間のフィールド値が計算されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3df39-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="3df39-118">[減価償却方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3df39-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="3df39-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3df39-119">Close the page.</span></span>



---
title: 均等償却を使用した一括比例配分減価償却資産の作成
description: 日本では、耐用年数期間中、毎年均等額で減価償却処理される固定資産のタイプが 3 つあります。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a7a491ad01a2cea6d4964b4ce19ed663d5bc67
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978551"
---
# <a name="create-lump-sum-depreciation-assets-using-equally-divided-method"></a><span data-ttu-id="dee8e-103">均等償却を使用した一括比例配分減価償却資産の作成</span><span class="sxs-lookup"><span data-stu-id="dee8e-103">Create lump-sum depreciation assets using equally divided method</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dee8e-104">日本では、耐用年数期間中、毎年均等額で減価償却処理される固定資産のタイプが 3 つあります。</span><span class="sxs-lookup"><span data-stu-id="dee8e-104">In Japan, 3 types of fixed assets are depreciated with equal amount in each year of its service life.</span></span> <span data-ttu-id="dee8e-105">その 3 つのタイプとは、一括比例配分資産、繰延資産、および低価額資産です。</span><span class="sxs-lookup"><span data-stu-id="dee8e-105">The 3 types are: lump sum assets, deferred assets and low-value assets.</span></span> 



<span data-ttu-id="dee8e-106">このタスクでは、一括比例配分の固定資産の作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-106">Use this task to learn how to create a lump sum fixed asset.</span></span>



<span data-ttu-id="dee8e-107">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dee8e-107">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="dee8e-108">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-108">This task uses the JPMF demo company data.</span></span>


## <a name="create-a-lumpsum-fixed-asset"></a><span data-ttu-id="dee8e-109">一括比例配分固定資産の作成</span><span class="sxs-lookup"><span data-stu-id="dee8e-109">Create a lumpsum fixed asset</span></span>
1. <span data-ttu-id="dee8e-110">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-110">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="dee8e-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee8e-111">Click New.</span></span>
3. <span data-ttu-id="dee8e-112">[固定資産グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-112">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="dee8e-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="dee8e-114">[タイプ] の規定値が [固定資産グループ] により設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-114">Confirm that the Type is defaulted from the Fixed asset group.</span></span>   
    * <span data-ttu-id="dee8e-115">[繰延資産] の [繰延タイプ] を設定します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-115">Set the Type to Deferred for Deferred asset.</span></span>  
    * <span data-ttu-id="dee8e-116">[資産分類] が [一括比例配分] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-116">Confirm that the Asset classification is set to Lump sum</span></span>  
    * <span data-ttu-id="dee8e-117">低価額資産の [低価額] に対する [資産分類] を設定します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-117">Set Asset classification to Low-value for low-value assets.</span></span>  
5. <span data-ttu-id="dee8e-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee8e-118">Click Save.</span></span>
6. <span data-ttu-id="dee8e-119">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dee8e-119">Click Books.</span></span>
7. <span data-ttu-id="dee8e-120">[減価償却] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-120">Expand the Depreciation section.</span></span>
    * <span data-ttu-id="dee8e-121">[方法] が [均等] であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-121">Confirm the Method is Equally divided</span></span>  

## <a name="confirm-the-depreciation-profile"></a><span data-ttu-id="dee8e-122">減価償却プロファイルの確認</span><span class="sxs-lookup"><span data-stu-id="dee8e-122">Confirm the depreciation profile</span></span>
1. <span data-ttu-id="dee8e-123">[固定資産] > [設定] > [減価償却プロファイル] に移動します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-123">Go to Fixed assets > Setup > Depreciation profiles.</span></span>
2. <span data-ttu-id="dee8e-124">[クイック フィルター] を使用して、[減価償却プロファイル] フィールドで「LUMPSUM」という値を指定してフィルターを実行します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-124">Use the Quick Filter to filter on the Depreciation profile field with a value of 'LUMPSUM'.</span></span>
    * <span data-ttu-id="dee8e-125">[方法] が [均等] であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-125">Confirm the Method is Equally divided</span></span>  
    * <span data-ttu-id="dee8e-126">[均等償却年数] が 3 年であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dee8e-126">Confirm that the Number of years to equally divide depreciation is 3</span></span>  
    * <span data-ttu-id="dee8e-127">この値は、固定資産のタイプが一括比例配分か、繰延資産か、または低価額資産かによって異なります。</span><span class="sxs-lookup"><span data-stu-id="dee8e-127">The value varies depending on the type of fixed asset is lump-sum, deferred asset or low-value asset.</span></span>  


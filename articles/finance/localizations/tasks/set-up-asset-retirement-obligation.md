---
title: 資産除去責務ドキュメントの設定と固定資産の ARO 金額の入力
description: 日本では、資産除去責務 (ARO) ドキュメントは資産除去責務の 1 つのタイプを識別します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetRetirementObligationDocument_JP, AssetTable, AssetRetirementObligation_JP, AssetRetirementObligationLine_JP
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fffa82b76a8fade3d1ef721336a9971edb42a1d0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988216"
---
# <a name="set-up-asset-retirement-obligation-documents-and-enter-aro-amount-on-a-fixed-asset"></a><span data-ttu-id="72a2b-103">資産除去責務ドキュメントの設定と固定資産の ARO 金額の入力</span><span class="sxs-lookup"><span data-stu-id="72a2b-103">Set up asset retirement obligation documents and enter ARO amount on a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72a2b-104">日本では、資産除去責務 (ARO) ドキュメントは資産除去責務の 1 つのタイプを識別します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-104">For Japan, an asset retirement obligation (ARO) document identifies one type of asset retirement obligation.</span></span> <span data-ttu-id="72a2b-105">固定資産帳簿に ARO ドキュメントを割り当てると、資産除去時に責務を履行すると予測されるキャッシュ フローを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="72a2b-105">When you assign an ARO document to a fixed asset book, you can specify the cash flow that is expected to perform the obligation at asset retirement.</span></span> 



<span data-ttu-id="72a2b-106">この手順では、ARO ドキュメントの作成、固定資産への割り当て、および見積除去減価の入力方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-106">Use this procedure to learn how to create ARO documents, assign it to a fixed asset and enter the estimated retirement cost.</span></span>



<span data-ttu-id="72a2b-107">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72a2b-107">In order to complete this procedure, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="72a2b-108">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="72a2b-108">This procedure was created using the demo data company JPMF.</span></span>


## <a name="setup-asset-retirement-obligation-document"></a><span data-ttu-id="72a2b-109">資産除去責務ドキュメントの設定</span><span class="sxs-lookup"><span data-stu-id="72a2b-109">Setup asset retirement obligation document</span></span>
1. <span data-ttu-id="72a2b-110">**固定資産 > 資産除去責務 > 資産除去責務ドキュメント** に移動します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-110">Go to **Fixed assets > Asset retirement obligations > Asset retirement obligation documents**.</span></span>
2. <span data-ttu-id="72a2b-111">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72a2b-111">Click **New**.</span></span>
3. <span data-ttu-id="72a2b-112">**ドキュメント ID** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-112">In the **Document ID** field, type a value.</span></span>
4. <span data-ttu-id="72a2b-113">**文書日付** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-113">In the **Document date** field, enter a date.</span></span>
    * <span data-ttu-id="72a2b-114">文書の日付は、固定資産帳簿に ARO ドキュメントを割り当てる際に使用される既定値です。</span><span class="sxs-lookup"><span data-stu-id="72a2b-114">The document date is the default value that is used when assigning the ARO document to a fixed asset book.</span></span>  
    * <span data-ttu-id="72a2b-115">**転記頻度** フィールドで、資産除去責務の支払利子発生頻度を選択します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-115">In the **Posting frequency** field, select the frequency for accruing the interest expense of the asset retirement obligation.</span></span>  
5. <span data-ttu-id="72a2b-116">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-116">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="72a2b-117">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72a2b-117">Click **Save**.</span></span>

## <a name="create-a-fixed-asset-and-assign-the-asset-retirement-obligation-document-to-it"></a><span data-ttu-id="72a2b-118">固定資産の作成および資産除去責務ドキュメントの割り当て</span><span class="sxs-lookup"><span data-stu-id="72a2b-118">Create a fixed asset and assign the asset retirement obligation document to it</span></span>
1. <span data-ttu-id="72a2b-119">**固定資産 > 資産除去責務 > 固定資産** に移動します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-119">Go to **Fixed assets > Asset retirement obligations > Fixed assets**.</span></span>
2. <span data-ttu-id="72a2b-120">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72a2b-120">Click **New**.</span></span>
3. <span data-ttu-id="72a2b-121">**固定資産グループ** フィールドで、固定資産に適用する固定資産グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-121">In the **Fixed asset group** field, select a fixed asset group to apply to the fixed asset.</span></span>
4. <span data-ttu-id="72a2b-122">**名前** フィールドに固定資産の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-122">In the **Name** field, enter a name for the fixed asset.</span></span>
5. <span data-ttu-id="72a2b-123">アクション ウィンドウで、**固定資産** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72a2b-123">On the Action Pane, click **Fixed asset**.</span></span>
6. <span data-ttu-id="72a2b-124">**資産除去責務** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72a2b-124">Click **Asset retirement obligation**.</span></span>
7. <span data-ttu-id="72a2b-125">**帳簿** フィールドで、固定資産の帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-125">In the **Book** field, select the book of the fixed asset.</span></span>
8. <span data-ttu-id="72a2b-126">**ドキュメント ID** フィールドで、固定資産に添付する資産除去ドキュメントの ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="72a2b-126">In the **Document ID** field, select the ID of the asset retirement document to attach to the fixed asset.</span></span>

## <a name="enter-the-asset-retirement-obligation-amounts"></a><span data-ttu-id="72a2b-127">資産除去責務金額の入力</span><span class="sxs-lookup"><span data-stu-id="72a2b-127">Enter the asset retirement obligation amounts</span></span>
1. <span data-ttu-id="72a2b-128">固定資産 **資産除去義務** ページの **見積除去** クイックタブで、**作成** を選択してドロップダウン メニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="72a2b-128">On the fixed asset **Asset retirement obligation** page, on the **Estimated retirement** FastTab, select **Create** to open the drop-down menu.</span></span>
2. <span data-ttu-id="72a2b-129">**トランザクション日付** フィールドで、資産除去責務を認識する日付を入力します</span><span class="sxs-lookup"><span data-stu-id="72a2b-129">In the **Transaction date** field, enter the date on which to recognize the asset retirement obligation</span></span>
3. <span data-ttu-id="72a2b-130">**見積除去原価調整** フィールドにキャッシュ フロー金額を入力します</span><span class="sxs-lookup"><span data-stu-id="72a2b-130">In the **Estimated retirement cost adjustment** field, enter the cash flow amount</span></span>
4. <span data-ttu-id="72a2b-131">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72a2b-131">Click **OK**.</span></span>

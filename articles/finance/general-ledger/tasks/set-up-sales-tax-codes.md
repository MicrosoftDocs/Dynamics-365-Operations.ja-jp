---
title: 消費税コードを設定します
description: このトピックでは、Dynamics 365 Finance で売上税コードを設定する方法について説明します。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f6df5ed3fc49b537845e7d418d4953c0faee5f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994543"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="bc44a-103">消費税コードを設定します</span><span class="sxs-lookup"><span data-stu-id="bc44a-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc44a-104">このトピックでは、消費税コードを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="bc44a-105">売上税コードは、法人が計算、収集、税務当局への支払いの義務のあるそれぞれの間接税または関税について作成されます。</span><span class="sxs-lookup"><span data-stu-id="bc44a-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="bc44a-106">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="bc44a-107">**ナビゲーション ウィンドウ > 税 > 間接税 > 売上税 > 売上税コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="bc44a-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-108">Select **New**.</span></span>
3. <span data-ttu-id="bc44a-109">**売上税コード** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="bc44a-110">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="bc44a-111">プルダウン リストを開いて **決済期間** を選択すると、この売上税の報告と支払いを行う売上税所轄官庁の指定や、その間隔の指定ができます。</span><span class="sxs-lookup"><span data-stu-id="bc44a-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="bc44a-112">総勘定元帳に売上税を転記する主勘定を指定するには、**元帳転記グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="bc44a-113">**計算** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="bc44a-114">これには、売上税額の計算方法を制御する複数のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="bc44a-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="bc44a-115">必要に応じて、これらのフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="bc44a-116">インターフェイスの上部にある **アクション ウィンドウ** で、**売上税コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="bc44a-117">**値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-117">Select **Values**.</span></span>
10. <span data-ttu-id="bc44a-118">この税コードの値を **値** 列に入力します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="bc44a-119">**計算** クイック タブの発生元フィールドで、単位あたりの金額がオンの場合、売上税金額の計算では、値にトランザクションの数量が乗算されます。</span><span class="sxs-lookup"><span data-stu-id="bc44a-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="bc44a-120">税コードが単位に基づく税でない場合、値は、売上税金額を計算するためにこの税コードの発生元に適用される割合を示す値になります。</span><span class="sxs-lookup"><span data-stu-id="bc44a-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="bc44a-121">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-121">Select **Save**.</span></span>
12. <span data-ttu-id="bc44a-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bc44a-122">Close the page.</span></span>
13. <span data-ttu-id="bc44a-123">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc44a-123">Select **Save**.</span></span>


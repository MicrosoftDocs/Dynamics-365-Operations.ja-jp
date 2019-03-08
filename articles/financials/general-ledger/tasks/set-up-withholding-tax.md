---
title: 源泉徴収税の設定
description: 源泉徴収税は仕入先に課せられる税金で、売上税トランザクションを作成しません。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 382b6332665af2491563960a75d498a4f007aba8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "337236"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="864eb-103">源泉徴収税の設定</span><span class="sxs-lookup"><span data-stu-id="864eb-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="864eb-104">源泉徴収税は仕入先に課せられる税金で、売上税トランザクションを作成しません。</span><span class="sxs-lookup"><span data-stu-id="864eb-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="864eb-105">仕入先支払に対して計算される源泉徴収税は負債です。</span><span class="sxs-lookup"><span data-stu-id="864eb-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="864eb-106">このため、源泉徴収税を転記するための有効な勘定は、貸借対照表勘定または負債勘定のみとなります。</span><span class="sxs-lookup"><span data-stu-id="864eb-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="864eb-107">このタスク ガイドでは、源泉徴収税の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="864eb-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="864eb-108">[税] > [間接税] > [源泉徴収税] > [源泉徴収税コード] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="864eb-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="864eb-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="864eb-109">Click New.</span></span>
3. <span data-ttu-id="864eb-110">[源泉徴収税コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="864eb-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="864eb-111">[源泉徴収税名] フィールドに、源泉徴収税コードの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="864eb-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="864eb-112">[主勘定] フィールドで、源泉徴収税の未払税金を転記する主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="864eb-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="864eb-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="864eb-113">Click Save.</span></span>
7. <span data-ttu-id="864eb-114">[値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="864eb-114">Click Values.</span></span>
8. <span data-ttu-id="864eb-115">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="864eb-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="864eb-116">[値] フィールドに、源泉徴収税の計算に使用する割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="864eb-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="864eb-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="864eb-117">Click Save.</span></span>
11. <span data-ttu-id="864eb-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="864eb-118">Close the page.</span></span>
12. <span data-ttu-id="864eb-119">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="864eb-119">Click Save.</span></span>
13. <span data-ttu-id="864eb-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="864eb-120">Close the page.</span></span>
14. <span data-ttu-id="864eb-121">[税] > [間接税] > [源泉徴収税] > [源泉徴収税グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="864eb-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="864eb-122">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="864eb-122">Click New.</span></span>
16. <span data-ttu-id="864eb-123">[源泉徴収税グループ] フィールドで、源泉徴収税グループの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="864eb-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="864eb-124">[説明] フィールドに、源泉徴収税グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="864eb-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="864eb-125">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="864eb-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="864eb-126">[源泉徴収税コード] フィールドで、源泉徴収税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="864eb-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="864eb-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="864eb-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="864eb-128">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="864eb-128">Click Save.</span></span>


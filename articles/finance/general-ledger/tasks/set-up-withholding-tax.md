---
title: 源泉徴収税の設定
description: このトピックでは、源泉徴収税を設定する方法について説明します。
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e7018c79e54841d0729636b08ad475a94d20d5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185960"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="96e56-103">源泉徴収税の設定</span><span class="sxs-lookup"><span data-stu-id="96e56-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="96e56-104">このトピックでは、源泉徴収税を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="96e56-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="96e56-105">*源泉徴収税*は仕入先に課せられる税金で、売上税トランザクションを作成しません。</span><span class="sxs-lookup"><span data-stu-id="96e56-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="96e56-106">仕入先支払に対して計算される源泉徴収税は負債です。</span><span class="sxs-lookup"><span data-stu-id="96e56-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="96e56-107">このため、源泉徴収税を転記するための有効な勘定は、貸借対照表勘定または負債勘定のみとなります。</span><span class="sxs-lookup"><span data-stu-id="96e56-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="96e56-108">このタスク ガイドでは、源泉徴収税の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="96e56-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="96e56-109">**ナビゲーション ウィンドウ > モジュール > 税 > 間接税 > 源泉徴収税 > 源泉徴収税コード**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="96e56-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="96e56-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96e56-110">Select **New**.</span></span>
3. <span data-ttu-id="96e56-111">**源泉徴収税コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="96e56-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="96e56-112">**源泉徴収税名**フィールドに、源泉徴収税コードの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="96e56-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="96e56-113">**主勘定**フィールドで、源泉徴収税の未払税金を転記する主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="96e56-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="96e56-114">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96e56-114">Select **Save**.</span></span>
7. <span data-ttu-id="96e56-115">**値**を選択し、リスト内の目的のレコードをマークします。</span><span class="sxs-lookup"><span data-stu-id="96e56-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="96e56-116">**値**フィールドに、源泉徴収税の計算に使用する割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="96e56-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="96e56-117">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96e56-117">Select **Save**.</span></span>
10. <span data-ttu-id="96e56-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="96e56-118">Close the page.</span></span>
11. <span data-ttu-id="96e56-119">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96e56-119">Select **Save**.</span></span>
12. <span data-ttu-id="96e56-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="96e56-120">Close the page.</span></span>
13. <span data-ttu-id="96e56-121">**ナビゲーション ウィンドウ > モジュール > 税 > 間接税 > 源泉徴収税 > 源泉徴収税グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="96e56-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="96e56-122">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96e56-122">Select **New**.</span></span>
15. <span data-ttu-id="96e56-123">**源泉徴収税グループ** フィールドで、源泉徴収税グループの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="96e56-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="96e56-124">**説明**フィールドに、源泉徴収税グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="96e56-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="96e56-125">**源泉徴収税コード** フィールドで、源泉徴収税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="96e56-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="96e56-126">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96e56-126">Select **Save**.</span></span>
19. <span data-ttu-id="96e56-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="96e56-127">Close the page.</span></span>


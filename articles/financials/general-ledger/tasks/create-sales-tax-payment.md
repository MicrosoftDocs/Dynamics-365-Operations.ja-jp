--- 
title: "売上税支払の作成"
description: "売上税の決済と転記のジョブは、売上税勘定の売上税残高を決済して、特定の期間の売上税決済勘定と相殺します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 9b6e60ff6465ef0bddda2e93b07f41e47f2e1ddd
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="9579a-103">売上税支払の作成</span><span class="sxs-lookup"><span data-stu-id="9579a-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9579a-104">売上税の決済と転記のジョブは、売上税勘定の売上税残高を決済して、特定の期間の売上税決済勘定と相殺します。</span><span class="sxs-lookup"><span data-stu-id="9579a-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="9579a-105">[税] > [申告] > [売上税] > [売上税の決済と転記] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9579a-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="9579a-106">[決済期間] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9579a-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9579a-107">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9579a-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9579a-108">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="9579a-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="9579a-109">[訂正を含める] オプションが [総勘定元帳のパラメータ] のページで選択されていない場合、決済は、異なるバージョンについて処理できます。</span><span class="sxs-lookup"><span data-stu-id="9579a-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="9579a-110">[オリジナル] は決済期間の最初の決済で、1 つの間隔について 1 回のみ処理できます。</span><span class="sxs-lookup"><span data-stu-id="9579a-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="9579a-111">最新の修正は、オリジナル バージョンの作成後に転記された売上税トランザクションを決済します。</span><span class="sxs-lookup"><span data-stu-id="9579a-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="9579a-112">[トランザクション日付] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="9579a-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="9579a-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9579a-113">Click OK.</span></span>



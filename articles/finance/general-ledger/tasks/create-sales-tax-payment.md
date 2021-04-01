---
title: 消費税支払の作成
description: 売上税の決済と転記のジョブでは、売上税勘定の売上税残高を決済して、特定の期間の売上税決済勘定と相殺します。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9523ef75953bdca36f509f596c51c08b12b3fdb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254466"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="1a48d-103">消費税支払の作成</span><span class="sxs-lookup"><span data-stu-id="1a48d-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a48d-104">売上税の決済と転記のジョブでは、売上税勘定の売上税残高を決済して、特定の期間の売上税決済勘定と相殺します。</span><span class="sxs-lookup"><span data-stu-id="1a48d-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="1a48d-105">**税 > 申告 > 売上税 > 売上税の決済と転記** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1a48d-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="1a48d-106">**決済期間** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="1a48d-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="1a48d-107">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a48d-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1a48d-108">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a48d-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="1a48d-109">**訂正を含める** オプションが **総勘定元帳のパラメーター** のページで選択されていない場合、決済処理で異なるバージョンを処理できます。</span><span class="sxs-lookup"><span data-stu-id="1a48d-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="1a48d-110">[オリジナル] は決済期間の最初の決済であり、1 つのサイクル間隔で 1 回のみ処理できます。</span><span class="sxs-lookup"><span data-stu-id="1a48d-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="1a48d-111">最新の修正は、オリジナル バージョンの作成後に転記された売上税のトランザクションを決済します。</span><span class="sxs-lookup"><span data-stu-id="1a48d-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="1a48d-112">**トランザクション日付** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a48d-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="1a48d-113">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a48d-113">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
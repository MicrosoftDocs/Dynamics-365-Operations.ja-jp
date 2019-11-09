---
title: 仕入先請求書の売上税の計算と調整
description: このトピックでは、Dynamics 365 Finance で、仕入先請求書の売上税を調整する方法について説明します。
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68e0df78516875168d977f78adf023887b2362d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186282"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="ec56f-103">仕入先請求書の売上税の計算と調整</span><span class="sxs-lookup"><span data-stu-id="ec56f-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ec56f-104">このトピックでは、仕入先請求書の売上税を調整する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="ec56f-105">オリジナルの元伝票が計算と異なる税額を表示している場合、転記前にこれらの金額を調整できます。</span><span class="sxs-lookup"><span data-stu-id="ec56f-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="ec56f-106">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="ec56f-107">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 請求書 > 請求書仕訳帳**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="ec56f-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-108">Select **New**.</span></span>
3. <span data-ttu-id="ec56f-109">新しい行の**名前**フィールドで、ドロップダウン メニューのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="ec56f-110">アクション ウィンドウで、**明細行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="ec56f-111">**勘定**フィールドで、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="ec56f-112">**請求書**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="ec56f-113">**貸方**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="ec56f-114">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="ec56f-115">**売上税**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="ec56f-116">**実際の売上税の合計金額**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="ec56f-117">**調整**タブで、売上税コードごとに売上税金額を調整できます。</span><span class="sxs-lookup"><span data-stu-id="ec56f-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="ec56f-118">**計算上の金額から実績をリセット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="ec56f-119">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-119">Select **OK**.</span></span>
14. <span data-ttu-id="ec56f-120">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec56f-120">Select **Save**.</span></span>

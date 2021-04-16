---
title: 固定資産の取得の提案
description: このトピックでは、固定資産仕訳帳の取得提案を使用して固定資産を取得する方法について説明します。
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817171"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="ddcf4-103">固定資産の取得の提案</span><span class="sxs-lookup"><span data-stu-id="ddcf4-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ddcf4-104">このトピックでは、固定資産仕訳帳の取得提案を使用して固定資産を取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="ddcf4-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="ddcf4-106">固定資産提案仕訳帳を使用して固定資産を取得するには、最初に固定資産レコードを作成し、次に、取得価格を資産帳簿に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="ddcf4-107">資産取得提案を作成する</span><span class="sxs-lookup"><span data-stu-id="ddcf4-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="ddcf4-108">資産取得提案を作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="ddcf4-109">ナビゲーション ウィンドウで、**モジュール > 固定資産 > 仕訳入力 > 固定資産仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="ddcf4-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-110">Select **New**.</span></span>
3. <span data-ttu-id="ddcf4-111">**名前** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="ddcf4-112">アクション ウィンドウで、**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="ddcf4-113">**提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="ddcf4-114">**取得提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="ddcf4-115">**フィルター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-115">Select **Filter**.</span></span> <span data-ttu-id="ddcf4-116">**リセット** を選択すると、前の値がクリアされます。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="ddcf4-117">**固定資産番号** の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="ddcf4-118">**基準** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="ddcf4-119">この提案と一緒に取得したい固定資産の残余基準を設定します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="ddcf4-120">**OK** を 2 回選択して、ウィンドウを終了します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="ddcf4-121">作成されたトランザクション明細行を確認します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="ddcf4-122">帳簿で設定された取得日付と取得価格が付いている固定資産のみが取得提案に含まれます。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="ddcf4-123">ページで、**帳簿** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="ddcf4-124">**投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="ddcf4-125">取得提案に既定の財務分析コードを含める</span><span class="sxs-lookup"><span data-stu-id="ddcf4-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="ddcf4-126">取得トランザクションは、Excel アドインを使用して作成できます。このトランザクションは、**固定資産 > 仕訳帳エントリ > 固定資産仕訳帳** にアクセスして作成できます。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="ddcf4-127">新しい仕訳帳を作成し、ページの **明細行** セクションに移動して Excel アイコンを選択し、固定資産仕訳帳明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="ddcf4-128">仕訳帳明細行を表す Excel テンプレートが作成され、開きます。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="ddcf4-129">テンプレートに追加する仕訳帳明細行のデータを追加し、その情報を再度システムに公開します。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="ddcf4-130">選択した資産帳と、Excel テンプレートに入力された対応する固定資産に対して既定の分析コードが設定されている場合、Excel からシステムに仕訳帳を発行するときに、既定の財務分析コードが資産帳マスター データから呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="ddcf4-131">Excel アドインから固定資産仕訳帳を発行する際に、資産帳に自動的に財務分析コードを含めるには、既定の分析コードを事前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddcf4-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]

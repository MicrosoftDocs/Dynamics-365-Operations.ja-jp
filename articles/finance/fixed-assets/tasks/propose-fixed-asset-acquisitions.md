---
title: 固定資産の取得の提案
description: このトピックでは、固定資産仕訳帳の取得提案を使用して固定資産を取得する方法について説明します。
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0997af638c141661afb677e2407a90a883168aed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445042"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="1e21d-103">固定資産の取得の提案</span><span class="sxs-lookup"><span data-stu-id="1e21d-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1e21d-104">このトピックでは、固定資産仕訳帳の取得提案を使用して固定資産を取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="1e21d-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="1e21d-106">固定資産提案仕訳帳を使用して固定資産を取得するには、最初に固定資産レコードを作成し、次に、取得価格を資産帳簿に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e21d-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="1e21d-107">ナビゲーション ウィンドウで、**モジュール > 固定資産 > 仕訳入力 > 固定資産仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="1e21d-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-108">Select **New**.</span></span>
3. <span data-ttu-id="1e21d-109">**名前** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="1e21d-110">アクション ペインで、**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="1e21d-111">**提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="1e21d-112">**取得提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="1e21d-113">**フィルター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-113">Select **Filter**.</span></span> <span data-ttu-id="1e21d-114">**リセット** を選択すると、前の値をクリアします。</span><span class="sxs-lookup"><span data-stu-id="1e21d-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="1e21d-115">**固定資産番号** の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="1e21d-116">**基準** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="1e21d-117">この提案と一緒に取得したい固定資産の残余基準を設定します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="1e21d-118">**OK** を 2 回選択して、ウィンドウを終了します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="1e21d-119">作成したトランザクション明細行を確認します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="1e21d-120">帳簿で設定された取得日付と取得価格が付いている固定資産のみが取得提案に含まれます。</span><span class="sxs-lookup"><span data-stu-id="1e21d-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="1e21d-121">ページで、**帳簿** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="1e21d-122">**投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e21d-122">Select **Post**.</span></span>

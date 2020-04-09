---
title: 固定資産の取得の提案
description: このトピックでは、固定資産仕訳帳の取得提案を使用して固定資産を取得する方法について説明します。
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
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
ms.openlocfilehash: e08177aad2db2438c2d5d4ddd294c1056b88167c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142734"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="d29ab-103">固定資産の取得の提案</span><span class="sxs-lookup"><span data-stu-id="d29ab-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d29ab-104">このトピックでは、固定資産仕訳帳の取得提案を使用して固定資産を取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="d29ab-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="d29ab-106">ナビゲーション ペインで、**モジュール > 固定資産 > 仕訳入力 > 固定資産仕訳帳**に移動します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="d29ab-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-107">Select **New**.</span></span>
3. <span data-ttu-id="d29ab-108">**名前**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="d29ab-109">アクション ペインで、**明細行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="d29ab-110">**提案**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="d29ab-111">**取得提案**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="d29ab-112">**フィルター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-112">Select **Filter**.</span></span> <span data-ttu-id="d29ab-113">**リセット**を選択すると、前の値をクリアします。</span><span class="sxs-lookup"><span data-stu-id="d29ab-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="d29ab-114">**固定資産番号**の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="d29ab-115">**基準**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="d29ab-116">この提案と一緒に取得したい固定資産の残余基準を設定します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="d29ab-117">**OK** を 2 回選択して、ウィンドウを終了します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="d29ab-118">作成したトランザクション明細行を確認します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="d29ab-119">帳簿で設定された取得日付と取得価格が付いている固定資産のみが取得提案に含まれます。</span><span class="sxs-lookup"><span data-stu-id="d29ab-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="d29ab-120">ページで、**帳簿**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="d29ab-121">**投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d29ab-121">Select **Post**.</span></span>


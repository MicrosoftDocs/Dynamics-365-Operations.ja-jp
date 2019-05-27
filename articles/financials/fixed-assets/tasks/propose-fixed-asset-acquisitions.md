---
title: 固定資産の取得の提案
description: この手順では、固定資産仕訳帳の取得提案を使用して固定資産の取得方法を示します。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1891206bb266b126eccfa789b8c8062c9bfa688b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570883"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="208d1-103">固定資産の取得の提案</span><span class="sxs-lookup"><span data-stu-id="208d1-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="208d1-104">この手順では、固定資産仕訳帳の取得提案を使用して固定資産の取得方法を示します。</span><span class="sxs-lookup"><span data-stu-id="208d1-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="208d1-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="208d1-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="208d1-106">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="208d1-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="208d1-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="208d1-107">Click New.</span></span>
3. <span data-ttu-id="208d1-108">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="208d1-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="208d1-109">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="208d1-109">Click Lines.</span></span>
5. <span data-ttu-id="208d1-110">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="208d1-110">Click Proposals.</span></span>
6. <span data-ttu-id="208d1-111">[取得提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="208d1-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="208d1-112">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="208d1-112">Click Filter.</span></span>
8. <span data-ttu-id="208d1-113">[リセット] をクリックすると、前の値をクリアします。</span><span class="sxs-lookup"><span data-stu-id="208d1-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="208d1-114">固定資産番号の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="208d1-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="208d1-115">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="208d1-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="208d1-116">この提案と一緒に取得したい固定資産の残余基準を設定します。</span><span class="sxs-lookup"><span data-stu-id="208d1-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="208d1-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="208d1-117">Click OK.</span></span>
12. <span data-ttu-id="208d1-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="208d1-118">Click OK.</span></span>
    * <span data-ttu-id="208d1-119">作成したトランザクション明細行を確認します。</span><span class="sxs-lookup"><span data-stu-id="208d1-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="208d1-120">帳簿で設定された取得日付と取得価格が付いている固定資産のみが取得提案に含まれます。</span><span class="sxs-lookup"><span data-stu-id="208d1-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="208d1-121">[帳簿] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="208d1-121">Click the Books tab.</span></span>
14. <span data-ttu-id="208d1-122">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="208d1-122">Click Post.</span></span>


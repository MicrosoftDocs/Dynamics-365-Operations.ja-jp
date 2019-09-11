---
title: 転記された仕訳帳の仕訳入力
description: この手順では、転記された仕訳入力の仕訳を行う方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e20229ca910aa0d7d820434c22edf5a27030bba5
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916256"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="de8a2-103">転記された仕訳帳の仕訳入力</span><span class="sxs-lookup"><span data-stu-id="de8a2-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="de8a2-104">この手順では、転記された仕訳入力の仕訳を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="de8a2-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="de8a2-105">この手順では、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="de8a2-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="de8a2-106">**ナビゲーション ウィンドウ**で、**モジュール > 一般会計 > 元帳の設定 > 一般会計パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de8a2-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="de8a2-107">**拡張仕訳元帳**フィールドは、はいまたはいいえに設定します。</span><span class="sxs-lookup"><span data-stu-id="de8a2-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="de8a2-108">[はい] の場合は、レポートの出力が異なります。</span><span class="sxs-lookup"><span data-stu-id="de8a2-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="de8a2-109">仕訳プロセスが実行されなかった場合に、期間を終了するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="de8a2-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="de8a2-110">このオプションが [はい] に設定されている場合、期間は仕訳プロセスがその期間に対して完了するまで、閉じることはできません。</span><span class="sxs-lookup"><span data-stu-id="de8a2-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="de8a2-111">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="de8a2-111">Close the page.</span></span>
5. <span data-ttu-id="de8a2-112">**ナビゲーション ウィンドウ**で、**モジュール > 一般会計 > 定期処理タスク > 仕訳**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de8a2-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="de8a2-113">**フィルター**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de8a2-113">Click **Filter**.</span></span>
7. <span data-ttu-id="de8a2-114">定義するフィルター基準の行を強調表示します。</span><span class="sxs-lookup"><span data-stu-id="de8a2-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="de8a2-115">**基準**フィールドで、フィルター基準を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="de8a2-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="de8a2-116">**OK** をクリックして、フィルター ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="de8a2-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="de8a2-117">**OK** をクリックして仕訳入力プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="de8a2-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="de8a2-118">レポートは、プロセスが完了した後生成されます。</span><span class="sxs-lookup"><span data-stu-id="de8a2-118">A report will be generated after the process is complete.</span></span>  


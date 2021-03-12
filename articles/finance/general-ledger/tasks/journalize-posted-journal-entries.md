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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad18063e0a66a4aac0ebef7f0ce45c73137abcc7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968532"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="cb675-103">転記された仕訳帳の仕訳入力</span><span class="sxs-lookup"><span data-stu-id="cb675-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb675-104">この手順では、転記された仕訳入力の仕訳を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cb675-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="cb675-105">この手順では、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="cb675-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="cb675-106">**ナビゲーション ウィンドウ** で、**モジュール > 一般会計 > 元帳の設定 > 一般会計パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb675-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="cb675-107">**拡張仕訳元帳** フィールドは、はいまたはいいえに設定します。</span><span class="sxs-lookup"><span data-stu-id="cb675-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="cb675-108">[はい] の場合は、レポートの出力が異なります。</span><span class="sxs-lookup"><span data-stu-id="cb675-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="cb675-109">仕訳プロセスが実行されなかった場合に、期間を終了するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="cb675-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="cb675-110">このオプションが [はい] に設定されている場合、期間は仕訳プロセスがその期間に対して完了するまで、閉じることはできません。</span><span class="sxs-lookup"><span data-stu-id="cb675-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="cb675-111">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cb675-111">Close the page.</span></span>
5. <span data-ttu-id="cb675-112">**ナビゲーション ウィンドウ** で、**モジュール > 一般会計 > 定期処理タスク > 仕訳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb675-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="cb675-113">**フィルター** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb675-113">Click **Filter**.</span></span>
7. <span data-ttu-id="cb675-114">定義するフィルター基準の行を強調表示します。</span><span class="sxs-lookup"><span data-stu-id="cb675-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="cb675-115">**基準** フィールドで、フィルター基準を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cb675-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="cb675-116">**OK** をクリックして、フィルター ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cb675-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="cb675-117">**OK** をクリックして仕訳入力プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="cb675-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="cb675-118">レポートは、プロセスが完了した後生成されます。</span><span class="sxs-lookup"><span data-stu-id="cb675-118">A report will be generated after the process is complete.</span></span>  


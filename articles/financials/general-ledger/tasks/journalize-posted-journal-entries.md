---
title: 転記された仕訳帳の仕訳入力
description: この手順では、転記された仕訳入力の仕訳を行う方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: cbf7ee8063487303cd4c8d2b76a8b44bacc86193
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846394"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="78bed-103">転記された仕訳帳の仕訳入力</span><span class="sxs-lookup"><span data-stu-id="78bed-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="78bed-104">この手順では、転記された仕訳入力の仕訳を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="78bed-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="78bed-105">この手順では、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="78bed-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="78bed-106">[総勘定元帳] > [元帳の設定] > [総勘定元帳パラメーター] で仕訳入力の設定を検証します。</span><span class="sxs-lookup"><span data-stu-id="78bed-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="78bed-107">拡張仕訳元帳フィールドは、[はい] または [いいえ] に設定します。</span><span class="sxs-lookup"><span data-stu-id="78bed-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="78bed-108">[はい] の場合は、レポートの出力が異なります。</span><span class="sxs-lookup"><span data-stu-id="78bed-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="78bed-109">仕訳プロセスが実行されなかった場合に、期間を終了するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="78bed-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="78bed-110">このオプションが [はい] に設定されている場合、期間は仕訳プロセスがその期間に対して完了するまで、閉じることはできません。</span><span class="sxs-lookup"><span data-stu-id="78bed-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="78bed-111">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="78bed-111">Close the page.</span></span>
5. <span data-ttu-id="78bed-112">[総勘定元帳] > [定期処理タスク] > [仕訳入力] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="78bed-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="78bed-113">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78bed-113">Click Filter.</span></span>
7. <span data-ttu-id="78bed-114">定義するフィルター基準の行を強調表示します。</span><span class="sxs-lookup"><span data-stu-id="78bed-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="78bed-115">[基準] フィールドで、フィルター基準を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="78bed-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="78bed-116">[OK] をクリックして、フィルター ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="78bed-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="78bed-117">[OK] をクリックして仕訳入力プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="78bed-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="78bed-118">レポートは、プロセスが完了した後生成されます。</span><span class="sxs-lookup"><span data-stu-id="78bed-118">A report will be generated after the process is complete.</span></span>  


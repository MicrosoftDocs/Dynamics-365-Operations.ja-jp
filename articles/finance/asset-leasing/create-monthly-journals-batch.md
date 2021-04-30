---
title: バッチ内の月次仕訳入力の作成
description: このトピックでは、バッチで仕訳入力を作成し、月別のリース経費を記録する際の効率を高める方法について説明します。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ca84e56569ea5ddbb4d5335d0944a6bd8a50a1b1
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881207"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="2f863-103">バッチ内の月次仕訳入力の作成</span><span class="sxs-lookup"><span data-stu-id="2f863-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f863-104">このトピックでは、バッチで仕訳入力を作成し、月別のリース経費を記録する際の効率を高める方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f863-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="2f863-105">バッチ処理を使用すると、複数のスケジュールから仕訳入力を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2f863-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="2f863-106">これらの仕訳入力には、リース支払、負債償却費、使用権 (ROU) 資産償却、履行費用経費が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2f863-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="2f863-107">また、バッチ処理を利用して、複数のリースの初期認識を同時に行ったり、複数のリースの移行調整を同時に行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="2f863-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="2f863-108">バッチ ジョブの設定や、複数のリースの支払請求書、減価償却、利息を処理するには、**資産リース \> 定期処理 \> バッチ仕訳作成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f863-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="2f863-109">表示されるダイアログ ボックスで、仕訳入力の作成元となるスケジュールを選択できます。</span><span class="sxs-lookup"><span data-stu-id="2f863-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="2f863-110">また、特定のエンティティ、リース グループ、またはリース ブックに対してバッチ処理を実行するかどうかを指定することもできます</span><span class="sxs-lookup"><span data-stu-id="2f863-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="2f863-111">負債の償却予定額、支払額、減価償却費、費用の計上は、リース取引開始時に認識したものを転記した後に行います。</span><span class="sxs-lookup"><span data-stu-id="2f863-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="2f863-112">仕訳入力は作成されますが、**実行** コマンドを選択するまでは転記されません。</span><span class="sxs-lookup"><span data-stu-id="2f863-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

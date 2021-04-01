---
title: リース負債の短期部分の再分類
description: このトピックでは、一部のリース負債を短期として再分類するための月次仕訳入力の作成方法について説明します。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9189033987a3072c7122e1a198768d9de6aa2a52
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254086"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="e6c4e-103">リース負債の短期部分の再分類</span><span class="sxs-lookup"><span data-stu-id="e6c4e-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6c4e-104">このトピックでは、一部のリース負債を短期として再分類するための月次仕訳入力の作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="e6c4e-105">バッチ プロセスで選択されたスケジュールが **短期リース負債の再分類** の場合は、仕訳入力が作成されます。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="e6c4e-106">このエントリは、月の最後の日にリース負債の現在の部分を転記するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="e6c4e-107">同時に、次の月の最初の日の時点で、取消エントリが転記されます。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="e6c4e-108">リース負債の短期の部分は、負債の償却スケジュールとして示されています。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="e6c4e-109">仕訳入力が転記されると、**負債再分類の仕訳が生成済み** 列が使用可能になり、スケジュールにも仕訳 ID が入力されます。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="e6c4e-110">短期負債の再登録仕訳入力を作成および転記するには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="e6c4e-111">**資産リース \> 定期 \> バッチ仕訳の生成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="e6c4e-112">**バッチ仕訳作成** ダイアログ ボックスの **スケジュールの選択** フィールドで、**短期リース負債の再分類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="e6c4e-113">**リース グループ゜** フィールドで、リース グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="e6c4e-114">または、**帳簿 ID** フィールドで、帳簿 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="e6c4e-115">**転記** パラメータをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="e6c4e-116">または、エントリを作成するが転記されない場合は、このパラメータをオフのままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="e6c4e-117">転記の前に **転記の前にプレビュー** パラメータをオンにして、このエントリを表示します。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="e6c4e-118">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6c4e-118">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 資産リースの移行調整仕訳入力の転記
description: このトピックでは、リース ポートフォリオを新しいリース会計基準、Accounting Standards Codification Topic 842 (ASC 842) および International Financial Reporting Standard 16 (IFRS 16) に移行できる機能について説明します。
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4af7b9dc7a03a6d17ff34ffc726eb87e848dd785
ms.sourcegitcommit: f0f5545a8ff99583e0131f435d91c64bb68a1c38
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "4445402"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="7e484-103">資産リースの移行調整仕訳入力の転記</span><span class="sxs-lookup"><span data-stu-id="7e484-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e484-104">このトピックでは、リース ポートフォリオを次の新しいリース会計基準、米国 (US GAAP) および International Financial Reporting Standard 16 (IFRS 16) の標準規格である、Accounting Standards Codification Topic 842 (ASC 842)、に移行するために使用できる機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="7e484-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="7e484-105">新しい基準への切り替えに関する帳簿の設定方法については、[リース帳簿の設定](set-up-lease-books.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e484-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="7e484-106">切り替え調整仕訳入力を作成すると、仕訳入力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7e484-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="7e484-107">この入力には、その日付に新しい標準が追加されたときにリースを記録したときの貸借対照表への影響が反映されます。</span><span class="sxs-lookup"><span data-stu-id="7e484-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="7e484-108">該当する日付のキャリー額に対して適切な資産勘定が借方に転記され、負債勘定が貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="7e484-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="7e484-109">この差額は、保留中の収益に借方または貸方記入されます。</span><span class="sxs-lookup"><span data-stu-id="7e484-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="7e484-110">新しい会計基準に準拠するように切り替え調整を転記するには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="7e484-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="7e484-111">**リースの概要** ページで、リースを選択して **帳簿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e484-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="7e484-112">帳簿で、**支払スケジュール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e484-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="7e484-113">**支払スケジュール** ダイアログ ボックスで、**確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e484-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="7e484-114">ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7e484-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="7e484-115">**切り替えの調整** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e484-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e484-116">**切り替え帳簿** フィールドが使用可能な帳簿に割り当てられているリース帳簿に対してのみ、切り替え調整を作成できます。</span><span class="sxs-lookup"><span data-stu-id="7e484-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="7e484-117">**リースの開始日** フィールドの値が切り替え日よりも後の場合、**切り替え調整** フィールドの値は更新されません。</span><span class="sxs-lookup"><span data-stu-id="7e484-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="7e484-118">仕訳入力を表示するには、**資産リース仕訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e484-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="7e484-119">新規仕訳を選択し、**転記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e484-119">Select the new journal, and then select **Post**.</span></span>

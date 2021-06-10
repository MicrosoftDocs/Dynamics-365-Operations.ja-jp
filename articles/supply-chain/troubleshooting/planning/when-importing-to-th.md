---
title: 変更を行っていないにもかかわらず、品目補充設定を保存するように求められます
description: 変更を行っていないにもかかわらず、品目補充設定を保存するように求められます。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049476"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="23a7a-103">変更を行っていないにもかかわらず、品目補充設定を保存するように求められます</span><span class="sxs-lookup"><span data-stu-id="23a7a-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="23a7a-104">KB 番号: 4615588</span><span class="sxs-lookup"><span data-stu-id="23a7a-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="23a7a-105">現象</span><span class="sxs-lookup"><span data-stu-id="23a7a-105">Symptoms</span></span>

<span data-ttu-id="23a7a-106">シナリオによっては、*品目補充 V2* エンティティを通じて品目をインポートした後に **品目補充** ページを開くと、次のメッセージが表示される場合があります:</span><span class="sxs-lookup"><span data-stu-id="23a7a-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="23a7a-107">閉じる前に変更内容を保存しますか?</span><span class="sxs-lookup"><span data-stu-id="23a7a-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="23a7a-108">何も変更を行っていない場合でも、このメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="23a7a-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="23a7a-109">解決策</span><span class="sxs-lookup"><span data-stu-id="23a7a-109">Resolution</span></span>

<span data-ttu-id="23a7a-110">**品目補充** ページには複雑な既定のロジックが含まれており、エンティティ インポートなどにより、データベースに直接変更が行われた後にメッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="23a7a-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="23a7a-111">たとえば、`AREGENERALSETTINGSOVERRIDDEN` のエンティティ フィールドは *いいえ* に設定されていますが、`PRODUCTCOVERAGEGROUPID` や `VENDORACCOUNTNUMBER` などのフィールドに新しい値や変更された値を提供するファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="23a7a-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="23a7a-112">この場合、`AREGENERALSETTINGSOVERRIDDEN` フィールドが *いいえ* に設定されているため、**品目補充** ページをインポート後に初めて開いたときにフィールドから値が自動的にクリアされます。</span><span class="sxs-lookup"><span data-stu-id="23a7a-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="23a7a-113">メッセージ ボックスのプロンプトに従って変更を保存すると、変更内容はデータベースに保存されます。</span><span class="sxs-lookup"><span data-stu-id="23a7a-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="23a7a-114">そうしない場合は、次にページを開いた時に同じメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="23a7a-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="23a7a-115">この動作を回避し、エンティティ インポートで `PRODUCTCOVERAGEGROUPID` などのフィールドの値も含めるには、インポート時に `AREGENERALSETTINGSOVERRIDDEN` を *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="23a7a-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>

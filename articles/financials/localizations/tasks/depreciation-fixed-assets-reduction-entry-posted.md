---
title: 圧縮記帳の転記が存在する固定資産の減価償却
description: このタスクを使用して、圧縮記帳で固定資産の減価償却を実行する方法を把握します。 このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d002e07263ade34c3414e73a351fc4b7436cd4f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565084"
---
# <a name="depreciation-of-fixed-assets-with-reduction-entry-posted"></a><span data-ttu-id="1afe6-104">圧縮記帳の転記が存在する固定資産の減価償却</span><span class="sxs-lookup"><span data-stu-id="1afe6-104">Depreciation of fixed assets with reduction entry posted</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1afe6-105">このタスクを使用して、圧縮記帳で固定資産の減価償却を実行する方法を把握します。</span><span class="sxs-lookup"><span data-stu-id="1afe6-105">Use this task to learn how to run fixed asset depreciation with reduction entries</span></span>



<span data-ttu-id="1afe6-106">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1afe6-106">In order to complete this task, the Fixed Asset configuration key must be selected.</span></span>



<span data-ttu-id="1afe6-107">このタスクは、デモデータ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="1afe6-107">This task was created using the JPMF demo data company.</span></span>

1. <span data-ttu-id="1afe6-108">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1afe6-108">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="1afe6-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1afe6-109">Click New.</span></span>
3. <span data-ttu-id="1afe6-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1afe6-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1afe6-111">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1afe6-111">Click Lines.</span></span>
5. <span data-ttu-id="1afe6-112">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1afe6-112">Click Proposals.</span></span>
6. <span data-ttu-id="1afe6-113">[償却提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1afe6-113">Click Depreciation proposal.</span></span>
7. <span data-ttu-id="1afe6-114">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1afe6-114">In the To date field, enter a date.</span></span>
8. <span data-ttu-id="1afe6-115">圧縮記帳割当が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1afe6-115">Verify that Reduction entry allocation is selected.</span></span>
9. <span data-ttu-id="1afe6-116">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1afe6-116">Click Filter.</span></span>
    * <span data-ttu-id="1afe6-117">オプション: フィルターを使用すると、必要な固定資産のみ処理されるので、より速く処理できます。</span><span class="sxs-lookup"><span data-stu-id="1afe6-117">Optional: Using the filter can help make the process faster by processing only the necessary fixed assets.</span></span>  
10. <span data-ttu-id="1afe6-118">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1afe6-118">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="1afe6-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1afe6-119">Click OK.</span></span>
12. <span data-ttu-id="1afe6-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1afe6-120">Click OK.</span></span>
    * <span data-ttu-id="1afe6-121">圧縮記帳に属する減価償却は、ドキュメント タイプにより下線が引かれた固定資産の減価償却とは別になります。</span><span class="sxs-lookup"><span data-stu-id="1afe6-121">The depreciation that is attributed to the reduction entry is separated from that of the underline fixed asset by Document type.</span></span>  
13. <span data-ttu-id="1afe6-122">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1afe6-122">Click Post.</span></span>


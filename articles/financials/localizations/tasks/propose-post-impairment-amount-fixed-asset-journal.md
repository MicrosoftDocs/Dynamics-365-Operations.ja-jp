---
title: 固定資産仕訳帳を使用した減損損失の提案と転記
description: この手順を用いて、固定資産仕訳帳を使用して減損金額を提示および転記する方法を把握します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b7353519782e62d57d66d9ba36a2f6a2b33a7c9c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371038"
---
# <a name="propose-and-post-the-impairment-amount-by-using-fixed-asset-journal"></a><span data-ttu-id="372d4-103">固定資産仕訳帳を使用した減損損失の提案と転記</span><span class="sxs-lookup"><span data-stu-id="372d4-103">Propose and post the impairment amount by using fixed asset journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="372d4-104">この手順を用いて、固定資産仕訳帳を使用して減損金額を提示および転記する方法を把握します。</span><span class="sxs-lookup"><span data-stu-id="372d4-104">Use this procedure to learn how to propose and post the impairment amount by using a fixed asset journal.</span></span>



<span data-ttu-id="372d4-105">このタスクを実行する前に、減損テスト結果がすでに作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="372d4-105">Be sure an impairment test result is already created prior to running this task.</span></span>



<span data-ttu-id="372d4-106">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="372d4-106">This procedure was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="372d4-107">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="372d4-107">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="372d4-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="372d4-108">Click New.</span></span>
3. <span data-ttu-id="372d4-109">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="372d4-109">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="372d4-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="372d4-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="372d4-111">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="372d4-111">Click Lines.</span></span>
6. <span data-ttu-id="372d4-112">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="372d4-112">Click Proposals.</span></span>
7. <span data-ttu-id="372d4-113">[減損提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="372d4-113">Click Impairment proposal.</span></span>
8. <span data-ttu-id="372d4-114">[減損テスト ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="372d4-114">In the Impairment test ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="372d4-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="372d4-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="372d4-116">この例では、「JPMF-000004」を選択します。</span><span class="sxs-lookup"><span data-stu-id="372d4-116">For this example select 'JPMF-000004.'</span></span>  
10. <span data-ttu-id="372d4-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="372d4-117">Click OK.</span></span>
    * <span data-ttu-id="372d4-118">減損テストの 2 つの固定資産は、次の情報と共に提案されます: 固定資産番号、貸方の減損金額、および減損テストの日付として日付。</span><span class="sxs-lookup"><span data-stu-id="372d4-118">Two fixed assets in the Impairment test were proposed with the following information: Fixed asset number, the impairment amount on credit, and the date as the date in impairment test.</span></span>  
11. <span data-ttu-id="372d4-119">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="372d4-119">Click Post.</span></span>


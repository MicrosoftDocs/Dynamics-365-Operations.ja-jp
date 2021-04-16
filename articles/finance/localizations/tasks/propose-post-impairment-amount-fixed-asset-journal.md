---
title: 固定資産仕訳帳を使用した減損損失の提案と転記
description: この手順を用いて、固定資産仕訳帳を使用して減損金額を提示および転記する方法を把握します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00a0e62077cde8f735a67b090b76c11540e1b1cd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830401"
---
# <a name="propose-and-post-the-impairment-amount-by-using-fixed-asset-journal"></a><span data-ttu-id="95f75-103">固定資産仕訳帳を使用した減損損失の提案と転記</span><span class="sxs-lookup"><span data-stu-id="95f75-103">Propose and post the impairment amount by using fixed asset journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95f75-104">この手順を用いて、固定資産仕訳帳を使用して減損金額を提示および転記する方法を把握します。</span><span class="sxs-lookup"><span data-stu-id="95f75-104">Use this procedure to learn how to propose and post the impairment amount by using a fixed asset journal.</span></span>



<span data-ttu-id="95f75-105">このタスクを実行する前に、減損テスト結果がすでに作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="95f75-105">Be sure an impairment test result is already created prior to running this task.</span></span>



<span data-ttu-id="95f75-106">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="95f75-106">This procedure was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="95f75-107">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="95f75-107">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="95f75-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95f75-108">Click New.</span></span>
3. <span data-ttu-id="95f75-109">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="95f75-109">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="95f75-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="95f75-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="95f75-111">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95f75-111">Click Lines.</span></span>
6. <span data-ttu-id="95f75-112">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95f75-112">Click Proposals.</span></span>
7. <span data-ttu-id="95f75-113">[減損提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95f75-113">Click Impairment proposal.</span></span>
8. <span data-ttu-id="95f75-114">[減損テスト ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="95f75-114">In the Impairment test ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="95f75-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="95f75-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="95f75-116">この例では、「JPMF-000004」を選択します。</span><span class="sxs-lookup"><span data-stu-id="95f75-116">For this example select 'JPMF-000004.'</span></span>  
10. <span data-ttu-id="95f75-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95f75-117">Click OK.</span></span>
    * <span data-ttu-id="95f75-118">減損テストの 2 つの固定資産は、次の情報と共に提案されます: 固定資産番号、貸方の減損金額、および減損テストの日付として日付。</span><span class="sxs-lookup"><span data-stu-id="95f75-118">Two fixed assets in the Impairment test were proposed with the following information: Fixed asset number, the impairment amount on credit, and the date as the date in impairment test.</span></span>  
11. <span data-ttu-id="95f75-119">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95f75-119">Click Post.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: 裏書済受取手形の決済
description: このタスクは、裏書きされた為替手形の決済について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillOfExchangeEndorseListPage, VendOpenTrans, CustBillOfExchangeEndorseSettle
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8f33545069084967f7ac69b89e682532739e22d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183725"
---
# <a name="settle-an-endorsed-bill-of-exchange"></a><span data-ttu-id="e6d97-103">裏書済受取手形の決済</span><span class="sxs-lookup"><span data-stu-id="e6d97-103">Settle an endorsed bill of exchange</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e6d97-104">このタスクは、裏書きされた為替手形の決済について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6d97-104">This task walks you through settling an endorsed bill of exchange.</span></span>



<span data-ttu-id="e6d97-105">このタスクを完了するには、裏書きされた為替手形および未処理の仕入先トランザクションが必要です。</span><span class="sxs-lookup"><span data-stu-id="e6d97-105">Before you can complete this task, you must have an endorsed bill of exchange and an open vendor transaction.</span></span> 



<span data-ttu-id="e6d97-106">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="e6d97-106">This task was created using the demo data company JPMF.</span></span>


## <a name="settle-a-vendor-transaction-that-was-generated-by-an-endorsement"></a><span data-ttu-id="e6d97-107">裏書によって生成された仕入先トランザクションの決済</span><span class="sxs-lookup"><span data-stu-id="e6d97-107">Settle a vendor transaction that was generated by an endorsement</span></span>
1. <span data-ttu-id="e6d97-108">[買掛金勘定] > [支払] > [裏書為替手形] に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6d97-108">Go to Accounts payable > Payments > Endorse bills of exchange.</span></span>
2. <span data-ttu-id="e6d97-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d97-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e6d97-110">ステータスが「裏書済」の為替手形を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d97-110">Select a bill of exchange that has a status of "Endorsed".</span></span>  
3. <span data-ttu-id="e6d97-111">[トランザクションの決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6d97-111">Click Settle transactions.</span></span>
4. <span data-ttu-id="e6d97-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d97-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e6d97-113">為替手形の裏書によって生成されたトランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d97-113">Select the transaction that was generated by the endorsement of the bill of exchange.</span></span>  
5. <span data-ttu-id="e6d97-114">[マーク] のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e6d97-114">Select the Mark check box.</span></span>
6. <span data-ttu-id="e6d97-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d97-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e6d97-116">対応する仕入先トランザクションで決済に使用するものを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d97-116">Select the corresponding vendor transaction to settle with.</span></span>  
7. <span data-ttu-id="e6d97-117">[マーク] のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e6d97-117">Select the Mark check box.</span></span>
8. <span data-ttu-id="e6d97-118">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6d97-118">Click Post.</span></span>

## <a name="settle-an-endorsed-bill-of-exchange"></a><span data-ttu-id="e6d97-119">裏書済受取手形の決済</span><span class="sxs-lookup"><span data-stu-id="e6d97-119">Settle an endorsed bill of exchange</span></span>
1. <span data-ttu-id="e6d97-120">[裏書済為替手形の決済] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e6d97-120">Click Settle endorsed bill of exchange to open the drop dialog.</span></span>
2. <span data-ttu-id="e6d97-121">[裏書済為替手形の決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6d97-121">Click Settle endorsed bill of exchange.</span></span>
    * <span data-ttu-id="e6d97-122">決済日は、必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="e6d97-122">You can change the settlement date if necessary.</span></span>  
    * <span data-ttu-id="e6d97-123">ステータスが「裏書決済済」に更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e6d97-123">Verify that the status has been updated to be "Endorsement settled".</span></span>  

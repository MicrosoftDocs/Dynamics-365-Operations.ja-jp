---
title: 裏書済受取手形の取消
description: このタスクは、裏書きされた為替手形の取消について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseReverse, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73da319a08a5a64dd4a7f21dab865cb08e5d9e65
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174653"
---
# <a name="reverse-an-endorsed-bill-of-exchange"></a><span data-ttu-id="a8dcd-103">裏書済受取手形の取消</span><span class="sxs-lookup"><span data-stu-id="a8dcd-103">Reverse an endorsed bill of exchange</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8dcd-104">このタスクは、裏書きされた為替手形の取消について説明します。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-104">This task walks you through reversing an endorsed bill of exchange.</span></span>



<span data-ttu-id="a8dcd-105">このタスクを完了するには、少なくとも 1 つの裏書きされた為替手形が必要です。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-105">Before you can complete this task, you must have at least one endorsed bill of exchange.</span></span> 

<span data-ttu-id="a8dcd-106">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-106">This task was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="a8dcd-107">[買掛金勘定] > [支払] > [裏書為替手形] に移動します。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-107">Go to Accounts payable > Payments > Endorse bills of exchange.</span></span>
2. <span data-ttu-id="a8dcd-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a8dcd-109">ステータスが「裏書済」の為替手形を選択します。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-109">Select a bill of exchange that has a status of "Endorsed".</span></span>  <span data-ttu-id="a8dcd-110">仕入先トランザクションが既に決済されている場合、為替手形を引き当てるられないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-110">Note that you cannot reserve a bill of exchange if the vendor transaction is already settled.</span></span> <span data-ttu-id="a8dcd-111">裏書を引き当てる前に決済を元に戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-111">You must undo the settlement before reserving the endorsement.</span></span>  
3. <span data-ttu-id="a8dcd-112">[裏書の取消] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-112">Click Reverse endorsement to open the drop dialog.</span></span>
4. <span data-ttu-id="a8dcd-113">[裏書の取消] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-113">Click Reverse endorsement.</span></span>
    * <span data-ttu-id="a8dcd-114">引当日は、必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-114">You can change the reverse date if necessary.</span></span>  
5. <span data-ttu-id="a8dcd-115">[照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-115">Click Inquiry.</span></span>
6. <span data-ttu-id="a8dcd-116">[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-116">Click Voucher.</span></span>
    * <span data-ttu-id="a8dcd-117">会計伝票が取消に対して生成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a8dcd-117">Verify that that an accounting voucher was generated for the reversal.</span></span>  

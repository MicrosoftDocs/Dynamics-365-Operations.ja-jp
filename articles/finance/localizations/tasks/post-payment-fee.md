---
title: 支払手数料の生成および転記
description: このタスクでは、日本の支払手数料を生成および転記する方法について説明します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, VendTableLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f69694b49304c0bc53b992db2bd7ee2505280d5d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820497"
---
# <a name="generate-and-post-payment-fee"></a><span data-ttu-id="7a8f3-103">支払手数料の生成および転記</span><span class="sxs-lookup"><span data-stu-id="7a8f3-103">Generate and post payment fee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a8f3-104">このタスクでは、日本の支払手数料を生成および転記する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-104">This task walks you through generating and posting a payment fee for Japan.</span></span>



<span data-ttu-id="7a8f3-105">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-105">This task was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="7a8f3-106">[買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-106">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="7a8f3-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-107">Click New.</span></span>
3. <span data-ttu-id="7a8f3-108">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7a8f3-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7a8f3-110">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-110">Click Lines.</span></span>
6. <span data-ttu-id="7a8f3-111">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-111">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="7a8f3-112">たとえば、「JPMF-000001」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-112">For example: enter 'JPMF-000001'</span></span>  
7. <span data-ttu-id="7a8f3-113">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-113">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="7a8f3-114">例: 「200000」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-114">For example: enter '200000'</span></span>  
8. <span data-ttu-id="7a8f3-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-115">Click Save.</span></span>
9. <span data-ttu-id="7a8f3-116">[支払手数料] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-116">Click the Payment fee tab.</span></span>
    * <span data-ttu-id="7a8f3-117">支払手数料が正しく生成されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-117">Verify that the payment fee is generated correctly.</span></span>  
    * <span data-ttu-id="7a8f3-118">支払金額、サード パーティ銀行口座、または銀行口座を変更して、これらのフィールドの組み合わせを変えると支払手数料の金額が変化することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-118">You can also try to change the amount of payment, third party bank account, or the bank account to see that different combinations of these fields will result in a different payment fee amount.</span></span>  
10. <span data-ttu-id="7a8f3-119">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7a8f3-119">Click Post.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
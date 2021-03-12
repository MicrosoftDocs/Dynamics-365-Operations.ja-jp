---
title: 支払手数料の生成および転記
description: このタスクでは、日本の支払手数料を生成および転記する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, VendTableLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12d662c55b99a3c1f8ec6c9b39d5e1f5aaad9d25
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968282"
---
# <a name="generate-and-post-payment-fee"></a><span data-ttu-id="3f6fd-103">支払手数料の生成および転記</span><span class="sxs-lookup"><span data-stu-id="3f6fd-103">Generate and post payment fee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f6fd-104">このタスクでは、日本の支払手数料を生成および転記する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-104">This task walks you through generating and posting a payment fee for Japan.</span></span>



<span data-ttu-id="3f6fd-105">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-105">This task was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="3f6fd-106">[買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-106">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="3f6fd-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-107">Click New.</span></span>
3. <span data-ttu-id="3f6fd-108">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3f6fd-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3f6fd-110">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-110">Click Lines.</span></span>
6. <span data-ttu-id="3f6fd-111">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-111">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="3f6fd-112">たとえば、「JPMF-000001」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-112">For example: enter 'JPMF-000001'</span></span>  
7. <span data-ttu-id="3f6fd-113">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-113">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="3f6fd-114">例: 「200000」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-114">For example: enter '200000'</span></span>  
8. <span data-ttu-id="3f6fd-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-115">Click Save.</span></span>
9. <span data-ttu-id="3f6fd-116">[支払手数料] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-116">Click the Payment fee tab.</span></span>
    * <span data-ttu-id="3f6fd-117">支払手数料が正しく生成されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-117">Verify that the payment fee is generated correctly.</span></span>  
    * <span data-ttu-id="3f6fd-118">支払金額、サード パーティ銀行口座、または銀行口座を変更して、これらのフィールドの組み合わせを変えると支払手数料の金額が変化することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-118">You can also try to change the amount of payment, third party bank account, or the bank account to see that different combinations of these fields will result in a different payment fee amount.</span></span>  
10. <span data-ttu-id="3f6fd-119">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f6fd-119">Click Post.</span></span>


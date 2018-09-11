--- 
title: "仕入先の設定と ISO20022 口座振替用の仕入先銀行口座の設定"
description: "この手順では、ISO20022 口座振替またはその他の仕入先支払ファイルの生成に必要な仕入先および仕入先固有の銀行口座情報を設定する方法を示します。"
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: ea1f0c6c4b3530eeae529d0932f8fd408a09cc54
ms.contentlocale: ja-jp
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="d60f6-103">仕入先の設定と ISO20022 口座振替用の仕入先銀行口座の設定</span><span class="sxs-lookup"><span data-stu-id="d60f6-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d60f6-104">この手順では、ISO20022 口座振替またはその他の仕入先支払ファイルの生成に必要な仕入先および仕入先固有の銀行口座情報を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d60f6-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="d60f6-105">この手順の作成に使用するデモ データの会社は DEMF です。</span><span class="sxs-lookup"><span data-stu-id="d60f6-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="d60f6-106">これは、5 つのうち 4 つ目の手順で、電子レポートのコンフィギュレーションを使用する仕入先支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="d60f6-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="d60f6-107">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="d60f6-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="d60f6-108">銀行詳細を設定します。</span><span class="sxs-lookup"><span data-stu-id="d60f6-108">Set up bank details</span></span>
1. <span data-ttu-id="d60f6-109">[買掛金勘定] > [仕入先] > [すべての仕入先] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d60f6-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="d60f6-110">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="d60f6-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d60f6-111">たとえば、[仕入先口座] フィールドに値「DE-001」でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="d60f6-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="d60f6-112">「DE-001」をクリックして、仕入先の詳細を開きます。</span><span class="sxs-lookup"><span data-stu-id="d60f6-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="d60f6-113">[アクション] ウィンドウで、[仕入先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d60f6-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="d60f6-114">[銀行口座] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d60f6-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="d60f6-115">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d60f6-115">Click Edit.</span></span>
    * <span data-ttu-id="d60f6-116">銀行口座が存在しない場合は、新しい口座を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d60f6-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="d60f6-117">[SWIFT コード] フィールドで、「COBADEFFXXX」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d60f6-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="d60f6-118">[IBAN] フィールドに「DE36200400000628808808」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d60f6-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="d60f6-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d60f6-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="d60f6-120">仕入先に対する支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="d60f6-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="d60f6-121">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d60f6-121">Click Edit.</span></span>
2. <span data-ttu-id="d60f6-122">[支払] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="d60f6-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="d60f6-123">[支払方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d60f6-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d60f6-124">一覧で、選択された行「SEPA CT」のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d60f6-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="d60f6-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d60f6-125">Click Save.</span></span>



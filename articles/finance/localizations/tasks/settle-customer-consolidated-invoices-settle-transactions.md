---
title: 決済トランザクションを使用した顧客月次締め請求書の決済
description: このトピックでは、月次締め請求書に対して作成および決済される支払に関する情報を提供します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustConsInvoice_JP, CustTable, CustOpenTrans
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc0657ea76bdf955d64922079e5677d7aa198a38
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988004"
---
# <a name="settle-customer-consolidated-invoices-by-using-settle-transactions"></a><span data-ttu-id="f0f4c-103">決済トランザクションを使用した顧客月次締め請求書の決済</span><span class="sxs-lookup"><span data-stu-id="f0f4c-103">Settle customer consolidated invoices by using settle transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0f4c-104">日本では、支払は月次締め請求書に対して行われ決済されます。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-104">In Japan, payments are made and settled against consolidated invoice.</span></span>

<span data-ttu-id="f0f4c-105">この手順では、決済トランザクションを使用した月次締め請求書の決済について説明します。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-105">This procedure walks you through settling a consolidated invoice using settle transactions.</span></span>

<span data-ttu-id="f0f4c-106">この手順を実行する前に、月次締め請求書が作成され確定済であること、および支払いが転記されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-106">Before you begin this procedure, make sure that a consolidated invoice is created and confirmed, and a payment has been posted.</span></span> 

<span data-ttu-id="f0f4c-107">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-107">This procedure was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="f0f4c-108">[売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-108">Go to Accounts receivable > Periodic tasks > Consolidated invoice.</span></span>
    * <span data-ttu-id="f0f4c-109">決済する月次締め請求書のステータスが「確定済」であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-109">Confirm the consolidated invoice you want to settle is at status of Confirmed.</span></span>  
    * <span data-ttu-id="f0f4c-110">月次締め請求書を作成および確認します。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-110">Create and confirm a consolidated invoice.</span></span>  
2. <span data-ttu-id="f0f4c-111">[売掛金勘定] > [顧客] > [すべての顧客] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-111">Go to Accounts receivable > Customers > All customers.</span></span>
3. <span data-ttu-id="f0f4c-112">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f0f4c-113">月次締め請求書を決済する顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-113">Select the customer that you want to settle the consolidated invoice for.</span></span>  
4. <span data-ttu-id="f0f4c-114">[アクション] ウィンドウで、[回収] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-114">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="f0f4c-115">[トランザクションの決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-115">Click Settle transactions.</span></span>
    * <span data-ttu-id="f0f4c-116">決済する月次締め請求書の確定には、[締め ID] フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-116">Use Consolidation ID field to confirm the consolidated invoice that you want to settle.</span></span>  
6. <span data-ttu-id="f0f4c-117">決済する明細行の検索と、その明細行のチェック ボックスの選択</span><span class="sxs-lookup"><span data-stu-id="f0f4c-117">Find a line to settle and select the check box for that line</span></span>
    * <span data-ttu-id="f0f4c-118">この手順をタスク ガイドとして実行している場合は、レコードを選択するためにタスク ガイドのロックを解除しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-118">If you're running this procedure as a task guide, you might need to unlock the task guide before you can select the record.</span></span>  
7. <span data-ttu-id="f0f4c-119">決済する別の明細行の検索と、その明細行のチェック ボックスの選択</span><span class="sxs-lookup"><span data-stu-id="f0f4c-119">Find another line to settle and click the check box for that line</span></span>
    * <span data-ttu-id="f0f4c-120">この手順をタスク ガイドとして実行している場合は、レコードを選択するためにタスク ガイドのロックを解除しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-120">If you're running this procedure as a task guide, you might need to unlock the task guide before you can select the record.</span></span>  
8. <span data-ttu-id="f0f4c-121">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-121">Click Post.</span></span>
9. <span data-ttu-id="f0f4c-122">[売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-122">Go to Accounts receivable > Periodic tasks > Consolidated invoice.</span></span>
    * <span data-ttu-id="f0f4c-123">[月次締め請求書] のステータスが [決済済] に更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f0f4c-123">Confirm that the status of the Consolidated invoice is updated to Settled.</span></span>  


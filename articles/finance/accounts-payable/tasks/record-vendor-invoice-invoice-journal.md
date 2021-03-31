---
title: 請求仕訳帳の仕入先請求書の記録
description: このタスク ガイドでは、発注書に関連付けられていない仕入先請求書を記録する方法について説明します。
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a60a5959046ca9e953bac80aaeb382d07a267643
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227139"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="1966f-103">請求仕訳帳の仕入先請求書の記録</span><span class="sxs-lookup"><span data-stu-id="1966f-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1966f-104">このタスク ガイドでは、発注書に関連付けられていない仕入先請求書を記録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1966f-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="1966f-105">このタイプの請求書の例には、消耗品やサービスの経費があります。</span><span class="sxs-lookup"><span data-stu-id="1966f-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="1966f-106">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="1966f-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="1966f-107">**ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > ワークスペース > 仕入先請求書入力** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1966f-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="1966f-108">**アクション ペイン** で、**新しい請求仕訳帳** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1966f-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="1966f-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1966f-109">Click **New**.</span></span>
4. <span data-ttu-id="1966f-110">**名前** フィールドで、仕訳帳名を入力するか、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="1966f-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="1966f-111">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1966f-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="1966f-112">**アクション ウィンドウ** で、**明細行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1966f-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="1966f-113">**日付** フィールドで、総勘定元帳を更新する転記日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1966f-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="1966f-114">**勘定** フィールドで、**仕入先** を指定します。</span><span class="sxs-lookup"><span data-stu-id="1966f-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="1966f-115">**請求書** フィールドに、請求書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="1966f-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="1966f-116">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1966f-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="1966f-117">**貸方** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1966f-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="1966f-118">**相手勘定** フィールドで、勘定番号を入力するか、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="1966f-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="1966f-119">**消費税グループ** は、仕入先勘定の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="1966f-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="1966f-120">**品目消費税グループ** は、**相手勘定** フィールドで指定された主勘定の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="1966f-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="1966f-121">**期日** は支払条件に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="1966f-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="1966f-122">**現金割引** は仕入先口座から既定値が取得されます。</span><span class="sxs-lookup"><span data-stu-id="1966f-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="1966f-123">仕入先請求書の仕訳帳のワークフローを有効にした場合は、**ワークフロー > 送信** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="1966f-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="1966f-124">送信が承認されると、元帳転記が "保留中" または "決算済" である期間内にトランザクションの転記日付が来る場合は、次の未処理期間の最初の日に日付が先行します。</span><span class="sxs-lookup"><span data-stu-id="1966f-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="1966f-125">**転記** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1966f-125">Click **Post**.</span></span>
13. <span data-ttu-id="1966f-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1966f-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
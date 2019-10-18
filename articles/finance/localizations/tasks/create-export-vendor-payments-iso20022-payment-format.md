---
title: ISO20022 支払形式を使用した仕入先支払の作成とエクスポート
description: この手順では、仕入先支払仕訳帳で支払明細行を作成する方法、および ISO2022 口座振替の例を使用して仕入先支払ファイルを生成する方法を示します。
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b70ad94014587ba8e55735192dbe0ab2e4adf4ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185822"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="c22bc-103">ISO20022 支払形式を使用した仕入先支払の作成とエクスポート</span><span class="sxs-lookup"><span data-stu-id="c22bc-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c22bc-104">このトピックでは、仕入先支払仕訳帳で支払明細行を作成する方法、および ISO2022 口座振替の例を使用して仕入先支払ファイルを生成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="c22bc-105">これは、5 つのうち 5 つ目の手順で、電子レポートのコンフィギュレーションを使用する仕入先支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="c22bc-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="c22bc-106">この例を完了するのにデモ データ DEMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="c22bc-107">例</span><span class="sxs-lookup"><span data-stu-id="c22bc-107">Example</span></span>

1.  <span data-ttu-id="c22bc-108">**買掛金勘定 > 支払 > 支払仕訳帳**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.  <span data-ttu-id="c22bc-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c22bc-109">Click **New**.</span></span>
3.  <span data-ttu-id="c22bc-110">**名前**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-110">In the **Name** field, enter or select a value.</span></span>
4.  <span data-ttu-id="c22bc-111">**明細行 > 支払提案 > 支払提案の作成**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="c22bc-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.  <span data-ttu-id="c22bc-112">**対象に含めるレコード** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-112">Expand the **Records to include** section.</span></span>
6.  <span data-ttu-id="c22bc-113">**フィルター**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c22bc-113">Click **Filter**.</span></span>
7.  <span data-ttu-id="c22bc-114">一覧で、**仕入先テーブル**の行および**仕入先フィールド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.  <span data-ttu-id="c22bc-115">**基準**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="c22bc-116">支払う仕入先トランザクションを選択するためのあらゆる基準を適用できます。この例では、DE-001 を仕入先として使用します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12. <span data-ttu-id="c22bc-117">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c22bc-117">Click **OK**.</span></span>
13. <span data-ttu-id="c22bc-118">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c22bc-118">Click **OK**.</span></span>
14. <span data-ttu-id="c22bc-119">**支払の作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c22bc-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="c22bc-120">ISO20022 支払ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-120">Generate an ISO20022 payment file.</span></span>
    1.  <span data-ttu-id="c22bc-121">**支払の生成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c22bc-121">Click **Generate payments**.</span></span>
    2.  <span data-ttu-id="c22bc-122">**支払方法**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.  <span data-ttu-id="c22bc-123">**ファイル名**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="c22bc-124">この例では、EUR 支払が原因で、生成されたファイルは SEPAに準拠します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="c22bc-125">他の通貨での支払いの生成には、ISO20022 口座振替や他の仕入先の支払形式も使用できます。</span><span class="sxs-lookup"><span data-stu-id="c22bc-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.  <span data-ttu-id="c22bc-126">**銀行口座**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c22bc-126">In the **Bank account** field, enter or select a value.</span></span>


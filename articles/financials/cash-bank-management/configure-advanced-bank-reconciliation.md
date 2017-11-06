---
title: "詳細な口座調整の設定プロセス"
description: "詳細な口座調整では、電子口座取引明細書をインポートし、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition での銀行トランザクションに合わせて自動的に調整することができます。  この資料では、調整のプロセスの設定について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: aec219f545e880407b9a7d62b2dda4a607ac6bdd
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="advanced-bank-reconciliation-setup-process"></a><span data-ttu-id="04e9a-104">詳細な口座調整の設定プロセス</span><span class="sxs-lookup"><span data-stu-id="04e9a-104">Advanced bank reconciliation setup process</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="04e9a-105">詳細な口座調整では、電子口座取引明細書をインポートし、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition での銀行トランザクションに合わせて自動的に調整することができます。</span><span class="sxs-lookup"><span data-stu-id="04e9a-105">Advanced bank reconciliation allows you to import electronic bank statements and automatically reconcile with bank transactions in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>  <span data-ttu-id="04e9a-106">この資料では、調整のプロセスの設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="04e9a-106">This article will explain the set up processes for reconciliation.</span></span>  

<span data-ttu-id="04e9a-107">詳細な口座調整機能を使用する前に設定する必要のあるいくつかの要素があります。</span><span class="sxs-lookup"><span data-stu-id="04e9a-107">There are a number of pieces that must be set up before using the advanced bank reconciliation functionality.</span></span> <span data-ttu-id="04e9a-108">口座取引明細書のインポートの設定の情報については、「[口座取引明細書のインポート プロセスの設定](set-up-advanced-bank-reconciliation-import-process.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04e9a-108">For more information about setting up bank statement import, see [Set up the bank statement import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>  <span data-ttu-id="04e9a-109">調整プロセスの設定の要件は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="04e9a-109">Requirements for set up of the reconciliation process are detailed below.</span></span>

## <a name="transaction-codes"></a><span data-ttu-id="04e9a-110">トランザクション コード</span><span class="sxs-lookup"><span data-stu-id="04e9a-110">Transaction codes</span></span>
<span data-ttu-id="04e9a-111">トランザクション コードは、銀行調整の照合ルールの一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="04e9a-111">Transaction codes can be used as part of the bank reconciliation matching rules.</span></span>  <span data-ttu-id="04e9a-112">トランザクション コードは Finance and Operations と口座取引明細書間の同じタイプのトランザクションのみの照合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="04e9a-112">Transaction codes will help to match only the same types of transactions between Finance and Operations and your bank statement.</span></span>  <span data-ttu-id="04e9a-113">このタイプの照合を行うには、まず Finance and Operations の銀行トランザクションに使用するトランザクション タイプを定義し、銀行で使用する明細書の取引コードにそれらのタイプをマップします。</span><span class="sxs-lookup"><span data-stu-id="04e9a-113">In order to do this type of matching, you must first define transaction types used for bank transactions from Finance and Operations, then map those types to statement transaction codes used by your bank.</span></span>  <span data-ttu-id="04e9a-114">Finance and Operations 銀行トランザクションのトランザクション タイプは、[**銀行トランザクション タイプ**] ページで定義されます。</span><span class="sxs-lookup"><span data-stu-id="04e9a-114">Transaction types for Finance and Operations bank transactions are defined on the **Bank transaction type** page.</span></span>  <span data-ttu-id="04e9a-115">またこれによって、トランザクション タイプに関連付けられた転記に使用する主勘定を定義します。</span><span class="sxs-lookup"><span data-stu-id="04e9a-115">This is also where you define the main account to be used for postings associated with that transaction type.</span></span> 

<span data-ttu-id="04e9a-116">Finance and Operations 銀行トランザクション タイプを定義した後、これらを電子口座取引明細書で使用するトランザクション コードにマップします。</span><span class="sxs-lookup"><span data-stu-id="04e9a-116">Once your Finance and Operations bank transaction codes are defined, you then map those to the transaction codes used in your electronic bank statements.</span></span>  <span data-ttu-id="04e9a-117">このマッピング プロセスは、[**取引コード マッピング**] ページを使用を使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="04e9a-117">This mapping process is done using the **Transaction code mapping** page.</span></span>  <span data-ttu-id="04e9a-118">トランザクション コードのマッピングは、銀行ごと個別に完了します。</span><span class="sxs-lookup"><span data-stu-id="04e9a-118">Transaction code mapping is completed separately for each bank account.</span></span>

## <a name="matching-rules-and-matching-rule-sets"></a><span data-ttu-id="04e9a-119">照合ルールおよび照合ルール セット</span><span class="sxs-lookup"><span data-stu-id="04e9a-119">Matching rules and matching rule sets</span></span>
<span data-ttu-id="04e9a-120">照合ルールによって、Finance and Operations 銀行トランザクションと口座取引明細書トランザクションとの間の自動調整の基準を定義できます。</span><span class="sxs-lookup"><span data-stu-id="04e9a-120">Matching rules allow you to define criteria for automatic reconciliation between Finance and Operations bank transactions and bank statement transactions.</span></span>  <span data-ttu-id="04e9a-121">照合ルールの設定は、[**調整照合ルール**] ページで行います。</span><span class="sxs-lookup"><span data-stu-id="04e9a-121">Set up of matching rules is done on **Reconciliation matching rules** page.</span></span>  <span data-ttu-id="04e9a-122">詳細については、「[口座調整照合ルールの設定](set-up-bank-reconciliation-matching-rules.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04e9a-122">For more information, see [Set up bank reconciliation matching rules](set-up-bank-reconciliation-matching-rules.md).</span></span> 

<span data-ttu-id="04e9a-123">照合ルール セットを使用して、口座調整プロセス中に順番に実行する照合ルールのグループを定義します。</span><span class="sxs-lookup"><span data-stu-id="04e9a-123">Matching rule sets are used to define a group of matching rules that are run in sequence during the bank reconciliation process.</span></span>  <span data-ttu-id="04e9a-124">照合ルール セットは、[**調整照合ルール セット**] ページで構成されています。</span><span class="sxs-lookup"><span data-stu-id="04e9a-124">Matching rule sets are configured on the **Reconciliation matching rule sets** page.</span></span>

## <a name="cash-and-bank-management-parameters"></a><span data-ttu-id="04e9a-125">現金および銀行管理パラメーター</span><span class="sxs-lookup"><span data-stu-id="04e9a-125">Cash and bank management parameters</span></span>
<span data-ttu-id="04e9a-126">[**現金および銀行管理パラメーター**] ページに詳細な口座調整プロセスに固有のいくつものパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="04e9a-126">There are a number of parameters specific to the advanced bank reconciliation process on the **Cash and bank management parameters** page.</span></span>  <span data-ttu-id="04e9a-127">[**借方/貸方欄の明細行の金額の表示**] は、[**口座取引明細書**] ページの金額の表示を変更します。</span><span class="sxs-lookup"><span data-stu-id="04e9a-127">The **Show statement line amount in debit/credit** changes the view of amounts on the **Bank statement** page.</span></span>  <span data-ttu-id="04e9a-128">このオプションを選択した場合、口座取引明細書トランザクションの金額が、借方列と貸方列に別々に表示されます。</span><span class="sxs-lookup"><span data-stu-id="04e9a-128">If this option is selected, the bank statement transaction amounts will be shown in separate debit and credit columns.</span></span>  <span data-ttu-id="04e9a-129">このオプションを選択しなかった場合、口座取引明細書トランザクションの金額が、単一の金額列に適切な記号で表示されます。</span><span class="sxs-lookup"><span data-stu-id="04e9a-129">If not selected, the bank statement transaction amounts will be shown in a single amount column with the appropriate sign.</span></span> 

<span data-ttu-id="04e9a-130">[パラメーター] ページで設定された検証オプションは、照合ルールで設定された選択を上書きします。</span><span class="sxs-lookup"><span data-stu-id="04e9a-130">The validation options set on the parameters page override the selections set on matching rules.</span></span>  <span data-ttu-id="04e9a-131">たとえば、[パラメーター] ページで設定された日付の違いを超える明細書を手動あるいは自動で照合することはできません。</span><span class="sxs-lookup"><span data-stu-id="04e9a-131">For example, you cannot manually or automatically match documents beyond the date difference set on the parameters page.</span></span>  <span data-ttu-id="04e9a-132">また、[**トランザクション タイプ マッピングの検証**] へのオプションを選択した場合、トランザクション タイプは、トランザクションが手動あるいは自動で照合されるために Finance and Operations 銀行トランザクションと口座取引明細書トランザクション間でマップされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="04e9a-132">Also, if the option to **Validate transaction type mapping** is selected, the transaction types must be mapped between the Finance and Operations bank transaction and bank statement transaction in order for the transactions to be manually or automatically matched.</span></span> 

<span data-ttu-id="04e9a-133">[**現金および銀行管理パラメーター**] ページで必要な番号順序を構成する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="04e9a-133">You also must configure the necessary number sequences on the **Cash and bank management parameters** page.</span></span>  <span data-ttu-id="04e9a-134">[**番号順序**] タブで、[**ID、明細書 ID、調整 ID、および口座調整**] 参照をダウンロードするための番号順序コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="04e9a-134">On the **Number sequences** tab, set number sequence codes for the Download **ID, Statement ID, Reconcile ID, and Bank reconciliation** references.</span></span>

## <a name="bank-account-reconciliation-options"></a><span data-ttu-id="04e9a-135">銀行口座調整のオプション</span><span class="sxs-lookup"><span data-stu-id="04e9a-135">Bank account reconciliation options</span></span>
<span data-ttu-id="04e9a-136">まず、銀行口座の詳細な口座調整を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="04e9a-136">You must first enable Advanced bank reconciliation for the bank account.</span></span>  <span data-ttu-id="04e9a-137">詳細な口座調整機能が有効になった後、いくつかの追加オプションが、[**銀行口座**] ページで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="04e9a-137">A number of additional options are available on the **Bank account** page once the Advanced bank reconciliation functionality is enabled.</span></span> 

<span data-ttu-id="04e9a-138">[**電子支払の確認としての口座取引明細の使用**] 機能は、口座調整機能を電子支払ステータスと機能的に統合します。</span><span class="sxs-lookup"><span data-stu-id="04e9a-138">**Use bank statements as confirmation of electronic payment** functionality integrates the bank reconciliation functionality with electronic payment statuses.</span></span>  <span data-ttu-id="04e9a-139">これが有効になると、電子支払ステータスが [**送信**] に設定されているため、銀行ドキュメントが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="04e9a-139">When this is enabled, a bank document will automatically be created for the electronic payment status is set to **Sent**.</span></span>  <span data-ttu-id="04e9a-140">さらに、支払が照合、調整、転記された後、電子支払ステータスは、[**送信**] から [**受信**] に更新されます。</span><span class="sxs-lookup"><span data-stu-id="04e9a-140">In addition, the status of an electronic payment will be updated from **Sent** to **Received** after the payment is matched, reconciled, and posted.</span></span> 

<span data-ttu-id="04e9a-141">[**ステートメントでの銀行口座名**] フィールドは、電子口座取引明細書の銀行口座に使用する名前です。</span><span class="sxs-lookup"><span data-stu-id="04e9a-141">The **Bank account name in statements** field is the name used for the bank account on your electronic bank statements.</span></span>  <span data-ttu-id="04e9a-142">この名前は、複数の銀行口座の情報を含む可能性のあるステートメントから銀行口座にどのトランザクションをインポートするかを決定する際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="04e9a-142">This name is used when determining what transactions to import for a bank account from a statement that may contain information for multiple bank accounts.</span></span> 

<span data-ttu-id="04e9a-143">[**インポート後の調整**] へのオプションは、自動的に口座取引明細書の検証、新しい銀行調整とワークシートの作成および既定の照合ルール セットの実行を行います。</span><span class="sxs-lookup"><span data-stu-id="04e9a-143">The option to **Reconcile after import** will automatically validate the bank statement, create a new bank reconciliation and worksheet, and run the Default matching rule set.</span></span>  <span data-ttu-id="04e9a-144">この機能は、手動で照合する必要があるトランザクションの時点までのプロセスを自動化します。</span><span class="sxs-lookup"><span data-stu-id="04e9a-144">This functionality automates the process up to the point of the transactions that must be manually matched.</span></span>  <span data-ttu-id="04e9a-145">銀行口座の設定は、インポートする時点では既定値です。</span><span class="sxs-lookup"><span data-stu-id="04e9a-145">The setting on the bank account will default when importing.</span></span>




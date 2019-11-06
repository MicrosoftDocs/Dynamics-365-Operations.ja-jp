---
title: 小売トランザクションの整合性チェック
description: このトピックでは、Dynamics 365 Retail の小売トランザクションの整合性チェック機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: b956565ac15b3d7b638cedaadc20923ee87b9c61
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622600"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="29f0b-103">小売トランザクションの整合性チェック</span><span class="sxs-lookup"><span data-stu-id="29f0b-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="29f0b-104">このトピックでは、小売トランザクションの整合性チェック機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-104">This topic describes the retail transaction consistency checker functionality.</span></span> <span data-ttu-id="29f0b-105">整合性チェックは、矛盾するトランザクションを特定し、明細書転記プロセスによって収集される前に隔離します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="29f0b-106">明細書が Retail に転記される際、小売トランザクション テーブルのデータ不整合が原因で転記が失敗する場合があります。</span><span class="sxs-lookup"><span data-stu-id="29f0b-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="29f0b-107">データの不整合は、販売時点管理 (POS) アプリケーションでの予期しない問題によって、またはトランザクションがサード パーティの POS システムから正しくインポートされなかった場合に起こります。</span><span class="sxs-lookup"><span data-stu-id="29f0b-107">The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="29f0b-108">こうした不整合は、次のような形で表れます。</span><span class="sxs-lookup"><span data-stu-id="29f0b-108">Examples of how these inconsistencies may appear include:</span></span> 

- <span data-ttu-id="29f0b-109">ヘッダー テーブルのトランザクションの合計が、明細行のトランザクションの合計と一致しない。</span><span class="sxs-lookup"><span data-stu-id="29f0b-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
- <span data-ttu-id="29f0b-110">ヘッダー テーブルの行数が、トランザクション テーブルの行数と一致しない。</span><span class="sxs-lookup"><span data-stu-id="29f0b-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
- <span data-ttu-id="29f0b-111">ヘッダー テーブルの税金額が、明細行の税金額と一致しない。</span><span class="sxs-lookup"><span data-stu-id="29f0b-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 

<span data-ttu-id="29f0b-112">明細書転記プロセスによって矛盾したトランザクションが収集されると、矛盾した売上請求書と支払仕訳帳が作成され、その結果、明細書転記プロセス全体が失敗します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="29f0b-113">このような状態になった明細書を修正するには、複数のトランザクション テーブルにわたって複雑なデータ修正を行わなければなりません。</span><span class="sxs-lookup"><span data-stu-id="29f0b-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="29f0b-114">小売トランザクションの整合性チェックには、こうした問題を防ぎます。</span><span class="sxs-lookup"><span data-stu-id="29f0b-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="29f0b-115">次の図は、トランザクションの整合性チェックを使用した転記プロセスを説明しています。</span><span class="sxs-lookup"><span data-stu-id="29f0b-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="29f0b-116">![小売トランザクションの整合性チェックを使用した明細書転記プロセス](./media/validchecker.png "小売トランザクションの整合性チェックを使用した明細書転記プロセス")</span><span class="sxs-lookup"><span data-stu-id="29f0b-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transaction consistency checker")</span></span>

<span data-ttu-id="29f0b-117">バッチ処理 **店舗トランザクションを検証する** では、次のシナリオで小売トランザクション テーブルの整合性をチェックします。</span><span class="sxs-lookup"><span data-stu-id="29f0b-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="29f0b-118">**顧客 ID** - 小売トランザクション テーブルの顧客 ID が HQ 顧客マスターに存在することを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-118">**Customer account** – Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="29f0b-119">**行数** - トランザクション ヘッダー テーブルにキャプチャされた明細行の数が、販売トランザクション テーブルの明細行の数と一致していることを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-119">**Line count** – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>
- <span data-ttu-id="29f0b-120">**税込み価格** – **税込み価格** パラメーターがトランザクション明細行間で一貫していることを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-120">**Price includes tax** – Validates that the **Price includes tax** parameter is consistent across transaction lines.</span></span>
- <span data-ttu-id="29f0b-121">**支払額** – 支払レコードがヘッダーの支払額と一致することを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-121">**Payment amount** - Validates that the payment records match the payment amount on header.</span></span>
- <span data-ttu-id="29f0b-122">**総額** – ヘッダーの総額が明細行の正味金額と税額の合計であることを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-122">**Gross amount** – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</span></span>
- <span data-ttu-id="29f0b-123">**正味金額** – ヘッダーの総額が明細行の正味金額と税額の合計であることを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-123">**Net amount** – Validates that the net amount on the header is the sum of the net amounts on the lines.</span></span>
- <span data-ttu-id="29f0b-124">**過少支払または過剰支払** – ヘッダーの総額と支払額の差が最大過少支払/過剰支払コンフィギュレーションを超えていないことを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-124">**Under / Over payment** – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</span></span>
- <span data-ttu-id="29f0b-125">**割引金額** – 割引テーブルの割引金額と小売トランザクション明細行のテーブルの割引金額が一致していること、およびヘッダーの割引金額が明細行の割引金額の合計であることを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-125">**Discount amount** – Validates that the discount amount on the discount tables and the discount amount on the retail transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</span></span>
- <span data-ttu-id="29f0b-126">**明細行割引** – トランザクション明細行の明細行割引が、トランザクション明細行に対応する割引テーブルのすべての明細行の合計であることを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-126">**Line discount** – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</span></span>
- <span data-ttu-id="29f0b-127">**ギフト カード品目** – Retail ではギフト カード品目の返品はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="29f0b-127">**Gift card item** – Retail doesn't support the return of gift card items.</span></span> <span data-ttu-id="29f0b-128">ただし、ギフト カードの残高をキャッシュ アウトできます。キャッシュ アウト明細行の代わりに返品明細行としてギフト カード品目を処理すると、明細書の転記プロセスに失敗します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-128">However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</span></span> <span data-ttu-id="29f0b-129">ギフト カード品目の検証プロセスにより、小売トランザクション テーブルの返品ギフト カード明細行品目のみがギフト カードのキャッシュ アウト明細行であることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="29f0b-129">The validation process for gift card items helps guarantee that the only return gift card line items on the retail transaction tables are gift card cash-out lines.</span></span>
- <span data-ttu-id="29f0b-130">**負の価格** – 負の価格のトランザクション明細行が存在しないことを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-130">**Negative price** – Validates that there are no negative price transaction lines.</span></span>
- <span data-ttu-id="29f0b-131">**品目およびバリアント** – トランザクション明細行の品目およびバリアントが、品目およびバリアント マスター ファイルに存在することを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-131">**Item & Variant** – Validates that items and variants on the transaction lines exist in the item and variant master file.</span></span>
- <span data-ttu-id="29f0b-132">**課税額** - 税レコードが明細行の税額と一致することを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-132">**Tax amount** - Validates that tax records match the tax amounts on the lines.</span></span>
- <span data-ttu-id="29f0b-133">**シリアル番号** - シリアル番号によって制御される品目のトランザクション明細行に、シリアル番号が存在するかを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-133">**Serial number** - Validates that the serial number is present in the transaction lines for items that are controlled by serial number.</span></span>
- <span data-ttu-id="29f0b-134">**符号** - 数量と正味金額の符号が、すべてのトランザクション明細行で同じであることを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-134">**Sign** - Validates that the sign on the quantity and the net amount are the same in all the transaction lines.</span></span>
- <span data-ttu-id="29f0b-135">**営業日** - 小売トランザクションの営業日すべての財務期間がオープンであることを検証します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-135">**Business date** - Validates that the financial periods for all the business dates for the retail transactions are open.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="29f0b-136">整合性チェックの設定</span><span class="sxs-lookup"><span data-stu-id="29f0b-136">Set up the consistency checker</span></span>

<span data-ttu-id="29f0b-137">**Retail \> Retail IT \> POS 転記** へ移動して、定期的実行のための "店舗トランザクションの検証" バッチ処理を構成します。</span><span class="sxs-lookup"><span data-stu-id="29f0b-137">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="29f0b-138">バッチ ジョブは、「明細書をバッチ計算する」や「明細書をバッチ転記する」の設定方法と同様に、店舗の組織階層を基にスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="29f0b-138">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="29f0b-139">このバッチ処理が 1 日に複数回実行されるように設定し、すべての P ジョブ実行の最後に実行されるようにスケジュールすることをおすすめします。</span><span class="sxs-lookup"><span data-stu-id="29f0b-139">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="29f0b-140">検証プロセスの結果</span><span class="sxs-lookup"><span data-stu-id="29f0b-140">Results of validation process</span></span>

<span data-ttu-id="29f0b-141">バッチ処理による検証確認の結果は、適切な小売トランザクションにタグ付けされています。</span><span class="sxs-lookup"><span data-stu-id="29f0b-141">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="29f0b-142">小売トランザクション レコードの **検証ステータス** フィールドは **成功** または **エラー** に設定され、検証が最後に実行された日付が **最後の検証日時** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="29f0b-142">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="29f0b-143">検証エラーを詳しく説明したエラー テキストを表示するには、関連する小売店舗のトランザクション レコードを選択し、**検証エラー** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="29f0b-143">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="29f0b-144">検証に失敗したトランザクション、およびまだ検証されていないトランザクションは、明細書に取り込まれません。</span><span class="sxs-lookup"><span data-stu-id="29f0b-144">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="29f0b-145">「明細書の計算」のプロセス中に、明細書に含むことができたが含まれなかったトランザクションがある場合、ユーザーに通知されます。</span><span class="sxs-lookup"><span data-stu-id="29f0b-145">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="29f0b-146">検証エラーが検出された場合、Microsoft サポートに問い合わせることでしかエラーは修正できません。</span><span class="sxs-lookup"><span data-stu-id="29f0b-146">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="29f0b-147">将来のリリースでは、エラーとなったレコードをユーザー インターフェイスを通じて修正するための機能が追加されます。</span><span class="sxs-lookup"><span data-stu-id="29f0b-147">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="29f0b-148">変更履歴を追跡するためのログおよび監査機能も利用可能になる予定です。</span><span class="sxs-lookup"><span data-stu-id="29f0b-148">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="29f0b-149">より多くのシナリオをサポートするための検証ルールは、将来のリリースで追加されます。</span><span class="sxs-lookup"><span data-stu-id="29f0b-149">Additional validation rules to support more scenarios will be added in a future release.</span></span>

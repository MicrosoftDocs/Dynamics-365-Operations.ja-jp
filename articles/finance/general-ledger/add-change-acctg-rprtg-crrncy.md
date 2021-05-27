---
title: 会計通貨またはレポート通貨の変更
description: このトピックでは、会計通貨またはレポート通貨を変更する方法や、元帳の設定にレポート通貨を追加する方法について説明します。
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 38b2cdb618d92dca7909a145e7fc07ddfc5f4d45
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017058"
---
# <a name="change-the-accounting-or-reporting-currency"></a><span data-ttu-id="e62c8-103">会計通貨またはレポート通貨の変更</span><span class="sxs-lookup"><span data-stu-id="e62c8-103">Change the accounting or reporting currency</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e62c8-104">このトピックでは、会計通貨またはレポート通貨を変更する方法や、元帳の設定にレポート通貨を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-104">This topic explains how to change the accounting or reporting currency, or add a reporting currency to the setup of a ledger.</span></span>

## <a name="symptom"></a><span data-ttu-id="e62c8-105">現象</span><span class="sxs-lookup"><span data-stu-id="e62c8-105">Symptom</span></span>

<span data-ttu-id="e62c8-106">会計通貨またはレポート通貨を変更したり、元帳の設定にレポート通貨を追加する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="e62c8-106">You want to change the accounting or reporting currency, or add a reporting currency to the ledger setup.</span></span> <span data-ttu-id="e62c8-107">これは通常、次のシナリオで発生します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-107">This typically occurs in the following scenarios:</span></span>

- <span data-ttu-id="e62c8-108">法人の設定時に間違った会計通貨またはレポート通貨が指定されました。</span><span class="sxs-lookup"><span data-stu-id="e62c8-108">The wrong accounting or reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="e62c8-109">現在、通貨を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e62c8-109">You now want to change that currency.</span></span>
- <span data-ttu-id="e62c8-110">法人の設定時にレポート通貨が指定されませんでした。</span><span class="sxs-lookup"><span data-stu-id="e62c8-110">No reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="e62c8-111">(レポート通貨はオプションです。) 現在、レポート通貨を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e62c8-111">(A reporting currency is optional.) You now want to add a reporting currency.</span></span>

<span data-ttu-id="e62c8-112">二重通貨機能を以前使用していなかった組織で、この機能の使用を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e62c8-112">An organization that didn't previously use the Dual currency capability wants to start to use it.</span></span> <span data-ttu-id="e62c8-113">この問題は通常、次のシナリオで発生します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-113">This issue typically occurs in the following scenarios.</span></span>

- <span data-ttu-id="e62c8-114">法人の設定時にレポート通貨が指定されましたが、現在、レポート通貨を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e62c8-114">A reporting currency was specified when a legal entity was set up, but the organization now wants to remove the reporting currency.</span></span>
- <span data-ttu-id="e62c8-115">組織は、Microsoft Dynamics 365 Finance にアップグレードまたは移行中で、会計通貨またはレポート通貨の変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="e62c8-115">The organization is upgrading or migrating to Microsoft Dynamics 365 Finance, and wants to change the accounting or reporting currency.</span></span>

## <a name="resolution"></a><span data-ttu-id="e62c8-116">解決策</span><span class="sxs-lookup"><span data-stu-id="e62c8-116">Resolution</span></span>

<span data-ttu-id="e62c8-117">最も重要な考慮事項は、元帳の設定でトランザクション (実績または予算) が法人に転記されているかどうかです。</span><span class="sxs-lookup"><span data-stu-id="e62c8-117">The most important consideration is whether any transactions (actual or budget) have been posted in the legal entity for the ledger setup.</span></span> <span data-ttu-id="e62c8-118">**トランザクション (実績または予算) が法人に転記されている場合は、会計通貨またはレポート通貨の変更や、レポート通貨の追加はできません。**</span><span class="sxs-lookup"><span data-stu-id="e62c8-118">**You can't change the accounting or reporting currency, or add a reporting currency, if any transactions (actual or budget) have been posted in the legal entity.**</span></span> <span data-ttu-id="e62c8-119">トランザクションが転記されたかどうかに応じて、次のいずれかのセクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e62c8-119">Follow the steps in one of the following sections, depending on whether transactions have been posted.</span></span>

### <a name="no-transactions-have-been-posted"></a><span data-ttu-id="e62c8-120">トランザクションが転記されていない</span><span class="sxs-lookup"><span data-stu-id="e62c8-120">No transactions have been posted</span></span>

1. <span data-ttu-id="e62c8-121">通貨を更新する法人で、**一般会計 \> 元帳の設定 \> 元帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-121">In the legal entity that you're updating currencies for, go to **General ledger \> Ledger setup \> Ledger**.</span></span>
2. <span data-ttu-id="e62c8-122">**元帳** ページで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-122">On the **Ledger** page, select **Edit**.</span></span>
3. <span data-ttu-id="e62c8-123">**通貨** クイック タブで、法人に使用する会計通貨とレポート通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-123">On the **Currency** FastTab, select the accounting currency and reporting currency to use for the legal entity.</span></span>
4. <span data-ttu-id="e62c8-124">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-124">Select **Save**.</span></span>

<span data-ttu-id="e62c8-125">会計通貨とレポート通貨のフィールドが **元帳** ページで使用できない場合、1 つ以上のトランザクション (実績または予算) が法人に転記されています。</span><span class="sxs-lookup"><span data-stu-id="e62c8-125">If the fields for the accounting currency and the reporting currency aren't available on the **Ledger** page, one or more transactions (actual or budget) have been posted in the legal entity.</span></span> <span data-ttu-id="e62c8-126">そのため、通貨を変更できません。</span><span class="sxs-lookup"><span data-stu-id="e62c8-126">Therefore, the currencies can't be changed.</span></span> <span data-ttu-id="e62c8-127">この場合、次のセクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e62c8-127">In this case, follow the steps in the next section.</span></span>

### <a name="transactions-have-been-posted"></a><span data-ttu-id="e62c8-128">トランザクションが転記されている</span><span class="sxs-lookup"><span data-stu-id="e62c8-128">Transactions have been posted</span></span>

<span data-ttu-id="e62c8-129">**トランザクションが法人に転記されている場合、会計通貨およびレポート通貨を変更または追加する方法でのみ、正しい通貨を持つ新しい法人を作成することができます。**</span><span class="sxs-lookup"><span data-stu-id="e62c8-129">**If transactions have been posted in the legal entity, the only way to change or add accounting and reporting currencies is to create a new legal entity that has the correct currencies.**</span></span> <span data-ttu-id="e62c8-130">このプロセスを容易にするために、システムのデータ管理では、設定レコードとマスター レコードを現在の法人から新しい法人にコピーできます。</span><span class="sxs-lookup"><span data-stu-id="e62c8-130">To help make this process easier, Data management in the system lets you copy setup records and master records from the current legal entity to a new legal entity.</span></span>

<span data-ttu-id="e62c8-131">会計通貨およびレポート通貨の変更は広範囲に影響します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-131">Changes to the accounting and reporting currencies are pervasive.</span></span> <span data-ttu-id="e62c8-132">これらは、一般会計だけでなく、すべての補助元 (売掛金勘定、買掛金勘定、在庫、プロジェクトなど)、すべての独立系ソフトウェア ベンダー (ISV) ソリューション、および金額を保存する目的で作成した拡張機能にも影響します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-132">They affect not only General ledger but also every subledger (Accounts receivable, Accounts payable, Inventory, Project, and so on), every independent software vendor (ISV) solutions, and any extension that you've made that stores amounts.</span></span>

<span data-ttu-id="e62c8-133">各金額を検索して別の通貨に換算するプロセスでは、エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="e62c8-133">The process of finding and translating each amount to a different currency is subject to error.</span></span> <span data-ttu-id="e62c8-134">そのため、エンジニアリング チームは、会計通貨とレポート通貨を変更または追加するスクリプトを承認しません。</span><span class="sxs-lookup"><span data-stu-id="e62c8-134">Therefore, the engineering team won't approve a script that changes or adds accounting and reporting currencies.</span></span> <span data-ttu-id="e62c8-135">また、Microsoft Dynamics AX 2012 で使用可能なツールで会計通貨とレポート通貨を変更または追加することもできますが、AX 2012 R3 と Finance の両方でこのツールは非推奨になっています。</span><span class="sxs-lookup"><span data-stu-id="e62c8-135">Additionally, although a tool that used to be available for Microsoft Dynamics AX 2012 let you change or add accounting and reporting currencies, that tool was deprecated for both AX 2012 R3 and Finance.</span></span>

<span data-ttu-id="e62c8-136">以下の手順に従って、現在の法人から新しい法人に設定とマスター データをコピーします。</span><span class="sxs-lookup"><span data-stu-id="e62c8-136">Follow these steps to copy the setup and master data from the current legal entity to a new legal entity.</span></span>

1. <span data-ttu-id="e62c8-137">**ワークスペース \> データ管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-137">Go to **Workspaces \> Data management**.</span></span>
2. <span data-ttu-id="e62c8-138">**インポート/エクスポート** グループで **テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-138">Select **Templates** under the **Import/Export** group.</span></span>
3. <span data-ttu-id="e62c8-139">テンプレートが使用可能であるか確認します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-139">Make sure that templates are available.</span></span> <span data-ttu-id="e62c8-140">使用できるテンプレートがない場合は、**既定のテンプレートの読み込み** を選択してテンプレートが生成されるのを待ちます。</span><span class="sxs-lookup"><span data-stu-id="e62c8-140">If no templates are available, select **Load default templates**, and wait for the templates to be generated.</span></span>
4. <span data-ttu-id="e62c8-141">**データ管理** ワークスペースに戻ります。</span><span class="sxs-lookup"><span data-stu-id="e62c8-141">Return to the **Data management** workspace.</span></span>
5. <span data-ttu-id="e62c8-142">**法人にコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-142">Select **Copy into legal entity**.</span></span>
6. <span data-ttu-id="e62c8-143">グループ名と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-143">Enter a group name and description.</span></span>
7. <span data-ttu-id="e62c8-144">**ソース法人** フィールドで、データのコピー元の法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-144">In the **Source legal entity** field, select the legal entity to copy data from.</span></span>
8. <span data-ttu-id="e62c8-145">**宛先の法人** クイック タブで **法人の作成** を選択し、ソース法人データのコピー先の新しい法人を作成します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-145">In the **Destination legal entities** FastTab, select **Create legal entities** to create a new legal entity that you can copy the source legal entity data to.</span></span> <span data-ttu-id="e62c8-146">**既存の選択** を選択してデータを既存の法人にコピーします。</span><span class="sxs-lookup"><span data-stu-id="e62c8-146">Select **Select existing** to copy data to an existing legal entity.</span></span>
9. <span data-ttu-id="e62c8-147">オプション: **番号順序のコピー** フィールドを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-147">Optional: Set the **Copy number sequences** field to **Yes**.</span></span> <span data-ttu-id="e62c8-148">(データをコピーする場合は、この手順をお推奨します。)</span><span class="sxs-lookup"><span data-stu-id="e62c8-148">(This step is recommended when you copy data.)</span></span>
10. <span data-ttu-id="e62c8-149">**選択したエンティティ** エリアで **テンプレートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-149">In the **Selected entities** area, select **Add template**.</span></span>
11. <span data-ttu-id="e62c8-150">使用するテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-150">Select the templates to use.</span></span> <span data-ttu-id="e62c8-151">新しい法人の推奨されるテンプレートには、**025 - 一般会計** と **財務** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e62c8-151">Suggested templates for a new legal entity include **025 - General Ledger** and **Financials**.</span></span> <span data-ttu-id="e62c8-152">その他すべての使用可能なテンプレートを確認し、どのテンプレートが要件に適用されるかどうかを確認することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-152">We recommend that you review all the other available templates to determine whether any of them apply to your requirements.</span></span>
12. <span data-ttu-id="e62c8-153">**法人にコピー** を選択してバッチ処理を開始すると、選択したエンティティが作成され、宛先の法人にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="e62c8-153">Select **Copy into legal entity** to start a batch process that will create the selected entities and copy them into the destination legal entity.</span></span>
13. <span data-ttu-id="e62c8-154">プロセスが完了した後で、トランザクションが転記される前に、元帳に移動し、このトピックで前述したように、会計通貨とレポート通貨を更新します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-154">After the process is completed, but before any transaction are posted, go to the ledger, and update the accounting and reporting currencies as described earlier in this topic.</span></span>

<span data-ttu-id="e62c8-155">会計通貨またはレポート通貨を変更できるよう新しい法人を作成した場合は、期首残高が古い法人の通貨から新しい通貨に換算済みであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e62c8-155">If you created a new legal entity so that you can change the accounting or reporting currency, verify that the beginning balances are translated from the currencies of the old legal entity to the new currencies.</span></span>

<span data-ttu-id="e62c8-156">上記の手順を示すビデオについては、[法人へのコピー](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e62c8-156">For a video that shows the preceding steps, see [Copy Into Legal Entity](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).</span></span>

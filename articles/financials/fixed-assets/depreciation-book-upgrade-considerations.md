---
title: 減価償却簿のアップグレードの概要
description: 以前のリリースでは、固定資産には 2 つの評価概念がありました - 価値モデルおよび減価償却簿。 Microsoft Dynamics 365 for Operations (1611) では、価値モデル機能および減価償却簿機能は帳簿と呼ばれる単一の概念に統合されました。 このトピックでは、アップグレードで考慮すべき点について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 805f6ab1cd1d0996e685278cc997f532213c76c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "359316"
---
# <a name="depreciation-book-upgrade-overview"></a><span data-ttu-id="66532-105">減価償却簿のアップグレードの概要</span><span class="sxs-lookup"><span data-stu-id="66532-105">Depreciation book upgrade overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66532-106">以前のリリースでは、固定資産には 2 つの評価概念がありました - 価値モデルおよび減価償却簿。</span><span class="sxs-lookup"><span data-stu-id="66532-106">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="66532-107">Microsoft Dynamics 365 for Operations (1611) では、価値モデル機能および減価償却簿機能は帳簿と呼ばれる単一の概念に統合されました。</span><span class="sxs-lookup"><span data-stu-id="66532-107">In Microsoft Dynamics 365 for Operations (1611), the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span> <span data-ttu-id="66532-108">このトピックでは、アップグレードで考慮すべき点について説明します。</span><span class="sxs-lookup"><span data-stu-id="66532-108">This topic provides some things to consider for the upgrade.</span></span> 

<span data-ttu-id="66532-109">アップグレード プロセスは、既存のセットアップと既存のすべてのトランザクションを新しい帳簿構造に移動します。</span><span class="sxs-lookup"><span data-stu-id="66532-109">The upgrade process will move your existing setup and all existing transactions to the new book structure.</span></span> <span data-ttu-id="66532-110">価値モデルは、現在のように総勘定元帳に転記する帳簿のままになります。</span><span class="sxs-lookup"><span data-stu-id="66532-110">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="66532-111">減価償却簿は、**総勘定元帳への転記**オプションが**いいえ**に設定されている帳簿に移動されます。</span><span class="sxs-lookup"><span data-stu-id="66532-111">Depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="66532-112">減価償却簿の仕訳帳名は、**なし**に設定されている転記階層の総勘定元帳の仕訳帳名に移動されます。</span><span class="sxs-lookup"><span data-stu-id="66532-112">Depreciation book journal names will be moved to a general ledger journal name with the posting layer set to **None**.</span></span> <span data-ttu-id="66532-113">減価償却簿トランザクションは、固定資産トランザクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="66532-113">Depreciation book transactions will be moved to Fixed asset transactions.</span></span> 

<span data-ttu-id="66532-114">データ アップグレードを実行する前に、トランザクション伝票に減価償却簿の仕訳帳明細行をアップグレードするために使用できる 2 つのオプションと、伝票シリーズに使用される番号順序を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66532-114">Before running the data upgrade, you should understand the two options available for upgrading depreciation book journal lines to transaction vouchers, and the number sequence that will be used for the voucher series.</span></span> 

<span data-ttu-id="66532-115">オプション 1: **システムで定義されている番号順序** - これはアップグレード パフォーマンスを最適化する既定のオプションです。</span><span class="sxs-lookup"><span data-stu-id="66532-115">Option 1:  **System-defined number sequence** - This is the default option to optimize upgrade performance.</span></span> <span data-ttu-id="66532-116">アップグレードは、番号順序フレームワークを使用しませんが、代わりにセット ベースのアプローチによる伝票を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="66532-116">The upgrade will not use the number sequences framework, but instead will allocate vouchers with a set-based approach.</span></span> <span data-ttu-id="66532-117">アップグレード後、新しい番号順序は、適切にアップグレードしたトランザクションに基づいて**次の番号セット**が作成されます。</span><span class="sxs-lookup"><span data-stu-id="66532-117">After the upgrade, the new number sequence will be created with the **Next number set** appropriately based on the upgraded transactions.</span></span> <span data-ttu-id="66532-118">既定では、使用される番号順序は、FADBUpgr\#\#\#\#\#\#\#\#\# 形式です。</span><span class="sxs-lookup"><span data-stu-id="66532-118">By default, the number sequence used will be in the FADBUpgr\#\#\#\#\#\#\#\#\# format.</span></span> <span data-ttu-id="66532-119">この方法を使用するとき、形式を調整するために使用可能ないくつかのパラメーターがあります:</span><span class="sxs-lookup"><span data-stu-id="66532-119">There are a few parameters available to you to adjust the format when using this approach:</span></span>

-   <span data-ttu-id="66532-120">**番号順序コード** – 番号順序を識別するコード。</span><span class="sxs-lookup"><span data-stu-id="66532-120">**Number sequence code** – The code to identify the number sequence.</span></span> <span data-ttu-id="66532-121">この番号順序コードは、アップグレードによって作成されるため存在できません。</span><span class="sxs-lookup"><span data-stu-id="66532-121">This number sequence code cannot exist since it will be created by the upgrade.</span></span>
    -   <span data-ttu-id="66532-122">定数名: **NumberSequenceDefaultCode**</span><span class="sxs-lookup"><span data-stu-id="66532-122">Constant name: **NumberSequenceDefaultCode**</span></span>
    -   <span data-ttu-id="66532-123">既定値: 「FADBUpgr」</span><span class="sxs-lookup"><span data-stu-id="66532-123">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="66532-124">**接頭語** – 伝票番号の接頭語として使用される定数文字列値。</span><span class="sxs-lookup"><span data-stu-id="66532-124">**Prefix** – The constant string value that will be used as a prefix for the voucher numbers.</span></span>
    -   <span data-ttu-id="66532-125">定数名: **NumberSequenceDefaultParameterPrefix**</span><span class="sxs-lookup"><span data-stu-id="66532-125">Constant name: **NumberSequenceDefaultParameterPrefix**</span></span>
    -   <span data-ttu-id="66532-126">既定値: 「FADBUpgr」</span><span class="sxs-lookup"><span data-stu-id="66532-126">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="66532-127">**英数字の長さ** – 番号順序の英数字区分の長さ。</span><span class="sxs-lookup"><span data-stu-id="66532-127">**Alphanumeric length** – The length of the alphanumeric segment of the number sequence.</span></span>
    -   <span data-ttu-id="66532-128">定数名: \*\*NumberSequenceDefaultParameterAlpanumericLength \*\*</span><span class="sxs-lookup"><span data-stu-id="66532-128">Constant name: \*\*NumberSequenceDefaultParameterAlpanumericLength \*\*</span></span>
    -   <span data-ttu-id="66532-129">既定値: 9</span><span class="sxs-lookup"><span data-stu-id="66532-129">Default value: 9</span></span>
-   <span data-ttu-id="66532-130">**開始番号** - 番号順序で使用される最初の番号。</span><span class="sxs-lookup"><span data-stu-id="66532-130">**Start number** - The first number to be used in the number sequence.</span></span>
    -   <span data-ttu-id="66532-131">定数名: \*\*NumberSequenceDefaultParameterStartNumber \*\*</span><span class="sxs-lookup"><span data-stu-id="66532-131">Constant name: \*\*NumberSequenceDefaultParameterStartNumber  \*\*</span></span>
    -   <span data-ttu-id="66532-132">既定値: 1</span><span class="sxs-lookup"><span data-stu-id="66532-132">Default value: 1</span></span>

<span data-ttu-id="66532-133">オプション 2: **既存のユーザー定義の番号順序** - このオプションは、アップグレードに使用する番号順序を定義できます。</span><span class="sxs-lookup"><span data-stu-id="66532-133">Option 2: **Existing user-defined number sequence** - This option will allow you to define the number sequence to be used for the upgrade.</span></span> <span data-ttu-id="66532-134">高度な番号順序のコンフィギュレーションが必要な場合はこのオプションの使用を検討してください。</span><span class="sxs-lookup"><span data-stu-id="66532-134">Consider using this option if you need advanced number sequence configuration.</span></span> <span data-ttu-id="66532-135">番号順序を使用するには、アップグレード クラス「ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans」を次の情報で変更する必要があります:</span><span class="sxs-lookup"><span data-stu-id="66532-135">To use a number sequence, you must modify the upgrade class ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans with the following information:</span></span>

-   <span data-ttu-id="66532-136">**番号順序コード** – 番号順序のコード。</span><span class="sxs-lookup"><span data-stu-id="66532-136">**Number sequence code** – The code of the number sequence.</span></span>
    -   <span data-ttu-id="66532-137">定数名: \*\*NumberSequenceExistingCode \*\*</span><span class="sxs-lookup"><span data-stu-id="66532-137">Constant name: \*\*NumberSequenceExistingCode \*\*</span></span>
    -   <span data-ttu-id="66532-138">既定値: 既定値はありません、番号順序コードを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66532-138">Default value: No default, this must be updated to the number sequence code.</span></span>
-   <span data-ttu-id="66532-139">**共有番号順序** – 番号順序のスコープを識別するブール値。</span><span class="sxs-lookup"><span data-stu-id="66532-139">**Shared number sequence** – A boolean value to identify the scope of the number sequence.</span></span> <span data-ttu-id="66532-140">すべての会社間の共有番号順序には「true」を使用し、企業固有のスコープには「false」を使用します。</span><span class="sxs-lookup"><span data-stu-id="66532-140">Use "true" for shared number sequences across all companies, and "false" for a company-specific scope.</span></span> <span data-ttu-id="66532-141">「false」を使用する場合、指定された名前の番号順序が、減価償却簿トランザクションを含むすべての会社に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66532-141">When using "false", the number sequence with the specified name must exist in every company that contains depreciation book transactions.</span></span> <span data-ttu-id="66532-142">減価償却簿トランザクションを含むすべてのパーティションには、共有番号順序が存在します。</span><span class="sxs-lookup"><span data-stu-id="66532-142">Shared number sequences exist in every partition that contains depreciation book transactions.</span></span>
    -   <span data-ttu-id="66532-143">定数名: \*\*NumberSequenceExistingIsShared \*\*</span><span class="sxs-lookup"><span data-stu-id="66532-143">Constant name: \*\*NumberSequenceExistingIsShared \*\*</span></span>
    -   <span data-ttu-id="66532-144">既定値: 「true」</span><span class="sxs-lookup"><span data-stu-id="66532-144">Default value: true</span></span>

<span data-ttu-id="66532-145">パラメーターは、「ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans」クラスの先頭にあります。</span><span class="sxs-lookup"><span data-stu-id="66532-145">The parameters are located at the beginning of the ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class.</span></span> 

<span data-ttu-id="66532-146">*// 伝票配賦の好ましいアプローチを指定* 
 *// 「true」、既存の番号順序コードを使用する場合* 
 *// 「false」、システムで定義されている番号順序 (既定) を使用する場合* const boolean NumberSequenceUseExistingCode = false;</span><span class="sxs-lookup"><span data-stu-id="66532-146">*// Specify a preferable approach of vouchers allocation* 
 *// true, if you want to use an existing number sequence code* 
 *// false, if you intend to use the system-defined number sequence (default)* const boolean NumberSequenceUseExistingCode = false;</span></span>  

<span data-ttu-id="66532-147">*// システム定義された番号順序のアプローチを使用する場合は、番号順序のパラメーターを指定します。*
 *// 新しい番号順序は、これらのパラメーターで作成されます。*</span><span class="sxs-lookup"><span data-stu-id="66532-147">*// If using the system-defined number sequence approach, specify the parameters for the number sequence.*
 *// A new number sequence will be created with these parameters.*</span></span> <span data-ttu-id="66532-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span><span class="sxs-lookup"><span data-stu-id="66532-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span></span>   

<span data-ttu-id="66532-149">*// 既存の番号順序アプローチを使用する場合は、既存の番号順序コードを指定します。* 
 *// 伝票の配賦は、既存の番号順序のために行ごとに移動します。*</span><span class="sxs-lookup"><span data-stu-id="66532-149">*// If using the existing number sequence approach, specify the existing number sequence code.* 
 *// Voucher allocation will go row-by-row for existing number sequences.*</span></span> <span data-ttu-id="66532-150">const str NumberSequenceExistingCode = ''; *// 既存の番号順序コードのスコープを指定* 
 *// 「true」、指定された番号順序が共有されている場合* 
 *// 「false」、指定された番号順序が会社単位である場合* 
 *// 指定されたスコープの番号順序コードが見つからない場合は、既定のシステム定義の番号順序が使用されます。*</span><span class="sxs-lookup"><span data-stu-id="66532-150">const str NumberSequenceExistingCode = ''; *// Specify the scope of the existing number sequence code* 
 *// true, if the specified number sequence is shared* 
 *// false, if the specified number sequence is per-company* 
 *// The default system-defined number sequence will be used if a number sequence code with the specified scope is not found.*</span></span> <span data-ttu-id="66532-151">const boolean NumberSequenceExistingIsShared = true;</span><span class="sxs-lookup"><span data-stu-id="66532-151">const boolean NumberSequenceExistingIsShared = true;</span></span> 

<span data-ttu-id="66532-152">定数が変更された後、クラスを含むプロジェクトを再構築します。</span><span class="sxs-lookup"><span data-stu-id="66532-152">Rebuild the project that contains the class after the constants have been modified.</span></span> 

<span data-ttu-id="66532-153">システム生成の番号順序アプローチ (オプション 1) を使用する場合、アップグレードは、アップグレード スクリプト パラメーターで指定された伝票番号を割り当てるためにセット ベースの処理が使用されます。</span><span class="sxs-lookup"><span data-stu-id="66532-153">When using the system-generated number sequence approach (option 1), the upgrade will use set-based processing to allocate the voucher numbers as specified in the upgrade script parameters.</span></span> <span data-ttu-id="66532-154">また、割り当て後に指定されたパラメーターで新しい番号順序を作成します。</span><span class="sxs-lookup"><span data-stu-id="66532-154">It will also create a new number sequence with specified parameters after the allocation.</span></span> 

<span data-ttu-id="66532-155">ユーザー定義の既存の番号順序アプローチ (オプション 2) を使用する場合は、データのアップグレードは、指定されたスコープの番号順序が減価償却簿トランザクションを持つ各パーティションおよび会社のデータベースに存在するかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="66532-155">When using the user-defined existing number sequence approach (option 2), the data upgrade checks whether the number sequence with the specified scope exists in the database for each partition and company with depreciation book transactions.</span></span> <span data-ttu-id="66532-156">それが存在する場合、アップグレードは行単位の処理を使用して番号順序のフレームワークを使用し番号順序で指定される伝票番号を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="66532-156">If it does exist, the upgrade will use row-by-row processing to allocate the voucher numbers as specified by the number sequence using the number sequence framework.</span></span> <span data-ttu-id="66532-157">指定したスコープで番号順序が存在しない場合、アップグレードは伝票番号を割り当てるために既定のシステムで定義された番号順序アプローチを使用し、割り当て後に指定した既定のパラメーターで新しい番号順序を作成します。</span><span class="sxs-lookup"><span data-stu-id="66532-157">If the number sequence does not exist with the specified scope, the upgrade will use the default system-defined number sequence approach to allocate the voucher numbers, and will create a new number sequence with specified default parameters after the allocation.</span></span>

<span data-ttu-id="66532-158">どちらのアプローチでも、データ アップグレード スクリプトは、以前の減価償却簿仕訳帳名のために作成された新しい総勘定元帳仕訳帳名の**伝票シリーズ**フィールドのために番号順序を使用します。</span><span class="sxs-lookup"><span data-stu-id="66532-158">With either approach, the data upgrade script will also use the number sequence for the **Voucher series** field on the new general ledger journal names created for the former depreciation book journal names.</span></span>




---
title: 現金管理の改善
description: このトピックでは、Dynamics 365 Commerce の POS で現金管理の改善について説明します。
author: anpurush
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
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
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0c561c39dfcbfa739c5a22394c05191e7f9bc107
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413718"
---
# <a name="cash-management-improvements"></a><span data-ttu-id="08ba9-103">現金管理の改善</span><span class="sxs-lookup"><span data-stu-id="08ba9-103">Cash management improvements</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="08ba9-104">現金管理は、現物店舗の小売業者にとって重要な機能です。</span><span class="sxs-lookup"><span data-stu-id="08ba9-104">Cash management is a key function for retailers in physical stores.</span></span> <span data-ttu-id="08ba9-105">小売業者は、店舗内のレジスターとレジ担当者間にて、現金の完全なトレーサビリティと責任、および動きが分かるシステムを店舗に必要としています。</span><span class="sxs-lookup"><span data-stu-id="08ba9-105">Retailers want their stores to have systems that can help them provide complete traceability and accountability of cash and its movement across the different registers and cashiers in a store.</span></span> <span data-ttu-id="08ba9-106">すべての相違点を調整し、説明責任を決定を可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ba9-106">They must be able to reconcile any differences and determine accountability.</span></span>


<span data-ttu-id="08ba9-107">Microsoft Dynamics 365 Commerce は、販売時点管理 (POS) アプリケーションでの現金管理機能を備えています。</span><span class="sxs-lookup"><span data-stu-id="08ba9-107">Microsoft Dynamics 365 Commerce has cash management capabilities in its point of sale (POS) application.</span></span> <span data-ttu-id="08ba9-108">ただし、バージョン 10.0.3 よりも前のバージョンの小売では、現金管理機能は店舗での現金移動を完全に追跡できないほど堅牢ではありません。</span><span class="sxs-lookup"><span data-stu-id="08ba9-108">However, in versions of Retail that are earlier than version 10.0.3, cash management functionality isn't robust enough to provide complete traceability of cash movements in stores.</span></span> <span data-ttu-id="08ba9-109">小売業者は店舗の現金を調整できますが、現金不一致が発生した場合には、説明責任を正確に判断することはできません。</span><span class="sxs-lookup"><span data-stu-id="08ba9-109">Although retailers can reconcile the cash for a store, they can't precisely determine accountability in the event of a cash discrepancy.</span></span>


<span data-ttu-id="08ba9-110">Retail バージョン 10.0.3 以降、小売業者は現金の処理に関するトレーサビリティを取得します。</span><span class="sxs-lookup"><span data-stu-id="08ba9-110">In Retail version 10.0.3 and later, retailers will gain traceability for cash handling.</span></span> <span data-ttu-id="08ba9-111">このトレーサビリティの一部として、小売業者は安全を定義し、両面の現金トランザクションを作成し、現金管理トランザクションを調整することができます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-111">As part of this traceability, retailers will be able to define safes, make two-sided cash transactions, and reconcile cash management transactions.</span></span>

## <a name="set-up-traceability-and-define-safes"></a><span data-ttu-id="08ba9-112">トレーサビリティの設定と安全の定義</span><span class="sxs-lookup"><span data-stu-id="08ba9-112">Set up traceability and define safes</span></span>

<span data-ttu-id="08ba9-113">新しい現金管理機能を設定するには、次の手順に従って店舗の機能プロファイルをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="08ba9-113">To set up the new cash management functionality, follow these steps to configure the functionality profile for stores.</span></span>

1. <span data-ttu-id="08ba9-114">**Retail と Commerce\> チャネル設定 \> POS の設定 \> POS プロファイル \> 機能プロファイル** の順に移動し、現金管理利用を改善したい店舗にリンクされた機能プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="08ba9-114">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**, and select a functionality profile that is linked to the stores where you want to make the improvements for cash management available.</span></span>
2. <span data-ttu-id="08ba9-115">機能プロファイル **機能** FastTab で、**詳細な現金管理** の下にある、**現金トレーサビリティを有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="08ba9-115">On the **Functions** FastTab of the functionality profile, under **Advanced cash management**, set the **Enable cash traceability** option to **Yes**.</span></span>
3. <span data-ttu-id="08ba9-116">安全を設定するには、**Retail と Commerce \> チャネル \> 店舗 \> すべての店舗** の順に移動し、店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="08ba9-116">To set up safes, go to **Retail and Commerce \> Channels \> Stores \> All stores**, and select a store.</span></span>
4. <span data-ttu-id="08ba9-117">**店舗** ページの、アクション ペインで、**設定** タブの **設定** グループで、**安全** を選択します。</span><span class="sxs-lookup"><span data-stu-id="08ba9-117">On the **Stores** page, on the Action Pane, on the **Set up** tab, in the **Set up** group, select **Safes**.</span></span> <span data-ttu-id="08ba9-118">このオプションを使用すると、店舗の複数の安全を定義および管理できます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-118">By using this option, you can define and maintain multiple safes for a store.</span></span>
4. <span data-ttu-id="08ba9-119">機能を使用する前に、**1070 チャネル構成** ディストリビューション スケジュール ジョブを実行して、構成をチャネル データベースに同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ba9-119">Before the functionality can be used, you must run the **1070 Channel configuration** distribution schedule job to sync these configurations to the channel database.</span></span>

## <a name="additional-cash-management-changes"></a><span data-ttu-id="08ba9-120">追加の現金管理の変更</span><span class="sxs-lookup"><span data-stu-id="08ba9-120">Additional cash management changes</span></span>

<span data-ttu-id="08ba9-121">Retail 10.0.3 以降では、現金トランザクションに関連する次の機能も提供されます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-121">In Retail version 10.0.3 and later, the following capabilities that are related to cash transactions are also provided:</span></span>

- <span data-ttu-id="08ba9-122">「開始金額の申告」を要求されるユーザーは、現金のソースを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ba9-122">A user who is prompted to "declare start amount" must enter the source of cash.</span></span> <span data-ttu-id="08ba9-123">ユーザーは、店舗で定義されている使用可能な安全を検索し、レジスターに入れることができるように現金が取り出されている安全を選択できます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-123">The user can search for the available safes that are defined in the store and select the safe that the cash is being taken out of so that it can be put into the register.</span></span>
- <span data-ttu-id="08ba9-124">「支払/入金の削除」操作を行うユーザーは、未処理の「釣銭入力」トランザクションの一覧で、操作が行われているトランザクションを選択するように求められます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-124">A user who does a "tender removal" operation is prompted to select, in a list of open "float entry" transactions, the transaction that the operation is being done against.</span></span> <span data-ttu-id="08ba9-125">対応する釣銭入力がシステムに存在しない場合、ユーザーはリンクされていない支払/入金削除トランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-125">If the corresponding float entry doesn't exist in the system, the user can create a non-linked tender removal transaction.</span></span>
- <span data-ttu-id="08ba9-126">「釣銭入力」操作を行うユーザーは、未処理の「支払/入金の削除」トランザクションの一覧で、釣銭入力操作が行われているトランザクションを選択するように求められます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-126">A "float entry" operation prompts a user to select, in a list of open "tender removal" transactions, the transaction that the float entry operation is being done against.</span></span> <span data-ttu-id="08ba9-127">対応する支払/入金削除がシステムに存在しない場合、ユーザーはリンクされていない釣銭入力トランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-127">If the corresponding tender removal doesn't exist in the system, the user can create a non-linked float entry transaction.</span></span>
- <span data-ttu-id="08ba9-128">「安全保管」を作成したユーザーが、現金が落とされている安全な場所を選択するように求められます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-128">A user who makes a "safe drop" is prompted to select the safe where the cash is being dropped.</span></span>
- <span data-ttu-id="08ba9-129">店舗で定義されている安全については、ユーザーは開始金額の申告、釣銭入力の実行、支払/入金削除の実行、および銀行入金の作成などの操作を管理できます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-129">For safes that are defined in a store, users can manage operations such as declaring the start amount, doing a float entry, doing a tender removal, and making a bank drop.</span></span>
- <span data-ttu-id="08ba9-130">適切なユーザー特権を持つユーザーに対して、「シフト管理」操作では、有効、中断、およびブラインド クローズ済みシフトの現金残高が表示されます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-130">For users who have the appropriate user privileges, "manage shifts" operations show the cash balances of active, suspended, and blind closed shifts.</span></span>
- <span data-ttu-id="08ba9-131">シフト内またはシフト間の現金トランザクションを調整するには、調整するシフトを選択し、**調整** を選択します。</span><span class="sxs-lookup"><span data-stu-id="08ba9-131">To reconcile the cash transactions within a shift or across shifts, select the shift to reconcile, and then select **Reconcile**.</span></span> <span data-ttu-id="08ba9-132">開いているビューには、調整済および未調整のトランザクションの一覧が個別のタブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-132">The view that is opened shows the list of reconciled and unreconciled transactions on separate tabs.</span></span> <span data-ttu-id="08ba9-133">このビューから、ユーザーは未調整トランザクションを選択して調整するか、以前に調整したトランザクションを選択して未調整にすることができます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-133">From this view, users can either select unreconciled transactions and reconcile them, or select previously reconciled transactions and unreconcile them.</span></span>
- <span data-ttu-id="08ba9-134">調整中に、選択したトランザクションのバランスが取れない場合、ユーザーは不均衡調整の理由説明を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ba9-134">During reconciliation, if the selected transaction doesn't balance, the user must enter a description of the reason for the unbalanced reconciliation.</span></span> <span data-ttu-id="08ba9-135">ユーザーは、単一のトランザクションを選択し、必要に応じて、関連する理由の説明に従って調整することができます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-135">Users can select a single transaction and reconcile it with the relevant reason description as they require.</span></span>
- <span data-ttu-id="08ba9-136">シフトが終了するまで、ユーザーはトランザクションを調整したり、未調整にすることができます。</span><span class="sxs-lookup"><span data-stu-id="08ba9-136">Users can continue to reconcile and unreconcile transactions until the shift is closed.</span></span> <span data-ttu-id="08ba9-137">シフトを終了した後は、トランザクションを調整することはできません。</span><span class="sxs-lookup"><span data-stu-id="08ba9-137">After a shift is closed, the transactions can't be unreconciled.</span></span>
- <span data-ttu-id="08ba9-138">シフトの終了を選択した場合、Commerce はシフトに未調整の現金管理トランザクションが含まれていないことを検証します。</span><span class="sxs-lookup"><span data-stu-id="08ba9-138">When a user chooses to close a shift, Commerce validates that there are no unreconciled cash management transactions in the shift.</span></span> <span data-ttu-id="08ba9-139">未調整トランザクションがある場合、ユーザーはシフトを終了させることはできません。</span><span class="sxs-lookup"><span data-stu-id="08ba9-139">Users can't close a shift if there are unreconciled transactions.</span></span>

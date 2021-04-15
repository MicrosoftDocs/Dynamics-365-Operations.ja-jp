---
title: ギフト カードとクレジット メモ操作のシームレスなオフライン切り替え
description: このトピックでは、特定の支払タイプに対してシームレスなオフライン切り替えを提供する改善の概要について説明します。
author: rubendel
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: a8eda003e4cd4cf0d43bb07c93bd8d68a2fb9e57
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792960"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="d8bca-103">ギフト カードとクレジット メモ操作のシームレスなオフライン切り替え</span><span class="sxs-lookup"><span data-stu-id="d8bca-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8bca-104">販売時点管理 (POS) デバイスがチャネル データベースへの接続を失った場合、処理中だったほとんどの POS 操作およびトランザクションは、レジ担当者が接続が切断されたことを示す警告メッセージを受信した後、処理を進めることができます。</span><span class="sxs-lookup"><span data-stu-id="d8bca-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="d8bca-105">ただし、場合によっては、トランザクションが Retail Real-time Service に依存する要素を持つため、これらの要素は POS がオフラインのときにはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="d8bca-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="d8bca-106">このトピックでは、これらのシナリオで接続の切断による影響を軽減するために役立ついくつかの機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d8bca-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="d8bca-107">オフライン モードにおけるギフト カード トランザクションを完了する</span><span class="sxs-lookup"><span data-stu-id="d8bca-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="d8bca-108">ギフト カードの残高は、Microsoft Dynamics 365 Commerce 本社で集中管理する必要があるため、内部ギフト カードは Real-time Service に依存します。</span><span class="sxs-lookup"><span data-stu-id="d8bca-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="d8bca-109">不正またはその他の同期の問題を防ぐために、ギフト カードはトランザクションに追加されるとすぐにロックされます。</span><span class="sxs-lookup"><span data-stu-id="d8bca-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="d8bca-110">ロック機能を使用すると、ギフト カードを複数のターミナルで同時に使用することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="d8bca-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="d8bca-111">トランザクションが完了すると、ギフト カードは更新されロック解除されます。</span><span class="sxs-lookup"><span data-stu-id="d8bca-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="d8bca-112">ただし、ギフト カードがトランザクションに追加された後に POS が接続を失った場合、ギフト カードは使用できなくなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d8bca-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="d8bca-113">この状況を回避するため、Dynamics 365 Commerce には POS がオフラインの間にギフト カード明細行を含むトランザクションを完了できるようにするパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="d8bca-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="d8bca-114">このパラメーターがオンになっている場合は、強制的にオフラインにされたギフト カード トランザクションは、オフライン トランザクションと共に保存され、オフライン トランザクションが同期されるとコマース本社に同期されます。</span><span class="sxs-lookup"><span data-stu-id="d8bca-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="d8bca-115">また同期により、ギフト カードのロックは解除され、別のターミナルで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d8bca-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="d8bca-116">オフライン モードに切り替えた後にギフト カード トランザクションを完了する機能を有効にするには、**コマース パラメーター** の **転記** タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="d8bca-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="d8bca-117">このタブで、**ギフトカード** クイック タブを見つけ、**オフライン モードにおけるギフト カード トランザクションの実行を許可する** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d8bca-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![オフラインのギフト カード設定](../media/gift.png)

<span data-ttu-id="d8bca-119">通常、コマース パラメーターはキャッシュされます。</span><span class="sxs-lookup"><span data-stu-id="d8bca-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="d8bca-120">したがって、このパラメーターの設定が更新され、チャネルに変更を同期するために配布スケジュールが開始された後、変更が有効になるまでに最大 24 時間かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="d8bca-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="d8bca-121">変更を直ちに有効にするには、Microsoft インターネット インフォメーション サービス (IIS) をリセットします。</span><span class="sxs-lookup"><span data-stu-id="d8bca-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="d8bca-122">オフライン モードにおけるクレジット メモ トランザクションを完了する</span><span class="sxs-lookup"><span data-stu-id="d8bca-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="d8bca-123">内部ギフト カードと同様に、クレジット メモはコマース本社で集中管理されます。</span><span class="sxs-lookup"><span data-stu-id="d8bca-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="d8bca-124">コマースには、POS がオフラインの間にクレジット メモ トランザクションを完了するためのパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="d8bca-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="d8bca-125">このパラメーターは、前のセクションで説明したギフト カード パラメーターのように機能します。</span><span class="sxs-lookup"><span data-stu-id="d8bca-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="d8bca-126">パラメーターがオンになっている場合は、強制的にオフラインにされたクレジット メモ トランザクションが、POS がオフラインの間に実行された他のトランザクションと共に、チャンネル データベースに同期されます。</span><span class="sxs-lookup"><span data-stu-id="d8bca-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="d8bca-127">オフライン モードに切り替えた後にクレジット メモ トランザクションを完了する機能を有効にするには、**コマース パラメーター** ページの **転記** タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="d8bca-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="d8bca-128">このタブで、**クレジット メモ** クイック タブを見つけ、**オフライン モードにおけるクレジット メモ トランザクションの実行を許可する** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d8bca-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![オフラインのクレジット メモの設定](../media/creditmemo.png)

<span data-ttu-id="d8bca-130">通常、コマース パラメーターはキャッシュされます。</span><span class="sxs-lookup"><span data-stu-id="d8bca-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="d8bca-131">したがって、このパラメーターの設定が更新され、チャネルに変更を同期するために配布スケジュールが開始された後、変更が有効になるまでに最大 24 時間かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="d8bca-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="d8bca-132">変更を直ちに有効にするには、IIS をリセットしてください。</span><span class="sxs-lookup"><span data-stu-id="d8bca-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8bca-133">関連トピック</span><span class="sxs-lookup"><span data-stu-id="d8bca-133">Related topics</span></span>

- [<span data-ttu-id="d8bca-134">オフライン販売時点管理 (POS) の機能</span><span class="sxs-lookup"><span data-stu-id="d8bca-134">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-offline-functionality)
- [<span data-ttu-id="d8bca-135">オンラインおよびオフラインでの販売時点管理 (POS) の操作</span><span class="sxs-lookup"><span data-stu-id="d8bca-135">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 入庫倉庫操作のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での入庫倉庫操作の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920990"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="89ead-103">入庫倉庫操作のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="89ead-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89ead-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management での入庫倉庫操作の処理中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="89ead-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="89ead-105">エラー メッセージ "品質指示 %1 が生成されました。</span><span class="sxs-lookup"><span data-stu-id="89ead-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="89ead-106">クラスター プロファイルが見つかりませんでした。コンフィギュレーションを確認してください" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="89ead-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="89ead-107">問題の説明</span><span class="sxs-lookup"><span data-stu-id="89ead-107">Issue description</span></span>

<span data-ttu-id="89ead-108">このエラー メッセージは、品質管理 (QMS) が有効になっている入庫プロセスに関連しています。</span><span class="sxs-lookup"><span data-stu-id="89ead-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="89ead-109">環境内のコンフィギュレーションによっては、エラー メッセージを生成するトランザクションに関する詳細情報を追加すると、問題を修正できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="89ead-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="89ead-110">問題の解決</span><span class="sxs-lookup"><span data-stu-id="89ead-110">Issue resolution</span></span>

<span data-ttu-id="89ead-111">最初に、[クラスター ピッキング](set-up-cluster-picking.md)設定を確認し、クラスター プロファイルが正しく設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89ead-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="89ead-112">クラスター プロファイルが設定されていない場合は、モバイル デバイスのメニュー項目をクラスター ピッキングに使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="89ead-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="89ead-113">環境によっては、その他の関連するコンフィギュレーションも検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89ead-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="89ead-114">混合ライセンス プレートの受取は、貸方を除く廃棄コードに対しては機能しません。</span><span class="sxs-lookup"><span data-stu-id="89ead-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="89ead-115">問題の説明</span><span class="sxs-lookup"><span data-stu-id="89ead-115">Issue description</span></span>

<span data-ttu-id="89ead-116">廃棄コードの **アクション** フィールドが *貸方* または *仕損* に設定されている場合、返品品目を処理するには、[混合ライセンス プレートの受取](mixed-license-plate-receiving.md) メニュー項目のみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="89ead-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="89ead-117">問題の解決</span><span class="sxs-lookup"><span data-stu-id="89ead-117">Issue resolution</span></span>

<span data-ttu-id="89ead-118">Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。</span><span class="sxs-lookup"><span data-stu-id="89ead-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="89ead-119">現在のところ、**アクション** フィールドが *貸方* または *仕損* に設定された[廃棄コード](../service-management/set-up-disposition-codes.md)のみが、混合ライセンス プレート受取でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="89ead-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="89ead-120">製品受領書の更新の定期処理タスクを実行すると、未確認の発注書が確認されます。</span><span class="sxs-lookup"><span data-stu-id="89ead-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="89ead-121">問題の説明</span><span class="sxs-lookup"><span data-stu-id="89ead-121">Issue description</span></span>

<span data-ttu-id="89ead-122">*製品受領書の更新* 定期タスクを実行すると、*登録済* の在庫トランザクション ステータスがある未確認の発注書が自動的に確認されます。</span><span class="sxs-lookup"><span data-stu-id="89ead-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="89ead-123">問題の解決</span><span class="sxs-lookup"><span data-stu-id="89ead-123">Issue resolution</span></span>

<span data-ttu-id="89ead-124">新しい入庫積荷処理機能 *積荷数量の受入超過* によってこの問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="89ead-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="89ead-125">この機能を有効にするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースに移動して、次の機能を (記載されている順序で) オンにします。</span><span class="sxs-lookup"><span data-stu-id="89ead-125">To turn on this feature, go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="89ead-126">購買注文在庫トランザクションを積荷に関連付けます</span><span class="sxs-lookup"><span data-stu-id="89ead-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="89ead-127">積荷数量の過剰入荷</span><span class="sxs-lookup"><span data-stu-id="89ead-127">Over receipt of load quantities</span></span>

<span data-ttu-id="89ead-128">詳細については、[発注書に対する登録済製品の数量の転記](inbound-load-handling.md#post-registered-quantities)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89ead-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="89ead-129">入庫注文を登録すると、"数量が有効ではありません" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="89ead-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="89ead-130">問題の説明</span><span class="sxs-lookup"><span data-stu-id="89ead-130">Issue description</span></span>

<span data-ttu-id="89ead-131">**ライセンス ユーザー グループ化ポリシー** フィールドが、着信注文の登録に使用されるモバイル デバイス メニュー項目に対して *ユーザー定義* に設定されている場合は、エラー メッセージ ("数量が有効ではありません") が表示され、登録を完了できません。</span><span class="sxs-lookup"><span data-stu-id="89ead-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="89ead-132">問題の原因</span><span class="sxs-lookup"><span data-stu-id="89ead-132">Issue cause</span></span>

<span data-ttu-id="89ead-133">*ユーザー定義* がライセンス プレートのグループ化ポリシーとして使用されている場合、単位シーケンス グループによって示される別のライセンス 契約で、受信する在庫が別のライセンス 契約に 分割されます。</span><span class="sxs-lookup"><span data-stu-id="89ead-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="89ead-134">受け取る品目を追跡するためにバッチ番号またはシリアル番号を使用する場合は、登録されたライセンス プレートごとに、各バッチまたはシリアルの数量を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89ead-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="89ead-135">ライセンス プレートで指定された数量が、現在の分析コードに対してまだ受け取る必要がある数量を超えている場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="89ead-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="89ead-136">問題の解決</span><span class="sxs-lookup"><span data-stu-id="89ead-136">Issue resolution</span></span>

<span data-ttu-id="89ead-137">モバイル デバイス メニュー項目を使用して品目を登録する場合、**ライセンス プレートのグループ化ポリシー** フィールドが *ユーザー定義* に設定されている場合は、ライセンスの承認番号、バッチ番号、またはシリアル番号の確認または入力をシステムで要求する場合があります。</span><span class="sxs-lookup"><span data-stu-id="89ead-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="89ead-138">ライセンス契約の確認ページには、現在のライセンス 契約に割り当てられている数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="89ead-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="89ead-139">バッチまたはシリアルの確認ページには、現在のライセンス 契約で引き続き受け取る必要がある数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="89ead-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="89ead-140">ライセンスプレートとバッチまたはシリアル番号の組み合わせに対して登録する数量を入力できるフィールドも含まれます。</span><span class="sxs-lookup"><span data-stu-id="89ead-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="89ead-141">この場合、ライセンスプレートに登録されている数量が、まだ受け取る必要がある数量を超えないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="89ead-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="89ead-142">また、受信注文の登録でライセンスが多数生成されている場合は、**ライセンス プレートのグループ化ポリシー** フィールドの値を *ライセンス プレートのグループ化* に変更したり、品目に新しい単位シーケンス グループを割り当てたり、単位シーケンスグループの **ライセンス プレートのグループ化** オプションを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="89ead-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

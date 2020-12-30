---
title: 入庫倉庫操作のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での入庫倉庫操作の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 60b6e37ec9d716f635c2d25374ac25a82286660e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645975"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="f27dc-103">入庫倉庫操作のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f27dc-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f27dc-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management での入庫倉庫操作の処理中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f27dc-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="f27dc-105">エラー メッセージ "品質指示 %1 が生成されました。</span><span class="sxs-lookup"><span data-stu-id="f27dc-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="f27dc-106">クラスター プロファイルが見つかりませんでした。コンフィギュレーションを確認してください" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f27dc-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f27dc-107">問題の説明</span><span class="sxs-lookup"><span data-stu-id="f27dc-107">Issue description</span></span>

<span data-ttu-id="f27dc-108">このエラー メッセージは、品質管理 (QMS) が有効になっている入庫プロセスに関連しています。</span><span class="sxs-lookup"><span data-stu-id="f27dc-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="f27dc-109">環境内のコンフィギュレーションによっては、エラー メッセージを生成するトランザクションに関する詳細情報を追加すると、問題を修正できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f27dc-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f27dc-110">問題の解決</span><span class="sxs-lookup"><span data-stu-id="f27dc-110">Issue resolution</span></span>

<span data-ttu-id="f27dc-111">最初に、[クラスター ピッキング](set-up-cluster-picking.md)設定を確認し、クラスター プロファイルが正しく設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f27dc-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="f27dc-112">クラスター プロファイルが設定されていない場合は、モバイル デバイスのメニュー項目をクラスター ピッキングに使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="f27dc-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="f27dc-113">環境によっては、その他の関連するコンフィギュレーションも検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f27dc-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="f27dc-114">混合ライセンス プレートの受取は、貸方を除く廃棄コードに対しては機能しません。</span><span class="sxs-lookup"><span data-stu-id="f27dc-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f27dc-115">問題の説明</span><span class="sxs-lookup"><span data-stu-id="f27dc-115">Issue description</span></span>

<span data-ttu-id="f27dc-116">廃棄コードの **アクション** フィールドが *貸方* または *仕損* に設定されている場合、返品品目を処理するには、[混合ライセンス プレートの受取](mixed-license-plate-receiving.md) メニュー項目のみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f27dc-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f27dc-117">問題の解決</span><span class="sxs-lookup"><span data-stu-id="f27dc-117">Issue resolution</span></span>

<span data-ttu-id="f27dc-118">Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。</span><span class="sxs-lookup"><span data-stu-id="f27dc-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="f27dc-119">現在のところ、**アクション** フィールドが *貸方* または *仕損* に設定された[廃棄コード](../service-management/set-up-disposition-codes.md)のみが、混合ライセンス プレート受取でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f27dc-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="f27dc-120">製品受領書の更新の定期処理タスクを実行すると、未確認の発注書が確認されます。</span><span class="sxs-lookup"><span data-stu-id="f27dc-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f27dc-121">問題の説明</span><span class="sxs-lookup"><span data-stu-id="f27dc-121">Issue description</span></span>

<span data-ttu-id="f27dc-122">*製品受領書の更新* 定期タスクを実行すると、*登録済* の在庫トランザクション ステータスがある未確認の発注書が自動的に確認されます。</span><span class="sxs-lookup"><span data-stu-id="f27dc-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f27dc-123">問題の解決</span><span class="sxs-lookup"><span data-stu-id="f27dc-123">Issue resolution</span></span>

<span data-ttu-id="f27dc-124">新しい入庫積荷処理機能 *積荷数量の受入超過* によってこの問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="f27dc-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="f27dc-125">この機能を有効にするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)に移動して、次の機能を (記載されている順序で) オンにします。</span><span class="sxs-lookup"><span data-stu-id="f27dc-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="f27dc-126">購買注文在庫トランザクションを積荷に関連付けます</span><span class="sxs-lookup"><span data-stu-id="f27dc-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="f27dc-127">積荷数量の過剰入荷</span><span class="sxs-lookup"><span data-stu-id="f27dc-127">Over receipt of load quantities</span></span>

<span data-ttu-id="f27dc-128">詳細については、[発注書に対する登録済製品の数量の転記](inbound-load-handling.md#post-registered-quantities)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f27dc-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

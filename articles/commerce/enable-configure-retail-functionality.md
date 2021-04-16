---
title: 新しい Commerce 環境におけるシード データの初期化
description: この記事では、Dynamics 365 Commerce の初期化プロセスの一部として作成されるデータについて説明します。
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9f534410b21fd97554f4e038bb14eebd5f887130
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792586"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="cba21-103">新しい Commerce 環境におけるシード データの初期化</span><span class="sxs-lookup"><span data-stu-id="cba21-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cba21-104">この記事では、Dynamics 365 Commerce の初期化プロセスの一部として作成されるデータについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cba21-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cba21-105">Commerce ソリューションが Microsoft Dynamics Lifecycle Services (LCS) によって配置された後、基本的なコンフィギュレーション データを作成するために、Commerce コンフィギュレーションを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cba21-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cba21-106">Commerce コンフィギュレーションを初期化する前に、店舗を設定する法人ごとの言語と住所が指定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cba21-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="cba21-107">この手順は、Commerce 用に使用する法人ごとに完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cba21-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="cba21-108">コンフィギュレーションを初期化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cba21-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="cba21-109">Commerce クライアントを起動します。</span><span class="sxs-lookup"><span data-stu-id="cba21-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="cba21-110">**Retail とコマース** &gt; **バックオフィスの設定** &gt; **パラメーター** &gt; **コマース パラメーター** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="cba21-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="cba21-111">**初期化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cba21-111">Click **Initialize**.</span></span>

<span data-ttu-id="cba21-112">初期化によって、次の既定のコンフィギュレーション データを作成します:</span><span class="sxs-lookup"><span data-stu-id="cba21-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="cba21-113">Commerce 用スケジューラ ジョブとサブジョブ</span><span class="sxs-lookup"><span data-stu-id="cba21-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="cba21-114">コマース チャネル スキーマ</span><span class="sxs-lookup"><span data-stu-id="cba21-114">Commerce channel schema</span></span>
- <span data-ttu-id="cba21-115">Commerce 配送スケジュール</span><span class="sxs-lookup"><span data-stu-id="cba21-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="cba21-116">ボタン グリッドと画像、テーマを含む、既定の画面レイアウト</span><span class="sxs-lookup"><span data-stu-id="cba21-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="cba21-117">タイムゾーン情報</span><span class="sxs-lookup"><span data-stu-id="cba21-117">Time zone information</span></span>
- <span data-ttu-id="cba21-118">販売時点管理 (POS) 操作</span><span class="sxs-lookup"><span data-stu-id="cba21-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="cba21-119">POS アクセス許可</span><span class="sxs-lookup"><span data-stu-id="cba21-119">POS permissions</span></span>
- <span data-ttu-id="cba21-120">チャンネル レポート</span><span class="sxs-lookup"><span data-stu-id="cba21-120">Channel reports</span></span>
- <span data-ttu-id="cba21-121">属性メタデータ</span><span class="sxs-lookup"><span data-stu-id="cba21-121">Attribute metadata</span></span>
- <span data-ttu-id="cba21-122">エンティティ検証テンプレート</span><span class="sxs-lookup"><span data-stu-id="cba21-122">Entity validation templates</span></span>
- <span data-ttu-id="cba21-123">Commerce Data Exchange セッション履歴を削除するバッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="cba21-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="cba21-124">また、Payment Card Industry (PCI) に関連付けられるログが Commerce データベースに対して有効になります。</span><span class="sxs-lookup"><span data-stu-id="cba21-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="cba21-125">別々に Commerce 用スケジューラをコンフィギュレーションするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="cba21-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="cba21-126">このオプションで、Commerce 用スケジューラのコンフィギュレーションを既定の設定にリセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="cba21-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="cba21-127">初期化の完了後に、追加の Commerce データをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cba21-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="cba21-128">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="cba21-128">Here are some examples:</span></span>

- <span data-ttu-id="cba21-129">コマース パラメーター</span><span class="sxs-lookup"><span data-stu-id="cba21-129">Commerce parameters</span></span>
- <span data-ttu-id="cba21-130">コマース スケジューラのパラメーター</span><span class="sxs-lookup"><span data-stu-id="cba21-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="cba21-131">Commerce チャネル</span><span class="sxs-lookup"><span data-stu-id="cba21-131">Commerce channels</span></span>
- <span data-ttu-id="cba21-132">レジスターとデバイス</span><span class="sxs-lookup"><span data-stu-id="cba21-132">Registers and devices</span></span>
- <span data-ttu-id="cba21-133">品揃え</span><span class="sxs-lookup"><span data-stu-id="cba21-133">Assortments</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
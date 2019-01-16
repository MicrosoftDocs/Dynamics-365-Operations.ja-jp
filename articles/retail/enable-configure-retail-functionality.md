---
title: "新しい Retail 環境でのシード データの初期化"
description: "この記事では、Microsoft Dynamics 365 for Retail の初期化処理の一部として作成されるデータについて説明します。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.contentlocale: ja-jp
ms.lasthandoff: 01/04/2019

---

# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="708e1-103">新しい Retail 環境でのシード データの初期化</span><span class="sxs-lookup"><span data-stu-id="708e1-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="708e1-104">この記事では、Microsoft Dynamics 365 for Retail の初期化処理の一部として作成されるデータについて説明します。</span><span class="sxs-lookup"><span data-stu-id="708e1-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="708e1-105">小売ソリューションが Microsoft Dynamics Lifecycle Services (LCS) によって配置された後、基本的なコンフィギュレーション データを作成するために、小売コンフィギュレーションを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="708e1-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="708e1-106">小売コンフィギュレーションを初期化する前に、小売店舗を設定する法人ごとの言語と住所が指定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="708e1-106">Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="708e1-107">この手順は、小売に使用する法人ごとに完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="708e1-107">This step must be completed for each legal entity that you use for retail.</span></span>

<span data-ttu-id="708e1-108">小売のコンフィギュレーションを初期化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="708e1-108">To initialize the retail configuration, follow these steps.</span></span>

1. <span data-ttu-id="708e1-109">Dynamics 365 for Retail クライアントを起動します。</span><span class="sxs-lookup"><span data-stu-id="708e1-109">Start the Dynamics 365 for Retail client.</span></span>
2. <span data-ttu-id="708e1-110">**小売** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売パラメーター**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="708e1-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3. <span data-ttu-id="708e1-111">**初期化**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="708e1-111">Click **Initialize**.</span></span>

<span data-ttu-id="708e1-112">初期化によって、次の既定のコンフィギュレーション データを作成します:</span><span class="sxs-lookup"><span data-stu-id="708e1-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="708e1-113">小売用スケジューラ ジョブとサブジョブ</span><span class="sxs-lookup"><span data-stu-id="708e1-113">Retail scheduler jobs and subjobs</span></span>
- <span data-ttu-id="708e1-114">小売チャンネル スキーマ</span><span class="sxs-lookup"><span data-stu-id="708e1-114">Retail channel schema</span></span>
- <span data-ttu-id="708e1-115">小売配送スケジュール</span><span class="sxs-lookup"><span data-stu-id="708e1-115">Retail distribution schedules</span></span>
- <span data-ttu-id="708e1-116">ボタン グリッドと画像、テーマを含む、既定の画面レイアウト</span><span class="sxs-lookup"><span data-stu-id="708e1-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="708e1-117">タイムゾーン情報</span><span class="sxs-lookup"><span data-stu-id="708e1-117">Time zone information</span></span>
- <span data-ttu-id="708e1-118">販売時点管理 (POS) 操作</span><span class="sxs-lookup"><span data-stu-id="708e1-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="708e1-119">POS アクセス許可</span><span class="sxs-lookup"><span data-stu-id="708e1-119">POS permissions</span></span>
- <span data-ttu-id="708e1-120">チャンネル レポート</span><span class="sxs-lookup"><span data-stu-id="708e1-120">Channel reports</span></span>
- <span data-ttu-id="708e1-121">属性メタデータ</span><span class="sxs-lookup"><span data-stu-id="708e1-121">Attribute metadata</span></span>
- <span data-ttu-id="708e1-122">エンティティ検証テンプレート</span><span class="sxs-lookup"><span data-stu-id="708e1-122">Entity validation templates</span></span>
- <span data-ttu-id="708e1-123">Commerce Data Exchange セッション履歴を削除するバッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="708e1-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="708e1-124">また、Payment Card Industry (PCI) に関連付けられるログが Dynamics 365 for Retail データベースに対して有効になります。</span><span class="sxs-lookup"><span data-stu-id="708e1-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span>

> [!NOTE]
> <span data-ttu-id="708e1-125">別々に小売用スケジューラをコンフィギュレーションするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="708e1-125">There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="708e1-126">このオプションで、小売用スケジューラのコンフィギュレーションを既定の設定にリセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="708e1-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span>

<span data-ttu-id="708e1-127">初期化の完了後に、追加の小売データをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="708e1-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="708e1-128">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="708e1-128">Here are some examples:</span></span>

- <span data-ttu-id="708e1-129">小売パラメーター</span><span class="sxs-lookup"><span data-stu-id="708e1-129">Retail parameters</span></span>
- <span data-ttu-id="708e1-130">小売用スケジューラのパラメーター</span><span class="sxs-lookup"><span data-stu-id="708e1-130">Retail scheduler parameters</span></span>
- <span data-ttu-id="708e1-131">小売チャンネル</span><span class="sxs-lookup"><span data-stu-id="708e1-131">Retail channels</span></span>
- <span data-ttu-id="708e1-132">レジスターとデバイス</span><span class="sxs-lookup"><span data-stu-id="708e1-132">Registers and devices</span></span>
- <span data-ttu-id="708e1-133">品揃え</span><span class="sxs-lookup"><span data-stu-id="708e1-133">Assortments</span></span>


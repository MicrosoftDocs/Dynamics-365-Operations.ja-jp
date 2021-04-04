---
title: RCS からの (ER) インポート構成
description: このトピックでは、ユーザーが RCS から ER 構成の新しいバージョンをインポートする方法を説明します。
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 799abeafe5f0929e6dd2f8a5f437f3c10b3b06d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570539"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="ef26a-103">RCS からの (ER) インポート構成</span><span class="sxs-lookup"><span data-stu-id="ef26a-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef26a-104">次の手順では、システム管理者または電子申告開発者ロールのユーザーが、Microsoft Regulatory Configuration Services (RCS) から新しいバージョンの電子申告 (ER) 構成をインポートする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="ef26a-105">この例では、RCS インスタンスで構成されている ER 構成のバージョンを選択して、Litware, Inc. というサンプル企業の現在のインスタンスにインポートします。ER 構成は会社間で共有されるため、これらの手順はすべての会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="ef26a-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="ef26a-106">これらの手順を完了するには、まず [コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) のトピックにある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef26a-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="ef26a-107">これらの手順を完了するには、**完了** または **共有** のステータスを持つ 1 つ以上の ER 構成を含む RCS インスタンスへのアクセスも必要です。</span><span class="sxs-lookup"><span data-stu-id="ef26a-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="ef26a-108">**組織管理** > **ワークスペース** > **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="ef26a-109">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ** としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="ef26a-110">このコンフィギュレーション プロバイダーが表示されない場合、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) というトピックの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef26a-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="ef26a-111">RCS 環境が自分の会社にプロビジョニングされていない場合は、外部リンク **Regulatory services – 構成** をクリックして、RCS 環境をプロビジョニングする指示に従います。</span><span class="sxs-lookup"><span data-stu-id="ef26a-111">If you have no RCS environment provisioned to your company, select **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="ef26a-112">**電子申告のパラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-112">Select **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="ef26a-113">**RCS** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef26a-113">Select the **RCS** tab.</span></span> 
6. <span data-ttu-id="ef26a-114">RCS 環境がすでに会社にプロビジョニングされている場合、表示されているページの URL を使ってアクセスします。</span><span class="sxs-lookup"><span data-stu-id="ef26a-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="ef26a-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef26a-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="ef26a-116">新しい ER リポジトリを登録します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="ef26a-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="ef26a-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="ef26a-118">Litware, Inc. プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="ef26a-119">リポジトリ を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-119">Select Repositories.</span></span> 
4. <span data-ttu-id="ef26a-120">追加を選択してドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="ef26a-120">Select Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="ef26a-121">構成リポジトリ タイプ フィールドで 'RCS' と入力します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="ef26a-122">レポジトリを作成を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-122">Select Create repository.</span></span> 
7. <span data-ttu-id="ef26a-123">RCS 環境表示名フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="ef26a-124">目的の RCS インスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-124">Select the desired RCS instance.</span></span> <span data-ttu-id="ef26a-125">複数のインスタンスがあることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ef26a-125">You can have several of them.</span></span> 
9. <span data-ttu-id="ef26a-126">OK を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-126">Select OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="ef26a-127">RCS ベースのリポジトリからの ER 構成のインポート</span><span class="sxs-lookup"><span data-stu-id="ef26a-127">Import ER configurations from RCS-based repository</span></span>
1. <span data-ttu-id="ef26a-128">**フィルタの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-128">Select **Show filters**.</span></span> 
2. <span data-ttu-id="ef26a-129">**次の値で始まる** フィルター演算子を使用して、**名前** フィールドにフィルター値 "RCS" を入力します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="ef26a-130">選択したリポジトリを開くには、**Regulatory Configuration Services への接続** ページで、**Regulatory Configuration Services に接続するには、ここを選択** のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, select **Select here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="ef26a-131">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-131">Select **Open**.</span></span> 
5. <span data-ttu-id="ef26a-132">**閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef26a-132">Select **Close**.</span></span> 
6. <span data-ttu-id="ef26a-133">ER 構成の目的のバージョンを選択、**インポート** を選択し、そのバージョンを現在のインスタンスにインポートします。</span><span class="sxs-lookup"><span data-stu-id="ef26a-133">Select the desired version of ER configuration and select **Import** to bring it in the current instance.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
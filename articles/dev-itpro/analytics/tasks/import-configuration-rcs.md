---
title: RCS からの (ER) インポート構成
description: このトピックでは、ユーザーが RCS から ER 構成の新しいバージョンをインポートする方法を説明します。
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c458cf815837fb7e4688c4c0443b7962cac403a5
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727009"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="f9c57-103">RCS からの (ER) インポート構成</span><span class="sxs-lookup"><span data-stu-id="f9c57-103">(ER) Import configurations from RCS</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9c57-104">次の手順では、システム管理者または電子申告開発者ロールのユーザーが、Microsoft Regulatory Configuration Services (RCS) から新しいバージョンの電子申告 (ER) 構成をインポートする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="f9c57-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="f9c57-105">この例では、RCS インスタンスで構成されている ER 構成のバージョンを選択して、Litware, Inc. というサンプル企業の現在の Finance and Operations インスタンスにインポートします。ER 構成は会社間で共有されるため、これらの手順はすべての会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="f9c57-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current Finance and Operations instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="f9c57-106">これらの手順を完了するには、まず[構成プロバイダーの作成およびび有効なプロバイダーとしてのマーク付け](er-configuration-provider-mark-it-active-2016-11.md) のトピックにある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9c57-106">To complete these steps, you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="f9c57-107">これらの手順を完了するには、**完了**または**共有**のステータスを持つ 1 つ以上の ER 構成を含む RCS インスタンスへのアクセスも必要です。</span><span class="sxs-lookup"><span data-stu-id="f9c57-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="f9c57-108">**組織管理** > **ワークスペース** > **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f9c57-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="f9c57-109">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ**としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f9c57-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="f9c57-110">この構成プロバイダーが表示されない場合は、[構成プロバイダーの作成および有効なプロバイダーとしてのマーク付け](er-configuration-provider-mark-it-active-2016-11.md) というトピックにある手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="f9c57-110">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="f9c57-111">RCS 環境が会社にプロビジョニングされていない場合は、外部リンク **Regulatory services ー 構成**をクリックして、RCS 環境をプロビジョニングする指示に従います。</span><span class="sxs-lookup"><span data-stu-id="f9c57-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="f9c57-112">**電子申告のパラメーター** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="f9c57-113">**RCS** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="f9c57-114">RCS 環境がすでに会社にプロビジョニングされている場合、表示されているページの URL を使ってアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="f9c57-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f9c57-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="f9c57-116">新しい ER リポジトリを登録します。</span><span class="sxs-lookup"><span data-stu-id="f9c57-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="f9c57-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="f9c57-118">Litware, Inc. プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9c57-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="f9c57-119">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-119">Click Repositories.</span></span> 
4. <span data-ttu-id="f9c57-120">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9c57-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="f9c57-121">構成リポジトリ タイプ フィールドで 'RCS' と入力します。</span><span class="sxs-lookup"><span data-stu-id="f9c57-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="f9c57-122">[リポジトリの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-122">Click Create repository.</span></span> 
7. <span data-ttu-id="f9c57-123">RCS 環境表示名フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f9c57-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="f9c57-124">目的の RCS インスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9c57-124">Select the desired RCS instance.</span></span> <span data-ttu-id="f9c57-125">複数のインスタンスがあることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f9c57-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="f9c57-126">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="f9c57-127">RCS ベースのリポジトリからの ER 構成のインポート</span><span class="sxs-lookup"><span data-stu-id="f9c57-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="f9c57-128">**フィルターの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="f9c57-129">**次の値で始まる**フィルター演算子を使用して、**名前**フィールドにフィルター値 "RCS" を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9c57-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="f9c57-130">選択したリポジトリを開くには、**Regulatory Configuration Services に接続する**ページで、**Regulatory Configuration Services に接続するには、ここをクリックしてください**のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="f9c57-131">**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-131">Click **Open**.</span></span> 
5. <span data-ttu-id="f9c57-132">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-132">Click **Close**.</span></span> 
6. <span data-ttu-id="f9c57-133">ER 構成の目的のバージョンを選択し、**インポート**をクリックし、そのバージョンを現在の Finance and Operations インスタンスにインポートします。</span><span class="sxs-lookup"><span data-stu-id="f9c57-133">Select the desired version of ER configuration and click **Import** to bring it in the current Finance and Operations instance.</span></span>


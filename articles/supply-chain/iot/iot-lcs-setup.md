---
title: LCS で IoT インテリジェンスをインストールする
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) に、IoT インテリジェンスをインストールする手順を説明します。
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386533"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="7929f-103">LCS で IoT インテリジェンスをインストールする</span><span class="sxs-lookup"><span data-stu-id="7929f-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7929f-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) に、IoT インテリジェンスをインストールする手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="7929f-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="7929f-105">アドインをインストールするには、事前に[Azure リソースを作成する ](iot-azure-setup.md)必要があります。</span><span class="sxs-lookup"><span data-stu-id="7929f-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="7929f-106">LCS 環境の設定</span><span class="sxs-lookup"><span data-stu-id="7929f-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="7929f-107">LCS を開いて、Microsoft Dynamics 365 Supply Chain Management 環境に移動します。</span><span class="sxs-lookup"><span data-stu-id="7929f-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="7929f-108">**環境アドイン**セクションまでスクロールします。</span><span class="sxs-lookup"><span data-stu-id="7929f-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="7929f-109">**新規アドインをインストールする**を選択して、環境に対して有効になっているアドインの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="7929f-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="7929f-110">**インストールするアドインの選択** ダイアログボックスで、**IoT インテリジェンス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7929f-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="7929f-111">**セットアップ アドイン** ダイアログ ボックスで、IoT ハブと Redis キャッシュの詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="7929f-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="7929f-112">必要となる値は、[Azureリソースの作成](iot-azure-setup.md) で作成した Key Vault で確認でき ます。</span><span class="sxs-lookup"><span data-stu-id="7929f-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="7929f-113">**テナント ID** – Azure ポータルで、Key Vault に移動し、左側のナビゲーションウィンドウで **概要** を選択して、**ディレクトリ ID**の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="7929f-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="7929f-114">コピーした値を **セットアップ アドイン** のダイアログ ボックスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7929f-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="7929f-115">**IoT イベントハブ - 互換エンドポイント Key Vault の URI** – Key Vault に移動し、続いて左側のナビゲーションウィンドウで **概要**を選択し、**DNS 名称**の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="7929f-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="7929f-116">コピーした値を **セットアップ アドイン** のダイアログ ボックスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7929f-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="7929f-117">**IoT イベント ハブ - 互換エンドポイントのシークレット名** – Key Vault に移動し、左側のナビゲーションウィンドウで **シークレット** を選択し、 IoT ハブが使用するイベント ハブの接続文字列が格納されているシークレット名をコピーします。</span><span class="sxs-lookup"><span data-stu-id="7929f-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="7929f-118">コピーした値を **セットアップ アドイン** のダイアログ ボックスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7929f-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="7929f-119">**Redis キャッシュ Key Vault の URI** – Key Vault に移動し、続いて左側のナビゲーションウィンドウで **概要**を選択し、**DNS 名称**の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="7929f-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="7929f-120">コピーした値を **セットアップ アドイン** のダイアログ ボックスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7929f-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="7929f-121">**Redis キャッシュ エンドポイントのシークレット名** – Key Vault に移動し、左側のナビゲーションウィンドウで **シークレット** を選択し、 Redis キャッシュが使用する接続文字列が格納されているシークレット名をコピーします。</span><span class="sxs-lookup"><span data-stu-id="7929f-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="7929f-122">コピーした値を **セットアップ アドイン** のダイアログ ボックスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7929f-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="7929f-123">条件に同意するには、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7929f-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="7929f-124">**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7929f-124">Select **Install**.</span></span>
8. <span data-ttu-id="7929f-125">"アドインのインストールが正常に開始されました" というメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7929f-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="7929f-126">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7929f-126">Select **OK**.</span></span>

<span data-ttu-id="7929f-127">以上で、LCS の設定が完了しました。</span><span class="sxs-lookup"><span data-stu-id="7929f-127">LCS setup is now completed.</span></span> <span data-ttu-id="7929f-128">次の手順では、[シナリオを設定](iot-scenario-setup.md)します。</span><span class="sxs-lookup"><span data-stu-id="7929f-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="7929f-129">アドインのアンインストール</span><span class="sxs-lookup"><span data-stu-id="7929f-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="7929f-130">Supply Chain Management で [シナリオを無効にします](iot-scenario-setup.md#how-to-disable-a-scenario)。</span><span class="sxs-lookup"><span data-stu-id="7929f-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="7929f-131">LCS で、Supply Chain Management 環境の詳細に移動します。</span><span class="sxs-lookup"><span data-stu-id="7929f-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="7929f-132">**環境アドイン**セクションまでスクロールします。</span><span class="sxs-lookup"><span data-stu-id="7929f-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="7929f-133">IoT インテリジェンス アドインの**アンインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7929f-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>

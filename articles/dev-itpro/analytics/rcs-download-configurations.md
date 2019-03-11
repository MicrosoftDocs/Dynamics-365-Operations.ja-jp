---
title: 規制コンフィギュレーション サービス (RCS) からの電子申告 (ER) 構成のインポート
description: このトピックは、規制コンフィギュレーション サービスから電子申告 (ER) コンフィギュレーションをインポートする方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 11/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionRepositoryTable
audience: IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 98ba483e67bd76e54ad1f85fa5f9cd736f7979a4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369595"
---
# <a name="import-electronic-reporting-er-configurations-from-regulatory-configuration-services-rcs"></a><span data-ttu-id="d3b9f-103">規制コンフィギュレーション サービス (RCS) からの電子申告 (ER) 構成のインポート</span><span class="sxs-lookup"><span data-stu-id="d3b9f-103">Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3b9f-104">規制コンフィギュレーション サービス (RCS) を使用すると電子申告 (ER) 構成をインポートできます。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-104">You can use Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="d3b9f-105">ER ツールは、1 つの会社用にプロビジョニングされた RCS の各インスタンスで構成されているコンフィギュレーションの一覧へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-105">The ER tool provides access to the list of configurations that have been configured in each instance of RCS that has been provisioned for your company.</span></span> <span data-ttu-id="d3b9f-106">この機能を使用して、Microsoft Dynamics 365 for Finance and Operations の現在のインスタンスに、RCS インスタンスで構成した構成をインポートできます。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-106">You can use this feature to import configurations that you configured in an RCS instance into the current instance of Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d3b9f-107">コンフィギュレーションをインポートした後、受信ドキュメントの処理や、送信電子ドキュメントの生成に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-107">After configurations are imported, they can be used to handle incoming documents or generate outgoing electronic documents.</span></span>

<span data-ttu-id="d3b9f-108">この機能の詳細を知るには、このトピックの例を実行します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-108">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="d3b9f-109">または、7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677) 業務プロセスの一部である **RCS からの ER インポート構成**タスク ガイドを再生します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-109">Alternatively, play the **ER Import configurations from RCS** task guide, which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="d3b9f-110">このタスク ガイドは [Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684)からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-110">This task guide can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="d3b9f-111">現在の Finance and Operations インスタンスに RCS インスタンスから ER コンフィギュレーションをインポートするプロセスを示します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-111">It walks you through the process of importing ER configurations from an RCS instance into the current Finance and Operations instance.</span></span>

## <a name="example-import-an-er-configuration-from-rcs"></a><span data-ttu-id="d3b9f-112">例: RCS からの ER コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="d3b9f-112">Example: Import an ER configuration from RCS</span></span>

<span data-ttu-id="d3b9f-113">この例では、システム管理者または電子報告開発者ロールのユーザーが RCS から ER コンフィギュレーションの新しいバージョンをインポートする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-113">This example shows how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an ER configuration from RCS.</span></span> <span data-ttu-id="d3b9f-114">この例では、RCS インスタンスで構成されている ER コンフィギュレーションの目的のバージョンを選択して、Litware, Inc. というサンプル企業の現在の Finance and Operations インスタンスにそのバージョンをインポートします。ER コンフィギュレーションは会社間で共有されるため、すべての会社でこれらの手順を完了することができます。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-114">In this example, you select the desired version of the ER configuration that has been configured in an RCS instance, and you import that version into the current Finance and Operations instance for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span>

<span data-ttu-id="d3b9f-115">この例の手順を完了するには、まず[コンフィギュレーションプロバイダーを作成し、それを有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md)にある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-115">To complete the steps in this example, you must first complete the steps in [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="d3b9f-116">**完了**または**共有**のステータスを持つ 1 つ以上の ER 構成を含む RCS インスタンスへのアクセスも必要です。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-116">You must also have access to an RCS instance that contains at least one ER configuration that has a status of either **Completed** or **Shared**.</span></span>

1. <span data-ttu-id="d3b9f-117">**組織管理  \> ワークスペース \> 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-117">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="d3b9f-118">**ローカライズのコンフィギュレーション** ページの **構成プロバイダー** セクションで、Litware, Inc. サンプル会社のコンフィギュレーション プロバイダーが一覧に表示されていること、および**アクティブ**とマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-118">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the configuration provider for the Litware, Inc. sample company is listed, and that it's marked as **Active**.</span></span> <span data-ttu-id="d3b9f-119">このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md)のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-119">If you don't see this configuration provider, follow the steps in [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="d3b9f-120">RCS 環境が会社に対してプロビジョニングされていない場合、**外部リンク** セクションの **規制サービス - 構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-120">If no RCS environment has been provisioned for your company, in the **External Links** section, select **Regulatory services – Configuration**.</span></span> <span data-ttu-id="d3b9f-121">次に、RCS 環境をプロビジョニングする指示に従います。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-121">Then follow the instructions to provision an RCS environment.</span></span>
4. <span data-ttu-id="d3b9f-122">**関連するリンク** セクションで、**電子申告のパラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-122">In the **Related links** section, select **Electronic reporting parameters**.</span></span>
5. <span data-ttu-id="d3b9f-123">**電子申告のパラメーター** ページで、**RCS** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-123">On the **Electronic reporting parameters** page, select the **RCS** tab.</span></span>
6. <span data-ttu-id="d3b9f-124">会社にプロビジョニングされた RCS 環境にアクセスするには、このタブの URL を使用します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-124">Use the URLs on this tab to access the RCS environment has been provisioned for your company.</span></span>
7. <span data-ttu-id="d3b9f-125">**電子申告のパラメーター** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-125">Close the **Electronic reporting parameters** page.</span></span>

### <a name="register-a-new-er-repository"></a><span data-ttu-id="d3b9f-126">新しい ER リポジトリの登録</span><span class="sxs-lookup"><span data-stu-id="d3b9f-126">Register a new ER repository</span></span>

1. <span data-ttu-id="d3b9f-127">**ローカライズのコンフィギュレーション** ページの一覧で **Litware, Inc.** コンフィギュレーション プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-127">On the **Localization configurations** page, select the **Litware, Inc.** configuration provider in the list.</span></span>
2. <span data-ttu-id="d3b9f-128">**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-128">Select **Repositories**.</span></span>
3. <span data-ttu-id="d3b9f-129">**追加** をクリックして、ドロップダウン ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-129">Select **Add** to open the drop-down dialog box.</span></span>
4. <span data-ttu-id="d3b9f-130">コンフィギュレーション リポジトリ タイプとして **RCS** を選択し、**リポジトリの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-130">Select **RCS** as the configuration repository type, and then select **Create repository**.</span></span>
6. <span data-ttu-id="d3b9f-131">**RCS 環境の表示名** フィールドで、目的の RCS インスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-131">In the **RCS environment display name** field, select the desired RCS instance.</span></span> <span data-ttu-id="d3b9f-132">複数のインスタンスがあることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-132">Note that you can have several instances.</span></span>
7. <span data-ttu-id="d3b9f-133"> *\*OK*\*を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-133">Select **OK**.</span></span>

### <a name="import-er-configurations-from-an-rcs-based-repository"></a><span data-ttu-id="d3b9f-134">RCS ベースのリポジトリからの ER コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="d3b9f-134">Import ER configurations from an RCS-based repository</span></span>

1. <span data-ttu-id="d3b9f-135">**コンフィギュレーション リポジトリ** ページで、ウィンドウの左側にある **フィルターの表示** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-135">On the **Configuration repositories** page, select the **Show filters** button on the left side of the window.</span></span>
2. <span data-ttu-id="d3b9f-136">**名前** フィルターで、フィルター演算子として **次の値で始まる** を選択し、フィルター値として **RCS** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-136">For the **Name** filter, select **begins with** as the filter operator, and then enter **RCS** as the filter value.</span></span>
3. <span data-ttu-id="d3b9f-137">リポジトリを選択し、開きます。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-137">Select the repository, and open it.</span></span>
3. <span data-ttu-id="d3b9f-138">**規制コンフィギュレーション サービスに接続する** ページで、**規制コンフィギュレーション サービスに接続するには、ここをクリックしてください** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-138">On the **Connect to Regulatory Configuration Services** page, select the **Click here to connect to Regulatory Configuration Services** link.</span></span>
4. <span data-ttu-id="d3b9f-139">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-139">Select **Open**.</span></span>
5. <span data-ttu-id="d3b9f-140">**閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-140">Select **Close**.</span></span>
6. <span data-ttu-id="d3b9f-141">ER コンフィギュレーションの目的のバージョンを選択し、**インポート** を選択しそのバージョンを Finance and Operations にインポートします。</span><span class="sxs-lookup"><span data-stu-id="d3b9f-141">Select the desired version of the ER configuration, and then select **Import** to import that version into Finance and Operations.</span></span>

## <a name="additional-resource"></a><span data-ttu-id="d3b9f-142">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="d3b9f-142">Additional resource</span></span>

- [<span data-ttu-id="d3b9f-143">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="d3b9f-143">Electronic reporting overview</span></span>](general-electronic-reporting.md)

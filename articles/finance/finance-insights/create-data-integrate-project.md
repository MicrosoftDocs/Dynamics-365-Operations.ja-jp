---
title: データ インテグレーター プロジェクトの作成 (プレビュー版)
description: このトピックでは、データインテ グレータープロジェクトの作成方法について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0029e093f524c61ff17a480ee3b881b3994ba95a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009451"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="73008-103">データ インテグレーター プロジェクトの作成 (プレビュー版)</span><span class="sxs-lookup"><span data-stu-id="73008-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="73008-104">このトピックでは、データインテ グレータープロジェクトの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="73008-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="73008-105">Microsoft Dynamics 365 Finance にサインインします。</span><span class="sxs-lookup"><span data-stu-id="73008-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="73008-106">**ワークスペース \> データ管理** に移動し、**データ エンティティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73008-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="73008-107">すべてのデータ エンティティが更新されるまで待機し、次のステップに進みます。</span><span class="sxs-lookup"><span data-stu-id="73008-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="73008-108">[Power Appsポータル](https://make.powerapps.com/)を開き、次 の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="73008-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="73008-109">適切な環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="73008-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="73008-110">左側のナビゲーション ペインで、**データ \> 接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73008-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="73008-111">次の項目の適切なインスタンスに接続します :</span><span class="sxs-lookup"><span data-stu-id="73008-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="73008-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="73008-112">Dynamics 365</span></span>
        - <span data-ttu-id="73008-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="73008-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="73008-114">[Power Apps 環境](https://admin.powerapps.com/environments)を開き、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="73008-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="73008-115">**データ インテグレーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73008-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="73008-116">**接続設定** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="73008-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="73008-117">**新規接続設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73008-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="73008-118">接続の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="73008-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="73008-119">次の項目に対して適切な接続を選択します。</span><span class="sxs-lookup"><span data-stu-id="73008-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="73008-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="73008-120">Dynamics 365</span></span>
        - <span data-ttu-id="73008-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="73008-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="73008-122">適切な組織のマッピングを選択します。</span><span class="sxs-lookup"><span data-stu-id="73008-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="73008-123">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73008-123">Select **Create**.</span></span>

5. <span data-ttu-id="73008-124">[Power Apps 環境](https://admin.powerapps.com/environments)を開き、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="73008-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="73008-125">作成した接続セットを使用して、次のテンプレートのデータ統合プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="73008-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="73008-126">顧客支払分析情報の結果 (CD から Fin と Ops)</span><span class="sxs-lookup"><span data-stu-id="73008-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="73008-127">キャッシュ フロー時系列の結果 (CD から Fin と Ops)</span><span class="sxs-lookup"><span data-stu-id="73008-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="73008-128">予算時系列の結果 (CD から Fin と Ops)</span><span class="sxs-lookup"><span data-stu-id="73008-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="73008-129">プロジェクトごとに適切なスケジューリングを設定します。</span><span class="sxs-lookup"><span data-stu-id="73008-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="73008-130">必要なエンティティが CDS に表示されない場合は、**与信と回収 > 設定 > Finance insights > Finance insights パラメーター** に移動し、顧客支払予測機能を有効にし、**予測モデルの作成** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="73008-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="73008-131">AI モデルの配置 (成功、失敗を問わない) が完了すると、統合の作成に必要な CDS エンティティが CDS にデプロイされます。</span><span class="sxs-lookup"><span data-stu-id="73008-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="73008-132">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="73008-132">Privacy notice</span></span>

<span data-ttu-id="73008-133">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="73008-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>

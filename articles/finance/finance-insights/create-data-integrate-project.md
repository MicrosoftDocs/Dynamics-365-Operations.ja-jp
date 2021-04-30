---
title: データ インテグレーター プロジェクトの作成 (プレビュー版)
description: このトピックでは、データインテ グレータープロジェクトの作成方法について説明します。
author: ShivamPandey-msft
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9ecf6ef7b7f052ebbb1201dcd04a7431f5b72ce5
ms.sourcegitcommit: b64c52d85aa6f110f3b1959a5521637dd8631b5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867450"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="0aeed-103">データ インテグレーター プロジェクトの作成 (プレビュー版)</span><span class="sxs-lookup"><span data-stu-id="0aeed-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="0aeed-104">このトピックでは、データインテ グレータープロジェクトの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="0aeed-105">Microsoft Dynamics 365 Finance にサインインします。</span><span class="sxs-lookup"><span data-stu-id="0aeed-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="0aeed-106">**ワークスペース \> データ管理** に移動し、**データ エンティティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="0aeed-107">すべてのデータ エンティティが更新されるまで待機し、次のステップに進みます。</span><span class="sxs-lookup"><span data-stu-id="0aeed-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="0aeed-108">[Power Appsポータル](https://make.powerapps.com/)を開き、次 の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="0aeed-109">適切な環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="0aeed-110">左側のナビゲーション ペインで、**データ \> 接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="0aeed-111">次の項目の適切なインスタンスに接続します :</span><span class="sxs-lookup"><span data-stu-id="0aeed-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="0aeed-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0aeed-112">Dynamics 365</span></span>
        - <span data-ttu-id="0aeed-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="0aeed-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="0aeed-114">[Power Apps 環境](https://admin.powerapps.com/environments)を開き、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="0aeed-115">**データ インテグレーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="0aeed-116">**接続設定** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="0aeed-117">**新規接続設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="0aeed-118">接続の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="0aeed-119">次の項目に対して適切な接続を選択します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="0aeed-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0aeed-120">Dynamics 365</span></span>
        - <span data-ttu-id="0aeed-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="0aeed-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="0aeed-122">適切な組織のマッピングを選択します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="0aeed-123">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-123">Select **Create**.</span></span>

5. <span data-ttu-id="0aeed-124">[Power Apps 環境](https://admin.powerapps.com/environments)を開き、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="0aeed-125">作成した接続セットを使用して、次のテンプレートのデータ統合プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="0aeed-126">顧客支払分析情報の結果 (CD から Fin と Ops)</span><span class="sxs-lookup"><span data-stu-id="0aeed-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="0aeed-127">バージョン 10.0.17 以降を使用している場合、顧客支払分析情報の結果 (CDS から Finance and Operations 10.0.17+) という名前のテンプレートを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0aeed-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="0aeed-128">キャッシュ フロー時系列の結果 (CD から Fin と Ops)</span><span class="sxs-lookup"><span data-stu-id="0aeed-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="0aeed-129">予算時系列の結果 (CD から Fin と Ops)</span><span class="sxs-lookup"><span data-stu-id="0aeed-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="0aeed-130">プロジェクトごとに適切なスケジューリングを設定します。</span><span class="sxs-lookup"><span data-stu-id="0aeed-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="0aeed-131">必要なエンティティが CDS に表示されない場合は、**与信と回収 > 設定 > Finance insights > Finance insights パラメーター** に移動し、顧客支払予測機能を有効にし、**予測モデルの作成** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0aeed-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="0aeed-132">AI モデルの配置 (成功、失敗を問わない) が完了すると、統合の作成に必要な CDS エンティティが CDS にデプロイされます。</span><span class="sxs-lookup"><span data-stu-id="0aeed-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="0aeed-133">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="0aeed-133">Privacy notice</span></span>

<span data-ttu-id="0aeed-134">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="0aeed-134">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

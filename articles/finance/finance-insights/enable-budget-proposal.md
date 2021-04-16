---
title: 予算案の有効化 (プレビュー)
description: このトピックでは、財務インサイトの予算案機能を有効にする方法について説明します。
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
ms.openlocfilehash: 7e90a1a2f2a8e7808f03ce9a6ee58c027bd48d8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818707"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="73b98-103">予算案の有効化 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="73b98-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="73b98-104">このトピックでは、財務インサイトの予算案機能を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="73b98-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="73b98-105">Microsoft Dynamics Lifecycle Services (LCS) で環境ページの情報を使用して、その環境に対する Azure SQL のプライマリ インスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="73b98-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="73b98-106">次の Transact-SQL (T-SQL) コマンドを実行して、サンドボックス環境のフライトを有効にします。</span><span class="sxs-lookup"><span data-stu-id="73b98-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="73b98-107">(Application Object Server \[AOS\] にリモートで接続する前に、LCS で IP アドレスに対してアクセスを有効にする必要がある場合があります。)</span><span class="sxs-lookup"><span data-stu-id="73b98-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="73b98-108">Microsoft Dynamics 365 Finance の配置が Service Fabric 配置である場合は、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="73b98-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="73b98-109">財務インサイト チームは既にフライトを有効にしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="73b98-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="73b98-110">**機能管理** ワークスペースに機能が表示されない場合、または有効にしようとしたときに問題が発生した場合は、[財務インサイト アプリ プレビュー チーム](mailto:fiap@microsoft.com) に電子メールを送信してください。</span><span class="sxs-lookup"><span data-stu-id="73b98-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="73b98-111">**機能管理** ワークスペースを開き、次の手順に従います:</span><span class="sxs-lookup"><span data-stu-id="73b98-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="73b98-112">**更新プログラムの確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73b98-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="73b98-113">**予算案** を検索し、その機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="73b98-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="73b98-114">**予算作成 \>設定 \> 基本予算作成 \> 予算案 (プレビュー)** に移動して、**機能の有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73b98-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="73b98-115">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="73b98-115">Privacy notice</span></span>
<span data-ttu-id="73b98-116">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="73b98-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
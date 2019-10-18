---
title: オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション
description: このトピックでは、オンプレミス配置の SQL Server Reporting Services (SSRS) のコンフィギュレーションに関する情報が提供されます。
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: bb6e8a55c9bee4e60c3a627409d2fbe3b8915196
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174239"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a><span data-ttu-id="0b8cc-103">オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="0b8cc-103">Configure SQL Server Reporting Services for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b8cc-104">このトピックの手順を使用して、Microsoft Dynamics 365 Finance + Operations のオンプレミス配置に SQL Server Reporting Services (SSRS) を構成します。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 Finance + Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="0b8cc-105">SQL Reporting Services Configuration Manager アプリケーションを開きます。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="0b8cc-106">**サーバー名**を既定のままにし、現在のコンピューターの名前、および**レポート サーバーのインスタンス**、**MSSQLSERVER** にします。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span>
3. <span data-ttu-id="0b8cc-107">**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-107">Click **Connect**.</span></span>

    <span data-ttu-id="0b8cc-108">[![サービス コンフィグレーション コネクションのレポート](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>

4. <span data-ttu-id="0b8cc-109">**サービス アカウント**タブをクリックし、設定が次の図と一致しているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="0b8cc-110">[![サービス アカウント タブ](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>

5. <span data-ttu-id="0b8cc-111">**Web サービス URL** タブをクリックし、設定が次の図と一致しているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="0b8cc-112">[![Web サービス URL タブ](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span>

6. <span data-ttu-id="0b8cc-113">**データベース**タブをクリックし、**データベース名**および**資格情報の設定**が次の図と一致しているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b8cc-114">新しいデータベースを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-114">You will need to create a new database.</span></span> <span data-ttu-id="0b8cc-115">これを行うには**データベースの変更**をクリックし、新しいデータベース名が **DynamicsAxReportServer** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="0b8cc-116">[![データベース タブ](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>

7. <span data-ttu-id="0b8cc-117">**Web ポータル URL** タブをクリックし、設定が次の図と一致しているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b8cc-118">**適用**をクリックし、ポータルの作成および適切なコンフィギュレーションを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-118">You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="0b8cc-119">[![web ポータル url タブ](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>

    <span data-ttu-id="0b8cc-120">ポータルを設定すると、**Web ポータル**タブは次の図と一致するようになります。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>

    <span data-ttu-id="0b8cc-121">[![web ポータル タブ](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>

8. <span data-ttu-id="0b8cc-122">レポートの URL をクリックし、SQL Server Reporting Services web ポータルを表示します。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span>
9. <span data-ttu-id="0b8cc-123">ポータルにアクセスしたら、**Dynamics** という名前の新規フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="0b8cc-124">[![ダイナミクス フォルダー](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>

10. <span data-ttu-id="0b8cc-125">**Reporting Services 構成マネージャー** で**電子メール設定**タブをクリックし、設定が次の図に一致しているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="0b8cc-126">[![電子メール設定タブ](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>

11. <span data-ttu-id="0b8cc-127">**実行アカウント**タブをクリックし、設定が次の図と一致しているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="0b8cc-128">[![実行アカウント タブ](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>

    <span data-ttu-id="0b8cc-129">**暗号化キー** タブでは既定の設定を変更しません。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-129">Don't change the default settings on the **Encryption Keys** tab.</span></span>

    <span data-ttu-id="0b8cc-130">[![暗号化キー タブ](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>

12. <span data-ttu-id="0b8cc-131">**定期売買の設定**タブをクリックし、設定が次の図と一致しているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="0b8cc-132">[![定期売買の設定タブ](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>

    <span data-ttu-id="0b8cc-133">**スケール アウト配置**タブでは既定の設定を変更しません。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-133">Don't change the default settings on the **Scale-out Deployment** tab.</span></span>

    <span data-ttu-id="0b8cc-134">[![スケール アウト配置タブ](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>

    <span data-ttu-id="0b8cc-135">**Power BI 統合**タブで既定の設定を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-135">Don't change the default settings on the **Power BI Integration** tab.</span></span>

    <span data-ttu-id="0b8cc-136">[![Power BI 統合タブ](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span>

13. <span data-ttu-id="0b8cc-137">**終了**をクリックし、**Reporting Services 構成マネージャー**を閉じます。</span><span class="sxs-lookup"><span data-stu-id="0b8cc-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="0b8cc-138">[![reporting services 構成マネージャーの終了](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="0b8cc-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
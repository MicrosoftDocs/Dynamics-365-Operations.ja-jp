---
title: "AX 2012 からのアップグレード - アップグレード後に完了するタスク"
description: "このトピックでは、Microsoft Dynamics AX 2012 からコードとデータのアップグレードを完了した後に、Microsoft Dynamics 365で実行する必要のある作業について説明します。"
author: tariqbell
manager: AnnBe
ms.date: 01/31/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 106163
ms.assetid: 
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 592dc6298170c68c78b32f047884b5e2861f32ff
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="upgrade-from-ax-2012---tasks-to-complete-after-upgrade"></a><span data-ttu-id="b42b5-103">AX 2012 からのアップグレード - アップグレード後に完了するタスク</span><span class="sxs-lookup"><span data-stu-id="b42b5-103">Upgrade from AX 2012 - Tasks to complete after upgrade</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="b42b5-104">このトピックでは、Microsoft Dynamics AX 2012 からコードとデータのアップグレードを完了した後に、Microsoft Dynamics 365で実行する必要のある作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="b42b5-104">This topic describes the tasks that you might have to perform in Microsoft Dynamics 365 for Operation after you complete a code and data upgrade from Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="b42b5-105">Microsoft Dynamics Lifecycle Services (LCS) で使用可能なプロセス データ パッケージ (PDP) には、次のメニュー項目へのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b42b5-105">A process data package (PDP) that is available in Microsoft Dynamics Lifecycle Services (LCS) includes links to the following menu items.</span></span> <span data-ttu-id="b42b5-106">この PDP は、**データ検証チェックリスト** ワークスペースに入力します。</span><span class="sxs-lookup"><span data-stu-id="b42b5-106">This PDP will fill in the **Data validation checklist** workspace.</span></span> <span data-ttu-id="b42b5-107">**データ検証チェックリスト** ワークスペースでは、ユーザーがプロジェクトを追跡し、それを実行するために必要なタスクを監視できます。</span><span class="sxs-lookup"><span data-stu-id="b42b5-107">The **Data validation checklist** workspace lets users track a project and monitor the tasks that are required in order to complete it.</span></span>

## <a name="document-management"></a><span data-ttu-id="b42b5-108">ドキュメント管理</span><span class="sxs-lookup"><span data-stu-id="b42b5-108">Document management</span></span>

<span data-ttu-id="b42b5-109">ドキュメント管理を使用する場合は、データベースに格納されている既存のドキュメントまたは添付ファイルを Microsoft Azure Blob ストレージに移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b42b5-109">If you use Document management, existing documents or attachments that are stored in the database must be migrated to Microsoft Azure Blob storage.</span></span> <span data-ttu-id="b42b5-110">この移行を完了するには、**ドキュメント管理パラメーター** ページの **ファイルを移行** タブで **ファイルを移行** ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="b42b5-110">To complete this migration, use the **Migrate files** button on the **Migrate files** tab on the **Document management parameters** page.</span></span>

## <a name="print-management"></a><span data-ttu-id="b42b5-111">印刷管理</span><span class="sxs-lookup"><span data-stu-id="b42b5-111">Print management</span></span>

<span data-ttu-id="b42b5-112">印刷管理を使用する場合、AX 2012 のネットワーク プリンタへの参照は無効になります。</span><span class="sxs-lookup"><span data-stu-id="b42b5-112">If you use Print management, the references to network printers from AX 2012 won’t be valid.</span></span> <span data-ttu-id="b42b5-113">**ドキュメント回覧** ページのネットワーク プリンターを設定して参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b42b5-113">You must set up and reference network printers on the **Document routing** page.</span></span> <span data-ttu-id="b42b5-114">詳細については、[ネットワーク プリンター デバイスを有効にするためにドキュメント回覧エージェントをインストールする](../analytics/install-document-routing-agent.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b42b5-114">For more information, see [Install the Document Routing Agent to enable network printer devices](../analytics/install-document-routing-agent.md).</span></span>

## <a name="retail"></a><span data-ttu-id="b42b5-115">Retail</span><span class="sxs-lookup"><span data-stu-id="b42b5-115">Retail</span></span>

<span data-ttu-id="b42b5-116">AX 2012 からアップグレードを完了すると、レジスターおよびデバイスを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b42b5-116">After you complete the upgrade from AX 2012, you must configure registers and devices.</span></span>

<span data-ttu-id="b42b5-117">レジスターを構成するには、**Retail** > **チャネル** > **小売店舗** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b42b5-117">To configure a register, click **Retail** > **Channels** > **Retail stores**.</span></span> <span data-ttu-id="b42b5-118">小売チャネルの行を選択し、**レジスター** 情報ボックスを展開します。</span><span class="sxs-lookup"><span data-stu-id="b42b5-118">Select the row for the retail channel, and then expand the **Registers** FactBox.</span></span> <span data-ttu-id="b42b5-119">**詳細**をクリックし、**新規**をクリックして、登録設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="b42b5-119">Click **More**, click **New**, and complete the setup of the register.</span></span>

<span data-ttu-id="b42b5-120">デバイスを構成するには、**Retail** > **チャンネル設定** > **POS 設定** をクリックし、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b42b5-120">To configure a device, click **Retail** > **Channel setup** > **POS Setup**, and then click **New**.</span></span>

<span data-ttu-id="b42b5-121">また、チャネル データベースのすべてのジョブ (9999) を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b42b5-121">Additionally, you must run all jobs (9999) for the channel database.</span></span> <span data-ttu-id="b42b5-122">**小売** > **本社の設定** > **小売用スケジューラ** > **チャネル データベース**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="b42b5-122">Click **Retail** > **Headquarters setup** > **Retail scheduler** > **Channel database**.</span></span> <span data-ttu-id="b42b5-123">適切なチャネル データベースの行を選択し、**データの完全な同期** をクリックします。**9999** (**すべてのジョブ**) 配送スケジュールを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b42b5-123">Select the row for the appropriate channel database, and then click **Full data sync**. Select the **9999** (**All jobs**) distribution schedule, and then click **OK**.</span></span> <span data-ttu-id="b42b5-124">ジョブを実行するには、もう一度 **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b42b5-124">Click **OK** again to run the job.</span></span>

## <a name="service-industries"></a><span data-ttu-id="b42b5-125">サービス業</span><span class="sxs-lookup"><span data-stu-id="b42b5-125">Service industries</span></span>

<span data-ttu-id="b42b5-126">AX 2012 からアップグレードを完了した後は、リソース キャパシティ ロールアップおよびプロジェクト元帳の会社間転記を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b42b5-126">After you complete the upgrade from AX 2012, you must set up resource capacity roll-up and project ledger intercompany posting.</span></span>

<span data-ttu-id="b42b5-127">リソース キャパシティのロールアップ バッチ ジョブを実行するには、**プロジェクト管理と会計** > **照会とレポート** > **キャパシティ同期** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b42b5-127">To run the Resource capacity roll-up batch job, click **Project management and accounting** > **Inquiries and reports** > **Capacity synchronization**.</span></span> <span data-ttu-id="b42b5-128">リソースおよびリソース カレンダーの予約データを設定するには、このバッチ ジョブを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b42b5-128">You must run this batch job to set up the resource and resource calendar reservation data.</span></span> <span data-ttu-id="b42b5-129">このデータは、プロジェクト リソースのスケジューリングを使用する場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="b42b5-129">This data will be required if you use project resource scheduling.</span></span> <span data-ttu-id="b42b5-130">詳細については、「[プロジェクト リソース](../../financials/project-management/project-resourcing.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b42b5-130">For more information, see [Project resourcing](../../financials/project-management/project-resourcing.md).</span></span>

<span data-ttu-id="b42b5-131">プロジェクト元帳の企業間転記を有効にするには、**プロジェクト管理と会計** > **設定** > **転記** > **元帳転記の設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b42b5-131">To enable project ledger intercompany posting, click **Project management and accounting** > **Setup** > **Posting** > **Ledger posting setup**.</span></span> <span data-ttu-id="b42b5-132">**原価会計**タブの、**勘定タイプ**フィールドで、**会社間原価**、および貸出側法人の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="b42b5-132">On the **Cost accounts** tab, in the **Ledger account types** field, select **Intercompany cost**, and then enter the details of the lending legal entity.</span></span> <span data-ttu-id="b42b5-133">**収益勘定**タブの、**勘定タイプ**フィールドで、**会社間収益**、および貸出側法人の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="b42b5-133">On the **Revenue accounts** tab, in the **Ledger account types** field, select **Intercompany revenue**, and then enter details of the borrowing legal entity.</span></span>

## <a name="budget-planning"></a><span data-ttu-id="b42b5-134">予算計画</span><span class="sxs-lookup"><span data-stu-id="b42b5-134">Budget planning</span></span>

<span data-ttu-id="b42b5-135">AX 2012 からのアップグレードが完了した後、予算計画の列とレイアウトを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b42b5-135">After you complete the upgrade from AX 2012, you must set up Budget planning columns and layouts.</span></span> <span data-ttu-id="b42b5-136">この設定を完了するには、**予算編成** > **設定** > **予算計画** > **予算計画構成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b42b5-136">To complete this setup, click **Budgeting** > **Setup** > **Budget planning** > **Budget planning configuration**.</span></span>

<span data-ttu-id="b42b5-137">また、各予算ステージに適切なレイアウトを使用するための予算計画プロセスを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b42b5-137">Additionally, you must update Budget planning processes so that they use the appropriate layout for each budget stage.</span></span> <span data-ttu-id="b42b5-138">予算計画プロセスを更新するには、**予算作成** > **設定** > **予算計画** > **予算計画プロセス**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b42b5-138">To update Budget planning processes, click **Budgeting** > **Setup** > **Budget planning** > **Budget planning process**.</span></span>

<span data-ttu-id="b42b5-139">予算計画のアップグレードの詳細については、[Microsoft Dynamics AX 2012 から予算計画にアップグレードする](upgrade-budget-planning.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b42b5-139">For more information about Budget planning upgrade, see [Upgrading to Budget planning from Microsoft Dynamics AX 2012](upgrade-budget-planning.md).</span></span>


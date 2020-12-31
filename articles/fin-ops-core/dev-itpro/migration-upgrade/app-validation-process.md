---
title: AX 2012 からのアップグレード - アップグレード後のタスク
description: このトピックでは、Microsoft Dynamics AX 2012 からコードとデータのアップグレードを完了した後に、Finance and Operations アプリで実行する必要があるタスクについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 11/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 106163
ms.assetid: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: f996ee91abe3ad4d35253d2a6e8fd359611d9c5f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683480"
---
# <a name="upgrade-from-ax-2012---post-upgrade-tasks"></a><span data-ttu-id="2310a-103">AX 2012 からのアップグレード - アップグレード後のタスク</span><span class="sxs-lookup"><span data-stu-id="2310a-103">Upgrade from AX 2012 - Post-upgrade tasks</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="2310a-104">このトピックでは、Microsoft Dynamics AX 2012 からコードとデータのアップグレードを完了した後に、Dynamics 365 Finance や Dynamics 365 Supply Chain Management などの Finance and Operations アプリで実行する必要があるタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2310a-104">This topic describes the tasks that you might have to perform in Finance and Operations apps, like Dynamics 365 Finance and Dynamics 365 Supply Chain Management, after you complete a code and data upgrade from Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="2310a-105">Microsoft Dynamics Lifecycle Services (LCS) で使用可能なプロセス データ パッケージ (PDP) には、次のメニュー項目へのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2310a-105">A process data package (PDP) that is available in Microsoft Dynamics Lifecycle Services (LCS) includes links to the following menu items.</span></span> <span data-ttu-id="2310a-106">この PDP は、**データ検証チェックリスト** ワークスペースに入力します。</span><span class="sxs-lookup"><span data-stu-id="2310a-106">This PDP will fill in the **Data validation checklist** workspace.</span></span> <span data-ttu-id="2310a-107">**データ検証チェックリスト** ワークスペースでは、ユーザーがプロジェクトを追跡し、それを実行するために必要なタスクを監視できます。</span><span class="sxs-lookup"><span data-stu-id="2310a-107">The **Data validation checklist** workspace lets users track a project and monitor the tasks that are required in order to complete it.</span></span>

## <a name="document-management"></a><span data-ttu-id="2310a-108">ドキュメント管理</span><span class="sxs-lookup"><span data-stu-id="2310a-108">Document management</span></span>

<span data-ttu-id="2310a-109">ドキュメント管理を使用する場合は、データベースに格納されている既存のドキュメントや添付ファイルを Microsoft Azure Blob ストレージに移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2310a-109">If you use document management, existing documents or attachments that are stored in the database should be migrated to Microsoft Azure Blob storage.</span></span> <span data-ttu-id="2310a-110">この移行を完了するには、**ドキュメント管理パラメーター** ページの **ファイルを移行** タブで **ファイルを移行** ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="2310a-110">To complete this migration, use the **Migrate files** button on the **Migrate files** tab on the **Document management parameters** page.</span></span> <span data-ttu-id="2310a-111">ドキュメント管理ではデータベースに格納されているファイルに引き続きアクセスできるため、この操作は重要ではありませんが、ファイルはかなりのデータベース記憶域を消費する可能性があり、取得の効率が低下します。</span><span class="sxs-lookup"><span data-stu-id="2310a-111">This operation is not critical as document management can still access file stored in the database, but the files can take considerable database storage and the retrieval is less efficient.</span></span> <span data-ttu-id="2310a-112">ファイル移行プロセスでは、可能性のあるすべてのデータベースファイルが Microsoft Azure Blob ストレージ に移行されます。発生したエラーは報告され、処理は続行されます。</span><span class="sxs-lookup"><span data-stu-id="2310a-112">The file migration process will migrate all possible database files to Microsoft Azure Blob storage, reporting on any failures and continuing.</span></span> <span data-ttu-id="2310a-113">エラーが報告された場合は、ファイル移行プロセスを再度実行します。</span><span class="sxs-lookup"><span data-stu-id="2310a-113">If any errors are reported, attempt running the file migration process again.</span></span>

<span data-ttu-id="2310a-114">ファイルの移行プロセスが正常に完了しない場合、データベースに保存されているファイルに Microsoft が修復できない損傷があることが考えられます。</span><span class="sxs-lookup"><span data-stu-id="2310a-114">If the file migration process isn’t able to complete without failure, this may be that the files stored in the database are corrupt, which Microsoft is unable to repair.</span></span> <span data-ttu-id="2310a-115">その場合は、業務に不可欠とならないサポート案件を開いて、添付ファイルをメモ レコードに変換できるようにすることができます。これにより、以前のメモとデータベースに保存されたファイルの名前が保持されます。</span><span class="sxs-lookup"><span data-stu-id="2310a-115">If this is the case, you can request a non-business critical support case be opened to enable conversion of the attachments into note records, which will retain any previous notes as well as the names of the files that were stored in the database.</span></span> <span data-ttu-id="2310a-116">ファイル自体の回復はできないことに留意してください。</span><span class="sxs-lookup"><span data-stu-id="2310a-116">Note that the files themselves cannot be recovered.</span></span>

## <a name="print-management"></a><span data-ttu-id="2310a-117">印刷管理</span><span class="sxs-lookup"><span data-stu-id="2310a-117">Print management</span></span>

<span data-ttu-id="2310a-118">印刷管理を使用する場合、AX 2012 のネットワーク プリンタへの参照は無効になります。</span><span class="sxs-lookup"><span data-stu-id="2310a-118">If you use Print management, the references to network printers from AX 2012 won’t be valid.</span></span> <span data-ttu-id="2310a-119">**ドキュメント回覧** ページのネットワーク プリンターを設定して参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2310a-119">You must set up and reference network printers on the **Document routing** page.</span></span> <span data-ttu-id="2310a-120">詳細については、 [ドキュメント ルーティング エージェントをインストールしてネットワーク印刷を有効にする](../analytics/install-document-routing-agent.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2310a-120">For more information, see [Install the Document Routing Agent to enable network printing](../analytics/install-document-routing-agent.md).</span></span>

## <a name="commerce"></a><span data-ttu-id="2310a-121">Commerce</span><span class="sxs-lookup"><span data-stu-id="2310a-121">Commerce</span></span>

<span data-ttu-id="2310a-122">AX 2012 からアップグレードを完了すると、レジスターおよびデバイスを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2310a-122">After you complete the upgrade from AX 2012, you must configure registers and devices.</span></span>

<span data-ttu-id="2310a-123">レジスターを構成するには、**Retail と Commerce** > **チャネル** > **店舗** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2310a-123">To configure a register, click **Retail and Commerce** > **Channels** > **Stores**.</span></span> <span data-ttu-id="2310a-124">チャネルの行を選択し、次に **レジスター** 情報ボックスを展開します。</span><span class="sxs-lookup"><span data-stu-id="2310a-124">Select the row for the channel, and then expand the **Registers** FactBox.</span></span> <span data-ttu-id="2310a-125">**詳細** をクリックし、**新規** をクリックして、登録設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="2310a-125">Click **More**, click **New**, and complete the setup of the register.</span></span>

<span data-ttu-id="2310a-126">デバイスを構成するには、**Retail と Commerce** > **チャンネル設定** > **POS 設定** をクリックし、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2310a-126">To configure a device, click **Retail and Commerce** > **Channel setup** > **POS Setup**, and then click **New**.</span></span>

<span data-ttu-id="2310a-127">また、チャネル データベースのすべてのジョブ (9999) を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2310a-127">Additionally, you must run all jobs (9999) for the channel database.</span></span> <span data-ttu-id="2310a-128">**Retail と Commerce** > **Headquarters の設定** > **Commerce スケジューラ** > **チャネル データベース** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="2310a-128">Click **Retail and Commerce** > **Headquarters setup** > **Commerce scheduler** > **Channel database**.</span></span> <span data-ttu-id="2310a-129">適切なチャネル データベースの行を選択し、**データの完全な同期** をクリックします。**9999** (**すべてのジョブ**) 配送スケジュールを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2310a-129">Select the row for the appropriate channel database, and then click **Full data sync**. Select the **9999** (**All jobs**) distribution schedule, and then click **OK**.</span></span> <span data-ttu-id="2310a-130">ジョブを実行するには、もう一度 **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2310a-130">Click **OK** again to run the job.</span></span>

## <a name="service-industries"></a><span data-ttu-id="2310a-131">サービス業</span><span class="sxs-lookup"><span data-stu-id="2310a-131">Service industries</span></span>

<span data-ttu-id="2310a-132">AX 2012 からアップグレードを完了した後は、リソース キャパシティ ロールアップおよびプロジェクト元帳の会社間転記を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2310a-132">After you complete the upgrade from AX 2012, you must set up resource capacity roll-up and project ledger intercompany posting.</span></span>

<span data-ttu-id="2310a-133">リソース キャパシティのロールアップ バッチ ジョブを実行するには、**プロジェクト管理と会計** > **照会とレポート** > **キャパシティ同期** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2310a-133">To run the Resource capacity roll-up batch job, click **Project management and accounting** > **Inquiries and reports** > **Capacity synchronization**.</span></span> <span data-ttu-id="2310a-134">リソースおよびリソース カレンダーの予約データを設定するには、このバッチ ジョブを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2310a-134">You must run this batch job to set up the resource and resource calendar reservation data.</span></span> <span data-ttu-id="2310a-135">このデータは、プロジェクト リソースのスケジューリングを使用する場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="2310a-135">This data will be required if you use project resource scheduling.</span></span> <span data-ttu-id="2310a-136">詳細については、「[プロジェクト リソース](../../../finance/project-management/project-resourcing.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2310a-136">For more information, see [Project resourcing](../../../finance/project-management/project-resourcing.md).</span></span>

<span data-ttu-id="2310a-137">プロジェクト元帳の企業間転記を有効にするには、**プロジェクト管理と会計** > **設定** > **転記** > **元帳転記の設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2310a-137">To enable project ledger intercompany posting, click **Project management and accounting** > **Setup** > **Posting** > **Ledger posting setup**.</span></span> <span data-ttu-id="2310a-138">**原価会計** タブの、**勘定タイプ** フィールドで、**会社間原価**、および貸出側法人の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="2310a-138">On the **Cost accounts** tab, in the **Ledger account types** field, select **Intercompany cost**, and then enter the details of the lending legal entity.</span></span> <span data-ttu-id="2310a-139">**収益勘定** タブの、**勘定タイプ** フィールドで、**会社間収益**、および貸出側法人の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="2310a-139">On the **Revenue accounts** tab, in the **Ledger account types** field, select **Intercompany revenue**, and then enter details of the borrowing legal entity.</span></span>

## <a name="budget-planning"></a><span data-ttu-id="2310a-140">予算計画</span><span class="sxs-lookup"><span data-stu-id="2310a-140">Budget planning</span></span>

<span data-ttu-id="2310a-141">AX 2012 からのアップグレードが完了した後、予算計画の列とレイアウトを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2310a-141">After you complete the upgrade from AX 2012, you must set up Budget planning columns and layouts.</span></span> <span data-ttu-id="2310a-142">この設定を完了するには、**予算編成** > **設定** > **予算計画** > **予算計画構成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2310a-142">To complete this setup, click **Budgeting** > **Setup** > **Budget planning** > **Budget planning configuration**.</span></span>

<span data-ttu-id="2310a-143">また、各予算ステージに適切なレイアウトを使用するための予算計画プロセスを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2310a-143">Additionally, you must update Budget planning processes so that they use the appropriate layout for each budget stage.</span></span> <span data-ttu-id="2310a-144">予算計画プロセスを更新するには、**予算作成** > **設定** > **予算計画** > **予算計画プロセス** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2310a-144">To update Budget planning processes, click **Budgeting** > **Setup** > **Budget planning** > **Budget planning process**.</span></span>

<span data-ttu-id="2310a-145">予算計画の更新に関する詳細については、 [予算計画の更新](upgrade-budget-planning.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2310a-145">For more information about Budget planning upgrade, see [Upgrade budget planning](upgrade-budget-planning.md).</span></span>
